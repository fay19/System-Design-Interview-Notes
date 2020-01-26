### SQL
Store data in rows and columns. Each row is a data entity, each column stores seperate data points of that entity.

### NoSQL
- Key-Value Store: Redis, Voldemort, Dynamo
- Document Database: data is stored in documents, and documents are grouped in collections. Each document can have an entirely different structure. CouchDB and MongoDB.
- Wide-Column Database: column famililies as container of rows. Best suited for analyzing large dataset - Cassandra and HBase.
- Graph Database: store data whose relations are best reprensented in a graph. Data is saved in graph with nodes(entities), properties(information about the entities), and lines(connections between the entities). 

### High level diffences
- Storeage 
- Schema
  - SQL is fixed schmea, NoSQL schema are dynamic. Columns can be added on the fly and each "row"(or equivalent) doesn't have to contain data for each "column"
- Querying
- Scalability
  - SQL are usually veritically scalable, i.e., by increasing the horsepower(higher memory, CPU and etc.) of the hardware, which can get very expensive. It is possible to scale a relational database across multipler servers, but this is challenging and time consuming process.
  - NoSQL are horizontally scalable, meaning we can add more servers easily in our NoSQL database infrastructure to handle a lot of traffic. More cost-effective than veritical scaling.
  - Reliability or ASCD Compliancy(Atomicity, Consistency, Isolation, Durability): most is SQL is ASCD compliant. Most NoSQL sacrifice ACID complaince for performance and scalability
  
### Which one to use
- Choose SQL
  - ACID is a must-have
  - data is structured and unchanging
- choose NoSQL
  - Storing large volumes of data that often have little to no structure
  - Making the most of clond computing and storage
  - Rapid development
     - Quick system iteration which requires making frequent updates to data structures without a lot of downtime between version. 
