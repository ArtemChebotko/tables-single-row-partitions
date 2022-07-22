<div class="top">

# Create table "actors"
### [◂](command:katapod.loadPage?step6){.steps} Step 7 of 9 [▸](command:katapod.loadPage?step8){.steps}
</div>

Our last table will store information about movie actors as shown below. This table 
with *single-row partitions* and a *composite partition key* is for you to define.

| first_name | last_name  | dob        |
|----------- |------------|------------|
| Johnny     | Depp       | 1963-06-09 |
| Anne       | Hathaway   | 1982-11-12 | 

Create the table:
<details>
  <summary>Solution</summary>

```
CREATE TABLE actors (
  first_name TEXT,
  last_name TEXT,
  dob DATE,
  PRIMARY KEY ((first_name, last_name))
);
```

</details>

Insert the rows:
<details>
  <summary>Solution</summary>

```
INSERT INTO actors (first_name, last_name, dob) 
VALUES ('Johnny', 'Depp', '1963-06-09');
INSERT INTO actors (first_name, last_name, dob) 
VALUES ('Anne', 'Hathaway', '1982-11-12');
```

</details>

Q1. Retrieve one row:
<details>
  <summary>Solution</summary>

```
SELECT * FROM actors
WHERE first_name = 'Johnny'
  AND last_name = 'Depp';
```

</details>

Q2. Retrieve all rows:
<details>
  <summary>Solution</summary>

```
SELECT * FROM actors;
```

</details>

[continue](command:katapod.loadPage?step8){.orange_bar}
