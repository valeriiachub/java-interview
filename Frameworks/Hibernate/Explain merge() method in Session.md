## Explain Session#merge() method

Session#merge() method takes an entity as a parameter and creates copy of the object which will placed into PersistenceContext and returns it.

It worth noting that original reference to the entity won't be managed by Hibernate so any change to the object state won't update database.
