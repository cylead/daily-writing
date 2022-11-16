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

Note the visulization of $A-\lambda I$