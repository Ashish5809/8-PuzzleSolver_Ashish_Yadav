# 8-PuzzleSolver_Ashish_Yadav
Overview
This project implements an 8-Puzzle Solver using the A search algorithm* with the Manhattan distance heuristic. The 8-puzzle is a sliding puzzle consisting of 8 numbered tiles and one empty space. The goal is to move the tiles using the empty space until the puzzle is in a solved configuration.

Features
User inputs the initial state of the puzzle.
The program solves the puzzle using A* search with the Manhattan distance heuristic.
Outputs the sequence of moves from the initial configuration to the goal state.
Validates user input to ensure correct formatting.
Requirements
Python 3.x
Installation
To use the 8-Puzzle Solver, follow the steps below:

Clone the repository:

bash
Copy
git clone https://github.com/yourusername/8-puzzle-solver.git
Navigate to the project directory:

bash
Copy
cd 8-puzzle-solver
Run the script:

You can directly run the Python script that solves the 8-puzzle.

bash
Copy
python8_puzzle_solver.py
The program will prompt you to input the initial configuration of the 8-puzzle.

Usage
When prompted, enter the initial configuration of the puzzle row by row, separating each tile by a space. Use 0 to represent the empty space.

Example input:

sql
Copy
Enter row 1 (space-separated values): 1 2 3
Enter row 2 (space-separated values): 5 6 0
Enter row 3 (space-separated values): 4 7 8
The program will output the sequence of moves to solve the puzzle.

Example output:

yaml
Copy
Start State:
1 2 3
5 6 0
4 7 8

Solution path:
1 2 3
5 6 0
4 7 8

1 2 3
5 0 6
4 7 8

1 2 3
0 5 6
4 7 8
Algorithm
The puzzle is solved using the A* search algorithm, a pathfinding algorithm that finds the shortest solution by using both the g-cost (steps taken) and the h-cost (Manhattan distance heuristic). The Manhattan distance heuristic computes the sum of the absolute distances between the current positions and the goal positions of each tile.

Steps:
Input validation: The program checks if the user's input is valid, ensuring that there are exactly 9 numbers (0 to 8) representing the tiles.

A* Search: The algorithm explores the puzzle states by sliding tiles and computes the f(n) cost function, which includes the actual cost (g(n)) and the heuristic (h(n)).

Output: The program outputs the sequence of moves required to solve the puzzle.

Example
Input:
sql
Copy
Enter row 1 (space-separated values): 1 2 3
Enter row 2 (space-separated values): 5 6 0
Enter row 3 (space-separated values): 4 7 8
Output:
python-repl
Copy
Start State:
1 2 3
5 6 0
4 7 8

Solution path:
1 2 3
5 6 0
4 7 8

1 2 3
5 0 6
4 7 8

1 2 3
0 5 6
4 7 8

... (more steps)
Troubleshooting
Invalid Input: If the input contains any numbers outside the range of 0 to 8 or if there are fewer or more than 9 numbers, the program will prompt you to re-enter the row correctly.

No Solution: If the puzzle is unsolvable (which happens in certain configurations), the program will output "No solution found."

License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgments
A* Search Algorithm: The core of this solution is based on the A* search algorithm.
Manhattan Distance Heuristic: The heuristic used for guiding the search.
