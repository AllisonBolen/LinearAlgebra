# Two Phase:
The purpose of the Two Phase algorithm:
- When dual and simplex don't work you use the two phase algorithm to find the optimal. When origin is infeasible and there is no dual feasibility. When the RHS of the tableau has negative values and the objective row has negative values, you use the two phase algorithm.
- The implementation of two phase is:
1. Reach a feasible solution.
  * Introduce one artificial variable for every negative RHS, opposite, sign of the excess var.
2. Continue with the ordinary simplex algorithm from the basic feasible solution you just obtained.
Results of phase one:
* Do the simplex alg on teh auxiliary objective row to optimize the aux. obj. row.
* If we finish phase one and get optimal but optimal is negative then the LP is infeasible.
* If we are at optimum and the RHS is negative, the original LP is infeasible.
* If we are at optimum and the RHS is 0, we are at a basic feasible point.
  * if there are not artificial variables that are basic then drop the art. vars. and auxiliary function.
  * if there are artificial vars that are still basic we have to keep those vars.
then go do the simplex until you are at optimum.

# References
[A](https://www.mathstools.com/section/main/Two-phase_Method_Example#.XBBnv5NKj_Q)
[B](http://optlab.mcmaster.ca/feng/4O03/Two.Phase.Simplex.pdf)

# [home](https://github.com/AllisonBolen/LinearAlgebra/tree/bolen)
