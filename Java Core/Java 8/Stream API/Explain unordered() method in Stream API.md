## Explain unordered() method in Stream API
The `unordered()` operation doesn't do any actions to explicitly unorder the stream. What it does is that it removes the constraint on the stream that it must remain ordered, thereby allowing subsequent operations to use optimizations that don't have to take ordering into consideration.

In cases where the stream has an encounter order, but the user does not particularly care about that encounter order, explicitly de-ordering the stream with unordered() may improve parallel performance for some stateful or terminal operations.
