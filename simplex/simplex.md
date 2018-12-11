# simplex
- Used when you want to find the optimum of a standard form LP.
-
## steps
- Start at a basic feasible point
  - Choose an entering variable: Using blands rule, pick the leftmost negative objective row values column.
  - Choose a leaving variable: preform the ratio test for the above column and select the lowest scoring row.
  - update tableau
  - repeat
- You hit optimum when the objective row of the tableau is all non negative
## Useful Info
- The feasible region tells you whats aloud, the objective function tells you whats good.
- Alternate optima will be convex combinations of basic feasible solutions.
  - triangle, corners, between corners.

## Outcomes:
- If you have all negative entries for a nonbasic variable and in the objective row then you have an unbounded LP.
- If you cant choose a leaving variable you have an unbounded LP and should find the simplex dir.
- If you cant choose and entering var then you are at optimum and you are finished with the simplex method.
- if you cant choose a leaving var you have an unbounded LP and you are done
- You can have a degenerate optimum as well, where your algorithm is infinitely looping between basic feasible points with the same optimal value. This can be avoided if bland's rule is used.
- This can be slightly in efficient though, you could potentially visit all BF points before getting to the optima.
You can reach optima, alternate optima, unbounded LP, or not start at a BFS
## Example
You can see an example of the simplex method in the [Pumpkin Spice Problem](https://github.com/AllisonBolen/LinearAlgebra/blob/bolen/simplex/pumpkinspice.nb). This shows facility with simplex as well as sensitivity analysis and shadow pricing.

# [home](https://github.com/AllisonBolen/LinearAlgebra/tree/bolen)
