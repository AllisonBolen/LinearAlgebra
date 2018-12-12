# Connections and Exploration

## Data Analytics
- Its interesting that I saw the simplex method being used in another of my courses. We didn't have to do it by hand we used excel but we did go over and analyze the results. It was interesting because this course helped me understand how excel came to its conclusions when given a problem and constraints.
- Seeing how excel formatted out put and split the sensitivity and analysis reports was interesting too. When we did these step by hand we could see both the result and the sensitivity and shadow variables all in just the tableau, but excel splits the reports. I think thats interesting because I always felt those two aspects of the tableau were closely tied, so splitting them up was counter intuitive.

# alternate algorithms:
## Ellipsoid
We learned about the simplex algorithm in class. It has its bugs like cycling, degeneracy, and it can loop through all points before finding the optimum. So I looked into another algorithm, the ellipsoid algorithm.

The Ellipsoid method is polynomial time for linear programming. It is a slow procedure unlike the simplex algorithm, but theoretically it can help when getting an optimal point for a linear program that has a large number of rows to analyze. The ellipsoid method depends instead on the size of data and dimension of the problem. Discovered in 1977 by a Russian  mathematician for general convex optimization problems, then used to prove polynomial time for solving linear programs by another mathematician in 1979. (Computers have gotten faster since the 70s, and even though the procedure can be slow it doesn't really matter because a computer can do it for us.)

Basically the ellipsoid method uses the volume of an ellipse that decrease in size with each of the iterations through the method, thus this creates a minimization of feasible points within the ellipse region.  (This link goes into more detail and has pseudo-code for the algorithm. [linking for my own curiosity](https://www.cs.princeton.edu/courses/archive/fall05/cos521/ellipsoid.pdf] (linking for my own curiosity)


# Interesting use cases for Optimizations:
Machine learning
Data science



# [home](https://github.com/AllisonBolen/LinearAlgebra/tree/bolen)
