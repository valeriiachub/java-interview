**List Object class methods**

    Class<?> getClass();
Returns the runtime class of this {@code Object}.

    void finilize();
Called by the garbage collector on an object when garbage collection determines that there are no more references to the object.

    void notify();
Wakes up a single thread that is waiting on this object's monitor. If any threads are waiting on this object, one of them is chosen to be awakened. The choice is arbitrary and occurs at the discretion of the implementation.

    void notifyAll();
Wakes up all threads that are waiting on this object's monitor.

    void wait(//);
Causes the current thread to wait until another thread invokes the `notify()` method or the `notifyAll()` method for this object.


    boolean equals();
    Object clone();