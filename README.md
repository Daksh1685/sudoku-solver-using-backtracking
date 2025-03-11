# Sudoku Solver

## Overview
This project is a C++ implementation of a Sudoku solver using a backtracking algorithm. It takes a 9x9 Sudoku board as input, attempts to solve it, and then prints both the unsolved and solved versions of the board.

## Features
- Displays the Sudoku board in a structured format.
- Checks for valid number placements in rows, columns, and 3x3 subgrids.
- Utilizes a recursive backtracking algorithm to solve the Sudoku puzzle efficiently.
- Handles cases where the Sudoku board is unsolvable.

## How It Works
1. The program initializes a predefined Sudoku board with some given numbers and zeros representing empty spaces.
2. It prints the unsolved board.
3. The `solveBoard` function recursively fills in numbers from 1 to 9 while ensuring that they meet Sudoku constraints.
4. If a valid number is found, it continues solving the rest of the board; otherwise, it backtracks.
5. Once solved, the final board is displayed.

## Code Explanation
- `printBoard()`: Displays the Sudoku board with grid formatting.
- `isNumberInRow()`: Checks if a number exists in a given row.
- `isNumberInColumn()`: Checks if a number exists in a given column.
- `isNumberInBox()`: Checks if a number exists in a 3x3 subgrid.
- `isValidPlacement()`: Ensures a number can be placed in a specific position.
- `solveBoard()`: Implements the backtracking algorithm to solve the puzzle.
- `main()`: Initializes the Sudoku board, calls the solver, and displays results.

## Running the Program
1. Ensure you have a C++ compiler installed (e.g., g++).
2. Save the code in a file named `sudoku_solver.cpp`.
3. Compile the program using:
   ```sh
   g++ sudoku_solver.cpp -o sudoku_solver
   ```
4. Run the executable:
   ```sh
   ./sudoku_solver
   ```

## Example Output
```
Unsolved Sudoku:
0 0 0 | 0 3 7 | 0 9 2
6 3 0 | 0 0 0 | 0 0 0
0 9 0 | 0 0 2 | 3 0 5
---------------------
8 7 0 | 0 0 0 | 0 0 1
0 2 0 | 9 0 1 | 0 4 0
9 0 0 | 0 0 0 | 0 2 7
---------------------
1 0 9 | 5 0 0 | 0 7 0
0 0 0 | 0 0 0 | 0 8 6
3 6 0 | 4 1 0 | 0 0 0

Solved successfully!

Solved Sudoku:
4 5 1 | 6 3 7 | 8 9 2
6 3 2 | 8 5 9 | 7 1 4
7 9 8 | 1 4 2 | 3 6 5
---------------------
8 7 4 | 2 9 6 | 5 3 1
5 2 3 | 9 7 1 | 6 4 8
9 1 6 | 3 8 5 | 4 2 7
---------------------
1 8 9 | 5 6 4 | 2 7 3
2 4 7 | 7 2 3 | 1 8 6
3 6 5 | 4 1 8 | 9 2 7
```
