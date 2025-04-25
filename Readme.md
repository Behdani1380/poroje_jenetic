seyeseh zeynab behdani :

This project solves the classic 8 Queens Problem using a Genetic Algorithm. 
The goal is to place 8 queens on an 8×8 chessboard such that no two queens threaten each other. 
This means no two queens should share the same row, column, or diagonal.



1.Creating the Initial Population
We start by generating a population of random solutions.
Each solution (or "individual") is a list of numbers representing the row positions of queens in each column.


2.Fitness Function
The fitness function calculates the number of conflicts (attacks) between the queens.
The fewer the conflicts, the better the solution. 
If the fitness is 0, there are no conflicts, and we have found a valid solution.