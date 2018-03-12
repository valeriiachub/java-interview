## List possible statements in JDBC
![enter image description here](https://img.shields.io/badge/Source-CHI%20Software-blue.svg)

**Statement**
Execute simple SQL query without parameters. We can't provide parameters to the statement in runtime.

Firstly, we need to retrieve the statement object from connection:

    Statement st = con.createStatement();

Then we can execute query on the object:

    st.executeQuery(SELECT * FROM employee);

If you need to INSERT, DELETE or UPDATE you need to use `executeUpdate()` method.
`executeQuery()` used only for `SELECT` statements.

**Where to use**: execute query only once without parameters in run time.
The performance of this interface is very low.

----------


**PreparedStatement**
1. `prepareStatement(String query)`  compiles the query and send it to the database for caching.
2. We can pass parameters to the statement in run time.


----------


**CallableStatement**
Execute a call to a database stored procedure.

    CallableStatement cs = DBConnection.prepareCall("CALL myStoredProcedure");


