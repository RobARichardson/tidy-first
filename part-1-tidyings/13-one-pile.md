# 13: One Pile

Sometimes we have to read code that's been split into too many tiny pieces such that it hinders understanding it.  In these moments, we can inline as much as code as needed until it's all in one big pile.  Then we can tidy from there.

The largest cost of code is the cost of readying & understanding it, not the cost of writing it. &#x20;

Tidy First has a bias towards lots of little pieces.  Theoretically, we can increase cohesion as a path to reducing coupling.  Practically, we can reduce the amount of detail that needs to be held in our heads at a given time.  The goal of these small pieces to to enable code to be understood a little at a time.&#x20;

However, sometimes this process goes wrong. Small pieces can make it harder to understand how the pieces interact.  To regain clarity, code must first be mooshed together so new, easier-to-understand parts can be extracted.

Symptoms:

1. Long, repeated argument lists
2. Repeated code, especially conditionals.
3. Poor naming of helper routines
4. Shared mutable data structures
