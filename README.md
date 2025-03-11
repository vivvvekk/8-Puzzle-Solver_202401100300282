# 8 Puzzle Solver

## Introduction
The 8-puzzle is a well-known problem in artificial intelligence that consists of a 3x3 grid with eight numbered tiles and one empty space. The goal is to move the tiles around using the empty space to achieve a desired goal configuration.

## Problem Statement
The challenge is to find the shortest sequence of moves that transforms a given **initial state** into the **goal state** by shifting tiles into the empty space. The valid moves include shifting a tile **Up, Down, Left, or Right** into the empty space.

### Example
#### **Initial State:**
```
1 2 3
4 0 5
6 7 8
```
#### **Goal State:**
```
1 2 3
4 5 6
7 8 0
```

## Methodology
To efficiently solve the problem, we use the **A* (A-star) search algorithm** combined with the **Manhattan Distance heuristic**, ensuring an optimal and efficient solution.

### **Approach:**
1. **State Representation:** The puzzle is represented as a 3x3 matrix where `0` denotes the empty space.
2. **Heuristic Function:** The **Manhattan Distance heuristic** calculates how far each tile is from its correct position in the goal state.
3. **Search Strategy:** The **A* algorithm** prioritizes states with the lowest total estimated cost (path cost + heuristic value).
4. **Priority Queue:** The algorithm maintains a **priority queue (min-heap)**, always expanding the most promising state first.

## How to Use the Solver
1. Run the program.
2. Enter the **start state** as a 3x3 grid (use `0` for the empty space).
3. Enter the **goal state** as a 3x3 grid.
4. The program will output the sequence of moves required to reach the goal state.

## Example Usage
### **Input:**
```bash
Enter the start state:
1 2 3
4 0 5
6 7 8

Enter the goal state:
1 2 3
4 5 6
7 8 0
```

### **Output:**
```bash
Solution found in 3 moves: ['Right', 'Down', 'Left']
```

## Requirements
- Python 3.x
- NumPy

## References
- Russell, S., & Norvig, P. (2010). *Artificial Intelligence: A Modern Approach*.
- GeeksforGeeks: A* Algorithm for 8-Puzzle Problem.
- NumPy Documentation: [NumPy](https://numpy.org/)

