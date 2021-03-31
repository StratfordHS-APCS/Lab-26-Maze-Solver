# Lab 26 - Maze Solver

### Directions

A maze is a two dimensional structure with an entrance and sometimes an exit.  The job for this program is to determine if the given maze has an exit.  All of the mazes will have the entrance point at the top left corner.  The exit point can be anywhere in the far right column.   A valid path will be a continuous block of 1s that connect the top left corner to any spot on the far right column.  A valid path can only be connected horizontally or vertically.  Diagonal connections are not legal.  The 1s in the file represent the path and 0s represent the walls of the maze.  Output `exit found` if there is a path leading to an exit out of the maze.  Output `exit not found` if there is not a path leading out of the maze.  Also, print out the maze.

### Assumptions

All input will be 1s and 0s.  The 1s represent the path and 0s show that there is no path in that area.  Open `maze.dat` to see the input format.

### Sample Output
```
1 0 0 0 1
1 1 1 1 0
0 0 1 0 1
0 1 1 1 0
0 0 0 0 1
exit not found

1 0 0 0 0 1 1
1 1 1 1 0 1 0
0 0 1 0 0 1 0
0 1 1 1 0 1 0
0 1 0 1 0 1 0
0 1 0 1 1 1 0
0 1 0 1 0 0 1
exit found

1 0 0 0 0 1 0
1 1 1 1 0 1 0
0 0 1 0 0 1 0
0 1 1 1 0 1 0
0 1 0 1 0 1 0
0 1 0 1 1 1 0
0 1 0 1 0 1 0
exit not found

1 0 1 1 0 1 0
1 1 1 1 1 1 0
0 0 1 0 0 0 1
0 1 1 1 1 1 1
0 1 0 1 0 1 0
1 1 1 1 1 1 0
0 1 0 1 0 1 0
exit found

1 0 1 1 0 1 0 1 1 1
1 1 1 1 1 1 0 1 0 1
0 0 1 0 0 0 1 1 1 1
0 1 1 1 1 1 1 1 0 1
0 1 0 1 0 1 0 1 0 1
1 1 1 1 1 1 0 1 1 1
0 1 0 1 0 1 0 0 0 1
0 1 1 1 0 1 0 0 0 0
0 1 0 1 0 1 0 1 1 1
0 1 1 1 1 1 0 1 1 1
exit found

1 0 1 1 0 1 1 1 1 0
1 1 1 1 1 1 0 1 0 1
0 0 1 0 0 0 1 1 1 0
0 1 1 1 1 1 1 1 0 1
0 1 0 1 0 1 0 1 0 1
1 1 1 1 1 1 0 1 1 0
0 1 0 1 0 1 0 0 0 0
0 1 1 1 0 1 0 0 1 1
0 1 0 1 0 1 0 1 1 1
0 1 1 1 1 1 0 1 1 1
exit not found

1 1 1 1
1 1 1 1
1 1 1 1
1 1 1 1
exit found


0 0 0 0
0 0 0 0
0 0 0 0
0 0 0 0
exit not found
```

### Algorithm Help
```
if ( row and col are in bounds and current spot is a 1 )
   mark spot as visited
   if we are at the exit
       mark exit found as true
   else
       4 recursive calls up down left right
```

### Extra Challenge (optional)

1. Output the number of steps for the shortest path.
2. Show the path taken on the printed maze.
