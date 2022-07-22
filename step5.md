<div class="top">

# Create table `movies`
### [◂](command:katapod.loadPage?step4){.steps} Step 5 of 9 [▸](command:katapod.loadPage?step6){.steps}
</div>

Our second table will store information about movies as shown below.  To define 
this table with *single-row partitions*, we can use `title` and `year`
as a *composite partition key*.

| title             | year | duration | avg_rating |
|-------------------|------|----------|------------|
|Alice in Wonderland| 2010 |   108    |    6.00    |
|Alice in Wonderland| 1951 |    75    |    7.08    |


Create the table:
```
CREATE TABLE movies (
  title TEXT,
  year INT,
  duration INT,
  avg_rating FLOAT,
  PRIMARY KEY ((title, year))
);
```

Insert the rows:
```
INSERT INTO movies (title, year, duration, avg_rating) 
VALUES ('Alice in Wonderland', 2010, 108, 6.00);
INSERT INTO movies (title, year, duration, avg_rating) 
VALUES ('Alice in Wonderland', 1951, 75, 7.08);
```

Q1. Retrieve one row:
```
SELECT * FROM movies
WHERE title = 'Alice in Wonderland'
  AND year = 2010;
```

Q2. Retrieve all rows:
```
SELECT * FROM movies;
```

[continue](command:katapod.loadPage?step6){.orange_bar}