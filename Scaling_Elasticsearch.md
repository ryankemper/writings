### How we scaled Elasticsearch to handle 1.4 TB of logs per day

#### Understanding Elasticsearch

[] Describe interaction between nodes/shards/indices

[] Go into lucene internals, show our diagram of how ES concepts map to Lucene concepts (e.g. Elasticsearch shard = Lucene index)


#### Outline of our configuration history

- Configuration Zero: Two index types, "job" and "everything else", job had no replicas
    * Indices a little bit too big

- Configuration One: Filebeat->Kafka->Logstash->Elasticsearch
    * Filebeat feeds into Kafka. Inclusion of Kafka means no longer dropping logs
    * Create separate Elasticsearch index per Kafka topic (side effect: orders of magnitude variance in index size)

    ^ Combination of no longer dropping logs + kafka topic<->ES index => cluster cannot handle this volume

- Final Configuration: Filebeat->Kafka->Logstash->Elasticsearch
    * Filebeat feeds into Kafka.
    * One daily index with as many shards as necessary to get the right size shards

#### What we look for in a healthy cluster

- Memory usage should be fluctuating around the 75% threshold. Look for a "sawtooth" pattern where memory approaches 75%, decreases as concurrent mark sweep garbage collection kicks in,


#### Context on final configuration

The current approach is dead simple - we just have an index for a day's logs, split up into 128 primary shards, with a replication factor of 1. The primary/replica shard count was chosen such that we make optimal use of our physical resources, while keeping shards between 10-50GB.
Hardware-wise, we just moved to 8 i3.8xlarge.elasticsearch nodes, which gives us 256 VCPU's and 1952 GB of ram, with a total of 32 NVMe SSDs.
With the above settings, that gives us ~16 GB shards, with 256 shards per day. So if searching across a single index (day) of logs, we've got exactly 1 vCPU per shard.
