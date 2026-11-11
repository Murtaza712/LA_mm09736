# Linear Algebra Proofs Compendium (Midterm II Master Reference)
*Comprehensive Exam Proofs: Vectors in $\mathbb{R}^n$ through Linear Transformations*

---

## Table of Contents

### Part I: Vectors, Projections, Inner Products & Cauchy-Schwarz ($\mathbb{R}^n$)
1. [Theorem 3.3.3: The Projection Theorem](#theorem-333-the-projection-theorem)
2. [Theorem 4.1.2: Properties of the Euclidean Inner Product](#theorem-412-properties-of-the-euclidean-inner-product)
3. [Theorem 4.1.3: The Cauchy-Schwarz Inequality in $\mathbb{R}^n$ (and Matrix Form)](#theorem-413-the-cauchy-schwarz-inequality-in-mathbbrn)
4. [Theorem 4.1.4: Properties of Length (Norm) in $\mathbb{R}^n$](#theorem-414-properties-of-length-norm-in-mathbbrn)
5. [Theorem 4.1.5: Properties of Distance in $\mathbb{R}^n$](#theorem-415-properties-of-distance-in-mathbbrn)
6. [Theorem 4.1.6: The Polarization Identity & Parallelogram Law](#theorem-416-the-polarization-identity-in-mathbbrn)
7. [Theorem 4.1.7: Pythagorean Theorem in $\mathbb{R}^n$](#theorem-417-pythagorean-theorem-in-mathbbrn)

### Part II: General Vector Spaces & Subspaces
8. [Theorem 5.1.1: Fundamental Vector Space Arithmetic](#theorem-511-fundamental-vector-space-arithmetic)
9. [Theorem 5.2.1: Subspace Test & Intersection vs. Union of Subspaces](#theorem-521-subspace-test--intersection-vs-union-of-subspaces)
10. [Theorem 5.2.2: Solution Space of a Homogeneous System ($A\mathbf{x} = \mathbf{0}$) is a Subspace](#theorem-522-solution-space-of-a-homogeneous-system-is-a-subspace)
11. [Theorem 5.2.3: $\text{Span}(S)$ is the Smallest Subspace Containing $S$](#theorem-523-textspans-is-the-smallest-subspace-containing-s)
12. [Theorem: The Column Space $\text{Col}(A)$ is Always a Subspace of $\mathbb{R}^m$](#theorem-the-column-space-textcola-is-always-a-subspace-of-mathbbrm)
13. [Theorem: Consistency Theorem for Linear Systems ($A\mathbf{x} = \mathbf{b}$)](#theorem-consistency-theorem-for-linear-systems-amathbfx--mathbfb)

### Part III: Linear Independence, Span, Bases & Dimension
14. [Theorem 5.3.1: The Redundancy Equivalence Theorem](#theorem-531-the-redundancy-equivalence-theorem)
15. [Theorem 5.3.2: Zero Vector and Two-Vector Dependency](#theorem-532-zero-vector-and-two-vector-dependency)
16. [Theorem: Every Non-Empty Subset of a Linearly Independent Set is Linearly Independent](#theorem-every-non-empty-subset-of-a-linearly-independent-set-is-linearly-independent)
17. [Theorem: The Plus/Minus Theorem (Extending & Trimming Sets)](#theorem-the-plusminus-theorem-extending--trimming-sets)
18. [Theorem 5.3.3 & 5.4.3: Dimension Bounds on Linear Independence and Spanning](#theorem-533--543-dimension-bounds-on-linear-independence-and-spanning)
19. [Theorem 5.4.1: Uniqueness of Basis Representation](#theorem-541-uniqueness-of-basis-representation)
20. [Theorem 5.4.5: The Half-Test for Basis (Basis Theorem in $n$-Dimensional Space)](#theorem-545-the-half-test-for-basis-basis-theorem-in-n-dimensional-space)

### Part IV: Row Space, Column Space, Rank & Nullity
21. [Theorem: Null Space & Column Linear Independence Equivalence](#theorem-null-space--column-linear-independence-equivalence)
22. [Theorems 5.5.4 & 5.5.5: Row Operations Preserve Row Space & Column Relations](#theorems-554--555-row-operations-preserve-row-space--column-relations)
23. [Theorem 5.6.1: Row Rank Equals Column Rank ($\dim(\text{Row}(A)) = \dim(\text{Col}(A))$)](#theorem-561-row-rank-equals-column-rank)
24. [Theorem 5.6.3: The Rank-Nullity Theorem for Matrices](#theorem-563-the-rank-nullity-theorem-for-matrices)

### Part V: Linear Transformations
25. [Theorem: Fundamental Properties of Linear Transformations](#theorem-fundamental-properties-of-linear-transformations)
26. [Theorem: Every Matrix Transformation $T(\mathbf{x}) = A\mathbf{x}$ is Linear](#theorem-every-matrix-transformation-tmathbfx--amathbfx-is-linear)
27. [Theorem: Standard Matrix Representation & Uniqueness ($T(\mathbf{x}) = A\mathbf{x}$)](#theorem-standard-matrix-representation--uniqueness)
28. [Theorem: Range of a Matrix Transformation Equals the Column Space ($R(T_A) = \text{Col}(A)$)](#theorem-range-of-a-matrix-transformation-equals-the-column-space)
29. [Theorem: Kernel and Range are Subspaces ($\ker(T) \subseteq V$ and $R(T) \subseteq W$)](#theorem-kernel-and-range-are-subspaces)
30. [Theorem: The Trivial Kernel Test for One-to-One Linear Transformations](#theorem-the-trivial-kernel-test-for-one-to-one-linear-transformations)
31. [Theorem: Composition of Linear Transformations is Linear & Matrix Product Rule](#theorem-composition-of-linear-transformations-is-linear--matrix-product-rule)
32. [Theorem: General Rank-Nullity Theorem & Equal-Dimension Equivalence](#theorem-general-rank-nullity-theorem--equal-dimension-equivalence)

---

# Part I: Vectors, Projections, Inner Products & Cauchy-Schwarz ($\mathbb{R}^n$)

---

## Theorem 3.3.3: The Projection Theorem

### Statement
> If $\mathbf{u}$ and $\mathbf{a}$ are vectors in $\mathbb{R}^n$ and $\mathbf{a} \neq \mathbf{0}$, then $\mathbf{u}$ can be expressed in **exactly one way** as:
> $$\mathbf{u} = \mathbf{w}_1 + \mathbf{w}_2$$
> where $\mathbf{w}_1$ is a scalar multiple of $\mathbf{a}$ (the orthogonal projection $\text{proj}_{\mathbf{a}}\mathbf{u}$) and $\mathbf{w}_2$ is orthogonal to $\mathbf{a}$:
> $$\mathbf{w}_1 = \frac{\mathbf{u} \cdot \mathbf{a}}{\|\mathbf{a}\|^2} \mathbf{a}, \qquad \mathbf{w}_2 = \mathbf{u} - \frac{\mathbf{u} \cdot \mathbf{a}}{\|\mathbf{a}\|^2} \mathbf{a}$$

### Proof

#### 1. Existence (Constructing $\mathbf{w}_1$ and $\mathbf{w}_2$)
Let $\mathbf{w}_1 = k\mathbf{a}$ for some scalar $k \in \mathbb{R}$, and define $\mathbf{w}_2 = \mathbf{u} - k\mathbf{a}$. Clearly, $\mathbf{w}_1 + \mathbf{w}_2 = \mathbf{u}$ and $\mathbf{w}_1$ is a scalar multiple of $\mathbf{a}$.

We require $\mathbf{w}_2$ to be orthogonal to $\mathbf{a}$:
$$\mathbf{w}_2 \cdot \mathbf{a} = 0$$
Substitute $\mathbf{w}_2 = \mathbf{u} - k\mathbf{a}$:
$$(\mathbf{u} - k\mathbf{a}) \cdot \mathbf{a} = 0$$
Using the distributive property of the dot product:
$$\mathbf{u} \cdot \mathbf{a} - k(\mathbf{a} \cdot \mathbf{a}) = 0$$
$$\mathbf{u} \cdot \mathbf{a} = k \|\mathbf{a}\|^2$$
Since $\mathbf{a} \neq \mathbf{0}$, we have $\|\mathbf{a}\|^2 \neq 0$, so we can divide by $\|\mathbf{a}\|^2$:
$$k = \frac{\mathbf{u} \cdot \mathbf{a}}{\|\mathbf{a}\|^2}$$
Thus, setting $\mathbf{w}_1 = \frac{\mathbf{u} \cdot \mathbf{a}}{\|\mathbf{a}\|^2}\mathbf{a}$ and $\mathbf{w}_2 = \mathbf{u} - \mathbf{w}_1$ gives a valid decomposition.

#### 2. Uniqueness
Suppose $\mathbf{u}$ can also be written as $\mathbf{u} = \mathbf{w}_1' + \mathbf{w}_2'$ where $\mathbf{w}_1' = k'\mathbf{a}$ and $\mathbf{w}_2' \cdot \mathbf{a} = 0$.
Since both decompositions sum to $\mathbf{u}$:
$$\mathbf{w}_1 + \mathbf{w}_2 = \mathbf{w}_1' + \mathbf{w}_2'$$
$$k\mathbf{a} + \mathbf{w}_2 = k'\mathbf{a} + \mathbf{w}_2' \implies (k - k')\mathbf{a} = \mathbf{w}_2' - \mathbf{w}_2$$
Take the dot product of both sides with $\mathbf{a}$:
$$(k - k')(\mathbf{a} \cdot \mathbf{a}) = (\mathbf{w}_2' - \mathbf{w}_2) \cdot \mathbf{a} = \mathbf{w}_2' \cdot \mathbf{a} - \mathbf{w}_2 \cdot \mathbf{a} = 0 - 0 = 0$$
Since $\mathbf{a} \neq \mathbf{0}$, $\mathbf{a} \cdot \mathbf{a} = \|\mathbf{a}\|^2 \neq 0$, which forces:
$$k - k' = 0 \implies k = k'$$
Hence $\mathbf{w}_1 = \mathbf{w}_1'$, and consequently $\mathbf{w}_2 = \mathbf{u} - \mathbf{w}_1 = \mathbf{u} - \mathbf{w}_1' = \mathbf{w}_2'$.

$$\blacksquare$$

---

## Theorem 4.1.2: Properties of the Euclidean Inner Product

### Statement
> If $\mathbf{u}, \mathbf{v}$, and $\mathbf{w}$ are vectors in $\mathbb{R}^n$ and $k$ is any scalar ($k \in \mathbb{R}$), then:
> * **(a) Symmetry Property:** $\mathbf{u} \cdot \mathbf{v} = \mathbf{v} \cdot \mathbf{u}$
> * **(b) Additivity / Distributive Property:** $(\mathbf{u} + \mathbf{v}) \cdot \mathbf{w} = \mathbf{u} \cdot \mathbf{w} + \mathbf{v} \cdot \mathbf{w}$
> * **(c) Homogeneity / Scalar Property:** $(k\mathbf{u}) \cdot \mathbf{v} = k(\mathbf{u} \cdot \mathbf{v})$
> * **(d) Positivity Property:** $\mathbf{v} \cdot \mathbf{v} \ge 0$. Further, $\mathbf{v} \cdot \mathbf{v} = 0$ if and only if $\mathbf{v} = \mathbf{0}$.

Let the vectors in $\mathbb{R}^n$ be denoted by their components:
$$\mathbf{u} = (u_1, u_2, \dots, u_n), \quad \mathbf{v} = (v_1, v_2, \dots, v_n), \quad \mathbf{w} = (w_1, w_2, \dots, w_n)$$
By definition, the Euclidean inner product (dot product) is:
$$\mathbf{u} \cdot \mathbf{v} = u_1 v_1 + u_2 v_2 + \dots + u_n v_n$$

### Proof of Part (a): $\mathbf{u} \cdot \mathbf{v} = \mathbf{v} \cdot \mathbf{u}$ (Symmetry)
By definition of the Euclidean inner product:
$$\mathbf{u} \cdot \mathbf{v} = u_1 v_1 + u_2 v_2 + \dots + u_n v_n$$
Since multiplication of real numbers is commutative ($u_i v_i = v_i u_i$ for all real numbers $u_i, v_i$):
$$= v_1 u_1 + v_2 u_2 + \dots + v_n u_n = \mathbf{v} \cdot \mathbf{u}$$

### Proof of Part (b): $(\mathbf{u} + \mathbf{v}) \cdot \mathbf{w} = \mathbf{u} \cdot \mathbf{w} + \mathbf{v} \cdot \mathbf{w}$ (Additivity)
First, compute the vector addition:
$$\mathbf{u} + \mathbf{v} = (u_1 + v_1, \; u_2 + v_2, \; \dots, \; u_n + v_n)$$
Compute the inner product with $\mathbf{w}$:
$$(\mathbf{u} + \mathbf{v}) \cdot \mathbf{w} = (u_1 + v_1)w_1 + (u_2 + v_2)w_2 + \dots + (u_n + v_n)w_n$$
By the distributive property of real numbers ($(u_i + v_i)w_i = u_i w_i + v_i w_i$):
$$= (u_1 w_1 + v_1 w_1) + (u_2 w_2 + v_2 w_2) + \dots + (u_n w_n + v_n w_n)$$
Regrouping terms:
$$= (u_1 w_1 + u_2 w_2 + \dots + u_n w_n) + (v_1 w_1 + v_2 w_2 + \dots + v_n w_n) = \mathbf{u} \cdot \mathbf{w} + \mathbf{v} \cdot \mathbf{w}$$

### Proof of Part (c): $(k\mathbf{u}) \cdot \mathbf{v} = k(\mathbf{u} \cdot \mathbf{v})$ (Homogeneity)
Compute scalar multiplication: $k\mathbf{u} = (k u_1, \; k u_2, \; \dots, \; k u_n)$.
$$(k\mathbf{u}) \cdot \mathbf{v} = (k u_1)v_1 + (k u_2)v_2 + \dots + (k u_n)v_n$$
By associativity of real multiplication ($(k u_i)v_i = k(u_i v_i)$):
$$= k(u_1 v_1) + k(u_2 v_2) + \dots + k(u_n v_n) = k(u_1 v_1 + u_2 v_2 + \dots + u_n v_n) = k(\mathbf{u} \cdot \mathbf{v})$$

### Proof of Part (d): $\mathbf{v} \cdot \mathbf{v} \ge 0$, and $\mathbf{v} \cdot \mathbf{v} = 0 \iff \mathbf{v} = \mathbf{0}$ (Positivity)
$$\mathbf{v} \cdot \mathbf{v} = v_1^2 + v_2^2 + \dots + v_n^2$$
1. **Non-negativity:** Since $v_i^2 \ge 0$ for every real number $v_i$, the sum of squares is $\ge 0$.
2. **Zero condition:** $v_1^2 + v_2^2 + \dots + v_n^2 = 0 \iff v_1 = v_2 = \dots = v_n = 0 \iff \mathbf{v} = \mathbf{0}$.

$$\blacksquare$$

---

## Theorem 4.1.3: The Cauchy-Schwarz Inequality in $\mathbb{R}^n$

### Statement
> If $\mathbf{u}$ and $\mathbf{v}$ are vectors in $\mathbb{R}^n$, then:
> $$|\mathbf{u} \cdot \mathbf{v}| \le \|\mathbf{u}\| \|\mathbf{v}\|$$
> Moreover, equality holds ($|\mathbf{u} \cdot \mathbf{v}| = \|\mathbf{u}\| \|\mathbf{v}\|$) if and only if one vector is a scalar multiple of the other (i.e., the vectors are collinear / linearly dependent).

### Proof (via Non-Negative Quadratic Polynomial)

**Case 1: $\mathbf{u} = \mathbf{0}$**
If $\mathbf{u} = \mathbf{0}$, then $\mathbf{u} \cdot \mathbf{v} = \mathbf{0} \cdot \mathbf{v} = 0$ and $\|\mathbf{u}\| = 0$.
Both sides equal $0$: $0 \le 0$, so the inequality (and equality) holds trivially.

**Case 2: $\mathbf{u} \neq \mathbf{0}$**
Let $t \in \mathbb{R}$ be any real scalar, and consider the vector $t\mathbf{u} + \mathbf{v}$.
By the positivity property of the Euclidean inner product (Theorem 4.1.2(d)):
$$p(t) = \|t\mathbf{u} + \mathbf{v}\|^2 = (t\mathbf{u} + \mathbf{v}) \cdot (t\mathbf{u} + \mathbf{v}) \ge 0 \quad \text{for all } t \in \mathbb{R}$$
Expanding using the additivity, homogeneity, and symmetry properties (Theorem 4.1.2):
$$p(t) = (\mathbf{u} \cdot \mathbf{u})t^2 + 2(\mathbf{u} \cdot \mathbf{v})t + (\mathbf{v} \cdot \mathbf{v}) \ge 0$$
Define constants $a = \mathbf{u} \cdot \mathbf{u} = \|\mathbf{u}\|^2$, $b = 2(\mathbf{u} \cdot \mathbf{v})$, and $c = \mathbf{v} \cdot \mathbf{v} = \|\mathbf{v}\|^2$.
Since $\mathbf{u} \neq \mathbf{0}$, $a = \|\mathbf{u}\|^2 > 0$. The function $p(t) = at^2 + bt + c$ is an upward-opening quadratic polynomial that is **never negative** ($p(t) \ge 0$ for all $t \in \mathbb{R}$).

Therefore, $p(t) = 0$ has **at most one real root** (either zero roots or one repeated root), which means its discriminant $\Delta = b^2 - 4ac$ must satisfy $\Delta \le 0$:
$$b^2 - 4ac \le 0$$
$$\big(2(\mathbf{u} \cdot \mathbf{v})\big)^2 - 4\|\mathbf{u}\|^2\|\mathbf{v}\|^2 \le 0$$
$$4(\mathbf{u} \cdot \mathbf{v})^2 \le 4\|\mathbf{u}\|^2\|\mathbf{v}\|^2$$
Dividing by $4$:
$$(\mathbf{u} \cdot \mathbf{v})^2 \le \|\mathbf{u}\|^2\|\mathbf{v}\|^2$$
Taking the non-negative square root of both sides:
$$|\mathbf{u} \cdot \mathbf{v}| \le \|\mathbf{u}\| \|\mathbf{v}\|$$

#### Equality Condition:
When $\mathbf{u} \neq \mathbf{0}$, equality holds if and only if $\Delta = 0$, which means there exists a real root $t_0$ such that $p(t_0) = \|t_0\mathbf{u} + \mathbf{v}\|^2 = 0$.
By positivity, $\|t_0\mathbf{u} + \mathbf{v}\| = 0 \iff t_0\mathbf{u} + \mathbf{v} = \mathbf{0} \iff \mathbf{v} = -t_0\mathbf{u}$ (a scalar multiple of $\mathbf{u}$).

$$\blacksquare$$

### Classic Exam Application: Matrix Cauchy-Schwarz Inequality
> **Problem:** If $\mathbf{u}, \mathbf{v}$ are $n \times 1$ column vectors and $A$ is an $n \times n$ matrix, prove:
> $$(\mathbf{v}^T A^T A \mathbf{u})^2 \le (\mathbf{u}^T A^T A \mathbf{u})(\mathbf{v}^T A^T A \mathbf{v})$$

<mark style="background-color: lightgreen;">Proof:</mark>
Let $\mathbf{x} = A\mathbf{u}$ and $\mathbf{y} = A\mathbf{v}$. Notice that $\mathbf{x} \cdot \mathbf{y} = \mathbf{y}^T \mathbf{x} = (A\mathbf{v})^T (A\mathbf{u}) = \mathbf{v}^T A^T A \mathbf{u}$.
By the Cauchy-Schwarz Inequality in $\mathbb{R}^n$ ($|\mathbf{x} \cdot \mathbf{y}|^2 \le \|\mathbf{x}\|^2 \|\mathbf{y}\|^2$):
$$(\mathbf{x} \cdot \mathbf{y})^2 \le (\mathbf{x} \cdot \mathbf{x})(\mathbf{y} \cdot \mathbf{y})$$
Substituting $\mathbf{x} = A\mathbf{u}$ and $\mathbf{y} = A\mathbf{v}$ back in:
$$\mathbf{x} \cdot \mathbf{x} = (A\mathbf{u})^T(A\mathbf{u}) = \mathbf{u}^T A^T A \mathbf{u}, \qquad \mathbf{y} \cdot \mathbf{y} = (A\mathbf{v})^T(A\mathbf{v}) = \mathbf{v}^T A^T A \mathbf{v}$$
$$(\mathbf{v}^T A^T A \mathbf{u})^2 \le (\mathbf{u}^T A^T A \mathbf{u})(\mathbf{v}^T A^T A \mathbf{v}) \quad \blacksquare$$

---

## Theorem 4.1.4: Properties of Length (Norm) in $\mathbb{R}^n$

### Statement
> If $\mathbf{u}$ and $\mathbf{v}$ are vectors in $\mathbb{R}^n$ and $k$ is any scalar ($k \in \mathbb{R}$), then:
> * **(a) Non-negativity:** $\|\mathbf{u}\| \ge 0$
> * **(b) Zero Condition:** $\|\mathbf{u}\| = 0$ if and only if $\mathbf{u} = \mathbf{0}$
> * **(c) Homogeneity:** $\|k\mathbf{u}\| = |k| \|\mathbf{u}\|$
> * **(d) Triangle Inequality:** $\|\mathbf{u} + \mathbf{v}\| \le \|\mathbf{u}\| + \|\mathbf{v}\|$

Let $\mathbf{u} = (u_1, u_2, \dots, u_n)$ and $\mathbf{v} = (v_1, v_2, \dots, v_n)$. 
By definition, $\|\mathbf{u}\| = \sqrt{\mathbf{u} \cdot \mathbf{u}} = \sqrt{u_1^2 + u_2^2 + \dots + u_n^2}$.

### Proof of Part (a): $\|\mathbf{u}\| \ge 0$
Since $u_i^2 \ge 0$ for each $i$, $u_1^2 + \dots + u_n^2 \ge 0$. The principal square root of a non-negative real number is always non-negative, so $\|\mathbf{u}\| \ge 0$.

### Proof of Part (b): $\|\mathbf{u}\| = 0 \iff \mathbf{u} = \mathbf{0}$
$$\|\mathbf{u}\| = 0 \iff \sqrt{u_1^2 + \dots + u_n^2} = 0 \iff u_1^2 + \dots + u_n^2 = 0 \iff u_1 = \dots = u_n = 0 \iff \mathbf{u} = \mathbf{0}$$

### Proof of Part (c): $\|k\mathbf{u}\| = |k| \|\mathbf{u}\|$
$$\|k\mathbf{u}\| = \sqrt{(ku_1)^2 + \dots + (ku_n)^2} = \sqrt{k^2(u_1^2 + \dots + u_n^2)} = \sqrt{k^2}\sqrt{u_1^2 + \dots + u_n^2} = |k|\|\mathbf{u}\|$$

### Proof of Part (d): $\|\mathbf{u} + \mathbf{v}\| \le \|\mathbf{u}\| + \|\mathbf{v}\|$ (The Triangle Inequality)
Start with the left-hand side squared using $\|\mathbf{x}\|^2 = \mathbf{x} \cdot \mathbf{x}$:
$$\|\mathbf{u} + \mathbf{v}\|^2 = (\mathbf{u} + \mathbf{v}) \cdot (\mathbf{u} + \mathbf{v}) = \|\mathbf{u}\|^2 + 2(\mathbf{u} \cdot \mathbf{v}) + \|\mathbf{v}\|^2$$
Since any real number is $\le$ its absolute value ($x \le |x|$):
$$\le \|\mathbf{u}\|^2 + 2|\mathbf{u} \cdot \mathbf{v}| + \|\mathbf{v}\|^2$$
Apply the **Cauchy-Schwarz Inequality** (Theorem 4.1.3, $|\mathbf{u} \cdot \mathbf{v}| \le \|\mathbf{u}\| \|\mathbf{v}\|$):
$$\le \|\mathbf{u}\|^2 + 2\|\mathbf{u}\| \|\mathbf{v}\| + \|\mathbf{v}\|^2 = (\|\mathbf{u}\| + \|\mathbf{v}\|)^2$$
Thus $\|\mathbf{u} + \mathbf{v}\|^2 \le (\|\mathbf{u}\| + \|\mathbf{v}\|)^2$. Since both sides are non-negative, taking square roots yields:
$$\|\mathbf{u} + \mathbf{v}\| \le \|\mathbf{u}\| + \|\mathbf{v}\|$$

$$\blacksquare$$

---

## Theorem 4.1.5: Properties of Distance in $\mathbb{R}^n$

### Statement
> If $\mathbf{u}, \mathbf{v}$, and $\mathbf{w}$ are vectors in $\mathbb{R}^n$, and $d(\mathbf{u}, \mathbf{v}) = \|\mathbf{u} - \mathbf{v}\|$, then:
> * **(a) Non-negativity:** $d(\mathbf{u}, \mathbf{v}) \ge 0$
> * **(b) Zero Condition / Identity:** $d(\mathbf{u}, \mathbf{v}) = 0 \iff \mathbf{u} = \mathbf{v}$
> * **(c) Symmetry:** $d(\mathbf{u}, \mathbf{v}) = d(\mathbf{v}, \mathbf{u})$
> * **(d) Triangle Inequality:** $d(\mathbf{u}, \mathbf{v}) \le d(\mathbf{u}, \mathbf{w}) + d(\mathbf{w}, \mathbf{v})$

### Proof of Part (a): $d(\mathbf{u}, \mathbf{v}) \ge 0$
Let $\mathbf{x} = \mathbf{u} - \mathbf{v}$. By Theorem 4.1.4(a), $\|\mathbf{x}\| \ge 0 \implies d(\mathbf{u}, \mathbf{v}) = \|\mathbf{u} - \mathbf{v}\| \ge 0$.

### Proof of Part (b): $d(\mathbf{u}, \mathbf{v}) = 0 \iff \mathbf{u} = \mathbf{v}$
By Theorem 4.1.4(b), $d(\mathbf{u}, \mathbf{v}) = 0 \iff \|\mathbf{u} - \mathbf{v}\| = 0 \iff \mathbf{u} - \mathbf{v} = \mathbf{0} \iff \mathbf{u} = \mathbf{v}$.

### Proof of Part (c): $d(\mathbf{u}, \mathbf{v}) = d(\mathbf{v}, \mathbf{u})$
$$d(\mathbf{u}, \mathbf{v}) = \|\mathbf{u} - \mathbf{v}\| = \|(-1)(\mathbf{v} - \mathbf{u})\| \overset{\text{Thm 4.1.4(c)}}{=} |-1| \|\mathbf{v} - \mathbf{u}\| = \|\mathbf{v} - \mathbf{u}\| = d(\mathbf{v}, \mathbf{u})$$

### Proof of Part (d): $d(\mathbf{u}, \mathbf{v}) \le d(\mathbf{u}, \mathbf{w}) + d(\mathbf{w}, \mathbf{v})$
Add and subtract $\mathbf{w}$ inside the norm:
$$d(\mathbf{u}, \mathbf{v}) = \|\mathbf{u} - \mathbf{v}\| = \|(\mathbf{u} - \mathbf{w}) + (\mathbf{w} - \mathbf{v})\|$$
By the Triangle Inequality for norms (Theorem 4.1.4(d)):
$$\|(\mathbf{u} - \mathbf{w}) + (\mathbf{w} - \mathbf{v})\| \le \|\mathbf{u} - \mathbf{w}\| + \|\mathbf{w} - \mathbf{v}\| = d(\mathbf{u}, \mathbf{w}) + d(\mathbf{w}, \mathbf{v})$$

$$\blacksquare$$

---

## Theorem 4.1.6: The Polarization Identity in $\mathbb{R}^n$

### Statement
> If $\mathbf{u}$ and $\mathbf{v}$ are vectors in $\mathbb{R}^n$ with the Euclidean inner product, then:
> $$\mathbf{u} \cdot \mathbf{v} = \frac{1}{4} \|\mathbf{u} + \mathbf{v}\|^2 - \frac{1}{4} \|\mathbf{u} - \mathbf{v}\|^2$$

### Proof
Expand both squared norms using $\|\mathbf{x}\|^2 = \mathbf{x} \cdot \mathbf{x}$ and Theorem 4.1.2:
$$\|\mathbf{u} + \mathbf{v}\|^2 = (\mathbf{u} + \mathbf{v}) \cdot (\mathbf{u} + \mathbf{v}) = \|\mathbf{u}\|^2 + 2(\mathbf{u} \cdot \mathbf{v}) + \|\mathbf{v}\|^2 \quad \text{--- (1)}$$
$$\|\mathbf{u} - \mathbf{v}\|^2 = (\mathbf{u} - \mathbf{v}) \cdot (\mathbf{u} - \mathbf{v}) = \|\mathbf{u}\|^2 - 2(\mathbf{u} \cdot \mathbf{v}) + \|\mathbf{v}\|^2 \quad \text{--- (2)}$$
Subtract Equation (2) from Equation (1):
$$\|\mathbf{u} + \mathbf{v}\|^2 - \|\mathbf{u} - \mathbf{v}\|^2 = 4(\mathbf{u} \cdot \mathbf{v})$$
Dividing by $4$ yields:
$$\mathbf{u} \cdot \mathbf{v} = \frac{1}{4} \|\mathbf{u} + \mathbf{v}\|^2 - \frac{1}{4} \|\mathbf{u} - \mathbf{v}\|^2$$

$$\blacksquare$$

* **Related Identity — The Parallelogram Equation:** Adding (1) and (2) yields:
  $$\|\mathbf{u} + \mathbf{v}\|^2 + \|\mathbf{u} - \mathbf{v}\|^2 = 2\|\mathbf{u}\|^2 + 2\|\mathbf{v}\|^2$$

---

## Theorem 4.1.7: Pythagorean Theorem in $\mathbb{R}^n$

### Statement
> If $\mathbf{u}$ and $\mathbf{v}$ are orthogonal vectors in $\mathbb{R}^n$ ($\mathbf{u} \cdot \mathbf{v} = 0$), then:
> $$\|\mathbf{u} + \mathbf{v}\|^2 = \|\mathbf{u}\|^2 + \|\mathbf{v}\|^2$$

### Proof
$$\|\mathbf{u} + \mathbf{v}\|^2 = (\mathbf{u} + \mathbf{v}) \cdot (\mathbf{u} + \mathbf{v}) = \|\mathbf{u}\|^2 + 2(\mathbf{u} \cdot \mathbf{v}) + \|\mathbf{v}\|^2$$
Since $\mathbf{u} \perp \mathbf{v}$, by definition $\mathbf{u} \cdot \mathbf{v} = 0$:
$$\|\mathbf{u} + \mathbf{v}\|^2 = \|\mathbf{u}\|^2 + 2(0) + \|\mathbf{v}\|^2 = \|\mathbf{u}\|^2 + \|\mathbf{v}\|^2$$

$$\blacksquare$$

---

# Part II: General Vector Spaces & Subspaces

---

## Theorem 5.1.1: Fundamental Vector Space Arithmetic

### Statement
> Let $V$ be any vector space, $\mathbf{u} \in V$, and $k \in \mathbb{R}$. Using only the 10 vector space axioms, prove:
> * **(a)** $0\mathbf{u} = \mathbf{0}$
> * **(b)** $k\mathbf{0} = \mathbf{0}$
> * **(c)** $(-1)\mathbf{u} = -\mathbf{u}$
> * **(d)** If $k\mathbf{u} = \mathbf{0}$, then $k = 0$ or $\mathbf{u} = \mathbf{0}$.

### Proofs
* **(a) Proof of $0\mathbf{u} = \mathbf{0}$:**
  Using the scalar distributive axiom (Axiom 8) with $0 + 0 = 0$:
  $$0\mathbf{u} = (0 + 0)\mathbf{u} = 0\mathbf{u} + 0\mathbf{u}$$
  Add the additive inverse $-(0\mathbf{u})$ (Axiom 5) to both sides:
  $$0\mathbf{u} + \big(-(0\mathbf{u})\big) = (0\mathbf{u} + 0\mathbf{u}) + \big(-(0\mathbf{u})\big)$$
  Using associativity (Axiom 3) and additive identity (Axiom 4):
  $$\mathbf{0} = 0\mathbf{u} + \mathbf{0} \implies \mathbf{0} = 0\mathbf{u}$$

* **(b) Proof of $k\mathbf{0} = \mathbf{0}$:**
  Using $\mathbf{0} + \mathbf{0} = \mathbf{0}$ and Axiom 7:
  $$k\mathbf{0} = k(\mathbf{0} + \mathbf{0}) = k\mathbf{0} + k\mathbf{0}$$
  Adding $-(k\mathbf{0})$ to both sides yields $\mathbf{0} = k\mathbf{0}$.

* **(c) Proof of $(-1)\mathbf{u} = -\mathbf{u}$:**
  We show that $\mathbf{u} + (-1)\mathbf{u} = \mathbf{0}$:
  $$\mathbf{u} + (-1)\mathbf{u} \overset{\text{Ax 10}}{=} 1\mathbf{u} + (-1)\mathbf{u} \overset{\text{Ax 8}}{=} (1 + (-1))\mathbf{u} = 0\mathbf{u} \overset{\text{Part (a)}}{=} \mathbf{0}$$
  Since adding $(-1)\mathbf{u}$ to $\mathbf{u}$ gives $\mathbf{0}$, and the additive inverse of $\mathbf{u}$ is unique, $(-1)\mathbf{u} = -\mathbf{u}$.

* **(d) Proof of Zero-Product Property:**
  Assume $k\mathbf{u} = \mathbf{0}$. If $k = 0$, the statement holds. Suppose $k \neq 0$; then $\frac{1}{k} \in \mathbb{R}$ exists. Multiply both sides by $\frac{1}{k}$:
  $$\frac{1}{k}(k\mathbf{u}) = \frac{1}{k}\mathbf{0}$$
  $$\left(\frac{1}{k} \cdot k\right)\mathbf{u} = \mathbf{0} \quad (\text{by Axiom 9 and Part (b)})$$
  $$1\mathbf{u} = \mathbf{0} \implies \mathbf{u} = \mathbf{0} \quad (\text{by Axiom 10})$$

$$\blacksquare$$

---

## Theorem 5.2.1: Subspace Test & Intersection vs. Union of Subspaces

### Statement (The Subspace Test)
> A non-empty subset $W$ of a vector space $V$ is a **subspace** of $V$ if and only if:
> 1. **Contains Zero (Non-empty anchor):** $\mathbf{0} \in W$
> 2. **Closed under Vector Addition:** If $\mathbf{u}, \mathbf{v} \in W$, then $\mathbf{u} + \mathbf{v} \in W$
> 3. **Closed under Scalar Multiplication:** If $k \in \mathbb{R}$ and $\mathbf{u} \in W$, then $k\mathbf{u} \in W$

### Proof: The Intersection of Two Subspaces is Always a Subspace
> **Proposition:** If $W_1$ and $W_2$ are subspaces of a vector space $V$, then their intersection $W_1 \cap W_2$ is also a subspace of $V$. *(However, their union $W_1 \cup W_2$ is NOT a subspace in general).*

1. **Zero Vector ($\mathbf{0} \in W_1 \cap W_2$):**
   Since $W_1$ and $W_2$ are both subspaces of $V$, $\mathbf{0} \in W_1$ and $\mathbf{0} \in W_2$. By definition of set intersection, $\mathbf{0} \in W_1 \cap W_2$.
2. **Closed under Addition:**
   Let $\mathbf{u}, \mathbf{v} \in W_1 \cap W_2$. Then:
   * $\mathbf{u}, \mathbf{v} \in W_1 \implies \mathbf{u} + \mathbf{v} \in W_1$ (since $W_1$ is a subspace).
   * $\mathbf{u}, \mathbf{v} \in W_2 \implies \mathbf{u} + \mathbf{v} \in W_2$ (since $W_2$ is a subspace).
   Since $\mathbf{u} + \mathbf{v}$ belongs to both $W_1$ and $W_2$, $\mathbf{u} + \mathbf{v} \in W_1 \cap W_2$.
3. **Closed under Scalar Multiplication:**
   Let $\mathbf{u} \in W_1 \cap W_2$ and $k \in \mathbb{R}$.
   * $\mathbf{u} \in W_1 \implies k\mathbf{u} \in W_1$, and $\mathbf{u} \in W_2 \implies k\mathbf{u} \in W_2$.
   Hence $k\mathbf{u} \in W_1 \cap W_2$.

Therefore, $W_1 \cap W_2$ is a valid subspace of $V$. $\blacksquare$

* **Why Union Fails (Counterexample):** In $\mathbb{R}^2$, let $W_1 = \text{the } x\text{-axis}$ and $W_2 = \text{the } y\text{-axis}$. Both are subspaces. Then $(1, 0) \in W_1 \cup W_2$ and $(0, 1) \in W_1 \cup W_2$, yet their sum $(1, 0) + (0, 1) = (1, 1)$ lies on neither axis, so $(1, 1) \notin W_1 \cup W_2$. *(Wait: $W_1 \cup W_2$ is a subspace if and only if $W_1 \subseteq W_2$ or $W_2 \subseteq W_1$).*

---

## Theorem 5.2.2: Solution Space of a Homogeneous System is a Subspace

### Statement
> If $A\mathbf{x} = \mathbf{0}$ is a homogeneous linear system of $m$ equations in $n$ unknowns, then the set of solution vectors $W = \{\mathbf{x} \in \mathbb{R}^n \mid A\mathbf{x} = \mathbf{0}\}$ (the Null Space of $A$) is a subspace of $\mathbb{R}^n$.

### Proof
Let $W = \{\mathbf{x} \in \mathbb{R}^n \mid A\mathbf{x} = \mathbf{0}\}$. We verify the three subspace conditions:
1. **Non-empty / Contains the Zero Vector ($\mathbf{0} \in W$):**
   Since $A\mathbf{0} = \mathbf{0}$, the zero vector $\mathbf{0} \in \mathbb{R}^n$ is always a solution, so $\mathbf{0} \in W$.
2. **Closure under Vector Addition:**
   Let $\mathbf{x}, \mathbf{x}' \in W$, so $A\mathbf{x} = \mathbf{0}$ and $A\mathbf{x}' = \mathbf{0}$.
   $$A(\mathbf{x} + \mathbf{x}') = A\mathbf{x} + A\mathbf{x}' = \mathbf{0} + \mathbf{0} = \mathbf{0}$$
   Thus $\mathbf{x} + \mathbf{x}' \in W$.
3. **Closure under Scalar Multiplication:**
   Let $\mathbf{x} \in W$ (so $A\mathbf{x} = \mathbf{0}$) and let $k \in \mathbb{R}$.
   $$A(k\mathbf{x}) = k(A\mathbf{x}) = k(\mathbf{0}) = \mathbf{0}$$
   Thus $k\mathbf{x} \in W$.

Since $W$ contains $\mathbf{0}$ and is closed under addition and scalar multiplication, **$W$ is a subspace of $\mathbb{R}^n$**.

$$\blacksquare$$

* **Non-Homogeneous Trap ($A\mathbf{x} = \mathbf{b}$ with $\mathbf{b} \neq \mathbf{0}$):** NEVER a subspace because $A\mathbf{0} = \mathbf{0} \neq \mathbf{b}$ ($\mathbf{0}$ is missing).

---

## Theorem 5.2.3: $\text{Span}(S)$ is the Smallest Subspace Containing $S$

### Statement
> If $S = \{\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_k\}$ is a set of vectors in a vector space $V$, then:
> * **(a)** The set $W = \text{span}(S)$ is a subspace of $V$.
> * **(b)** $W$ is the *smallest* subspace of $V$ that contains $S$; that is, any other subspace $W'$ of $V$ containing $S$ must satisfy $W \subseteq W'$.

### Proof
* **Part (a): $W = \text{span}(S)$ is a subspace of $V$**
  1. **Zero Vector:** Setting $c_1 = c_2 = \dots = c_k = 0$ gives $\mathbf{0} = 0\mathbf{v}_1 + 0\mathbf{v}_2 + \dots + 0\mathbf{v}_k \in \text{span}(S) = W$.
  2. **Closed under Addition:** Let $\mathbf{u} = \sum_{i=1}^k c_i \mathbf{v}_i$ and $\mathbf{w} = \sum_{i=1}^k d_i \mathbf{v}_i$ be in $W$. Then:
     $$\mathbf{u} + \mathbf{w} = (c_1 + d_1)\mathbf{v}_1 + \dots + (c_k + d_k)\mathbf{v}_k$$
     Since each $c_i + d_i \in \mathbb{R}$, $\mathbf{u} + \mathbf{w}$ is a linear combination of vectors in $S$, so $\mathbf{u} + \mathbf{w} \in W$.
  3. **Closed under Scalar Multiplication:** Let $\alpha \in \mathbb{R}$ and $\mathbf{u} = \sum_{i=1}^k c_i \mathbf{v}_i \in W$. Then:
     $$\alpha\mathbf{u} = (\alpha c_1)\mathbf{v}_1 + \dots + (\alpha c_k)\mathbf{v}_k \in W$$
  Thus $W = \text{span}(S)$ is a subspace of $V$.

* **Part (b): $W$ is the smallest subspace containing $S$**
  First, each $\mathbf{v}_j \in W$ (set $c_j = 1$ and all other $c_i = 0$), so $S \subseteq W$.
  Now let $W'$ be *any* subspace of $V$ such that $S \subseteq W'$. That means $\mathbf{v}_1, \dots, \mathbf{v}_k \in W'$.
  Because $W'$ is a subspace, it is closed under scalar multiplication and addition. Therefore, for any scalars $c_1, \dots, c_k \in \mathbb{R}$, the linear combination:
  $$c_1 \mathbf{v}_1 + c_2 \mathbf{v}_2 + \dots + c_k \mathbf{v}_k \in W'$$
  Since every element of $W = \text{span}(S)$ has this form, $W \subseteq W'$.

$$\blacksquare$$

---

## Theorem: The Column Space $\text{Col}(A)$ is Always a Subspace of $\mathbb{R}^m$

### Statement
> For any $m \times n$ matrix $A$, the column space $\text{Col}(A) = \{A\mathbf{x} \mid \mathbf{x} \in \mathbb{R}^n\}$ is a valid subspace of $\mathbb{R}^m$.

### Proof
1. **Zero Vector ($\mathbf{0}_m \in \text{Col}(A)$):**
   Choose $\mathbf{x} = \mathbf{0}_n \in \mathbb{R}^n$. Since $A\mathbf{0}_n = \mathbf{0}_m$, $\mathbf{0}_m \in \text{Col}(A)$.
2. **Closed under Addition:**
   Let $\mathbf{u}, \mathbf{v} \in \text{Col}(A)$. Then there exist $\mathbf{x}_1, \mathbf{x}_2 \in \mathbb{R}^n$ such that $\mathbf{u} = A\mathbf{x}_1$ and $\mathbf{v} = A\mathbf{x}_2$.
   $$\mathbf{u} + \mathbf{v} = A\mathbf{x}_1 + A\mathbf{x}_2 = A(\mathbf{x}_1 + \mathbf{x}_2)$$
   Since $(\mathbf{x}_1 + \mathbf{x}_2) \in \mathbb{R}^n$, $\mathbf{u} + \mathbf{v} \in \text{Col}(A)$.
3. **Closed under Scalar Multiplication:**
   Let $\mathbf{u} = A\mathbf{x}_1 \in \text{Col}(A)$ and $c \in \mathbb{R}$.
   $$c\mathbf{u} = c(A\mathbf{x}_1) = A(c\mathbf{x}_1)$$
   Since $c\mathbf{x}_1 \in \mathbb{R}^n$, $c\mathbf{u} \in \text{Col}(A)$.

$$\blacksquare$$

---

## Theorem: Consistency Theorem for Linear Systems ($A\mathbf{x} = \mathbf{b}$)

### Statement
> A system of linear equations $A\mathbf{x} = \mathbf{b}$ is **consistent** if and only if the vector $\mathbf{b}$ is in the column space of $A$:
> $$A\mathbf{x} = \mathbf{b} \text{ is consistent} \iff \mathbf{b} \in \text{Col}(A)$$

### Proof (Bidirectional $\iff$)
Let $A = \begin{bmatrix} \mathbf{c}_1 & \mathbf{c}_2 & \cdots & \mathbf{c}_n \end{bmatrix}$ be $m \times n$ with $\mathbf{c}_j \in \mathbb{R}^m$, and $\mathbf{x} = \begin{bmatrix} x_1 & \dots & x_n \end{bmatrix}^T \in \mathbb{R}^n$.
By definition of matrix multiplication:
$$A\mathbf{x} = x_1 \mathbf{c}_1 + x_2 \mathbf{c}_2 + \dots + x_n \mathbf{c}_n \quad \text{--- (Eq. 1)}$$

* **Forward Direction ($\implies$):** Assume $A\mathbf{x} = \mathbf{b}$ is consistent.
  There exists at least one vector $\mathbf{x} \in \mathbb{R}^n$ such that $A\mathbf{x} = \mathbf{b}$. By Eq. 1, $x_1\mathbf{c}_1 + \dots + x_n\mathbf{c}_n = \mathbf{b}$. Thus $\mathbf{b}$ is a linear combination of the columns of $A$, meaning $\mathbf{b} \in \text{span}\{\mathbf{c}_1, \dots, \mathbf{c}_n\} = \text{Col}(A)$.

* **Backward Direction ($\impliedby$):** Assume $\mathbf{b} \in \text{Col}(A)$.
  By definition of column space, there exist scalars $s_1, \dots, s_n \in \mathbb{R}$ such that $s_1\mathbf{c}_1 + \dots + s_n\mathbf{c}_n = \mathbf{b}$. Defining $\mathbf{s} = \begin{bmatrix} s_1 & \dots & s_n \end{bmatrix}^T \in \mathbb{R}^n$, Eq. 1 gives $A\mathbf{s} = \mathbf{b}$. Thus the system has a solution and is consistent.

$$\blacksquare$$

---

# Part III: Linear Independence, Span, Bases & Dimension

---

## Theorem 5.3.1: The Redundancy Equivalence Theorem

### Statement
> A set $S = \{\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_k\}$ with $k \ge 2$ vectors is **linearly dependent** if and only if at least one vector in $S$ is expressible as a linear combination of the other vectors in $S$.

### Proof (Bidirectional $\iff$)
* **Direction 1 ($\impliedby$): Redundancy $\implies$ Linear Dependence**
  Suppose at least one vector in $S$ (say $\mathbf{v}_1$, without loss of generality) can be written as a linear combination of the others:
  $$\mathbf{v}_1 = a_2\mathbf{v}_2 + a_3\mathbf{v}_3 + \dots + a_k\mathbf{v}_k$$
  Rearranging all terms to one side:
  $$(-1)\mathbf{v}_1 + a_2\mathbf{v}_2 + a_3\mathbf{v}_3 + \dots + a_k\mathbf{v}_k = \mathbf{0}$$
  Since the coefficient of $\mathbf{v}_1$ is $-1 \neq 0$, this is a non-trivial solution to $\sum c_i\mathbf{v}_i = \mathbf{0}$. Hence $S$ is linearly dependent.

* **Direction 2 ($\implies$): Linear Dependence $\implies$ Redundancy**
  Suppose $S$ is linearly dependent. Then there exist scalars $c_1, \dots, c_k$, **not all zero**, such that:
  $$c_1\mathbf{v}_1 + c_2\mathbf{v}_2 + \dots + c_k\mathbf{v}_k = \mathbf{0}$$
  Since not all $c_i$ are zero, pick an index with a non-zero scalar (without loss of generality, say $c_1 \neq 0$). Isolate $c_1\mathbf{v}_1$ and divide by $c_1$:
  $$c_1\mathbf{v}_1 = -c_2\mathbf{v}_2 - \dots - c_k\mathbf{v}_k$$
  $$\mathbf{v}_1 = \left(-\frac{c_2}{c_1}\right)\mathbf{v}_2 + \dots + \left(-\frac{c_k}{c_1}\right)\mathbf{v}_k$$
  Thus $\mathbf{v}_1$ is expressible as a linear combination of the remaining vectors.

$$\blacksquare$$

---

## Theorem 5.3.2: Zero Vector and Two-Vector Dependency

### Statement
> * **(a)** Any finite set of vectors containing the zero vector $\mathbf{0}$ is **linearly dependent**.
> * **(b)** A set $S = \{\mathbf{s}_1, \mathbf{s}_2\}$ with exactly two vectors is **linearly independent** if and only if neither vector is a scalar multiple of the other.

### Proofs
* **Proof of Part (a):**
  Let $S = \{\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_r, \mathbf{0}\}$. Consider the linear combination:
  $$0\mathbf{v}_1 + 0\mathbf{v}_2 + \dots + 0\mathbf{v}_r + 1\mathbf{0} = \mathbf{0}$$
  Because the coefficient of $\mathbf{0}$ is $1 \neq 0$, the equation has a **non-trivial solution** (not all coefficients are zero). Therefore, $S$ is linearly dependent.

* **Proof of Part (b) (via Contrapositive):**
  Proving *"$S$ is linearly independent iff neither vector is a scalar multiple of the other"* is logically equivalent to proving its contrapositive: *"$S$ is linearly dependent iff one vector is a scalar multiple of the other."*
  * **($\implies$) Assume $S$ is linearly dependent:**
    There exist scalars $k_1, k_2$, not both zero ($k_1 \neq 0$ or $k_2 \neq 0$), such that:
    $$k_1\mathbf{s}_1 + k_2\mathbf{s}_2 = \mathbf{0}$$
    * If $k_1 \neq 0$: $\mathbf{s}_1 = -\frac{k_2}{k_1}\mathbf{s}_2$ ($\mathbf{s}_1$ is a scalar multiple of $\mathbf{s}_2$).
    * If $k_2 \neq 0$: $\mathbf{s}_2 = -\frac{k_1}{k_2}\mathbf{s}_1$ ($\mathbf{s}_2$ is a scalar multiple of $\mathbf{s}_1$).
  * **($\impliedby$) Assume one vector is a scalar multiple of the other:**
    Without loss of generality, suppose $\mathbf{s}_2 = k\mathbf{s}_1$ for some scalar $k \in \mathbb{R}$. Then:
    $$k\mathbf{s}_1 - 1\mathbf{s}_2 = \mathbf{0}$$
    Since the coefficient of $\mathbf{s}_2$ is $-1 \neq 0$, the coefficients are not all zero, so $S$ is linearly dependent.

$$\blacksquare$$

---

## Theorem: Every Non-Empty Subset of a Linearly Independent Set is Linearly Independent

### Statement
> Show that if $S = \{\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_r\}$ is a linearly independent set of vectors in $V$, then every non-empty subset $S' \subseteq S$ is also linearly independent.

### Proof
Let $S' = \{\mathbf{v}_{i_1}, \mathbf{v}_{i_2}, \dots, \mathbf{v}_{i_k}\}$ be any non-empty subset of $S$ (where $1 \le k \le r$).
Consider the homogeneous linear combination of vectors in $S'$:
$$c_1 \mathbf{v}_{i_1} + c_2 \mathbf{v}_{i_2} + \dots + c_k \mathbf{v}_{i_k} = \mathbf{0}$$
We can expand this equation to include **all** vectors in $S$ by assigning a coefficient of $0$ to every vector in $S \setminus S'$:
$$c_1 \mathbf{v}_{i_1} + \dots + c_k \mathbf{v}_{i_k} + \sum_{\mathbf{v}_j \in S \setminus S'} 0 \cdot \mathbf{v}_j = \mathbf{0}$$
This forms a linear combination of the entire set $S$ that equals $\mathbf{0}$. Since $S$ is linearly independent, **every scalar coefficient in this equation must be zero**. In particular:
$$c_1 = c_2 = \dots = c_k = 0$$
Thus, $S'$ is linearly independent.

$$\blacksquare$$

---

## Theorem: The Plus/Minus Theorem (Extending & Trimming Sets)

### Statement
> Let $S$ be a non-empty set of vectors in a vector space $V$:
> * **(a) The "Plus" Part (Extending Independence):** If $S = \{\mathbf{v}_1, \dots, \mathbf{v}_r\}$ is a linearly independent set and $\mathbf{v} \in V$ is a vector that **does NOT lie in $\text{span}(S)$**, then $S \cup \{\mathbf{v}\} = \{\mathbf{v}_1, \dots, \mathbf{v}_r, \mathbf{v}\}$ is also **linearly independent**.
> * **(b) The "Minus" Part (Trimming Redundancy):** If a vector $\mathbf{v} \in S$ is expressible as a linear combination of the other vectors in $S$, and if $S \setminus \{\mathbf{v}\}$ denotes the set obtained by removing $\mathbf{v}$ from $S$, then $S$ and $S \setminus \{\mathbf{v}\}$ span the **exact same space**:
>   $$\text{span}(S) = \text{span}(S \setminus \{\mathbf{v}\})$$

### Proofs

* **Proof of (a) — Plus Part (illustrated for $\{\mathbf{v}_1, \dots, \mathbf{v}_r, \mathbf{v}\}$):**
  Consider the homogeneous equation:
  $$k_1\mathbf{v}_1 + \dots + k_r\mathbf{v}_r + k\mathbf{v} = \mathbf{0}$$
  Suppose for contradiction that $k \neq 0$. Then we can isolate $\mathbf{v}$ and divide by $k$:
  $$\mathbf{v} = \left(-\frac{k_1}{k}\right)\mathbf{v}_1 + \dots + \left(-\frac{k_r}{k}\right)\mathbf{v}_r$$
  This expresses $\mathbf{v}$ as a linear combination of vectors in $S$, contradicting the given hypothesis that $\mathbf{v} \notin \text{span}(S)$.
  Therefore, we must have $k = 0$. Substituting $k = 0$ back leaves:
  $$k_1\mathbf{v}_1 + \dots + k_r\mathbf{v}_r = \mathbf{0}$$
  Since $S$ is linearly independent, $k_1 = k_2 = \dots = k_r = 0$. Since all coefficients $(k_1, \dots, k_r, k)$ are zero, $S \cup \{\mathbf{v}\}$ is linearly independent.

* **Proof of (b) — Minus Part:**
  Let $S = \{\mathbf{v}_1, \dots, \mathbf{v}_r, \mathbf{v}\}$ where $\mathbf{v} = a_1\mathbf{v}_1 + \dots + a_r\mathbf{v}_r$.
  1. Clearly $\text{span}(S \setminus \{\mathbf{v}\}) \subseteq \text{span}(S)$ since removing a vector cannot add combinations.
  2. Conversely, let $\mathbf{w} \in \text{span}(S)$:
     $$\mathbf{w} = c_1\mathbf{v}_1 + \dots + c_r\mathbf{v}_r + c\mathbf{v}$$
     Substitute $\mathbf{v} = \sum_{i=1}^r a_i \mathbf{v}_i$:
     $$\mathbf{w} = (c_1 + c a_1)\mathbf{v}_1 + \dots + (c_r + c a_r)\mathbf{v}_r \in \text{span}(S \setminus \{\mathbf{v}\})$$
     Thus $\text{span}(S) \subseteq \text{span}(S \setminus \{\mathbf{v}\})$, proving equality.

$$\blacksquare$$

---

## Theorem 5.3.3 & 5.4.3: Dimension Bounds on Linear Independence and Spanning

### Statement (General Vector Space $V$ with $\dim(V) = n$)
> Let $V$ be a finite-dimensional vector space and let $S = \{\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_n\}$ be any basis for $V$ (so $\dim(V) = n$). Prove that:
> * **(a)** Any set $S' = \{\mathbf{w}_1, \mathbf{w}_2, \dots, \mathbf{w}_m\} \subset V$ with **$m > n$ vectors** is **linearly dependent**. *(In $\mathbb{R}^n$, any $> n$ vectors are LD).*
> * **(b)** Any set $S' = \{\mathbf{w}_1, \mathbf{w}_2, \dots, \mathbf{w}_m\} \subset V$ with **$m < n$ vectors** **cannot span $V$**.

### Proofs

#### Proof of Part (a): More than $n$ vectors ($m > n$) $\implies$ Linearly Dependent
Since $S = \{\mathbf{v}_1, \dots, \mathbf{v}_n\}$ is a basis of $V$, every vector $\mathbf{w}_j \in S'$ can be written as a linear combination of the basis vectors:
$$\mathbf{w}_j = \sum_{i=1}^n a_{ij}\mathbf{v}_i \quad \text{for } j = 1, 2, \dots, m$$
To test linear independence of $S'$, consider:
$$k_1\mathbf{w}_1 + k_2\mathbf{w}_2 + \dots + k_m\mathbf{w}_m = \mathbf{0}$$
Substituting the basis expansions and regrouping by $\mathbf{v}_1, \dots, \mathbf{v}_n$:
$$\sum_{j=1}^m k_j \left(\sum_{i=1}^n a_{ij}\mathbf{v}_i\right) = \sum_{i=1}^n \left(\sum_{j=1}^m a_{ij}k_j\right)\mathbf{v}_i = \mathbf{0}$$
Because $S = \{\mathbf{v}_1, \dots, \mathbf{v}_n\}$ is linearly independent, every coefficient multiplying $\mathbf{v}_i$ must equal $0$:
$$\begin{cases}
a_{11}k_1 + a_{12}k_2 + \dots + a_{1m}k_m = 0 \\
\vdots \\
a_{n1}k_1 + a_{n2}k_2 + \dots + a_{nm}k_m = 0
\end{cases}$$
This is a homogeneous linear system of **$n$ equations in $m$ unknowns** ($k_1, \dots, k_m$). Since $m > n$ (more unknowns than equations), the system must have at least one free variable and thus admits a **non-trivial solution**. Therefore, $S'$ is linearly dependent!

*(Note: For $V = \mathbb{R}^n$, the standard basis is $\mathbf{e}_1, \dots, \mathbf{e}_n$, so the coefficients $a_{ij}$ are simply the entries of the vectors $\mathbf{w}_j$, giving the exact $n \times m$ matrix system directly!)*

#### Proof of Part (b): Fewer than $n$ vectors ($m < n$) $\implies$ Does Not Span $V$
Suppose for contradiction that $S' = \{\mathbf{w}_1, \dots, \mathbf{w}_m\}$ with $m < n$ *does* span $V$.
Then each basis vector $\mathbf{v}_j \in S$ ($j = 1, \dots, n$) can be written as a linear combination of $\mathbf{w}_1, \dots, \mathbf{w}_m$:
$$\mathbf{v}_j = \sum_{i=1}^m a_{ij}\mathbf{w}_i$$
Consider the homogeneous equation on the basis $S$: $k_1\mathbf{v}_1 + \dots + k_n\mathbf{v}_n = \mathbf{0}$. Substituting gives:
$$\sum_{i=1}^m \left(\sum_{j=1}^n a_{ij}k_j\right)\mathbf{w}_i = \mathbf{0}$$
Setting each inner sum to zero produces a homogeneous system of **$m$ equations in $n$ unknowns** ($k_1, \dots, k_n$):
$$\sum_{j=1}^n a_{ij}k_j = 0 \quad (i = 1, \dots, m)$$
Since $m < n$ (more unknowns than equations), this homogeneous system has a **non-trivial solution** (not all $k_j = 0$) that satisfies $\sum_{j=1}^n k_j\mathbf{v}_j = \mathbf{0}$.
This directly contradicts the fact that $S = \{\mathbf{v}_1, \dots, \mathbf{v}_n\}$ is a basis (linearly independent). Therefore, $S'$ cannot span $V$.

$$\blacksquare$$

---

## Theorem 5.4.1: Uniqueness of Basis Representation

### Statement
> If $S = \{\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_n\}$ is a basis for a vector space $V$, then every vector $\mathbf{v} \in V$ can be expressed in the form $\mathbf{v} = c_1\mathbf{v}_1 + c_2\mathbf{v}_2 + \dots + c_n\mathbf{v}_n$ in **exactly one way**.

### Proof
Since $S$ spans $V$, at least one such representation exists for every $\mathbf{v} \in V$.
To prove uniqueness, suppose $\mathbf{v}$ has two representations:
$$\mathbf{v} = c_1\mathbf{v}_1 + c_2\mathbf{v}_2 + \dots + c_n\mathbf{v}_n \quad \text{--- (1)}$$
$$\mathbf{v} = k_1\mathbf{v}_1 + k_2\mathbf{v}_2 + \dots + k_n\mathbf{v}_n \quad \text{--- (2)}$$
Subtract Equation (1) from Equation (2):
$$\mathbf{v} - \mathbf{v} = (k_1 - c_1)\mathbf{v}_1 + (k_2 - c_2)\mathbf{v}_2 + \dots + (k_n - c_n)\mathbf{v}_n$$
$$\mathbf{0} = (k_1 - c_1)\mathbf{v}_1 + (k_2 - c_2)\mathbf{v}_2 + \dots + (k_n - c_n)\mathbf{v}_n$$
Since $S$ is a basis, its vectors are **linearly independent**, so the only solution is the trivial one where every coefficient is zero:
$$k_1 - c_1 = 0, \quad k_2 - c_2 = 0, \quad \dots, \quad k_n - c_n = 0$$
$$k_1 = c_1, \quad k_2 = c_2, \quad \dots, \quad k_n = c_n$$
Thus, the coordinate representation is strictly unique.

$$\blacksquare$$

---

## Theorem 5.4.5: The Half-Test for Basis (Basis Theorem in $n$-Dimensional Space)

### Statement
> If $V$ is an $n$-dimensional vector space ($\dim(V) = n$) and $S$ is a set in $V$ containing **exactly $n$ vectors**, then $S$ is a basis for $V$ if **EITHER** $S$ spans $V$ **OR** $S$ is linearly independent.

### Proof
* **Case 1: Assume $|S| = n$ and $S$ spans $V$.** *(We must prove $S$ is linearly independent).*
  Suppose for contradiction that $S$ is NOT linearly independent. By Theorem 5.3.1, some vector $\mathbf{v} \in S$ is a linear combination of the other vectors in $S$.
  By the **Minus part** of the Plus/Minus Theorem, removing $\mathbf{v}$ preserves the span, so the remaining set $S \setminus \{\mathbf{v}\}$ (which has **$n - 1$ vectors**) still spans $V$.
  However, this is a **contradiction** by Theorem 5.4.3(b): fewer than $n$ vectors ($n - 1 < n$) cannot span an $n$-dimensional vector space!
  Hence, $S$ must be linearly independent, and therefore $S$ is a basis for $V$.

* **Case 2: Assume $|S| = n$ and $S$ is linearly independent.** *(We must prove $S$ spans $V$).*
  Suppose for contradiction that $S$ does NOT span $V$. Then there must exist some vector $\mathbf{v} \in V$ such that $\mathbf{v} \notin \text{span}(S)$.
  By the **Plus part** of the Plus/Minus Theorem, inserting $\mathbf{v}$ into $S$ yields $S \cup \{\mathbf{v}\}$ (which has **$n + 1$ vectors**) that is also linearly independent.
  However, this is a **contradiction** by Theorem 5.4.3(a): a set with more than $n$ vectors ($n + 1 > n$) in an $n$-dimensional space cannot be linearly independent!
  Hence, $S$ must span $V$, and therefore $S$ is a basis for $V$.

$$\blacksquare$$

---

# Part IV: Row Space, Column Space, Rank & Nullity

---

## Theorem: Null Space & Column Linear Independence Equivalence

### Statement
> For any $m \times n$ matrix $A$, the column vectors of $A$ are **linearly independent** if and only if the null space of $A$ contains only the zero vector:
> $$\text{Columns of } A \text{ are linearly independent} \iff \text{Null}(A) = \{\mathbf{0}\} \iff \text{Nullity}(A) = 0$$

### Proof
Let $A = \begin{bmatrix} \mathbf{a}_1 & \mathbf{a}_2 & \dots & \mathbf{a}_n \end{bmatrix}$ and $\mathbf{x} = \begin{bmatrix} x_1 & x_2 & \dots & x_n \end{bmatrix}^T$.
By definition of matrix multiplication:
$$A\mathbf{x} = \mathbf{0} \iff x_1\mathbf{a}_1 + x_2\mathbf{a}_2 + \dots + x_n\mathbf{a}_n = \mathbf{0}$$
* **($\implies$)** If the columns are linearly independent, the only scalars solving $x_1\mathbf{a}_1 + \dots + x_n\mathbf{a}_n = \mathbf{0}$ are $x_1 = \dots = x_n = 0$, i.e. $\mathbf{x} = \mathbf{0}$. Hence $\text{Null}(A) = \{\mathbf{0}\}$.
* **($\impliedby$)** Conversely, if $\text{Null}(A) = \{\mathbf{0}\}$, then the only solution to $A\mathbf{x} = \mathbf{0}$ is $\mathbf{x} = \mathbf{0}$, meaning $x_1 = \dots = x_n = 0$ is the only solution to $x_1\mathbf{a}_1 + \dots + x_n\mathbf{a}_n = \mathbf{0}$. Thus the columns are linearly independent.

$$\blacksquare$$

---

## Theorems 5.5.4 & 5.5.5: Row Operations Preserve Row Space & Column Relations

### Statements
> Let $R$ be obtained from a matrix $A$ by elementary row operations (e.g., $R$ is an REF/RREF of $A$):
> * **(a) Theorem 5.5.4:** Elementary row operations do **not** change the row space of a matrix: $\text{Row}(A) = \text{Row}(R)$ (and thus $\dim(\text{Row}(A)) = \dim(\text{Row}(R))$).
> * **(b) Theorem 5.5.5:** Elementary row operations do **not** change the linear dependency relationships among the columns of $A$. Therefore, the pivot columns of $A$ form a basis for $\text{Col}(A)$, and $\dim(\text{Col}(A)) = \dim(\text{Col}(R))$.

### Proof Sketches
* **Why $\text{Row}(A) = \text{Row}(R)$:** Every elementary row operation (swapping two rows, scaling a row by $k \neq 0$, or replacing $R_i$ by $R_i + cR_j$) produces new rows that are **linear combinations of the rows of $A$**. Thus $\text{Row}(R) \subseteq \text{Row}(A)$. Because every ERO is reversible by an inverse ERO, the rows of $A$ are also linear combinations of the rows of $R$, so $\text{Row}(A) \subseteq \text{Row}(R)$. Hence $\text{Row}(A) = \text{Row}(R)$.
* **Why column relations are preserved:** If $R = EA$ for an invertible product of elementary matrices $E$, then $R\mathbf{x} = \mathbf{0} \iff E(A\mathbf{x}) = \mathbf{0} \iff A\mathbf{x} = \mathbf{0}$. Writing $A\mathbf{x} = \sum x_j \mathbf{a}_j$ and $R\mathbf{x} = \sum x_j \mathbf{r}_j$, the **exact same scalars** $x_j$ satisfy $\sum x_j \mathbf{a}_j = \mathbf{0}$ as satisfy $\sum x_j \mathbf{r}_j = \mathbf{0}$! Therefore, a subset of columns of $A$ is linearly independent (or forms a basis of $\text{Col}(A)$) if and only if the corresponding columns of $R$ are linearly independent!

---

## Theorem 5.6.1: Row Rank Equals Column Rank

### Statement
> If $A$ is any $m \times n$ matrix, then the row space and column space of $A$ have the **exact same dimension**:
> $$\dim(\text{Row}(A)) = \dim(\text{Col}(A))$$

### Proof
Let $R$ be any row-echelon form (REF) of $A$.
* By Theorem 5.5.4, elementary row operations preserve the row space, so:
  $$\dim(\text{Row}(A)) = \dim(\text{Row}(R))$$
* By Theorem 5.5.5, elementary row operations preserve linear independence relations among the columns, so:
  $$\dim(\text{Col}(A)) = \dim(\text{Col}(R))$$

Thus, the proof is complete if we show $\dim(\text{Row}(R)) = \dim(\text{Col}(R))$ for the row-echelon form $R$:
1. The **nonzero row vectors** of $R$ are linearly independent (because of the staircase of leading $1$'s) and span $\text{Row}(R)$, so:
   $$\dim(\text{Row}(R)) = \text{number of nonzero rows in } R$$
2. The **columns containing leading $1$'s** (pivot columns) of $R$ form a basis for $\text{Col}(R)$, so:
   $$\dim(\text{Col}(R)) = \text{number of columns containing leading } 1\text{'s in } R$$
3. However, every nonzero row of $R$ has **exactly one** leading $1$, and every column with a leading $1$ corresponds to **exactly one** nonzero row. Therefore, the number of nonzero rows equals the number of leading $1$'s (pivots).

Consequently, $\dim(\text{Row}(R)) = \dim(\text{Col}(R))$, and hence:
$$\dim(\text{Row}(A)) = \dim(\text{Col}(A))$$

$$\blacksquare$$

---

## Theorem 5.6.3: The Rank-Nullity Theorem for Matrices

### Statement
> If $A$ is any $m \times n$ matrix (having $n$ columns), then:
> $$\text{Rank}(A) + \text{Nullity}(A) = n$$
> where $\text{Rank}(A) = \dim(\text{Col}(A)) = \dim(\text{Row}(A))$ and $\text{Nullity}(A) = \dim(\text{Null}(A))$.

### Proof
Let $R = \text{RREF}(A)$ be the reduced row-echelon form of $A$, and let $r$ be the number of leading $1$'s (pivots) in $R$.
1. By definition of rank and Theorem 5.6.1, $\text{Rank}(A) = r$ (the number of pivot columns).
2. In the homogeneous system $A\mathbf{x} = \mathbf{0} \iff R\mathbf{x} = \mathbf{0}$:
   * There are $n$ total variables (one for each column of $A$).
   * Exactly $r$ variables correspond to pivot columns (**leading/pivot variables**).
   * The remaining $n - r$ variables correspond to non-pivot columns (**free variables**).
3. Solving $R\mathbf{x} = \mathbf{0}$ expresses each of the $r$ pivot variables uniquely in terms of the $n - r$ free variables. Setting one free variable to $1$ and all other free variables to $0$ yields $n - r$ solution vectors $\mathbf{v}_1, \dots, \mathbf{v}_{n-r} \in \mathbb{R}^n$ such that every solution is $\mathbf{x} = t_1\mathbf{v}_1 + \dots + t_{n-r}\mathbf{v}_{n-r}$.
   * Because each $\mathbf{v}_j$ has a $1$ in the coordinate of its free variable and $0$ in the coordinates of all other free variables (forming an embedded $(n-r)\times(n-r)$ identity submatrix), these $n - r$ vectors are strictly linearly independent and span $\text{Null}(A)$.
   * *(If $r = n$, there are $0$ free variables, $\text{Null}(A) = \{\mathbf{0}\}$, and $\text{Nullity}(A) = 0 = n - n$).*
4. Therefore, $\text{Nullity}(A) = n - r$. Summing the two gives:
   $$\text{Rank}(A) + \text{Nullity}(A) = r + (n - r) = n$$

$$\blacksquare$$

---

# Part V: Linear Transformations

---

## Theorem: Fundamental Properties of Linear Transformations

### Statement
> Let $T: V \to W$ be a linear transformation ($T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v})$ and $T(c\mathbf{u}) = cT(\mathbf{u})$). Prove:
> * **(a) Zero Vector Preservation:** $T(\mathbf{0}_V) = \mathbf{0}_W$
> * **(b) Negation Preservation:** $T(-\mathbf{u}) = -T(\mathbf{u})$
> * **(c) Difference Preservation:** $T(\mathbf{u} - \mathbf{v}) = T(\mathbf{u}) - T(\mathbf{v})$
> * **(d) Superposition Principle:** $T(c_1\mathbf{v}_1 + \dots + c_k\mathbf{v}_k) = c_1 T(\mathbf{v}_1) + \dots + c_k T(\mathbf{v}_k)$

### Proofs
* **(a)** Choose $c = 0 \in \mathbb{R}$ and any $\mathbf{u} \in V$:
  $$T(\mathbf{0}_V) = T(0 \cdot \mathbf{u}) \overset{\text{homogeneity}}{=} 0 \cdot T(\mathbf{u}) = \mathbf{0}_W$$
* **(b)** Choose $c = -1$:
  $$T(-\mathbf{u}) = T((-1)\mathbf{u}) = (-1)T(\mathbf{u}) = -T(\mathbf{u})$$
* **(c)** Combine additivity and (b):
  $$T(\mathbf{u} - \mathbf{v}) = T(\mathbf{u} + (-\mathbf{v})) = T(\mathbf{u}) + T(-\mathbf{v}) = T(\mathbf{u}) - T(\mathbf{v})$$
* **(d)** Apply additivity repeatedly, then pull out each scalar $c_i$ using homogeneity:
  $$T(c_1\mathbf{v}_1 + \dots + c_k\mathbf{v}_k) = T(c_1\mathbf{v}_1) + \dots + T(c_k\mathbf{v}_k) = c_1 T(\mathbf{v}_1) + \dots + c_k T(\mathbf{v}_k)$$

$$\blacksquare$$

---

## Theorem: Every Matrix Transformation $T(\mathbf{x}) = A\mathbf{x}$ is Linear

### Statement
> For any $m \times n$ matrix $A$, the transformation $T: \mathbb{R}^n \to \mathbb{R}^m$ defined by $T(\mathbf{x}) = A\mathbf{x}$ is a linear transformation.

### Proof
Let $\mathbf{u}, \mathbf{v} \in \mathbb{R}^n$ and $c \in \mathbb{R}$. By the distributive and associative properties of matrix multiplication:
1. **Additivity:**
   $$T(\mathbf{u} + \mathbf{v}) = A(\mathbf{u} + \mathbf{v}) = A\mathbf{u} + A\mathbf{v} = T(\mathbf{u}) + T(\mathbf{v})$$
2. **Homogeneity:**
   $$T(c\mathbf{u}) = A(c\mathbf{u}) = c(A\mathbf{u}) = cT(\mathbf{u})$$

Both linearity axioms hold, so $T$ is linear.

$$\blacksquare$$

---

## Theorem: Standard Matrix Representation & Uniqueness

### Statement
> Let $T: \mathbb{R}^n \to \mathbb{R}^m$ be any linear transformation. Then there exists a **unique** $m \times n$ matrix $[T]$ (called the standard matrix of $T$) such that $T(\mathbf{x}) = [T]\mathbf{x}$ for all $\mathbf{x} \in \mathbb{R}^n$, given explicitly by:
> $$[T] = \begin{bmatrix} T(\mathbf{e}_1) & T(\mathbf{e}_2) & \dots & T(\mathbf{e}_n) \end{bmatrix}$$
> where $\{\mathbf{e}_1, \dots, \mathbf{e}_n\}$ is the standard basis of $\mathbb{R}^n$.

### Proof
1. **Existence:**
   Any vector $\mathbf{x} = \begin{bmatrix} x_1 \\ \vdots \\ x_n \end{bmatrix} \in \mathbb{R}^n$ can be written as $\mathbf{x} = x_1\mathbf{e}_1 + x_2\mathbf{e}_2 + \dots + x_n\mathbf{e}_n$.
   By linearity of $T$:
   $$T(\mathbf{x}) = T(x_1\mathbf{e}_1 + x_2\mathbf{e}_2 + \dots + x_n\mathbf{e}_n) = x_1 T(\mathbf{e}_1) + x_2 T(\mathbf{e}_2) + \dots + x_n T(\mathbf{e}_n)$$
   By definition of matrix-vector multiplication, this linear combination of columns equals:
   $$T(\mathbf{x}) = \begin{bmatrix} T(\mathbf{e}_1) & T(\mathbf{e}_2) & \dots & T(\mathbf{e}_n) \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix} = [T]\mathbf{x}$$
2. **Uniqueness:**
   Suppose another $m \times n$ matrix $B = \begin{bmatrix} \mathbf{b}_1 & \dots & \mathbf{b}_n \end{bmatrix}$ also satisfies $T(\mathbf{x}) = B\mathbf{x}$ for all $\mathbf{x} \in \mathbb{R}^n$.
   Evaluating at each standard basis vector $\mathbf{e}_j$ ($j = 1, \dots, n$):
   $$T(\mathbf{e}_j) = B\mathbf{e}_j = \mathbf{b}_j \quad (\text{since } B\mathbf{e}_j \text{ extracts the } j\text{-th column of } B)$$
   Hence every column of $B$ equals $T(\mathbf{e}_j)$, so $B = [T]$.

$$\blacksquare$$

---

## Theorem: Range of a Matrix Transformation Equals the Column Space

### Statement
> Prove that the range of a matrix transformation $T: \mathbb{R}^n \to \mathbb{R}^m$ given by $T(\mathbf{x}) = A\mathbf{x}$ is equal to the column space of $A$:
> $$R(T) = \text{Col}(A)$$

### Proof
By definition, the range of $T$ is the set of all possible outputs:
$$R(T) = \{T(\mathbf{x}) \mid \mathbf{x} \in \mathbb{R}^n\}$$
Let $A$ be an $m \times n$ matrix partitioned into its column vectors $\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_n \in \mathbb{R}^m$:
$$A = \begin{bmatrix} \mathbf{v}_1 & \mathbf{v}_2 & \dots & \mathbf{v}_n \end{bmatrix}, \quad \text{and let } \mathbf{x} = \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix} \in \mathbb{R}^n$$
Evaluating $T(\mathbf{x}) = A\mathbf{x}$ via the column view of matrix multiplication:
$$T(\mathbf{x}) = \begin{bmatrix} \mathbf{v}_1 & \mathbf{v}_2 & \dots & \mathbf{v}_n \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix} = x_1\mathbf{v}_1 + x_2\mathbf{v}_2 + \dots + x_n\mathbf{v}_n$$
Thus, every output of $T$ is a linear combination of the columns of $A$.
As $\mathbf{x}$ ranges over every possible input vector $(x_1, \dots, x_n) \in \mathbb{R}^n$, the output $T(\mathbf{x}) = A\mathbf{x}$ ranges over every possible linear combination of the columns of $A$, which is precisely $\text{span}\{\mathbf{v}_1, \dots, \mathbf{v}_n\} = \text{Col}(A)$.

Hence, $R(T) = \text{Col}(A)$.

$$\blacksquare$$

---

## Theorem: Kernel and Range are Subspaces

### Statement
> Let $T: V \to W$ be a linear transformation between vector spaces $V$ and $W$. Prove that:
> * **(a)** $\ker(T) = \{\mathbf{v} \in V \mid T(\mathbf{v}) = \mathbf{0}_W\}$ is a **subspace of the domain $V$**.
> * **(b)** $R(T) = \{T(\mathbf{v}) \mid \mathbf{v} \in V\}$ is a **subspace of the codomain $W$**.

### Proofs

#### Part (a): $\ker(T)$ is a subspace of $V$
1. **Contains Zero ($\mathbf{0}_V \in \ker(T)$):**
   Since $T$ is linear, $T(\mathbf{0}_V) = \mathbf{0}_W$, so $\mathbf{0}_V \in \ker(T)$.
2. **Closed under Addition:**
   Let $\mathbf{u}, \mathbf{v} \in \ker(T)$, meaning $T(\mathbf{u}) = \mathbf{0}_W$ and $T(\mathbf{v}) = \mathbf{0}_W$.
   $$T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v}) = \mathbf{0}_W + \mathbf{0}_W = \mathbf{0}_W$$
   Therefore, $\mathbf{u} + \mathbf{v} \in \ker(T)$.
3. **Closed under Scalar Multiplication:**
   Let $\mathbf{u} \in \ker(T)$ (so $T(\mathbf{u}) = \mathbf{0}_W$) and $c \in \mathbb{R}$.
   $$T(c\mathbf{u}) = cT(\mathbf{u}) = c\mathbf{0}_W = \mathbf{0}_W$$
   Therefore, $c\mathbf{u} \in \ker(T)$.

#### Part (b): $R(T)$ is a subspace of $W$
1. **Contains Zero ($\mathbf{0}_W \in R(T)$):**
   Since $\mathbf{0}_V \in V$ and $T(\mathbf{0}_V) = \mathbf{0}_W$, there is an input mapping to $\mathbf{0}_W$, so $\mathbf{0}_W \in R(T)$.
2. **Closed under Addition:**
   Let $\mathbf{w}_1, \mathbf{w}_2 \in R(T)$. Then there exist $\mathbf{v}_1, \mathbf{v}_2 \in V$ such that $T(\mathbf{v}_1) = \mathbf{w}_1$ and $T(\mathbf{v}_2) = \mathbf{w}_2$.
   By additivity of $T$:
   $$\mathbf{w}_1 + \mathbf{w}_2 = T(\mathbf{v}_1) + T(\mathbf{v}_2) = T(\mathbf{v}_1 + \mathbf{v}_2)$$
   Since $(\mathbf{v}_1 + \mathbf{v}_2) \in V$, $\mathbf{w}_1 + \mathbf{w}_2$ is the image of an element of $V$, so $\mathbf{w}_1 + \mathbf{w}_2 \in R(T)$.
3. **Closed under Scalar Multiplication:**
   Let $\mathbf{w}_1 = T(\mathbf{v}_1) \in R(T)$ and $c \in \mathbb{R}$.
   $$c\mathbf{w}_1 = cT(\mathbf{v}_1) = T(c\mathbf{v}_1)$$
   Since $c\mathbf{v}_1 \in V$, $c\mathbf{w}_1 \in R(T)$.

$$\blacksquare$$

---

## Theorem: The Trivial Kernel Test for One-to-One Linear Transformations

### Statement
> Let $T: V \to W$ be a linear transformation between vector spaces $V$ and $W$. Then $T$ is **one-to-one** (injective) if and only if the kernel of $T$ consists of only the zero vector:
> $$T \text{ is one-to-one} \iff \ker(T) = \{\mathbf{0}\}$$

### Core Intuition: Why Do We Only Solve $A\mathbf{x} = \mathbf{0}$ Instead of Checking Every Arbitrary $A\mathbf{x} = \mathbf{b}$?

A very natural question is: *"One-to-one means NO output $\mathbf{b}$ anywhere can have two different inputs. Why do we only test $\mathbf{b} = \mathbf{0}$ instead of testing an arbitrary $\mathbf{b}$?"*

The answer is **linearity** ($T(\mathbf{u} - \mathbf{w}) = T(\mathbf{u}) - T(\mathbf{w})$), which works in both directions:

1. **Any collision at ANY $\mathbf{b}$ automatically shows up at $\mathbf{0}$ (The $\mathbf{b}$ Cancels Out!):**
   Suppose some arbitrary vector $\mathbf{b}$ could be hit by two distinct inputs $\mathbf{u} \neq \mathbf{w}$:
   $$A\mathbf{u} = \mathbf{b} \quad \text{and} \quad A\mathbf{w} = \mathbf{b}$$
   Subtract the two equations:
   $$A\mathbf{u} - A\mathbf{w} = \mathbf{b} - \mathbf{b} \implies A(\mathbf{u} - \mathbf{w}) = \mathbf{0}$$
   The arbitrary $\mathbf{b}$ **completely cancels out**! Every collision $(\mathbf{u}, \mathbf{w})$ at any target $\mathbf{b}$ creates a non-zero vector $\mathbf{v}_h = (\mathbf{u} - \mathbf{w}) \neq \mathbf{0}$ that solves $A\mathbf{x} = \mathbf{0}$. Therefore, if $A\mathbf{x} = \mathbf{0}$ has ONLY $\mathbf{x} = \mathbf{0}$, no collision can exist at *any* $\mathbf{b}$!

2. **Any collapse at $\mathbf{0}$ copies itself to EVERY reachable $\mathbf{b}$ ($\mathbf{x} = \mathbf{x}_p + \mathbf{x}_h$):**
   Conversely, if there exists a non-zero $\mathbf{v}_h \in \ker(T)$ ($A\mathbf{v}_h = \mathbf{0}$), take ANY target $\mathbf{b}$ reached by some input $\mathbf{x}_p$ ($A\mathbf{x}_p = \mathbf{b}$). For every scalar $c \in \mathbb{R}$:
   $$A(\mathbf{x}_p + c\mathbf{v}_h) = A\mathbf{x}_p + c(A\mathbf{v}_h) = \mathbf{b} + c(\mathbf{0}) = \mathbf{b}$$
   So every single reachable $\mathbf{b}$ has infinitely many pre-images $\mathbf{x}_p + c\mathbf{v}_h$.

3. **Why this fails for Non-Linear functions:**
   For non-linear maps (like $f(x) = (x - 2)^2$), $f(x) = 0$ has only one solution ($x = 2$), yet $f(x) = 1$ has two ($x = 1, 3$), because $f(u) - f(w) \neq f(u - w)$. **Linearity is the exact superpower that makes $\mathbf{0}$ a universal detector for the entire space.**

### Proof (Bidirectional $\iff$)

Recall: $T$ is one-to-one $\iff \big(T(\mathbf{u}) = T(\mathbf{w}) \implies \mathbf{u} = \mathbf{w}\big)$ for all $\mathbf{u}, \mathbf{w} \in V$.

#### 1. Forward Direction ($\implies$): Assume $T$ is one-to-one, prove $\ker(T) = \{\mathbf{0}_V\}$
1. By linearity, $T(\mathbf{0}_V) = \mathbf{0}_W$, so $\mathbf{0}_V \in \ker(T)$.
2. Let $\mathbf{v}$ be any arbitrary vector in $\ker(T)$, meaning $T(\mathbf{v}) = \mathbf{0}_W$.
3. Equating gives $T(\mathbf{v}) = T(\mathbf{0}_V)$.
4. Since $T$ is one-to-one, $T(\mathbf{v}) = T(\mathbf{0}_V) \implies \mathbf{v} = \mathbf{0}_V$.
5. Hence, $\ker(T) = \{\mathbf{0}_V\}$.

#### 2. Backward Direction ($\impliedby$): Assume $\ker(T) = \{\mathbf{0}_V\}$, prove $T$ is one-to-one
1. Let $\mathbf{u}, \mathbf{w} \in V$ such that $T(\mathbf{u}) = T(\mathbf{w})$.
2. Subtracting gives $T(\mathbf{u}) - T(\mathbf{w}) = \mathbf{0}_W$.
3. By linearity, $T(\mathbf{u} - \mathbf{w}) = \mathbf{0}_W$, so $(\mathbf{u} - \mathbf{w}) \in \ker(T)$.
4. Since $\ker(T) = \{\mathbf{0}_V\}$, it follows that $\mathbf{u} - \mathbf{w} = \mathbf{0}_V \implies \mathbf{u} = \mathbf{w}$.
5. Thus, $T$ is one-to-one.

$$\blacksquare$$

---

## Theorem: Composition of Linear Transformations is Linear & Matrix Product Rule

### Statement
> Let $T_1: U \to V$ and $T_2: V \to W$ be linear transformations. Define the composition $(T_2 \circ T_1): U \to W$ by $(T_2 \circ T_1)(\mathbf{u}) = T_2(T_1(\mathbf{u}))$. Then:
> * **(a)** $T_2 \circ T_1$ is a linear transformation.
> * **(b)** If $U = \mathbb{R}^n$, $V = \mathbb{R}^k$, and $W = \mathbb{R}^m$, the standard matrix of the composition is the matrix product $[T_2 \circ T_1] = [T_2][T_1]$.

### Proofs
* **Proof of (a):** Let $\mathbf{u}, \mathbf{v} \in U$ and $c \in \mathbb{R}$.
  1. **Additivity:**
     $$(T_2 \circ T_1)(\mathbf{u} + \mathbf{v}) = T_2(T_1(\mathbf{u} + \mathbf{v})) \overset{T_1 \text{ lin.}}{=} T_2(T_1(\mathbf{u}) + T_1(\mathbf{v})) \overset{T_2 \text{ lin.}}{=} T_2(T_1(\mathbf{u})) + T_2(T_1(\mathbf{v})) = (T_2 \circ T_1)(\mathbf{u}) + (T_2 \circ T_1)(\mathbf{v})$$
  2. **Homogeneity:**
     $$(T_2 \circ T_1)(c\mathbf{u}) = T_2(T_1(c\mathbf{u})) \overset{T_1 \text{ lin.}}{=} T_2(cT_1(\mathbf{u})) \overset{T_2 \text{ lin.}}{=} cT_2(T_1(\mathbf{u})) = c(T_2 \circ T_1)(\mathbf{u})$$

* **Proof of (b):** For any $\mathbf{x} \in \mathbb{R}^n$:
  $$(T_2 \circ T_1)(\mathbf{x}) = T_2(T_1(\mathbf{x})) = [T_2]([T_1]\mathbf{x}) = \big([T_2][T_1]\big)\mathbf{x}$$
  By uniqueness of the standard matrix representation, $[T_2 \circ T_1] = [T_2][T_1]$.

$$\blacksquare$$

---

## Theorem: General Rank-Nullity Theorem & Equal-Dimension Equivalence

### Statement
> * **(a) Rank-Nullity Theorem for Transformations:** If $T: V \to W$ is a linear transformation from an $n$-dimensional vector space $V$ into a vector space $W$, then:
>   $$\text{rank}(T) + \text{nullity}(T) = \dim(R(T)) + \dim(\ker(T)) = \dim(V) = n$$
> * **(b) Equal-Dimension Equivalence:** If $\dim(V) = \dim(W) = n$ (finite), then $T$ is **one-to-one** if and only if $T$ is **onto**.

### Proofs

#### Proof of Part (a): $\text{rank}(T) + \text{nullity}(T) = n$
Let $k = \text{nullity}(T) = \dim(\ker(T))$.
* *(Boundary cases)* If $k = n$, then $\ker(T) = V$, so $T(\mathbf{v}) = \mathbf{0}$ for all $\mathbf{v} \in V \implies R(T) = \{\mathbf{0}\} \implies \text{rank}(T) = 0$, and $0 + n = n$.
* *(General case $0 \le k < n$)* Let $\{\mathbf{u}_1, \dots, \mathbf{u}_k\}$ be a basis for $\ker(T)$ (if $k = 0$, start with the empty set). Extend this linearly independent set to a basis of all of $V$:
  $$B = \{\mathbf{u}_1, \dots, \mathbf{u}_k, \mathbf{v}_1, \dots, \mathbf{v}_{n-k}\}$$
  We prove that $S = \{T(\mathbf{v}_1), \dots, T(\mathbf{v}_{n-k})\}$ is a **basis for $R(T)$**:
  1. **$S$ spans $R(T)$:** Let $\mathbf{w} \in R(T)$, so $\mathbf{w} = T(\mathbf{x})$ for some $\mathbf{x} \in V$. Write $\mathbf{x}$ in the basis $B$:
     $$\mathbf{x} = c_1\mathbf{u}_1 + \dots + c_k\mathbf{u}_k + d_1\mathbf{v}_1 + \dots + d_{n-k}\mathbf{v}_{n-k}$$
     Apply $T$ and use $T(\mathbf{u}_i) = \mathbf{0}$ (since $\mathbf{u}_i \in \ker(T)$):
     $$\mathbf{w} = T(\mathbf{x}) = \sum_{i=1}^k c_i \underbrace{T(\mathbf{u}_i)}_{\mathbf{0}} + \sum_{j=1}^{n-k} d_j T(\mathbf{v}_j) = d_1 T(\mathbf{v}_1) + \dots + d_{n-k} T(\mathbf{v}_{n-k}) \in \text{span}(S)$$
  2. **$S$ is linearly independent:** Suppose $d_1 T(\mathbf{v}_1) + \dots + d_{n-k} T(\mathbf{v}_{n-k}) = \mathbf{0}$. By linearity:
     $$T(d_1\mathbf{v}_1 + \dots + d_{n-k}\mathbf{v}_{n-k}) = \mathbf{0} \implies (d_1\mathbf{v}_1 + \dots + d_{n-k}\mathbf{v}_{n-k}) \in \ker(T)$$
     Since $\{\mathbf{u}_1, \dots, \mathbf{u}_k\}$ spans $\ker(T)$, there exist scalars $c_1, \dots, c_k$ such that:
     $$d_1\mathbf{v}_1 + \dots + d_{n-k}\mathbf{v}_{n-k} = c_1\mathbf{u}_1 + \dots + c_k\mathbf{u}_k$$
     $$(-c_1)\mathbf{u}_1 + \dots + (-c_k)\mathbf{u}_k + d_1\mathbf{v}_1 + \dots + d_{n-k}\mathbf{v}_{n-k} = \mathbf{0}$$
     Since $B$ is a basis of $V$ (linearly independent), every coefficient is zero, so $d_1 = \dots = d_{n-k} = 0$.

  Therefore, $S$ is a basis for $R(T)$, giving $\text{rank}(T) = \dim(R(T)) = n - k$. Hence:
  $$\text{rank}(T) + \text{nullity}(T) = (n - k) + k = n$$

#### Proof of Part (b): Equal Dimensions $\implies$ ($T$ 1-to-1 $\iff$ $T$ onto)
Assume $\dim(V) = \dim(W) = n$.
$$T \text{ is one-to-one} \iff \ker(T) = \{\mathbf{0}\} \iff \text{nullity}(T) = 0$$
By Part (a) (Rank-Nullity Theorem):
$$\text{nullity}(T) = 0 \iff \text{rank}(T) = n - 0 = n = \dim(W)$$
Since $R(T)$ is a subspace of the finite-dimensional space $W$, $\dim(R(T)) = \dim(W)$ if and only if $R(T) = W$, which is the exact definition of $T$ being **onto**.

$$\blacksquare$$
