<div class="top">

# What tables with single-row partitions are good for?
### [◂](command:katapod.loadPage?step7){.steps} Step 8 of 9 [▸](command:katapod.loadPage?step9){.steps}
</div>

Next, update the row using the CQL `UPDATE` statement:
```
UPDATE users SET name = 'Joseph' 
WHERE email = 'joe@datastax.com';

SELECT * FROM users;
```

Update another row in the table:

<details>
  <summary>Solution</summary> 

```
UPDATE users SET name = 'Jennifer' 
WHERE email = 'jen@datastax.com';

SELECT * FROM users;
```

</details>

[continue](command:katapod.loadPage?step9){.orange_bar}
