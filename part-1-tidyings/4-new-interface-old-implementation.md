# 4: New Interface, Old Implementation

You need to call a routine but the interface makes it difficult/complicated/confusing/tedious. &#x20;

Implement and use the interface you wish you could call.  Implement the new interface by calling the old one.

A pass-through interface is the micro-scale essence of software design.&#x20;

The same impulse holds true when you are:

* Coding Backward: Start with the last line of a routine, as if you already had all the intermediate results you needed.
* Coding Test-First: Start with the test you need to pass.
* Designing Helpers: If only I had a routine/object/service that did XXX, then the rest of this would be easy.
