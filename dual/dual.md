# Dual Simplex
## References:
[One](https://www.linearprogramming.info/how-to-solve-a-linear-programming-model-with-dual-simplex-method/)
[Primal v Dual](https://www.linearprogramming.info/primal-dual-relationships-in-linear-programming-duality-theory-in-lp/)
## Contex:
- Dual simplex is used when the tableau represents a point that is dual feasible (objective row >= 0) and not primal feasible (RHS <0)
- The objective row of an LP is non negative exactly when the tableau corresponds to a feasible point for the dual LP.
- Primal: Original LP
- Dual: the values in the objective row of the primal LP are values of variables in the dual
- The basic point is dual feasible when the objective row is positive
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
