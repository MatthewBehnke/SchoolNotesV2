#ComputerScience  #IowaStateUniversity  #COMS321 


[[COM S 321]] 

---


# Cache Design

we must decide if [[cache]] is physical, virtual, or hybrid

- Cache is entirely physical
	- Must resolve physical addresses before going to the cache
- Cache is entirely virtual
	- Addresses are not unique 
	- Very complex and expensive (not used at all)
- Cache is virtually indexed and physically tagged
	- Index and offset bits are virtual and available immediately
	- Virtual addresses register begins in parallel with cache access   
	- When addresses are resolved compare physical tag
- Cache is physically indexed and virtually tagged
	- does not make sense (not used at all) 

## Uses
- [[Virtual Memory]]

## Online Resources

## Examples 

### 64 bit 	
64 bit virtual address space 
8 GB 2^32 byte physical memory 
4kB pages (2^12 bytes each)

64 but address space / 2^12 page size -> 52 bit pages numbers  -> 2^52 pages

