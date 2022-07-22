<div class="top">

# Working with tables
### [◂](command:katapod.loadPage?step8){.steps} Step 9 of 9 [▸](command:katapod.loadPage?step10){.steps}
</div>

Try the following CQL shell commands and CQL statements that are applicable to tables. 

1. List the names of all tables in the current keyspace:
```
DESCRIBE TABLES;
```

2. Output all CQL statements that can be used to recreate the given table:
```
DESCRIBE TABLE movies;
```

3. Alter the given table:
```
ALTER TABLE movies ADD country TEXT;
```

4. Delete all rows from the table:
```
TRUNCATE movies;
```

5. Remove the given table:
```
DROP TABLE movies;
```

[continue](command:katapod.loadPage?finish){.orange_bar}
