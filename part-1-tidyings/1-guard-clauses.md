# 1. Guard Clauses

Code like this:

```
if(condition)
... some code ...
```

Or like this:

```
if(condition)
    if(not other condition)
        ... some code ...
```

Tidy the code above to something like this:

```
if(not condition) return
if(other condition) return

... some code ...
```

As a reader, it's easy to get lost in nested conditions. &#x20;

Code with guard clauses is easier to read & analyze because the preconditions are explicit.

Don't overdo guard clauses - a routine with sever or eight clauses is NOT easier to ready.
