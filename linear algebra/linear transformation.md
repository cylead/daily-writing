### Linear transformation and matrix-vector multiplication
$$Ax=b$$
A:(m,n), x:(n,1),b:(m,1)
Column vectors of A:
$$A = [A_1,...,A_n]$$
Broadly speaking, $x$is linearly transformed to $b$ through the matrix $A$.  

$x=[x_1, ..., x_n]$ is a n-dimensional vector with basis [1, 0, ..., 0], [0, 1,..., 0], ..., [0, ..., 0, 1]. These bases are mapped to the new bases in m-dimensional space: $A_1,...,A_n$, and x is mapped to $$Ax = x_1 A_1 + ... + x_nA_n = b$$

This process can be visualized!!!

Then $Ax$ lies in the column space of $A$, we can discuss column rank </= $n$ or $m$.

eg:
$m=n=3$
If $A_i$ are linearly dependent, and the column rank is 1. The endpoint of $x$ will be transformed to a point on a line.

And certain points on a plane (null space) will be transformed to the origin.

#### special matrix
orthogonal matrix: rotation, end point on the unit circle.
diagonal matrix: stretch

#### Typical forms
$M$ is a matrix (linear), but we want to check how it looks like from the perspective transformed by A. Then we get $A^{-1}MA$.

Special case: when $A$ is the eigen matrix of M, $A^{-1}MA$ becomes diagonal because the eigen vectors keeps the directions after the transformation.

This means $M = A\Lambda A^{-1}$, which is the eigen value decomposition.

#### row operations
multiply on the left.
This is useful to under stand the using elimination to solve $Ax=b$.
Example:
Find the inverse of 
$$\left[\begin{matrix}
1 & 0 & 0\\ -3 & 1 & 0\\ 0 & 0 & 1
\end{matrix}\right] 
$$
What the matrix does is subtracting 3 times row1 from row2, so we just add 3 times row1 back the inverse is:
$$\left[\begin{matrix}
1 & 0 & 0\\ 3 & 1 & 0\\ 0 & 0 & 1
\end{matrix}\right] 
$$
#### data science
Dataset: If we consider the column vectors, then we should view each columns as a sample, and do right matrix-vector multiplication.

### Dot product
A:(1, m), x: (m, 1)
$A_i$ are scalars, which means the m-dimensional vector $x
$ is transformed onto the real-line.

Some duality: which real line in the m-dimensional space? 
The vector $A^T$. This leads to the projection interpretation of dot product.

Other things: 
symmetry in dot product: think about the case when two vectors have equal lengths, then extend it with different lengths.

### Eigenvalue
Under a linear transformation $A$, which vectors' directions do not change?  
Note the visualization of $A-\lambda I$.

When A is symmetrical, the eigenmatrix is an orthogonal matrix. Geometric interpertation: (rotation)(strech)(ratation).
(any interpertation about how it is related to the symmetry?).
This is called spectral decomposition.

This leads to the fact that we can do eigenvalue decomposition of $AA^T$ and $A^TA$ when A is not square, and the result is related to the singular value decomposition of $A$: $A=U\Sigma V^T$.
