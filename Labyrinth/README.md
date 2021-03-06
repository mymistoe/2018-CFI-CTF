# Labyrinth

> programming

Author: [filedesless](https://github.com/filedesless)

`localhost:24001`

You have 2 seconds to send back a valid path between S and E
(ex: RIGHT,RIGHT,RIGHT,DOWN,RIGHT,RIGHT,UP,UP,UP,UP,UP,LEFT)

Here are some interesting reads: 

 - https://docs.python.org/3/library/socket.html
 - https://en.wikipedia.org/wiki/Algorithm

## Setup

Requirements:
- docker

Start:

```shell
docker-compose up
```

## Writeup

The challenge is a service running on port 24001, the user have to connect to it with a tool like netcat.

```
λ $ nc localhost 24001
You have 2 seconds to send back a valid path between S and E
(ex: RIGHT,RIGHT,RIGHT,DOWN,RIGHT,RIGHT,UP,UP,UP,UP,UP,LEFT)
+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+
+,+, , , ,+, , , , , , , ,+, , , ,+, , , ,+, , , , , , , ,+, , , , , ,+, , , , , , , ,+, , , , , , , , , , , , , , , , , ,+, , , , , , , , , ,+, , , , , , , , , ,+, , , , , ,+,+
+,+,+,+, ,+, ,+,+,+, ,+,+,+, ,+, ,+, ,+, ,+, ,+, ,+,+,+, ,+, ,+,+,+, ,+, ,+,+,+,+,+, ,+, ,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+, ,+,+,+,+,+, ,+,+,+, ,+, ,+, ,+,+,+,+,+,+,+, ,+, ,+,+,+,+
+,+, , , ,+, , , ,+, , , , , ,+, ,+, ,+, , , ,+, , , ,+, , , ,+, ,+, ,+, , , , , ,+, , , ,+, , , , , , , , , , , , , ,+, , , ,+, , , ,+, ,+, ,+, ,+, , , , , ,+, , , ,+, , , ,+,+
+,+, ,+,+,+,+,+, ,+,+,+,+,+,+,+, ,+, ,+,+,+,+,+,+,+, ,+,+,+,+,+, ,+, ,+,+,+,+,+, ,+,+,+,+,+, ,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+, ,+, ,+,+,+, ,+, ,+,+,+,+,+, ,+, ,+, ,+,+,+,+,+, ,+,+
+,+, ,+, , , , , ,+, , , ,+, ,+, , , ,+, ,+, , , , , ,+, , , , , ,+, ,+, , , ,+, , , ,+, , , , , , , , , , , ,+, , , , , , , ,+, ,+, , , ,+, , , , , ,+, ,+, , , ,+, ,+, , , ,+,+
+,+, ,+, ,+,+,+,+,+, ,+, ,+, ,+,+,+,+,+, ,+, ,+,+,+,+,+,+,+, ,+,+,+, ,+, ,+, ,+,+,+, ,+,+,+, ,+,+,+,+,+,+,+, ,+, ,+,+,+,+,+,+,+, ,+, ,+, ,+,+,+,+,+, ,+,+,+,+,+, ,+, ,+, ,+,+,+,+
+,+, ,+, ,+, , , , , ,+, ,+, , , ,+, , , ,+, ,+, , , , , ,+, , , , , ,+, ,+, , , ,+, , , ,+, , , , , ,+, , , ,+, ,+, , , , , , , ,+, ,+, , , , , ,+, , , , , ,+, ,+, ,+, , , ,+,+
+,+, ,+, ,+, ,+,+,+,+,+, ,+, ,+, ,+,+,+, ,+, ,+, ,+,+,+, ,+, ,+,+,+,+,+, ,+,+,+, ,+,+,+, ,+, ,+,+,+,+,+, ,+,+,+, ,+, ,+, ,+,+,+,+,+, ,+,+,+,+,+, ,+,+,+,+,+, ,+, ,+, ,+,+,+, ,+,+
+,+, ,+, ,+, , , , , ,+, , , ,+, , , ,+, ,+, ,+, , , ,+, ,+, , , ,+, , , , , ,+, , , , , ,+, ,+, , , , , ,+, , , ,+, ,+, , , ,+, , , ,+, ,+, , , , , ,+, , , ,+, , , , , ,+, ,+,+
+,+, ,+, ,+,+,+,+,+, ,+,+,+,+,+,+,+, ,+, ,+, ,+,+,+, ,+, ,+,+,+, ,+,+,+,+,+, ,+,+,+,+,+,+,+,+,+, ,+,+,+, ,+, ,+,+,+,+,+,+,+, ,+, ,+,+,+, ,+, ,+,+,+,+,+, ,+,+,+,+,+,+,+, ,+, ,+,+
+,+, ,+, ,+, , , , , ,+, , , , , , , ,+, ,+, ,+, , , ,+, , , ,+, , , , , ,+, ,+, , , ,+, , , ,+, , , ,+, ,+, , , , , ,+, , , ,+, ,+, , , ,+, , , , , ,+, , , , , ,+, , , ,+, , ,E
+,+, ,+, ,+, ,+,+,+,+,+, ,+,+,+,+,+,+,+, ,+, ,+, ,+,+,+,+,+, ,+,+,+,+,+, ,+, ,+, ,+, ,+, ,+, ,+,+,+, ,+,+,+,+,+,+,+, ,+, ,+,+,+, ,+, ,+,+,+,+,+,+,+, ,+,+,+,+,+, ,+,+,+,+,+, ,+,+
+,+, ,+, ,+, ,+, , , , , , , , , ,+, , , ,+, , , ,+, , , , , ,+, ,+, , , ,+, ,+, ,+, , , ,+, , , , , ,+, , , , , ,+, , , ,+, ,+, ,+, , , , , , , ,+, , , ,+, , , ,+, , , ,+, ,+,+
+,+, ,+, ,+, ,+,+,+,+,+,+,+,+,+, ,+, ,+,+,+,+,+,+,+, ,+,+,+,+,+, ,+, ,+,+,+, ,+, ,+,+,+,+,+,+,+,+,+,+,+, ,+, ,+,+,+,+,+,+,+, ,+, ,+,+,+, ,+,+,+, ,+,+,+, ,+, ,+,+,+, ,+, ,+, ,+,+
+,+, ,+, ,+, , , ,+, , , ,+, , , , , ,+, , , , , , , ,+, , , , , ,+, , , , , ,+, , , ,+, , , , , ,+, , , ,+, , , , , , , ,+, , , , , , , ,+, , , , , ,+, ,+, , , , , ,+, , , ,+,+
+,+, ,+, ,+, ,+, ,+, ,+, ,+,+,+,+,+,+,+, ,+,+,+,+,+,+,+,+,+, ,+,+,+,+,+,+,+,+,+, ,+, ,+, ,+,+,+, ,+, ,+,+,+,+,+,+,+,+,+, ,+, ,+,+,+,+,+,+,+,+,+,+,+, ,+, ,+,+,+,+,+,+,+,+,+, ,+,+
+,+, , , ,+, ,+, , , ,+, ,+, , , , , , , ,+, , , , , , , ,+, , , , , , , , , ,+, ,+, ,+, ,+, ,+, , , ,+, , , , , , , ,+, , , , , ,+, , , , , , , ,+, ,+, , , , , ,+, ,+, , , ,+,+
+,+, ,+,+,+,+,+,+,+,+,+, ,+, ,+,+,+,+,+,+,+, ,+, ,+,+,+, ,+,+,+,+,+, ,+,+,+, ,+, ,+, ,+, ,+, ,+,+,+,+,+, ,+,+,+, ,+,+,+,+,+,+,+,+,+, ,+,+,+,+,+, ,+,+,+, ,+,+,+, ,+, ,+, ,+,+,+,+
+,+, , , ,+, , , , , , , ,+, , , , , ,+, , , ,+, ,+, ,+, , , , , , , ,+, , , ,+, ,+, ,+, ,+, ,+, , , , , , , ,+, ,+, , , , , , , ,+, , , ,+, ,+, , , , , ,+, ,+, , , ,+, , , ,+,+
+,+,+,+, ,+, ,+,+,+,+,+, ,+,+,+,+,+, ,+,+,+,+,+, ,+, ,+,+,+, ,+,+,+,+,+,+,+, ,+,+,+, ,+, ,+, ,+, ,+,+,+,+,+,+,+, ,+, ,+,+,+,+,+, ,+,+,+, ,+, ,+,+,+,+,+,+,+, ,+,+,+, ,+,+,+, ,+,+
+,+, ,+, , , ,+, ,+, , , ,+, , , ,+, ,+, , , , , ,+, , , , , ,+, , , , , ,+, , , , , ,+, ,+, , , , , , , ,+, , , ,+, , , , , ,+, , , ,+, ,+, , , ,+, , , , , ,+, , , , , ,+, ,+,+
+,+, ,+,+,+,+,+, ,+, ,+,+,+, ,+, ,+, ,+, ,+,+,+,+,+,+,+,+,+,+,+, ,+,+,+, ,+,+,+,+,+, ,+, ,+,+,+, ,+,+,+,+,+, ,+, ,+,+,+,+,+, ,+,+,+, ,+, ,+, ,+, ,+, ,+,+,+, ,+, ,+,+,+,+,+, ,+,+
+,+, , , ,+, ,+, , , ,+, , , ,+, ,+, ,+, , , , , , , , , ,+, , , , , ,+, ,+, , , ,+, ,+, , , ,+, ,+, , , , , ,+, , , , , ,+, , , ,+, , , ,+, ,+, , , ,+, ,+, , , ,+, , , , , ,+,+
+,+, ,+, ,+, ,+, ,+,+,+, ,+,+,+,+,+, ,+, ,+,+,+,+,+,+,+, ,+, ,+,+,+,+,+, ,+, ,+,+,+, ,+,+,+, ,+, ,+, ,+,+,+,+,+,+,+,+,+, ,+,+,+, ,+, ,+,+,+,+,+, ,+,+,+, ,+,+,+,+,+, ,+,+,+,+,+,+
+,+, ,+, , , ,+, ,+, , , , , ,+, , , ,+, , , , , ,+, ,+, ,+, ,+, , , , , ,+, , , , , ,+, , , ,+, ,+, , , ,+, , , , , ,+, ,+, ,+, ,+, ,+, , , ,+, ,+, , , ,+, , , , , ,+, , , ,+,+
+,+, ,+,+,+,+,+, ,+, ,+,+,+, ,+, ,+,+,+,+,+,+,+, ,+, ,+, ,+, ,+, ,+,+,+,+,+,+,+,+,+,+,+, ,+,+,+, ,+,+,+, ,+,+,+, ,+,+,+, ,+, ,+, ,+,+,+, ,+, ,+, ,+,+,+, ,+, ,+,+,+,+,+,+,+, ,+,+
+,+, ,+, , , , , ,+, ,+, ,+, ,+, ,+, , , , , ,+, , , ,+, , , ,+, , , , , , , ,+, , , , , ,+, ,+, ,+, ,+, , , ,+, , , , , ,+, ,+, , , ,+, ,+, ,+, , , , , ,+, ,+, , , , , , , ,+,+
+,+, ,+, ,+,+,+,+,+, ,+, ,+, ,+, ,+,+,+,+,+, ,+,+,+, ,+,+,+,+,+,+,+,+,+,+,+, ,+, ,+,+,+,+,+, ,+, ,+, ,+,+,+, ,+, ,+,+,+,+,+, ,+,+,+, ,+, ,+, ,+, ,+,+,+,+,+, ,+, ,+,+,+,+,+,+,+,+
+,+, ,+, ,+, , , , , ,+, ,+, ,+, , , ,+, , , ,+, , , ,+, ,+, , , , , , , ,+, ,+, , , ,+, , , , , , , ,+, , , ,+, ,+, , , , , , , ,+, ,+, ,+, ,+, ,+, , , , , ,+, , , , , , , ,+,+
+,+, ,+, ,+, ,+,+,+,+,+, ,+, ,+,+,+, ,+, ,+,+,+, ,+,+,+, ,+, ,+, ,+,+,+, ,+, ,+,+,+, ,+,+,+,+,+, ,+,+,+, ,+,+,+, ,+, ,+,+,+, ,+, ,+, ,+, ,+, ,+,+,+, ,+,+,+,+,+,+,+, ,+,+,+, ,+,+
+,+, , , ,+, , , , , , , ,+, , , ,+, ,+, ,+, , , ,+, , , ,+, ,+, ,+, ,+, ,+, ,+, , , ,+, , , ,+, ,+, , , ,+, , , ,+, , , ,+, ,+, ,+, , , ,+, , , , , ,+, , , , , ,+, ,+, ,+, ,+,+
+,+, ,+,+,+,+,+,+,+, ,+,+,+,+,+, ,+, ,+, ,+, ,+,+,+, ,+, ,+, ,+, ,+, ,+, ,+, ,+, ,+,+,+, ,+, ,+,+,+, ,+,+,+, ,+,+,+,+,+, ,+, ,+,+,+,+,+,+,+,+,+,+,+,+,+, ,+,+,+, ,+, ,+, ,+, ,+,+
+,+, ,+, , , , , ,+, ,+, , , ,+, ,+, ,+, , , ,+, , , ,+, , , ,+, ,+, , , ,+, ,+, ,+, , , ,+, , , , , ,+, ,+, , , ,+, , , ,+, , , , , , , ,+, , , , , , , ,+, , , ,+, , , ,+, ,+,+
+,+, ,+,+,+, ,+, ,+,+,+, ,+, ,+, ,+, ,+,+,+, ,+,+,+,+,+,+,+,+,+, ,+, ,+,+,+, ,+, ,+,+,+, ,+,+,+,+,+,+,+, ,+,+,+, ,+,+,+,+,+,+,+,+,+, ,+, ,+,+,+,+,+, ,+,+,+, ,+,+,+,+,+,+,+, ,+,+
+,+, , , , , ,+, , , , , ,+, , , ,+, , , ,+, , , ,+, , , , , , , ,+, , , ,+, ,+, , , , , ,+, , , ,+, , , , , ,+, ,+, , , ,+, , , , , ,+, , , , , , , ,+, ,+, , , , , , , , , ,+,+
+,+,+,+,+,+,+,+,+,+, ,+,+,+,+,+,+,+,+,+, ,+,+,+, ,+, ,+,+,+,+,+,+,+,+,+, ,+, ,+,+,+,+,+,+,+, ,+, ,+, ,+,+,+, ,+, ,+, ,+, ,+, ,+,+,+, ,+,+,+,+,+,+,+,+,+, ,+,+,+,+,+,+,+,+,+, ,+,+
S, , , , ,+, , , , , ,+, , , , , , , , , ,+, , , ,+, ,+, , , , , , , , , ,+, , , , , , , ,+, ,+, ,+, ,+, ,+, ,+, , , ,+, ,+, ,+, , , ,+, , , , , , , ,+, , , , , , , ,+, , , ,+,+
+,+,+,+, ,+,+,+,+,+,+,+, ,+,+,+,+,+,+,+,+,+, ,+,+,+, ,+, ,+,+,+,+,+,+,+,+,+, ,+,+,+,+,+, ,+, ,+, ,+, ,+, ,+, ,+,+,+,+,+, ,+, ,+, ,+,+,+, ,+,+,+,+,+, ,+,+,+, ,+,+,+, ,+, ,+,+,+,+
+,+, , , ,+, , , ,+, , , ,+, , , , , , , ,+, ,+, , , ,+, ,+, , , , , , , ,+, ,+, , , , , ,+, ,+, , , ,+, ,+, ,+, , , ,+, ,+, ,+, , , ,+, , , ,+, ,+, , , ,+, ,+, , , ,+, , , ,+,+
+,+, ,+,+,+, ,+, ,+, ,+,+,+, ,+, ,+,+,+, ,+, ,+,+,+, ,+, ,+,+,+, ,+,+,+, ,+, ,+,+,+,+,+, ,+, ,+,+,+,+,+, ,+, ,+, ,+,+,+, ,+, ,+, ,+,+,+,+,+, ,+, ,+,+,+, ,+, ,+, ,+,+,+,+,+, ,+,+
+,+, ,+, , , ,+, , , ,+, ,+, ,+, ,+, , , ,+, , , , , ,+, , , ,+, , , ,+, ,+, ,+, , , ,+, , , ,+, , , , , , , ,+, , , ,+, ,+, ,+, ,+, , , ,+, , , , , ,+, ,+, ,+, , , , , , , ,+,+
+,+, ,+,+,+, ,+,+,+,+,+, ,+, ,+, ,+,+,+, ,+,+,+,+,+,+,+,+,+, ,+, ,+,+,+, ,+, ,+, ,+, ,+,+,+,+,+,+,+,+,+, ,+,+,+,+,+, ,+, ,+, ,+,+,+, ,+, ,+,+,+,+,+, ,+, ,+, ,+,+,+,+,+,+,+,+,+,+
+,+, , , ,+, ,+, , , , , ,+, ,+, , , ,+, , , , , , , ,+, , , ,+, ,+, , , ,+, ,+, ,+, ,+, , , , , , , ,+, , , , , , , ,+, ,+, , , , , ,+, , , ,+, , , ,+, ,+, , , ,+, , , , , ,+,+
+,+,+,+, ,+, ,+, ,+,+,+,+,+, ,+,+,+, ,+,+,+,+,+, ,+,+,+, ,+,+,+,+,+, ,+, ,+, ,+, ,+, ,+, ,+,+,+,+,+, ,+,+,+,+,+,+,+, ,+, ,+,+,+,+,+, ,+, ,+,+,+, ,+,+,+, ,+,+,+, ,+, ,+,+,+,+,+,+
+,+, , , ,+, ,+, , , ,+, , , ,+, ,+, , , ,+, , , ,+, , , ,+, , , , , ,+, ,+, ,+, ,+, , , ,+, , , ,+, , , ,+, , , , , ,+, , , , , ,+, ,+, , , , , , , ,+, ,+, ,+, ,+, , , , , ,+,+
+,+, ,+,+,+, ,+, ,+, ,+, ,+,+,+, ,+,+,+, ,+,+,+,+,+, ,+,+,+,+,+, ,+,+,+, ,+, ,+, ,+,+,+,+,+, ,+, ,+,+,+, ,+,+,+,+,+,+,+,+,+,+,+, ,+,+,+,+,+,+,+,+,+, ,+, ,+, ,+, ,+, ,+,+,+, ,+,+
+,+, , , , , ,+, ,+, , , ,+, , , ,+, , , ,+, , , , , ,+, , , ,+, ,+, ,+, ,+, , , ,+, , , ,+, ,+, ,+, , , ,+, , , , , , , , , ,+, , , , , , , ,+, , , ,+, ,+, , , ,+, ,+, , , ,+,+
+,+,+,+,+,+,+,+, ,+,+,+,+,+,+,+, ,+, ,+,+,+, ,+,+,+,+,+, ,+, ,+, ,+, ,+, ,+,+,+,+,+, ,+, ,+, ,+, ,+, ,+,+,+, ,+,+,+,+,+,+,+, ,+,+,+,+,+,+,+, ,+,+,+,+,+, ,+, ,+,+,+,+,+, ,+, ,+,+
+,+, , , , , , , , , , , , , , , ,+, , , , , , , , , , , ,+, , , ,+, , , , , , , , , ,+, , , ,+, ,+, , , , , , , , , , , ,+, , , , , , , , , , , , , , , ,+, , , , , , , ,+, ,+,+
+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+,+
```

The user is given a CSV maze, where " " stands for a passage, "+" for a wall, "S" for start and "E" for exit. He has to find a way to solve the maze. This can be done using Depth-First Search<sup>[1]</sup>. You start by exploring a random path, stacking cells and marking them visited as you traverse them, and when confronted to a dead-end, backtrack by popping cells until you find yourself able to explore another unvisited cell. Repeat until you get to the exit.

Here's an excerpt of the source code illustrating the backtracking algorithm:

```python
def solve(m: Maze) -> List[Cell]:
    start = [ c for c in m.cells() if c.val is "S" ][0]
    stack = [ start ]

    cell = stack.pop()
    while cell.val is not "E":
        cell.visited = True
        neighbors = [ c for c in m.neighbors(cell, 1) 
                if c.val is not "+" and not c.visited ]

        if len(neighbors) > 0:
            stack.append(cell)
            stack.append(neighbors[0])

        cell = stack.pop()
    
    return stack
```

From there it's only a matter of connecting via a socket, parsing the maze, and sending back the path in the proper format. Example of this can be found scattered between `src/client.py` (which spits out the flag), `src/solver.py` (which implements logic) and `src/maze.py` (for shared utilities). You then get rewarded with the flag:

`CFI{85AEAEB2534F45A4931117C5CEA07348}`

refs:

1. https://en.wikipedia.org/wiki/Depth-first_search
