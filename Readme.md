seyedeh zeynab behdani :

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

3.Parent Selection
To generate the next generation, two parents are selected randomly, 
but with a preference for parents with better fitness (lower fitness value).



elaheh afsharnasab:


4.Uses ordered crossover to preserve valid permutations

Selects a random crossover point between columns

Takes the first segment from one parent and fills remaining positions from the other parent

Ensures each queen appears exactly once in each column

Produces two children by swapping parent roles


5.With default 10% probability, swaps two randomly selected queens

Maintains permutation validity (no duplicate queens in columns)

Introduces diversity to escape local optima

Mutation rate is tunable (typically between 1-10%)



6.Initialization: Creates random population of solutions

Generational Loop:

Sorts population by fitness (conflict count)

Returns immediately if perfect solution found (0 conflicts)

Implements elitism by preserving the best solution

Fills new population through selection, crossover and mutation

Termination: Returns None if no solution found after all generations



