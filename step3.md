<div class="top">

# Let's get started ...
### [◂](command:katapod.loadPage?step2){.steps} Step 3 of 9 [▸](command:katapod.loadPage?step4){.steps}
</div>

A keyspace is a namespace for a set of tables sharing a data replication strategy and some options. 
It is conceptually similar to a "database" in a relational database management system.

Create the keyspace:
```
CREATE KEYSPACE killr_video
WITH replication = {
  'class': 'NetworkTopologyStrategy', 
  'DC-Houston': 1 }; 
```

Our keyspace name is `killr_video`. Any data in this keyspace will be replicated to datacenter `DC-Houston` 
using replication strategy `NetworkTopologyStrategy` and replication factor `1`. In production, however, we strongly 
recommend multiple datacenters and at least three replicas per datacenter for higher availability.

[continue](command:katapod.loadPage?step4){.orange_bar}