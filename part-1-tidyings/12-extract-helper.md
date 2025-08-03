---
description: This is also known as Extract Method.
---

# 12: Extract Helper

When you see a block of code inside of a routine that has an obvious purpose and limited interaction with other code in the routine, extract it as a helper routine.  Name the helper after the purpose it serves instead of how the helper works.

This is also known as [Extract Method](https://refactoring.guru/extract-method).&#x20;

So this....

```
routine()
    ...stuff that stays the same...
    ...stuff that needs to change...
    ...stuff that stays the same...
```

Becomes this:

```
helper()
    ...stuff that needs to change...
    
routine()
    ...stuff that stays the same...
    helper()
    ...stuff that stays the same...
```

Another case for Extract Helper is expressing temporal coupling where `a` needs to be called before `b`.

When you frequently see:

```
foo.a()
foo.b()
```

Then do this:

```
ab()
    a()
    b()
```

Often we grow fond of helper methods and keep them around.  Frequently, you'll find yourself wanting to use your new helper again within hours or minutes.  Interfaces become tools for thinking about problems. New interfaces emerge when we're ready to think more abstractly.
