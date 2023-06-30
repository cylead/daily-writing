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
   1. dimension reduction, not by projection, but by connecting through a hole
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
       1. prove it is convex: second order, use the definition of positive semi-definite
10. log matrix determinant function is concave
    1.  degenerated case
    2.  use the second definition of convex/concave, the key to simplify the determinant is to write matrix as the product of other matrix (matrix decomposition) end of v13
11. operations that preserve convexity
    1.  nonnegative weighted sums -> generalized to integral
    2.  composition with an affine mapping
    3.  point wise maximum and supremum
12. prove that sum of r largest components of a vector is a convex function 
   1. affine + maximum 
13. prove that spectral norm/induced 2-norm is convex
    1.  supremum, end of v14
14. The 4 cases of composition function
    1. do not have to remember them
    2. scalar case, 2nd differentiable 
    3. other: extension is necessary!
 15. KL divergence convexity
     1.  special case of the perspective of function
     2.  special case of the Bregman divergence (not necessarily convex)
 16. conjugate function
     1.  how to geometrically interpret it? p91
     2.  the conjugate function is convex, interpretation: the sup of a set of lines. useful for later optimization 
     3.  the conjugate conjugate is not the function itself, only when the function is convex and closed (p94)
 17. Quasi convex (unimodal function): all the alpha-sublevel set is convex 
     1.  also, quasiconcave, quasilinear,
     2.  the unimodal function optimization problem can be solved using convex optimization method (eg, GD), but multimodal function opt is hard.
     3.  eg: Quasi convex but concave:  -e^x
     4.  inequality definition, geometric interpretation
18. the linear-fraction function is a quasiconvex function 
     1.  a convex set will be mapped to a convex set by the linear-fraction function, but the function is not necessarily convex
19. prove that the vector geometric mean is concave on a specical domain (v19 quiz)
    1.  2nd condition on 3.1.5 not correct!
20. the zero norm is quasiconvex in the 1 dimensional case, not quasiconvex in the 2 dimensional case, but possible to use other functions to approximate
21. four definition of quasiconvex function
22. leading submatrix of a positive semidefinite matrix is still positive semidefinite?
    1.  use the definition, or the determinant property.
23. link between convex sets and convex function   
    1.  epigraph (special case of alpha-sublevel set)
    2.  quasiconvex


### LLM
### what I am interested in
1. why are llm so good
   1. me: the capacity of the "sequences of tokens" is so large, everything that can be described by language could be included
2. how to train them
3. how to evaluate them
### not interested so far 
1. risks
### LM
#### definition
1. probability distribution over sequences of tokens
   1. A token can be a word, punctuation mark, or number, etc.
#### properties of LLM
1. Emergence
2. main capability: conditional generation, but this is a general capability
3. In-context learning:  a large language model learns to accomplish a task after seeing only a few examples — despite the fact that it **wasn't trained for that task**
#### How to perfrom adaptation on LLMs?



### from colleagues
Sara: lower bound of sum of products of comminatory and exp
tried: stirling's approximaton
sigma -> 0 ?