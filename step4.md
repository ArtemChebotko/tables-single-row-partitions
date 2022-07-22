<div class="top">

# Create table "users"
### [◂](command:katapod.loadPage?step3){.steps} Step 4 of 9 [▸](command:katapod.loadPage?step5){.steps}
</div>

Our first table will store information about users as shown below. To define 
this table with *single-row partitions*, we can use `email`
as a *simple partition key*.

| email            | name | age | date_joined |
|------------------|------|-----|-------------|
| joe@datastax.com |  Joe |  25 |  2020-01-01 |
| jen@datastax.com |  Jen |  27 |  2020-01-01 | 

Create the table:
```
CREATE TABLE users (
  email TEXT,
  name TEXT,
  age INT,
  date_joined DATE,
  PRIMARY KEY ((email))
);
```

Insert the rows:
```
INSERT INTO users (email, name, age, date_joined) 
VALUES ('joe@datastax.com', 'Joe', 25, '2020-01-01');
INSERT INTO users (email, name, age, date_joined) 
VALUES ('jen@datastax.com', 'Jen', 27, '2020-01-01');
```

Q1. Retrieve one row:
```
SELECT * FROM users
WHERE email = 'joe@datastax.com';
```

Q2. Retrieve all rows:
```
SELECT * FROM users;
```

[continue](command:katapod.loadPage?step5){.orange_bar}