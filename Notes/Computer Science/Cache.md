#ComputerScience  #IowaStateUniversity  #COMS321 


[[Classes/ISU/COM S 321/COM S 321]] 

---

# Cache

Temporary way to store information to decrease time to get data.

## Uses

- [[DRAM]]
- [[SRAM]]
- [[L1 Cache]]
- [[L2 Cache]]

## Online Resources
- Wikipedia https://en.wikipedia.org/wiki/Cache_(computing)

## Types 

- [[Direct Mapping Cache]]
- [[Sets Associative Caches]]


## What to do in the event of a cache miss

If we are reading then we just recursively go to the next level. 

If we are writing then we need to propagate  down through the memory hierarchy to write data at all levels. This is handled in one of two possible ways 

- [[Write back caching]]
- [[Write through caching]] 
