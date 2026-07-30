# PCA (Principal Component Analysis)


### Issues with PCA

1. Time complexity issue
2. Non-linear data

**Time complexity issue:**

$C = \frac{1}{n} XX^T$

- $O(d^3)$
- If $d>>n$ , algorithm become computationally lengthy.

### How to fix??

**fact 1:**

The PCs can be written as linear combination of data points.

$Cw_k = λ_kw_k$
 $\implies w_k = \sum ^n _{i=1} (\cfrac{x^T_iw_k}{n \lambda_K})x_i$

$w_k = Xα_k$

- If we can find $α_k$ , we are done.
- elements in $α_k$ also contains the $w_k$ .

Doing some algebra, we get

$Kα_k = nλ_kα_k$

where $K = X^T X$

So,the $α_ks$, calculated using solving the above eigenequation, are same as we are looking for????
Are these eigenvectors the same as eigenvectots of the covariance matrix??

These $α_k$ must satisfy the following

 $α_k^TKα_k = 1$

**Fact 2**

The nonzero eigenvalues of $XX^T$ and $X^TX$ are same.
Using this fact and a bit more algebra, we can say that these $α_k$ are

$α_k = \cfrac{β_k}{\sqrt{nλ_k}}$ 

Where $β_k$ is the unit eigenvector corresponding to $k^{th}$ largest eigenvalue $n \lambda_k$ .

**Algorithm:**

- Step 1: Compute $K = X^T X$
- Step 2: Compute eigen-decomposition of $K$
    - Let $\{β_1, β_2, ..., β_l\}$ are the unit eigenvectors corresponding to eigenvalues $\{nλ_1, nλ_2, ..., nλ_l\}$
- Step 3: set $α_k = \cfrac{\beta_k}{\sqrt{nλ_k}} = \cfrac{\text{unit eigenvector}}{\sqrt{\text{eigenvalue of K}}}$
- Step 4: $w_k = Xα_k$

### Non-linear data:

Data may not live in low dimensional linear subspace.

Consider the following relationship between the features:

$f^2_1 − 2af_1 + a^2 + f^2_2 −  2bf_2 + b^2 − 1 = 0$

Can we transform the dataset into higher dimension space such that the data live in linear subspace of that higher dimension space???

For the above data, consider the following transformation:
$[f_1, f_2] → [f^2_1 , f^2_2 , f_1 f_2 , f_1 , f_2 , 1]$ 

Then for $u = [1, 1, 0, −2a, −2b, a^2 + b^2 − 1]$

 $\phi (x_i)^T u = 0$

$u$ is orthogonal to $\phi(x_i)$ for all $i$ .
That is $\phi (x_i)$ live in a linear subspace.

u  i

$\phi(x_1), \phi(x_2), ..., \phi(x_n)$ live in a linear subspace of a higher dimension space for an appropriate .
Apply PCA on $\phi(xi)$ s.
**Note**: $\phi(xi)$ s need not to be centered even if xi s are centered.

If we apply the PCA on the transformed dataset, the K matrix will be given as

$K = [\phi(x_i )^T \phi(x_i )] _ {n×n}$

We need to transform each and every data point and compute the dot product for each pair.
There is better way to do it!!

## Kernel function

A function $k:\R^d \times \R^d \to \R$ is called a valid kernel if there exist a transformation mapping $\phi : \R^d \to \R^D$ such that

$k(x_i, x_j ) = \phi(x_i)^T \phi(x_j )$

How to check whether a function is a valid kernel?

1. Find out an appropriate mapping $\phi$
Or
2. Check the following two conditions:
- Symmetric: check $k(x_i, x_j ) = k(x_j , x_i)$ For all  $i, j$
- for any dataset $\{x_1, x_2, ..., x_n\}$, the matrix $K = [k(x_i , x_j )]$  is a positive semi definite.
    - Check if all the eigenvalues are non-negative or not.

Now, matrix can easily be computed as

$K_{ij} = k(x_i, x_j )$

Now, we have everything ready. Just apply the algorithm discussed in issue 1.

### Algorithm:

- step 1 Compute K using the kernel function.
- step 2 Center the matrix: $K_C = K − I_nK − KI_n + I_nkI_n$
where $I_n$  is the $(n, n)$  matrix with all entries equal to $1/n$ .
- Step 3: Compute eigen-decomposition of
Let $\{β_1, β_2, ..., β_l\}$ are the unit eigenvectors corresponding to eigenvalues $\{nλ_1, nλ_2, ..., nλ_l\}$
- Step 4: set $α_k = \cfrac{β_k} {\sqrt{nλ_k}}  = \cfrac {\text{unit eigenvector} }{\sqrt{\text{eigenvalue of K} }}$
- step 5: $w_k = \phi (X)α_k$

$w_k$ can not be computed without knowing $\phi$ explicitly.
But we still can compute the projetion:

$\phi (x_i)^T w_k = \sum ^n _{j=1} \alpha_{kj}k(x_i,x_j)$