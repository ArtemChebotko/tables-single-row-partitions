<div class="top">

# Working with tables
### [◂](command:katapod.loadPage?step8){.steps} Step 9 of 9 [▸](command:katapod.loadPage?step10){.steps}
</div>

Finally, delete the row using the CQL `DELETE` statement:
```
DELETE FROM users 
WHERE email = 'joe@datastax.com';

SELECT * FROM users;
```

Deleting another row from the table:

<details>
  <summary>Solution</summary>

```
DELETE FROM users 
WHERE email = 'jen@datastax.com';

SELECT * FROM users;
```

</details>

[continue](command:katapod.loadPage?finish){.orange_bar}
