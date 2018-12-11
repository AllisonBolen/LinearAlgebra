# Dual Simplex
## References:
[One](https://www.linearprogramming.info/how-to-solve-a-linear-programming-model-with-dual-simplex-method/)
[Primal v Dual](https://www.linearprogramming.info/primal-dual-relationships-in-linear-programming-duality-theory-in-lp/)
## Primal vs Dual
- Primal: Original LP
- Dual: the values in the objective row of the primal LP are values of variables in the dual
- When you solve any linear program you are also solving its dual.
- Minimizing b^Ty is equivalent to maximizing -b^Ty where b and y are vectors.
- Primal > dual > dual > original primal. The dual of the dual is the original.
### Weak Duality:
Given an LP in standard (max, st <=) form and its dual in minimize form (>=), If vector x is feasible for the primal (max) LP and vector y_x is feasible for the dual (min) LP, then y_x^Tb>=c^Tx_* where y, b, and c are vectors.
- If the dual is feasible the primal is bounded, and if the primal is feasible then the primal is not infeasible.
- Consequences:
  - if the dual has any feasible points, then the primal cannot be unbounded, so primal must either be in-feasible or obtain an optimal value.
  - If Primal is feasible then dual cannot be bounded <-> if D is unbounded the primal is infeasible.
  - If D is feasible then primal cannot be unbounded, if Primal is unbounded then Dual is infeasible.
  - If Primal and dual are both feasible then both obtain and optimum.
  - Proof:  see notebook [WeakDualProof.nb]()
## Strong Duality:
if x is infeasible for Primal and y is infeasible for Dual then there exist optimal (basic) x^* and y^* and y^\*Tb = c^Tx^*
If you've got feasibility then both must be optimum.
## Context:
- Dual simplex is used when the tableau represents a point that is dual feasible (objective row >= 0) and not primal feasible (RHS <0)
- The objective row of an LP is non negative exactly when the tableau corresponds to a feasible point for the dual LP.
- The basic point is dual feasible when the objective row is positive.
- Optimality <-> no negatives in the objective row <-> dual feasibility.
- The dual simplex alg. can be used when you have a basic feasible point that is dual feasible but (possibly) not feasible.
Steps:
- Convert primal into Dual
- Pick a leaving variable based on the most negative basic variable in the RHS.
- Pick an entering column based on the dual ratio test, the entering variable will be the smallest negative \frac{objective Row at i}{pivot row at i}
- Pivot on the row col element
- if you no longer have negatives in the RHS stop, if you do, repeat the above steps.
- You are at optimum when there are no more negatives in the right hand side of the LP.

### Example:
[warehouse.nb](https://github.com/AllisonBolen/LinearAlgebra/blob/bolen/dual/warehouse.nb)


# [home](https://github.com/AllisonBolen/LinearAlgebra/tree/bolen)
