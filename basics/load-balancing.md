## Load Balancing

### What is load balancing
- Distribute load across a cluster of servers
- Monitor server status
- Stop sending traffice to not responding or error server
- in between of clients and servers
- prevent SPOF, improve overall availibity and responsiveness
- Multi-layer of load balancing
  ![graph](../images/multi-layer-lb.png)


### Benefits
- faster, uninterrupted service
- less downtime, higher throughput
- low latency
- predicative analytics to determine traffic bottlenecks, which provide actionable insights - key to autmation and can help drive business decisions
- few failed and stressed components

### Algorithms
- Health checks algo
  - least connection method
    - large number of persistent connection are unevenly distributed between servers
  - least response time method
  - least bandwith method
  - Round Robin method
    - servce are of equal specification
    - not many persistent connections
  - Weighted Round Robin Method
    - server with different processing capacities
    - higher weighted server gets high priority and get more connections
  - IP hash
    - hash client IP address to redirect traffic to get random assignment

### Redunant Load Balancers
- load balancer can be SPOF
- add a redundant LB, take over when first one failed
    
