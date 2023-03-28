### optimization
#### Affine
1. The equivalency of two definitions of affine
2. The subspace associated with an affine set is a subspace
3. The solution set to a linear equation system is an affine set. The associated subspace is its null space.
4. Any affine set can be expressed as the solution set to a linear equation system.
   1. construct the associated subspace, which is also a subspace of R^n, find the orthogonal complement space in R^n, find the basis vector and construct A, Ax = 0, A(x+x_0) = Ax_0
   2. I checked this with the [solution](https://math.stackexchange.com/questions/2812843/every-affine-set-can-be-expressed-as-the-solution-set-of-a-system-of-linear-equa) online 

#### cone 
analogy: collection of rays that starts at the origin 

#### special case of convex set
1. Euclidean ball is a convex set.
2. Simplex is a type of polydedron
   1. proof: p33
### positive semidefinite
1. How to judge the positive semidefiniteness?
   1. eigenvalue
   2. leading principal minors are all nonnegative

### Operations that preserve convexity
1. Affine function: $R^n$ -> $R^m$, y = Ax+b (this is a specical case, [definition](https://mathworld.wolfram.com/AffineFunction.html))
   1. Think about the svd of A, it is rotation + stretch + translation
2. The sum of two convex sets is convex
   1. p38/v7 27min: use the direct or Cartesian product + affine function
3. The solution set to the linear matrix inequality (LMI) is convex
   1. p38: why R^n -> S^m is an affine function? 
4. Eucliean ball to the ellipsoid is an affine mapping
   1. p39 $\|P^{=1/2}(x-x_c)\|\leq 1$
5. perspective function
   1. dimention reduction, not by projection, but by connecting through a hole
   2. prove that under the perspective function, line segment is transformed to another line segment. (just prove the one-to-one mapping)
6. Linear-fractional functions (import non-linear function): affine + perspective
   1. eg: joint probability -> conditional probablity

### convex function
1. spectral norm/induced 2-norm ？
2. easy to make mistakes: indicator function needs to be extended to infinity, the other "凹" shape function does not work v10 9min
3. prove the first-order convexity condition p70
   1. one dimension case: trick 1: take the limit on both sides of inequality, trick 2: weighted average of two inequality,
   2. general: use the 2nd+3rd definition of convex function, 
4. second order condition
5. in all the definitions of convex function, the domain should be a convex set
   1. eg: 1/(x^2)
6. Prove the vector norm is a convex function
   1. definition 1 and the defintion of vector norm
7. zero norm is not convex 
   1. special case: one dimension
   2. related: using zero norm for optimization is hard
8. difference between the max function and the infinity norm
   1. absolute value
9. max function related
   1.  min max optimizaton, game theory, GAN, SVM
   2.  log-sum-exp

### from colleagues
Sara: lower bound of sum of products of comminatory and exp
tried: stirling's approximaton
sigma -> 0 ?