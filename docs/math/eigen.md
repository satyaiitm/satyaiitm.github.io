# eigenvalues and eigenvectors

Here’s a comprehensive list of the key properties of eigenvalues and eigenvectors:

### Properties of Eigenvalues

1. **Sum and Product of Eigenvalues**:
    - The sum of the eigenvalues of a matrix $A$  is equal to the trace of $A$ (the sum of the diagonal elements).
    - The product of the eigenvalues is equal to the determinant of $A$ .
2. **Eigenvalues of Similar Matrices**:
    - Similar matrices (i.e., matrices  $A$  and  $B$  such that $( B = P^{-1}AP ))$ have the same eigenvalues.
3. **Eigenvalues of Powers of a Matrix**:
    - If  $\lambda$  is an eigenvalue of  $A$ , then  $\lambda^k$  is an eigenvalue of  $A^k$  for any positive integer  $k$ .
4. **Eigenvalues of the Inverse of a Matrix**:
    - If  $\lambda$  is a nonzero eigenvalue of an invertible matrix A , then $\frac{1}{\lambda}$  is an eigenvalue of  $A^{-1}$ .
5. **Spectral Radius**:
    - The spectral radius of a matrix \( A \), which is the largest absolute value among its eigenvalues, indicates the matrix's dominant eigenvalue's "strength."
6. **Eigenvalues of Transpose**:
    - The eigenvalues of  $A^T$  are the same as those of  $A$ .
7. **Eigenvalues and Stability in Dynamical Systems**:
    - For a linear system  $\dot{x} = Ax$ , if all eigenvalues of  $A$  have negative real parts, the system is stable.
8. **Zero Eigenvalues and Matrix Singularity**:
    - If  $0$  is an eigenvalue of  $A$ , then  $A$  is singular (non-invertible).
9. **Algebraic and Geometric Multiplicities**:
    - The algebraic multiplicity (how many times an eigenvalue is repeated) is at least as large as its geometric multiplicity (the number of linearly independent eigenvectors associated with it).
10. **Hermitian and Symmetric Matrices**:
    - For Hermitian (complex conjugate transpose equal to itself) or symmetric (transpose equal to itself) matrices, all eigenvalues are real.
11. **Positive Definite and Semi-Definite Matrices**:
    - For a positive definite matrix, all eigenvalues are positive. For a positive semi-definite matrix, all eigenvalues are non-negative.
12. **Skew-Symmetric Matrices**:
    - If  $A$  is a real skew-symmetric matrix (i.e.,  $A^T = -A$ ), its eigenvalues are purely imaginary or zero.
13. **Orthogonal Matrices**:
    - For an orthogonal matrix  $Q$  (i.e.,  $Q^T Q = I$ ), eigenvalues have an absolute value of 1 (they lie on the unit circle in the complex plane).

### Properties of Eigenvectors

1. **Uniqueness of Eigenvectors**:
    - Eigenvectors corresponding to distinct eigenvalues of a matrix are linearly independent.
2. **Scaling of Eigenvectors**:
    - If  $\mathbf{v}$  is an eigenvector of  $A$  associated with eigenvalue  $\lambda$ , then any scalar multiple  $c\mathbf{v}$  (where  $c \neq 0$ ) is also an eigenvector associated with  $\lambda$ .
3. **Orthogonality of Eigenvectors for Symmetric Matrices**:
    - For symmetric (or Hermitian) matrices, eigenvectors corresponding to distinct eigenvalues are orthogonal to each other.
4. **Eigenvectors of Similar Matrices**:
    - If  $A$  and  $B$  are similar matrices, their eigenvectors are related through the transformation matrix  $P$  (i.e., if  $B = P^{-1}AP$ , then the eigenvectors of  $B$  are transformed by  $P$  from the eigenvectors of  $A$ ).
5. **Eigenvectors of Power of a Matrix**:
    - If  $\mathbf{v}$  is an eigenvector of  $A$  corresponding to eigenvalue  $\lambda$ , then  $\mathbf{v}$  is also an eigenvector of  $A^k$  corresponding to eigenvalue  $\lambda^k$ .
6. **Eigenvectors and Diagonalization**:
    - A matrix $A$  can be diagonalized if it has a complete set of linearly independent eigenvectors.
7. **Eigenvectors of a Diagonal Matrix**:
    - For a diagonal matrix, the standard basis vectors are the eigenvectors.
8. **Invariance under Scalar Multiplication**:
    - If  $A\mathbf{v}$ = $\lambda \mathbf{v}$ , then  $cA\mathbf{v} = c\lambda \mathbf{v}$  for any scalar  $c$ , meaning the scalar multiple  $cA$  has eigenvector  $\mathbf{v}$  associated with eigenvalue  $c\lambda$ .
