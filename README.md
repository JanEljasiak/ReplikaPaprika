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

After running sudoku_solver.py you should see 3 examples of sudoku puzzles on the different levels. You can simply add your board by creating an instance of Sudoku class in the same convention as in examples. Program should show unsolved and solved sudoku and time needed for solving it.

