<div class="top">

# Create table `genres`
### [◂](command:katapod.loadPage?step5){.steps} Step 6 of 9 [▸](command:katapod.loadPage?step7){.steps}
</div>

Add the row into our table using the CQL `INSERT` statement:
```
INSERT INTO users (email, name, age, date_joined) 
VALUES ('joe@datastax.com', 'Joe', 25, '2020-01-01');
```

Insert another row into the table:

<details>
  <summary>Solution</summary> 

```
INSERT INTO users (email, name, age, date_joined) 
VALUES ('jen@datastax.com', 'Jen', 27, '2020-01-01');
```

</details>

[continue](command:katapod.loadPage?step7){.orange_bar}