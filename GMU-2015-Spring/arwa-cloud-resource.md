## Automatic, Optimal, and Near-Optimal Resource Allocation in Cloud Computing

- Arwa Aldhalaan
- Date: 04/23/2015

### Background
- SaaS
  - pay as they use
- IaaS

### Intro
- Cloud computing is based on large distributed system
- resource management in cloud is very challengeing

### Problem Statement
- management their resource in dynamic environments
- how to process customer's requirements by allocation machines
- number and types of machines to run services
- challenge
  - dynamic
- automaic, optimization techniques to meet QoS reqirements

### Arch
- users make request to SaaS
- SaaS require IaaS
- IaaS requires migraiton

### Live virtual machine migration
- pages of the address of the virtual machine is copied when the VM is running
- dyanmic migrate the dirty pages
- advantage: very low downtime
- optimal value of alpha
  - non-linear optimizer decides alpha
  - tradeoff between alpha and network utilization
  - alpha is high, then long downtime, low network utilization
- heuristic solution to this problem

### Problem Description
- The cloud provider has to make an optimal decision where to send the request
- constraints
  - SLA constraints: weighted average of ...
- Heuristic search
  - hill-climbing, determine neighborhood
  - reuse virtual machine that is already in the cloud
- Better revenue than Best-fit strategy

### Cloud Virtual Machine Allocation
- two virtual machine in the same physical machine
  - take into account of commmunication costs
  - communication strength 
- problem statement: consumers arrive at the server with number of virutla machines, comunication of vms, types of vms
- proble model: consider linear revenue and exponential revenue model
- consumers make request of a group of virtual mahines
- dynamic find the allocation of virutla machines to maxmize the cloud provider revenue
- solution: do not colocate
  - users pays more if the cmmunication is better
- heuristic solutions
  - algorithm 1: allocate as close as possible, depending on communication strength
  - alg 2: take into account of de-allocate of some virtual machines
  - alg 3: 
  - Advance alg: consider deallocation, using climb hill
- solution: build a tree where the edge is the communication strength
- Experiments: compare with OPT
- availability constraints: if a machine is down, then the service may down
  - there is a tradeoff between the revenue and availability

### SaaS
- Model: customer can subsribe
- Problem: the optimal type and number of virtual machines to run the request from customers
- Model
  - cost: p_i * b_i
  - constraint: running time
- Heuristic solution
  - scaleupdown: repalce large with small
  - compare with optimal solution
  
### Related work
- energy consumption
- maximize revenue subject to constraints of quality guaranteee

### Idea
- take into account of the interation of vms
- types of vms
- reuse vms
- dynamic pricing model
- define service level agreement
- resource allocation in cloud data center: fair resource share?


### More
- workload: Poisson distribution
- service agreements: response time, recover time
  - how to allocate resources in cloud
- design hyperviser for simulation
  - different virutalization
  - container technology: have no virtualization
  

  
### Summary
In this talk, the speaker introduces her PhD research on how to automatically and optimally or near-optimally allocate the resource in the cloud infrastructure in order to maximize revenue while meeting the QoS requirements. As the cloud computing becomes more nd more popular, cloud services such as SaaS and IaaS become more and more popular. 
