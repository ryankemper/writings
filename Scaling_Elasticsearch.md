How we scaled Elasticsearch to handle 1.4 TB of logs per day

- Configuration Zero: Two index types, "job" and "everything else", job had no replicas
    * Indices a little bit too big

- Configuration One: Filebeat->Kafka->Logstash->Elasticsearch
    * Filebeat feeds into Kafka. Inclusion of Kafka means no longer dropping logs
    * Create separate Elasticsearch index per Kafka topic (side effect: orders of magnitude variance in index size)

- Final Configuration: Filebeat->Kafka->Logstash->Elasticsearch
    * Filebeat feeds into Kafka.
    * One daily index with as many shards as necessary to get the right size shards

The current approach is dead simple - we just have an index for a day's logs, split up into 128 primary shards, with a replication factor of 1. The primary/replica shard count was chosen such that we make optimal use of our physical resources, while keeping shards between 10-50GB.
Hardware-wise, we just moved to 8 i3.8xlarge.elasticsearch nodes, which gives us 256 VCPU's and 1952 GB of ram, with a total of 32 NVMe SSDs.
With the above settings, that gives us ~16 GB shards, with 256 shards per day. So if searching across a single index (day) of logs, we've got exactly 1 vCPU per shard.
