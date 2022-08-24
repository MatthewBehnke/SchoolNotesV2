[[Iowa State University]] [[COM S 311]] [[2021-10-07]]

# Notes for 

## 1

- Run a BFS search from D to a node to find its level and then from the node to D and find its level. Then add the two levels together and that is the length to the first node. then repeat this for every node there after. Add up everything together and that is the length getafix has to travel. 

- One way to improve this would be to store the level from D to every node along the path and then use a hashmap to take a shortcut. 


- Run bfs once to find every nodes. Then from every other node run bfs to find the level from that house to D. At most we would run BFS only the number of houses plus 1 or garfilds house.  the Runtime of this algo would be O(V(V+E))

## 2

We are checking for the existatense of a vertex in any graph that can be reached by every other vertex. 

This might be able to be done by a modified BFS or DFS


Idea on how to do this

Store the graph as a matrix 
Take the inverse of the graph
Check for a mother

Should be able to be done in O(V + E) Time

## 3

Run BFS but then any node that visited == true then it holds true.

O(V + E) at max

### 4

