#ComputerScience  #IowaStateUniversity  #COMS311 


[[COM S 311]] 

---

# Bellman-Ford Algorithm


Uses [[Relaxation]]

$SD(t,i) = min \{SD(t, s-i), min\{SD(u , i - 1) + ut(u,t) | u-> t\}\}$
$SD(t,0) = 0$

$\forall t : SD(t, |V| -1)$

## Algo
$\forall v \in V dict[v][0] = \infty$
$dict[s][0] = 0$

$for\ i = 1\ to\ |v| - 1 \{$
$\ \ \ \ \ for\ each\ v \in V\{$
$\ \ \ \ \ \ \ \ \ \ for\ each\ u\ ->\ v\ \in E\  \{$
$\ \ \ \ \ \ \ \ \ \ \ \ \ \ \ dict[v][i] = min\{dict[v][i-1], dict[u][i-1] + wt(u,v)\}$
$\ \ \ \ \ \ \ \ \ \ \}$
$\ \ \ \ \ \}$
$\}$

## Example 

A directed graph

|     | s   | a   | b   | c   | d   | e   |
| --- | --- | --- | --- | --- | --- | --- |
| s   | 0   | 5   |     | -2  |     |     |
| a   |     | 0   | 1   |     |     |     |
| b   |     |     | 0   |     | 8   |     |
| c   |     |     | 4   | 0   | 4   |     |
| d   |     |     |     |     | 0   | 1   |
| e   |     |     |     |     |     | 0   |


|     | s   | a              | b                    | c            | d                         | e                              |
| --- | --- | -------------- | -------------------- | ------------ | ------------------------- | ------------------------------ |
| 0   | 0   | $\infty$       | $\infty$             | $\infty$     | $\infty$                  | $\infty$                       |
| 1   | 0   | 5  (s -> a)    | $\infty$             | -2  (s -> a) | $\infty$                  | $\infty$                       |
| 2   | 0   | 0 (s-> c -> a) | 2 (s -> c -> b)      | -2  (s -> a) | 2 (s -> c -> d)           | $\infty$                       |
| 3   | 0   | 0 (s-> c -> a) | 1 (s -> c -> a -> b) | -2  (s -> a) | 1 (s -> c -> b -> d)      | 3 (s -> c -> d -> e )          |
| 4   | 0   | 0 (s-> c -> a) | 1 (s -> c -> a -> b) | -2  (s -> a) | 0 (s -> c -> a -> b -> d) | 2 (s -> c -> b -> d -> e)      |
| 5   | 0   | 0 (s-> c -> a) | 1 (s -> c -> a -> b) | -2  (s -> a) | 0 (s -> c -> a -> b -> d) | 1 (s -> c -> a -> b -> d -> e) | 

