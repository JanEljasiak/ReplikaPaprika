SUDOKU SOLVER

This is a program which prints solution of any valid sudoku puzzle using backtracking algorithm (https://en.wikipedia.org/wiki/Sudoku_solving_algorithms#Backtracking).
It takes up to 10 seconds to find a solution at the hardest level and it is solved almost instantly at the easiest.


1. REQUIREMENTS

The program uses 2 modules:

import time
from termcolor import colored

"time" is used for measurements of time needed to solve the sudoku puzzles.
"termcolor" is used to change colors in printing different kind of sudoku numbers

Possibly, firstly you will need to install modul "termcolor" on your computer. If you use Windows you can just simply write in Command Promp:

pip install termocolor

2. HOW TO USE
3. 
After running sudoku_solver.py you should see 3 examples of sudoku puzzles on the different levels. You can simply add your board by creating an instance of Sudoku class in the same convention as in examples. Program should show unsolved and solved sudoku and time needed for solving it.

3. RUN WITH THE UNCHANGED DATA

Sudoku - Level easy
- - - - - - - - - - - - - 
| 9 7 1 | 0 0 0 | 0 3 2 | 
| 0 4 6 | 1 0 0 | 0 8 7 | 
| 0 8 0 | 0 0 3 | 6 1 9 | 
- - - - - - - - - - - - - 
| 6 3 0 | 0 5 7 | 1 2 0 | 
| 4 1 5 | 6 3 2 | 0 0 0 | 
| 0 0 9 | 8 4 1 | 3 5 6 | 
- - - - - - - - - - - - - 
| 0 0 7 | 3 0 4 | 2 0 0 | 
| 0 0 0 | 0 0 5 | 0 0 1 | 
| 0 0 0 | 0 0 8 | 0 7 0 | 
- - - - - - - - - - - - - 
Solved sudoku
- - - - - - - - - - - - - 
| 9 7 1 | 5 8 6 | 4 3 2 | 
| 3 4 6 | 1 2 9 | 5 8 7 | 
| 5 8 2 | 4 7 3 | 6 1 9 | 
- - - - - - - - - - - - - 
| 6 3 8 | 9 5 7 | 1 2 4 | 
| 4 1 5 | 6 3 2 | 7 9 8 | 
| 7 2 9 | 8 4 1 | 3 5 6 | 
- - - - - - - - - - - - - 
| 8 9 7 | 3 1 4 | 2 6 5 | 
| 2 6 3 | 7 9 5 | 8 4 1 | 
| 1 5 4 | 2 6 8 | 9 7 3 | 
- - - - - - - - - - - - - 
Sudoku was solved in 0.02498650550842285s

Sudoku - Level normal
- - - - - - - - - - - - - 
| 0 2 0 | 9 0 4 | 0 1 8 | 
| 6 0 1 | 0 0 7 | 0 0 0 | 
| 0 0 0 | 0 0 0 | 0 0 0 | 
- - - - - - - - - - - - - 
| 0 4 0 | 8 0 0 | 0 0 7 | 
| 0 0 0 | 0 0 0 | 0 3 0 | 
| 0 0 0 | 1 7 0 | 0 0 5 | 
- - - - - - - - - - - - - 
| 0 0 0 | 0 0 0 | 8 6 0 | 
| 0 0 0 | 7 0 0 | 0 0 1 | 
| 0 0 4 | 2 5 1 | 0 0 0 | 
- - - - - - - - - - - - - 
Solved sudoku
- - - - - - - - - - - - - 
| 3 2 5 | 9 6 4 | 7 1 8 | 
| 6 8 1 | 5 2 7 | 3 9 4 | 
| 4 7 9 | 3 1 8 | 2 5 6 | 
- - - - - - - - - - - - - 
| 1 4 3 | 8 9 5 | 6 2 7 | 
| 7 5 8 | 6 4 2 | 1 3 9 | 
| 2 9 6 | 1 7 3 | 4 8 5 | 
- - - - - - - - - - - - - 
| 5 1 7 | 4 3 9 | 8 6 2 | 
| 9 3 2 | 7 8 6 | 5 4 1 | 
| 8 6 4 | 2 5 1 | 9 7 3 | 
- - - - - - - - - - - - - 
Sudoku was solved in 0.39177417755126953s

Sudoku - Level hard
- - - - - - - - - - - - - 
| 0 0 0 | 0 3 0 | 9 0 0 | 
| 4 0 5 | 0 0 0 | 0 0 0 | 
| 1 0 0 | 0 0 0 | 0 0 0 | 
- - - - - - - - - - - - - 
| 0 3 0 | 0 8 0 | 0 0 5 | 
| 0 0 2 | 0 0 0 | 0 1 0 | 
| 0 0 0 | 0 0 0 | 0 4 6 | 
- - - - - - - - - - - - - 
| 0 7 0 | 0 0 0 | 2 0 0 | 
| 6 0 0 | 5 0 0 | 0 0 0 | 
| 0 0 0 | 1 0 0 | 0 0 0 | 
- - - - - - - - - - - - - 
Solved sudoku
- - - - - - - - - - - - - 
| 7 2 6 | 4 3 5 | 9 8 1 | 
| 4 9 5 | 8 1 7 | 6 3 2 | 
| 1 8 3 | 2 6 9 | 5 7 4 | 
- - - - - - - - - - - - - 
| 9 3 4 | 6 8 1 | 7 2 5 | 
| 8 6 2 | 7 5 4 | 3 1 9 | 
| 5 1 7 | 3 9 2 | 8 4 6 | 
- - - - - - - - - - - - - 
| 3 7 1 | 9 4 6 | 2 5 8 | 
| 6 4 8 | 5 2 3 | 1 9 7 | 
| 2 5 9 | 1 7 8 | 4 6 3 | 
- - - - - - - - - - - - - 
Sudoku was solved in 10.054255723953247s
