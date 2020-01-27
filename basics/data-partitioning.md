## Data Partitioning

## What is data partitioning
- split up DB/table across multipler machines
- horizontal scaling is cheaper and more feasible than vertical scaling

## Partitioning methods

### Horizontal partitioning
- Range based partitioning
- Data sharding
- may lead to unbalanced servers if the value whose range used for sharding isn't chosen carefully

### Vertical partitioning
- divide data by specific feature and store seperately on different server
- Pro
  - straight forward to implement
  - low impact on application
- Con
  - to support growth of the application, a database may need furthur partitioning
  
### Directory based partitioning
- loosely coupled lookup service in between database and application
- lookup service know partition schemes and abstract away from database access code
- database can scale without impact on application
- Con
  - can be SPOF

### Partitioning Criteria
- Key or Hash-based partitioning
  - hash some key attributes that yield the partition number
  - need to redistribution if more server is added, work around - Consistent Hashing
- List Partitioning
  - Each partition is assigned to a list of values
- Round-robin partitioning
- Composite partitioning
  - combination of any above
  
### Common Problems of Data Partitioning
- joins and denormalization
  - joins across server is not performance efficient
  - workaround: denormalize database so required joins can be performed from a single table
 
- Referential integrity
  - extremely difficult to enforce data intergrity constrainst such as foreign key
  - application code need to enforce it - run regular SQL jobs to clean up danging references
  
- Rebalancing
  - reason of rebalancing
    - data distribution is not uniform
    - a lot of load on one shard
  - rebalancing without downtime is extremely difficult
  - lookup service can help, but will create SPOF
    

