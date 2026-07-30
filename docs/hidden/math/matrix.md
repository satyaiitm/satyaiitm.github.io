

**What is a matrix?**
Definition . A matrix is a rectangular array of numbers, arranged in rows and columns. (plural : matrices)
**Two important notions:**
• An $m × n$ matrix has $m$ rows and n columns.
• (i, j)-th entry of a matrix is the entry occuring in the i-th row and j-th column.
Let us try to understand these notions using the following example:
Example . 

$$
\begin {bmatrix} 1&2&3 \\ 2&3&4 \end{bmatrix} _{2\times3}     \begin {bmatrix} 1&2&3 \\ 4&5&6 \\ 7&8&9 \end{bmatrix} _{3X3}
$$

# Types of Matrix
The Comprehensive Matrix Taxonomy Guide


## Visual Reference: Types of Matrices 

$\begin{array}{ccc}\begin{array}{c} \textbf{Row Matrix} \\ \begin{bmatrix} 3 & 5 & 7 \end{bmatrix} \end{array} & \begin{array}{c} \textbf{Column Matrix} \\ \begin{bmatrix} 2 \\ 4 \\ 6 \end{bmatrix} \end{array} & \begin{array}{c} \textbf{Square Matrix} \\ \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} \end{array} \\[25pt]
\begin{array}{c} \textbf{Diagonal Matrix} \\ \begin{bmatrix} 4 & 0 \\ 0 & 9 \end{bmatrix} \end{array} & \begin{array}{c} \textbf{Scalar Matrix} \\ \begin{bmatrix} 5 & 0 \\ 0 & 5 \end{bmatrix} \end{array} & \begin{array}{c} \textbf{Identity Matrix} \\ \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} \end{array} \\[25pt]
\begin{array}{c} \textbf{Zero or Null Matrix} \\ \begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix} \end{array} & \begin{array}{c} \textbf{Upper Triangular} \\ \begin{bmatrix} 1 & 2 & 3 \\ 0 & 4 & 5 \\ 0 & 0 & 6 \end{bmatrix} \end{array} & \begin{array}{c} \textbf{Lower Triangular} \\ \begin{bmatrix} 1 & 0 & 0 \\ 2 & 3 & 0 \\ 4 & 5 & 6 \end{bmatrix} \end{array} \\[25pt]
\begin{array}{c} \textbf{Symmetric Matrix} \\ \begin{bmatrix} 1 & 2 \\ 2 & 3 \end{bmatrix} \end{array} & \begin{array}{c} \textbf{Skew-Symmetric} \\ \begin{bmatrix} 0 & 2 \\ -2 & 0 \end{bmatrix} \end{array} & \begin{array}{c} \textbf{Singular Matrix} \\ \begin{bmatrix} 2 & 4 \\ 1 & 2 \end{bmatrix} \end{array} \\[25pt]
\begin{array}{c} \textbf{Non-Singular Matrix} \\ \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} \end{array} & \begin{array}{c} \textbf{Orthogonal Matrix} \\ \begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix} \end{array} & \begin{array}{c} \textbf{Equal Matrices} \\ \begin{bmatrix} 2 & 3 \\ 4 & 5 \end{bmatrix} = \begin{bmatrix} 2 & 3 \\ 4 & 5 \end{bmatrix} \end{array}\end{array}$



