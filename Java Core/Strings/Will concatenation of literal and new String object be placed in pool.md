## Will concatenation of literal and new String object be placed in pool?
    String str = "Hello" + new String(" World");

**Solution**
No.

From [JSL](https://docs.oracle.com/javase/specs/jls/se8/html/jls-3.html#jls-3.10.5):

> Strings computed by concatenation at run time are newly created and
> therefore distinct.

From Cay Horstmann's book:

> If the virtual machine always arranges for equal strings to be shared,
> then you could use the `==` operator for testing equality. **But only
> string literals are shared, not strings that are the result of
> operations like + or substring.**

Worth noting that `new String(" World")`actually creates two objects: one is literal and it's placed in the string pool and another it's newly created `String` object for which we have a reference now.