## Explain entity state transitions

> **1. Transient object**

Transient objects exist in heap memory. Hibernate odes not manage transient objects or persist changes to transient objects.

To persist the changes to a transient object, you would have to ask the session the transient object to the database, at which point Hibernate assigns the object an identified and marks the object as being in persistent state.

> **2. Persistent object**

Persistent objects exist in the database and Hibernate manages the persistence for persistent objects.

If fields or properties change on a persistent object, Hibernate will keep the database representation up to date when the application marks the changes as to be committed.

> **3. Detached object**

Detached objects have a representation in the database, but changes to the object will not be reflected in the database, and vice-versa. This temporary separation of the object and the database is shown in image below.

In order to persist changes made to a detached object, the application must reattach it to a valid Hibernate session. A detached instance can be associated with a new Hibernate session when your application calls on the load, refresh, merge, update(), or save() methods on the new session a reference to the detached object. After the call, the detached object would be a persistent object managed by the new Hibernate session.

> **4. Removed object**

Removed objects are objects that are being manage by Hibernate(persistent objects) that have been passed to the sessions's remove() method. When the application marks the changes held in the session as to be commited, the entries in the database that correspond to removed objects are deleted.