| Category | Matrix Type | Mathematical Definition & Properties | Illustrative Example / Structure |
| :--- | :--- | :--- | :---: |
| **1. Structural Shapes** | **Square Matrix** | $m = n$ (Equal rows and columns). **Note:** We only define the main diagonal (the $(i,i)$-th elements) for square matrices. | $\begin{bmatrix} 0 & 0 & 0 \\\ 0 & 0 & 0 \\\ 0 & 0 & 0 \end{bmatrix}_{3 \times 3}$ |
| | **Rectangular Matrix** | $m \neq n$ (Rows do not equal columns) | — |
| | **Row Vector** | Matrix of size $1 \times n$ | $\begin{bmatrix} a_1 & a_2 & \dots & a_n \end{bmatrix}$ |
| | **Column Vector** | Matrix of size $m \times 1$ | $\begin{bmatrix} a_1 \\\ a_2 \\\ \vdots \\\ a_m \end{bmatrix}$ |
| **2. Basic Entry-Based** | **Zero / Null Matrix ($O$)** | $a_{ij} = 0 \quad \forall \, i, j$ | — |
| | **Identity Matrix ($I_n$)** | A scalar matrix whose main diagonal elements are all exactly $1$. | $\begin{bmatrix} 1 & 0 & 0 \\\ 0 & 1 & 0 \\\ 0 & 0 & 1 \end{bmatrix}$ |
| | **Diagonal Matrix ($D$)** | All off-diagonal elements are zero ($a_{ij} = 0 \;\; \forall \, i \neq j$). The main diagonal elements are typically non-zero. | $\begin{bmatrix} 1 & 0 & 0 \\\ 0 & 2 & 0 \\\ 0 & 0 & 3 \end{bmatrix}_{3 \times 3}$ |
| | **Scalar Matrix** | A square matrix where all diagonal elements are equal, and off-diagonal elements are zero ($a_{ij} = k \text{ if } i=j$). | $\begin{bmatrix} -3 & 0 & 0 \\\ 0 & -3 & 0 \\\ 0 & 0 & -3 \end{bmatrix}$ or $\begin{bmatrix} 0 & 0 & 0 \\\ 0 & 0 & 0 \\\ 0 & 0 & 0 \end{bmatrix}$ or $\begin{bmatrix} 1 & 0 & 0 \\\ 0 & 1 & 0 \\\ 0 & 0 & 1 \end{bmatrix}$ |
| **3. Triangular Matrices** | **Upper Triangular** | All elements below the main diagonal are zero ($a_{ij} = 0 \quad \forall \, i > j$). | $\begin{bmatrix} 1 & 2 & 3 \\\ 0 & 4 & 5 \\\ 0 & 0 & 6 \end{bmatrix}$ |
| | **Lower Triangular** | All elements above the main diagonal are zero ($a_{ij} = 0 \quad \forall \, i < j$). | $\begin{bmatrix} 1 & 0 & 0 \\\ 2 & 3 & 0 \\\ 4 & 5 & 6 \end{bmatrix}$ |
| | **Strictly Triangular** | $a_{ij} = 0 \quad \forall \, i = j$ (Zeros all along the main diagonal). | — |
| **4. Symmetry Operations**| **Symmetric Matrix** | Equal to its own transpose ($A = A^T \iff a_{ij} = a_{ji}$). | $\begin{bmatrix} 1 & 2 & 3 \\\ 2 & 4 & 5 \\\ 3 & 5 & 6 \end{bmatrix}$ |
| | **Skew-Symmetric** | Equal to its negative transpose ($A = -A^T \iff a_{ij} = -a_{ji}$). **Note:** Main diagonal elements must be exactly $0$. | $\begin{bmatrix} 0 & 2 & -3 \\\ -2 & 0 & 5 \\\ 3 & -5 & 0 \end{bmatrix}$ |
| | **Hermitian Matrix** | Equal to its complex conjugate transpose ($A^* = A \iff a_{ij} = \overline{a_{ji}}$). | — |
| | **Skew-Hermitian** | Equal to its negative complex conjugate transpose ($A^* = -A \iff a_{ij} = -\overline{a_{ji}}$). | — |
| **5. Operational & Spectral**| **Orthogonal Matrix** | $A^T A = A A^T = I \iff A^{-1} = A^T$ (Real orthonormal columns). | — |
| | **Unitary Matrix** | $A^* A = A A^* = I \iff A^{-1} = A^*$ (Complex orthonormal columns). | — |
| | **Normal Matrix** | $A^* A = A A^* \quad$ (Commutes with its conjugate transpose). | — |
| | **Invertible / Regular** | $\det(A) \neq 0 \iff A^{-1} \text{ exists}$. | — |
| | **Singular Matrix** | $\det(A) = 0 \iff \text{No inverse exists}$. | — |
| **6. Algebraic Powers** | **Idempotent Matrix** | $A^2 = A \quad$ (Acts as a geometric projection). | — |
| | **Nilpotent Matrix** | $A^k = O \quad$ for some positive integer $k$. | — |
| | **Involutary Matrix** | $A^2 = I \iff A = A^{-1}$ (Acts as its own inverse matrix reflection). | — |




