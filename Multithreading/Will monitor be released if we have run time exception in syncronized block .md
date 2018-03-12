## Will monitor be released if we have run time exception in synchronized block?

From JLS:

> If execution of the Block completes normally, then the lock is unlocked and the synchronized statement completes normally. If execution of the Block completes abruptly for any reason, then t**he lock is unlocked** and the synchronized statement then completes abruptly for the same reason.