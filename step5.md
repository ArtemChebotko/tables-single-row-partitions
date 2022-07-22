<div class="top">

# Create table `movies`
### [◂](command:katapod.loadPage?step4){.steps} Step 5 of 9 [▸](command:katapod.loadPage?step6){.steps}
</div>

A Cassandra table has named columns with data types, rows with values, and a primary key to uniquely identify each row. 
As an example, let's create table `users` with four columns and primary key `email`. 

Create the table:
```
CREATE TABLE users (
  email TEXT PRIMARY KEY,
  name TEXT,
  age INT,
  date_joined DATE
);
```

[continue](command:katapod.loadPage?step6){.orange_bar}