- **Orthogonal Matrix**: An orthogonal matrix has columns that are orthonormal vectors, meaning they are perpendicular and have a length of one, while a unitary matrix can have complex entries and preserves inner products in a more general sense.
- **Unitary Matrices**: These are similar to orthogonal matrices but can include complex numbers; their defining property is that their conjugate transpose is equal to their inverse.
- **Normal Matrix**: A normal matrix commutes with its conjugate transpose, which is a broader category than unitary matrices, as not all normal matrices are unitary; unitary matrices specifically require the matrix to be square and have orthonormal columns.
- **Symmetric Matrices**: While orthogonal matrices have the property that their transpose equals their inverse, symmetric matrices have the property that they are equal to their own transpose, which is a different concept
- **Similar matrices**: Two matrices are similar if they represent the same linear transformation in different bases, but not all similar matrices are unitarily diagonalizable, as similarity does not guarantee the existence of a unitary matrix for diagonalization.
- **Skew-Symmetric Matrices**: These are square matrices that are equal to the negative of their own transpose, meaning that the elements satisfy the condition $A^T = -A$, which is the opposite of symmetric matrices.
- **Diagonal Matrices**: While all symmetric matrices can be diagonal, not all diagonal matrices are symmetric; a diagonal matrix is symmetric only if its diagonal elements are equal.
- **Orthogonal Matrices**: These are square matrices whose rows and columns are orthonormal vectors, which means that they can be symmetric, but they specifically satisfy the condition $A^T A = I$, where I is the identity matrix



### Summary Table

| Matrix Type | Defining Property |
|-------------|-------------------|
| Square | $m=n$ |
| Rectangular | $m\ne n$ |
| Zero | $a_{ij}=0$ |
| Identity | $I$ |
| Diagonal | $a_{ij}=0,\ i\ne j$ |
| Scalar | $A=kI$ |
| Upper Triangular | $a_{ij}=0,\ i>j$ |
| Lower Triangular | $a_{ij}=0,\ i<j$ |
| Symmetric | $A^T=A$ |
| Skew-Symmetric | $A^T=-A$ |
| Hermitian | $A^*=A$ |
| Orthogonal | $A^TA=I$ |
| Unitary | $A^*A=I$ |
| Normal | $A^*A=AA^*$ |
| Invertible | $\det(A)\ne0$ |
| Singular | $\det(A)=0$ |
| Idempotent | $A^2=A$ |
| Nilpotent | $A^k=O$ |
| Involutory | $A^2=I$ |
| Positive Definite | $x^TAx>0$ |
| Positive Semi-Definite | $x^TAx\ge0$ |
| Projection | $P^2=P$ |







## Matrix Multiplication

 $A_{m×n}B_{n×p} = (AB)_{m×p}$ 

$\boxed{(AB)_{ij} = \textstyle \sum _{k=1}^n  A_{ik} .B_{kj}}$

$\begin{bmatrix}1 & 2 & 3 \\. & . & . \\. &.  & .\end{bmatrix} \times \begin{bmatrix} 1&.  \\2 & . \\3 & .\end{bmatrix}$
$\text{Remark - Multiplication of matrices A and B is defined only when thenumber of <<columns of A>> is the same as the <<number of rows of B>>}$

$$
\begin {bmatrix} c&0&0 \\ 0&c&0 \\ 0&0&c \end{bmatrix} _{3X3} = \begin {bmatrix} 1&2 \\ 3&4 \\ 5&6 \end{bmatrix} _{3X2} =\begin {bmatrix} c1&c2 \\ c3&c4 \\ c5&c6 \end{bmatrix} _{3X2} = c\begin {bmatrix} 1&2 \\ 3&4 \\ 5&6 \end{bmatrix} _{3X2}
$$





## 1. Rows Multiplied by Columns (Standard Element-wise)

$\begin{aligned}
A = \begin{bmatrix} 1 & 2 & 2 & 0 \\ 2 & 1 & 2 & 1 \\ 0 & 2 & 1 & 2 \end{bmatrix}, \quad
B = \begin{bmatrix} 1 & 2 \\ -2 & -1 \\ -1 & 2 \\ 2 & -2 \end{bmatrix}
\end{aligned}$


------------------------------
## 2. Linear Combination of $A$'s Columns (Column-wise)

$\begin{aligned}
A = \underbrace{\begin{bmatrix} 1 & 2 & 2 & 0 \\ 2 & 1 & 2 & 1 \\ 0 & 2 & 1 & 2 \end{bmatrix}}_{\mathbf{a}_1 \quad \mathbf{a}_2 \quad \mathbf{a}_3 \quad \mathbf{a}_4}, \quad
B = \begin{bmatrix} 1 & 2 \\ -2 & -1 \\ -1 & 2 \\ 2 & -2 \end{bmatrix}
\end{aligned}$


------------------------------
## 3. Linear Combination of $B$'s Rows (Row-wise)

