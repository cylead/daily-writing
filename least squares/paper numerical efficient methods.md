### Why is condition number used to measure the sensitivity?

$$\kappa(A) = ||A|| \cdot ||A^+||$$
If the norm is the Euclidian norm
$$\kappa(A) = \frac{\sigma_{max}(A)}{\sigma_{min}(A)}$$
where $\sigma$ is the singular values of $A$
Use the sub-multiplicative property, it can be proved that for equation $Ax=b$
If there is perturbations to b,

$$\frac{1}{\kappa(A)} \frac{||b-\hat{b}||}{||b||} \leq \frac{||x-\hat{x}||}{||x||} \leq 
\kappa(A)\frac{||b-\hat{b}||}{||b||}$$

If there is a perturbation on $A$, 
$$\frac{||x-\hat{x}||}{||x||} \leq 
\kappa(A)\frac{||A-\hat{A}||}{||A||}$$


#### What type of norm should be used in the calculation of condition number?

Theorem: In finite dimensions, all norms are equivalent to each other. For all pairs of norms n and m, there exists two constant c and C such that $0 \leq c \leq C$, and for any $x \in S$, we have 
$$c ||x||_n \leq ||x||_m \leq C||x||_n$$

Prove: refer to the paper or https://math.stackexchange.com/questions/57686/understanding-of-the-theorem-that-all-norms-are-equivalent-in-finite-dimensional

Triangular inequality + Bolzano–Weierstrass theorem

In the link, it is shown that in infinite dimension spaces, one can have inequivalent norms.

other resources: http://mathonline.wikidot.com/equivalence-of-norms-in-a-finite-dimensional-linear-space
https://math.mit.edu/~stevenj/18.335/norm-equivalence.pdf

This theorem shows that norms are always within a constant factor of one another. 
$\kappa$

### Why different numerical methods' numerical stability are different?
Normal equations: not recommanded although the fasteast,
ATA, Cholesky
$\kappa (A^TA) = (\kappa(A))^2$, use the SVD to understand this

Orthogonal methods: QR factorization
QR (Householder numerically stable then Gram-Schmidt), solve the square system (triangular)
Problem: in the QR factorization step, if $A$ is close to rank-deficient, the Q may not be orthogonal

SVD
Orthogonal transformation -> diagonal system
In the case when $A$ is rank-defficient, we can still compute the Least Squares Solution by selecting the solution that has the smallest norm among the solutions
### What are the methods applied in the machine learning libaries?

scipy (in the last para, non-linear least square problems): https://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.least_squares.html

https://docs.scipy.org/doc/scipy/reference/generated/scipy.linalg.lstsq.html#scipy.linalg.lstsq
use the Cut-off ratio for small singular values
, options for LAPACK dirvers, refer to the LINPAC link below

not proper to use matrix inverse: https://stackoverflow.com/questions/34170618/normal-equation-and-numpy-least-squares-solve-methods-difference-in-regress

numpy.linalg.lstsq
https://numpy.org/doc/stable/reference/generated/numpy.linalg.lstsq.html#numpy.linalg.lstsq
use the Cut-off ratio for small singular values

LAPACK:
https://netlib.org/lapack/lug/node27.html
and document in this directory



