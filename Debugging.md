# Debugging

### Introduction

Debugging is one of the most important skills for "real-world" development work.

There's sometimes a misconception that debugging is a skill for the "Ops" folks, but not necessary for a run-of-the-mill developer. This could not be further from the truth.

What this article covers: The high-level philosophy of debugging.

What this article doesn't cover: Specific tricks like usage of programs like GDB, etc.

### What is debugging?

At its core, debugging is solving an observed problem with a system by iteratively improving our understanding of the system until the cause of the bug is known.

A "bug" is defined as an observed behavior of the system that falls out of line with the behavioral specifications. These can be explicit, such as in a requirements doc, or implicit - your users know a bug when they see one, even if they can't articulate precisely what's behaving incorrectly.

Our goal with debugging is to figure out what's going wrong where. Remember, nearly all bugs are the result of taking [TODO: improve this] something to its logical conclusion.

Bugs arise because the automated system is doing what it's told to do, but what it was told to do did not account for certain edge cases: unexpected input, counter-intuitive interleaving of events, etc.

Often, after we discover the root cause of a bug, we have the sensation of "of course!". In retrospect the trap we walked into feels supremely obvious, but without the benefit of hindsight, we don't know where to look for the landmine.

### The high-level algorithm

Step 0: Document the observed behavior of the system. In this stage, finding the "steps to reproduce" (commonly abbreviated STR) is critical. By their nature, the trickiest bugs do not have reliable STR (or more accurately, finding the reliable STR is prohibitively difficult), but many bugs do have reliable reproductions.

Step 1: Come up with a set of possible hypotheses, loosely ranked by estimated likelihood. This doesn't have to be an actual percent number; rather, it's sufficient to know the relative rankings (ex: of hypotheses A, B, and C, A is the most likely.)

Step 2: Greedily choose the most likely hypothesis from Step 1, and identify what datapoints would allow us to either confirm or deny the hypothesis. It works out that it's generally easier to find data that definitively denies a hypothesis, rather than data that definitively proves a hypothesis.

At this point we just loop over Steps 1 and 2 repeatedly (perhaps returning to Step 0 if we find errors in our understanding of observed behavior) until we are confident that we have found a hypothesis that *has real explanatory power*.

## Principles

### Principle 0: Separate your observations from your hypotheses

The data we decide to gather is influenced by our outlined hypotheses (whether explicitly or implicitly). However, it's critical that observations/datapoints are gathered as "artifacts" - that is, well-documented observations that can be understood by someone who has not participated in the debugging process thus far.

What's the motivation for this principle? Often, we start out with a certain hypothesis, and look for data that confirms our "pet theory". The problem is, our attachment to this original hypothesis leads us to (a) miss uncovering key datapoints that are not adequately explained by our hypothesis, and possibly (b) fail to notice that some part of the data we _have_ gathered already is misaligned with our hypothesis.

In short, all of our observations are filtered through the lens with which we view them. This is unavoidable, but by packaging these observations up into discrete, self-enclosed units, we can minimize the risk that we get anchored on the wrong hypothesis; and perhaps more importantly, when we iterate and develop new hypotheses, we can "test" these hypotheses against our accumulated set of observations.

### Principle 1: Give the "Why" rather than just the "What"

[TODO]

## Biases

As humans, we are genetically endowed with a set of cognitive biases that work to promote our survival/success in the environment that originally shaped us. Some of these biases, such as optimism bias, can still serve us well in situations we encounter. But overall, we need to be wary of our biases, since they will by definition distort clear perception.

### Hindsight Bias

This bias leads us to evaluate our past decisions as if we should have known information that we later discovered. This leads us to mis-attribute the root cause of a bug to "making a preventable mistake" rather than "making a mistake that logically followed from the set of information we had access to at the time". Understanding this bias is critical after we have discovered the bug and have moved forward to the "Root Cause Analysis" stage where we examine the structural factors that led to the bug/error in the first place.

### Fundamental Attribution Error

[TODO] In short, blaming the person rather than the situation. Not just in the literal sense of "blame" but also "failing to examine structural/systemic factors"
