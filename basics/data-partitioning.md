# Data Partitioning

## What is data partitioning
- Split up DB/table across multipler machines
- Horizontal scaling is cheaper and more feasible than vertical scaling

## Partitioning methods

### Horizontal partitioning
- Range based partitioning
- Data sharding
- may lead to unbalanced servers if the value whose range used for sharding isn't chosen carefully

### Vertical partitioning
- Divide data by specific feature and store seperately on different server
- Pro
  - Straight forward to implement
  - Low impact on application
- Con
  - to support growth of the application, a database may need furthur partitioning
  
### Directory based partitioning
- Loosely coupled lookup service in between database and application
- Lookup service know partition schemes and abstract away from database access code
- Database can scale without impact on application
- Con
  - Can be SPOF

## Partitioning Criteria
- Key or Hash-based partitioning
  - Hash some key attributes that yield the partition number
  - Need to redistribution if more server is added, work around - Consistent Hashing
- List Partitioning
  - Each partition is assigned to a list of values
- Round-robin partitioning
- Composite partitioning
  - Combination of any above
  
## Common Problems of Data Partitioning
- Joins and denormalization
  - Joins across server is not performance efficient
  - Workaround: denormalize database so required joins can be performed from a single table
 
- Referential integrity
  - Extremely difficult to enforce data intergrity constrainst such as foreign key
  - Application code need to enforce it - run regular SQL jobs to clean up danging references
  
- Rebalancing
  - Reason of rebalancing
    - data distribution is not uniform
    - a lot of load on one shard
  - Rebalancing without downtime is extremely difficult
  - Lookup service can help, but will create SPOF
    