$\begin{aligned}
A = \begin{bmatrix} 1 & 2 & 2 & 0 \\ 2 & 1 & 2 & 1 \\ 0 & 2 & 1 & 2 \end{bmatrix}, \quad
B = \begin{bmatrix} 1 & 2 \\ -2 & -1 \\ -1 & 2 \\ 2 & -2 \end{bmatrix}
\begin{matrix} \mathbf{b}_1^T \\ \mathbf{b}_2^T \\ \mathbf{b}_3^T \\ \mathbf{b}_4^T \end{matrix}
\end{aligned}$


------------------------------
## 4. Columns Multiplied by Rows (Outer Product Expansion)

$\begin{aligned}
A = \underbrace{\begin{bmatrix} 1 & 2 & 2 & 0 \\ 2 & 1 & 2 & 1 \\ 0 & 2 & 1 & 2 \end{bmatrix}}_{\mathbf{a}_1 \quad \mathbf{a}_2 \quad \mathbf{a}_3 \quad \mathbf{a}_4}, \quad
B = \begin{bmatrix} 1 & 2 \\ -2 & -1 \\ -1 & 2 \\ 2 & -2 \end{bmatrix}
\begin{matrix} \mathbf{b}_1^T \\ \mathbf{b}_2^T \\ \mathbf{b}_3^T \\ \mathbf{b}_4^T \end{matrix}
\end{aligned}$




## 1. Column-by-Column Method (Top Left)

$\begin{aligned}
&A = \begin{bmatrix} 1 & 2 & 2 & 0 \\ 2 & 1 & 2 & 1 \\ 0 & 2 & 1 & 2 \end{bmatrix}, \quad B = \begin{bmatrix} 1 & 2 \\ -2 & -1 \\ -1 & 2 \\ 2 & -2 \end{bmatrix} \\[2ex]
&1 \begin{bmatrix} 1 \\ 2 \\ 0 \end{bmatrix} + (-2) \begin{bmatrix} 2 \\ 1 \\ 2 \end{bmatrix} + (-1) \begin{bmatrix} 2 \\ 2 \\ 1 \end{bmatrix} + 2 \begin{bmatrix} 0 \\ 1 \\ 2 \end{bmatrix} = \begin{bmatrix} -5 \\ 0 \\ -1 \end{bmatrix} \\[1.5ex]
&2 \begin{bmatrix} 1 \\ 2 \\ 0 \end{bmatrix} + (-1) \begin{bmatrix} 2 \\ 1 \\ 2 \end{bmatrix} + 2 \begin{bmatrix} 2 \\ 2 \\ 1 \end{bmatrix} + (-2) \begin{bmatrix} 0 \\ 1 \\ 2 \end{bmatrix} = \begin{bmatrix} 4 \\ 5 \\ -4 \end{bmatrix}
\end{aligned}
\qquad AB = \begin{bmatrix} -5 & 4 \\ 0 & 5 \\ -1 & -4 \end{bmatrix}$


## 2. Row-by-Row Method (Top Right)

$\begin{aligned}
&A = \begin{bmatrix} 1 & 2 & 2 & 0 \\ 2 & 1 & 2 & 1 \\ 0 & 2 & 1 & 2 \end{bmatrix}, \quad B = \begin{bmatrix} 1 & 2 \\ -2 & -1 \\ -1 & 2 \\ 2 & -2 \end{bmatrix} \\[2ex]
&\begin{array}{ccc}
\text{ Row 1} & \text{ Row 2} & \text{ Row 3} \\
\begin{aligned}
&1 \begin{bmatrix} 1 & 2 \end{bmatrix} \\
+\; &2 \begin{bmatrix} -2 & -1 \end{bmatrix} \\
+\; &2 \begin{bmatrix} -1 & 2 \end{bmatrix} \\
+\; &0 \begin{bmatrix} 2 & -2 \end{bmatrix} \\
\hline
&\begin{bmatrix} -5 & 4 \end{bmatrix}
\end{aligned}
&
\begin{aligned}
&2 \begin{bmatrix} 1 & 2 \end{bmatrix} \\
+\; &1 \begin{bmatrix} -2 & -1 \end{bmatrix} \\
+\; &2 \begin{bmatrix} -1 & 2 \end{bmatrix} \\
+\; &1 \begin{bmatrix} 2 & -2 \end{bmatrix} \\
\hline
&\begin{bmatrix} 0 & 5 \end{bmatrix}
\end{aligned}
&
\begin{aligned}
&0 \begin{bmatrix} 1 & 2 \end{bmatrix} \\
+\; &2 \begin{bmatrix} -2 & -1 \end{bmatrix} \\
+\; &1 \begin{bmatrix} -1 & 2 \end{bmatrix} \\
+\; &2 \begin{bmatrix} 2 & -2 \end{bmatrix} \\
\hline
&\begin{bmatrix} -1 & -4 \end{bmatrix}
\end{aligned}
\end{array}
\end{aligned}
\qquad AB = \begin{bmatrix} -5 & 4 \\ 0 & 5 \\ -1 & -4 \end{bmatrix}$


