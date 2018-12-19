# In hibernate Configuration:

<property name=”hbm2ddl.auto”></property>
For this property it having values like -> create, update, validate, create-drop
If the value is create -> it delete existing tables and creates a new table with the mapping name.
Update -> if any table required it will create table, if any table required alter operation it will do that.
Validate -> check mapping schema against table schema.(it means it checks the mapping file is valid for database table schema).
Ex: mapping contains 5 columns, table contains 10 columns no problem
      Mapping contains 5 columns , table contains 3 columns it makes validation failed.(exception case)
Create-drop: drop the existing table, creates new table, and again drops the table at the time of sessionFactory.close(), for testing purpose it is best use case