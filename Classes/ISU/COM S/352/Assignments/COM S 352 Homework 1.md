#IowaStateUniversity
#ComputerScience 
#COMS352 
#Homework 

---

# [[COM S 352]] Homework 1

### 1 a

There is a context switch. The scheduler replaces the currently running process and replaces it with the next (based on some algo) process from the ready queue 

### 1 b

There is a context switch. The currently running process is placed into a blocked state the scheduler replaces it with the next ( based o some algo)


### 2.

Three programs are serviced in a multi programming system. Program A contains 50ms of computation followed by 100ms of I/O on hardware devices 1. program B contains 20ms of computation followed by 50 ms on hardware device 2. Program C contains 50ms of computation followed by 100ms I/O on hardware device 2.Each device can service only one I/O request at a tome.What is the minimum time it will take to complete all three programs   

| Time | A | B | C | Notes | 
| 0 | Ready | Ready | Running || 
| 50 | Running | Ready | Blocked | | 
| 100 | Blocked | Running | Blocked |  | 
| 120 | Blocked | Blocked | Blocked | | 
| 150 | Blocked | Blocked | | | 
| 170 | Blocked | | | | 
| 200 | | | | A is finished | 


### 3. 

Describe The purpose of each of the following terms 

System Call: A system library and transfer control to the OS in kernel mode 
Interrupt: signal from a hardware source that gives CPU control to the interrupt handler 
Trap: signal from a software source that gives CPU control to the interrupt handler 

### 4. 

What is the purpose of multiple privilege levels 

- We don't want the user process to be able to access each other's memory or the memory of the OS or other resources 
- When a process executes in user mode it is restricted. In what instructions it can execute. Only OS code executes in kernel mode 
- Advantage 
	- Single level: With a single level OS libraries can be called with a simple function calls.  
	- Multiple levels. We can restrict what user processes are able to do to protect memory and resources 
### 5. 

- The result of the loop is that the child forks a new process and this happens recursively 
- So an infinite number of processes are created 
- Eventually the system will run out of memory or process ids
- The parents call wait so they never terminates 

### 6 a

- The shell calls fork()
- Child calls exec() to run "grep COMS352 *"


### 6 b 

- pripe the standard out of one app into the standard in of another app. 
- Check with xv6-riscv code
