**Are servlets thread-safe?**  
Servlet instances are inherently **not thread safe** because of the multi threaded nature of the Java Programming language.  

But that said, Java classes are Thread safe if you don't have instance variables. Only instance variables need to synchronize.  Variables declared in the methods are thread safe as each thread creates its own Program Stack and function variables are allocated in stack.   

This means that variable in a methods are created for each thread, hence does not have any thread sync issues associated.