9. **Eigenvectors and Stability Analysis in Dynamical Systems**:
    - The eigenvectors of the system matrix  $A$  indicate the directions of the system's growth or decay and help analyze stability.
10. **Right and Left Eigenvectors**:
    - For a non-square matrix or generalized cases, there can be both right eigenvectors (satisfying  $A \mathbf{v} = \lambda \mathbf{v}$ ) and left eigenvectors (satisfying  $\mathbf{w}^T A = \lambda \mathbf{w}^T$ ), which are generally different.

### Combined Properties of Eigenvalues and Eigenvectors

1. **Diagonalization and Jordan Form**:
    - A matrix  $A$  is diagonalizable if it has a full set of linearly independent eigenvectors. If not, it can still be put in Jordan form, where each Jordan block corresponds to an eigenvalue.
2. **Similarity Transformations**:
    - Eigenvalues are invariant under similarity transformations, but eigenvectors change according to the transformation matrix  $P$  (if  $B = P^{-1}AP$ ).
3. **Stability and Dynamics**:
    - In applications, eigenvalues determine the nature (e.g., oscillatory, stable, or unstable) of system dynamics, while eigenvectors give the directions of these dynamics.
4. **Spectral Theorem**:
    - The spectral theorem states that any symmetric matrix  $A$  can be decomposed into a form  $A = Q \Lambda Q^T$ , where  $Q$  is an orthogonal matrix containing the eigenvectors and  $\Lambda$  is a diagonal matrix with the eigenvalues on the diagonal.

## **Diagonalization**

**Diagonalization** is a process in linear algebra where we convert a matrix into a diagonal form, making it simpler to work with. Specifically, a matrix  A  is said to be **diagonalizable** if there exists an invertible matrix  P  and a diagonal matrix  D  such that:
$A = PDP^{-1}$
where:

- P  is a matrix whose columns are the eigenvectors of  A .
- D  is a diagonal matrix containing the eigenvalues of  A  along the diagonal.

Diagonalizing a matrix can make computations like finding powers of the matrix or analyzing its behavior in systems of differential equations much easier.

### When Can a Matrix Be Diagonalized?

A matrix \( A \) can be diagonalized if:

1. It has \( n \) **linearly independent eigenvectors** (where \( n \) is the size of \( A \), for an \( n \times n \) matrix).
2. The algebraic multiplicity of each eigenvalue (i.e., how many times it appears as a root of the characteristic polynomial) matches its geometric multiplicity (the dimension of its eigenspace).

In practical terms, for an \( $n \times n$ \) matrix, if \( A \) has \( n \) distinct eigenvalues, then it is diagonalizable.

### Diagonalization Process

1. **Find the Eigenvalues**: Solve the characteristic polynomial \(\det(A - \lambda I) = 0\) to find the eigenvalues of \( A \).
2. **Find the Eigenvectors**: For each eigenvalue \( \lambda \), find the eigenvectors by solving \( (A - \lambda I) \mathbf{x} = 0 \).
3. **Form the Matrix \( P \)**: Construct the matrix \( P \) with each column as an eigenvector of \( A \).
4. **Form the Matrix \( D \)**: Create the diagonal matrix \( D \), placing each eigenvalue in the corresponding diagonal position (matching the position of its eigenvector in \( P \)).
5. **Verify**: Confirm that \( A = PDP^{-1} \) by multiplying the matrices to ensure the equality holds.

### Example

Consider the matrix:

$A = \begin{pmatrix} 4 & 1 \\ 2 & 3 \end{pmatrix}$

### Step 1: Find the Eigenvalues

1. Calculate  $\det(A - \lambda I) = 0$ :

$\det\begin{pmatrix} 4 - \lambda & 1 \\ 2 & 3 - \lambda \end{pmatrix} = (4 - \lambda)(3 - \lambda) - (2)(1) = \lambda^2 - 7\lambda + 10 = 0$

2. $Solve  \lambda^2 - 7\lambda + 10 = 0 \ to \ find \ \lambda = 5 \ and \ \lambda = 2$ .

### Step 2: Find Eigenvectors

1. $For  \lambda = 5 , solve  (A - 5I)\mathbf{x} = 0 :$

$\begin{pmatrix} -1 & 1 \\ 2 & -2 \end{pmatrix} \mathbf{x} = 0 \Rightarrow \mathbf{x} = \begin{pmatrix} 1 \\ 1 \end{pmatrix}$