## 3. Outer Product Expansion / Columns $\times$ Rows (Bottom)

$\begin{aligned}
&A = \begin{bmatrix} 1 & 2 & 2 & 0 \\ 2 & 1 & 2 & 1 \\ 0 & 2 & 1 & 2 \end{bmatrix}, \quad B = \begin{bmatrix} 1 & 2 \\ -2 & -1 \\ -1 & 2 \\ 2 & -2 \end{bmatrix} \\[2ex]
&\begin{bmatrix} 1 \\ 2 \\ 0 \end{bmatrix} \begin{bmatrix} 1 & 2 \end{bmatrix} + \begin{bmatrix} 2 \\ 1 \\ 2 \end{bmatrix} \begin{bmatrix} -2 & -1 \end{bmatrix} + \begin{bmatrix} 2 \\ 2 \\ 1 \end{bmatrix} \begin{bmatrix} -1 & 2 \end{bmatrix} + \begin{bmatrix} 0 \\ 1 \\ 2 \end{bmatrix} \begin{bmatrix} 2 & -2 \end{bmatrix} \\[2ex]
&= \begin{bmatrix} 1 & 2 \\ 2 & 4 \\ 0 & 0 \end{bmatrix} + \begin{bmatrix} -4 & -2 \\ -2 & -1 \\ -4 & -2 \end{bmatrix} + \begin{bmatrix} -2 & 4 \\ -2 & 4 \\ -1 & 2 \end{bmatrix} + \begin{bmatrix} 0 & 0 \\ 2 & -2 \\ 4 & -4 \end{bmatrix} = \begin{bmatrix} -5 & 4 \\ 0 & 5 \\ -1 & -4 \end{bmatrix}
\end{aligned}$


**Properties of matrix addition and multiplication**

- $AB \ne BA$ 
- $(A + B) + C = A + (B + C )$ (Associativity of addition)
- $(AB)C = A(BC )$ (Associativity of multiplication)
- $A + B = B + A$ (Commutativity of addition)
- $λ(A + B) = λA + λB$ for some real number λ.
- $λ(AB) = (λA)B = A(λB)$ for some real number λ.
- $A(B + C ) = AB + AC$
- $(A + B)C = AC + BC$
- $(AB)^T = B^T  A^T$
- $I_n A = AI_n = A_{n \times m}$ 

- if $A = B^T$  then $AB$ is symmetric matrix
- if $E_2E_1B = B$ then $E_2E_1 = I$
- if A and B bothe are “lower triangular matrix ” then AB is also “lower triangular matrix” (same for upper_triangular matrix and diagonal matrix)
- if A is lower-triangular and B is Upper-triangular matrix, then in general $AB,BA,A^TA, B^TB,AA^T,BB^T$ none of these are triangular

**some fun with matrix multiplication**

$I = \begin {bmatrix} 1&0&0 \\ 0&1&0 \\ 0&0&1 \end{bmatrix}$, $A = \begin {bmatrix} 1&2&3 \\ 4&5&6 \\ 7&8&9 \end{bmatrix}$ then $IA = \begin {bmatrix} 1&2&3 \\ 4&5&6 \\ 7&8&9 \end{bmatrix}$

$P = \begin {bmatrix} 0&1&0 \\ 1&0&0 \\ 0&0&1 \end{bmatrix}$, $A = \begin {bmatrix} 1&2&3 \\ 4&5&6 \\ 7&8&9 \end{bmatrix}$then

 $PA = \begin {bmatrix}  4&5&6 \\ 1&2&3 \\ 7&8&9 \end{bmatrix}$ (this is pre-multiplication, it changes the position of the rows)

$AP = \begin {bmatrix} 2&1&3 \\ 5&4&6 \\ 8&7&9 \end{bmatrix}$ (this is post-multiplication, it changes the position of the columns)

# Trace   ($tr(A)$)

$\boxed{tr(A) = \sum _i a_{ii}}$  (sum of all diagonal elements)

$A = \begin {bmatrix} a&b&c \\ d&e&f \\ g&h&i \end{bmatrix}$  then     $tr(A) = a + e + i$

**Properties of trace of a matrix**

