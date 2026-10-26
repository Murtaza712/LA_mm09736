# Linear Algebra - Comprehensive Course Notes (MATH 205)
*Compiled by Muhammad Murtaza (mm09736)*

> **Primary Video Resource:** [Khan Academy - Linear Algebra: Vectors and Spaces Playlist](https://youtube.com/playlist?list=PLFD0EB975BA0CC1E0&si=iGs-3q68QXF9kTuJ)

## Table of Contents
- [1. Linear Equations & Systems](#1-linear-equations--systems)
  - [The Matrix Form ($Ax = b$)](#the-matrix-form-ax--b)
  - [The Geometry of Solutions (2D)](#the-geometry-of-solutions-2d)
- [2. Matrix Fundamentals](#2-matrix-fundamentals)
  - [What is a Matrix?](#what-is-a-matrix)
  - [Special Matrices](#special-matrices)
  - [Basic Operations & Properties](#basic-operations--properties)
- [3. Matrix Multiplication ($AB$)](#3-matrix-multiplication-ab)
  - [The Compatibility Rule](#the-compatibility-rule)
  - [Example: Row by Column Multiplication](#example-row-by-column-multiplication)
  - [Crucial Properties](#crucial-properties)
- [4. Inverses & Determinants](#4-inverses--determinants)
  - [Inverse Matrices ($A^{-1}$)](#inverse-matrices-a-1)
  - [Introduction to Determinants](#introduction-to-determinants)
- [5. Elementary Matrices & The Master Theorem](#5-elementary-matrices--the-master-theorem)
  - [Elementary Row Operations (EROs) & Elementary Matrices](#elementary-row-operations-eros--elementary-matrices)
  - [Theorem 1.5.2 (Invertibility of Elementary Matrices)](#theorem-1-5-2)
  - [Theorem 1.4.3 (RREF of a Square Matrix)](#theorem-1-4-3)
  - [Theorem 1.5.3 (Equivalent Statements / The "Master Theorem")](#theorem-1-5-3)
  - [Theorem 1.6.1 (Number of Solutions to a Linear System)](#theorem-1-6-1)
  - [Theorem 1.6.2 (Solving Linear Systems with Inverses)](#theorem-1-6-2)
  - [Theorem 1.6.4 (Equivalent Statements / Continuation of Master Theorem)](#theorem-1-6-4)
- [6. Methods for Solving Systems ($Ax = b$)](#6-methods-for-solving-systems-ax--b)
  - [Method 1: The Inverse Method (Using $[A | I]$)](#method-1-the-inverse-method-using-a--i)
  - [Method 2: Gaussian Elimination (Row-Echelon Form - REF)](#method-2-gaussian-elimination-row-echelon-form---ref)
  - [Method 3: Gauss-Jordan Elimination (Reduced Row-Echelon Form - RREF)](#method-3-gauss-jordan-elimination-reduced-row-echelon-form---rref)
  - [How Many Solutions? Three Possibilities (via RREF)](#how-many-solutions-three-possibilities-via-rref)
  - [Free Variables & Parametric Form](#free-variables--parametric-form)
- [7. LU Decomposition](#7-lu-decomposition)
  - [Conditions for LU Decomposition](#conditions-for-lu-decomposition)
  - [The Shortcut Method: Build $L$ While You Build $U$](#the-shortcut-method-build-l-while-you-build-u)
  - [How to Solve $Ax = b$ using LU Decomposition](#how-to-solve-ax--b-using-lu-decomposition)
- [8. Determinants and Their Properties](#8-determinants-and-their-properties)
  - [What is a Determinant? (A Layman's Intro)](#what-is-a-determinant-a-laymans-intro)
  - [How Row Operations (EROs) Affect Determinants](#how-row-operations-eros-affect-determinants)
  - [Theorem 2.2.4 (Determinants of Elementary Matrices)](#theorem-2-2-4)
  - [Redundancy = Zero](#redundancy--zero)
  - [The Big Trap: Addition](#the-big-trap-addition)
  - [The Multiplicative Properties](#the-multiplicative-properties)
  - [Determinants and the Master Theorem](#determinants-and-the-master-theorem)
    - [Theorem 2.3.3 (Determinant Test for Invertibility)](#theorem-2-3-3)
    - [Theorem 2.3.6 (Equivalent Statements / The Master Theorem - Expanded)](#theorem-2-3-6)
- [9. Finding Determinants using Cofactor Expansions](#9-finding-determinants-using-cofactor-expansions)
  - [Minors and Cofactors](#minors-and-cofactors)
  - [Theorem 2.1.1 (Expansions by Cofactors)](#theorem-2-1-1)
  - [Determinants of Triangular Matrices](#determinants-of-triangular-matrices)
  - [The Adjoint Matrix ($Adj(A)$)](#the-adjoint-matrix-adja)
  - [Geometric Intuition: Why the Inverse Formula Works](#geometric-intuition-why-the-inverse-formula-works)
- [10. Cramer's Rule](#10-cramers-rule)
- [11. Vectors in 2D & 3D (Refresher)](#11-vectors-in-2d--3d-refresher)
  - [Vector Basics & Length](#vector-basics--length)
  - [The Dot Product](#the-dot-product)
  - [Projections (Splitting a Vector)](#projections-splitting-a-vector)
  - [Direction Cosines](#direction-cosines)
- [12. Euclidean n-Space ($\mathbb{R}^n$)](#12-euclidean-n-space-rn)
- [13. General Vector Spaces](#13-general-vector-spaces)
  - [The 10 Axioms of a Vector Space](#the-10-axioms-of-a-vector-space)
  - [Proving vs. Disproving a Vector Space](#proving-vs-disproving-a-vector-space)
  - [Subspaces & The Subspace Test](#subspaces--the-subspace-test)
  - [Solution Space of $Ax = 0$ (Null Space)](#solution-space-of-ax--0-null-space)
  - [Linear Combinations & Span](#linear-combinations--span)
    - [Theorem 5.2.3 (Span is a Subspace)](#theorem-5-2-3)
  - [Linear Dependence & Linear Independence](#linear-dependence--linear-independence)
    - [Theorem 5.3.1 (The Redundancy Equivalence Theorem)](#theorem-5-3-1)
    - [Theorem 5.3.2 (Zero Vector and Two-Vector Dependency)](#theorem-5-3-2)
    - [Theorem 5.3.3 (More Vectors than Dimensions in $\mathbb{R}^n$)](#theorem-5-3-3)
  - [Comprehensive Worked Examples](#comprehensive-worked-examples)
  - [Basis of a Subspace](#basis-of-a-subspace)
    - [Theorem (Uniqueness of Basis Representation)](#theorem-uniqueness-basis)
  - [The Null Space of a Matrix & Finding its Basis](#the-null-space-of-a-matrix--finding-its-basis)
    - [Theorem (Null Space & Linear Independence Equivalence)](#theorem-null-independence)
  - [The Column Space of a Matrix](#the-column-space-of-a-matrix)
    - [Theorem (Solvability of $Ax = b$ via Column Space)](#theorem-column-space-consistency)
  - [Finding Bases for Null Space & Column Space (Unified Walkthrough)](#finding-bases-for-null-space--column-space-unified-walkthrough)
  - [Rank, Nullity & The Rank-Nullity Theorem](#rank-nullity--the-rank-nullity-theorem)
    - [Theorem (The Rank-Nullity Theorem / Dimension Theorem)](#theorem-rank-nullity)
- [14. Vocabulary Glossary](#14-vocabulary-glossary)

---

<div style="page-break-before: always; break-before: page;"></div>

## Index of Theorems
- [Theorem 1.4.1 (Properties of Matrix Arithmetic)](#theorem-1-4-1)
- [Theorem 1.4.2 (Properties of Zero Matrices)](#theorem-1-4-2)
- [Theorem 1.4.3 (RREF of a Square Matrix)](#theorem-1-4-3)
- [Theorem 1.4.4 (Uniqueness of Inverse)](#theorem-1-4-4)
- [Theorem 1.4.5 (The 2 x 2 Inverse Formula)](#theorem-1-4-5)
- [Theorem 1.4.6 (Inverse of a Product / The Reverse Rule)](#theorem-1-4-6)
- [Theorem 1.4.7 & 1.4.8 (Laws of Exponents for Matrices)](#theorem-1-4-7)
- [Theorem 1.4.9 (Properties of the Transpose)](#theorem-1-4-9)
- [Theorem 1.4.10 (Invertibility of a Transpose)](#theorem-1-4-10)
- [Theorem 1.5.2 (Invertibility of Elementary Matrices)](#theorem-1-5-2)
- [Theorem 1.5.3 (Equivalent Statements / The "Master Theorem")](#theorem-1-5-3)
- [Theorem 1.6.1 (Number of Solutions to a Linear System)](#theorem-1-6-1)
- [Theorem 1.6.2 (Solving Linear Systems with Inverses)](#theorem-1-6-2)
- [Theorem 1.6.3 (One-Sided Inverse Theorem)](#theorem-1-6-3)
- [Theorem 1.6.4 (Equivalent Statements / Continuation of Master Theorem)](#theorem-1-6-4)
- [Theorem 1.6.5 (Invertibility of a Product)](#theorem-1-6-5)
- [Theorem 2.1.1 (Expansions by Cofactors)](#theorem-2-1-1)
- [Theorem (Determinant of a Triangular Matrix)](#theorem-triangular-det)
- [Theorem (Cramer's Rule)](#theorem-2-1-4)
- [Theorem 2.2.4 (Determinants of Elementary Matrices)](#theorem-2-2-4)
- [Theorem 2.3.3 (Determinant Test for Invertibility)](#theorem-2-3-3)
- [Theorem 2.3.4 (Determinant of a Product)](#theorem-2-3-4)
- [Theorem 2.3.6 (Equivalent Statements / The Master Theorem - Expanded)](#theorem-2-3-6)
- [Theorem 3.3.3 (The Projection Theorem)](#theorem-3-3-3)
- [Theorem 4.1.2 (Properties of Euclidean Inner Product)](#theorem-4-1-2)
- [Theorem 4.1.3 (Cauchy-Schwarz Inequality in $\mathbb{R}^n$)](#theorem-4-1-3)
- [Theorem 4.1.4 (Properties of Length in $\mathbb{R}^n$)](#theorem-4-1-4)
- [Theorem 4.1.5 (Properties of Distance in $\mathbb{R}^n$)](#theorem-4-1-5)
- [Theorem 4.1.7 (Pythagorean Theorem in $\mathbb{R}^n$)](#theorem-4-1-7)
- [Theorem 5.2.1 (The Subspace Test)](#theorem-5-2-1)
- [Theorem 5.2.2 (Solution Space of a Homogeneous System / Null Space)](#theorem-5-2-2)
- [Theorem 5.2.3 (Span is a Subspace)](#theorem-5-2-3)
- [Theorem 5.3.1 (The Redundancy Equivalence Theorem)](#theorem-5-3-1)
- [Theorem 5.3.2 (Zero Vector and Two-Vector Dependency)](#theorem-5-3-2)
- [Theorem 5.3.3 (More Vectors than Dimensions in $\mathbb{R}^n$)](#theorem-5-3-3)
- [Theorem (Uniqueness of Basis Representation)](#theorem-uniqueness-basis)
- [Theorem (Null Space & Linear Independence Equivalence)](#theorem-null-independence)
- [Theorem (Solvability of $Ax = b$ via Column Space)](#theorem-column-space-consistency)
- [Theorem (The Rank-Nullity Theorem / Dimension Theorem)](#theorem-rank-nullity)

---

<div style="page-break-before: always; break-before: page;"></div>

## 1. Linear Equations & Systems
A **linear equation** in $n$ variables takes the form: $a_1x_1 + a_2x_2 + \dots + a_nx_n = b$.
All variables must be to the first power. No products of variables (like $xy$), and no functions of variables (like $\sqrt{x}$ or $\sin(x)$).

A **System of Linear Equations** is a set of these equations. We classify systems by their solutions:
*   **Consistent:** The system has *at least one* solution.
*   **Inconsistent:** The system has *no solution* at all.
*   **Homogeneous:** The equations all equal zero ($Ax = \mathbf{0}$). It is *always consistent* because $x = \mathbf{0}$ is always a solution (the "trivial solution").
*   **Non-Homogeneous:** The equations equal constants ($Ax = \mathbf{b}$).

### The Matrix Form ($Ax = b$)
Any system of linear equations can be rewritten cleanly into a single matrix equation $Ax = b$.
For example, given the system:
$$
\begin{cases}
2x_1 + 3x_2 = 5 \\
4x_1 - 1x_2 = 6
\end{cases}
$$

We map the components directly into matrices:
*   **$A$ (The Coefficient Matrix):** Contains all the numbers attached to the variables.
    $$A = \begin{bmatrix} 2 & 3 \\ 4 & -1 \end{bmatrix}$$
*   **$x$ (The Unknown Variable Matrix):** A column vector containing the variables we are trying to solve for.
    $$x = \begin{bmatrix} x_1 \\ x_2 \end{bmatrix}$$
*   **$b$ (The Constants Matrix):** A column vector containing the answers on the right-most part of the equation.
    $$b = \begin{bmatrix} 5 \\ 6 \end{bmatrix}$$

Putting it all together, $Ax = b$ looks exactly like this:
$$\begin{bmatrix} 2 & 3 \\ 4 & -1 \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \end{bmatrix} = \begin{bmatrix} 5 \\ 6 \end{bmatrix}$$

### The Geometry of Solutions (2D)
When analyzing a system of two variables, the equations represent lines in a 2D plane:
1.  **Intersecting Lines (Unique Solution):** The lines cross at exactly one point $(x_1, x_2)$. Consistent.
2.  **Parallel Lines (Zero Solutions):** The lines have the same slope but different intercepts. They never cross. Inconsistent.
3.  **Coincident Lines (Infinitely Many Solutions):** One equation is just a multiple of the other (e.g., $x+y=1$ and $2x+2y=2$). They represent the exact same line drawn twice. Consistent.

---

<div style="page-break-before: always; break-before: page;"></div>

## 2. Matrix Fundamentals

### What is a Matrix?
A rectangular array of numbers enclosed in brackets.
*   **Order (Size):** Always described as **Rows $\times$ Columns**. 
    *   *Example:* $\begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix}$ has $2$ rows and $3$ columns. It is a $2 \times 3$ matrix.
*   **Equality:** Two matrices are equal ($A = B$) ONLY if they have the exact same size AND corresponding entries match perfectly.
    *   *Example:* $\begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} \neq \begin{bmatrix} 1 & 2 \\ 4 & 3 \end{bmatrix}$ (entries don't match).
*   **Row/Column Vectors:** A matrix with only one column ($m \times 1$) or one row ($1 \times n$).
    *   *Example:* $\begin{bmatrix} 1 \\ 2 \\ 3 \end{bmatrix}$ is a column vector ($3 \times 1$). $\begin{bmatrix} 1 & 2 & 3 \end{bmatrix}$ is a row vector ($1 \times 3$).

### Basic Operations & Properties
*   **Addition ($A + B$):** Must be the exact same size. Add entry-wise.
    *   *Example:* $\begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} + \begin{bmatrix} 5 & 6 \\ 7 & 8 \end{bmatrix} = \begin{bmatrix} 6 & 8 \\ 10 & 12 \end{bmatrix}$
*   **Scalar Multiplication ($cA$):** Multiply every entry by $c$.
    *   *Example:* $3 \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} = \begin{bmatrix} 3 & 6 \\ 9 & 12 \end{bmatrix}$

> ### <a id="theorem-1-4-1"></a><mark>Theorem 1.4.1 (Properties of Matrix Arithmetic)</mark>
> Assuming matrix sizes permit the operations, the following familiar laws hold:
> *   **Commutative Law for Addition:** $A + B = B + A$
> *   **Associative Laws:** $A + (B + C) = (A + B) + C$  and  $A(BC) = (AB)C$
> *   **Distributive Laws:** $A(B + C) = AB + AC$ and $(B + C)A = BA + CA$

*(Note: Scalar multiplication also distributes intuitively over addition and subtraction: $a(B \pm C) = aB \pm aC$, and scalars can be pulled out of matrix multiplication: $a(BC) = (aB)C = B(aC)$).*

### Special Matrices
*   **The Zero (Null) Matrix ($O$ or $0$):** A matrix where every entry is $0$.
    *   *Example:* $O = \begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix}$

> ### <a id="theorem-1-4-2"></a><mark>Theorem 1.4.2 (Properties of Zero Matrices)</mark>
> Assuming sizes allow operations:
> *   $A + 0 = 0 + A = A$
> *   $A - A = 0$
> *   $0 - A = -A$
> *   $A0 = 0$ and $0A = 0$

*   **Diagonal Matrix:** A square matrix where every entry *off* the main diagonal is zero. 
    *   *Example:* $\begin{bmatrix} 5 & 0 \\ 0 & -2 \end{bmatrix}$
*   **The Identity Matrix ($I$):** A diagonal matrix with $1$s on the main diagonal. $diag(1, 1, \dots, 1)$. Multiplying by it changes nothing: $AI = IA = A$.
    *   *Example:* $I_3 = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$

*   **Transpose ($A^T$):** Flips rows and columns over the main diagonal.
    *   *Example:* If $A = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix}$, then $A^T = \begin{bmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{bmatrix}$

> ### <a id="theorem-1-4-9"></a><mark>Theorem 1.4.9 (Properties of the Transpose)</mark>
> Assuming sizes allow operations:
> *   **Double Transpose:** $((A)^T)^T = A$
> *   **Addition/Subtraction:** $(A \pm B)^T = A^T \pm B^T$
> *   **Scalar Multiplication:** $(kA)^T = kA^T$
> *   **Multiplication (Reverse Rule):** $(AB)^T = B^TA^T$ (The order flips, just like inverses!).
> *   **Symmetric Matrix:** $A^T = A$. (The main diagonal acts like a mirror). 
> *   *Example:* $\begin{bmatrix} 1 & 5 \\ 5 & 2 \end{bmatrix}$
> *   **Skew-Symmetric Matrix:** $A^T = -A$. 
> *   *Example:* $\begin{bmatrix} 0 & 2 \\ -2 & 0 \end{bmatrix}$

<mark style="background-color: lightgreen;">Proof</mark> **(Why the diagonal must be zero):** 
If $A^T = -A$, then for any entry on the main diagonal $a_{ii}$, the transpose entry is still $a_{ii}$. 
$$a_{ii} = -a_{ii}$$
$$2a_{ii} = 0$$
$$a_{ii} = 0$$

*   **Transpose Proofs & Tricks:**
*   <mark style="background-color: lightgreen;">Proof</mark> **of Theorem 1.4.9(d) ($(AB)^T = B^TA^T$):** 
Let's verify this for general $2 \times 2$ matrices $A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$ and $B = \begin{bmatrix} e & f \\ g & h \end{bmatrix}$.
**Left side:** 
$$AB = \begin{bmatrix} ae+bg & af+bh \\ ce+dg & cf+dh \end{bmatrix}$$
$$(AB)^T = \begin{bmatrix} ae+bg & ce+dg \\ af+bh & cf+dh \end{bmatrix}$$
**Right side:** 
$$B^T A^T = \begin{bmatrix} e & g \\ f & h \end{bmatrix} \begin{bmatrix} a & c \\ b & d \end{bmatrix} = \begin{bmatrix} ea+gb & ec+gd \\ fa+hb & fc+hd \end{bmatrix}$$
Since multiplication of normal numbers is commutative ($ea = ae$), the left and right sides are perfectly equal!

*   **Generalization ($n$ matrices):** The transpose of a product of any number of matrices is equal to the product of their transposes in reverse order:
$$(A_1 A_2 \dots A_n)^T = A_n^T \dots A_2^T A_1^T$$

*   <mark style="background-color: lightgreen;">Proof</mark> **that $A + A^T$ is symmetric:**
Take the transpose of the whole expression: 
$$(A + A^T)^T = A^T + (A^T)^T$$
$$= A^T + A$$
$$= A + A^T$$
Since it evaluates back to its original self, it is symmetric.

*   <mark style="background-color: lightgreen;">Proof</mark> **that $A - A^T$ is skew-symmetric:**
Take the transpose: 
$$(A - A^T)^T = A^T - (A^T)^T$$
$$= A^T - A$$
$$= -(A - A^T)$$
Since it evaluates to its own negative, it is skew-symmetric.

*   <mark style="background-color: lightgreen;">Proof</mark> **that $AA^T$ and $A^TA$ are symmetric:**
Take the transpose using Theorem 1.4.9(d):
$$(AA^T)^T = (A^T)^T A^T = A A^T \quad \text{(It equals itself!)}$$
$$(A^TA)^T = A^T (A^T)^T = A^T A \quad \text{(It equals itself!)}$$

---

<div style="page-break-before: always; break-before: page;"></div>

## 3. Matrix Multiplication ($AB$)

### The Compatibility Rule
You can only multiply $A \times B$ if the "inside" dimensions match. 
*   If $A$ is $(m \times \mathbf{n})$ and $B$ is $(\mathbf{n} \times p)$, they **can** be multiplied.
*   The resulting matrix will have the "outside" dimensions: $(m \times p)$.

### Example: Row by Column Multiplication
To find an entry in $AB$, take a row of $A$ and a column of $B$, multiply matching items, and sum them up (dot product).
$$A = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix}, \quad B = \begin{bmatrix} 7 & 8 \\ 9 & 1 \\ 2 & 3 \end{bmatrix}$$
$A$ is $2 \times 3$, $B$ is $3 \times 2$. The result $C = AB$ will be $2 \times 2$.
*   $C_{11} = (1 \cdot 7) + (2 \cdot 9) + (3 \cdot 2) = 7 + 18 + 6 = 31$
*   $C_{12} = (1 \cdot 8) + (2 \cdot 1) + (3 \cdot 3) = 8 + 2 + 9 = 19$
*   $C_{21} = (4 \cdot 7) + (5 \cdot 9) + (6 \cdot 2) = 28 + 45 + 12 = 85$
*   $C_{22} = (4 \cdot 8) + (5 \cdot 1) + (6 \cdot 3) = 32 + 5 + 18 = 55$
$$AB = \begin{bmatrix} 31 & 19 \\ 85 & 55 \end{bmatrix}$$

### Crucial Properties
*   **Order Matters!** Matrix multiplication is NOT commutative. **$AB \neq BA$** (in almost all cases). 
    *   <mark style="background-color: lightgreen;">Proof:</mark> **Why $(A+B)^2 \neq A^2 + B^2 + 2AB$**
        $$(A+B)^2 = (A+B)(A+B) = A(A+B) + B(A+B) = A^2 + AB + BA + B^2$$
        Because $AB$ and $BA$ are usually not equal, you cannot combine them into $2AB$. This identity only works if $A$ and $B$ commute!
*   **Associative Law:** $A(BC) = (AB)C$.
*   **Multiplying by a Diagonal Matrix:** Diagonal matrices act like a set of independent scale factors.
    *   **Left multiply ($DA$):** Scales row $i$ of $A$ by $d_i$.
        *Example:* $\begin{bmatrix} \mathbf{2} & 0 \\ 0 & \mathbf{3} \end{bmatrix} \begin{bmatrix} 1 & 1 \\ 1 & 1 \end{bmatrix} = \begin{bmatrix} \mathbf{2} & \mathbf{2} \\ \mathbf{3} & \mathbf{3} \end{bmatrix}$ (Row 1 doubled, Row 2 tripled).
    *   **Right multiply ($AE$):** Scales column $j$ of $A$ by $e_j$.
        *Example:* $\begin{bmatrix} 1 & 1 \\ 1 & 1 \end{bmatrix} \begin{bmatrix} \mathbf{2} & 0 \\ 0 & \mathbf{3} \end{bmatrix} = \begin{bmatrix} \mathbf{2} & \mathbf{3} \\ \mathbf{2} & \mathbf{3} \end{bmatrix}$ (Column 1 doubled, Column 2 tripled).
*   **The Cancellation Law Does NOT Hold:** In standard arithmetic, if $ab = ac$ and $a \neq 0$, then $b = c$. Also, if $ad = 0$, then either $a = 0$ or $d = 0$. Neither rule applies to matrices!
    *   *Example 3:* Let $A = \begin{bmatrix} 0 & 1 \\ 0 & 2 \end{bmatrix}, B = \begin{bmatrix} 1 & 1 \\ 3 & 4 \end{bmatrix}, C = \begin{bmatrix} 2 & 5 \\ 3 & 4 \end{bmatrix}, D = \begin{bmatrix} 3 & 7 \\ 0 & 0 \end{bmatrix}$.
        Notice that $AB = AC = \begin{bmatrix} 3 & 4 \\ 6 & 8 \end{bmatrix}$. Even though $A \neq 0$, we cannot "cancel" $A$ to conclude $B = C$ (since $B \neq C$).
        Furthermore, $AD = \begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix} = 0$. The product is zero, yet neither $A$ nor $D$ are zero matrices!

---

<div style="page-break-before: always; break-before: page;"></div>

## 4. Inverses & Determinants

### Inverse Matrices ($A^{-1}$)
*   **Definition:** If $Q$ and $A$ are square matrices of the same order $n$, $Q$ is an inverse of $A$ if and only if: 
    $$QA = AQ = I_n = I \iff Q = A^{-1}$$
*   **Nonsingular / Invertible:** $A$ has an inverse.
*   **Singular:** No inverse of $A$ exists.

> ### <a id="theorem-1-4-4"></a><mark>Theorem 1.4.4 (Uniqueness of Inverse)</mark>
> If $B$ and $C$ are both inverses of the matrix $A$, then $B = C$.

<mark style="background-color: lightgreen;">Proof:</mark> 
Since $B$ is an inverse of $A$, we have $BA = I$.
Multiplying both sides on the right by $C$:
$$(BA)C = IC = C$$
By the Associative Law, we can regroup the left side: $(BA)C = B(AC)$. 
Since $C$ is also an inverse of $A$, we know $AC = I$. Substituting this in gives:
$$B(AC) = B(I) = B$$
Because $(BA)C$ evaluates to $C$ (from the first step) and $B$ (from the second step), we conclude $\therefore C = B$.

> ### <a id="theorem-1-4-6"></a><mark>Theorem 1.4.6 (Inverse of a Product / The Reverse Rule)</mark>
> If $A$ and $B$ are invertible matrices of the same size, then $(AB)^{-1} = B^{-1}A^{-1}$. Notice the order flips!

<mark style="background-color: lightgreen;">Proof:</mark> To verify $B^{-1}A^{-1}$ is the true inverse of $AB$, we multiply them together to see if they simplify down to $I$:
$$(AB)(B^{-1}A^{-1}) = A(BB^{-1})A^{-1} = AIA^{-1} = AA^{-1} = I$$
$$(B^{-1}A^{-1})(AB) = B^{-1}(A^{-1}A)B = B^{-1}IB = B^{-1}B = I$$
Since both left and right multiplication result in $I$, it is proven!

*   **Generalization ($n$ matrices):** A product of any number of invertible matrices is invertible. The inverse of the product is the product of the inverses, *in reverse order*.
$$(A_1 A_2 \dots A_n)^{-1} = A_n^{-1} A_{n-1}^{-1} \dots A_2^{-1} A_1^{-1}$$

> ### <a id="theorem-1-4-7"></a><mark>Theorem 1.4.7 & 1.4.8 (Laws of Exponents for Matrices)</mark>
> If $A$ is a square matrix and $r, s$ are integers, standard exponent laws apply: $A^r A^s = A^{r+s}$ and $(A^r)^s = A^{rs}$.
> Furthermore, if $A$ is *invertible*, the following holds:
> *   **(a) The Inverse of an Inverse:** $(A^{-1})^{-1} = A$.
> *   **(b) Powers of Inverses:** $(A^n)^{-1} = (A^{-1})^n$ for $n = 0, 1, 2, \dots$
> *   **(c) Scalar Multiplication:** For any nonzero scalar $k$, $(kA)^{-1} = \frac{1}{k} A^{-1}$.

<mark style="background-color: lightgreen;">Proof</mark> **(a):** By definition, we need a matrix that multiplies with $A^{-1}$ to give $I$.
$$AA^{-1} = I \quad \text{and} \quad A^{-1}A = I$$
Since $A$ perfectly satisfies the condition to be the inverse of $A^{-1}$, then $(A^{-1})^{-1} = A$.

<mark style="background-color: lightgreen;">Proof</mark> **(b):** Let's post-multiply $A^n$ by $(A^{-1})^n$ to see if they collapse into $I$:
$$A^n (A^{-1})^n = (\underbrace{A\dots A}_{n})(\underbrace{A^{-1}\dots A^{-1}}_{n})$$
$$= A\dots A(AA^{-1})A^{-1}\dots A^{-1}$$
$$= A\dots A(I)A^{-1}\dots A^{-1} = I$$
*(The chain cascades and cancels from the inside out. The same happens for pre-multiplication, proving it is the inverse).*

> ### <a id="theorem-1-4-10"></a><mark>Theorem 1.4.10 (Invertibility of a Transpose)</mark>
> If $A$ is invertible, then its transpose $A^T$ is also invertible, and $(A^T)^{-1} = (A^{-1})^T$.

<mark style="background-color: lightgreen;">Proof:</mark> By definition, if $(A^{-1})^T$ is truly the inverse of $A^T$, then multiplying them must equal $I$.
Let's multiply them, and use the transpose property $(AB)^T = B^TA^T$ to pull the $T$ outside:
$$A^T(A^{-1})^T = (A^{-1}A)^T = I^T = I$$
$$(A^{-1})^T A^T = (AA^{-1})^T = I^T = I$$
Both equations simplify to $I$, so $(A^{-1})^T$ is indeed the inverse!

> ### <a id="theorem-1-6-3"></a><mark>Theorem 1.6.3 (One-Sided Inverse Theorem)</mark>
> Let $A$ be a square matrix. If another square matrix $B$ satisfies $BA = I$, then $B = A^{-1}$. (Similarly, if $AB = I$, then $B = A^{-1}$). This means for square matrices, you only need to check *one* side to confirm it's the true inverse!

<mark style="background-color: lightgreen;">Proof:</mark> Given $BA = I$, we can use Theorem 1.5.3 (The Master Theorem) to show $A$ is invertible. Let $x_0$ be any solution to $Ax = 0$.
Left-multiply both sides of $Ax_0 = 0$ by $B$:
$$B(Ax_0) = B(0)$$
$$(BA)x_0 = 0$$
$$Ix_0 = 0$$
$$x_0 = 0$$
Since $Ax = 0$ yields only the trivial solution $x_0 = 0$, the Master Theorem guarantees that $A$ is invertible (meaning $A^{-1}$ exists). Knowing $A^{-1}$ exists, we can post-multiply our original given equation ($BA = I$) by $A^{-1}$:
$$(BA)A^{-1} = I A^{-1}$$
$$B(AA^{-1}) = A^{-1}$$
$$B(I) = A^{-1}$$
$$B = A^{-1}$$

### Introduction to Determinants
*(Note: We will explore determinants deeply in upcoming lectures. For now, here are the absolute basics needed for inverses).*

> ### <a id="theorem-1-4-5"></a><mark>Theorem 1.4.5 (The 2 x 2 Inverse Formula)</mark>
> For a $2 \times 2$ matrix $A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$:
> *   Calculate the **Determinant**: $\det(A) = ad - bc$.
> *   If $\det(A) = 0$, the matrix is **Singular** (no inverse).
> *   If $\det(A) \neq 0$, the matrix is **Nonsingular** (invertible), and the inverse is:
> $$A^{-1} = \frac{1}{\det(A)} \begin{bmatrix} d & -b \\ -c & a \end{bmatrix}$$
> *(Swap the main diagonal entries, and flip the signs of the off-diagonal entries).*

**2. Determinant of a Diagonal Matrix**
If a matrix is diagonal, finding its determinant is incredibly easy: just multiply all the entries on the main diagonal together.
*   *Example:* If $D = \begin{bmatrix} 2 & 0 & 0 \\ 0 & -3 & 0 \\ 0 & 0 & 5 \end{bmatrix}$, then $\det(D) = (2)(-3)(5) = -30$.
*   *Trick:* Because of this, a diagonal matrix is invertible if and only if *every single entry* on its main diagonal is non-zero (otherwise the product/determinant would be 0).

---

<div style="page-break-before: always; break-before: page;"></div>

## 5. Elementary Matrices & The Master Theorem

### Elementary Row Operations (EROs) & Elementary Matrices
To solve any system, we manipulate its matrix using three "legal" moves called **EROs**:
1.  **Scaling:** Multiply a row by a nonzero constant.
2.  **Swapping:** Interchange two rows.
3.  **Replacement:** Add a multiple of one row to another.

**Elementary Matrices ($E$):** An elementary matrix is formed by applying exactly *one* ERO to the Identity Matrix $I$.
*   *The Magic Trick:* Applying an ERO to a matrix $A$ by hand produces the exact same result as left-multiplying that matrix by $E$. 
*   *Example (Swapping Rows):* Let's swap Row 1 and Row 2 of $A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$. 
    If we swap rows on the Identity matrix $I$, we get our elementary matrix $E = \begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix}$. 
    Now, watch the multiplication: $EA = \begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix} \begin{bmatrix} a & b \\ c & d \end{bmatrix} = \begin{bmatrix} c & d \\ a & b \end{bmatrix}$. The rows swapped!

> ### <a id="theorem-1-4-3"></a><mark>Theorem 1.4.3 (RREF of a Square Matrix)</mark>
> If $R$ is the reduced row-echelon form of an $n \times n$ matrix $A$, then either $R$ has a row of zeros or $R$ is the identity matrix $I_n$. 
> *(Note: If $R$ is $I_n$, $A$ is invertible. If $R$ has a row of zeros, $A$ is singular).*

> ### <a id="theorem-1-5-2"></a><mark>Theorem 1.5.2 (Invertibility of Elementary Matrices)</mark>
> Every elementary matrix is invertible, and the inverse is also an elementary matrix.

> ### <a id="theorem-1-5-3"></a><a id="theorem-153-equivalent-statements--the-master-theorem"></a><mark>Theorem 1.5.3 (Equivalent Statements / The "Master Theorem")</mark>
> If $A$ is an $n \times n$ matrix, the following statements are completely equivalent (they are all true, or all false):
> *   **(a)** $A$ is invertible.
> *   **(b)** $Ax = 0$ has only the trivial solution ($x = 0$).
> *   **(c)** The reduced row-echelon form (RREF) of $A$ is $I_n$.
> *   **(d)** $A$ is expressible as a product of elementary matrices.

<mark style="background-color: lightgreen;">Proof</mark> **(The Chain of Implications):** We prove they are equivalent by showing $(a) \implies (b) \implies (c) \implies (d) \implies (a)$.
*   **$(a) \implies (b)$:** Assume $A$ is invertible. Let $x_0$ be any solution to the equation $Ax_0 = 0$. Left-multiply both sides by $A^{-1}$:
    $$A^{-1}(Ax_0) = A^{-1}0$$
    $$(A^{-1}A)x_0 = 0$$
    $$Ix_0 = 0 \implies x_0 = 0$$
    Thus, only the trivial solution exists.
*   **$(b) \implies (c)$:** Assume $Ax = 0$ has only the trivial solution. If we write this as an augmented matrix $[A | 0]$ and row reduce it, the only solution being $x_1=0, x_2=0 \dots x_n=0$ means the final RREF equations are exactly:
    $$x_1 = 0, \quad x_2 = 0, \quad \dots \quad x_n = 0$$
    This means the RREF matrix looks like $[I_n | 0]$. If we drop the zero column, this proves the RREF of $A$ itself is exactly $I_n$.
*   **$(c) \implies (d)$:** Assume the RREF of $A$ is $I_n$. This means a sequence of elementary row operations turns $A$ into $I_n$. Let $E_1, E_2 \dots E_k$ be their corresponding elementary matrices:
    $$E_k \dots E_2 E_1 A = I_n$$
    Because every elementary matrix is invertible, we multiply both sides by their inverses to isolate $A$:
    $$A = E_1^{-1} E_2^{-1} \dots E_k^{-1} I_n$$
    $$A = E_1^{-1} E_2^{-1} \dots E_k^{-1}$$
    Since the inverse of an elementary matrix is just another elementary matrix, $A$ is successfully expressed as a product of elementary matrices!
*   **$(d) \implies (a)$:** Assume $A$ is a product of elementary matrices. Since every elementary matrix is invertible, $A$ is simply a product of invertible matrices. By Theorem 1.4.6, a product of invertible matrices is always invertible! Thus, $A$ is invertible, and the chain is complete.

> ### <a id="theorem-1-6-1"></a><mark>Theorem 1.6.1 (Number of Solutions to a Linear System)</mark>
> Every system of linear equations has no solutions, or has exactly one solution, or has infinitely many solutions.

<mark style="background-color: lightgreen;">Proof:</mark> The proof is complete if we can show that a system with more than one solution must automatically have infinitely many solutions. 
Assume $Ax = b$ has more than one solution. Let $x_1$ and $x_2$ be two *distinct* solutions.
Since they are solutions, we know:
$$Ax_1 = b \quad \text{and} \quad Ax_2 = b$$
Let's define a new vector $x_0 = x_1 - x_2$. Because $x_1$ and $x_2$ are distinct, $x_0 \neq 0$.
Now, let's multiply $A$ by $x_0$:
$$Ax_0 = A(x_1 - x_2) = Ax_1 - Ax_2 = b - b = 0$$
So, $Ax_0 = 0$.
Now, let $k$ be any arbitrary scalar constant. Let's test if a new vector $x = x_1 + k x_0$ is a solution:
$$A(x_1 + k x_0) = Ax_1 + A(k x_0)$$
$$= Ax_1 + k(Ax_0)$$
Substitute in what we know ($Ax_1 = b$ and $Ax_0 = 0$):
$$= b + k(0)$$
$$= b$$
Because $A(x_1 + k x_0) = b$, the vector $x_1 + k x_0$ is a valid solution! 
Since $k$ can be *any* real number, there are infinitely many values for $x_1 + k x_0$. Thus, the system has infinitely many solutions.

> ### <a id="theorem-1-6-2"></a><mark>Theorem 1.6.2 (Solving Linear Systems with Inverses)</mark>
> If $A$ is an invertible $n \times n$ matrix, then for each $n \times 1$ matrix $b$, the system of equations $Ax = b$ has exactly one solution, namely $x = A^{-1}b$.

<mark style="background-color: lightgreen;">Proof:</mark> Since $A(A^{-1}b) = (AA^{-1})b = Ib = b$, it follows that $x = A^{-1}b$ is a valid solution of $Ax = b$. To show that this is the *only* solution, we will assume that $x_0$ is an arbitrary solution and then show that $x_0$ must equal $A^{-1}b$.
If $x_0$ is any solution, then $Ax_0 = b$. Left-multiplying both sides by $A^{-1}$, we obtain:
$$A^{-1}(Ax_0) = A^{-1}b$$
$$(A^{-1}A)x_0 = A^{-1}b$$
$$Ix_0 = A^{-1}b$$
$$x_0 = A^{-1}b$$
This proves $x = A^{-1}b$ is the unique solution.

> ### <a id="theorem-1-6-4"></a><mark>Theorem 1.6.4 (Equivalent Statements / Continuation of Master Theorem)</mark>
> This theorem incorporates Determinants into the Master Theorem, adding statement (g). If $A$ is an $n \times n$ matrix, then the following are equivalent:
> *   **(a)** $A$ is invertible.
> *   **(b)** $Ax = 0$ has only the trivial solution.
> *   **(c)** The reduced row-echelon form of $A$ is $I_n$.
> *   **(d)** $A$ is expressible as a product of elementary matrices.
> *   **(e)** $Ax = b$ is consistent for every $n \times 1$ matrix $b$.
> *   **(f)** $Ax = b$ has exactly one solution for every $n \times 1$ matrix $b$.

<mark style="background-color: lightgreen;">Proof:</mark>
Since we proved in Theorem 1.5.3 that (a), (b), (c), and (d) are equivalent, it is sufficient to prove that $(a) \implies (f) \implies (e) \implies (a)$.
*   **$(a) \implies (f)$:** This was already proved in Theorem 1.6.2 (If $A$ is invertible, there is exactly one solution $x = A^{-1}b$).
*   **$(f) \implies (e)$:** This is self-evident. If $Ax = b$ has exactly one solution, then by definition it must be consistent.
*   **$(e) \implies (a)$:** If $Ax = b$ is consistent for every possible $b$, then in particular, the following $n$ systems are all consistent:
    $$Ax = \begin{bmatrix} 1 \\ 0 \\ \dots \\ 0 \end{bmatrix}, \quad Ax = \begin{bmatrix} 0 \\ 1 \\ \dots \\ 0 \end{bmatrix}, \quad \dots, \quad Ax = \begin{bmatrix} 0 \\ 0 \\ \dots \\ 1 \end{bmatrix}$$
    Let $x_1, x_2, \dots, x_n$ be the respective solutions of these systems. Let us form an $n \times n$ matrix $C$ using these solution vectors as its columns: $C = [x_1 | x_2 | \dots | x_n]$.
    As discussed in matrix multiplication rules (column-by-column), the successive columns of the product $AC$ will be $Ax_1, Ax_2, \dots, Ax_n$. Thus:
    $$AC = [Ax_1 | Ax_2 | \dots | Ax_n] = \begin{bmatrix} 1 & 0 & \dots & 0 \\ 0 & 1 & \dots & 0 \\ \dots & \dots & \dots & \dots \\ 0 & 0 & \dots & 1 \end{bmatrix} = I$$
    By Theorem 1.6.3 (One-Sided Inverse), since $AC = I$, it follows that $C = A^{-1}$. Thus, $A$ is invertible!

> ### <a id="theorem-1-6-5"></a><mark>Theorem 1.6.5 (Invertibility of a Product)</mark>
> Let $A$ and $B$ be square matrices of the same size. If $AB$ is invertible, then $A$ and $B$ must also be invertible.

<mark style="background-color: lightgreen;">Proof:</mark> Since $AB$ is invertible, it has an inverse, let's call it $C$. By the definition of an inverse, multiplying $AB$ by $C$ yields the identity matrix $I$:
$$(AB)C = I \quad \text{and} \quad C(AB) = I$$
Using the associative property of matrix multiplication, we can regroup these equations:
$$A(BC) = I \quad \text{and} \quad (CA)B = I$$
By **Theorem 1.6.3 (One-Sided Inverse Theorem)**, if a square matrix can be multiplied by another matrix to yield $I$, then it is invertible.
*   Since $A(BC) = I$, the matrix $BC$ acts as the inverse of $A$. Thus, $A$ is invertible.
*   Since $(CA)B = I$, the matrix $CA$ acts as the inverse of $B$. Thus, $B$ is invertible.
Therefore, both $A$ and $B$ must be invertible.

---

<div style="page-break-before: always; break-before: page;"></div>

## 6. Methods for Solving Systems ($Ax = b$)
There are three primary methods for solving systems, each with a specific use case:

### Method 1: The Inverse Method (Using $[A | I]$)
**Best for:** Solving *many* different systems that all share the exact same coefficient matrix $A$, but have different answers $b$. Once you find $A^{-1}$, you can just compute $x = A^{-1}b$ repeatedly.
1.  Setup the augmented matrix: **$[A | I]$**
2.  Apply EROs until the left side perfectly matches the Identity Matrix.
3.  The result on the right is your inverse: **$[I | A^{-1}]$**.

**Worked Example:** Find the inverse of $A = \begin{bmatrix} 2 & 4 \\ 1 & 3 \end{bmatrix}$.
*   **Step 1 (Setup):** $\begin{bmatrix} 2 & 4 & | & 1 & 0 \\ 1 & 3 & | & 0 & 1 \end{bmatrix}$
*   **Step 2 (Swap R1 & R2 to get a leading 1):** $\begin{bmatrix} 1 & 3 & | & 0 & 1 \\ 2 & 4 & | & 1 & 0 \end{bmatrix}$
*   **Step 3 ($R_2 \leftarrow R_2 - 2R_1$):** $\begin{bmatrix} 1 & 3 & | & 0 & 1 \\ 0 & -2 & | & 1 & -2 \end{bmatrix}$
*   **Step 4 ($R_2 \leftarrow R_2 \div -2$):** $\begin{bmatrix} 1 & 3 & | & 0 & 1 \\ 0 & 1 & | & -0.5 & 1 \end{bmatrix}$
*   **Step 5 ($R_1 \leftarrow R_1 - 3R_2$):** $\begin{bmatrix} 1 & 0 & | & 1.5 & -2 \\ 0 & 1 & | & -0.5 & 1 \end{bmatrix}$
*   **Result:** $A^{-1} = \begin{bmatrix} 1.5 & -2 \\ -0.5 & 1 \end{bmatrix}$.

<mark style="background-color: lightgreen;">Proof:</mark> **Why does this method work?**
Suppose $\theta_1, \theta_2, \dots, \theta_k$ are the EROs that turn an invertible matrix $A$ into $I$, with corresponding elementary matrices $E_1, E_2, \dots, E_k$.
Applying them one after another to $A$:
$$\theta_k \dots \theta_2 \theta_1 (A) = E_k \dots E_2 E_1 A = I$$
Writing $P$ for the product of all those elementary matrices, we get the seed equation:
$$PA = I \quad \text{where} \quad P = E_k \dots E_2 E_1$$
Since $A$ is invertible, multiply both sides of $PA = I$ on the right by $A^{-1}$:
$$PAA^{-1} = IA^{-1}$$
$$PI = A^{-1}$$
$$P = A^{-1}$$
This proves that $P$ (the exact same chain of row operations applied to the Identity matrix) equals the inverse! That's why $[A | I]$ becomes $[I | A^{-1}]$.

### Method 2: Gaussian Elimination (Row-Echelon Form - REF)
**Best for:** Solving a *single* system quickly by hand. 
You set up an augmented matrix $[A | b]$ and use EROs to create a "staircase" pattern known as **Row-Echelon Form (REF)**.
*   **The Rules of REF:**
    1.  Rows of all zeros must be at the very bottom.
    2.  The first non-zero number in a row must be a `1` (called a "leading 1").
    3.  Each leading `1` must be further to the right than the leading `1` in the row above it.
*   *Example of REF:* 
    $$\begin{bmatrix} \mathbf{1} & 2 & 3 & | & 9 \\ 0 & \mathbf{1} & 4 & | & 5 \\ 0 & 0 & \mathbf{1} & | & 2 \end{bmatrix}$$
*   **Next step:** Stop here, convert back to equations (e.g., the bottom row means $1z = 2$), and use **back-substitution** to find the rest of the variables.
    *   **Worked Example (Back-Substitution):**
        Using the REF matrix above:
        *   Row 3: $z = 2$
        *   Row 2: $y + 4z = 5 \implies y + 4(2) = 5 \implies y = -3$
        *   Row 1: $x + 2y + 3z = 9 \implies x + 2(-3) + 3(2) = 9 \implies x = 9$
        *   **Solution:** $(9, -3, 2)$

### Method 3: Gauss-Jordan Elimination (Reduced Row-Echelon Form - RREF)
**Best for:** Solving a *single* system completely so the matrix hands you the answers directly, with zero algebra required at the end.
You take your REF matrix one step further into **Reduced Row-Echelon Form (RREF)**.
*   **The Rules of RREF:**
    1.  It must meet all the rules of REF (the staircase of leading 1s).
    2.  **Crucial Addition:** Each leading `1` (pivot) must be the *only* non-zero number in its entire column. You must create zeros both ABOVE and BELOW every pivot.
*   **Worked Example (Continuing from REF to RREF):** 
    Let's take the REF matrix from Method 2 and turn it into RREF by clearing the numbers *above* the pivots.
    *   *Start (REF):* $\begin{bmatrix} 1 & 2 & 3 & | & 9 \\ 0 & 1 & 4 & | & 5 \\ 0 & 0 & 1 & | & 2 \end{bmatrix}$
    *   *Step 1 (Clear above $z$-pivot: $R_2 \leftarrow R_2 - 4R_3$ and $R_1 \leftarrow R_1 - 3R_3$):* $\begin{bmatrix} 1 & 2 & 0 & | & 3 \\ 0 & 1 & 0 & | & -3 \\ 0 & 0 & 1 & | & 2 \end{bmatrix}$
    *   *Step 2 (Clear above $y$-pivot: $R_1 \leftarrow R_1 - 2R_2$):* $\begin{bmatrix} 1 & 0 & 0 & | & 9 \\ 0 & 1 & 0 & | & -3 \\ 0 & 0 & 1 & | & 2 \end{bmatrix}$
    *   *Result:* The matrix is in RREF. The solution is exactly $(9, -3, 2)$ without doing any algebra on paper!

### How Many Solutions? Three Possibilities (via RREF)
A **Pivot** is the leading `1` in a row in RREF. By looking at the pivot columns in an augmented matrix $[A | b]$, you can instantly determine which of the exactly 3 possibilities holds:

**1. Unique Solution:** Every non-augmented column is a pivot column.
*Example:* 
$$\begin{bmatrix} 1 & 0 & 0 & | & a \\ 0 & 1 & 0 & | & b \\ 0 & 0 & 1 & | & c \end{bmatrix} \implies \begin{cases} x = a \\ y = b \\ z = c \end{cases}$$

**2. Infinitely Many Solutions:** The last column is not a pivot, AND at least one other column is not a pivot column (i.e. there is at least 1 free variable). 
*Example:*
$$\begin{bmatrix} 1 & -2 & 0 & 3 & | & 1 \\ 0 & 0 & 1 & 4 & | & -1 \end{bmatrix}$$
(Columns 2 and 4 lack pivots, so they are free variables).

**3. No Solution:** The last (augmented) column is a pivot column.
*Example:*
$$\begin{bmatrix} 1 & 0 & 0 & | & 0 \\ 0 & 1 & 0 & | & 0 \\ 0 & 0 & 0 & | & 1 \end{bmatrix} \implies 0 = 1$$

---

### Free Variables & Parametric Form
*   **Definition:** A variable $x_i$ is a free variable if its column, in a row-echelon form of the matrix, is not a pivot column.

**Recipe: Parametric Form**
1.  Write the system as an augmented matrix.
2.  Row reduce to reduced row-echelon form (RREF).
3.  Write the corresponding system of equations.
4.  Move all free variables to the right-hand side.

*Example (translating RREF to parametric form):*
Given the RREF matrix: $\begin{bmatrix} 1 & 0 & 5 & | & 1 \\ 0 & 1 & 2 & | & -1 \end{bmatrix}$
*   **Step 3 (Equations):** $\begin{cases} x + 5z = 1 \\ y + 2z = -1 \end{cases}$
*   **Step 4 (Move free variable $z$ to right):** $\begin{cases} x = 1 - 5z \\ y = -1 - 2z \\ z = z \quad \text{(any real number)} \end{cases}$

---

<div style="page-break-before: always; break-before: page;"></div>

## 7. LU Decomposition
LU Decomposition is essentially the matrix form of Gaussian Elimination. It is a method of taking a square matrix $A$ and factoring it into two separate matrices:
$$A = LU$$
*   **$L$ (Lower Triangular):** A lower triangular matrix with $1$s down the main diagonal. This matrix acts as a "memory bank" that records all the row operations you performed.
*   **$U$ (Upper Triangular):** An upper triangular matrix. This is exactly the Row-Echelon Form of matrix $A$. 

**The Advantage:**
If you need to solve $Ax = b$ for several *different* target vectors ($b$), standard Gaussian Elimination forces you to augment the matrix $[A | b]$ and do all the row operations from scratch every single time the $b$ changes. 
By decomposing $A$ into $L$ and $U$ once, you can reuse them to instantly solve for any future $b$ vectors without ever needing to recalculate the row operations.

### Conditions for LU Decomposition
Plain LU decomposition is only possible under one strict condition:
*   **No Row Swaps Allowed:** You must be able to reduce $A$ to Row-Echelon form ($U$) *without ever interchanging any rows*. If you hit a $0$ pivot and are forced to swap rows to keep going, plain LU decomposition fails for that matrix.

### The Shortcut Method: Build $L$ While You Build $U$
You do not need a separate pass to find $L$. You can pull it out "for free" while you perform Gaussian Elimination to find $U$.

1.  **Reduce $A$ to $U$:** Use standard Gaussian Elimination, but remember the golden rule: *no row swaps allowed*.
2.  **Use Only Row Additions:** To eliminate an entry below the pivot, always use an operation in the form: $R_i \rightarrow R_i - m_{ij}R_j$.
3.  **Drop into $L$:** Every time you perform that operation to kill an entry, take the multiplier you used ($m_{ij}$) and drop it directly into matrix $L$ at the exact same position $(i, j)$.
    *   *(Shortcut logic: Just drop the **opposite** of whatever you added to the row into the $L$ matrix).*
4.  **Finish $L$:** Place $1$s down the entire main diagonal of $L$, and $0$s everywhere above the diagonal. 

**Worked Example:**
Let $A = \begin{bmatrix} 1 & 4 & -3 \\ -2 & 8 & 5 \\ 3 & 4 & 7 \end{bmatrix}$. We will reduce it to $U$ and build $L$ simultaneously.

*   **Op 1:** Clear the $-2$ in position $(2,1)$. 
    *   Operation: $R_2 \rightarrow R_2 + 2R_1$. 
    *   The opposite of $+2$ is **$-2$**. Drop $-2$ into $L_{21}$.
*   **Op 2:** Clear the $3$ in position $(3,1)$.
    *   Operation: $R_3 \rightarrow R_3 - 3R_1$.
    *   The opposite of $-3$ is **$+3$**. Drop $+3$ into $L_{31}$.
*   **Op 3:** Clear the remaining number below the diagonal in position $(3,2)$.
    *   Operation: $R_3 \rightarrow R_3 + \frac{1}{2}R_2$.
    *   The opposite of $+\frac{1}{2}$ is **$-\frac{1}{2}$**. Drop $-0.5$ into $L_{32}$.

Your $U$ matrix is the result of those operations:
$$U = \begin{bmatrix} 1 & 4 & -3 \\ 0 & 16 & -1 \\ 0 & 0 & 15.5 \end{bmatrix}$$

Your $L$ matrix is built from the opposites, with $1$s on the diagonal:
$$L = \begin{bmatrix} 1 & 0 & 0 \\ \mathbf{-2} & 1 & 0 \\ \mathbf{3} & \mathbf{-0.5} & 1 \end{bmatrix}$$

### How to Solve $Ax = b$ using LU Decomposition
Once you have factored $A$ into $L$ and $U$, you solve the system in two incredibly fast steps using a "middleman" vector called $y$. 
Since $A = LU$, the equation $Ax = b$ becomes $LUx = b$. We group $Ux$ together and define it as $y$ (so $Ux = y$). This leaves us with $Ly = b$.

*   **Step 1: Solve $Ly = b$ (Forward Substitution)**
    Because $L$ is a lower triangular matrix, the very first equation only has one variable! You instantly find $y_1$, plug it into the second equation to find $y_2$, and work your way *downwards* to find the entire vector $y$.
*   **Step 2: Solve $Ux = y$ (Backward Substitution)**
    Now take your newly found $y$ vector and set it equal to $Ux$. Because $U$ is an upper triangular matrix (Row-Echelon form), the very last equation only has one variable. You instantly find $x_n$, and work your way *upwards* to find the entire vector $x$, which is your final answer!

*(The beauty of this method is that neither step requires row reduction—they just require simple algebraic substitution!)*

---

<div style="page-break-before: always; break-before: page;"></div>

## 8. Determinants and Their Properties

### What is a Determinant? (A Layman's Intro)
Every square matrix acts as a mathematical transformation that can stretch or shrink space. The **determinant**, denoted as $\det(A)$ or $|A|$, is a single scalar number that summarizes exactly how much that matrix scales things. 

*   If $\det(A) = 2$, the matrix doubles the area/volume of whatever it transforms.
*   If $\det(A) = 0$, the matrix completely crushes space flat (which is why a matrix with a determinant of zero has no inverse—you cannot mathematically "un-crush" a flat object!).

**Calculating a $2 \times 2$ Determinant:**
For a $2 \times 2$ matrix, finding this scaling factor is straightforward. We cross-multiply the diagonals and subtract them:
$$A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$$
$$\det(A) = ad - bc$$
*(Example: For $\begin{bmatrix} 3 & 2 \\ 1 & 4 \end{bmatrix}$, the determinant is $(3)(4) - (2)(1) = 12 - 2 = 10$.)*

While calculating the determinant of a $2 \times 2$ matrix is simple, expanding larger matrices by hand using brute-force formulas gets highly tedious. Instead, we use an algebraic toolkit of properties that allow us to evaluate and manipulate determinants efficiently.

### How Row Operations (EROs) Affect Determinants
Applying an Elementary Row Operation changes the determinant in specific, predictable ways:

1.  **Adding Rows (Replacement):** Adding a multiple of one row/col to another leaves the determinant **unchanged**.
    *   $R_i \rightarrow R_i + kR_j \implies \text{No Change}$
    *   *Proof ($2 \times 2$ case for $C_1 \rightarrow C_1 + C_2$):* 
    $$\begin{vmatrix} a + b & b \\ c + d & d \end{vmatrix} = (a+b)d - b(c+d) = ad + bd - bc - bd = ad - bc$$
    *(The extra terms always cancel out!)*
2.  **Swapping Rows:** Interchanging two rows/cols **flips the sign** of the determinant.
    *   $R_i \leftrightarrow R_j \implies \text{Multiplies } \det \text{ by } -1$
3.  **Scaling a Row:** Multiplying a single row/col by a scalar $k$ scales the determinant by $k$.
    *   $R_i \rightarrow kR_i \implies \text{Multiplies } \det \text{ by } k$
    *   *Proof ($2 \times 2$ case, factoring $k$ out of the first column):*
    $$\begin{vmatrix} ka & b \\ kc & d \end{vmatrix} = (ka)d - b(kc) = k(ad - bc) = k\det(A)$$
    *   *Warning:* Scaling the *entire* $n \times n$ matrix $A$ scales the determinant by $k^n$, so $\det(kA) = k^n \det(A)$.

> ### <a id="theorem-2-2-4"></a><mark>Theorem 2.2.4 (Determinants of Elementary Matrices)</mark>
> This theorem directly links the ERO determinant properties to Elementary Matrices ($E$). Since an elementary matrix is formed by applying exactly one ERO to the Identity Matrix $I_n$, and we know $\det(I_n) = 1$, we can determine $\det(E)$ instantly:
> *   **(a)** If $E$ results from multiplying a row of $I_n$ by $k$, then $\det(E) = k \cdot \det(I_n) = k$.
> *   **(b)** If $E$ results from interchanging two rows of $I_n$, then $\det(E) = -1 \cdot \det(I_n) = -1$.
> *   **(c)** If $E$ results from adding a multiple of one row of $I_n$ to another, then $\det(E) = 1 \cdot \det(I_n) = 1$.
>
> 
### Redundancy = Zero
If a matrix has structural redundancy, it represents a "collapsed" system that cannot be inverted. Thus, its determinant is instantly $0$. You do not need to do any math if you spot:

1.  **Zero Row/Col:** A matrix with a row or column of all zeros has $\det(A) = 0$.
    *   *Proof ($2 \times 2$ case):* $\begin{vmatrix} a & 0 \\ b & 0 \end{vmatrix} = \begin{vmatrix} a & b \\ 0 & 0 \end{vmatrix} = 0$
2.  **Identical Rows/Cols:** A matrix with two completely identical rows or columns has $\det(A) = 0$.
    *   *Proof ($2 \times 2$ case with identical columns):* $\begin{vmatrix} a & a \\ b & b \end{vmatrix} = ab - ab = 0$
3.  **Proportional Rows/Cols:** A matrix where one row/col is a scalar multiple of another has $\det(A) = 0$.
    *   *Example:* Column 2 is exactly twice column 3:
    $$\det \begin{bmatrix} -2 & 8 & 4 \\ 3 & 2 & 1 \\ 1 & 10 & 5 \end{bmatrix} = 0 \quad (C_2 = 2C_3)$$
    *(Once you spot a proportional pair, you already know the answer is zero—no need to expand anything).*

### The Big Trap: Addition
Determinants are **NOT** additive. 
$$\det(A + B) \neq \det(A) + \det(B)$$
*   *Counterexample:* Let $A = \begin{bmatrix} 1 & 2 \\ 2 & 5 \end{bmatrix}$ and $B = \begin{bmatrix} 3 & 1 \\ 1 & 3 \end{bmatrix}$. Then $A+B = \begin{bmatrix} 4 & 3 \\ 3 & 8 \end{bmatrix}$.
    $$\det(A) = 1, \quad \det(B) = 8, \quad \det(A+B) = 23$$
    $$\det(A) + \det(B) = 9 \neq 23$$

**The Addition Rule (The One Case Where It Does Add):**
If matrices $A$, $B$, and $C$ differ in only **one row** (say row $i$), and row $i$ of $C$ equals $(\text{row } i \text{ of } A) + (\text{row } i \text{ of } B)$, then the determinant is additive in that row *alone*.
*   *Example:*
    $$\begin{vmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \end{vmatrix} + \begin{vmatrix} a_{11} & a_{12} \\ b_{21} & b_{22} \end{vmatrix} = \begin{vmatrix} a_{11} & a_{12} \\ a_{21} + b_{21} & a_{22} + b_{22} \end{vmatrix}$$

### The Multiplicative Properties
Determinants behave very predictably under standard matrix algebra operations:
1.  **Products:** $\det(AB) = \det(A)\det(B)$ (for same-size square matrices, see Theorem 2.3.4 below).
2.  **Identity:** $\det(I) = 1$ (for an identity matrix of any size).
3.  **Inverses:** $\det(A^{-1}) = \frac{1}{\det(A)}$. *(This proves mathematically why $\det(A)$ cannot be $0$ for an invertible matrix!).*
4.  **Transposes:** $\det(A^T) = \det(A)$. *(Rows and columns are completely interchangeable when calculating a determinant).*
    *   *Proof ($2 \times 2$ case):* Transposing just swaps the off-diagonal entries, which the formula treats symmetrically. 
    $$A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}, \quad A^T = \begin{bmatrix} a & c \\ b & d \end{bmatrix}$$
    $$\det(A) = ad - bc$$
    $$\det(A^T) = ad - cb = ad - bc$$

> ### <a id="theorem-2-3-4"></a><mark>Theorem 2.3.4 (Determinant of a Product)</mark>
> If $A$ and $B$ are square matrices of the same size, then:
> $$\det(AB) = \det(A) \det(B)$$

<mark style="background-color: lightgreen;">Proof</mark> **(Two Cases):**
*   **Case 1 (Suppose $A$ is not invertible):**
    If $A$ is not invertible, then $\det(A) = 0$.
    By Theorem 1.6.5, if $AB$ is invertible, then $A$ and $B$ must be invertible. Therefore, if $A$ is not invertible, the product $AB$ is also not invertible.
    Therefore, $\det(AB) = 0$.
    Substituting into the formula: $\det(AB) = \det(A)\det(B) \implies 0 = 0 \cdot \det(B) \implies 0 = 0$. (QED for Case 1).
*   **Case 2 (Suppose $A$ is invertible):**
    By the Master Theorem, an invertible matrix $A$ is expressible as a product of elementary matrices:
    $$A = E_1 E_2 \dots E_r \quad \text{--- (1)}$$
    Now, let's take the determinant of $AB$:
    $$\det(AB) = \det(E_1 E_2 \dots E_r B)$$
    Using the property that $\det(EB) = \det(E)\det(B)$ for elementary matrices:
    $$\det(AB) = \det(E_1) \det(E_2) \dots \det(E_r) \det(B)$$
    $$\det(AB) = \det(E_1 E_2 \dots E_r) \det(B)$$
    Substitute $A$ back in using (1):
    $$\det(AB) = \det(A)\det(B)$$

### Determinants and the Master Theorem

> ### <a id="theorem-2-3-3"></a><mark>Theorem 2.3.3 (Determinant Test for Invertibility)</mark>
> A square matrix $A$ is invertible if and only if $\det(A) \neq 0$.

*   <mark style="background-color: lightgreen;">Proof:</mark> Let $R$ be the reduced row-echelon form of $A$. We can express $R$ as the product of elementary matrices applied to $A$:
    $$R = E_r \dots E_2 E_1 A$$
    Taking the determinant of both sides (using the multiplication property):
    $$\det(R) = \det(E_r) \dots \det(E_2) \det(E_1) \det(A)$$
    By Theorem 2.2.4, the determinants of elementary matrices are always non-zero. Therefore, $\det(R)$ will be zero if and only if $\det(A)$ is zero.
    *   **If $A$ is invertible:** The Master Theorem states $R = I_n$. Since $\det(I_n) = 1 \neq 0$, then $\det(R) \neq 0$, which forces $\det(A) \neq 0$.
    *   **If $\det(A) \neq 0$:** This forces $\det(R) \neq 0$. Because $\det(R)$ is not zero, $R$ cannot contain a row of zeros. By Theorem 1.4.3, an RREF matrix without a zero row must be the identity matrix $I_n$. If $R = I_n$, the Master Theorem states $A$ is invertible.

> ### <a id="theorem-2-3-6"></a><mark>Theorem 2.3.6 (Equivalent Statements / The Master Theorem - Expanded)</mark>
> This theorem incorporates Determinants into the Master Theorem, adding statement (g). If $A$ is an $n \times n$ matrix, then the following are equivalent:
> *   **(a)** $A$ is invertible.
> *   **(b)** $Ax = 0$ has only the trivial solution.
> *   **(c)** The reduced row-echelon form of $A$ is $I_n$.
> *   **(d)** $A$ is expressible as a product of elementary matrices.
> *   **(e)** $Ax = b$ is consistent for every $n \times 1$ matrix $b$.
> *   **(f)** $Ax = b$ has exactly one solution for every $n \times 1$ matrix $b$.
> *   **(g)** $\det(A) \neq 0$.

---

<div style="page-break-before: always; break-before: page;"></div>

## 9. Finding Determinants using Cofactor Expansions

To calculate the determinant of a large $n \times n$ matrix, we can recursively break it down into smaller $(n-1) \times (n-1)$ matrices.

### Minors and Cofactors
Before we can calculate a full determinant, we need to understand its building blocks: Minors and Cofactors.

<mark>Definition (Minors and Cofactors):</mark>
If $A$ is a square matrix, then the **minor of entry $a_{ij}$** is denoted by $M_{ij}$ and is defined to be the determinant of the submatrix that remains after the $i$-th row and $j$-th column are deleted from $A$. 
The number $(-1)^{i+j} M_{ij}$ is denoted by $C_{ij}$ and is called the **cofactor of entry $a_{ij}$**.

*   **The Relationship:** The cofactor and the minor differ only in sign: $C_{ij} = \pm M_{ij}$.
*   **The Checkerboard Trick:** A quick way to determine whether to use $+$ or $-$ is to use the "checkerboard" array pattern of signs. You start with a $+$ in the top left and alternate:
    $$\begin{bmatrix} + & - & + & - & \dots \\ - & + & - & + & \dots \\ + & - & + & - & \dots \\ \dots & \dots & \dots & \dots & \dots \end{bmatrix}$$
    *(Example: The entry $a_{11}$ gets a $+$ (since $(-1)^{1+1} = +1$), so $C_{11} = M_{11}$. The entry $a_{32}$ gets a $-$ (since $(-1)^{3+2} = -1$), so $C_{32} = -M_{32}$.)*

**Worked Example:** Finding Minors and Cofactors
Let $A = \begin{bmatrix} 3 & 1 & -4 \\ 2 & 5 & 6 \\ 1 & 4 & 8 \end{bmatrix}$.

1.  **Finding $M_{11}$ and $C_{11}$:**
    Cross out Row 1 and Column 1. The remaining submatrix is $\begin{bmatrix} 5 & 6 \\ 4 & 8 \end{bmatrix}$.
    $$M_{11} = \det \begin{bmatrix} 5 & 6 \\ 4 & 8 \end{bmatrix} = (5)(8) - (6)(4) = 40 - 24 = 16$$
    Since $(1, 1)$ is a $+$ on the checkerboard, $C_{11} = M_{11} = 16$.

2.  **Finding $M_{32}$ and $C_{32}$:**
    Cross out Row 3 and Column 2. The remaining submatrix is $\begin{bmatrix} 3 & -4 \\ 2 & 6 \end{bmatrix}$.
    $$M_{32} = \det \begin{bmatrix} 3 & -4 \\ 2 & 6 \end{bmatrix} = (3)(6) - (-4)(2) = 18 + 8 = 26$$
    Since $(3, 2)$ is a $-$ on the checkerboard, $C_{32} = -M_{32} = -26$.

> ### <a id="theorem-2-1-1"></a><mark>Theorem 2.1.1 (Expansions by Cofactors)</mark>
> The determinant of an $n \times n$ matrix $A$ can be computed by multiplying the entries in **any** row (or column) by their cofactors and adding the resulting products. 
> *   **Expansion along the $i$-th row:**
>     $$\det(A) = a_{i1}C_{i1} + a_{i2}C_{i2} + \dots + a_{in}C_{in}$$
> *   **Expansion along the $j$-th column:**
>     $$\det(A) = a_{1j}C_{1j} + a_{2j}C_{2j} + \dots + a_{nj}C_{nj}$$
>
> 
**Strategy: "Smart Choice" of Row or Column**
Because the theorem guarantees that *any* row or column will yield the correct determinant, you should always choose the row or column containing the **most zeros**. 
Since $0 \times C_{ij} = 0$, hunting for zeros allows you to entirely skip calculating massive sub-determinants, drastically pruning the recursive calculation tree.

**Worked Example:** Smart Choice on a $4 \times 4$ Matrix
Let $A = \begin{bmatrix} 1 & 0 & 0 & -1 \\ 3 & 1 & 2 & 2 \\ 1 & 0 & -2 & 1 \\ 2 & 0 & 0 & 1 \end{bmatrix}$.

1.  **Step 1:** Look for the most zeros. Column 2 is almost entirely zeros (`0, 1, 0, 0`). We expand along Column 2:
    $$\det(A) = (0 \cdot C_{12}) + (1 \cdot C_{22}) + (0 \cdot C_{32}) + (0 \cdot C_{42})$$
    Because of the zeros, the problem collapses instantly to just $1 \cdot C_{22}$.
    *   The entry is $1$.
    *   The sign for position $(2,2)$ is $+$ (since $(-1)^{2+2} = +1$).
    *   Cross out Row 2 and Column 2 to get the $3 \times 3$ minor.
    $$\det(A) = +1 \begin{vmatrix} 1 & 0 & -1 \\ 1 & -2 & 1 \\ 2 & 0 & 1 \end{vmatrix}$$
2.  **Step 2:** We now have a $3 \times 3$ matrix. Hunt for zeros again! Column 2 is `0, -2, 0`. Expand along this new Column 2.
    *   The only non-zero entry is $-2$.
    *   The sign for position $(2,2)$ in a $3 \times 3$ matrix is $+$ (since $(-1)^{2+2} = +1$).
    *   Cross out Row 2 and Column 2 to get the $2 \times 2$ minor.
    $$\det(A) = +1 \cdot \left( +(-2) \begin{vmatrix} 1 & -1 \\ 2 & 1 \end{vmatrix} \right) = -2 \begin{vmatrix} 1 & -1 \\ 2 & 1 \end{vmatrix}$$
3.  **Step 3:** Evaluate the final $2 \times 2$ determinant using $ad - bc$.
    $$\det \begin{bmatrix} 1 & -1 \\ 2 & 1 \end{bmatrix} = (1)(1) - (-1)(2) = 1 + 2 = 3$$
    Multiply by the scalar we pulled out:
    $$\det(A) = -2 \cdot 3 = -6$$
*(By hunting for zeros, we solved a $4 \times 4$ matrix by calculating only a single $2 \times 2$ determinant, completely avoiding the dozens of sub-determinants we would have otherwise had to compute!)*

### Determinants of Triangular Matrices
A square matrix with a solid block of zeros on one side of the main diagonal is called a **triangular matrix**. There are two types:
*   **Lower Triangular:** All entries *above* the main diagonal are zero. 
*   **Upper Triangular:** All entries *below* the main diagonal are zero. (Note: Every matrix in Row-Echelon Form is upper triangular since it naturally has zeros below the pivots!)
*   *(Note: Diagonal matrices, like the Identity matrix $I$, are both upper and lower triangular at the same time).*

Finding the determinant of any triangular matrix is remarkably simple:

> ### <a id="theorem-triangular-det"></a><mark>Theorem (Determinant of a Triangular Matrix)</mark>
> $$\det(\text{triangular matrix}) = \text{product of its diagonal entries}$$
> 
> <mark style="background-color: lightgreen;">Proof (Why?):</mark> This shortcut is a direct consequence of Theorem 2.1.1 (Cofactor Expansions). If you have a lower triangular matrix and you expand along the very first row, every single entry in that row is $0$ *except* for the first diagonal entry $a_{11}$. As you continue the recursive expansion down the matrix, you keep getting $0$s for every branch except the diagonal branch. The only surviving term at the end of the chain is $a_{11} \times a_{22} \times \dots \times a_{nn}$.

### The Adjoint Matrix ($Adj(A)$)

<mark>Definition (Matrix of Cofactors & Adjoint):</mark>
If $A$ is any $n \times n$ matrix and $C_{ij}$ is the cofactor of $a_{ij}$, then the matrix formed by all these cofactors is called the **matrix of cofactors from $A$**:
$$\begin{bmatrix} C_{11} & C_{12} & \dots & C_{1n} \\ C_{21} & C_{22} & \dots & C_{2n} \\ \vdots & \vdots & \ddots & \vdots \\ C_{n1} & C_{n2} & \dots & C_{nn} \end{bmatrix}$$
The transpose of this matrix is called the **adjoint of $A$** and is denoted by $\text{adj}(A)$.

**Property of Cofactor Expansions:**
As we know, multiplying the entries of a row by their *own* cofactors gives the determinant. However, if one multiplies the entries in any row by the corresponding cofactors from a **different** row, the sum of these products is **always zero**. 

The generalized formula for the inverse of any square matrix $A$ is:
$$A^{-1} = \frac{1}{\det(A)} \text{adj}(A)$$
*(Recall from Section 4 that for a $2 \times 2$ matrix, $\text{adj}(A)$ is just swapping the main diagonal and flipping the signs of the off-diagonal: $\begin{bmatrix} d & -b \\ -c & a \end{bmatrix}$).*

**Worked Example:** Adjoint of a $3 \times 3$ Matrix
Let $A = \begin{bmatrix} 3 & 2 & -1 \\ 1 & 6 & 3 \\ 2 & -4 & 0 \end{bmatrix}$. 
If you calculate all 9 cofactors (using the $C_{ij} = (-1)^{i+j} M_{ij}$ formula and the checkerboard signs), you get the matrix of cofactors. Transposing that matrix yields:
$$\text{adj}(A) = \begin{bmatrix} 12 & 4 & 12 \\ 6 & 2 & -10 \\ -16 & 16 & 16 \end{bmatrix}$$

### Geometric Intuition: Why the Inverse Formula Works
To truly understand the formula $A^{-1} = \frac{1}{\det(A)}\text{adj}(A)$, we must view a matrix geometrically as an **action**, rather than algebraically as a shelf of numbers.

A square matrix acts as a transformation that grabs points on a grid and moves them. The columns of the matrix dictate exactly where the original $X$-axis and $Y$-axis land.
When a matrix transforms space, it can do three things:
1.  **Stretch/Squish** (Changing the area/volume).
2.  **Rotate** (Spinning the grid).
3.  **Skew** (Tilting the axes so they are no longer perpendicular).

**The Reversal Machine ($A^{-1}$)**
To find the inverse, we must perfectly reverse all three of these actions. The formula splits this into two elegant jobs:
*   **The Un-Stretching:** The determinant ($\det(A)$) tells us exactly how much the original matrix multiplied the area of the grid. If $\det(A) = 3$, the area tripled. To reverse this, we must shrink everything back down by $3$. This is why the formula scales the matrix by multiplying by $\frac{1}{\det(A)}$.
*   **The Un-Skewing & Un-Rotating:** The Adjoint ($\text{adj}(A)$) is built directly out of the "footprints" (the cofactors) of where the axes originally landed. By using these coordinates to map a path backward, the Adjoint inherently restores the axes back to their perfect, un-rotated $90^\circ$ orientation. 

$$A^{-1} = [\text{Un-stretch the Area}] \times [\text{Un-rotate and Un-skew}]$$
$$A^{-1} = \left[ \frac{1}{\det(A)} \right] \text{adj}(A)$$

*(Note: If a matrix crushes the 2D grid completely flat into a 1D line, the area becomes $0$. Because thousands of points get smashed together into the same line, the transformation cannot be reversed. This perfectly explains why a matrix with $\det(A) = 0$ has no inverse!)*

---

<div style="page-break-before: always; break-before: page;"></div>

## 10. Cramer's Rule
Cramer's Rule is a method for solving a system of linear equations using *only determinants*, completely bypassing Row Reduction (RREF) or calculating the full inverse matrix. It is extremely useful when you only need to solve for one specific variable in a system.

> ### <a id="theorem-2-1-4"></a><mark>Theorem (Cramer's Rule)</mark>
> If $Ax = b$ is a system of $n$ linear equations in $n$ unknowns such that $\det(A) \neq 0$, then the system has a unique solution. This solution is:
> $$x_1 = \frac{\det(A_1)}{\det(A)}, \quad x_2 = \frac{\det(A_2)}{\det(A)}, \quad \dots, \quad x_n = \frac{\det(A_n)}{\det(A)}$$
> where $A_j$ is the matrix obtained by replacing the entries in the $j$-th column of $A$ by the entries in the answer matrix $b$.

> [!NOTE] Not Part of Syllabus
> The following proof is not required for the exam, but it is an extremely elegant mathematical trick that is highly interesting to look at.

<mark style="background-color: lightgreen;">Proof:</mark> The mathematical proof of Cramer's Rule relies on a brilliant "Trojan Horse" trick using properties of determinants and the identity matrix.

**Step 1: The Setup**
Consider the system $Ax = B$. If $A$ is invertible (meaning $\det(A) \neq 0$), we know the unique solution is:
$$x = A^{-1}B$$
We also know that $A^{-1}A = I_n$. If we break the identity matrix into its column vectors $[e_1 | e_2 | \dots | e_n]$, we can write:
$$A^{-1}[c_1 | c_2 | \dots | c_n] = [e_1 | e_2 | \dots | e_n]$$
This means that for any column $k$, $A^{-1}c_k = e_k$.

**Step 2: The "Trojan Horse" Matrix ($D_k$)**
We construct a new matrix called $D_k$. This matrix is identical to the Identity matrix $I_n$, except we replace the $k$-th column with our solution vector $x$:
$$D_k = \begin{bmatrix} 1 & 0 & \dots & x_1 & \dots & 0 \\ 0 & 1 & \dots & x_2 & \dots & 0 \\ \vdots & \vdots & \ddots & \vdots & & \vdots \\ 0 & 0 & \dots & x_n & \dots & 1 \end{bmatrix}$$
If we calculate the determinant of $D_k$ by expanding along the $k$-th row, every entry is $0$ except for $x_k$, and its minor is simply $I_{n-1}$. Therefore:
$$\det(D_k) = x_k \quad \text{--- (Equation 1)}$$

**Step 3: Factoring out $A^{-1}$**
Let's rewrite the columns of $D_k$ using our knowledge from Step 1 ($e_k = A^{-1}c_k$) and our solution equation ($x = A^{-1}B$):
$$D_k = [A^{-1}c_1 | \dots | A^{-1}c_{k-1} | A^{-1}B | A^{-1}c_{k+1} | \dots | A^{-1}c_n]$$
We can factor out the $A^{-1}$ matrix from every column:
$$D_k = A^{-1} [c_1 | \dots | c_{k-1} | B | c_{k+1} | \dots | c_n]$$

**Step 4: The Reveal**
Look closely at the matrix left inside the brackets. It is exactly the original matrix $A$, but with the $k$-th column replaced by the answer vector $B$. By definition, this is exactly the matrix $A_k$ from Cramer's Rule!
Therefore:
$$D_k = A^{-1}A_k$$

**Step 5: The Final Determinant**
Take the determinant of both sides using the multiplicative property ($\det(AB) = \det(A)\det(B)$):
$$\det(D_k) = \det(A^{-1}A_k)$$
$$\det(D_k) = \det(A^{-1})\det(A_k)$$
Since $\det(A^{-1}) = \frac{1}{\det(A)}$, this becomes:
$$\det(D_k) = \frac{\det(A_k)}{\det(A)} \quad \text{--- (Equation 2)}$$

By combining Equation 1 ($\det(D_k) = x_k$) and Equation 2, we arrive at Cramer's Rule:
$$x_k = \frac{\det(A_k)}{\det(A)}$$

---

<div style="page-break-before: always; break-before: page;"></div>

## 11. Vectors in 2D & 3D (Refresher)
This section serves as a refresher on vector geometry from Calculus II, establishing the toolkit needed before defining formal Vector Spaces.

### Vector Basics & Length
*   **What is a Vector?** A quantity completely determined by magnitude (length) and direction. It is represented geometrically as a directed line segment (an arrow).
*   **Scalars ($k$):** A scalar is just a regular, everyday real number (like $5$, $-2$, or $0.5$). Its only job is to *scale* a vector. 
    *   *Note on Absolute Value:* The formula $|k| = -k$ if $k < 0$ is just a mathematical instruction for "flip the sign to make it positive." When you multiply a vector $\vec{v}$ by a negative scalar (e.g., $k = -2$), the negative sign flips the arrow's direction $180^\circ$, and the absolute value $|-2| = 2$ tells you to stretch its length by $2$.
*   **The Norm (Length):** The length of a vector $\vec{v} = \langle x, y, z \rangle$ is denoted by double bars $||\vec{v}||$ and is a direct 3D generalization of the Pythagorean theorem:
    $$||\vec{v}|| = \sqrt{x^2 + y^2 + z^2}$$
*   **Unit Vectors:** A vector with a length of exactly $1$ ($||\vec{v}|| = 1$). The standard unit vectors along the 3D axes are $\hat{i} = \langle 1, 0, 0 \rangle$, $\hat{j} = \langle 0, 1, 0 \rangle$, and $\hat{k} = \langle 0, 0, 1 \rangle$.

### The Dot Product
The dot product (or Euclidean inner product) multiplies two vectors together to produce a **single scalar number** (not a vector). It encodes both length and the angle between the vectors.
*   **Geometric Definition:**
    $$\vec{u} \cdot \vec{v} = ||\vec{u}|| \, ||\vec{v}|| \cos(\theta)$$
*   **Algebraic (Component) Formula:**
    $$\vec{u} \cdot \vec{v} = u_1v_1 + u_2v_2 + u_3v_3$$
*   **Dot Product with Itself:**
    $$\vec{u} \cdot \vec{u} = ||\vec{u}||^2$$
*   **Orthogonality (Perpendicularity):** Two vectors are orthogonal (perpendicular) if and only if the angle between them is $90^\circ$. Because $\cos(90^\circ) = 0$, their dot product evaluates exactly to zero:
    $$\vec{u} \cdot \vec{v} = 0 \iff \vec{u} \perp \vec{v}$$

### Projections (Splitting a Vector)
Often, we need to decompose a vector $\vec{u}$ into two perpendicular pieces: one pointing along a chosen direction $\vec{a}$, and one pointing perfectly perpendicular to $\vec{a}$. 

> ### <a id="theorem-3-3-3"></a><mark>Theorem 3.3.3 (The Projection Theorem)</mark>
> If $\vec{u}$ and $\vec{a}$ are vectors and $\vec{a} \neq \mathbf{0}$, then $\vec{u}$ can be expressed in exactly one way as:
> $$\vec{u} = \vec{w}_1 + \vec{w}_2$$
> Where $\vec{w}_1$ is a scalar multiple of $\vec{a}$ (the projection), and $\vec{w}_2$ is orthogonal to $\vec{a}$. 
> $$\vec{w}_1 = \text{proj}_{\vec{a}} \vec{u} = \frac{\vec{u} \cdot \vec{a}}{||\vec{a}||^2} \vec{a}$$

**Intuition Behind the Formula:**
Think of calculating an $x$-component in 2D physics using $||\vec{u}||\cos(\theta)$. The projection theorem is just the 3D "universal" version of that, allowing you to tilt your axis to any random vector $\vec{a}$.
1.  **The Length (The Shadow):** Using the geometric dot product formula, we can isolate $||\vec{u}||\cos(\theta)$ to find the exact length of the shadow $\vec{u}$ casts onto $\vec{a}$: 
    $$||\vec{u}|| \cos(\theta) = \frac{\vec{u} \cdot \vec{a}}{||\vec{a}||}$$
2.  **The Direction:** To force our scalar length to point in the correct direction without changing its size, we multiply it by the unit vector of $\vec{a}$, which is $\frac{\vec{a}}{||\vec{a}||}$.
3.  **The Result:** Multiplying the Length by the Direction gives:
    $$\left( \frac{\vec{u} \cdot \vec{a}}{||\vec{a}||} \right) \left( \frac{\vec{a}}{||\vec{a}||} \right) = \left( \frac{\vec{u} \cdot \vec{a}}{||\vec{a}||^2} \right) \vec{a}$$

**The Orthogonal Component ($\vec{w}_2$):**
In 2D physics, finding the vertical component is easy ($||\vec{u}||\sin(\theta)$) because there is only one "up" direction. In 3D space, there is a full $360^\circ$ disk of directions perpendicular to $\vec{a}$. To bypass nightmare 3D trigonometry, we use a simple vector addition shortcut.
Since walking along the shadow ($\vec{w}_1$) and then straight up the vertical piece ($\vec{w}_2$) gets you to the exact same destination as the original vector ($\vec{u}$), we know $\vec{w}_1 + \vec{w}_2 = \vec{u}$. 
By rearranging this algebraically, we get the orthogonal component instantly:
$$\vec{w}_2 = \vec{u} - \text{proj}_{\vec{a}} \vec{u}$$

### Direction Cosines
To perfectly describe a 3D direction without a full spherical coordinate system, we measure the angles the vector makes with the three axes: $\alpha$ (with the x-axis), $\beta$ (with the y-axis), and $\gamma$ (with the z-axis).
Using basic right-triangle trigonometry ($SOH CAH TOA$), the cosines of these angles are exactly the vector's coordinates divided by its total length (the hypotenuse):
$$\cos\alpha = \frac{x}{||\vec{v}||}, \quad \cos\beta = \frac{y}{||\vec{v}||}, \quad \cos\gamma = \frac{z}{||\vec{v}||}$$

*   **The Magic Identity:** Because of the 3D Pythagorean theorem ($x^2 + y^2 + z^2 = ||\vec{v}||^2$), squaring and adding these three cosines will always equal exactly $1$:
    $$\cos^2\alpha + \cos^2\beta + \cos^2\gamma = 1$$
*   **The Takeaway:** The vector formed by these cosines $\langle \cos\alpha, \cos\beta, \cos\gamma \rangle$ is simply the **Unit Vector** pointing in the exact same direction as $\vec{v}$.

---

<div style="page-break-before: always; break-before: page;"></div>

## 12. Euclidean n-Space ($\mathbb{R}^n$)
While 2D and 3D vectors map perfectly to physical space, mathematics allows us to generalize vectors to any number of dimensions ($n$). 

*   **n-tuples:** If $n$ is a positive integer, an **ordered n-tuple** is a sequence of $n$ real numbers $(x_1, x_2, \dots, x_n)$. 
*   **$\mathbb{R}^n$ (n-space):** The set of all such n-tuples is called $n$-space, denoted by $\mathbb{R}^n$.

Vectors in $\mathbb{R}^n$ behave exactly identically to 2D and 3D vectors. Addition, scalar multiplication, and even geometric concepts like length and angles all still apply.

### The Euclidean Inner Product (Dot Product)
The dot product scales up infinitely. In $\mathbb{R}^n$, it is called the **Euclidean Inner Product**.
If $\vec{u} = \langle u_1, u_2, \dots, u_n \rangle$ and $\vec{v} = \langle v_1, v_2, \dots, v_n \rangle$, then:
$$\vec{u} \cdot \vec{v} = u_1v_1 + u_2v_2 + \dots + u_nv_n$$

> ### <a id="theorem-4-1-2"></a><mark>Theorem 4.1.2 (Properties of Euclidean Inner Product)</mark>
> If $\vec{u}, \vec{v}, \vec{w}$ are vectors in $\mathbb{R}^n$ and $k$ is a scalar:
> *   **(a) Symmetry:** $\vec{u} \cdot \vec{v} = \vec{v} \cdot \vec{u}$
> *   **(b) Distributivity:** $(\vec{u} + \vec{v}) \cdot \vec{w} = \vec{u} \cdot \vec{w} + \vec{v} \cdot \vec{w}$
> *   **(c) Homogeneity:** $(k\vec{u}) \cdot \vec{v} = k(\vec{u} \cdot \vec{v})$
> *   **(d) Positivity:** $\vec{v} \cdot \vec{v} \ge 0$, and $\vec{v} \cdot \vec{v} = 0 \iff \vec{v} = \mathbf{0}$

> ### <a id="theorem-4-1-3"></a><mark>Theorem 4.1.3 (Cauchy-Schwarz Inequality in $\mathbb{R}^n$)</mark>
> The absolute value of a dot product can never exceed the product of the vectors' lengths.
> $$|\vec{u} \cdot \vec{v}| \le ||\vec{u}|| \, ||\vec{v}||$$

### Norm and Distance in $\mathbb{R}^n$
The Pythagorean theorem and the distance formula scale up directly by adding more terms under the square root.

*   **Euclidean Norm (Length):** $||\vec{u}|| = \sqrt{u_1^2 + u_2^2 + \dots + u_n^2}$
*   **Euclidean Distance:** $d(\vec{u}, \vec{v}) = ||\vec{u} - \vec{v}|| = \sqrt{(u_1 - v_1)^2 + \dots + (u_n - v_n)^2}$

> ### <a id="theorem-4-1-4"></a><mark>Theorem 4.1.4 (Properties of Length in $\mathbb{R}^n$)</mark>
> *   **(a)** $||\vec{u}|| \ge 0$
> *   **(b)** $||\vec{u}|| = 0 \iff \vec{u} = \mathbf{0}$
> *   **(c)** $||k\vec{u}|| = |k| \, ||\vec{u}||$
> *   **(d) Triangle Inequality:** $||\vec{u} + \vec{v}|| \le ||\vec{u}|| + ||\vec{v}||$

<mark style="background-color: lightgreen;">Proof</mark> **(c) (Scaling Length):**
$$||k\vec{u}|| = \sqrt{(ku_1)^2 + (ku_2)^2 + \dots + (ku_n)^2}$$
$$= \sqrt{k^2 (u_1^2 + u_2^2 + \dots + u_n^2)}$$
$$= |k| \sqrt{u_1^2 + u_2^2 + \dots + u_n^2} = |k| \, ||\vec{u}||$$

<mark style="background-color: lightgreen;">Proof</mark> **(d) (Triangle Inequality):**
We start with the golden rule that squared length equals the dot product with itself:
$$||\vec{u} + \vec{v}||^2 = (\vec{u} + \vec{v}) \cdot (\vec{u} + \vec{v})$$
$$= ||\vec{u}||^2 + 2(\vec{u} \cdot \vec{v}) + ||\vec{v}||^2$$
Since any number is $\le$ its absolute value, we replace the middle term:
$$\le ||\vec{u}||^2 + 2|\vec{u} \cdot \vec{v}| + ||\vec{v}||^2$$
Apply the Cauchy-Schwarz Inequality ($|\vec{u} \cdot \vec{v}| \le ||\vec{u}|| \, ||\vec{v}||$):
$$\le ||\vec{u}||^2 + 2||\vec{u}||\,||\vec{v}|| + ||\vec{v}||^2$$
Factor the perfect square:
$$\le (||\vec{u}|| + ||\vec{v}||)^2$$
Taking the square root of both sides yields $||\vec{u} + \vec{v}|| \le ||\vec{u}|| + ||\vec{v}||$.

> ### <a id="theorem-4-1-5"></a><mark>Theorem 4.1.5 (Properties of Distance in $\mathbb{R}^n$)</mark>
> Distance shares similar logical rules to length.
> *   **(a)** $d(\vec{u}, \vec{v}) \ge 0$
> *   **(b)** $d(\vec{u}, \vec{v}) = 0 \iff \vec{u} = \vec{v}$
> *   **(c) Symmetry:** $d(\vec{u}, \vec{v}) = d(\vec{v}, \vec{u})$
> *   **(d) Triangle Inequality:** $d(\vec{u}, \vec{v}) \le d(\vec{u}, \vec{w}) + d(\vec{w}, \vec{v})$ (Taking a detour through $\vec{w}$ is always longer or equal to going straight).

### Orthogonality & The Pythagorean Theorem
Even in hyperspace, we can determine if two vectors are perfectly perpendicular. 
**Definition:** Two vectors $\vec{u}$ and $\vec{v}$ in $\mathbb{R}^n$ are **orthogonal** if $\vec{u} \cdot \vec{v} = 0$.

> ### <a id="theorem-4-1-7"></a><mark>Theorem 4.1.7 (Pythagorean Theorem in $\mathbb{R}^n$)</mark>
> If $\vec{u}$ and $\vec{v}$ are orthogonal vectors, then:
> $$||\vec{u} + \vec{v}||^2 = ||\vec{u}||^2 + ||\vec{v}||^2$$

<mark style="background-color: lightgreen;">Proof</mark> **:**
$$||\vec{u} + \vec{v}||^2 = (\vec{u} + \vec{v}) \cdot (\vec{u} + \vec{v})$$
$$= ||\vec{u}||^2 + 2(\vec{u} \cdot \vec{v}) + ||\vec{v}||^2$$
Since the vectors are orthogonal, $\vec{u} \cdot \vec{v} = 0$. The middle term vanishes.
$$= ||\vec{u}||^2 + 0 + ||\vec{v}||^2 = ||\vec{u}||^2 + ||\vec{v}||^2$$

---

<div style="page-break-before: always; break-before: page;"></div>

## 13. General Vector Spaces
We now shift to a much broader definition of vectors: **"Vector" is a job title.**
If a set of objects (which could be matrices, functions, polynomials, or arrows) has a sensible "addition" and "scalar multiplication" that behave exactly as we expect them to, we call that set a **Vector Space**, and we refer to its elements as **vectors**.

### The 10 Axioms of a Vector Space
Let $V$ be a set of objects. $V$ is a vector space if all 10 of these axioms hold for all vectors $\vec{u}, \vec{v}, \vec{w}$ in $V$ and all scalars $k, l$:

**The "Vegas" Rules (Closure):**
1.  **Closure under Addition:** $\vec{u} + \vec{v}$ is in $V$.
6.  **Closure under Scalar Multiplication:** $k\vec{u}$ is in $V$.
*(If operations pull you outside the set, it is not a vector space).*

**The "Undo" Rules (Identities):**
4.  **Zero Vector:** There is a $\mathbf{0}$ in $V$ such that $\vec{u} + \mathbf{0} = \vec{u}$. *(This implies a vector space is never empty).*
5.  **Negative Vector:** Every $\vec{u}$ has an inverse $-\vec{u}$ such that $\vec{u} + (-\vec{u}) = \mathbf{0}$.

**The Arithmetic Rules:**
2.  **Commutative:** $\vec{u} + \vec{v} = \vec{v} + \vec{u}$
3.  **Associative (Addition):** $\vec{u} + (\vec{v} + \vec{w}) = (\vec{u} + \vec{v}) + \vec{w}$
7.  **Distributive (Scalar over Vector Add):** $k(\vec{u} + \vec{v}) = k\vec{u} + k\vec{v}$
8.  **Distributive (Scalar Add over Vector):** $(k + l)\vec{u} = k\vec{u} + l\vec{u}$
9.  **Associative (Scalar Multiplication):** $k(l\vec{u}) = (kl)\vec{u}$
10. **Scalar Identity:** $1\vec{u} = \vec{u}$

### Proving vs. Disproving a Vector Space
*   **To Prove:** You must systematically show that all 10 axioms hold true. (Most fall out directly from real-number arithmetic applied entrywise, like showing all $2 \times 2$ matrices form a vector space).
*   **To Disprove:** You only need to find **one** axiom that fails. 
    *   *Tip:* Always check Axiom 1 (Closure under addition) and Axiom 6 (Closure under scalar multiplication) first. They kill more failed candidates than any other axiom.

### Subspaces & The Subspace Test
> **Video Resource:** [Khan Academy - Linear Subspaces of $\mathbb{R}^n$](https://youtu.be/pMFv6liWK4M?si=vUzhx0MK-GSeuwX9)

A **subspace** $W$ of a vector space $V$ is a subset of $V$ that is *itself* a vector space under the addition and scalar multiplication defined on $V$.

Rather than testing all 10 axioms to verify if a subset is a subspace, we use a powerful shortcut: since $W$ lives inside an already verified vector space $V$, it automatically inherits properties like commutativity and associativity. We only need to check **three conditions**:

> ### <a id="theorem-5-2-1"></a><mark>Theorem 5.2.1 (The Subspace Test)</mark>
> A subset $V$ of $\mathbb{R}^n$ is a **linear subspace** if and only if it satisfies all three conditions:
> *   **(a) Contains the Zero Vector:** The zero vector $\mathbf{0}$ of $\mathbb{R}^n$ is in $V$.
> *   **(b) Closure under Scalar Multiplication:** For any vector $\mathbf{x} \in V$ and any scalar $c \in \mathbb{R}$, the product $c\mathbf{x}$ is also in $V$.
> *   **(c) Closure under Addition:** For any vectors $\mathbf{a}, \mathbf{b} \in V$, their sum $\mathbf{a} + \mathbf{b}$ is also in $V$.

*(Pro-tip: Always check condition (a) first! If $\mathbf{0} \notin V$, the candidate fails instantly and is NOT a subspace).*

#### Video Examples & Analysis:
*   **Example 1: The Zero Vector Subspace ($\{\mathbf{0}\}$):**
    A set containing *only* the zero vector in $\mathbb{R}^3$ (or $\mathbb{R}^n$) is a valid subspace:
    *   $\mathbf{0} \in \{\mathbf{0}\}$ (Contains zero).
    *   $c \cdot \mathbf{0} = \mathbf{0} \in \{\mathbf{0}\}$ (Closed under scalar multiplication).
    *   $\mathbf{0} + \mathbf{0} = \mathbf{0} \in \{\mathbf{0}\}$ (Closed under addition).
*   **Example 2: The Half-Plane (Counterexample):**
    Let $S$ be the set of vectors in $\mathbb{R}^2$ where the first coordinate is non-negative: $S = \left\{\begin{bmatrix} x_1 \\ x_2 \end{bmatrix} \in \mathbb{R}^2 \;\middle|\; x_1 \ge 0\right\}$.
    *   Contains $\mathbf{0} = \begin{bmatrix}0\\0\end{bmatrix}$ because $0 \ge 0$.
    *   Closed under addition: If $a_1 \ge 0$ and $b_1 \ge 0$, then $a_1 + b_1 \ge 0$.
    *   **FAILS Closure under Scalar Multiplication:** Take $\mathbf{x} = \begin{bmatrix} 2 \\ 3 \end{bmatrix} \in S$ and scalar $c = -1$.
        $$c\mathbf{x} = -1\begin{bmatrix} 2 \\ 3 \end{bmatrix} = \begin{bmatrix} -2 \\ -3 \end{bmatrix}$$
        Here, the first coordinate $-2 < 0$, which falls outside $S$. Thus, $S$ is **NOT a subspace**!
*   **Example 3: Span of a Single Vector (Line through Origin):**
    The span of $\mathbf{v} = \begin{bmatrix} 1 \\ 1 \end{bmatrix}$ in $\mathbb{R}^2$:
    $$\text{span}\left(\left\{\begin{bmatrix} 1 \\ 1 \end{bmatrix}\right\}\right) = \left\{ c\begin{bmatrix} 1 \\ 1 \end{bmatrix} = \begin{bmatrix} c \\ c \end{bmatrix} \;\middle|\; c \in \mathbb{R} \right\}$$
    Geometrically, this forms the line $y = x$ passing through the origin. Any two points on this line added together stay on the line, and scaling any point stays on the line. Hence, it is a valid 1D subspace of $\mathbb{R}^2$.
    *(Note: Any line that does NOT pass through the origin, e.g. $y = x + 1$, fails Rule 1 because it does not contain $\mathbf{0}$, so it can never be a subspace).*
*   **Example 4: Span of Any Set of Vectors:**
    The span of *any* set of vectors $\{\mathbf{v}_1, \dots, \mathbf{v}_k\}$ is **100% guaranteed to be a valid subspace** (proven in Theorem 5.2.3 below).

---

### Solution Space of $Ax = 0$ (Null Space)

> ### <a id="theorem-5-2-2"></a><mark>Theorem 5.2.2 (Solution Space of a Homogeneous System)</mark>
> If $Ax = \mathbf{0}$ is a homogeneous linear system of $m$ equations in $n$ unknowns, then the set of solution vectors is a subspace of $\mathbb{R}^n$.

<mark style="background-color: lightgreen;">Proof:</mark>
Let $W$ be the set of all solution vectors to the homogeneous system $Ax = \mathbf{0}$. To prove $W$ is a subspace of $\mathbb{R}^n$, we verify the three conditions of Theorem 5.2.1 (The Subspace Test):

1.  **Non-empty / Contains the Zero Vector:**
    The zero vector $\mathbf{0} \in \mathbb{R}^n$ is always a solution because:
    $$A\mathbf{0} = \mathbf{0}$$
    (the trivial solution always exists). Thus, $\mathbf{0} \in W$, meaning $W$ is not empty.

2.  **Closure under Addition:**
    Let $\mathbf{x}$ and $\mathbf{x}'$ be any two solution vectors in $W$. Since they are solutions, by definition:
    $$A\mathbf{x} = \mathbf{0} \quad \text{and} \quad A\mathbf{x}' = \mathbf{0}$$
    Now, test their sum $\mathbf{x} + \mathbf{x}'$ by multiplying by $A$:
    $$A(\mathbf{x} + \mathbf{x}') = A\mathbf{x} + A\mathbf{x}' = \mathbf{0} + \mathbf{0} = \mathbf{0}$$
    Since $A(\mathbf{x} + \mathbf{x}') = \mathbf{0}$, the vector $\mathbf{x} + \mathbf{x}'$ is also a valid solution. Thus, $W$ is closed under addition.

3.  **Closure under Scalar Multiplication:**
    Let $\mathbf{x}$ be any solution vector in $W$ (so $A\mathbf{x} = \mathbf{0}$) and let $k$ be any real scalar. Test the scaled vector $k\mathbf{x}$ by multiplying by $A$:
    $$A(k\mathbf{x}) = k(A\mathbf{x}) = k(\mathbf{0}) = \mathbf{0}$$
    Since $A(k\mathbf{x}) = \mathbf{0}$, the vector $k\mathbf{x}$ is also a valid solution. Thus, $W$ is closed under scalar multiplication.

Because all three conditions of Theorem 5.2.1 are satisfied, the solution set $W$ is officially a **subspace of $\mathbb{R}^n$**.

> [!WARNING] Common Exam Trap: Non-Homogeneous Systems ($Ax = b$)
> If $\mathbf{b} \neq \mathbf{0}$, the solution set to $Ax = \mathbf{b}$ is **NEVER a subspace**. 
> *   **Zero Vector Fails:** $A\mathbf{0} = \mathbf{0} \neq \mathbf{b}$ (zero is never a solution).
> *   **Closure Fails:** If $A\mathbf{x} = \mathbf{b}$ and $A\mathbf{x}' = \mathbf{b}$, then $A(\mathbf{x} + \mathbf{x}') = A\mathbf{x} + A\mathbf{x}' = \mathbf{b} + \mathbf{b} = 2\mathbf{b} \neq \mathbf{b}$.

---

### Linear Combinations & Span
> **Video Resource:** [Khan Academy - Linear Combinations and Span](https://youtu.be/Qm_OS-8COwU?si=RmmDgK9z6id4qWOC)

#### 1. Linear Combinations
Let $V$ be a vector space. A vector $\mathbf{w}$ in $V$ is called a **linear combination** of the vectors $\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_k$ in $V$ if $\mathbf{w}$ can be expressed in the form:
$$\mathbf{w} = c_1 \mathbf{v}_1 + c_2 \mathbf{v}_2 + \dots + c_k \mathbf{v}_k$$
where $c_1, c_2, \dots, c_k$ are arbitrary scalars (called the *weights* or *coefficients*).

*   *Example in $\mathbb{R}^2$:* 
    Let $\mathbf{v}_1 = \begin{bmatrix} 1 \\ 2 \end{bmatrix}$ and $\mathbf{v}_2 = \begin{bmatrix} 0 \\ 3 \end{bmatrix}$. 
    If we pick scalars $c_1 = 3$ and $c_2 = -1$, the linear combination is:
    $$\mathbf{w} = 3\begin{bmatrix} 1 \\ 2 \end{bmatrix} + (-1)\begin{bmatrix} 0 \\ 3 \end{bmatrix} = \begin{bmatrix} 3 \\ 6 \end{bmatrix} + \begin{bmatrix} 0 \\ -3 \end{bmatrix} = \begin{bmatrix} 3 \\ 3 \end{bmatrix}$$
    Therefore, $\begin{bmatrix} 3 \\ 3 \end{bmatrix}$ is a valid linear combination of $\mathbf{v}_1$ and $\mathbf{v}_2$.

#### 2. The Span of a Set of Vectors
If $S = \{\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_k\}$ is a non-empty set of vectors in a vector space $V$, then the **span** of $S$, denoted by $\text{span}(S)$ or $\text{span}\{\mathbf{v}_1, \dots, \mathbf{v}_k\}$, is defined to be the set of **all possible linear combinations** of the vectors in $S$:
$$\text{span}(S) = \{c_1 \mathbf{v}_1 + c_2 \mathbf{v}_2 + \dots + c_k \mathbf{v}_k \mid c_1, c_2, \dots, c_k \in \mathbb{R}\}$$

*   **Spanning a Vector Space:** If every vector in $V$ can be expressed as a linear combination of vectors in $S$, then we say that $S$ **spans $V$**, or that $\text{span}(S) = V$. In this case, $S$ is called a **spanning set** for $V$.

**Geometric Visualization of Span:**
*   **Zero Vector alone:** $\text{span}\{\mathbf{0}\} = \{\mathbf{0}\}$ (a single point at the origin).
*   **One non-zero vector:** $\text{span}\{\mathbf{v}\}$ is a **1D line** passing through the origin in the direction of $\mathbf{v}$.
*   **Two non-collinear vectors:** $\text{span}\{\mathbf{v}_1, \mathbf{v}_2\}$ is a **2D flat plane** passing through the origin.
*   **Three non-coplanar vectors:** $\text{span}\{\mathbf{v}_1, \mathbf{v}_2, \mathbf{v}_3\}$ fills out an entire **3D volume** passing through the origin.

> ### <a id="theorem-5-2-3"></a><mark>Theorem 5.2.3 (Span is a Subspace)</mark>
> If $S = \{\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_k\}$ is a set of vectors in a vector space $V$, then:
> *   **(a)** The set $W = \text{span}(S)$ is a subspace of $V$.
> *   **(b)** $W$ is the *smallest* subspace of $V$ that contains $S$, in the sense that any other subspace of $V$ that contains $S$ must automatically contain $W$.

<mark style="background-color: lightgreen;">Proof (a):</mark>
To prove that $W = \text{span}(S)$ is a subspace of $V$, we verify the three conditions of Theorem 5.2.1 (The Subspace Test):
1.  **Contains the Zero Vector ($\mathbf{0} \in W$):**
    By setting all scalar coefficients to zero ($c_1 = c_2 = \dots = c_k = 0$), we get:
    $$\mathbf{0} = 0\mathbf{v}_1 + 0\mathbf{v}_2 + \dots + 0\mathbf{v}_k$$
    Since the zero vector can be expressed as a linear combination of vectors in $S$, $\mathbf{0} \in W$.
2.  **Closure under Addition:**
    Let $\mathbf{u}$ and $\mathbf{w}$ be any two arbitrary vectors in $W$. By definition of span:
    $$\mathbf{u} = c_1 \mathbf{v}_1 + c_2 \mathbf{v}_2 + \dots + c_k \mathbf{v}_k$$
    $$\mathbf{w} = d_1 \mathbf{v}_1 + d_2 \mathbf{v}_2 + \dots + d_k \mathbf{v}_k$$
    Adding them yields:
    $$\mathbf{u} + \mathbf{w} = (c_1 + d_1)\mathbf{v}_1 + (c_2 + d_2)\mathbf{v}_2 + \dots + (c_k + d_k)\mathbf{v}_k$$
    Since each $(c_i + d_i)$ is simply a real scalar, $\mathbf{u} + \mathbf{w}$ is expressible as a linear combination of vectors in $S$. Thus, $\mathbf{u} + \mathbf{w} \in W$.
3.  **Closure under Scalar Multiplication:**
    Let $k$ be any real scalar, and let $\mathbf{u} \in W$. Then:
    $$k\mathbf{u} = k(c_1 \mathbf{v}_1 + c_2 \mathbf{v}_2 + \dots + c_k \mathbf{v}_k) = (kc_1)\mathbf{v}_1 + (kc_2)\mathbf{v}_2 + \dots + (kc_k)\mathbf{v}_k$$
    Since each $(kc_i)$ is a real scalar, $k\mathbf{u}$ is a valid linear combination of vectors in $S$. Thus, $k\mathbf{u} \in W$.

Since all three conditions hold, $W = \text{span}(S)$ is guaranteed to be a **subspace of $V$**.

#### 3. Algebraic Verification Recipe: Does a set span $\mathbb{R}^n$?
To verify whether a given collection of vectors $\{\mathbf{v}_1, \dots, \mathbf{v}_k\}$ spans the entire space $\mathbb{R}^n$:
1.  **Set up the generic equation:** Let $\mathbf{b} = \begin{bmatrix} b_1 & b_2 & \dots & b_n \end{bmatrix}^T$ be an arbitrary vector with unknown real entries. Set:
    $$c_1 \mathbf{v}_1 + c_2 \mathbf{v}_2 + \dots + c_k \mathbf{v}_k = \mathbf{b}$$
2.  **Form the Augmented Matrix $[A \mid \mathbf{b}]$:** Place the vectors as columns of matrix $A$:
    $$[A \mid \mathbf{b}] = \left[ \begin{array}{cccc|c} \mathbf{v}_1 & \mathbf{v}_2 & \dots & \mathbf{v}_k & \mathbf{b} \end{array} \right]$$
3.  **Row-Reduce to Echelon Form:**
    *   **If the system is consistent for ALL possible vectors $\mathbf{b}$:** (i.e., every row contains a pivot, meaning no row of all zeros equals an expression in $b_i$), then the set **spans $\mathbb{R}^n$**.
    *   **If a zero row appears with a condition on $\mathbf{b}$:** (e.g., $[0 \, 0 \dots 0 \mid b_3 - 2b_1 + b_2]$), the system is *inconsistent* for any vector that does not satisfy $b_3 - 2b_1 + b_2 = 0$. The vectors **do not span $\mathbb{R}^n$**; instead, they span only the restricted subspace plane defined by that equation.

---

### Linear Dependence & Linear Independence
> **Video Resources:** 
> *   Conceptual Overview: [Khan Academy - Introduction to Linear Independence](https://youtu.be/CrV1xCWdY-g?si=J1__7pwZPAHoCnrI)
> *   Formal Definition & Proof: [Khan Academy - Linear Dependence Definition & Proof](https://youtu.be/Alhcv5d_XOs?si=uir2EAfCrEKR9y9X)
> *   Comprehensive 3D Walkthrough: [Khan Academy - Span & Linear Independence in $\mathbb{R}^3$ Example](https://youtu.be/9kW6zFK5E5c?si=J3XfcL8wyqZLLq6t)

#### 1. Intuition: "Redundancy" vs. "New Direction"
When assembling a collection of vectors, we want to know whether each vector we add is actually contributing useful geometric territory:
*   **Linearly Dependent (Redundant):** At least one vector in the set can already be constructed by taking a linear combination of the other vectors. Adding this vector provides **zero new directionality** and does not expand the dimension of the span:
    $$\text{span}(\mathbf{v}_1, \dots, \mathbf{v}_{k-1}, \mathbf{v}_k) = \text{span}(\mathbf{v}_1, \dots, \mathbf{v}_{k-1})$$
*   **Linearly Independent (No Waste):** No vector in the set can be formed from the others. Every single vector "breaks out" into a genuinely new dimension, expanding the dimension of the span by $+1$.

#### 2. The Formal Definition
Let $S = \{\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_k\}$ be a set of vectors in a vector space $V$. Consider the homogeneous vector equation:
$$c_1 \mathbf{v}_1 + c_2 \mathbf{v}_2 + \dots + c_k \mathbf{v}_k = \mathbf{0}$$

This equation always has at least the **trivial solution**: $c_1 = c_2 = \dots = c_k = 0$.
*   **Linearly Independent (LI):** If the trivial solution is the **ONLY** solution to the equation.
*   **Linearly Dependent (LD):** If there exists a **non-trivial solution**—meaning we can find scalars $c_1, c_2, \dots, c_k$, **not all zero** (at least one $c_i \neq 0$), that satisfy the equation.

> ### <a id="theorem-5-3-1"></a><mark>Theorem 5.3.1 (The Redundancy Equivalence Theorem)</mark>
> A set $S$ with two or more vectors is linearly dependent if and only if at least one of the vectors in $S$ is expressible as a linear combination of the other vectors in $S$.
> Conversely, a set $S$ is linearly independent if and only if no vector in $S$ is expressible as a linear combination of the other vectors in $S$.

<mark style="background-color: lightgreen;">Proof (The Two-Way $\iff$ Chain):</mark>
*   **Direction 1 ($\impliedby$ Redundancy implies Linear Dependence):**
    Suppose one vector (without loss of generality, say $\mathbf{v}_1$) is a linear combination of the remaining vectors:
    $$\mathbf{v}_1 = a_2 \mathbf{v}_2 + a_3 \mathbf{v}_3 + \dots + a_k \mathbf{v}_k$$
    Subtract $\mathbf{v}_1$ from both sides:
    $$(-1)\mathbf{v}_1 + a_2 \mathbf{v}_2 + a_3 \mathbf{v}_3 + \dots + a_k \mathbf{v}_k = \mathbf{0}$$
    Notice the coefficient of $\mathbf{v}_1$ is $-1 \neq 0$. Because we have found a combination equal to $\mathbf{0}$ where at least one coefficient is non-zero, $S$ is **linearly dependent**.
*   **Direction 2 ($\implies$ Linear Dependence implies Redundancy):**
    Assume $S$ is linearly dependent. By definition, there exist scalars $c_1, c_2, \dots, c_k$, not all zero, such that:
    $$c_1 \mathbf{v}_1 + c_2 \mathbf{v}_2 + \dots + c_k \mathbf{v}_k = \mathbf{0}$$
    Since not all scalars are zero, choose any vector whose coefficient is non-zero (say $c_1 \neq 0$). 
    Because $c_1 \neq 0$, we can isolate $c_1 \mathbf{v}_1$ and divide both sides by $c_1$:
    $$c_1 \mathbf{v}_1 = -c_2 \mathbf{v}_2 - c_3 \mathbf{v}_3 - \dots - c_k \mathbf{v}_k$$
    $$\mathbf{v}_1 = \left(-\frac{c_2}{c_1}\right)\mathbf{v}_2 + \left(-\frac{c_3}{c_1}\right)\mathbf{v}_3 + \dots + \left(-\frac{c_k}{c_1}\right)\mathbf{v}_k$$
    Thus, $\mathbf{v}_1$ is explicitly expressed as a linear combination of the other vectors.

> [!NOTE] Concept: "No Single Bad Apple"
> Redundancy is a collective property of the set, not a fault of a single vector. Any vector in the dependency equation with a non-zero coefficient can be isolated as the "redundant" one.

#### 3. Redundancy vs. Collinearity: The 2-Vector vs. 3+ Vector Rule
*   **For 2 vectors:** Linear dependence is **identical** to collinearity. Two vectors are dependent if and only if one is a scalar multiple of the other ($\mathbf{v}_2 = c\mathbf{v}_1$).
*   **For 3 or more vectors:** Linear dependence **does NOT require any two vectors to be collinear**. Three vectors can be linearly dependent simply by being **coplanar** (lying on the same 2D plane).
    *   *Counterexample:* $\mathbf{v}_1 = \begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix}, \mathbf{v}_2 = \begin{bmatrix} 0 \\ 1 \\ 0 \end{bmatrix}, \mathbf{v}_3 = \begin{bmatrix} 1 \\ 1 \\ 0 \end{bmatrix}$. No two vectors are scalar multiples (they are perpendicular / distinct), yet $\mathbf{v}_3 = \mathbf{v}_1 + \mathbf{v}_2$. The set is linearly dependent because $\mathbf{v}_3$ is trapped in the $xy$-plane!

> ### <a id="theorem-5-3-2"></a><mark>Theorem 5.3.2 (Zero Vector and Two-Vector Dependency)</mark>
> *   **(a)** Any finite set of vectors that contains the zero vector $\mathbf{0}$ is **automatically linearly dependent**.
>     *Proof:* For $S = \{\mathbf{0}, \mathbf{v}_1, \dots, \mathbf{v}_k\}$, the equation $1\mathbf{0} + 0\mathbf{v}_1 + \dots + 0\mathbf{v}_k = \mathbf{0}$ has a non-zero coefficient ($1 \neq 0$) for $\mathbf{0}$.
> *   **(b)** A set with exactly two vectors is linearly independent if and only if neither vector is a scalar multiple of the other.

> ### <a id="theorem-5-3-3"></a><mark>Theorem 5.3.3 (More Vectors than Dimensions in $\mathbb{R}^n$)</mark>
> Let $S = \{\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_r\}$ be a set of vectors in $\mathbb{R}^n$. If $r > n$ (more vectors than the dimension of the space), then $S$ is **guaranteed to be linearly dependent**.

<mark style="background-color: lightgreen;">Proof:</mark>
Let $\mathbf{v}_j = \begin{bmatrix} v_{1j} & v_{2j} & \dots & v_{nj} \end{bmatrix}^T$. The vector equation $c_1 \mathbf{v}_1 + \dots + c_r \mathbf{v}_r = \mathbf{0}$ equates to the homogeneous linear system:
$$\begin{cases}
v_{11}c_1 + v_{12}c_2 + \dots + v_{1r}c_r = 0 \\
v_{21}c_1 + v_{22}c_2 + \dots + v_{2r}c_r = 0 \\
\vdots \\
v_{n1}c_1 + v_{n2}c_2 + \dots + v_{nr}c_r = 0
\end{cases}$$
This is a homogeneous system of $n$ equations in $r$ unknowns ($c_1, \dots, c_r$). Because $r > n$ (more unknowns than equations), by Theorem 1.6.1/Gaussian elimination, the system **must have at least one free variable**. A free variable yields infinitely many non-trivial solutions. Since non-trivial solutions exist, the set $S$ is linearly dependent.

#### 4. Dimension of Span vs. Ambient Space ($\mathbb{R}^n$)
*   If a set of $k$ vectors has $m$ redundant vectors, the **dimension of its span** is:
    $$\text{Dimension of Span} = k - m \quad (\text{Rank})$$
*   **Ambient Space vs. Subspace:** If the vectors live in $\mathbb{R}^n$:
    *   If $k - m = n$, the span covers **all of $\mathbb{R}^n$**.
    *   If $k - m < n$, the span forms a **$(k-m)$-dimensional flat subspace** (a line, plane, etc.) slicing through the origin inside $\mathbb{R}^n$. It does *not* cover all of $\mathbb{R}^n$.
*   **Redundancy does NOT shrink span:** Having redundant vectors never reduces the territory your set can reach; it only means the set is inefficient (not minimal).

#### 5. The Master Theorem Connection ($n$ Vectors in $\mathbb{R}^n$)
When testing exactly $n$ vectors in $\mathbb{R}^n$, we form the square matrix $A = [\mathbf{v}_1 \mid \mathbf{v}_2 \mid \dots \mid \mathbf{v}_n]$. By the Master Theorem (Theorem 2.3.6):
$$\text{Linearly Independent} \iff \text{Spans } \mathbb{R}^n \iff A\mathbf{c} = \mathbf{0} \text{ has only trivial solution} \iff \det(A) \neq 0 \iff A \text{ is invertible}$$

---

### Comprehensive Worked Examples

#### Example 1: Testing 2 Vectors in $\mathbb{R}^2$ (Linearly Independent)
Vectors: $\mathbf{v}_1 = \begin{bmatrix} 2 \\ 1 \end{bmatrix}, \mathbf{v}_2 = \begin{bmatrix} 3 \\ 2 \end{bmatrix}$.
*   Set $c_1 \begin{bmatrix} 2 \\ 1 \end{bmatrix} + c_2 \begin{bmatrix} 3 \\ 2 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \end{bmatrix} \implies \begin{cases} 2c_1 + 3c_2 = 0 \\ 1c_1 + 2c_2 = 0 \end{cases}$
*   Row operation ($R_1 \leftarrow R_1 - 2R_2$): $-c_2 = 0 \implies c_2 = 0 \implies c_1 = 0$.
*   **Result:** Only the trivial solution exists $\implies$ **Linearly Independent**. Since they are 2 independent vectors in $\mathbb{R}^2$, they span all of $\mathbb{R}^2$.

#### Example 2: Testing 3 Vectors in $\mathbb{R}^2$ (Linearly Dependent)
Vectors: $\mathbf{v}_1 = \begin{bmatrix} 2 \\ 1 \end{bmatrix}, \mathbf{v}_2 = \begin{bmatrix} 3 \\ 2 \end{bmatrix}, \mathbf{v}_3 = \begin{bmatrix} 1 \\ 2 \end{bmatrix}$.
*   By Theorem 5.3.3 ($r=3 > n=2$), this set is **instantly linearly dependent** without doing any algebra!
*   To find the non-trivial relation: $c_1 \begin{bmatrix} 2 \\ 1 \end{bmatrix} + c_2 \begin{bmatrix} 3 \\ 2 \end{bmatrix} + c_3 \begin{bmatrix} 1 \\ 2 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \end{bmatrix}$
    $$\begin{cases} 2c_1 + 3c_2 + c_3 = 0 \\ c_1 + 2c_2 + 2c_3 = 0 \end{cases}$$
*   Setting the free variable $c_3 = -1$ yields $c_2 = 3$ and $c_1 = -4$:
    $$-4\begin{bmatrix} 2 \\ 1 \end{bmatrix} + 3\begin{bmatrix} 3 \\ 2 \end{bmatrix} - 1\begin{bmatrix} 1 \\ 2 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \end{bmatrix}$$
*   Non-zero scalars found $\implies$ **Linearly Dependent**.

#### Example 3: Proving Span and Linear Independence in $\mathbb{R}^3$ Simultaneously
Let $S = \left\{ \begin{bmatrix} 1 \\ -1 \\ 2 \end{bmatrix}, \begin{bmatrix} 2 \\ 1 \\ 3 \end{bmatrix}, \begin{bmatrix} -1 \\ 0 \\ 2 \end{bmatrix} \right\}$. 
Does $S$ span $\mathbb{R}^3$, and is $S$ linearly independent?

*   **Step 1: Set up for generic vector $\begin{bmatrix} a \\ b \\ c \end{bmatrix} \in \mathbb{R}^3$:**
    $$c_1 \begin{bmatrix} 1 \\ -1 \\ 2 \end{bmatrix} + c_2 \begin{bmatrix} 2 \\ 1 \\ 3 \end{bmatrix} + c_3 \begin{bmatrix} -1 \\ 0 \\ 2 \end{bmatrix} = \begin{bmatrix} a \\ b \\ c \end{bmatrix}$$
    This yields the linear system:
    $$\begin{cases} 
    c_1 + 2c_2 - c_3 = a \quad \text{--- (Eq 1)} \\
    -c_1 + c_2 = b \quad \text{--- (Eq 2)} \\
    2c_1 + 3c_2 + 2c_3 = c \quad \text{--- (Eq 3)}
    \end{cases}$$
*   **Step 2: Eliminate $c_1$:**
    *   Add Eq 1 to Eq 2: $3c_2 - c_3 = a + b \quad \text{--- (Eq 4)}$
    *   Eq 3 minus $2 \times$ Eq 1: $-c_2 + 4c_3 = c - 2a \quad \text{--- (Eq 5)}$
*   **Step 3: Eliminate $c_2$:**
    *   Multiply Eq 5 by $3$ and add to Eq 4:
        $$11c_3 = 3(c - 2a) + (a + b) = 3c - 5a + b$$
        $$c_3 = \frac{1}{11}(-5a + b + 3c)$$
*   **Step 4: Back-substitute to isolate all scalars:**
    $$c_2 = \frac{1}{3}(a + b + c_3)$$
    $$c_1 = a - 2c_2 + c_3$$
*   **Conclusion 1 (Span):** For *any* arbitrary real values $a, b, c$, real solutions for $c_1, c_2, c_3$ exist (no division by zero occurs). Therefore, **$S$ spans all of $\mathbb{R}^3$**!
*   **Conclusion 2 (Linear Independence):** To test for linear independence, set $\begin{bmatrix} a \\ b \\ c \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix}$:
    $$c_3 = \frac{1}{11}(0) = 0 \implies c_2 = \frac{1}{3}(0) = 0 \implies c_1 = 0$$
    The only solution to the homogeneous equation is the trivial solution $c_1 = c_2 = c_3 = 0$. Therefore, **$S$ is linearly independent**!

---

### Basis of a Subspace
> **Video Resource:** [Khan Academy - Basis of a Subspace](https://youtu.be/zntNi3-ybfQ?si=U2jXGzhiX4S3_JRD)

When we combine **Spanning** (coverage) and **Linear Independence** (minimalism/zero waste), we arrive at the central definition of modern linear algebra: the **Basis**.

<mark>Definition (Basis of a Subspace):</mark>
Let $V$ be a subspace of $\mathbb{R}^n$. A set of vectors $B = \{\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_k\}$ is called a **basis** for the subspace $V$ if and only if it satisfies two conditions:
1.  **$B$ Spans $V$:** $\text{span}(B) = V$ (The vectors can construct every single vector in $V$).
2.  **$B$ is Linearly Independent:** $c_1 \mathbf{v}_1 + \dots + c_k \mathbf{v}_k = \mathbf{0} \implies c_1 = \dots = c_k = 0$ (No vector in $B$ is redundant).

#### The Intuition: "A Minimal Spanning Set"
*   **A Spanning Set alone** might be bloated. If you have 10 vectors that span a 2D plane, they can reach everywhere on the plane, but 8 of them are useless clutter (redundant).
*   **A Linearly Independent Set alone** is efficient, but it might not be big enough. A single vector in $\mathbb{R}^3$ has zero waste, but it only reaches a 1D line, leaving out the rest of the 3D space.
*   **A Basis is "Goldilocks":** It has *just enough* vectors to cover the entire subspace, but *not a single vector more*. If you remove even one vector from a basis, it can no longer span the space. If you add even one vector, it becomes linearly dependent.
*   **A Coordinate Grid:** A basis provides a unique coordinate frame for its subspace.

---

#### Video Example 1: Testing if a Set Forms a Basis for $\mathbb{R}^2$
Let $S = \left\{ \begin{bmatrix} 2 \\ 3 \end{bmatrix}, \begin{bmatrix} 7 \\ 0 \end{bmatrix} \right\}$. Is $S$ a basis for $\mathbb{R}^2$?

*   **Step 1: Test Spanning Condition ($\text{span}(S) = \mathbb{R}^2$)**
    We test whether an arbitrary vector $\begin{bmatrix} x_1 \\ x_2 \end{bmatrix} \in \mathbb{R}^2$ can be written as:
    $$c_1 \begin{bmatrix} 2 \\ 3 \end{bmatrix} + c_2 \begin{bmatrix} 7 \\ 0 \end{bmatrix} = \begin{bmatrix} x_1 \\ x_2 \end{bmatrix}$$
    This produces the system of equations:
    $$\begin{cases} 
    2c_1 + 7c_2 = x_1 \quad \text{--- (Eq 1)} \\ 
    3c_1 + 0c_2 = x_2 \quad \text{--- (Eq 2)} 
    \end{cases}$$
    From Eq 2:
    $$c_1 = \frac{x_2}{3}$$
    Substitute $c_1$ into Eq 1:
    $$2\left(\frac{x_2}{3}\right) + 7c_2 = x_1 \implies 7c_2 = x_1 - \frac{2}{3}x_2 \implies c_2 = \frac{x_1}{7} - \frac{2}{21}x_2$$
    Notice that no matter what real numbers we choose for $x_1$ and $x_2$, we obtain valid, real values for $c_1$ and $c_2$. Therefore, **$S$ spans all of $\mathbb{R}^2$**!

*   **Step 2: Test Linear Independence**
    We test if $c_1 \begin{bmatrix} 2 \\ 3 \end{bmatrix} + c_2 \begin{bmatrix} 7 \\ 0 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \end{bmatrix}$ allows any non-trivial solution.
    Using our solved equations from Step 1, plug in $x_1 = 0$ and $x_2 = 0$:
    $$c_1 = \frac{0}{3} = 0$$
    $$c_2 = \frac{0}{7} - \frac{2}{21}(0) = 0$$
    The *only* solution is the trivial solution $c_1 = 0$ and $c_2 = 0$. Therefore, **$S$ is linearly independent**!

*   **Conclusion:** Because $S$ satisfies both conditions, $S$ is officially a **basis for $\mathbb{R}^2$**.

---

#### Video Example 2: Why Redundancy Disqualifies a Basis
Suppose we take the same set $S$ and add a third vector that is a linear combination of them, say $\mathbf{v}_{\text{special}} = \mathbf{v}_1 + \mathbf{v}_2 = \begin{bmatrix} 9 \\ 3 \end{bmatrix}$:
$$S' = \left\{ \begin{bmatrix} 2 \\ 3 \end{bmatrix}, \begin{bmatrix} 7 \\ 0 \end{bmatrix}, \begin{bmatrix} 9 \\ 3 \end{bmatrix} \right\}$$
*   Does $S'$ span $\mathbb{R}^2$? **Yes.** Adding more vectors never shrinks your span.
*   Is $S'$ linearly independent? **No!** Because $1\mathbf{v}_1 + 1\mathbf{v}_2 - 1\mathbf{v}_{\text{special}} = \mathbf{0}$ provides a non-trivial solution ($c_1=1, c_2=1, c_3=-1$).
*   **Verdict:** $S'$ is **NOT a basis**. A basis cannot contain any redundant vectors.

---

#### Standard Basis vs. Multiple Bases
*   **The Standard Basis of $\mathbb{R}^2$:** The most intuitive and simplest basis for $\mathbb{R}^2$ is made of the standard unit vectors:
    $$T = \{\hat{i}, \hat{j}\} = \left\{ \begin{bmatrix} 1 \\ 0 \end{bmatrix}, \begin{bmatrix} 0 \\ 1 \end{bmatrix} \right\}$$
    Any vector $\begin{bmatrix} x_1 \\ x_2 \end{bmatrix}$ is trivially $x_1\begin{bmatrix}1\\0\end{bmatrix} + x_2\begin{bmatrix}0\\1\end{bmatrix}$.
*   **Infinitely Many Bases:** A subspace does not have just one basis! As shown above, both $S = \left\{\begin{bmatrix}2\\3\end{bmatrix}, \begin{bmatrix}7\\0\end{bmatrix}\right\}$ and $T = \left\{\begin{bmatrix}1\\0\end{bmatrix}, \begin{bmatrix}0\\1\end{bmatrix}\right\}$ are valid bases for $\mathbb{R}^2$. In fact, every non-zero subspace has **infinitely many different bases**.

---

#### Fundamental Theorem: Uniqueness of Basis Representation

> ### <a id="theorem-uniqueness-basis"></a><mark>Theorem (Uniqueness of Basis Representation)</mark>
> Let $B = \{\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_n\}$ be a basis for a subspace $V$. Then every vector $\mathbf{a} \in V$ can be expressed as a linear combination of the basis vectors in **one and only one unique way**.

<mark style="background-color: lightgreen;">Proof (by Contradiction):</mark>
Suppose there exists some vector $\mathbf{a} \in V$ that can be represented as a linear combination of the basis vectors in **two different ways**:
$$\mathbf{a} = c_1 \mathbf{v}_1 + c_2 \mathbf{v}_2 + \dots + c_n \mathbf{v}_n \quad \text{--- (Representation 1)}$$
$$\mathbf{a} = d_1 \mathbf{v}_1 + d_2 \mathbf{v}_2 + \dots + d_n \mathbf{v}_n \quad \text{--- (Representation 2)}$$
where at least one coefficient is different (i.e., $c_i \neq d_i$ for some $i$).

Now, subtract Representation 2 from Representation 1:
$$\mathbf{a} - \mathbf{a} = (c_1 - d_1)\mathbf{v}_1 + (c_2 - d_2)\mathbf{v}_2 + \dots + (c_n - d_n)\mathbf{v}_n$$
$$\mathbf{0} = (c_1 - d_1)\mathbf{v}_1 + (c_2 - d_2)\mathbf{v}_2 + \dots + (c_n - d_n)\mathbf{v}_n$$

Notice what this equation represents: it is a linear combination of the vectors in $B$ that equals the zero vector $\mathbf{0}$.
However, by definition, $B$ is a basis, which means its vectors are **linearly independent**.
By the definition of linear independence, the *only* solution to a linear combination equaling $\mathbf{0}$ is the trivial solution where **every single coefficient is zero**:
$$c_1 - d_1 = 0 \implies c_1 = d_1$$
$$c_2 - d_2 = 0 \implies c_2 = d_2$$
$$\vdots$$
$$c_n - d_n = 0 \implies c_n = d_n$$

This directly contradicts our assumption that there was at least one index where $c_i \neq d_i$!
Therefore, the two representations must be identical. Every vector in $V$ has a **strictly unique coordinate representation** relative to a basis. $\blacksquare$

---

### The Null Space of a Matrix & Finding its Basis
> **Video Resources:** 
> *   Theory & Subspace Proof: [Khan Academy - The Null Space of a Matrix](https://youtu.be/jCwRV1QL_Xs?si=pT1t04snAQg2Wjw7)
> *   Calculation & Basis Walkthrough: [Khan Academy - Null Space 2: Calculating the Null Space of a Matrix](https://youtu.be/qvyboGryeA8?si=fa2s5FjFNxjti9nC)
> *   Connection to Linear Independence: [Khan Academy - Null space 3: Relation to linear independence](https://youtu.be/vFctYRhK2M0?si=m817tQm5qm3hWnnX)

#### 1. What is the Null Space?
Let $A$ be an $m \times n$ matrix (having $m$ rows and $n$ columns).
The **Null Space of $A$** (often denoted $\text{Null}(A)$ or $N(A)$, and sometimes called the **Kernel** $\ker(A)$) is the set of all vectors $\mathbf{x} \in \mathbb{R}^n$ that satisfy the homogeneous matrix equation:
$$A\mathbf{x} = \mathbf{0}$$

$$\text{Null}(A) = \{\mathbf{x} \in \mathbb{R}^n \mid A\mathbf{x} = \mathbf{0}\}$$

*   **Dimensional Compatibility & Where it Lives:**
    Because $A$ is $m \times n$:
    $$\underset{(m \times n)}{A} \;\; \underset{(n \times 1)}{\mathbf{x}} = \underset{(m \times 1)}{\mathbf{0}}$$
    *   The vector $\mathbf{x}$ must have $n$ entries to multiply with $A$. Therefore, **$\text{Null}(A)$ is a subspace of $\mathbb{R}^n$** (the domain / input space).
    *   The output $\mathbf{0}$ has $m$ entries, residing in $\mathbb{R}^m$ (the codomain / output space).
*   **The Practical Meaning:** Solving for the null space is identical to solving the homogeneous linear system of equations $A\mathbf{x} = \mathbf{0}$.

---

#### 2. Formal Proof: Why $\text{Null}(A)$ is Always a Valid Subspace of $\mathbb{R}^n$
To prove that $\text{Null}(A)$ is a subspace of $\mathbb{R}^n$, we test the three subspace conditions:

1.  **Contains the Zero Vector ($\mathbf{0} \in \text{Null}(A)$):**
    For any $m \times n$ matrix $A$, multiplying by the zero vector in $\mathbb{R}^n$ yields:
    $$A\mathbf{0}_n = \mathbf{0}_m$$
    Since the zero vector satisfies the equation $A\mathbf{x} = \mathbf{0}$, $\mathbf{0} \in \text{Null}(A)$.

2.  **Closed under Vector Addition:**
    Let $\mathbf{v}_1, \mathbf{v}_2 \in \text{Null}(A)$. By definition, $A\mathbf{v}_1 = \mathbf{0}$ and $A\mathbf{v}_2 = \mathbf{0}$.
    Using the distributive property of matrix multiplication:
    $$A(\mathbf{v}_1 + \mathbf{v}_2) = A\mathbf{v}_1 + A\mathbf{v}_2 = \mathbf{0} + \mathbf{0} = \mathbf{0}$$
    Since their sum also maps to $\mathbf{0}$, $(\mathbf{v}_1 + \mathbf{v}_2) \in \text{Null}(A)$.

3.  **Closed under Scalar Multiplication:**
    Let $\mathbf{v}_1 \in \text{Null}(A)$ (so $A\mathbf{v}_1 = \mathbf{0}$) and let $c$ be any real scalar ($c \in \mathbb{R}$).
    $$A(c\mathbf{v}_1) = c(A\mathbf{v}_1) = c(\mathbf{0}) = \mathbf{0}$$
    Since the scaled vector also maps to $\mathbf{0}$, $c\mathbf{v}_1 \in \text{Null}(A)$.

Since all 3 criteria hold, $\text{Null}(A)$ is **guaranteed to be a linear subspace of $\mathbb{R}^n$**.

---

#### 3. Step-by-Step Recipe: Calculating a Basis for $\text{Null}(A)$
To find a basis for the null space of a matrix $A$:
1.  **Row-Reduce to RREF:** Transform matrix $A$ into its Reduced Row-Echelon Form ($\text{RREF}(A)$) by applying Elementary Row Operations (EROs). (Since the right-hand side is $\mathbf{0}$, row operations never alter the zero vector, so working directly on $A$ is sufficient).
2.  **Identify Pivot vs. Free Variables:**
    *   **Pivot Variables:** Variables corresponding to columns with leading $1$s.
    *   **Free Variables:** Variables corresponding to columns *without* leading $1$s.
3.  **Express Pivot Variables in Terms of Free Variables:** Rewrite the equations from RREF so that each pivot variable is isolated on the left.
4.  **Write the General Solution in Parametric Vector Form:** Decompose the solution vector $\mathbf{x}$ as a linear combination of constant vectors, factored by each free variable.
5.  **Extract the Basis Vectors:** The constant vectors attached to the free variables form a **basis** for $\text{Null}(A)$.
    *   *Why are they linearly independent?* Each basis vector has a $1$ in the row of its corresponding free variable and $0$ in the rows of all other free variables. This identity-like structure makes it impossible for any vector to be a combination of the others!
    *   *Dimension (Nullity):* The dimension of the null space, $\dim(\text{Null}(A))$ (called the **nullity** of $A$), is **strictly equal to the number of free variables**.

---

#### 4. Complete Worked Example from the Video ($3 \times 4$ Matrix)
Find a basis and the dimension for the null space of the $3 \times 4$ matrix:
$$A = \begin{bmatrix} 1 & 1 & 1 & 1 \\ 1 & 2 & 3 & 4 \\ 1 & 3 & 5 & 7 \end{bmatrix}$$

##### Step 1: Set up the homogeneous equation
We seek all vectors $\mathbf{x} = \begin{bmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{bmatrix} \in \mathbb{R}^4$ such that:
$$\begin{bmatrix} 1 & 1 & 1 & 1 \\ 1 & 2 & 3 & 4 \\ 1 & 3 & 5 & 7 \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix}$$

##### Step 2: Row-reduce $A$ to RREF
*   $R_2 \leftarrow R_2 - R_1$:
    $$\begin{bmatrix} 1 & 1 & 1 & 1 \\ 0 & 1 & 2 & 3 \\ 1 & 3 & 5 & 7 \end{bmatrix}$$
*   $R_3 \leftarrow R_3 - R_1$:
    $$\begin{bmatrix} 1 & 1 & 1 & 1 \\ 0 & 1 & 2 & 3 \\ 0 & 2 & 4 & 6 \end{bmatrix}$$
*   $R_3 \leftarrow R_3 - 2R_2$:
    $$\begin{bmatrix} 1 & 1 & 1 & 1 \\ 0 & 1 & 2 & 3 \\ 0 & 0 & 0 & 0 \end{bmatrix}$$
*   $R_1 \leftarrow R_1 - R_2$:
    $$\text{RREF}(A) = \begin{bmatrix} 1 & 0 & -1 & -2 \\ 0 & 1 & 2 & 3 \\ 0 & 0 & 0 & 0 \end{bmatrix}$$

##### Step 3: Identify variables and isolate pivot variables
*   Columns 1 and 2 contain pivots $\implies x_1, x_2$ are **pivot variables**.
*   Columns 3 and 4 contain no pivots $\implies x_3, x_4$ are **free variables**.

From Row 1:
$$x_1 - x_3 - 2x_4 = 0 \implies x_1 = x_3 + 2x_4$$
From Row 2:
$$x_2 + 2x_3 + 3x_4 = 0 \implies x_2 = -2x_3 - 3x_4$$

##### Step 4: Write in parametric vector form
$$\mathbf{x} = \begin{bmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{bmatrix} = \begin{bmatrix} x_3 + 2x_4 \\ -2x_3 - 3x_4 \\ x_3 \\ x_4 \end{bmatrix} = \begin{bmatrix} x_3 \\ -2x_3 \\ x_3 \\ 0 \end{bmatrix} + \begin{bmatrix} 2x_4 \\ -3x_4 \\ 0 \\ x_4 \end{bmatrix}$$

Factor out the free parameters $x_3$ and $x_4$:
$$\mathbf{x} = x_3 \begin{bmatrix} 1 \\ -2 \\ 1 \\ 0 \end{bmatrix} + x_4 \begin{bmatrix} 2 \\ -3 \\ 0 \\ 1 \end{bmatrix}$$

##### Step 5: State the Null Space and Basis
*   **The Null Space:**
    $$\text{Null}(A) = \text{span}\left( \left\{ \begin{bmatrix} 1 \\ -2 \\ 1 \\ 0 \end{bmatrix}, \begin{bmatrix} 2 \\ -3 \\ 0 \\ 1 \end{bmatrix} \right\} \right)$$
*   **The Basis for $\text{Null}(A)$:**
    $$B_{\text{null}} = \left\{ \begin{bmatrix} 1 \\ -2 \\ 1 \\ 0 \end{bmatrix}, \begin{bmatrix} 2 \\ -3 \\ 0 \\ 1 \end{bmatrix} \right\}$$
*   **Dimension (Nullity):**
    $$\text{nullity}(A) = \dim(\text{Null}(A)) = 2 \quad (\text{equal to the number of free variables})$$

---

#### 5. The Grand Connection: Null Space & Linear Independence
> **Video Resource:** [Khan Academy - Null space 3: Relation to linear independence](https://youtu.be/vFctYRhK2M0?si=m817tQm5qm3hWnnX)

By writing the matrix-vector product $A\mathbf{x}$ in its **column picture**:
$$A\mathbf{x} = \begin{bmatrix} | & | & & | \\ \mathbf{v}_1 & \mathbf{v}_2 & \dots & \mathbf{v}_n \\ | & | & & | \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix} = x_1 \mathbf{v}_1 + x_2 \mathbf{v}_2 + \dots + x_n \mathbf{v}_n = \mathbf{0}$$

We uncover an immediate and powerful equivalence between the null space and the columns of $A$:

*   **Case 1: The Columns of $A$ are Linearly Independent**
    *   By definition of linear independence, the *only* solution to $x_1 \mathbf{v}_1 + x_2 \mathbf{v}_2 + \dots + x_n \mathbf{v}_n = \mathbf{0}$ is $x_1 = x_2 = \dots = x_n = 0$.
    *   This means the **only** vector in $\text{Null}(A)$ is the zero vector:
        $$\text{Null}(A) = \{\mathbf{0}\}$$
    *   Because there is only the trivial solution, **there are zero free variables** ($\text{nullity}(A) = 0$). Every single column is a pivot column!
    *   *Square $n \times n$ Matrix Connection:* If $A$ is $n \times n$ and its columns are linearly independent, then every column has a leading pivot, so:
        $$\text{RREF}(A) = I_n = \begin{bmatrix} 1 & 0 & \dots & 0 \\ 0 & 1 & \dots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \dots & 1 \end{bmatrix}$$
        *(This connects directly back to the Master Theorem: $A$ is invertible $\iff \det(A) \neq 0 \iff \text{Null}(A) = \{\mathbf{0}\}$).*

*   **Case 2: The Columns of $A$ are Linearly Dependent**
    *   By definition of linear dependence, there exist non-trivial weights (at least one $x_i \neq 0$) such that $x_1 \mathbf{v}_1 + \dots + x_n \mathbf{v}_n = \mathbf{0}$.
    *   This means $\text{Null}(A)$ contains non-zero vectors:
        $$\text{Null}(A) \neq \{\mathbf{0}\} \quad (\text{Contains infinitely many vectors})$$
    *   $\text{RREF}(A)$ will have **at least one free variable** (at least one column without a pivot), meaning $\text{nullity}(A) \ge 1$.

> ### <a id="theorem-null-independence"></a><mark>Theorem (Null Space & Linear Independence Equivalence)</mark>
> For any $m \times n$ matrix $A$:
> $$\text{Columns of } A \text{ are Linearly Independent} \iff \text{Null}(A) = \{\mathbf{0}\} \iff \text{Nullity}(A) = 0 \iff \text{Zero Free Variables}$$

---

<div style="page-break-before: always; break-before: page;"></div>

### The Column Space of a Matrix
> **Video Resource:** [Khan Academy - Column space of a matrix](https://youtu.be/st6D5OdFV9M?si=gZhA-vEjqZ87meq6)

#### 1. What is the Column Space?
Let $A$ be an $m \times n$ matrix (having $m$ rows and $n$ columns). Written in terms of its column vectors:
$$A = \begin{bmatrix} | & | & & | \\ \mathbf{a}_1 & \mathbf{a}_2 & \dots & \mathbf{a}_n \\ | & | & & | \end{bmatrix}$$
where each column vector $\mathbf{a}_j$ has $m$ entries ($\mathbf{a}_j \in \mathbb{R}^m$).

The **Column Space of $A$** (denoted $\text{Col}(A)$ or $C(A)$, and sometimes called the **Range** of the linear transformation defined by $A$) is the set of all possible linear combinations of the column vectors of $A$:
$$\text{Col}(A) = \text{span}(\{\mathbf{a}_1, \mathbf{a}_2, \dots, \mathbf{a}_n\}) = \left\{ A\mathbf{x} \mid \mathbf{x} \in \mathbb{R}^n \right\}$$

*   **Where does the Column Space live? (Domain vs. Codomain):**
    *   $\mathbf{x}$ has $n$ entries, so $\mathbf{x} \in \mathbb{R}^n$ (the domain / input space).
    *   The matrix-vector product $A\mathbf{x}$ has $m$ entries, so $A\mathbf{x} \in \mathbb{R}^m$ (the codomain / output space).
    *   Therefore, **$\text{Col}(A)$ is a subspace of $\mathbb{R}^m$**, whereas **$\text{Null}(A)$ is a subspace of $\mathbb{R}^n$**.

---

#### 2. Formal Proof: Why $\text{Col}(A)$ is Always a Valid Subspace of $\mathbb{R}^m$
To verify that $\text{Col}(A)$ constitutes a valid linear subspace of $\mathbb{R}^m$, we test the three subspace conditions:

1.  **Contains the Zero Vector ($\mathbf{0} \in \text{Col}(A)$):**
    Choose the input vector $\mathbf{x} = \mathbf{0} \in \mathbb{R}^n$.
    $$A\mathbf{0}_n = \mathbf{0}_m$$
    Since the zero vector of $\mathbb{R}^m$ can be generated by multiplying $A$ by an input vector in $\mathbb{R}^n$, $\mathbf{0}_m \in \text{Col}(A)$.

2.  **Closed under Vector Addition:**
    Let $\mathbf{u}, \mathbf{v} \in \text{Col}(A)$. By definition of the column space, there exist vectors $\mathbf{x}_1, \mathbf{x}_2 \in \mathbb{R}^n$ such that:
    $$\mathbf{u} = A\mathbf{x}_1 \quad \text{and} \quad \mathbf{v} = A\mathbf{x}_2$$
    Adding them:
    $$\mathbf{u} + \mathbf{v} = A\mathbf{x}_1 + A\mathbf{x}_2 = A(\mathbf{x}_1 + \mathbf{x}_2)$$
    Since $\mathbb{R}^n$ is closed under addition, $(\mathbf{x}_1 + \mathbf{x}_2) \in \mathbb{R}^n$. Because their sum is expressed as $A$ times a valid vector in $\mathbb{R}^n$, $(\mathbf{u} + \mathbf{v}) \in \text{Col}(A)$.

3.  **Closed under Scalar Multiplication:**
    Let $\mathbf{u} \in \text{Col}(A)$ (so $\mathbf{u} = A\mathbf{x}_1$) and let $c$ be any real scalar ($c \in \mathbb{R}$).
    $$c\mathbf{u} = c(A\mathbf{x}_1) = A(c\mathbf{x}_1)$$
    Since $c\mathbf{x}_1 \in \mathbb{R}^n$, the scaled vector is also in the column space: $c\mathbf{u} \in \text{Col}(A)$.

Since all three conditions are satisfied, $\text{Col}(A)$ is **guaranteed to be a linear subspace of $\mathbb{R}^m$**.

---

#### 3. Linear Systems & Solvability via Column Space
Recall the column interpretation of matrix-vector multiplication:
$$A\mathbf{x} = \begin{bmatrix} | & | & & | \\ \mathbf{a}_1 & \mathbf{a}_2 & \dots & \mathbf{a}_n \\ | & | & & | \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix} = x_1 \mathbf{a}_1 + x_2 \mathbf{a}_2 + \dots + x_n \mathbf{a}_n$$
The expression $A\mathbf{x}$ is literally a linear combination of the columns of $A$.

When we examine the non-homogeneous equation $A\mathbf{x} = \mathbf{b}$, we are asking:
*"Can the target vector $\mathbf{b}$ be constructed as a linear combination of the columns of $A$?"*
If yes, a solution $\mathbf{x}$ exists. If no, no solution exists.

> ### <a id="theorem-column-space-consistency"></a><mark>Theorem (Solvability of $Ax = b$ via Column Space)</mark>
> For any $m \times n$ matrix $A$ and any target vector $\mathbf{b} \in \mathbb{R}^m$:
> The linear system $A\mathbf{x} = \mathbf{b}$ is **consistent** (has at least one solution) if and only if $\mathbf{b}$ belongs to the column space of $A$:
> $$A\mathbf{x} = \mathbf{b} \text{ has a solution} \iff \mathbf{b} \in \text{Col}(A)$$

---

<div style="page-break-before: always; break-before: page;"></div>

### Finding Bases for Null Space & Column Space (Unified Walkthrough)
> **Video Resource:** [Khan Academy - Null space and column space basis](https://youtu.be/_uTAdf_AsfQ?si=rYwvAlgsEzvjOH9B)

In this video, Sal Khan works through a single comprehensive example that unifies solving for the **Null Space basis**, identifying the **Column Space basis**, and seeing firsthand how column redundancy works.

Find a basis and dimension for both $\text{Null}(A)$ and $\text{Col}(A)$ for the $3 \times 4$ matrix:
$$A = \begin{bmatrix} 1 & 1 & 1 & 1 \\ 2 & 1 & 4 & 3 \\ 3 & 4 & 1 & 2 \end{bmatrix}$$
with column vectors:
$$\mathbf{a}_1 = \begin{bmatrix} 1 \\ 2 \\ 3 \end{bmatrix}, \quad \mathbf{a}_2 = \begin{bmatrix} 1 \\ 1 \\ 4 \end{bmatrix}, \quad \mathbf{a}_3 = \begin{bmatrix} 1 \\ 4 \\ 1 \end{bmatrix}, \quad \mathbf{a}_4 = \begin{bmatrix} 1 \\ 3 \\ 2 \end{bmatrix}$$

---

#### Step 1: Gaussian Elimination to Reduced Row-Echelon Form ($\text{RREF}$)
We row-reduce the matrix $A$:
$$A = \begin{bmatrix} 1 & 1 & 1 & 1 \\ 2 & 1 & 4 & 3 \\ 3 & 4 & 1 & 2 \end{bmatrix}$$

1.  Eliminate entries below the first pivot in Column 1 ($R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - 3R_1$):
    $$\begin{bmatrix} 1 & 1 & 1 & 1 \\ 0 & -1 & 2 & 1 \\ 0 & 1 & -2 & -1 \end{bmatrix}$$

2.  Scale Row 2 to make the pivot positive ($R_2 \leftarrow -R_2$):
    $$\begin{bmatrix} 1 & 1 & 1 & 1 \\ 0 & 1 & -2 & -1 \\ 0 & 1 & -2 & -1 \end{bmatrix}$$

3.  Eliminate Row 3 using Row 2 ($R_3 \leftarrow R_3 - R_2$):
    $$\begin{bmatrix} 1 & 1 & 1 & 1 \\ 0 & 1 & -2 & -1 \\ 0 & 0 & 0 & 0 \end{bmatrix}$$

4.  Eliminate the entry above the second pivot in Row 1 ($R_1 \leftarrow R_1 - R_2$):
    $$\text{RREF}(A) = \begin{bmatrix} 1 & 0 & 3 & 2 \\ 0 & 1 & -2 & -1 \\ 0 & 0 & 0 & 0 \end{bmatrix}$$

---

#### Step 2: Basis and Dimension for the Null Space ($\text{Null}(A)$)
From $\text{RREF}(A)$:
*   **Pivot Columns:** Columns 1 and 2 contain leading $1$s $\implies x_1, x_2$ are **pivot variables**.
*   **Free Columns:** Columns 3 and 4 contain no pivots $\implies x_3, x_4$ are **free variables**.

Rewrite the system $A\mathbf{x} = \mathbf{0}$ with pivot variables expressed in terms of free variables:
$$x_1 + 3x_3 + 2x_4 = 0 \implies x_1 = -3x_3 - 2x_4$$
$$x_2 - 2x_3 - x_4 = 0 \implies x_2 = 2x_3 + x_4$$

Write the general solution vector $\mathbf{x} \in \mathbb{R}^4$ in **parametric vector form**:
$$\mathbf{x} = \begin{bmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{bmatrix} = \begin{bmatrix} -3x_3 - 2x_4 \\ 2x_3 + x_4 \\ x_3 \\ x_4 \end{bmatrix} = x_3 \begin{bmatrix} -3 \\ 2 \\ 1 \\ 0 \end{bmatrix} + x_4 \begin{bmatrix} -2 \\ 1 \\ 0 \\ 1 \end{bmatrix}$$

*   **Basis for $\text{Null}(A)$:**
    $$B_{\text{null}} = \left\{ \begin{bmatrix} -3 \\ 2 \\ 1 \\ 0 \end{bmatrix}, \begin{bmatrix} -2 \\ 1 \\ 0 \\ 1 \end{bmatrix} \right\}$$
*   **Dimension (Nullity):**
    $$\text{Nullity}(A) = \dim(\text{Null}(A)) = 2 \quad (\text{equal to the } 2 \text{ free variables})$$

---

#### Step 3: Basis and Dimension for the Column Space ($\text{Col}(A)$)
By definition, $\text{Col}(A) = \text{span}(\{\mathbf{a}_1, \mathbf{a}_2, \mathbf{a}_3, \mathbf{a}_4\})$.
To find a **basis**, we must find a linearly independent subset that still spans the space (i.e., we must identify and remove all redundant columns).

Let the columns of $\text{RREF}(A)$ be denoted $\mathbf{r}_1, \mathbf{r}_2, \mathbf{r}_3, \mathbf{r}_4$:
$$\mathbf{r}_1 = \begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix}, \quad \mathbf{r}_2 = \begin{bmatrix} 0 \\ 1 \\ 0 \end{bmatrix}, \quad \mathbf{r}_3 = \begin{bmatrix} 3 \\ -2 \\ 0 \end{bmatrix}, \quad \mathbf{r}_4 = \begin{bmatrix} 2 \\ -1 \\ 0 \end{bmatrix}$$

By immediate visual inspection of the RREF columns:
$$\mathbf{r}_3 = 3\mathbf{r}_1 - 2\mathbf{r}_2$$
$$\mathbf{r}_4 = 2\mathbf{r}_1 - 1\mathbf{r}_2$$

##### The Critical Principle: Row Operations Preserve Column Relations
Elementary row operations never change the solution set to $A\mathbf{x} = \mathbf{0}$. Therefore, **any linear dependence relationship between columns in $\text{RREF}(A)$ holds identically between the columns of the original matrix $A$**:
$$\mathbf{a}_3 = 3\mathbf{a}_1 - 2\mathbf{a}_2$$
$$\mathbf{a}_4 = 2\mathbf{a}_1 - 1\mathbf{a}_2$$

Let's verify this directly using the original columns of $A$:
$$3\mathbf{a}_1 - 2\mathbf{a}_2 = 3\begin{bmatrix} 1 \\ 2 \\ 3 \end{bmatrix} - 2\begin{bmatrix} 1 \\ 1 \\ 4 \end{bmatrix} = \begin{bmatrix} 3 - 2 \\ 6 - 2 \\ 9 - 8 \end{bmatrix} = \begin{bmatrix} 1 \\ 4 \\ 1 \end{bmatrix} = \mathbf{a}_3 \quad \checkmark$$
$$2\mathbf{a}_1 - 1\mathbf{a}_2 = 2\begin{bmatrix} 1 \\ 2 \\ 3 \end{bmatrix} - 1\begin{bmatrix} 1 \\ 1 \\ 4 \end{bmatrix} = \begin{bmatrix} 2 - 1 \\ 4 - 1 \\ 6 - 4 \end{bmatrix} = \begin{bmatrix} 1 \\ 3 \\ 2 \end{bmatrix} = \mathbf{a}_4 \quad \checkmark$$

*   Because $\mathbf{a}_3$ and $\mathbf{a}_4$ are linear combinations of $\mathbf{a}_1$ and $\mathbf{a}_2$, they are **redundant vectors**. Discarding them does not reduce the span:
    $$\text{Col}(A) = \text{span}(\{\mathbf{a}_1, \mathbf{a}_2, \mathbf{a}_3, \mathbf{a}_4\}) = \text{span}(\{\mathbf{a}_1, \mathbf{a}_2\})$$
*   Because columns 1 and 2 are pivot columns (forming the standard unit vectors $\begin{bmatrix}1\\0\\0\end{bmatrix}$ and $\begin{bmatrix}0\\1\\0\end{bmatrix}$ in RREF), $\mathbf{a}_1$ and $\mathbf{a}_2$ are guaranteed to be **linearly independent**.

Therefore, the **pivot columns of the ORIGINAL matrix $A$ form a basis for $\text{Col}(A)$**:
$$B_{\text{col}} = \left\{ \begin{bmatrix} 1 \\ 2 \\ 3 \end{bmatrix}, \begin{bmatrix} 1 \\ 1 \\ 4 \end{bmatrix} \right\}$$

> [!CAUTION]
> ### Major Warning: Never Take Basis Vectors from $\text{RREF}(A)$ for $\text{Col}(A)$
> While you can read the basis for the *null space* directly from the RREF equations, you **MUST NEVER** take the columns of $\text{RREF}(A)$ as the basis for $\text{Col}(A)$!
> *   Row operations preserve the row space, but **alter the column space**.
> *   Notice that the columns of $\text{RREF}(A)$ have a $0$ in their third row. They only span vectors in the $xy$-plane of $\mathbb{R}^3$.
> *   However, the original columns of $A$ span a completely different 2D tilted plane through the origin in $\mathbb{R}^3$!
> *   **Golden Rule:** Use $\text{RREF}(A)$ strictly to discover **which column indices** are pivot columns (here: columns 1 and 2), and then extract those exact column indices from the **original matrix $A$**.

---

<div style="page-break-before: always; break-before: page;"></div>

### Rank, Nullity & The Rank-Nullity Theorem
> **Video Resources:**
> *   Theory of Nullity & Subspace Dimension: [Khan Academy - Dimension of the null space or nullity](https://youtu.be/abYAUqs_n6I?si=_ZSX6UP-iZ99lgMU)
> *   Theory of Rank & Column Space Basis: [Khan Academy - Dimension of the column space or rank](https://youtu.be/JUgrBkPteTg?si=XHnXVRT7-_4wbtvP)

#### 1. Core Definitions
*   **Dimension of a Subspace ($\dim(V)$):** The number of vectors in any basis for that subspace. (All bases for a given subspace are proven to have the exact same number of elements).
*   **Rank ($\text{Rank}(A)$):** The dimension of the column space of $A$:
    $$\text{Rank}(A) = \dim(\text{Col}(A)) = \text{Number of Pivot Columns in } \text{RREF}(A)$$
*   **Nullity ($\text{Nullity}(A)$):** The dimension of the null space of $A$:
    $$\text{Nullity}(A) = \dim(\text{Null}(A)) = \text{Number of Free Variables (Non-Pivot Columns) in } \text{RREF}(A)$$

---

#### 2. Crucial Terminology Distinction: "Independent Variables" vs. "Linearly Independent Vectors"
A frequent source of student confusion is mixing up the everyday algebraic term *"independent variables"* with the geometric concept of *"linearly independent vectors"*:

| Concept | Type of Entity | Meaning in the System $A\mathbf{x} = \mathbf{0}$ |
| :--- | :--- | :--- |
| **Free Variables** | **Scalars** ($x_i$) | **Independent Variables:** You are 100% free to choose any real number for them. |
| **Pivot Variables** | **Scalars** ($x_i$) | **Dependent Variables:** Their values are strictly fixed/dependent on the values chosen for the free variables. |
| **Pivot Columns of $A$** | **Vectors** ($\mathbf{a}_i \in \mathbb{R}^m$) | **Linearly Independent Vectors:** None of them can be formed by the others; they form the basis for $\text{Col}(A)$. |
| **Free Columns of $A$** | **Vectors** ($\mathbf{a}_i \in \mathbb{R}^m$) | **Linearly Dependent Vectors:** They are redundant combinations of the pivot columns. |
| **Solution Vectors ($\mathbf{v}_i$)** | **Vectors** ($\mathbf{v}_i \in \mathbb{R}^n$) | **Linearly Independent Vectors:** The vectors factored out by the free variables in parametric form form the basis for $\text{Null}(A)$. |

> **Key Takeaway:** Free variables are *algebraically independent variables*. In the matrix, their columns are *linearly dependent (redundant)*, but in the null space, each free variable creates a *linearly independent direction* ($\mathbf{v}_i$) in $\mathbb{R}^n$ that satisfies $A\mathbf{x} = \mathbf{0}$.

---

#### 3. Complete Nullity Walkthrough: $2 \times 5$ Matrix (Video 12)
Find the nullity and a basis for the null space of:
$$B = \begin{bmatrix} 1 & 1 & 2 & 3 & 2 \\ 1 & 1 & 3 & 1 & 4 \end{bmatrix}$$
Here $B$ is a $2 \times 5$ matrix ($m = 2$ rows, $n = 5$ columns).

##### Step 1: Row reduce to RREF
*   $R_2 \leftarrow R_2 - R_1$:
    $$\begin{bmatrix} 1 & 1 & 2 & 3 & 2 \\ 0 & 0 & 1 & -2 & 2 \end{bmatrix}$$
*   $R_1 \leftarrow R_1 - 2R_2$:
    $$\text{RREF}(B) = \begin{bmatrix} 1 & 1 & 0 & 7 & -2 \\ 0 & 0 & 1 & -2 & 2 \end{bmatrix}$$

##### Step 2: Identify variables & isolate pivots
*   Pivot columns: Columns 1 and 3 $\implies x_1, x_3$ are **pivot variables**.
*   Non-pivot columns: Columns 2, 4, and 5 $\implies x_2, x_4, x_5$ are **free variables** (3 free variables).
*   Equations:
    $$x_1 = -x_2 - 7x_4 + 2x_5$$
    $$x_3 = 2x_4 - 2x_5$$

##### Step 3: Write solution in parametric vector form
$$\mathbf{x} = \begin{bmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \\ x_5 \end{bmatrix} = x_2 \begin{bmatrix} -1 \\ \mathbf{1} \\ 0 \\ \mathbf{0} \\ \mathbf{0} \end{bmatrix} + x_4 \begin{bmatrix} -7 \\ \mathbf{0} \\ 2 \\ \mathbf{1} \\ \mathbf{0} \end{bmatrix} + x_5 \begin{bmatrix} 2 \\ \mathbf{0} \\ -2 \\ \mathbf{0} \\ \mathbf{1} \end{bmatrix} = x_2 \mathbf{v}_1 + x_4 \mathbf{v}_2 + x_5 \mathbf{v}_3$$

##### Step 4: Proving Linear Independence (The Embedded Identity Matrix)
Look at rows 2, 4, and 5 (the entries corresponding to the free variables):
$$\begin{bmatrix} \text{Row 2 } (x_2) \\ \text{Row 4 } (x_4) \\ \text{Row 5 } (x_5) \end{bmatrix} \implies \begin{bmatrix} \mathbf{1} & \mathbf{0} & \mathbf{0} \\ \mathbf{0} & \mathbf{1} & \mathbf{0} \\ \mathbf{0} & \mathbf{0} & \mathbf{1} \end{bmatrix} = I_3$$
Because each basis vector has a $1$ where all other vectors have $0$, no vector can ever be constructed as a linear combination of the others!
*   **Basis for $\text{Null}(B)$:**
    $$B_{\text{null}} = \left\{ \begin{bmatrix} -1 \\ 1 \\ 0 \\ 0 \\ 0 \end{bmatrix}, \begin{bmatrix} -7 \\ 0 \\ 2 \\ 1 \\ 0 \end{bmatrix}, \begin{bmatrix} 2 \\ 0 \\ -2 \\ 0 \\ 1 \end{bmatrix} \right\}$$
*   **Nullity:**
    $$\text{Nullity}(B) = \dim(\text{Null}(B)) = 3 \quad (\text{equal to the } 3 \text{ free variables})$$

---

#### 4. Complete Rank Walkthrough: $4 \times 5$ Matrix (Video 13)
Find the rank and a basis for the column space of a $4 \times 5$ matrix $A = [\mathbf{a}_1 \; \mathbf{a}_2 \; \mathbf{a}_3 \; \mathbf{a}_4 \; \mathbf{a}_5]$.

##### Step 1: Row reduce $A$ to RREF
Through elementary row operations:
$$\text{RREF}(A) = R = \begin{bmatrix} 1 & 0 & -1 & 0 & 4 \\ 0 & 1 & 2 & 0 & 1 \\ 0 & 0 & 0 & 1 & -3 \\ 0 & 0 & 0 & 0 & 0 \end{bmatrix}$$

##### Step 2: Locate pivot columns
*   Column 1 has leading 1 in Row 1.
*   Column 2 has leading 1 in Row 2.
*   Column 4 has leading 1 in Row 3.
*   Pivot columns in $R$: **Columns 1, 2, and 4**.

##### Step 3: Extract the basis from the ORIGINAL matrix $A$
*   The pivot columns of the original matrix form a basis for $\text{Col}(A)$:
    $$B_{\text{col}} = \{\mathbf{a}_1, \mathbf{a}_2, \mathbf{a}_4\}$$
*   **Rank:**
    $$\text{Rank}(A) = \dim(\text{Col}(A)) = 3 \quad (\text{equal to the } 3 \text{ pivot columns})$$
*   **Nullity & Total Dimensions Check:**
    $$\text{Nullity}(A) = 5 - 3 = 2 \quad (\text{columns 3 and 5 are non-pivot columns})$$
    $$\text{Rank}(A) + \text{Nullity}(A) = 3 + 2 = 5 = n \quad \checkmark$$

##### Step 4: The Optical Illusion Debunked (Why Pivot Columns are Independent and Non-Pivots are Dependent)
A common student trap is thinking: *"In RREF, the pivot variables are isolated in terms of free variables ($x_1 = x_3 - 4x_5$), so don't the pivot columns depend on the non-pivot columns?"*

**The Answer:** It is the exact **opposite**! In terms of *vectors*, the non-pivot columns are completely built from the pivot columns:
1.  **Examine Column 3 ($\mathbf{r}_3$):**
    $$\mathbf{r}_3 = \begin{bmatrix} -1 \\ 2 \\ 0 \\ 0 \end{bmatrix} = -1 \begin{bmatrix} 1 \\ 0 \\ 0 \\ 0 \end{bmatrix} + 2 \begin{bmatrix} 0 \\ 1 \\ 0 \\ 0 \end{bmatrix} = -\mathbf{r}_1 + 2\mathbf{r}_2 \implies \mathbf{a}_3 = -\mathbf{a}_1 + 2\mathbf{a}_2$$
    Column 3 is a direct linear combination of Columns 1 and 2. It is **redundant (linearly dependent)**!
2.  **Examine Column 5 ($\mathbf{r}_5$):**
    $$\mathbf{r}_5 = \begin{bmatrix} 4 \\ 1 \\ -3 \\ 0 \end{bmatrix} = 4\mathbf{r}_1 + 1\mathbf{r}_2 - 3\mathbf{r}_4 \implies \mathbf{a}_5 = 4\mathbf{a}_1 + 1\mathbf{a}_2 - 3\mathbf{a}_4$$
    Column 5 is a direct linear combination of Columns 1, 2, and 4. It is **redundant (linearly dependent)**!
3.  **Can Pivot Columns Build Each Other?**
    Try to build $\mathbf{r}_1$ using $\mathbf{r}_2$ and $\mathbf{r}_4$:
    $$\begin{bmatrix} \mathbf{1} \\ 0 \\ 0 \\ 0 \end{bmatrix} \stackrel{?}{=} c_2 \begin{bmatrix} \mathbf{0} \\ 1 \\ 0 \\ 0 \end{bmatrix} + c_4 \begin{bmatrix} \mathbf{0} \\ 0 \\ 1 \\ 0 \end{bmatrix} \implies c_2(0) + c_4(0) = 0 \neq \mathbf{1}$$
    It is mathematically impossible! Each pivot column has a leading $1$ where all other pivot columns have zeros. Therefore, **the pivot columns are strictly linearly independent**.

*   **The Builders:** Pivot columns $\mathbf{a}_1, \mathbf{a}_2, \mathbf{a}_4$ are the independent generators $\implies$ **Basis for $\text{Col}(A)$**.
*   **The Clones:** Non-pivot columns $\mathbf{a}_3, \mathbf{a}_5$ are redundant copies $\implies$ **Discarded from the basis**.
*   **The Sliders:** Free variables $x_3, x_5$ are algebraic sliders. Because columns 3 and 5 are clones, you can dial their weights to anything, and the pivot columns can always counter-balance them to $\mathbf{0}$.

---

#### 5. The Rank-Nullity Theorem (The Dimension Theorem)

> ### <a id="theorem-rank-nullity"></a><mark>Theorem (The Rank-Nullity Theorem / Dimension Theorem)</mark>
> For any $m \times n$ matrix $A$ with $n$ columns:
> $$\text{Rank}(A) + \text{Nullity}(A) = n$$
> $$\dim(\text{Col}(A)) + \dim(\text{Null}(A)) = n$$

---

#### 6. Core Intuition: Conservation of Dimensions
Why does this theorem hold so universally?

Think of every column of an $m \times n$ matrix $A$ as representing one variable of your input space $\mathbb{R}^n$. You start with an available budget of **$n$ total dimensions**.

When you perform Gaussian elimination on $A$, every column must fall into one of two mutually exclusive categories:
1.  **Pivot Column (Independent Output Dimension):**
    The column points in a brand-new direction that cannot be created by any previous columns. It extends the reach of your span, providing a genuine new dimension in the output space.
    $$\text{Useful Dimension} \implies \text{Contributes } +1 \text{ to } \text{Rank}(A)$$
2.  **Free Variable Column (Redundant Column / Degree of Freedom to $\mathbf{0}$):**
    The column is a linear combination of earlier pivot columns. It adds zero new dimensions to the output span (it is redundant). But because it duplicates earlier directions, it creates an independent way for non-zero inputs to cancel each other out to $\mathbf{0}$ ($A\mathbf{x} = \mathbf{0}$).
    $$\text{Redundant Dimension} \implies \text{Contributes } +1 \text{ to } \text{Nullity}(A)$$

Because **every column in a matrix is either a pivot column or a free variable column**, the sum of the two must equal the total number of columns:
$$\underbrace{\text{Rank}(A)}_{\text{Pivot Columns (Output Span Dimension)}} + \underbrace{\text{Nullity}(A)}_{\text{Free Columns (Degrees of Freedom to } \mathbf{0})} = \underbrace{n}_{\text{Total Columns (Input Dimension)}}$$

In our worked examples:
*   For the $3 \times 4$ matrix: $\text{Rank} + \text{Nullity} = 2 + 2 = 4 = n \quad \checkmark$
*   For the $2 \times 5$ matrix $B$: $\text{Rank} + \text{Nullity} = 2 + 3 = 5 = n \quad \checkmark$
*   For the $4 \times 5$ matrix $A$: $\text{Rank} + \text{Nullity} = 3 + 2 = 5 = n \quad \checkmark$

---

#### 7. The Grand Unification: The Invertibility Master Theorem
For a square $n \times n$ matrix $A$, the Rank-Nullity Theorem connects everything we have studied into one unified web of equivalence. The following statements are either **all true** or **all false**:

1.  $A$ is invertible ($A^{-1}$ exists).
2.  $\det(A) \neq 0$.
3.  $\text{RREF}(A) = I_n$ (the $n \times n$ identity matrix).
4.  The column vectors of $A$ are **linearly independent**.
5.  The column vectors of $A$ **span $\mathbb{R}^n$**.
6.  The column vectors of $A$ form a **basis for $\mathbb{R}^n$**.
7.  $\text{Col}(A) = \mathbb{R}^n$.
8.  $\text{Rank}(A) = n$ (matrix has **full rank**; all $n$ columns are pivot columns).
9.  $\text{Null}(A) = \{\mathbf{0}\}$ (only the trivial solution exists for $A\mathbf{x} = \mathbf{0}$).
10. $\text{Nullity}(A) = 0$ (zero free variables).
11. $A\mathbf{x} = \mathbf{b}$ has a unique solution for every $\mathbf{b} \in \mathbb{R}^n$.

---

<div style="page-break-before: always; break-before: page;"></div>

## 14. Vocabulary Glossary
Here is a master list of all the terminology introduced in this document:

*   **Linear Equation:** An equation where all variables are to the first power, and there are no products of variables or special functions.
*   **System of Linear Equations:** A set of multiple linear equations evaluated together.
*   **Consistent System:** A system that has at least one valid solution.
*   **Inconsistent System:** A system that has absolutely no valid solutions.
*   **Homogeneous System:** A system where all equations equal exactly zero ($Ax=0$).
*   **Trivial Solution:** The guaranteed solution $x=0$ in a homogeneous system.
*   **Matrix:** A rectangular array of numbers.
*   **Order of a Matrix:** The size of the matrix, read as Rows $\times$ Columns.
*   **Zero (Null) Matrix ($O$):** A matrix where every single entry is $0$.
*   **Diagonal Matrix:** A square matrix where every entry *off* the main diagonal is zero.
*   **Identity Matrix ($I$):** A diagonal matrix populated entirely with $1$s on the main diagonal. Acts as the number "1" for matrices.
*   **Transpose ($A^T$):** The operation of flipping a matrix's rows and columns over its main diagonal.
*   **Symmetric Matrix:** A square matrix that perfectly equals its own transpose ($A = A^T$).
*   **Skew-Symmetric Matrix:** A square matrix that equals the negative of its own transpose ($A = -A^T$). The main diagonal must be all zeros.
*   **Invertible (Nonsingular) Matrix:** A square matrix $A$ that possesses a valid inverse matrix $A^{-1}$, meaning $AA^{-1} = I$.
*   **Singular Matrix:** A square matrix that does not have an inverse.
*   **Elementary Row Operations (EROs):** The three legal moves used to solve systems (Scaling a row, Swapping rows, or Adding a multiple of one row to another).
*   **Elementary Matrix:** A matrix generated by applying exactly one ERO to the Identity matrix.
*   **Row-Echelon Form (REF):** A stair-step matrix format where leading entries are $1$, zeros are below the leading $1$s, and rows of all zeros are at the bottom.
*   **Reduced Row-Echelon Form (RREF):** The strictest matrix format. It meets all REF criteria, PLUS every leading $1$ is the *only* non-zero number in its entire column.
*   **Pivot (Leading 1):** The first non-zero number in a row of an REF or RREF matrix.
*   **Free Variable:** A variable in a system whose corresponding matrix column does *not* contain a pivot.
*   **Parametric Form:** The final format of equations where leading variables are defined in terms of free variables.
*   **Linear Combination:** A vector obtained by multiplying a collection of vectors by scalar constants and adding the results ($c_1 \mathbf{v}_1 + \dots + c_k \mathbf{v}_k$).
*   **Span ($\text{span}(S)$):** The set of all possible linear combinations that can be generated by a set of vectors $S$. The span of any subset is guaranteed to be a subspace.
*   **Spanning Set:** A set of vectors $S$ whose linear combinations completely cover the vector space $V$ ($\text{span}(S) = V$).
*   **Linearly Independent (LI):** A set of vectors where the vector equation $c_1 \mathbf{v}_1 + \dots + c_k \mathbf{v}_k = \mathbf{0}$ has *only* the trivial solution ($c_1 = \dots = c_k = 0$). Every vector contributes a brand-new dimension with zero redundancy.
*   **Linearly Dependent (LD):** A set of vectors where at least one vector can be expressed as a linear combination of the others (at least one non-zero scalar solves $c_1 \mathbf{v}_1 + \dots + c_k \mathbf{v}_k = \mathbf{0}$).
*   **Collinear Vectors:** Vectors that lie along the exact same 1D line through the origin (multiples of each other). For exactly 2 vectors, collinearity is identical to linear dependence.
*   **Coplanar Vectors:** Vectors that lie in the exact same 2D plane through the origin. Three vectors in $\mathbb{R}^3$ are linearly dependent if and only if they are coplanar.
*   **Basis:** A set of vectors that is both linearly independent (zero redundancy) and spans the subspace ($\text{span}(B) = V$). It serves as a minimal spanning set and defines a unique coordinate system for every vector in that subspace.
*   **Standard Basis:** The canonical basis for $\mathbb{R}^n$ consisting of standard unit vectors $\mathbf{e}_1, \dots, \mathbf{e}_n$ (such as $\hat{i} = \begin{bmatrix}1\\0\end{bmatrix}$ and $\hat{j} = \begin{bmatrix}0\\1\end{bmatrix}$ in $\mathbb{R}^2$).
*   **Null Space (Kernel):** The set of all vectors $\mathbf{x} \in \mathbb{R}^n$ that satisfy the homogeneous matrix equation $A\mathbf{x} = \mathbf{0}$. It is always a valid subspace of $\mathbb{R}^n$.
*   **Nullity:** The dimension of the null space ($\dim(\text{Null}(A))$), which is strictly equal to the number of free variables in $\text{RREF}(A)$.
*   **Column Space ($\text{Col}(A)$ or Range):** The subspace of $\mathbb{R}^m$ formed by the span of the column vectors of an $m \times n$ matrix $A$, representing all possible output vectors $A\mathbf{x}$.
*   **Rank ($\text{rank}(A)$):** The dimension of the column space of $A$ ($\dim(\text{Col}(A))$), which is strictly equal to the number of pivot columns in $\text{RREF}(A)$.
*   **Rank-Nullity Theorem (Dimension Theorem):** The fundamental conservation law stating that for any $m \times n$ matrix $A$, $\text{Rank}(A) + \text{Nullity}(A) = n$ (Pivot columns + Free columns = Total columns).
