# A-Path-Finding
This repository contains an A* pathfinding algorithm implementation. The A* algorithm is a popular algorithm for finding the shortest path between two points on a graph. It is often used in video games, robotics, and other applications where efficient pathfinding is required.

## 1. Imports and Setup:
Imports: The code imports the pygame library for graphics, math for calculations, and PriorityQueue for implementing the A* algorithm.
Window Setup: It creates a window titled "A* Path Finding Algorithm" with a width of 800 pixels.
Colors: It defines various colors to represent different elements in the grid.

## 2. Spot Class:
This class represents individual squares in the grid.
It stores information like its position, color, neighbors, and width.
Methods allow for:
Checking its state (open, closed, barrier, start, end).
Resetting its color.
Marking it as a specific type of spot.
Drawing it on the Pygame window.
Updating its neighbors based on the grid.

## 3. Heuristic Function (h):
Estimates the distance between two points (used in pathfinding).
In this case, it simply uses the Manhattan distance (sum of horizontal and vertical distances).

## 4. Reconstruct Path Function:
Backtracks from the goal to the start using the came_from dictionary to trace the shortest path.
Colors each spot in the path purple for visual representation.

## 5. A Algorithm Implementation:*
Core logic for finding the shortest path using A*.
It involves:
Maintaining a priority queue of open spots to explore.
Tracking the cost to reach each spot (g_score) and the estimated total cost (f_score).
Iteratively exploring neighbors of the current spot and updating their scores.
Reconstructing the path once the goal is reached.

## 6. Grid Creation and Drawing Functions:
make_grid creates a 2D grid of Spot objects based on the given number of rows and width.
draw_grid draws the grid lines on the Pygame window.
draw draws the entire grid, including the spots, on the window.

## 7. User Input Handling:
The main function continuously listens for user input:
Mouse clicks to set start, end, and barriers.
Spacebar to start the pathfinding algorithm.
C key to clear the grid.

## 8. Main Loop:
The main function runs the main game loop, handling events and updating the display.
It handles user input, draws the grid, and calls the A* algorithm when needed.