- $tr(A) = tr(A^T)$
- $tr(cA) = c . tr(A)$
- $tr(A+B)=tr(A)+tr(B)$
- $tr(AB)=tr(BA)$
- $tr(ABC)=tr(BAC)=tr(CAB)$


# Transpose Matrix ($A^T$)

$\boxed{A_{ij} \to A_{ji}}$

$A = \begin {bmatrix} 1&2&3 \\ 4&5&6 \\ 7&8&9 \end{bmatrix}$ then $A^T = \begin {bmatrix} 1&4&7 \\ 2&5&8 \\ 3&6&9 \end{bmatrix}$

**Properties of transpose of a matrix**

- $\left[ A^{T}\right] ^{T}=A$
- $\left( cA\right) ^{T}=cA^{T}$
- $\left( A+B\right) ^{T}=A^{T}+B^{T}$
- $\left( AB\right) ^{T}=B^{T}A^{T}$
- $det(A^T) = det(A)$


# Determinant

 Notation ======  $det(A)$ or $|A|$
It is used in :
- solving a system of linear equations,
- finding the inverse of a matrix,
- calculus and more.

**First order Determinant :**
If A = [a]
$det(A) = a$
**Second Order Determinant**

$A = \begin {bmatrix} a&b \\ c&d \end {bmatrix}$
 $det(A) = ad − bc$

**Third Order Determinant:**

 $A = \begin {bmatrix}
a & b & c\\
d & e & f \\
g & h & i \end {bmatrix}$

$$
\text{Expansion along the first row} >>>\\  det(A) =a \times det \begin {bmatrix}
e & f \\
h & i \end {bmatrix} - b \times det \begin {bmatrix}
d & f \\
g & i \end {bmatrix}+c \times det \begin {bmatrix}
d & e \\
g & h \end {bmatrix} \\ \\
\\ \begin {bmatrix}
a & . & .\\
. & e & f \\
. & h & i \end {bmatrix} , 
\begin {bmatrix}
. & b & .\\
d & . & f \\
g & . & i \end {bmatrix}
\begin {bmatrix}
. & . & c\\
d & e & . \\
g & h & . \end {bmatrix}
$$

Expansion along the any row    $(-1)^{i+j} \to \begin {bmatrix}
+ & - & +\\
- & + & - \\
+ & - & + \end {bmatrix}$

**Third order determinant**
Consider a $3 × 3$ matrix A as follows: 
$A = \begin {bmatrix}a_{11}&a_{12}&a_{13}\\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33} \end {bmatrix}$

$\boxed{det(A) = (−1)^{1+1}a_{11} × det \begin {bmatrix} a22& a23\\a32 &a33 \end {bmatrix}+ (−1)^{1+2}a_{12} × det \begin {bmatrix} a21& a23\\a31& a33 \end {bmatrix}+ (−1)^{1+3}a_{13} × det \begin {bmatrix} a21& a22\\a31& a32 \end {bmatrix}\\} \\ \text{((expended over first row, we can expand similar over second or third row))}$

$=a11(a22.a33 − a23.a32) − a12(a21.a33 − a23.a31) + a13(a21.a32 − a22.a31)$

$$
\begin {bmatrix}
a11 & . & .\\
. & a22 & a23 \\
. & a32 & a33 \end {bmatrix} 
\begin {bmatrix}
. & a12 & .\\
a21 & . & a23 \\
a31 & . & a33 \end {bmatrix}
\begin {bmatrix}
. & . & a13\\
a21 & a22 & . \\
a31 & a32 & . \end {bmatrix}
$$

## Minot

$A_{n\times n}$  $\longrightarrow$ n can be at most 4 $(n \le 4)$

Name = the $(i,j)^{th }$ minor

Notation = $M_{ij}$

$$
A = \begin {bmatrix}
a & b & c\\
d & e & f \\
g & h & i \end {bmatrix} \\
M_{11} = det \begin {bmatrix}
e & f \\
h & i \end {bmatrix} M_{12} = det \begin {bmatrix}
d & f \\
g & i \end {bmatrix} M_{13} = det \begin {bmatrix}
d & e \\
g & h \end {bmatrix}
$$

## Cofactor

Name = the $(i,j)-th$ cofactor

Notation = $C_{ij}$

$$
C_{ij} = (-1)^{i+j} M_{ij}
$$

