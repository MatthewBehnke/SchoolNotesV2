#ComputerScience  #IowaStateUniversity  #COMS321 


[[COM S 321]] 

---

# Memory Hierarchies

Physical constructs that take advantage of [[Locality]]


- Lowest: 
	- Disk: has everything the computers has stored
- highest
	- level 1 cache: very small, has little 

There are multiple layers in between with smaller spaces near the top and larger spaces near the bottom. The layers are the fastest at the top and get  slower a the more layers traveled down until then disk which is the lowest but also the slowest.

Data is transferred between layers in blocks or lines. With this when we ask for an address we get the all of the data in the block the address is in. This way we can take advantage of the [[Locality]] and [[Temporal]] ideas and speed up sequential access to data that we have strong reasoning to believe will be access soon. 

## Hitting and Missing data

When we want an address we first go to the cache. If the data exists in the l1 cache then it will be a hit and the data gets returned to the CPU. If the data does not exist in the [[L1 Cache]] then it will be a miss but the L1 cache will then ask the [[L2 Cache]] for the data. This process continues recursively until it has to go to disk. 

When data is being brought up from a lower level like disk to memory or memory to l2 cache it being it up in lines or blocks. 

We can describe the rate of success by hits / accesses and the miss rate by miss / accesses or 1 - hit rate. 

## Types of Physical Memory

- [[SRAM]] Static ram 
- [[DRAM]] Dynamic ram
- [[Magnetic Disk]]
- [[Flash Disks]]
- [[Magnetic Tape]]