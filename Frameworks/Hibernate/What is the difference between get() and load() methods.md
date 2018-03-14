## What is difference between session.get() and session.load()?

**Session#load** 
The method will always return proxy without hitting the database. In hibernate, proxy is an object with the given identifier value, it's properties are not initialized, it just look like a temporary fake object.

**Session#get**
It always hit the database and return the real object, an object that represent the database row, not proxy.
