# Introduction
In this project I've developed a solver for the minesweeper game.

# Implementation
The high level algorithm works in this way:
- At each iteration a cell is opened
- Thanks to the information retrieved (the number inside the cell), update the internal knowldge "S"
- Select the next cell X at position i,j and decide if: S -> X_i,j is a mine or S-> X_i,j is a safe cell
- Reapeat

In some cases,  we can't infer a safe cell or a cell that contains a mine (too few information). In these cases, it select the cell with the lowest probability to contains the mine, in other word the cell with the lowest number of interpretation that satisfies the formula S -> X_i,j is a mine.
