# 16: Separate Tidying

## Where do you put tidying?&#x20;

#### Here's an ugly piece of tail chasing:

1. I put my tidyings in with my behavior changes
2. Reviewers complain that my PRs are too long.
3. I separate the tidyings into their own PRs, either before (more likely) or after the behavior changes.
4. Reviewers complain that the tidying PRs are pointless
5. Go to 1.

Tidyings have to go somewhere otherwise we don't do it. Where should they go?

**Summary**: They go in their own PR with as few per PR as possible.

### Phases

As we learn to tidy, we go through predictable phases:

1. We begin with an undifferentiated mass of changes.
2. After learning the tidyings, it's as if our picture under the microscope snaps into focus. Some changes are **Behavior** while others are **Structure**. However, there is no distinct flow between the two.
3. After a while, we start noticing common flows where each tidying leads to another or enables the behavior change.  Programming becomes more like Chess with a sequence of moves.

At this point, we still have a large, single PR. Every move was intentional, aimed at making changes easier but when we put it all together, we've got a bit of a mess.  Reviewers will balk.

## Split the changes

Split each change (step) into a separate PR.  Sequences of tidyings (or even just one) go in one PR. Behavior changes go in another.  Each time we switch between tidying/structure (S) and changing behavior (B), we open a new PR.

<p align="center"><strong>B ➡️ SS ➡️B ➡️ SSS ➡️ BB ➡️ S</strong></p>

### How we lump or split PRs is a trade-off

* Large, all-inclusive PR show the whole picture but are often too much for the reviewer.
* Tiny PRs invited feedback in the small sense but come at the risk of going into the weeds.

### Review Latency

* Review latency is also an incentive. &#x20;
* Rapid reviews encourage more frequent, smaller PRs
* Slow reviews encourage large PRs, further slowing down reviews.