$\left[\begin{array}{ccc}
C_{11} & C_{12} & C_{13} \\
C_{21} & C_{22} & C_{23} \\
C_{31} & C_{32} & C_{33} 
\end{array}\right] = \begin {bmatrix}
M_{11} & -M_{12} & M_{13}\\
-M_{21} & M_{22} & -M_{23} \\
M_{31} & -M_{32} & M_{33} \end {bmatrix}$

**Back to Determinants** 

$\text {\ (expention along the first row)} \\ det(A) =a . det \begin {bmatrix}
e & f \\
h & i \end {bmatrix} - b.det \begin {bmatrix}
d & f \\
g & i \end {bmatrix}+c.det \begin {bmatrix}
d & e \\
g & h \end {bmatrix}$

$det(A)$   in terms of minor
$det(A)= a.M_{11}-b.M_{12}+c.M_{13}$ 

$(det(A) \ in \ terms \ of \ cofactor) \\det(A)= a.C_{11}+b.C_{12}+c.C_{13} \qquad$ 

**Determinant can be calculated by expanding any row or cloumn. and the result is the same.**

$det(A) = \sum^n_{j=1} (-1)^{i+j} a_{ij}M_{ij} \qquad \text{for a fixed i} \\= (-1)^{i+j}a_{ij} M_{ij} +(-1)^{i+j}a_{ij} M_{ij}+(-1)^{i+j}a_{ij} M_{ij}$

$det(A) = \sum^n_{i=1} (-1)^{i+j} a_{ij}M_{ij} \qquad \text{for a fixed j} \\= (-1)^{i+j}a_{ij} M_{ij} +(-1)^{i+j}a_{ij} M_{ij}+(-1)^{i+j}a_{ij} M_{ij}$

(Expention along any row or column) to find determinant of a matrix

**Properties of determinant of matrices.**

- $det(I)=1$ (of any order n)
- $det(A^{2}) = [{det(A)}]^2$
- $det(AA^{−1}) = det(I)$, i.e., $det(A).det(A^{−1}) = 1$ 
- $det(PAP^{-1})=det(A)$
- $det(A^{−1}) = \frac {1}{det(A)}$ .
- $det(A^T ) = det(A)$, where $A^T$ denotes the transpose of matrix A.
- $det(AB) = det(A)det(B)$, where both A and B are n × n matrices 
- $det \left( cA\right) _{n\times n}=c^{n}\left| A\right|$

- **Switching two rows or columns**  = changes the sign of the determinant.
    
    $det\begin{bmatrix} 1&5&-7\\6&0&4\\2&3&5 \end{bmatrix} = -det\begin{bmatrix} 2&3&5\\6&0&4\\ 1&5&-7\end{bmatrix} \ ( here \ R_1 \ and  \ R_2\  interchanged)$  
    
- Add scaler multiple of one **row or column** to othor
    

$$ R_1 \rightarrow R_1 + kR_3 $$

$$
\det\begin{bmatrix}
1 & 5 & -7\\
6 & 0 & 4\\
2 & 3 & 5
\end{bmatrix}
=
\det\begin{bmatrix}
1+2k & 5+3k & -7+5k\\
6 & 0 & 4\\
2 & 3 & 5
\end{bmatrix}
$$

    
- Scalar multiplication of a row by a constant t multiplies the determinant by t.
    
    $det\begin{bmatrix} 17(6)&3(6)&5(6)\\6&0&4\\2&3&5 \end{bmatrix} = 6 \times det\begin{bmatrix} 17&3&5\\6&0&4\\2&3&5 \end{bmatrix}$ 
    
    $det\begin{bmatrix} 17/6&3/6&5/6\\6&0&4\\2&3&5 \end{bmatrix} = 1/6 \ \ det \begin{bmatrix} 17&3&5\\6&0&4\\2&3&5 \end{bmatrix}$
    
    $\boxed{det(k.A)=k^n.det(A) \qquad were \ A \ is \ A_{(n\times n)} \ matrix }$
    
    $det
    \begin{bmatrix} 17(6)&3(6)&5(6)\\6(4)&0(4)&4(4)\\2(2)&3(2)&5(2) \end{bmatrix} = 6.4.2.\ det \begin{bmatrix} 17&3&5\\6&0&4\\2&3&5 \end{bmatrix}$
    
- If all the values of a row or a column is zero = determinant is zero
    
    $det\begin{bmatrix} 0&0&0\\6&0&4\\2&3&5 \end{bmatrix} = 0$
    