2. $For  \lambda = 2 , solve  (A - 2I)\mathbf{x} = 0 :$

$\begin{pmatrix} 2 & 1 \\ 2 & 1 \end{pmatrix} \mathbf{x} = 0 \Rightarrow \mathbf{x} = \begin{pmatrix} -1 \\ 2 \end{pmatrix}$

### Step 3: Form Matrices ( P ) and ( D )

1. Construct  $P$  using the eigenvectors:

$P = \begin{pmatrix} 1 & -1 \\ 1 & 2 \end{pmatrix}$

2. Construct  D  using the eigenvalues:

$D = \begin{pmatrix} 5 & 0 \\ 0 & 2 \end{pmatrix}$

### Step 4: Verify

To verify  $A = PDP^{-1}$ , calculate  $PDP^{-1}$  and check if it equals  $A$ .

### Why Diagonalize a Matrix?

Diagonalizing a matrix simplifies matrix operations, especially:

- **Raising the matrix to a power**: If \( $A = PDP^{-1}$ \), then \( $A^k = PD^kP^{-1}$ \), where \( D^k \) is simply the diagonal matrix with each diagonal entry raised to the \( k \)-th power.
- **Solving differential equations**: In systems of linear differential equations, diagonalization can decouple equations, making solutions straightforward.
- **Analyzing transformations**: In linear algebra and physics, diagonalizing transformations can reveal invariant directions and scaling factors, aiding geometric interpretations.

Diagonalization is thus a powerful tool for simplifying complex matrix operations and gaining insights into the structure of linear transformations.

## **Diagonalizability**

Here’s a comprehensive list of key properties related to matrix diagonalization:

### 1. **Definition of Diagonalizability**

- A square matrix  $A$  of size  $n \times n$  is **diagonalizable** if there exists an invertible matrix  $P$  and a diagonal matrix  $D$  such that:

$A = PDP^{-1}$
- Here,  $P$  is a matrix whose columns are the eigenvectors of  $A$, and  $D$  is a diagonal matrix with the corresponding eigenvalues on the diagonal.

### 2. **Necessary and Sufficient Condition for Diagonalizability**

- A matrix  A  is diagonalizable if and only if it has  n  **linearly independent eigenvectors**.
- Equivalently, the **algebraic multiplicity** (the number of times an eigenvalue appears in the characteristic polynomial) of each eigenvalue must equal its **geometric multiplicity** (the number of linearly independent eigenvectors corresponding to that eigenvalue).

### 3. **Diagonalizability and Distinct Eigenvalues**

- If  A  has \( n \) **distinct eigenvalues** (i.e., no repeated eigenvalues), then \( A \) is guaranteed to be diagonalizable.
- Conversely, having repeated eigenvalues doesn’t guarantee diagonalizability; it depends on whether there are enough linearly independent eigenvectors.

### 4. **Similarity Invariance**

- Diagonalizability is invariant under similarity transformations. If \( $B = P^{-1}AP$ \) and \( A \) is diagonalizable, then \( B \) is also diagonalizable.

### 5. **Diagonalization of Symmetric (Hermitian) Matrices**

- Real symmetric matrices (or Hermitian matrices in the complex case) are always diagonalizable.
- For these matrices, all eigenvalues are real, and the eigenvectors corresponding to distinct eigenvalues are orthogonal.

### 6. **Diagonalization of Orthogonal Matrices**

- If \( A \) is an orthogonal matrix (i.e., \( $A^T A = I$ \)), then it is diagonalizable if all eigenvalues lie on the complex unit circle (i.e., have absolute value 1).

### 7. **Power of a Diagonalizable Matrix**

- For a diagonalizable matrix \( $A = PDP^{-1}$ \), the power \( $A^k$ \) can be computed easily as:
\[
$A^k = PD^kP^{-1}$
\]
- Here, \( $D^k$ \) is simply the diagonal matrix with each eigenvalue raised to the \( k \)-th power on the diagonal.

### 8. **Exponentiation of a Diagonalizable Matrix**

- The matrix exponential \( $e^{At}$ \) for a diagonalizable matrix \( $A = PDP^{-1}$ \) can be calculated as:
\[
$e^{At} = Pe^{Dt}P^{-1}$
\]
- where \( $e^{Dt}$ \) is a diagonal matrix with entries \( $e^{\lambda_i t}$ \) (where \( $\lambda_i$ \) are the eigenvalues of \( A \)) on the diagonal.

### 9. **Similarity of Powers and Diagonalization**

- If  A  is diagonalizable, then any power  $A^k$  is also diagonalizable and has the same eigenvectors as  A  with eigenvalues  $\lambda^k$ , where  $\lambda$  are the eigenvalues of  A .

