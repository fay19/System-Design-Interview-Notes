# System-Design-Interview-Notes

## Steps
### Scope the problem

- what are the functional requirements and what are the non-funtional requirements
  - Non functional requirements usually include: trade off across high availibility, high reliability, high consistency and low latency. It usually determined by the characteristics of the system
- Design considerations：
  - 确认系统的特性，e.g.: instagram is read heavy,
  - 需要多available
  - 需要多reliable
- Capacity estimation and constraints：
  - 单位数据的size
  - 每天产生多少单位的数据，每秒呢？
  - 每天产生的数据的总size
  - 数据大约需要存储多少年？需要多的space
  - 用户总数量和日活数量

### Sketch up an abstract design
- High level system design
- Building blocks of the system
- what are the relationships of each component
- Database schema design
- Component Design
- System API or Functionaility implementation details

#### Distributed System: identifying and address bottlenecks
- Data replication and redundancy
- Data Sharding
- Cache and load balancing

## 常见知识点
- Object Storage: object storage usually store the data as objects. Each object include the data itself and a variable amount of metatdata. Facebook phones, Spotify songs, Dropbox files are all object storage. Amazon S3, Google cloud storage alson leveraged on object storage architecture.
- 常见的四种NoSQL
  - Key-Value Store: Redis, Voldemort, Dynamo
  - Document Database: data is stored in documents, and documents are grouped in collections. Each document can have an entirely different structure. CouchDB and MongoDB.
  - Wide-Column Database: column famililies as container of rows. Best suited for analyzing large dataset - Cassandra and HBase.
  - Graph Database: store data whose relations are best reprensented in a graph. Data is saved in graph with nodes(entities), properties(information about the entities), and lines(connections between the entities). 


## Distributed System Design Basics
