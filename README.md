# System-Design-Interview-Notes

### Steps:
#### 1. Scope the problem: what are the functional requirements and what are the non-funtional requirements
Non functional requirements usually include:
trade off across high availibility, high reliability, high consistency and low latency. It usually determined by the characteristics of the system

#### 2. Design considerations：
- 确认系统的特性，e.g.: instagram is read heavy,
- 需要多available
- 需要多reliable

#### 3. Capacity estimation and constraints：
- 单位数据的size
- 每天产生多少单位的数据，每秒呢？
- 每天产生的数据的总size
- 数据大约需要存储多少年？需要多的space
- 用户总数量和日活数量

#### 4. High level system design

#### 5. Database schema design

#### 6. Component Design

#### 7. System API or Functionaility implementation details

#### 8. Distributed System
- Data replication and redundancy
- Data Sharding

#### 9. Cache and load balancing
