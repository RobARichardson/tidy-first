# 7: Move Declaration & Initialization Together

Sometimes variable initialization and declaration drift apart.

While a variable's name gives a hint of its role, the initialization reinforces the message of the name.

Code that separates declaration from initialization makes it harder to read.  By the time  you get to the initialization, some of the context has been forgotten.

#### Example:

```
fn()
    int a
    ...some code that doesn't use a
    a = ...
    int b
    ...some more code, maybe it uses a but doesn't use b.
    b = ...a...
    ...some code that uses b
```

Tidy this by moving the initialization up to the declaration

```
fn()
    int a = ...
    ...some code that doesn't use a
    ...some more code, maybe it uses a but doesn't use b
    int b = ...a...
    ...some code that uses b
```

Play around with the order.&#x20;

It is easier to read and understand the code if each of the variables is declared and initialized just before it's used?  Or, is it better if they're all declared and initialized at the top of the function?  Imagine the experience for the next reader.

We need maintain the order of dependencies with respect to variable initialization.

{% hint style="success" %}
Work in small steps That's the tidying way. Big design changes too hard & scary? Take smaller steps.
{% endhint %}
