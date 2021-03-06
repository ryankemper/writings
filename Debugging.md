# Debugging

### Why this article might be relevant to you

Debugging is one of the most important skills for "real-world" development work.

There's sometimes a misconception that debugging is a skill for the "Ops" folks, but not necessary for your standard software developer. This could not be further from the truth.

Furthermore, at least in traditional computer science curriculum, **the principles of debugging are not taught**. Rather, people tend to develop an intuition for debugging over years of experience troubleshooting and putting out fires. There's no substitute for experience, but I strongly believe that a simple grounding in the fundamental "philosophy of debugging" puts an individual way ahead of the curve.

**What this article covers:** The high-level algorithm and philosophy of debugging, including cognitive biases that can lead us astray

**What this article doesn't cover:** Specific tricks like usage of programs like GDB, etc.

### What is debugging?

At its core, _debugging_ is solving an observed problem with a system by iteratively improving our understanding of the system until the cause of the bug is known.

A _bug_ is defined as an observed behavior of the system that falls out of line with the behavioral specifications. These can be explicit, such as in a requirements doc, or implicit - your users know a bug when they see one, even if they can't articulate precisely what's behaving incorrectly.

Our goal with debugging is to figure out what's going wrong where. Remember, **nearly all bugs are the logical conclusion of the software we wrote doing exactly what we told it to do**.

Bugs arise because the automated system is doing what it's told to do, but what it was told to do did not account for certain edge cases: unexpected input, counter-intuitive interleaving of events, etc.

Often, after we discover the root cause of a bug, we have the sensation of "of course!". In retrospect the trap we walked into feels supremely obvious, but without the benefit of hindsight, we don't know where to look for the landmine.

### The high-level algorithm

**Step 0:** Document the observed behavior of the system. In this stage, finding the "steps to reproduce" (commonly abbreviated STR) is critical. By their nature, the trickiest bugs do not have reliable STR (or more accurately, finding the reliable STR is prohibitively difficult), but many bugs do have reliable reproductions.

**Step 1:** Come up with a set of possible hypotheses, loosely ranked by estimated likelihood. This doesn't have to be an actual percent number; rather, it's sufficient to know the relative rankings (ex: of hypotheses A, B, and C, A is the most likely.)

**Step 2:** Greedily choose the most likely hypothesis from Step 1, and identify what datapoints would allow us to either confirm or deny the hypothesis. It works out that it's generally easier to find data that definitively denies a hypothesis, rather than data that definitively proves a hypothesis.

At this point we just loop over Steps 1 and 2 repeatedly (perhaps returning to Step 0 if we find errors in our understanding of observed behavior) until we are confident that we have found a hypothesis that *has real explanatory power*.

## Principles

Whether we're debugging our C program down into the assembly level, or just trying to figure out why a global variable got mutated in a high-level interpreted language, there are principles that are so effective as to be considered universal.

### Principle 0: Separate your observations from your hypotheses

The data we decide to gather is influenced by our outlined hypotheses (whether explicitly or implicitly). However, it's critical that observations/datapoints are gathered as "artifacts" - that is, well-documented observations that can be understood by someone who has not participated in the debugging process thus far. *Tip*: It's often helpful to keep track of these artifacts - links to dashboards, log lines, etc - in a centralized location.

What's the motivation for this principle? Often, we start out with a certain hypothesis, and look for data that confirms our "pet theory". The problem is, our attachment to this original hypothesis leads us to **(a)** miss uncovering key datapoints that are not adequately explained by our hypothesis, and possibly **(b)** fail to notice that some part of the data we _have_ gathered already is misaligned with our hypothesis.

In short, all of our observations are filtered through the lens with which we view them. This is unavoidable, but by packaging these observations up into discrete, self-enclosed units, we can minimize the risk that we get anchored on the wrong hypothesis; and perhaps more importantly, when we iterate and develop new hypotheses, we can "test" these hypotheses against our accumulated set of observations.

### Principle 1: Know your assumptions

One of the most common ways to get stuck for enormous amounts of time is to get bit by unchecked assumptions.

A common pattern is that we start out debugging with a set of assumptions that we believe to be true. However, we don't check these assumptions. Assumptions are a useful tool - they provide us the intellectual cover to operate at a higher abstraction level. But, particularly when we start finding that our observations do not mesh with our model of the system, we need to circle back and re-examine the implicit assumptions that we've been working under.

