<div class="top">

# Create table `actors`
### [◂](command:katapod.loadPage?step6){.steps} Step 7 of 9 [▸](command:katapod.loadPage?step8){.steps}
</div>

Now, retrieve the row using the CQL `SELECT` statement:
```
SELECT * FROM users
WHERE email = 'joe@datastax.com';
```

Retrieve a different row from the table:

<details>
  <summary>Solution</summary> 

```
SELECT * FROM users
WHERE email = 'jen@datastax.com';
```

</details>

[continue](command:katapod.loadPage?step8){.orange_bar}
