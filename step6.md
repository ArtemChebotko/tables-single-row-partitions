<div class="top">

# Create table `genres`
### [◂](command:katapod.loadPage?step5){.steps} Step 6 of 9 [▸](command:katapod.loadPage?step7){.steps}
</div>

Our next table will store information about movie genres as shown below. This table 
with *single-row partitions* and a *simple partition key* is for you to define.

| genre     | description |
|-----------|-------------|
| Adventure |  A story about a protagonist who journeys to epic or distant places to accomplish something. |
| Fantasy   |  A story about magic or supernatural forces. | 

Create the table:
<details>
  <summary>Solution</summary>

```
CREATE TABLE genres (
  genre TEXT,
  description TEXT,
  PRIMARY KEY ((genre))
);
```

</details>

Insert the rows:
<details>
  <summary>Solution</summary>

```
INSERT INTO genres (genre, description) 
VALUES ('Adventure', 'A story about a protagonist who journeys to epic or distant places to accomplish something.');
INSERT INTO genres (genre, description) 
VALUES ('Fantasy', 'A story about magic or supernatural forces.');
```

</details>

Q1. Retrieve one row:
<details>
  <summary>Solution</summary>

```
SELECT * FROM genres
WHERE genre = 'Fantasy';
```

</details>

Q2. Retrieve all rows:
<details>
  <summary>Solution</summary>

```
SELECT * FROM genres;
```

</details>

[continue](command:katapod.loadPage?step7){.orange_bar}