## What is dirty checking?

An object with modifications that haven't yet been propagated to the database is considered *dirty*. 

Just before commiting transaction Hibernate checks the state of the object after save() or get() and current state of the object. If some properties were modified than Hibernate perform update query.
