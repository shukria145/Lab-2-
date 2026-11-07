# Lab-2-## Section 7: Compare BFS and DFS

Here are the results from running the code:

| Algorithm | Path Length | Maximum Frontier |
| :--- | :--- | :--- |
| *BFS* | 8 | 13 |
| *DFS* | 14 | 9 |

### Answer these questions:

**1. Which algorithm found the shorter path?**  
  BFS found the shorter path.

 **2. Which algorithm had the larger maximum frontier?**  
BFS had the larger maximum frontier.

 **3. Why did the two algorithms produce different paths on the same maze?**  
 Because BFS explores level-by-level (FIFO) to find the shortest route, while DFS dives deep into one branch as far as possible before backtracking (LIFO).

 **4. Does DFS always produce the shortest path? Why or why not?**  
No. DFS just finds a path; it doesn't check if it's the shortest because it stops as soon as it hits the goal, even if it took a long route.

 **5. Does BFS always produce the shortest path when every movement costs 1? Why?**  
 Yes. Because it explores all nodes at the current depth before moving deeper, it is guaranteed to find the goal in the fewest possible steps.

---
g
## Section 9: Experiment 2 — Change start and goal

### Answer these questions:

> *1. Does BFS's path length ever change if you re-run it with the same start/goal? Does DFS's?*
> BFS will never change (it's always the shortest). DFS might change if you change the order of the directions list, but if the code stays exactly the same, re-running it will give the same path.

> *2. As the distance between start and goal grows, what happens to the maximum frontier size for each algorithm?*
> For BFS, the frontier grows much faster (it expands in a wide circle). For DFS, the frontier grows much slower (it only remembers the path it's currently on).

> *3. Can you find a (start, goal) pair where BFS and DFS return the same path? What does that tell you about the maze structure?*
> Yes (e.g., if the goal is right next to the start). It tells us that there is only one direct, unobstructed path between them, so both algorithms are forced to take the same route.

> *4. What happens if goal is unreachable from start (e.g. sealed off by walls)? Try it — what do bfs() and dfs() return?*
> They will eventually explore the entire open space, the frontier will become empty, the while loop will end, and the function will return None
