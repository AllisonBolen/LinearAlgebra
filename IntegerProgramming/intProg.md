# integer programing
An integer programming problem is a mathematical optimization or feasibility program in which some or all of the variables are restricted to be integers.
## Steps
0. Rescale so everything is an int
1. Solve the linear relaxation
2. if the lp relaxation yields integer results we are done
3. Otherwise we have two possible approaches
   - branch and bound or cutting plane

## Branch and Bound

### Steps
- Given the results of the relaxation if they are all integer values we are done if not
then we need to branch on a non integer variable.
- Then solve the LP relaxation of the current problem.
- If the solution is an integer stop on this branch.
- The value of the objective gives us a bound. If infeasible, we cant go further.
- if non integer:
  - if the result of this branch is less than a bound we found on a previous branch then we know that going further own this branch wont give us any better answers.
  - if it is better however then we continue to branch on a non int var and repeat.

- This is not the best always, you could branch forever and the growth is exponential because it functions like a tree. this is a brute force algorithm.

### References for branch and bound
[Geek knapsack](https://www.geeksforgeeks.org/0-1-knapsack-using-branch-and-bound/) (AWESOME TUTORIAL)
[Cheesy as hell tutorial but I love it](https://ocw.mit.edu/courses/sloan-school-of-management/15-053-optimization-methods-in-management-science-spring-2013/tutorials/MIT15_053S13_tut10.pdf)

## Cutting plane
At each step, if the current LP relaxation has any non integer values, introduce a new constraint so that the current (non-integer) point violates the constraint and no valid integer solutions violate the constraint. It is basically cutting out all the invalid options during runtime. (I know this isn't a real way to describe math but this algorithm feels more reactive than preventative.)
Elementary row ops do not change the solution set. At any stage of solving the LP relaxation, the feasible points have not changed, which means the points that satisfy the constraints as originally written are exactly the points that satisfy the constraints as currently written.


### Refrences for cutting plane:
[Power point download link (Awesome walk through)](http://cgm.cs.mcgill.ca/~avis/courses/567/notes/cutplane_ex.ppt)

# [home](https://github.com/AllisonBolen/LinearAlgebra/tree/bolen)
