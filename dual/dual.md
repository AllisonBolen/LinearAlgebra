# Dual Simplex

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
- You are at optimum when there are no more negatives in the right hand side of the LP.
