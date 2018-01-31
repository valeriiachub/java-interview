**What is exception wrapping?**
Suppose there is an interface:

    public interface AnInterface {
        void foo();
        void bar();
        void baz();
    }

Also there are many implementations of the interface. Suppose we have an implementation's method which throws a checked exception: 

    class Impl implements AnInterface {
        public void foo() throws Exception {
            ...
            throw new Exception();
        }
    
        public void bar() {
    
        }
    
        public void baz() {
    
        }
    }



Our interface doesn't declare the exception via `throws` keyword. 

Now, if append to our implementation's method `throws ...`  then we need to do it also in our interface. If we do this in our interface we need to append this also to all implementations of the interface method. And finally whenever we use an interface implementation method we need to handle the exception(although we need the exception only in one implementation, it will affect all implementations).

----------
To avoid the mess we need to use **exception wrapping**. What we need to do is to create our custom `RuntimeException` (in order to distinguish it from a regular runtime exception) and throw this exception. We don't need to append `throws` keyword to the method in the case. But we must remember to handle the exception(for the implementation) whenever we invoke it:

    try {
        impl.foo();
    } catch (CustomRuntimeException e) {
        //handling
    }

