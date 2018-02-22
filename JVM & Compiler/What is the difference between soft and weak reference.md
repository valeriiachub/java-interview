A **Weak reference** is a reference that does not protect a referenced object from collection by GC. i.e. garbage collects when no Strong or Soft refs. 

A **Soft reference** is eligible for collection by garbage collector, but probably won't be collected until its memory is needed. i.e. garbage collects before `OutOfMemoryError`. Soft references are most often used to implement memory-sensitive caches. 
