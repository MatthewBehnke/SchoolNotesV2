## Direct mapping cache

Addresses are broken into 3 parts;
- Tag: Highest order bits used to check if write got the right data
- Index: middle bits used to select a line in the code
- offset: Lowest order bits used to select data within a line  (indexes a line)


## Examples

#### Cache 
is 8 KB
Lines are 64 bytes
direct mapped


How many lines? 
What are the tag, index and offset bits

1 KB  = 1024 bytes = $2^{10}$
8 KB  = $2^{13}$ bytes 

64 bit lines  = $2^{6}$ bytes

$2^{13}/2^6$ = $2^{7}$ = 128 lines

6 bit offset 
7 bit index

64 - 13 = 51 bit tag

Bit per line - value bit - keeps track of input or highest info in line is valid.

#### Cache

is 16 KB
Lines are 256 bytes
direct mapped

How many lines? 
What are the tag, index, and offset bits? 
How much overhead is required? 

16KB  = $2^{14}$ bytes
256 bytes lines  = $2^{8}$ bytes

$2^{14} / 2^8$ = $2^6$ lines

tag = 50
index = 6 
offset  = 8

50 bits for tag + 1 valid $\times 2^6$ = overhead
51 $\times 2^3$ bytes overhead
408 bytes overhead

#### cache 

tag = 48 bit
index = 9 bit
offset = 7 bit

Line length = $2^7$ = 128 bits long
there are $2^9$ = 512 lines 
the cache is $2^9$ x $2^9$ = $2^{18}$ = {5536} bytes = 64 KB

overhead (48 tag buts + 1 ) $\times 2^9$ = 49 $\times 2^9$ = 49 $\times 2^6$ = 3136 bytes overhead 