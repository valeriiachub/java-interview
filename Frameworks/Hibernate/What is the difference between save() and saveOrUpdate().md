## What is the difference between save() and saveOrUpdate() methods?
Session#save() method saves a record only if it's unique with respect to its primary key and will fail to insert if primary key already exists in the table.

Session#saveOrUpdate() method inserts a new record if primary key is unique and will update an existing record if primary key exists in the table already.
