# 9: Explaining Constants

You're reading along and see a number you don't recognize. Or you see a constant string repeated all over the code.

Create a symbolic constant. Replace all usage with the symbol.

This is not okay:

```
if response.code = 404
    ...blah blah blah...
```

We're not here to judge the person who made the mess. We're here to take care of ourselves by tidying first before changing things:

```
PAGE_NOT_FOUND = 404
if response.code = PAGE_NOT_FOUND
    ...blah blah blah...
```

**Be careful:** The same literal can appear in two places but have different meaning. It doesn't help to tidy to:

```
ONE = 1
...ONE... # everywhere you need unity
```

**You're reading. You understand. You're putting that understanding into the code so you don't have to hold it in your head.**

