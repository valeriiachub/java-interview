## How much memory an object takes?

Java object consist of:

 1. **Object's header**.
Memory size: 8 bytes(for 32 bit system) or 16 bytes(for 64 bit system).
Header contains mark work(?), hash code, garbage collection information, type information, lock information(multithreading). If the object is array then we have additional 4 bytes to store it's size.
 2. **Memory for primitive types**.
 3. **Memory for reference types**.
 4. **Alignment(number of bytes should be a multiple of eight)**.