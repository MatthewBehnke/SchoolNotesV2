#ComputerScience  #IowaStateUniversity  #COMS321 


[[COM S 321]] 

---

# Program Performance

##  Items that affect program performance

* Choice of Algorithm
* Language 
	* `Python` is slow
	* `C` is faster
* Compiler
	* [GCC](https://en.wikipedia.org/wiki/GNU_Compiler_Collection) is king
* Architecture ([ISA Instruction set architecture](https://en.wikipedia.org/wiki/Instruction_set_architecture))
	Kinda like an API for a processor
* Architecture ([Microarchitecture](https://en.wikipedia.org/wiki/Microarchitecture))
	- Microarchitecture implements the ISA
	- I/O + Memory systems
		- L1/2/3 & system cache 	

## How did computers become so fast?

- Design for the future!
	- Forces the rest of the industry to keep up
	- Industry [Roadmap for the future](https://en.wikipedia.org/wiki/International_Technology_Roadmap_for_Semiconductors)
		-	The document exists to push both sides
			-	Semiconductor manufactures (TMSC)
			-	The plant manufactures
	-	Use abstraction effectively
		EX: team designs a component then able to place those components effectively
	-  Design for the common case
		Applies to software as well
		-  Don't worry about the things that happen rarely
		-  Focus on things that happen all the time
		- Premature optimization is the root of all evil 
	- Exploit parallelism
		- Recognize that as an instruction runs it does not use the whole chip so design 
		  Chip that can be used effectively 
  	- Predict
		- Most of the time you will need the next instruction not some random instruction
		- Helpful to be right most of the time
		- Use cache to access information fast
	- [[Locality]]
	- Use hierarchical structures 
		- L1 cache - N 10 cycles 
		- L2 cache - N 100 
		- L3 cache - N 1000
	- Be dependable
		- cross talk
		- em noise 
		- alpha particles (terrestrial radiation )
		- Cosmic rays (Gamma particles)
***

#ComputerScience #Machine-LevelPrograming #ComputerArchitecture