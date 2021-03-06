Cyclone： Dynamic Virtualization for Cloud Security 
---

- by *Matt Caesar*， UIUC

### Intro
- Today's cloud environment not meet DoD neds

### Towards a solution
- encapsulate clouds into "enclaves"
- manipulate the environement in which software executes
- Motivating Example
	- warfighter notices that some server have high traffic
	- maybe by DDoS attack
	- when server sends faulty packets, network is paused
	- they determines workaround to block attack
	- tests workaround in clone
	- can be installed in real cloud
- clouds don't support these functions
	- cloning, rewinding, fast forwarding, replaying...

### Dynamic virtualization for cloud security
- Cyclone: bring the benefits of single-machine vertualization to the entire clouds
- introduces several dynamic capabilities
	- changing time
	- changing space
	- changing input

### System architecture
- endpoint hypervisor
- switches
- endpoint server/host
- cloud virtualization controller

### Proving dynamic capabilities
- capabilities provided by distributed algs.
- develop algoritms
	- ensemable migration, clonding, distributed pause, reproducible executin, fast forwarding, network inputchecking

### Lessons
- dealing with uncertainty
	- original proposal: reliable information about cloud's current state
	- in practise, unrelible/challenged clouds, partial deployments, delays, data acquisition bugs
	- solution: explicitly model uncertainty in cloud's current state
	
- configuration
	- original: fixed software, fixed protocol
	- but it would be better to support configuration
	- because in practise, need to interface with other systems, use preferred software bases, change protocols based on environment
	- ability to enable/disable functionality
- support multiple users/objectives

### Compositional Hypervisor
- a transparent layer between physical cloud and actors

### Example
- want to shift traffic from server 1 to server 2
- the cloud controller will talk to the route table, letting it change the route table

### Conclusion
- Dynamic virtualization can beneffit cloud security
	- cloud-wide virtualization enable the control of shape, time and inputs
- Cyclone
	- virtualizes ensemables of end hosts and network devies
	- provide algorithms to control execution and enalbe advanced functions
