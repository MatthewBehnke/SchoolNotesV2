#ComputerScience  #IowaStateUniversity  #COMS321 


[[Classes/ISU/COM S 321/COM S 321]] 

---

# Measuring Performance

* CPU time = CPU clock cycles *  clock cycle time
* Clock cycle time = $\frac{1}{clock\ rate}$
* CPU time = $\frac{CPU\ clock\ cycles}{clock\ rate}$

## To improve Performance

* Increase clock cycle rate (hardware)
* Decrease number of clock cycles (software probably)

## The CPU performance Equation
CPU TIME = $\frac{Instruction\ Count\ \times\ cycles\ per\ instruction}{clock\ cycles}$

Examples: 

A processor has 3 classes of instructions
* Perhmps 
* integer
* memory

Instructions per class
* A takes 3 cycles
* B takes 1 cycle
* C takes 4 cycles

Programs 1 + 2 compute the same thing but they use different implementations

|           | Class A | Class B | Class C |
| --------- | ------- | ------- | ------- |
| program 1 | 10000   | 10000   | 10000   |
| program 2 | 12000   | 10900   | 80000   |
      
What program is faster

Assume cycle rate is 3.5 GHz

(10000 * 3 + 10000 * 1 + 10000 * 4) / 3.5 GHz = 80000/3.5Ghz - Program 1

(12000 * 3 + 10599 * 1 + 80000 * 4)/ 3.5 GHz = 78500/3.5GHz - Program 2


---

TIME = $\frac{Seconds}{Program}$ = $\frac{Instructions}{Program} \times \frac{Clock\ Cycles}{Instructions} \times \frac{seconds}{clock\ cycles}$ 


---

[[The Power Wall]]