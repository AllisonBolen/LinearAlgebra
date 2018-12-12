#Affine Scaling

## Info:
Affine scaling is an algorithm for solving linear programming problems. Specifically, it is an interior point method.
Affine scaling has two parts, the first part finds a feasible point to start optimizing with. The second part does the actual optimization while staying strictly inside the feasible region.
Affine scaling is an interior point alg. because it works for all values that are strictly greater than 0.
Interior point algs. approximate optimum and tell you how close you are to optimum. These are good at testing how close you are to optimum, so if you are working with another algorithm and its taking a very long time to calculate you can test a point whit an interior point alg. to see how far you need to travel yet, maybe you're close and should continue, maybe you aren't and should find another algorithm to work with. 

## Steps:
- find an interior point (guess)
- scale the problem to fit "center"
- choose the direction of greatest improvement
- project that direction on allowable directions
- Move toward the direction of greatest increase.
As you can see in the file. We have to set up a basic feasible interior point to start with then you scale that point so it is one unit away from every boundary.  Then you find the gradient and move in that direction , but technically if you move all the way in that direction you will violate the constraints so we project on to the null space of the matrix. then we can see how far we can move with out hitting the boundary. Then you will set the new point as the new starting point and continue the process until you are about machine epsilon away from the boundary. Then you are at optima.
## References:
[Question](https://scicomp.stackexchange.com/questions/772/what-are-the-advantages-disadvantages-of-interior-point-methods-over-simplex-met)
[Software for Interior points](https://projects.coin-or.org/Ipopt)
[Slides](https://slideplayer.com/slide/9781024/)
[wiki](https://en.wikipedia.org/wiki/Affine_scaling)
## example:
Assessment 4 question 1. ()[]
In class example ()[]
# [home](https://github.com/AllisonBolen/LinearAlgebra/tree/bolen)