- If two row (or column) are identical = determinant is zero
    
    $\begin{vmatrix} 2&3&5\\6&0&4\\2&3&5 \end{vmatrix} = 0$
    
    $det\begin{bmatrix} a&b&c\\a+2x&b+2y&c+2z\\x&y&z \end{bmatrix}  = det\begin{bmatrix} a&b&c\\a&b&c\\x&y&z  \end{bmatrix} + det\begin{bmatrix} a&b&c\\2x&2y&2z\\x&y&z  \end{bmatrix}\\ =det\begin{bmatrix} a&b&c\\a&b&c\\x&y&z  \end{bmatrix} + 2 \times det\begin{bmatrix} a&b&c\\x&y&z\\x&y&z  \end{bmatrix} = 0 + 2(0) = 0$
    
- Determinant of a **upper-triangular or lower-triangular** matrix is equan to the multiplication fo the diagonal elements of the matrix.
    
    $\begin{vmatrix} a&b&c\\0&e&f\\0&0&z  \end{vmatrix} = \begin{vmatrix} a&0&0\\d&e&0\\x&y&z \end{vmatrix} =  a . e . z$
    
    $\begin{vmatrix} 1&0&0\\0&1&0\\0&0&1  \end{vmatrix}=\begin{vmatrix} 1&0\\0&1 \end{vmatrix}=1$
    

# Adjoint of a squire matrix

**Adjoint or Adjugate or Adjunct**

$A = \begin {bmatrix}
a & b & c\\
d & e & f \\
g & h & i \end {bmatrix}\\
Minor \longrightarrow
M_{11} = det \begin {bmatrix}
e & f \\
h & i \end {bmatrix} \\
Cofactor \longrightarrow
C_{ij} = (-1)^{i+j} M_{ij}$

$Cofactor \ matrix = \begin {bmatrix}C11&C12&C13\\
C21 & C22 & C23 \\
C31 & C32 & C33 \end {bmatrix}$

$Adjoint \ matrix = \large C^T \\(transpose \ of \ cofactor \ matrix)$

**Properties of Adjoint matrix**

- $Adj(I_{3X3})=I_{3X3}$
- $Adj(Zero\ matrix)=Zero \ matrix$
- $Adj(A)=A^{-1} \qquad then \qquad det(A)=1$
- $Adj(AB)= Adj(B).Adj(A)$
- $Adj(A+B)=Adj(A)+Adj(B)$
- $Adj(A^T)=Adj(A)^T$
- $Adj(A^{-1})=Adj(A)^{-1}$
- $A.Adj(A)=Adj(A).A=det(A).I$
- $|Adj(A)|=|A|^{n-1}$
- $Adj(Adj(A))=|A|^{n-2} . A$
- $Adj(k.A)=k^{n-1}.Adj(A)$

# Inverse of a matrix

$$
A^{-1} = \frac{1}{det(A)} \ adj(A)
$$

$A = \begin{bmatrix} a &b \\ c &d \end{bmatrix} , then \to A^{-1} = \frac{1}{ad-bc}\begin{bmatrix} d &-b \\ -c & a \end{bmatrix}$

$[A | I] \to [I | A^{-1}]$

**Property**

- if $A = A^{-1}$ then $A^2 = I$
- $(A ^{-1})^T = (A ^T)^{-1}$
- $(AB)^{-1} = B^{-1} A^{-1}$
- $(I+A)^{-1} = A^{-1}(I+A^{-1})^{-1}$
- $(symmetric)^{-1} = symmetric$
- $(diagonal)^{-1} = diagonal \to \begin {smallmatrix}
a & 0 & 0\\
0 & b & 0 \\
0 & 0 & c \end {smallmatrix}^{-1} = \begin {smallmatrix}
1/a & 0 & 0\\
0 & 1/b & 0 \\
0 & 0 & 1/c \end {smallmatrix}$
- $(triangular)^{-1} = triangular \text{(of same pattern, and diagonal elements will be reciprocal)}$

# (Reduced ) Row echelon form

Axiams

- The first non-zero element in each row must be ‘1’
- Each leading element in a column to athe right of the leading entry in the previous row.
- Row with all zero element, if any are below rows having a non-zero element.
- for a non-zero row, the leading entry in the row is the only non_zero entry iin the column (RFEF)

$\begin{bmatrix}a^* & 2  & 3 & 4  \\0 & 0  & b^* & 3 \\ 0 & 0 &0 & 0\end{bmatrix}$ , a* and b* 

# Linear equations and matrices

One of the important applications of matrices is to study the system of linear equa-
tions. A set of linear equations can be represented in terms of matrices. We will
study later how we can find solutions of the system using this representation. For
now, let us take to example to understand how we can represent the systems using
matrices.

## Linear equation



