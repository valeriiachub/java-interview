## What is the difference between intermediate and terminal operations?  
All operations are either intermediate or terminal.  

**Intermediate operations** are those operations that return _Stream_ itself allowing for further operations on a stream. These operations are always lazy, i.e. they do not process the stream at the call site, an intermediate operation can only process data when there is a terminal operation.

**Terminal operations** terminate the pipeline and initiate stream processing. The stream is passed through all intermediate operations during terminal operation call.


