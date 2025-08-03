# 10: Explicit Parameters

It's common to see blocks of parameters passed to a method as a map.  This is hard to read and understand what data is required by the method.  It also opens up the horrific abuse of modifying the parameters for later use.

Split the routine. The top part gathers the parameters and passes them explicity to the second part.

Example:

```
params = {a:1, b: 2}
foo(params)

function foo(params)
    ...params.a... ...params.b...
    
```

Make the parameters explicit by splitting `foo`:

```
function foo(params)
    foo_body(params.a, params.b)
    
function foo_body(a, b)
    ...a... ...b...
```

#### Anther case for Explicit Parameters:&#x20;

When you find the use of environment variables deep in the bowels of the code. Make parameters explicit, then be prepared to push them up the chain of calling functions.  This makes code easier to read, test, & analyze.
