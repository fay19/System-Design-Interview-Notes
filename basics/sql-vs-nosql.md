### SQL
Store data in rows and columns. Each row is a data entity, each column stores seperate data points of that entity.

### NoSQL
- Key-Value Store
  - Redis, Voldemort, Dynamo
- Document Database
  - data is stored in documents
  - documents are grouped in collections
  - Each document can have an entirely different structure
  - CouchDB and MongoDB.
- Wide-Column Database
  - column famililies as container of rows
  - Best suited for analyzing large dataset
  - Cassandra and HBase.
- Graph Database
  - store data whose relations are best reprensented in a graph. 
  - Data is saved in graph with nodes(entities), properties(information about the entities), and lines(connections between the entities). 

### High level diffences
- Storeage 
- Schema
  - SQL is fixed schmea, NoSQL schema are dynamic
  - NoSQL Columns can be added on the fly and each "row"(or equivalent) doesn't have to contain data for each "column"
- Querying
- Scalability
  - SQL 
    - veritically scalable by increasing the horsepower(higher memory, CPU and etc.) of the hardware and are expensive
    - horizontally scalable but is challenging and time consuming.
  - NoSQL
    - horizontally scalable(add more servers). More cost-effective than veritical scaling.
- Reliability or ASCD Compliancy(Atomicity, Consistency, Isolation, Durability)
  - most is SQL is ASCD compliant
  - Most NoSQL sacrifice ACID complaince for performance and scalability
  
### Which one to use
- SQL
  - ACID is a must-have
  - data is structured and unchanging
- NoSQL
  - Storing large volumes of data that often have little to no structure
  - Making the most of clond computing and storage
  - Rapid development
     - Quick system iteration which requires making frequent updates to data structures without a lot of downtime between version. 
