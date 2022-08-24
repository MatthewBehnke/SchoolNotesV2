
#ComputerScience  #IowaStateUniversity  #COMS311 


[[COM S 311]] 

---

# Greedy Algorithm Scheduling

```
Sort the J in ascending order of their end time J'
start time = 0
for  i = 1 to |J'|
	if J'[i] starttime => starttime
		starttime = J'[i].endtime
		add J'[i] to soluution set
return solution set

```



 Interval Scheduling  or  job scheduling (set of jobs to do)
- Each job has 
	- start time 
	- end time
- No over lapping jobs
- Objective is to select the max number of non overlapping jobs

###  Optimal Substructure Property 

L is a set of intervals (jobs)
OPT is  a subset of L which is the max subset of non overlapping jobs
OPT $I_{j1}, I_{j2} ... I_{jn}$
Let L' be some set of intervals that appear after all intervals in L
If OPT' is a subset of L' : minimal subset of non overlapping jobs 
$OPT\ \cup\ OPT'$ is the maximal subset of a intervals in $L \cup L'$.

So what is the greedy choice property? 

Let $I_{j1}$ $I_{j2}$ ,...,$I_{jn}$ the jobs that re part of the optimal solution. $I_{jth}$ is the non-overlapping job w/ the earliest end time. 


Let OPT be the solution set ordering according to endtime' 
Let Greedy "  " "  "  " " generated using greedy choice property.
Let the first k jobs match in OPT & Greedy
$I_{K+1}: K + 1$ the job in OPT
$I'_{K+1}: K + 1$ the job in Greedy
$I_{K+1} \not= I_{K+1}$

endtime($I_{K+1}$) $\geq$ endtime($I'_{K+1}$)

Replace in OPT  $I_{K+1}$ with $I'_{k+1}$ (because ' has the earliest endtime). 

This will result in another optional $sot^n$ $OPT'$

OPT' ad greedy matches in the first k+1 jobs. 