<div class="top">

# What tables with single-row partitions are good for?
### [◂](command:katapod.loadPage?step7){.steps} Step 8 of 9 [▸](command:katapod.loadPage?step9){.steps}
</div>

In Cassandra, tables are designed to support specific queries. Tables with 
single-row partitions are generally used to store and retrieve entities 
by their unique identifiers, such as retrieving a *user by email* or *movie by title and year*.

Of course, it is possible to use tables with 
single-row partitions for relationships, such as *user rated movie* in the example below, but tables 
with multi-row partitions are much more suitable for that. 
 
```
-- Not a good way to 
-- store relationships ... 
CREATE TABLE user_rated_movie (
  email TEXT,
  title TEXT,
  year INT,
  rating INT,
  PRIMARY KEY ((email, title, year))
);

-- Tables with multi-row partitions 
-- are the way to go ...
-- Get all rating left by a user
CREATE TABLE ratings_by_user (
  email TEXT,
  title TEXT,
  year INT,
  rating INT,
  PRIMARY KEY ((email), title, year)
);
--  Get all ratings left for a movie
CREATE TABLE ratings_by_movie (
  email TEXT,
  title TEXT,
  year INT,
  rating INT,
  PRIMARY KEY ((title, year), email)
);
```

[continue](command:katapod.loadPage?step9){.orange_bar}
