# 8: Explaining Variables

Some expressions grow. Even if they start small, they grow, and grow.

Later on, we return and try to understand what is happening.

When you understand part of a big, hairy expression, extract the subexpression into a variable name that captures the intention.

This is often seen in graphics code:

```
return new Point(
    ...big long expression...
    ...another big long expression...
)
```

Before changing the expression, tidy it first:

```
x := ...big long expression...
y := ...another big long expression...
return new Point(x,y)
```

In this tidying we're taking the hard-won understanding and putting it back into the code.  Changing the expressions is now easier.  Next time, they'll be easier to read.

{% hint style="success" %}
As always, separate the tidying commit from the behavior change commit
{% endhint %}