### 10. **Jordan Form for Non-Diagonalizable Matrices**

- If a matrix is not diagonalizable, it can still be transformed into a Jordan canonical form, which is almost diagonal but has some \( 1 \)s on the superdiagonal (above the main diagonal) in some Jordan blocks.

### 11. **Stability Analysis in Dynamical Systems**

- In systems of differential equations, if the matrix representing the system is diagonalizable, its eigenvalues determine the system's stability, and diagonalization simplifies solving the system by decoupling equations.

### 12. **Sum and Product of Eigenvalues in Diagonalization**

- In a diagonalizable matrix \( A \), the trace of \( A \) (sum of the eigenvalues) and determinant of \( A \) (product of the eigenvalues) are preserved in the diagonal form:
\[
$\text{tr}(A) = \sum_{i=1}^n \lambda_i, \quad \det(A) = \prod_{i=1}^n \lambda_i$
\]

### 13. **Diagonalization and Matrix Functions**

- Matrix functions \( $f(A)$ \), such as \( \sin(A) \) or \( \cos(A) \), can be computed easily if \( A \) is diagonalizable, as:
\[
$f(A) = Pf(D)P^{-1}$
\]
- This method applies the function \( f \) directly to the eigenvalues in \( D \).

### 14. **Invariance of Eigenvalues in Diagonalization**

- Diagonalization preserves eigenvalues across similar matrices. If \( $A = PDP^{-1}$ \), both \( $A$ \) and \( D \) share the same eigenvalues.

### 15. **Real and Complex Diagonalization**

- A real matrix may have complex eigenvalues and thus may only be diagonalizable over the complex numbers. In such cases, we can use complex eigenvectors to diagonalize \( A \) in the complex vector space.

Diagonalization is thus a powerful tool in simplifying matrix operations and understanding matrix behavior in both theoretical and practical applications, including powers of matrices, differential equations, and system stability.

Here’s a list of properties associated with **Schur's Theorem** in the context of linear algebra:

1. **Existence of Triangular Form**:
    - Schur's Theorem states that any square matrix \( A \) can be decomposed as \( $A = QUQ^*$\), where:
        - \( Q \) is a unitary matrix (i.e., \( Q^*Q = I \), where \( Q^* \) is the conjugate transpose of \( Q \)),
        - \( U \) is an upper triangular matrix.
2. **Eigenvalues on the Diagonal**:
    - The diagonal elements of \( U \) in Schur’s decomposition are the eigenvalues of \( A \).
    - This means that the eigenvalues of \( A \) appear on the diagonal of the triangular matrix \( U \).
3. **Unitarily Similar**:
    - Schur's Theorem ensures that any matrix \( A \) is unitarily similar to an upper triangular matrix. This preserves eigenvalues and is useful for spectral analysis.
4. **Orthogonal Basis of Eigenvectors (for Normal Matrices)**:
    - For normal matrices \( A \) (i.e., \( AA^* = A^*A \)), Schur's decomposition becomes a diagonal decomposition, where \( U \) is a diagonal matrix, and \( Q \) contains an orthonormal basis of eigenvectors of \( A \).
5. **Schur Decomposition in Real Case**:
    - For real matrices, a similar decomposition called the **real Schur decomposition** can be used. It expresses \( A \) as \( A = Q T Q^T \), where \( T \) is a quasi-upper triangular matrix containing real eigenvalues or 2x2 blocks for complex-conjugate pairs.
6. **Preservation of Spectral Radius**:
    - Schur's decomposition helps in calculating the spectral radius of \( A \), as the eigenvalues are located on the diagonal of \( U \), and the largest absolute value among these eigenvalues is the spectral radius.
7. **Similarity Transformations**:
    - The unitary matrix \( Q \) in Schur’s Theorem does not change the eigenvalues, meaning eigenvalues of \( A \) and \( U \) remain the same under this transformation.
8. **Relation to QR Algorithm**:
    - Schur’s Theorem is central to the convergence properties of the QR algorithm, which iteratively reduces a matrix to upper triangular form to reveal eigenvalues.
9. **Simplicity in Matrix Powers**:
    - Schur decomposition simplifies computation of powers of \( A \), as \( A^k = Q U^k Q^* \) allows powers to be computed based on the upper triangular matrix \( U \), which is simpler than \( A \) itself.
10. **Numerical Stability**:
    - The use of unitary matrices \( Q \) in Schur decomposition makes it numerically stable, meaning it is less sensitive to rounding errors in numerical calculations.