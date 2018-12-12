# Karush Kuhn Tucker


For constrained optimization, critical points are found using KKT conditions. For the NLP
Maximize: \(f(x)\)
Subject to: \(g(x)\le 0\)

KKT conditions are:
1) \(\nabla f(xc) = \lambda \nabla g(xc)\) (stationarity),
2) \(\lambda \ge 0\) (dual feasibility),
3) \(g(xc)\le 0\) (feasibility), and
4) \(\lambda g(xc)=0\) (complementary slackness)

The interpretation is (roughly), either xc is interior and the gradient of f is the zero vector, or xc is at the boundary and any direction of increase would violate the constraint. (Info from prof)

If the result violate a KKT condition then the result is not optimal.

## References
[A](https://www.youtube.com/watch?v=JTTiELgMyuM)
[B](http://www2.imm.dtu.dk/courses/02711/lecture3.pdf)
[C](https://www.youtube.com/watch?v=AQWy73cHoIU)
[D](https://www.youtube.com/watch?v=AQWy73cHoIU)

to be honest I don't really understand KKT
# [home](https://github.com/AllisonBolen/LinearAlgebra/tree/bolen)
