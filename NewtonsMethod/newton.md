# Newtons method
References:
- [video](https://www.youtube.com/watch?v=28BMpgxn_Ec)
- [Slides](http://www.ece.mcmaster.ca/~xwu/part4.pdf)
- [Book Link](https://www.cs.ccu.edu.tw/~wtchu/courses/2014s_OPT/Lectures/Chapter%209%20Newton%27s%20Method.pdf)
##Information:
- Newton's method for optimization is a second order method: the first order, the gradian and the second derivative aka the hessian are all used.
- Zero Finding: In the first order you are just searching for a point where the function is 0.  
- Minimizing or maximizing optimization: We want to find where the derivative of the function is 0.
- Con: it can be hard to tell if you are going toward a max or a min since newtons method functions the same for both.
- Pro: Newtons method is generally faster.  
  - Set count limit (maybe N=100 or so)
  - Set tolerance (for example, tol= $MachineEpsilon*10)
  - Initialize current point: xc=x_{0}
  - Set count: n=0
  - Do:{
       - Solve (Hessian(xc)).s=(gradient(xc)) for s
       - xc = xc - s
       - n=n+1
- }until (Norm(s)<tol or n>N)

Newton's method is used for unconstrained optimization.
### Walk Through:
  find the maximum value of f(x)=2sin(x)-\frac{x^2}{10} with and initial guess of x_0 = 2.5.
  Solution:
    Take the derivative of the original
    f'(x) = 2cos(x)-\frac{2x}{10} = 2 cos(x)-\frac{x}{5}
    Take the derivative of the derivative, or second derivative of the original.
    f''(x)=-2sinx-\frac{1}{5}
    Preform the following step to get x_i+1:
    x_i+1 = x_i - \frac{-2cos(x)-\frac{x_i}{5}}{-2sinx-i-\frac{1}{5}}
    (You would repeat this step to get a new point on the function for as long as ||x_i-x_i+1|| is not zero to reach optimum)
    x_0=2.5, x_1=0.995, x_2=1.469
    (See slides link)

### better walk through
A better walk through is provided in the Book link on page 4-7.

## Comparable:
#### Steepest Descent
###References:
- [Document](http://fivedots.coe.psu.ac.th/~mitchai/wp-content/uploads/2009/07/steepest.pdf)
- [Wolfram](http://mathworld.wolfram.com/MethodofSteepestDescent.html)
- [Other](http://www.math.usm.edu/lambers/mat419/lecture10.pdf)
- [Awesome Video Tutorial](https://www.youtube.com/watch?v=MbYvM2NFLec)
- [Awesome Video Tutorial Part 2](https://www.youtube.com/watch?v=30TLyHgjfJ4)

- The steepest descent method uses only first derivatives in
selecting a suitable search direction.
- The gradient of a function represents the direction of increase.
- Use this method when Newtons method is unreliable and you can't find the solution using traditional analytics, use steepest decent.
- For steps on how to solve one check the video listed above. By far my favorite tutorial so far.

### Interesting:
I kept reading in comments on videos and articles that people use both newtons method and steepest decent a lot in machine learning programs. Thats cool as hell.

# [home](https://github.com/AllisonBolen/LinearAlgebra/tree/bolen)
