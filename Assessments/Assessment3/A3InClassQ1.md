Assessment Three:

#Question One:
The purpose of the Two Phase algorithm:
- When dual and simplex don't work you use the two phase algorithm to find the optimal. When origin is infeasible and there is no dual feasibility. When the RHS of the tableau has negative values and the objective row has negative values, you use the two phase algorithm.
- The implementation of two phase is:
1. Reach a feasible solution.
  * Intorduce one artificail variable for every negative RHS, opposite, sign of the excess var.
2. Continue with the ordinary simplex algorithm from the basic feasible solution you just obtained.
Results of phase one:
* If we finish phase one and get optimal but optimal is negative then the LP is infeasible.
* If we are at optimum and the RHS is negative, the original LP is infeasible.
* If we are at optimum and the RHS is 0, we are at a basic feasible point.
  * if there are not artificial variables that are basic then drop the art. vars. and auxiliary function.
  * if there are artificial vars that are still basic we have to keep those vars.
then go do the simplex until you are at optimum.

#Question 2:
An LP has objective function  maximize : 3x1 + 2 x2 - x3 , slack
variables s1, s2, s3, and s4, four main constraints, and all variables
non-negative.

A. There will always be 4 basic and 3 non basic variables at an feasible solution for this LP
B. The current point is (x1,x2,x3,s1,s2,s3,s4)=(0,0,6,0,8,3,5). Is this a basic point or not, and how can you tell?
This point is basic because it is all non negative values.
C. The objective function coefficient vector is [3,2,-1,0,0,0,0]. Its dot product with a direction vector gives the amount that moving in that direction would change the objective function value, so positive dot product means objective would increase, negative dot product means objective would decrease.

For ii, unbounded LP would mean a direction of improvement for the objective that never causes any variables (decision or slack) to become negative.
- I: See [A3InclassQ2CII.nb](https://github.com/AllisonBolen/LinearAlgebra/blob/bolen/Assesments/Assesment3/A3InClassQ2CII.nb) for the answers for this.

- II: You could tell that this lp is unbounded because the direction of improvement would never have any variables become negative. We can see that with direction 2 we have a valid direction of improvement however there are not any negative variables so this means that the LP is unbounded.

#Question 3
A. Set up of word problem:
Min: 4u +10g +25p
st: 1/5u + 3/10g + p >= 1000
    1/5 + 1/10g +1/20p <= 164
    g <= 500
    u,g,p >= 0
reconfigure to standard inequ. form :
min: 4u +10g +25p
st: -1/5u - 3/10g - p <= -1000
    1/5 + 1/10g +1/20p <= 164
    g <= 500
    u,g,p >= 0
Convert from min to max b/c its easier to do maximizations:
max: -4u -10g -25p  (Flip the objective function)
st -1/5u - 3/10g - p <= -1000
    1/5 + 1/10g +1/20p <= 164
    g <= 500
    u,g,p >= 0
Approach: I think this will be a two phase problem because we have an infeasible basis to start with.
You know I really don't know how to do two phase though. Good page to [checkout](https://www.slideshare.net/mplad/two-phase-method-linear-programming). My attempt at this problem is shown in [A3InClassQ3.nb](https://github.com/AllisonBolen/LinearAlgebra/blob/bolen/Assesments/Assesment3/)

#Question 4:
Max z = 2x1 + 3x2
st: 4x1 + 3x2 ≤ 15
    x1 + x2 ≤ 4
    x1 x2 ≥ 0
A. infeasible, v[3,3] breaks constraint 1.
B. infeasible, v[-1,2] breaks constraint 3.
C. feasible interior.
D.feasible boundary.

#Question 5:
A. If John and Jane have the opportunity to rent more land for planting at $2000 per acre for
the growing season, should they? Explain.
* No, the cost of more land outweighs the profit. Since the cost of 2000$ is more than the shadow price which is 0, buying more land would not affect the optimum. We technically also have 5 acres of land left over at optimum, so there is no need to buy more, land is not our limiter right now.
B. John and Jane find a fertilizer distributor who can sell them fertilizer at $55 per ton. Should
they purchase more?
* Yes, 55 < 125/2.
C. How much additional profit (if any) could John and Jane expect if they had an additional
10 workers?
* If they hired an additional 10 workers their total workers would be 110 and their profit would go up by 25*10 because the shadow price of a worker is 25 per worker they would gain an additional 250 in profit.
D. For parts 5a and 5b, what is the maximum John and Jane could rent/purchase and still
have the same optimal basis?
Using the final tableau that they computed you cant determine how
much fertilizer to buy while maintaining the basis.
If we take the current final RHS and the current column for
fertilizer we can calculate the limits[20, 20, 5] + deltaF.
[-1/4, 3/8, -1/8] >= [0,0,0] thus:
20 - df * 1/4 >= 0
20 + df * 3/8 >= 0
5 - df * 1/8  >= 0
Then:
df >= 80
df >= -53.3
df >= 40
* They can rent up to 40 more tons of fertilizer with out changing the basis.
You would do the same process for the land column and RHS. Resulting in
dl * 0 >= -20
dl * 0 >= -20
dl >= -5
Where dl is the change in land. Though I am not entirely sure how to interpret this result. You cant buy anymore land without changing the basis.
E. Look again at part 5c. If John and Jane have 10 extra workers, how much of their land
should they plant with corn versus wheat?
You can find the new final RHS by taking the current RHS and the column for labor and replacing deltaLabor with 10:
20 +  deltaLabor * 1/2
20 +  deltaLabor * -1/4
5 +  deltaLabor * -1/4
Then:
20 +  10 * 1/2
20 +  10 * -1/4
5 +  10 * -1/4
=
20 +  10 * 1/2
20 +  10 * -1/4
5 +  10 * -1/4
=
25
17.5
2.5
Where they would want to plant 25 acres of wheat and 17.5 acres of corn and have 2.5 acres of land left over, with a new optimum at 10250$.
#Question 6
A. Neither , you have interior points and border points
B. Interior, all points are in the interior of the feasible region
C. Neither , you have interior points and border points
D. Simplex all points are on the border
E. Neither, infeasible
