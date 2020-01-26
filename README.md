# System-Design-Interview-Notes

## Steps:
### Scope the problem

1. what are the functional requirements and what are the non-funtional requirements
- Non functional requirements usually include: trade off across high availibility, high reliability, high consistency and low latency. It usually determined by the characteristics of the system
2. Design considerations：
- 确认系统的特性，e.g.: instagram is read heavy,
- 需要多available
- 需要多reliable
3. Capacity estimation and constraints：
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