While it's great to have validated _all_ of our assumptions, in practice doing so is borderline impossible. Instead, what I recommend doing is _outlining_ the assumptions being made. This won't be an exhaustive list, but it serves as a nice starting point.

Then, when it feels like a dead end has been reached, or an observation seems impossible given the assumptions we've made, we then circle back and validate our assumptions one-by-one. I recommend proceeding from "easiest to validate" to "hardest to validate".

**Always remember that assumptions serve a useful purpose**. They allow us to operate at a certain level of abstraction. Without abstraction, we experience recursive explosion, where progressively replacing our abstractions with more accurate models of the world quickly brings us all the way down to the emergent properties of the universe.

For example, one abstraction that modern computing relies heavily on is the idea of a _bit_. As software engineers, we think of a bit as "a 0 or 1". Seems simple, right? But our notion of a bit is really an over-simplification. Modern computers represent a bit using the physical (electrochemical) properties of semi-conductors. We distinguish a 0 vs a 1 based off whether the voltage is low or high respectively. Because this abstraction of a bit is really being represented by a physical process, it's possible for inconveniently timed electromagnetic fluctuations to "flip" the value, changing a 0 to a 1 or vice versa.

One of the most fundamental assumptions we make when debugging is that the behavior we observe is precisely the behavior that our code specifies. But when bit flips occur, it's possible - indeed, highly likely - that we will observe some sort of behavior (output) that is **impossible to produce from our source code**. Because the chance of a bit flip occurring is vanishingly small, they tend to only pop up when you're operating at ["Google scale"](http://www.cs.toronto.edu/~bianca/papers/sigmetrics09.pdf).

Following the assumption-validation algorithm above, we would check for bit flips after exhaustively checking our easier-to-validate assumptions, such as "the file I'm looking at is what my server is actually running". This is the right way to do it, because otherwise we run the risk of falling deep into a "rabbit hole", looking for bit flips when there are none, when the real issue is often really just our code, or a library we depend upon, or a compiler bug.

By being aware of our assumptions, such as "Once physically stored in memory, values will stay the same unless our code intentionally mutates them", we put ourselves in the right position to eventually uncover the real problem.

### Principle 2: Follow your hypothesis to its logical conclusion

Often, when we think we've discovered the root cause, we're content with an explanation like "high CPU load on this machine led to the program crashing". If we just stop there, we're going to end up being wrong a large portion of the time. We need to have a model of _why_ CPU load would lead to a program crashing - otherwise our explanation has no real [explanatory power](https://en.wikipedia.org/wiki/Explanatory_power).

Remember, **a hypothesis is a model of reality.** And like all models, to be useful, it needs to have some sort of explanatory value that extends beyond the behavior that constitutes the bug. For example, we might predict that high CPU load lead to a crash because it temporally "spaced out" the instructions that code "usually" runs in a small interval of time, causing a race condition to be exposed that led to the ultimate crash. Now we have something that we can actually test. Note that even this new explanation is still vague - "causing a race condition" is a bit handwavey - but like everything in engineering, and indeed life, the key is to **iterate**, progressively working towards a more accurate model. We will never construct a model that perfectly matches reality - that's why we call it "reality". But we can keep iterating until we have achieved an acceptable level of accuracy.

## Biases

As humans, we are genetically endowed with a set of cognitive biases that are believed to promote our survival/success in the environment that originally shaped us. Some of these biases, such as optimism bias, can still serve us well in situations we encounter. But overall, we need to be wary of our biases, since they will by definition distort clear perception.

Understanding biases therefore helps us to see things more clearly. But watch out for the trap - just because we intellectually can rattle of a list of biases, does not mean we are immune to them. We must be perpetually on guard. In short, as soon as we think we've won the battle against cognitive biases, we've really lost it. (See: [Bias blind spot](https://en.wikipedia.org/wiki/Bias_blind_spot))

### Anchoring Effect

This effect leads us to be irrationally attached to our initial ideas/hypothesis. As a result, we now have a blind spot that leads us to miss a datapoint that would have disproved our initial hypothesis.

The best way to combat this distortion, beyond simply being aware of it, is adhering to **Principle #0: Separate your observations from your hypotheses**.

### Availability heuristic

The tendency to overestimate the likelihood of events that have occurred most recently or are highly salient (and thus readily surface in our memory). Can be thought of as the step-child of the Anchoring Effect and (see next) Hindsight Bias.

Among other things, this can manifest itself as seeing a symptom that we've previously seen, and then immediately assuming that the root cause is the same as the previous root cause that we uncovered.

### Hindsight Bias

This bias leads us to evaluate our past decisions as if we had known information that we later discovered. This leads us to mis-attribute the root cause of a bug to "making a preventable mistake" rather than "making a mistake that logically followed from the set of information we had access to at the time". Understanding this bias is critical after we have discovered the bug and have moved forward to the "Root Cause Analysis" stage where we examine the structural factors that led to the bug/error in the first place.

### Fundamental Attribution Error

Wikipedia says it best: the [Fundamental Attribution Error](https://en.wikipedia.org/wiki/Fundamental_attribution_error) is "the tendency for people to under-emphasize situational explanations for an individual's observed behavior while over-emphasizing dispositional and personality-based explanations for their behavior"

In short, this generally manifests itself as blaming the person rather than the situation - not just in the literal sense of the word "blame" but also as in "failing to examine structural/systemic factors that allowed the error to occur".

### Bandwagon Effect

The tendency to adopt the beliefs that others around us have. This manifests itself as an organization rapidly converging on the same purported root cause of a bug, when really the cause lies eleswhere. This is especially dangerous when paired with / caused by the Anchoring Effect. It's very possible for a hypothesis that was proposed early on to be blindly parroted by others in an organization, failing to update our model of the world as new observations are made.

### Base Rate Fallacy

Humans have a lot of trouble with statistics, and this fallacy is a great example of that.

The base rate fallacy occurs when we neglect to consider the rate at which an effect occurs in the general sense, leading us to be wildly off base about the likelihood of a certain occurence.

The example of "bit flips" outlined in **Principle #1: Know your assumptions** serves as a good example here. If you're debugging bizarre behavior on software that runs on a single machine for a short period of time, while bit flips are certainly still possible, they are highly unlikely to be the true root cause.

### Recency illusion

"The illusion that a phenomenon one has noticed only recently is itself recent."

This one is highly relevant to debugging. A common technique to simplify the search space is to examine what changed around the time that a problem was noticed. This is often an effective strategy, but it leads us astray when the issue has actually been present for a long time, yet we simply failed to notice it until now.

## A bit on Root Cause Analysis

The **root cause analysis** process - hereafter abbreviated as _RCA_ - could be described as "finding the bug _behind the bug_". When operating in this mode, we are looking to examine the structural factors that made the bug possible in the first place. If we skip this crucial process, we will fix the "local" bug, but will not make any progress on addressing the "global" vulnerability that lead to the bug's manifestation.

Remember: _the bug is trying to tell you something_. As a quick analogy, as our understanding of medical science has advanced, we've learned that there is a difference between a _symptom_ and a _problem_. The symptom is the externally visible manifestation of a problem - in logical terms, the existence of a symptom implies the existence of a problem, but the causality does not work the other way: **suppressing a symptom will never fix the underlying problem**.

This is why if your first response to feeling sick is to pound 800 mg of Ibuprofen (Advil), yet you make no changes to your environment, nor your sleep, nor your diet/exercise, you'll find yourself getting repeatedly sick.

Similarly, if your response to an operator running a command that blows away your production database is to add a section to your documentation saying "make sure commands you run won't blow away the production database", you'll soon find the same problem surfacing again, just under slightly different conditions. **The same unaddressed structural vulnerability can manifest itself in a countably infinite number of ways.**

A full explanation of the RCA process and how to conduct a proper post-mortem could occupy the size of a small novel, so that's all I'll say on the matter.

## Conclusion

The high level process here is simple: construct hypotheses, gather data, and then reconcile your hypotheses with your data. Rinse and repeat.

In practice, implementing this strategy effectively takes a great deal of learning and hands-on experience. Some of the best debugggers and metaphorical firefighters tend to be the seat-of-the-pants type, who don't appear to be following a structured process at all. Yet if you examine their behavior, you'll likely find that they've been implementing the algorithm that I've specified subconsciously.

Whether you're just starting your career or you've been in the industry for decades, mastering the art of debugging, as well as the "soft skills" of incident management - effective, low-context communication, and maintaining a calm demeanor just to name two - will pay enormous dividends.
