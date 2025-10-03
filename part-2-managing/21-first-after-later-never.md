# 21: First, After, Later, Never

## Summary (TLDR)

Tidy Never when:

* You're never changing this code again.
* There's nothing to learn by improving the design.

Tidy Later when:

* You have a big batch of tidying to do without an immediate payoff.
* There's eventual payoff for completing the tidying.
* You can tidy in little batches.

Tidy After when:

* Waiting until next time to tidy will be more expensive.
* You won't feel a sense of completion if you don't tidy after.

Tidy First when:

* It will pay off immediately, either in improved comprehension or in cheaper behavior changes.
* You know what to tidy and how.

## Never

When should we say: "Yes, this is a giant mess, and we should consciously choose not to do anything about it"?

The best reason is when we're never going to change the behavior of the code ever, ever again.

It's rare that code never requires behavior changes.

For truly static systems, "If it ain't broke, don't fix it." applies.

## Later

The mythological status of tidying later is used as justification for tidying too much now, whether that is before or after.

You really can tidy later but you may not like the prerequisite.

Is there enough time to do your work?  How would we work if we had enough time? If the answer is wildly different from what you are actually doing, then no, there's not enough time to do your work.

We should examine the assumption that there's not enough time to do our work.  What would we do if we believed there was?  You might make a list of messes to cleanup later (aka "fun list").  Later, instead of jumping to the next feature, you might grab an item from the "fun list".

If there's an area of the system that's guaranteed to change, tidying creates value if it simplifies future changes.

Tidying later (when not tied to an immediate behavior change) creates value in a couple ways:

* Reducing the tax of messiness
* A Learning Tool: We're bound to learn something as we move code to it's new structure. It's is a great way to become aware of the detailed consequences of your design. Tidying illuminates the design as it _**could**_ be.

Tidying Feels Good. Don't underestimate how much better we are as programmers when we're happy.

## After

If you're going to change the behavior in the area again, a tidy after approach makes some sense.

How much tidying are we talking about? An hour? Do it. Spending a week tidying after? That doesn't make sense.  Put it on the Fun List.

Tidy after when...

* You're going to change the same area again. Soon.
* It's cheaper to tidy now.
* The cost of tidying is roughly in proportion to the cost of behavior changes.

## First

Tidy first? It depends!

I need to change the behavior of some code. The code is messy. Do I tidy first? Ask yourself the following:

* How much harder is the messy change?&#x20;
  * If tidying doesn't make it easier, don't tidy first.
* How immediate is the benefit of tidying? &#x20;
  * Are you trying to comprehend the code before making behavior changes? Tidying helps you comprehend faster.
* How will this tidying amortize?&#x20;
  * Will we only change this code once? Consider limiting the tidying.
  * Will it payoff weekly for years to come, go for it.
* How sure are you of your tidying?
  * Avoid speculation.&#x20;
  * Will it make the code easier to understand?&#x20;
  * Will it make the change easier?

### In general...

Bias towards tidying first but be wary of tidying becoming an end to itself.  The cataloged tidings are intentionally tiny. A bias towards tidying shouldn't cost much and most of the time it will pay off.
