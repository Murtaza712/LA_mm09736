# Past Exam & Quiz Questions — Midterm II Compilation (MATH 205 Linear Algebra)

This document compiles **every single relevant question and proof** from all files in `past assessments/` (12 exam/solution files and 13 unique quiz solution files) covering the **Midterm II syllabus**:

1. **Vectors in $\mathbb{R}^n$, Dot Product, Norm, Distance, Orthogonality & Inner Product Inequalities**
2. **General Vector Spaces (10 Axioms) & Arithmetic Properties**
3. **Subspaces & The Subspace Test**
4. **Linear Combinations, Span, Linear Independence/Dependence, Bases & Dimension**
5. **Fundamental Matrix Subspaces ($\text{Row}, \text{Col}, \text{Null}$), Rank–Nullity & Consistency Bridges**
6. **Linear Transformations, Standard Matrices, Kernel ($\ker T$), Range ($R(T)$), One-to-One & Onto**

> **Coverage Note:** All 29 files (25 unique after removing exact MD5 duplicates) in `past assessments/` were scanned, including embedded raster/vector equations and `.docx` solution images. Official grading-key solutions are integrated and verified for arithmetic accuracy; printed typos in old exam papers are flagged explicitly. Pure Chapter 1–2 matrix/determinant/LU/Cramer questions (pre-Midterm I) and Chapter 6–7 Gram–Schmidt / Orthogonal Matrix / Eigenvalue / Diagonalization questions (Final-only topics) are listed briefly in the [Appendix](#appendix-files-scanned--excluded-topics) at the end.

---

## Table of Contents & Fast Proof Index

### Topic Sections
- [Part 1: Vectors, Inner Products, Norms & Inequalities](#part-1-vectors-inner-products-norms--inequalities)
- [Part 2: General Vector Spaces (10 Axioms) & Properties](#part-2-general-vector-spaces-10-axioms--properties)
- [Part 3: Subspaces & The Subspace Test](#part-3-subspaces--the-subspace-test)
- [Part 4: Span, Linear Independence, Bases & Dimension](#part-4-span-linear-independence-bases--dimension)
- [Part 5: Row Space, Column Space, Null Space, Rank–Nullity & Consistency](#part-5-row-space-column-space-null-space-ranknullity--consistency)
- [Part 6: Linear Transformations, Standard Matrices, Kernel & Range](#part-6-linear-transformations-standard-matrices-kernel--range)
- [Appendix: Files Scanned & Excluded Topics](#appendix-files-scanned--excluded-topics)

### High-Yield `[PROOF]` Checklist (Every Proof Seen in Past Exams/Quizzes)
| ID | Theorem / Claim | Source(s) |
| :--- | :--- | :--- |
| **Q1.1** | $(\mathbf{u}+\mathbf{v})\cdot\mathbf{w} = \mathbf{u}\cdot\mathbf{w}+\mathbf{v}\cdot\mathbf{w}$ | Sp26 Mid B Q3(a) |
| **Q1.2** | $A\mathbf{u}\cdot\mathbf{v} = \mathbf{u}\cdot A^T\mathbf{v}$ and $\mathbf{u}\cdot A\mathbf{v} = A^T\mathbf{u}\cdot\mathbf{v}$ | F22 Mid Q9(a), Sp26 `MID+B` Q5 |
| **Q1.3** | Unit vector $\frac{1}{\|\mathbf{v}\|}\mathbf{v}$ has norm $1$ | Sp24 Mid B Q2(a) |
| **Q1.4** | Polarization & Parallelogram identities | F22 FE Q1(a), Sp23 FE Q3(b), Quiz 11 P1 |
| **Q1.6** | General Cauchy–Schwarz: $\lvert\langle \mathbf{u},\mathbf{v}\rangle\rvert \le \|\mathbf{u}\|\|\mathbf{v}\|$ | Sp22 FE Q7(a), Sp23 FE Q3(a), Sp24 FE Q8(b), Quiz 11 P2(a) |
| **Q1.7** | Integral Cauchy–Schwarz on $C[0,1]$ | F22 FE Q7 |
| **Q1.8** | Matrix Cauchy–Schwarz: $(\mathbf{v}^T A^T A\mathbf{u})^2 \le (\mathbf{u}^T A^T A\mathbf{u})(\mathbf{v}^T A^T A\mathbf{v})$ | Sp24 Mid B Q5, Sp25 FE P4(a) |
| **Q1.9** | Triangle inequality $\|\mathbf{u}+\mathbf{v}\|\le\|\mathbf{u}\|+\|\mathbf{v}\|$ & norm properties | Sp22 Mid Q5(a), F22 Mid Q9(b), Sp26 Mid B Q3(b), Sp22 FE Q7(b), Quiz 11 P5 |
| **Q1.10** | Distance triangle inequality $d(\mathbf{u},\mathbf{v})\le d(\mathbf{u},\mathbf{w})+d(\mathbf{w},\mathbf{v})$ | Sp22 Mid Q5(b), F22 FE Q1(b) |
| **Q1.11** | Pythagorean theorem for $2$ and $r$ pairwise orthogonal vectors | Sp24 Mid B Q2(b), Quiz 11 P2(b) |
| **Q1.12** | $\mathbf{w}\perp\mathbf{u}_1,\mathbf{u}_2 \implies \mathbf{w}\perp k_1\mathbf{u}_1+k_2\mathbf{u}_2$; $A\mathbf{x}=\mathbf{0}\iff \mathbf{x}\perp$ rows | Sp22 FE Q10, Quiz 11 P6 |
| **Q2.1** | Zero vector space $V=\{\mathbf{0}\}$ satisfies all 10 axioms | Sp24 Mid B Q3 |
| **Q2.2** | Positive reals $(0,\infty)$ under $u+v=uv$, $ku=u^k$ (all 10 axioms / Ax 4–5) | Sp23 Mid Q5, Sp22 Mid Q6(b), F22 FE Q2(a), Sp24 FE Q3 |
| **Q2.4** | Can a vector space have only 2 distinct elements? (Disproof) | Sp22 Mid Q6(a) |
| **Q2.5** | $k\mathbf{0}=\mathbf{0}$ and $(-1)\mathbf{u}=-\mathbf{u}$ in any vector space $V$ | F22 FE Q3(a),(b) |
| **Q3.1** | Two-condition Subspace Test ($W\neq\emptyset$, closed under $+$, scalar mult) | F22 Mid Q7, Sp24 FE Q5 |
| **Q3.2** | One-step subspace test ($k\mathbf{u}+\mathbf{v}\in W$); $W_1\cap W_2$ is a subspace | F22 Mid Q8(a)(i), Sp22 FE Q4(a),(e) |
| **Q3.3–3.5** | Subspace verifications ($P_n$ even, $p'(0)=0$, $p'(1)=0$, matrices, integrals) | Sp25 FE P9(a),(b), Sp22 Mid Q10, Quiz 6 P1, P4–P7 |
| **Q4.1** | $\text{span}\{v_1,\dots,v_r\}$ is the smallest subspace containing $v_1,\dots,v_r$ | F22 FE Q8(a),(b) |
| **Q4.5** | Two vectors LI $\iff$ neither is a scalar multiple; $\{\mathbf{a}-\mathbf{b},\mathbf{b}-\mathbf{c},\mathbf{c}-\mathbf{a}\}$ LD | F22 FE Q2(b), Sp22 Mid Q7(a) |
| **Q4.6** | $S$ LI and $\mathbf{c}\notin\text{span}(S) \implies S\cup\{\mathbf{c}\}$ LI; $S$ LI $\iff$ no vector is LC of others | Sp22 Mid Q7(b), Q8 |
| **Q4.7** | Orthogonal set of nonzero vectors is linearly independent | Sp23 FE Q8, Quiz 11 P4(a) |
| **Q4.8** | $>n$ vectors is LD ($\mathbb{R}^n$ & general $n$-dim $V$); $<n$ vectors does not span | Sp23 Mid Q6, Sp23 FE Q4, Sp24 FE Q2, Sp25 FE P3(a),(b) |
| **Q4.9** | Plus/Minus Basis Theorems (reduce spanning set / extend LI set) | Sp22 Mid Q9, F22 FE Q4(a),(b) |
| **Q4.10** | Half-Test ($\|S\|=n$); $\dim(W)\le\dim(V)$ and $\dim(W)=\dim(V)\implies W=V$ | Sp22 FE Q5(a),(b), Sp24 FE Q4 |
| **Q5.1** | Solution structure of $A\mathbf{x}=\mathbf{b}$ as $\mathbf{x}=\mathbf{x}_1+\mathbf{x}_0$ | Sp22 Mid Q4 |
| **Q5.2** | $A\mathbf{x}=\mathbf{b}$ consistent $\iff \mathbf{b}\in\text{Col}(A)$ | Sp23 FE Q2(a), Sp25 FE P4(b) |
| **Q5.3** | $A\mathbf{x}=\mathbf{b}$ consistent $\forall \mathbf{b}\iff A$ invertible; Master Theorem 4-way cycle | Sp22 FE Q8, Sp24 Mid A Q2, Sp24 FE Q1, Sp23 Mid Q7 |
| **Q5.4** | $\dim(\text{Row}(A))=\dim(\text{Col}(A))$ and $\text{rank}(A)=\text{rank}(A^T)$ | Sp23 FE Q1(a),(b) |
| **Q6.1** | $T(A)=\det(A)$ nonlinear; $T$ 1-to-1 $\iff\ker(T)=\{\mathbf{0}\}$; matrix rep; $\dim R(T_A)=\text{rank}(A)$ | Sp23 FE Q6(c)–(e), Q2(b) |

---

## Part 1: Vectors, Inner Products, Norms & Inequalities

### Q1.1 `[PROOF]` Linearity of Euclidean Dot Product
**Source:** *Spring 2026 Midterm Part B Q3(a) [4 Marks] (+ Official Sol in `MID+B+Solution.docx`)*

> If $\mathbf{u}, \mathbf{v}, \mathbf{w}$ are vectors in $\mathbb{R}^n$, prove that:
> $$(\mathbf{u} + \mathbf{v}) \cdot \mathbf{w} = \mathbf{u} \cdot \mathbf{w} + \mathbf{v} \cdot \mathbf{w}$$

**Solution:**
Let $\mathbf{u} = (u_1, u_2, \dots, u_n)$, $\mathbf{v} = (v_1, v_2, \dots, v_n)$, and $\mathbf{w} = (w_1, w_2, \dots, w_n)$. Then:
$$\begin{aligned}
(\mathbf{u} + \mathbf{v}) \cdot \mathbf{w} &= (u_1 + v_1,\, u_2 + v_2,\, \dots,\, u_n + v_n) \cdot (w_1, w_2, \dots, w_n) \\
&= (u_1 + v_1)w_1 + (u_2 + v_2)w_2 + \dots + (u_n + v_n)w_n \\
&= (u_1 w_1 + u_2 w_2 + \dots + u_n w_n) + (v_1 w_1 + v_2 w_2 + \dots + v_n w_n) \\
&= \mathbf{u} \cdot \mathbf{w} + \mathbf{v} \cdot \mathbf{w}. \quad \blacksquare
\end{aligned}$$

---

### Q1.2 `[PROOF]` Matrix Adjoint Identity for Euclidean Dot Product
**Source:** *Fall 2022 Midterm Q9(a) [~5 Marks]; `MID+B+Solution.docx` Q5*

> Let $\mathbf{u}$ and $\mathbf{v}$ be vectors in $\mathbb{R}^n$ (treated as $n \times 1$ column matrices) and let $A$ be an $n \times n$ matrix. Show:
> - **(Fall 22 Mid Q9a):** $A\mathbf{u} \cdot \mathbf{v} = \mathbf{u} \cdot A^T\mathbf{v}$
> - **(Sp26 `MID+B` Q5):** $\mathbf{u} \cdot A\mathbf{v} = A^T\mathbf{u} \cdot \mathbf{v}$

**Solution:**
First, recall the key bridge between **dot product** and **matrix multiplication** for any $n \times 1$ column vectors $\mathbf{a}, \mathbf{b}$:
$$\mathbf{a} \cdot \mathbf{b} = a_1 b_1 + \dots + a_n b_n = \mathbf{a}^T \mathbf{b} = \mathbf{b}^T \mathbf{a}.$$
*(Using $\mathbf{a}\cdot\mathbf{b} = \mathbf{a}^T\mathbf{b}$ transposes the **first** vector; Howard Anton's convention $\mathbf{a}\cdot\mathbf{b} = \mathbf{b}^T\mathbf{a}$ transposes the **second** vector. Just pick ONE rule and stay consistent!)*

**Using $\mathbf{a} \cdot \mathbf{b} = \mathbf{a}^T \mathbf{b}$ (cleanest):**
1. **For $A\mathbf{u} \cdot \mathbf{v} = \mathbf{u} \cdot A^T\mathbf{v}$:**
   $$A\mathbf{u} \cdot \mathbf{v} = (A\mathbf{u})^T \mathbf{v} = (\mathbf{u}^T A^T) \mathbf{v} = \mathbf{u}^T (A^T \mathbf{v}) = \mathbf{u} \cdot (A^T \mathbf{v}). \quad \blacksquare$$
2. **For $\mathbf{u} \cdot A\mathbf{v} = A^T\mathbf{u} \cdot \mathbf{v}$:**
   $$\mathbf{u} \cdot A\mathbf{v} = \mathbf{u}^T (A\mathbf{v}) = (\mathbf{u}^T A)\mathbf{v} = \big((A^T)^T \text{ trick: } \mathbf{u}^T A = (A^T\mathbf{u})^T\big) = (A^T\mathbf{u})^T \mathbf{v} = A^T\mathbf{u} \cdot \mathbf{v}. \quad \blacksquare$$

**Equivalent `MID+B` official proof (using Anton's convention $\mathbf{a} \cdot \mathbf{b} = \mathbf{b}^T \mathbf{a}$):**
$$\mathbf{u} \cdot A\mathbf{v} = (A\mathbf{v})^T \mathbf{u} = (\mathbf{v}^T A^T) \mathbf{u} = \mathbf{v}^T (A^T \mathbf{u}) = (A^T \mathbf{u}) \cdot \mathbf{v}. \quad \blacksquare$$
*(Why: reading $\mathbf{b}^T \mathbf{a} = \mathbf{a} \cdot \mathbf{b}$ backwards with $\mathbf{b}=\mathbf{v}$ and $\mathbf{a}=A^T\mathbf{u}$ directly gives $\mathbf{v}^T(A^T\mathbf{u}) = (A^T\mathbf{u})\cdot\mathbf{v}$. The official `MID+B` PDF wrote the redundant extra step $(A^T\mathbf{u})\cdot(\mathbf{v}^T)^T$ before simplifying $(\mathbf{v}^T)^T = \mathbf{v}$.)*

---

### Q1.3 `[PROOF]` Normalization of a Nonzero Vector
**Source:** *Spring 2024 Midterm Part B Q2(a) [4 Marks] (+ Official Sol)*

> Show that if $\mathbf{v}$ is a nonzero vector in $\mathbb{R}^n$, then $\dfrac{1}{\|\mathbf{v}\|}\mathbf{v}$ has Euclidean norm $1$.

**Solution:**
Since $\mathbf{v} = (v_1, v_2, \dots, v_n) \neq \mathbf{0}$, we have $\|\mathbf{v}\| = \sqrt{v_1^2 + v_2^2 + \dots + v_n^2} > 0$, so:
$$\frac{1}{\|\mathbf{v}\|}\mathbf{v} = \left(\frac{v_1}{\|\mathbf{v}\|},\, \frac{v_2}{\|\mathbf{v}\|},\, \dots,\, \frac{v_n}{\|\mathbf{v}\|}\right).$$
Taking its Euclidean norm:
$$\left\|\frac{1}{\|\mathbf{v}\|}\mathbf{v}\right\| = \sqrt{\left(\frac{v_1}{\|\mathbf{v}\|}\right)^2 + \left(\frac{v_2}{\|\mathbf{v}\|}\right)^2 + \dots + \left(\frac{v_n}{\|\mathbf{v}\|}\right)^2} = \sqrt{\frac{v_1^2 + v_2^2 + \dots + v_n^2}{v_1^2 + v_2^2 + \dots + v_n^2}} = \sqrt{1} = 1. \quad \blacksquare$$

*(Shorter inner-product version: $\left\|\frac{1}{\|\mathbf{v}\|}\mathbf{v}\right\| = \left|\frac{1}{\|\mathbf{v}\|}\right|\|\mathbf{v}\| = \frac{\|\mathbf{v}\|}{\|\mathbf{v}\|} = 1$.)*

---

### Q1.4 `[PROOF]` Polarization Identity & Parallelogram Law
**Sources:**
- *Fall 2022 FE Q1(a) [5 Marks]* ($\mathbf{u}, \mathbf{v} \in \mathbb{R}^k$: $\mathbf{u}\cdot\mathbf{v} = \frac{1}{4}(\|\mathbf{u}+\mathbf{v}\|^2 - \|\mathbf{u}-\mathbf{v}\|^2)$)
- *Spring 2023 FE Q3(b) [5 Marks]* (General inner product space $V$: $\langle \mathbf{u},\mathbf{v}\rangle = \frac{1}{4}\|\mathbf{u}+\mathbf{v}\|^2 - \frac{1}{4}\|\mathbf{u}-\mathbf{v}\|^2$)
- *Quiz 11 Problem 1(a),(b) (+ Official Sol)* ($\|\mathbf{u}+\mathbf{v}\|^2 + \|\mathbf{u}-\mathbf{v}\|^2 = 2\|\mathbf{u}\|^2 + 2\|\mathbf{v}\|^2$; note Quiz 11 printed missing squares on the RHS, proved with squares in the official key)

> Let $V$ be an inner product space (or $\mathbb{R}^k$ with Euclidean dot product) and let $\mathbf{u}, \mathbf{v} \in V$. Prove:
> - **(a) Parallelogram Law:** $\|\mathbf{u}+\mathbf{v}\|^2 + \|\mathbf{u}-\mathbf{v}\|^2 = 2\|\mathbf{u}\|^2 + 2\|\mathbf{v}\|^2$
> - **(b) Polarization Identity:** $\langle \mathbf{u}, \mathbf{v}\rangle = \dfrac{1}{4}\left(\|\mathbf{u}+\mathbf{v}\|^2 - \|\mathbf{u}-\mathbf{v}\|^2\right)$

**Solution:**
Using the norm definition $\|\mathbf{w}\|^2 = \langle \mathbf{w}, \mathbf{w}\rangle$ along with symmetry and bilinearity (additivity + homogeneity) of the inner product:
$$\begin{aligned}
\|\mathbf{u}+\mathbf{v}\|^2 &= \langle \mathbf{u}+\mathbf{v}, \mathbf{u}+\mathbf{v}\rangle = \langle\mathbf{u},\mathbf{u}\rangle + \langle\mathbf{u},\mathbf{v}\rangle + \langle\mathbf{v},\mathbf{u}\rangle + \langle\mathbf{v},\mathbf{v}\rangle = \|\mathbf{u}\|^2 + 2\langle\mathbf{u},\mathbf{v}\rangle + \|\mathbf{v}\|^2, \\
\|\mathbf{u}-\mathbf{v}\|^2 &= \langle \mathbf{u}-\mathbf{v}, \mathbf{u}-\mathbf{v}\rangle = \langle\mathbf{u},\mathbf{u}\rangle - \langle\mathbf{u},\mathbf{v}\rangle - \langle\mathbf{v},\mathbf{u}\rangle + \langle\mathbf{v},\mathbf{v}\rangle = \|\mathbf{u}\|^2 - 2\langle\mathbf{u},\mathbf{v}\rangle + \|\mathbf{v}\|^2.
\end{aligned}$$
- **(a) Add the two equations:**
  $$\|\mathbf{u}+\mathbf{v}\|^2 + \|\mathbf{u}-\mathbf{v}\|^2 = 2\|\mathbf{u}\|^2 + 2\|\mathbf{v}\|^2. \quad \blacksquare$$
- **(b) Subtract the second from the first:**
  $$\|\mathbf{u}+\mathbf{v}\|^2 - \|\mathbf{u}-\mathbf{v}\|^2 = 4\langle \mathbf{u}, \mathbf{v}\rangle \implies \langle \mathbf{u}, \mathbf{v}\rangle = \frac{1}{4}\left(\|\mathbf{u}+\mathbf{v}\|^2 - \|\mathbf{u}-\mathbf{v}\|^2\right). \quad \blacksquare$$

*(For $\mathbb{R}^k$ specifically, write $\mathbf{u}\cdot\mathbf{v}$ in place of $\langle\mathbf{u},\mathbf{v}\rangle$.)*

---

### Q1.5 `[CALC]` Computing Dot Product from Norms
**Source:** *Quiz 6 Problem 2 (+ Official Sol)*

> Find $\mathbf{u}\cdot\mathbf{v}$ given that $\|\mathbf{u}+\mathbf{v}\| = 3$ and $\|\mathbf{u}-\mathbf{v}\| = 1$.

**Solution:**
Using $\|\mathbf{u}+\mathbf{v}\|^2 = \|\mathbf{u}\|^2 + 2(\mathbf{u}\cdot\mathbf{v}) + \|\mathbf{v}\|^2 = 9$ and $\|\mathbf{u}-\mathbf{v}\|^2 = \|\mathbf{u}\|^2 - 2(\mathbf{u}\cdot\mathbf{v}) + \|\mathbf{v}\|^2 = 1$, subtract the two equations (Polarization Identity):
$$4(\mathbf{u}\cdot\mathbf{v}) = 9 - 1 = 8 \implies \mathbf{u}\cdot\mathbf{v} = 2.$$

---

### Q1.6 `[PROOF]` Cauchy–Schwarz Inequality (General Inner Product Space)
**Sources:** *Spring 2022 FE Q7(a) [7 Marks]; Spring 2023 FE Q3(a) [5 Marks]; Spring 2024 FE Q8(b) [6 Marks]; Quiz 11 P2(a)*

> Let $V$ be a real inner product space with $\mathbf{u}, \mathbf{v} \in V$. Prove that:
> $$|\langle \mathbf{u}, \mathbf{v}\rangle| \le \|\mathbf{u}\|\,\|\mathbf{v}\|$$
> *(Note: Spring 2022 FE Q7(a) had a printed typo writing $\|\mathbf{x}\| = \langle \mathbf{x},\mathbf{x}\rangle$ instead of $\sqrt{\langle \mathbf{x},\mathbf{x}\rangle}$. In standard exams use $\|\mathbf{x}\| = \sqrt{\langle\mathbf{x},\mathbf{x}\rangle}$.)*

**Solution:**
**Case 1: $\mathbf{u} = \mathbf{0}$.**
Then $\|\mathbf{u}\| = 0$ and $\langle \mathbf{0}, \mathbf{v}\rangle = 0$ (since $\langle 0\mathbf{u},\mathbf{v}\rangle = 0\langle\mathbf{u},\mathbf{v}\rangle = 0$). Both sides equal $0$, so $0 \le 0$ holds.

**Case 2: $\mathbf{u} \neq \mathbf{0}$.**
Then $\langle \mathbf{u},\mathbf{u}\rangle = \|\mathbf{u}\|^2 > 0$. Let $t \in \mathbb{R}$ be any real scalar, and consider $\mathbf{w} = t\mathbf{u} + \mathbf{v}$. By positivity of the inner product:
$$\langle t\mathbf{u} + \mathbf{v},\, t\mathbf{u} + \mathbf{v}\rangle \ge 0.$$
Expand using bilinearity and symmetry:
$$t^2\langle\mathbf{u},\mathbf{u}\rangle + 2t\langle\mathbf{u},\mathbf{v}\rangle + \langle\mathbf{v},\mathbf{v}\rangle \ge 0 \implies at^2 + bt + c \ge 0$$
where $a = \langle\mathbf{u},\mathbf{u}\rangle = \|\mathbf{u}\|^2 > 0$, $b = 2\langle\mathbf{u},\mathbf{v}\rangle$, and $c = \langle\mathbf{v},\mathbf{v}\rangle = \|\mathbf{v}\|^2$.
Since this quadratic in $t$ is always $\ge 0$ and opens upward ($a > 0$), it can have at most one real root, so its discriminant must satisfy $\Delta \le 0$:
$$b^2 - 4ac \le 0 \implies \left(2\langle\mathbf{u},\mathbf{v}\rangle\right)^2 - 4\|\mathbf{u}\|^2\|\mathbf{v}\|^2 \le 0 \implies \langle\mathbf{u},\mathbf{v}\rangle^2 \le \|\mathbf{u}\|^2\|\mathbf{v}\|^2.$$
Taking square roots of both nonnegative sides gives:
$$|\langle\mathbf{u},\mathbf{v}\rangle| \le \|\mathbf{u}\|\,\|\mathbf{v}\|. \quad \blacksquare$$

*(Equality holds if and only if $\mathbf{u}$ and $\mathbf{v}$ are linearly dependent.)*

---

### Q1.7 `[PROOF]` Integral Cauchy–Schwarz Inequality on $C[0, 1]$
**Source:** *Fall 2022 FE Q7 [10 Marks]*

> Let $f(x)$ and $g(x)$ be continuous functions on $[0, 1]$. Prove that:
> $$\left(\int_0^1 f(x)g(x)\,dx\right)^2 \le \left(\int_0^1 f^2(x)\,dx\right)\left(\int_0^1 g^2(x)\,dx\right)$$

**Solution:**
Let $V = C[0,1]$ be equipped with the inner product $\langle f, g \rangle = \int_0^1 f(x)g(x)\,dx$, or prove directly:
- **If $\int_0^1 f^2(x)\,dx = 0$:** Since $f^2(x) \ge 0$ is continuous on $[0,1]$, this forces $f(x) \equiv 0$ on $[0,1]$, so both sides equal $0$ and the inequality holds.
- **If $\int_0^1 f^2(x)\,dx > 0$:** For every $t \in \mathbb{R}$, $(tf(x) + g(x))^2 \ge 0$ for all $x \in [0,1]$, hence:
  $$\int_0^1 (tf(x) + g(x))^2\,dx \ge 0.$$
  Expanding the integrand and using linearity of the definite integral:
  $$t^2\left(\int_0^1 f^2(x)\,dx\right) + 2t\left(\int_0^1 f(x)g(x)\,dx\right) + \left(\int_0^1 g^2(x)\,dx\right) \ge 0 \quad \forall t \in \mathbb{R}.$$
  This quadratic $at^2 + bt + c \ge 0$ (with $a = \int_0^1 f^2(x)\,dx > 0$) has non-positive discriminant $b^2 - 4ac \le 0$:
  $$4\left(\int_0^1 f(x)g(x)\,dx\right)^2 - 4\left(\int_0^1 f^2(x)\,dx\right)\left(\int_0^1 g^2(x)\,dx\right) \le 0,$$
  so:
  $$\left(\int_0^1 f(x)g(x)\,dx\right)^2 \le \left(\int_0^1 f^2(x)\,dx\right)\left(\int_0^1 g^2(x)\,dx\right). \quad \blacksquare$$

---

### Q1.8 `[PROOF]` Matrix Cauchy–Schwarz Inequality
**Sources:** *Spring 2024 Midterm Part B Q5 [10 Marks] (+ Official Sol); Spring 2025 FE Solution Problem 4a*

> Prove: If $\mathbf{u}$ and $\mathbf{v}$ are $n \times 1$ matrices and $A$ is an $n \times n$ matrix, then:
> $$(\mathbf{v}^T A^T A \mathbf{u})^2 \le (\mathbf{u}^T A^T A \mathbf{u})(\mathbf{v}^T A^T A \mathbf{v})$$
> *(Typo alert: Spring 2024 Midterm Part B printed $(\mathbf{u}^T A^T A \mathbf{v})$ at the far right instead of $(\mathbf{v}^T A^T A \mathbf{v})$; the Spring 2025 FE Solution corrected it to $\mathbf{v}^T A^T A \mathbf{v}$.)*

**Solution (Official Spring 2025 FE Key):**
Let $\mathbf{x} = A\mathbf{u}$ and $\mathbf{y} = A\mathbf{v}$ in $\mathbb{R}^n$. Observe that:
$$\mathbf{y} \cdot \mathbf{x} = \mathbf{y}^T \mathbf{x} = (A\mathbf{v})^T (A\mathbf{u}) = \mathbf{v}^T A^T A \mathbf{u}.$$
Similarly,
$$\|\mathbf{x}\|^2 = \mathbf{x}^T \mathbf{x} = (A\mathbf{u})^T(A\mathbf{u}) = \mathbf{u}^T A^T A \mathbf{u}, \qquad \|\mathbf{y}\|^2 = \mathbf{y}^T \mathbf{y} = (A\mathbf{v})^T(A\mathbf{v}) = \mathbf{v}^T A^T A \mathbf{v}.$$
Applying the squared Cauchy–Schwarz inequality $(\mathbf{x}\cdot\mathbf{y})^2 \le \|\mathbf{x}\|^2\|\mathbf{y}\|^2$ in $\mathbb{R}^n$:
$$(\mathbf{v}^T A^T A \mathbf{u})^2 \le (\mathbf{u}^T A^T A \mathbf{u})(\mathbf{v}^T A^T A \mathbf{v}). \quad \blacksquare$$

---

### Q1.9 `[PROOF]` Triangle Inequality & Inner Product Norm Properties
**Sources:**
- *Spring 2022 Mid Q5(a) [5 Marks]; Fall 2022 Mid Q9(b); Spring 2026 Mid Part B Q3(b) [6 Marks] (+ `MID+B`)* (in $\mathbb{R}^n$)
- *Spring 2022 FE Q7(b) [3 Marks]; Quiz 11 Problem 5(a)–(c)* (in any inner product space $V$)

> Let $V$ be an inner product space (or $\mathbb{R}^n$) and $\mathbf{u}, \mathbf{v} \in V$. Prove:
> - **(a)** $\|\mathbf{u}\| \ge 0$ *(Quiz 11 P5a)*
> - **(b)** $\|k\mathbf{u}\| = |k|\|\mathbf{u}\|$ *(Quiz 11 P5c)*
> - **(c) Triangle Inequality:** $\|\mathbf{u} + \mathbf{v}\| \le \|\mathbf{u}\| + \|\mathbf{v}\|$

**Solution:**
- **(a)** By definition $\|\mathbf{u}\| = \sqrt{\langle\mathbf{u},\mathbf{u}\rangle}$, and positivity gives $\langle\mathbf{u},\mathbf{u}\rangle \ge 0$, so $\|\mathbf{u}\| \ge 0$.
- **(b)** $\|k\mathbf{u}\| = \sqrt{\langle k\mathbf{u}, k\mathbf{u}\rangle} = \sqrt{k^2\langle\mathbf{u},\mathbf{u}\rangle} = |k|\sqrt{\langle\mathbf{u},\mathbf{u}\rangle} = |k|\|\mathbf{u}\|$.
- **(c) Triangle Inequality:** Compute $\|\mathbf{u}+\mathbf{v}\|^2$:
  $$\begin{aligned}
  \|\mathbf{u}+\mathbf{v}\|^2 &= \langle \mathbf{u}+\mathbf{v}, \mathbf{u}+\mathbf{v}\rangle \\
  &= \|\mathbf{u}\|^2 + 2\langle\mathbf{u},\mathbf{v}\rangle + \|\mathbf{v}\|^2 \\
  &\le \|\mathbf{u}\|^2 + 2|\langle\mathbf{u},\mathbf{v}\rangle| + \|\mathbf{v}\|^2 \qquad (\text{since } x \le |x| \text{ for any } x \in \mathbb{R}) \\
  &\le \|\mathbf{u}\|^2 + 2\|\mathbf{u}\|\|\mathbf{v}\| + \|\mathbf{v}\|^2 \qquad (\text{by the Cauchy–Schwarz inequality}) \\
  &= (\|\mathbf{u}\| + \|\mathbf{v}\|)^2.
  \end{aligned}$$
  Since both $\|\mathbf{u}+\mathbf{v}\|$ and $\|\mathbf{u}\|+\|\mathbf{v}\|$ are nonnegative, taking square roots yields:
  $$\|\mathbf{u}+\mathbf{v}\| \le \|\mathbf{u}\| + \|\mathbf{v}\|. \quad \blacksquare$$

---

### Q1.10 `[PROOF]` Triangle Inequality for Distance
**Sources:** *Spring 2022 Mid Q5(b) [5 Marks]; Fall 2022 FE Q1(b) [5 Marks]*

> If $\mathbf{u}, \mathbf{v}, \mathbf{w}$ are vectors in $\mathbb{R}^n$, show that:
> $$d(\mathbf{u}, \mathbf{v}) \le d(\mathbf{u}, \mathbf{w}) + d(\mathbf{w}, \mathbf{v})$$

**Solution:**
Recall the Euclidean distance $d(\mathbf{a}, \mathbf{b}) = \|\mathbf{a} - \mathbf{b}\|$. Write $\mathbf{u} - \mathbf{v} = (\mathbf{u} - \mathbf{w}) + (\mathbf{w} - \mathbf{v})$ and apply the norm triangle inequality $\|\mathbf{x}+\mathbf{y}\| \le \|\mathbf{x}\|+\|\mathbf{y}\|$ with $\mathbf{x}=\mathbf{u}-\mathbf{w}$ and $\mathbf{y}=\mathbf{w}-\mathbf{v}$:
$$d(\mathbf{u}, \mathbf{v}) = \|\mathbf{u} - \mathbf{v}\| = \|(\mathbf{u} - \mathbf{w}) + (\mathbf{w} - \mathbf{v})\| \le \|\mathbf{u} - \mathbf{w}\| + \|\mathbf{w} - \mathbf{v}\| = d(\mathbf{u}, \mathbf{w}) + d(\mathbf{w}, \mathbf{v}). \quad \blacksquare$$

---

### Q1.11 `[PROOF]` Pythagorean Theorem for Two and $r$ Pairwise Orthogonal Vectors
**Sources:** *Quiz 11 Problem 2(b) (+ Official Sol); Spring 2024 Mid Part B Q2(b) [6 Marks] (+ Official Sol)*

> - **(a)** If $\mathbf{u} \perp \mathbf{v}$ in an inner product space $V$, prove that $\|\mathbf{u}+\mathbf{v}\|^2 = \|\mathbf{u}\|^2 + \|\mathbf{v}\|^2$.
> - **(b)** Show that if $\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_r$ are pairwise orthogonal vectors in $\mathbb{R}^n$, then:
>   $$\|\mathbf{v}_1 + \mathbf{v}_2 + \dots + \mathbf{v}_r\|^2 = \|\mathbf{v}_1\|^2 + \|\mathbf{v}_2\|^2 + \dots + \|\mathbf{v}_r\|^2$$

**Solution:**
- **(a)** Since $\mathbf{u}\perp\mathbf{v}$, $\langle\mathbf{u},\mathbf{v}\rangle = 0$. Therefore:
  $$\|\mathbf{u}+\mathbf{v}\|^2 = \langle \mathbf{u}+\mathbf{v}, \mathbf{u}+\mathbf{v}\rangle = \|\mathbf{u}\|^2 + 2\langle\mathbf{u},\mathbf{v}\rangle + \|\mathbf{v}\|^2 = \|\mathbf{u}\|^2 + \|\mathbf{v}\|^2.$$
- **(b)** Since $\mathbf{v}_1$ is orthogonal to $\mathbf{v}_2, \dots, \mathbf{v}_r$, we have $\mathbf{v}_1 \cdot (\mathbf{v}_2 + \dots + \mathbf{v}_r) = \mathbf{v}_1\cdot\mathbf{v}_2 + \dots + \mathbf{v}_1\cdot\mathbf{v}_r = 0$. Applying part (a) repeatedly (induction / $r-1$ steps):
  $$\begin{aligned}
  \|\mathbf{v}_1 + \mathbf{v}_2 + \dots + \mathbf{v}_r\|^2 &= \|\mathbf{v}_1 + (\mathbf{v}_2 + \dots + \mathbf{v}_r)\|^2 \\
  &= \|\mathbf{v}_1\|^2 + \|\mathbf{v}_2 + \dots + \mathbf{v}_r\|^2 \\
  &= \|\mathbf{v}_1\|^2 + \|\mathbf{v}_2\|^2 + \dots + \|\mathbf{v}_r\|^2. \quad \blacksquare
  \end{aligned}$$
  *(Equivalently, expand $(\sum_{i=1}^r \mathbf{v}_i)\cdot(\sum_{j=1}^r \mathbf{v}_j) = \sum_{i=1}^r \|\mathbf{v}_i\|^2 + \sum_{i\neq j}\mathbf{v}_i\cdot\mathbf{v}_j = \sum_{i=1}^r \|\mathbf{v}_i\|^2$ since $\mathbf{v}_i\cdot\mathbf{v}_j = 0$ for $i\neq j$.)*

---

### Q1.12 `[PROOF]` Orthogonality to Span & Row-Orthogonality of $\text{Null}(A)$
**Sources:** *Quiz 11 Problem 6 (+ Official Sol); Spring 2022 FE Q10 [10 Marks]*

> - **(a) (Quiz 11 P6):** Let $V$ be an inner product space. Show that if $\mathbf{w}$ is orthogonal to both $\mathbf{u}_1$ and $\mathbf{u}_2$, it is orthogonal to $k_1\mathbf{u}_1 + k_2\mathbf{u}_2$ for all scalars $k_1, k_2$. Interpret geometrically in $\mathbb{R}^3$.
> - **(b) (Sp22 FE Q10):** Let $A\mathbf{x} = \mathbf{0}$ be a homogeneous system where $A$ is $m \times n$. Prove that $\mathbf{x} = [x_1, x_2, \dots, x_n]^T$ is a solution if and only if $\mathbf{x}$ is orthogonal to every row vector of $A$ (Euclidean inner product).

**Solution:**
- **(a)** Suppose $\langle \mathbf{w}, \mathbf{u}_1\rangle = 0$ and $\langle \mathbf{w}, \mathbf{u}_2\rangle = 0$. By bilinearity of the inner product:
  $$\langle \mathbf{w}, k_1\mathbf{u}_1 + k_2\mathbf{u}_2\rangle = k_1\langle \mathbf{w}, \mathbf{u}_1\rangle + k_2\langle \mathbf{w}, \mathbf{u}_2\rangle = k_1(0) + k_2(0) = 0.$$
  *Geometric interpretation in $\mathbb{R}^3$:* If $\mathbf{u}_1, \mathbf{u}_2$ are non-collinear, $\text{span}\{\mathbf{u}_1, \mathbf{u}_2\}$ is a plane through the origin; $\mathbf{w}$ is orthogonal to every vector in the plane (i.e., $\mathbf{w}$ is a normal vector to the plane).
- **(b)** Let $\mathbf{r}_1, \mathbf{r}_2, \dots, \mathbf{r}_m$ be the row vectors of $A$. By definition of matrix multiplication, the $i$-th entry of $A\mathbf{x}$ is the Euclidean dot product $\mathbf{r}_i \cdot \mathbf{x}$:
  $$A\mathbf{x} = \begin{bmatrix} \mathbf{r}_1 \cdot \mathbf{x} \\ \mathbf{r}_2 \cdot \mathbf{x} \\ \vdots \\ \mathbf{r}_m \cdot \mathbf{x} \end{bmatrix}.$$
  Therefore:
  $$A\mathbf{x} = \mathbf{0} \iff \mathbf{r}_i \cdot \mathbf{x} = 0 \text{ for all } i = 1, \dots, m \iff \mathbf{x} \text{ is orthogonal to every row vector of } A. \quad \blacksquare$$

---

### Q1.13 `[CALC]` Orthogonal Unit Vectors in $\mathbb{R}^4$
**Source:** *Quiz 6 Problem 3 (+ Official Sol)*

> Find two vectors of norm $1$ that are orthogonal to $\mathbf{u} = (2, 1, -4, 0)$ and $\mathbf{v} = (-1, -1, 2, 2)$.

**Solution:**
Let $\mathbf{w} = (w_1, w_2, w_3, w_4)$. Orthogonality requires:
1. $\mathbf{u} \cdot \mathbf{w} = 2w_1 + w_2 - 4w_3 = 0 \implies w_2 = -2w_1 + 4w_3$,
2. $\mathbf{v} \cdot \mathbf{w} = -w_1 - w_2 + 2w_3 + 2w_4 = 0$.

Substitute $w_2$ into (2):
$$-w_1 - (-2w_1 + 4w_3) + 2w_3 + 2w_4 = 0 \implies w_1 - 2w_3 + 2w_4 = 0 \implies w_1 = 2w_3 - 2w_4.$$
Then $w_2 = -2(2w_3 - 2w_4) + 4w_3 = 4w_4$. Setting $w_3 = s, w_4 = t$ gives $\mathbf{w} = (2s - 2t,\, 4t,\, s,\, t)$.
- Take $s = 1, t = 0$: $\mathbf{a} = (2, 0, 1, 0)$ has $\|\mathbf{a}\| = \sqrt{5}$, giving $\mathbf{w}_1 = \left(\dfrac{2}{\sqrt{5}},\, 0,\, \dfrac{1}{\sqrt{5}},\, 0\right)$.
- Take $s = 0, t = 1$: $\mathbf{b} = (-2, 4, 0, 1)$ has $\|\mathbf{b}\| = \sqrt{4 + 16 + 1} = \sqrt{21}$, giving $\mathbf{w}_2 = \left(-\dfrac{2}{\sqrt{21}},\, \dfrac{4}{\sqrt{21}},\, 0,\, \dfrac{1}{\sqrt{21}}\right)$.

---

### Q1.14 `[CALC]` Integral Inner Product Evaluation
**Source:** *Spring 2023 FE Q5(a) [4 Marks]*

> Use the inner product $\langle \mathbf{f} \mid \mathbf{g}\rangle = \int_0^1 f(x)g(x)\,dx$ to compute $\langle \mathbf{f} \mid \mathbf{g}\rangle$ for $\mathbf{f} = \cos 2\pi x$ and $\mathbf{g} = \sin 2\pi x$.

**Solution:**
$$\langle \mathbf{f} \mid \mathbf{g}\rangle = \int_0^1 \cos(2\pi x)\sin(2\pi x)\,dx = \frac{1}{2}\int_0^1 \sin(4\pi x)\,dx = \frac{1}{2}\left[-\frac{\cos(4\pi x)}{4\pi}\right]_0^1 = -\frac{1}{8\pi}\big(\cos(4\pi) - \cos(0)\big) = -\frac{1}{8\pi}(1 - 1) = 0.$$

---

## Part 2: General Vector Spaces (10 Axioms) & Properties

### Q2.1 `[PROOF]` The Zero Vector Space $V = \{0\}$ (All 10 Axioms)
**Source:** *Spring 2024 Midterm Part B Q3 [10 Marks] (+ Official Sol)*

> Let $V$ consist of a single object, denoted by $\mathbf{0}$, and define $\mathbf{0} + \mathbf{0} = \mathbf{0}$ and $k\mathbf{0} = \mathbf{0}$ for all scalars $k$. Show that $V$ is a vector space.

**Solution:**
Let $\mathbf{u}, \mathbf{v}, \mathbf{w} \in V$. Since $V = \{\mathbf{0}\}$, we necessarily have $\mathbf{u} = \mathbf{v} = \mathbf{w} = \mathbf{0}$. Verify all 10 axioms:
1. **Closure under addition:** $\mathbf{u} + \mathbf{v} = \mathbf{0} + \mathbf{0} = \mathbf{0} \in V$.
2. **Commutativity:** $\mathbf{u} + \mathbf{v} = \mathbf{0} + \mathbf{0} = \mathbf{v} + \mathbf{u}$.
3. **Associativity:** $\mathbf{u} + (\mathbf{v} + \mathbf{w}) = \mathbf{0} + (\mathbf{0} + \mathbf{0}) = \mathbf{0} + \mathbf{0} = (\mathbf{0} + \mathbf{0}) + \mathbf{0} = (\mathbf{u} + \mathbf{v}) + \mathbf{w}$.
4. **Zero vector (Additive identity):** Since $\mathbf{0} \in V$, $\mathbf{0} + \mathbf{u} = \mathbf{u} + \mathbf{0} = \mathbf{0} + \mathbf{0} = \mathbf{0} = \mathbf{u}$.
5. **Additive inverse:** Choose $-\mathbf{u} = \mathbf{0} \in V$; then $\mathbf{u} + (-\mathbf{u}) = (-\mathbf{u}) + \mathbf{u} = \mathbf{0} + \mathbf{0} = \mathbf{0}$.
6. **Closure under scalar multiplication:** For any $k \in \mathbb{R}$, $k\mathbf{u} = k\mathbf{0} = \mathbf{0} \in V$.
7. **Distributivity (scalar over vector sum):** $k(\mathbf{u} + \mathbf{v}) = k(\mathbf{0} + \mathbf{0}) = k\mathbf{0} = \mathbf{0} = \mathbf{0} + \mathbf{0} = k\mathbf{0} + k\mathbf{0} = k\mathbf{u} + k\mathbf{v}$.
8. **Distributivity (vector over scalar sum):** $(k + l)\mathbf{u} = (k + l)\mathbf{0} = \mathbf{0} = \mathbf{0} + \mathbf{0} = k\mathbf{0} + l\mathbf{0} = k\mathbf{u} + l\mathbf{u}$.
9. **Associativity of scalar multiplication:** $k(l\mathbf{u}) = k(l\mathbf{0}) = k\mathbf{0} = \mathbf{0} = (kl)\mathbf{0} = (kl)\mathbf{u}$.
10. **Multiplicative identity of $1$:** $1\mathbf{u} = 1\mathbf{0} = \mathbf{0} = \mathbf{u}$.

All 10 axioms hold, so $V = \{\mathbf{0}\}$ is a vector space. $\blacksquare$

---

### Q2.2 `[PROOF]` Positive Reals $V = (0, \infty)$ with $u \oplus v = uv$ and $k \odot u = u^k$
**Sources:**
- *Spring 2023 Midterm Q5 [10 Marks]* (Full proof of **all 10 axioms**)
- *Spring 2022 Midterm Q6(b) [5 Marks]* (Identify zero element & show Axiom 4)
- *Fall 2022 FE Q2(a) [6 Marks] & Spring 2024 FE Q3 [6 Marks]* (Identify $\mathbf{0}$ and $-\mathbf{u}$, prove Axioms 4 & 5)

> Consider the set $V = S = (0, \infty)$ of all positive real numbers with operations:
> - Vector addition: $\mathbf{u} \oplus \mathbf{v} = uv$ (ordinary multiplication)
> - Scalar multiplication: $k \odot \mathbf{u} = u^k$ (exponentiation, $k \in \mathbb{R}$)
>
> **(A)** Prove $V$ is a vector space (all 10 axioms).
> **(B)** Identify the zero vector $\mathbf{0}$ and negative $-\mathbf{u}$, and verify Axioms 4 & 5.

**Solution:**
Let $u, v, w \in (0, \infty)$ and $k, m \in \mathbb{R}$.
1. **Closure under addition:** Since $u > 0$ and $v > 0$, $u \oplus v = uv > 0$, so $u \oplus v \in V$.
2. **Commutativity:** $u \oplus v = uv = vu = v \oplus u$.
3. **Associativity:** $(u \oplus v) \oplus w = (uv)w = u(vw) = u \oplus (v \oplus w)$.
4. **Zero vector (Additive identity):** Choose $\mathbf{0}_V = 1$ (note $1 \in (0, \infty)$!). Check Axiom 4:
   $$u \oplus \mathbf{0}_V = u \cdot 1 = u, \qquad \mathbf{0}_V \oplus u = 1 \cdot u = u.$$
5. **Additive inverse:** For each $u \in (0, \infty)$, define $-\mathbf{u} = \dfrac{1}{u} = u^{-1}$ (which is $> 0$, hence in $V$). Check Axiom 5:
   $$u \oplus (-\mathbf{u}) = u \cdot \frac{1}{u} = 1 = \mathbf{0}_V, \qquad (-\mathbf{u}) \oplus u = \frac{1}{u} \cdot u = 1 = \mathbf{0}_V.$$
6. **Closure under scalar multiplication:** Since $u > 0$ and $k \in \mathbb{R}$, $k \odot u = u^k > 0$, so $k \odot u \in V$.
7. **Scalar distributivity over vector addition:**
   $$k \odot (u \oplus v) = (uv)^k = u^k v^k = (k \odot u) \oplus (k \odot v).$$
8. **Vector distributivity over scalar addition:**
   $$(k + m) \odot u = u^{k+m} = u^k u^m = (k \odot u) \oplus (m \odot u).$$
9. **Scalar associativity:**
   $$k \odot (m \odot u) = k \odot (u^m) = (u^m)^k = u^{mk} = u^{km} = (km) \odot u.$$
10. **Scalar identity $1$:**
    $$1 \odot u = u^1 = u.$$

Hence $V = (0, \infty)$ is a vector space (and parts (B) follow directly from Axioms 4 & 5 with $\mathbf{0}_V = 1$ and $-\mathbf{u} = 1/u$). $\blacksquare$

---

### Q2.3 `[CHECK]` Disproving a Candidate Vector Space & Finding ALL Failed Axioms
**Source:** *Fall 2022 Midterm Q6 [10 Marks]*

> Check whether the set $V = \mathbb{R}^3$ of all triples of real numbers with standard vector addition $\mathbf{u} + \mathbf{v} = (x_1+x_2,\, y_1+y_2,\, z_1+z_2)$ and scalar multiplication defined by:
> $$k(x, y, z) = (k^2 x,\, k^2 y,\, k^2 z)$$
> is a vector space or not. If not, **identify all axioms that fail to hold**.

**Solution:**
Let's systematically check all 10 axioms (for arbitrary $\mathbf{u}=(x_1,y_1,z_1), \mathbf{v}=(x_2,y_2,z_2) \in \mathbb{R}^3$ and $k, m \in \mathbb{R}$):

- **Axioms 1–5 (Addition only):** Standard addition on $\mathbb{R}^3$ is unchanged, so Axioms **1, 2, 3, 4, 5 all HOLD** ($\mathbf{0} = (0,0,0)$ and $-\mathbf{u} = (-x_1,-y_1,-z_1)$).
- **Axiom 6 (Closure under scalar multiplication):** $k(x,y,z) = (k^2x, k^2y, k^2z) \in \mathbb{R}^3$. **HOLDS.**
- **Axiom 7 ($k(\mathbf{u}+\mathbf{v}) = k\mathbf{u}+k\mathbf{v}$):**
  - LHS: $k(x_1+x_2, y_1+y_2, z_1+z_2) = (k^2(x_1+x_2), k^2(y_1+y_2), k^2(z_1+z_2))$.
  - RHS: $(k^2x_1, k^2y_1, k^2z_1) + (k^2x_2, k^2y_2, k^2z_2) = (k^2x_1+k^2x_2, k^2y_1+k^2y_2, k^2z_1+k^2z_2)$.
  - Since LHS $=$ RHS, Axiom **7 HOLDS.**
- **Axiom 8 ($(k+m)\mathbf{u} = k\mathbf{u}+m\mathbf{u}$):** **FAILS!**
  - LHS: $(k+m)\mathbf{u} = \big((k+m)^2 x, (k+m)^2 y, (k+m)^2 z\big) = \big((k^2+2km+m^2)x, \dots\big)$.
  - RHS: $k\mathbf{u}+m\mathbf{u} = \big((k^2+m^2)x, (k^2+m^2)y, (k^2+m^2)z\big)$.
  - Counterexample: take $k=1, m=1, \mathbf{u}=(1,0,0)$: LHS $= 2(1,0,0) = (4,0,0)$, whereas RHS $= 1(1,0,0) + 1(1,0,0) = (1,0,0)+(1,0,0) = (2,0,0) \neq (4,0,0)$.
- **Axiom 9 ($k(m\mathbf{u}) = (km)\mathbf{u}$):**
  - LHS: $k(m^2 x, m^2 y, m^2 z) = (k^2 m^2 x, k^2 m^2 y, k^2 m^2 z)$.
  - RHS: $((km)^2 x, (km)^2 y, (km)^2 z) = (k^2 m^2 x, k^2 m^2 y, k^2 m^2 z)$.
  - Wait — Axiom **9 HOLDS!**
- **Axiom 10 ($1\mathbf{u} = \mathbf{u}$):**
  - $1(x,y,z) = (1^2 x, 1^2 y, 1^2 z) = (x,y,z)$. Axiom **10 HOLDS.**

**Conclusion:** $V$ is **NOT** a vector space. **Only Axiom 8 fails** (Axioms 1–7, 9, and 10 all hold).

---

### Q2.4 `[PROOF]` Can a Vector Space Contain Only Two Distinct Elements?
**Source:** *Spring 2022 Midterm Q6(a) [5 Marks]*

> Prove or disprove the following claim: *"It is possible for a vector space (over $\mathbb{R}$) to contain only two distinct elements."*

**Solution:**
The claim is **FALSE** (disprove by contradiction).
Suppose $V$ is a real vector space with $|V| = 2$. Since every vector space contains a zero vector $\mathbf{0}$, there must exist some nonzero vector $\mathbf{v} \in V$ ($\mathbf{v} \neq \mathbf{0}$), so $V = \{\mathbf{0}, \mathbf{v}\}$.
By Axiom 6 (closure under scalar multiplication by any real scalar $k \in \mathbb{R}$), both $2\mathbf{v}$ and $\mathbf{v}$ must belong to $V$, and in particular $2\mathbf{v} \in \{\mathbf{0}, \mathbf{v}\}$:
- If $2\mathbf{v} = \mathbf{0}$, multiply both sides by $\frac{1}{2}$: $\frac{1}{2}(2\mathbf{v}) = \frac{1}{2}\mathbf{0} \implies \mathbf{v} = \mathbf{0}$, contradicting $\mathbf{v} \neq \mathbf{0}$.
- If $2\mathbf{v} = \mathbf{v}$, add $-\mathbf{v}$ to both sides: $2\mathbf{v} - \mathbf{v} = \mathbf{0} \implies (2-1)\mathbf{v} = \mathbf{0} \implies \mathbf{v} = \mathbf{0}$, again contradicting $\mathbf{v} \neq \mathbf{0}$.

Hence $2\mathbf{v}$ cannot equal either $\mathbf{0}$ or $\mathbf{v}$, so $V$ must contain infinitely many distinct elements ($k\mathbf{v}$ for all $k \in \mathbb{R}$ are distinct). A real vector space can only have $1$ element ($V = \{\mathbf{0}\}$) or infinitely many elements—never $2$. $\blacksquare$

---

### Q2.5 `[PROOF]` Fundamental Arithmetic Properties in Any Vector Space
**Source:** *Fall 2022 FE Q3(a),(b) [5+5 Marks]*

> Let $V$ be a vector space, $\mathbf{u} \in V$, and $k$ a scalar. Prove:
> - **(a)** $k\mathbf{0} = \mathbf{0}$
> - **(b)** $(-1)\mathbf{u} = -\mathbf{u}$

**Solution:**
- **(a) Prove $k\mathbf{0} = \mathbf{0}$:**
  By Axiom 4, $\mathbf{0} + \mathbf{0} = \mathbf{0}$. Multiplying both sides by $k$ and applying Axiom 7:
  $$k\mathbf{0} = k(\mathbf{0} + \mathbf{0}) = k\mathbf{0} + k\mathbf{0}.$$
  Add the additive inverse $-(k\mathbf{0})$ (which exists by Axiom 5) to both sides:
  $$k\mathbf{0} + \big(-(k\mathbf{0})\big) = (k\mathbf{0} + k\mathbf{0}) + \big(-(k\mathbf{0})\big).$$
  By Axioms 3, 5, and 4:
  $$\mathbf{0} = k\mathbf{0} + \Big(k\mathbf{0} + \big(-(k\mathbf{0})\big)\Big) = k\mathbf{0} + \mathbf{0} = k\mathbf{0}. \quad \blacksquare$$

- **(b) Prove $(-1)\mathbf{u} = -\mathbf{u}$:**
  We must show that $(-1)\mathbf{u}$ satisfies the defining property of the additive inverse of $\mathbf{u}$, namely $\mathbf{u} + (-1)\mathbf{u} = \mathbf{0}$:
  $$\begin{aligned}
  \mathbf{u} + (-1)\mathbf{u} &= 1\mathbf{u} + (-1)\mathbf{u} \qquad (\text{Axiom 10}) \\
  &= \big(1 + (-1)\big)\mathbf{u} \qquad (\text{Axiom 8}) \\
  &= 0\mathbf{u} \\
  &= \mathbf{0} \qquad (\text{since } 0\mathbf{u} = (0+0)\mathbf{u} = 0\mathbf{u}+0\mathbf{u} \implies 0\mathbf{u} = \mathbf{0}).
  \end{aligned}$$
  By Axiom 2, $(-1)\mathbf{u} + \mathbf{u} = \mathbf{0}$ as well. Since additive inverses are unique (add $-\mathbf{u}$ to $\mathbf{u}+(-1)\mathbf{u}=\mathbf{0}$), it follows that $(-1)\mathbf{u} = -\mathbf{u}$. $\blacksquare$

---

## Part 3: Subspaces & The Subspace Test

### Q3.1 `[PROOF]` The Two-Condition Subspace Test
**Sources:** *Fall 2022 Midterm Q7 [10 Marks]; Spring 2024 FE Q5 [10 Marks]*

> **Prove:** If $W$ is a set of one or more vectors from a vector space $V$, then $W$ is a subspace of $V$ if and only if:
> - **(a)** If $\mathbf{u}, \mathbf{v} \in W$, then $\mathbf{u} + \mathbf{v} \in W$.
> - **(b)** If $k$ is any scalar and $\mathbf{u} \in W$, then $k\mathbf{u} \in W$.

**Solution:**
- **($\Rightarrow$) Forward Direction:**
  Assume $W$ is a subspace of $V$. By definition, $W$ is itself a vector space under the addition and scalar multiplication of $V$. Therefore, it satisfies **Axiom 1** (closure under addition, which is condition (a)) and **Axiom 6** (closure under scalar multiplication, which is condition (b)).

- **($\Leftarrow$) Converse Direction:**
  Assume $W$ is nonempty and conditions (a) and (b) hold. To show $W$ is a subspace of $V$, we must verify all 10 vector space axioms for $W$:
  - **Axiom 1** holds by condition (a).
  - **Axiom 6** holds by condition (b).
  - **Axioms 2, 3, 7, 8, 9, 10** hold automatically for all vectors in $W$ because every vector in $W$ also belongs to the parent vector space $V$, where these equality-based algebraic laws already hold.
  - **Axiom 4 (Zero vector $\mathbf{0} \in W$):** Since $W$ has at least one vector, pick any $\mathbf{u} \in W$. Setting $k = 0$ in condition (b) gives $0\mathbf{u} \in W$. Since $0\mathbf{u} = \mathbf{0}$ in $V$, we have $\mathbf{0} \in W$ (and $\mathbf{u}+\mathbf{0}=\mathbf{0}+\mathbf{u}=\mathbf{u}$).
  - **Axiom 5 (Additive inverses in $W$):** For any $\mathbf{u} \in W$, setting $k = -1$ in condition (b) gives $(-1)\mathbf{u} \in W$. Since $(-1)\mathbf{u} = -\mathbf{u}$ in $V$, we have $-\mathbf{u} \in W$ (and $\mathbf{u}+(-\mathbf{u})=\mathbf{0}$).

  Since all 10 axioms hold in $W$, $W$ is a subspace of $V$. $\blacksquare$

---

### Q3.2 `[T/F + PROOF]` One-Step Subspace Test & Intersection of Two Subspaces
**Sources:** *Fall 2022 Mid Q8(a)(i); Spring 2022 FE Q4(a), Q4(e)*

> Indicate whether each statement is **always true** or **sometimes false**, and justify:
> - **(a)** *The intersection of two subspaces of a vector space $V$ is also a subspace of $V$.* *(Sp22 FE Q4a)*
> - **(b)** *If $W$ is a nonempty set of vectors from a vector space $V$, and $k\mathbf{u} + \mathbf{v} \in W$ for all $\mathbf{u}, \mathbf{v} \in W$ and all scalars $k \in \mathbb{R}$, then $W$ is a subspace of $V$.* *(F22 Mid Q8a(i), Sp22 FE Q4e)*

**Solution:**
- **(a) ALWAYS TRUE.** Let $W_1, W_2$ be subspaces of $V$, and $W = W_1 \cap W_2$.
  1. Since $\mathbf{0} \in W_1$ and $\mathbf{0} \in W_2$, we have $\mathbf{0} \in W$, so $W \neq \emptyset$.
  2. If $\mathbf{u}, \mathbf{v} \in W$, then $\mathbf{u}, \mathbf{v} \in W_1$ (so $\mathbf{u}+\mathbf{v} \in W_1$) and $\mathbf{u}, \mathbf{v} \in W_2$ (so $\mathbf{u}+\mathbf{v} \in W_2$). Hence $\mathbf{u}+\mathbf{v} \in W_1 \cap W_2 = W$.
  3. If $k \in \mathbb{R}$ and $\mathbf{u} \in W$, then $k\mathbf{u} \in W_1$ and $k\mathbf{u} \in W_2$, so $k\mathbf{u} \in W$.
  By the Subspace Test, $W_1 \cap W_2$ is a subspace of $V$.

- **(b) ALWAYS TRUE.** Given $W \neq \emptyset$ and $k\mathbf{u}+\mathbf{v} \in W$ for all $\mathbf{u}, \mathbf{v} \in W, k \in \mathbb{R}$:
  1. **Closed under addition:** Set $k = 1$; then $1\mathbf{u} + \mathbf{v} = \mathbf{u} + \mathbf{v} \in W$ for all $\mathbf{u}, \mathbf{v} \in W$.
  2. **Zero vector is in $W$:** Pick any $\mathbf{u}_0 \in W$ (exists since $W \neq \emptyset$) and set $\mathbf{u}=\mathbf{v}=\mathbf{u}_0, k=-1$; then $(-1)\mathbf{u}_0 + \mathbf{u}_0 = \mathbf{0} \in W$.
  3. **Closed under scalar multiplication:** For any $\mathbf{u} \in W$ and $k \in \mathbb{R}$, set $\mathbf{v} = \mathbf{0} \in W$; then $k\mathbf{u} + \mathbf{0} = k\mathbf{u} \in W$.
  By the Subspace Test, $W$ is a subspace of $V$.

---

### Q3.3 `[PROOF + CALC]` Subspaces of Polynomials $P_n$
**Sources:** *Spring 2025 FE Solution P9(a),(b); Spring 2022 Midterm Q10 [10 Marks]*

> - **(a) (Sp25 FE P9a):** Show that $W_1 = \{p(x) \in P_n : p(-x) = p(x)\}$ (even polynomials) is a subspace of $P_n$.
> - **(b) (Sp25 FE P9b):** Show that $W_2 = \{p(x) \in P_n : p'(0) = 0\}$ is a subspace of $P_n$, and find a basis for $W_2$.
> - **(c) (Sp22 Mid Q10):** Show that the set $W_3$ of all polynomials in $P_n$ that have a horizontal tangent at $x = 1$ (i.e., $p'(1) = 0$) is a subspace of $P_n$.

**Solution:**
- **(a)** Let $W_1 = \{p \in P_n : p(-x) = p(x)\}$:
  1. **Zero polynomial:** $0(-x) = 0 = 0(x) \implies 0 \in W_1$ ($W_1 \neq \emptyset$).
  2. **Addition:** If $p, q \in W_1$, then $(p+q)(-x) = p(-x)+q(-x) = p(x)+q(x) = (p+q)(x) \implies p+q \in W_1$.
  3. **Scalar mult:** If $p \in W_1, c \in \mathbb{R}$, then $(cp)(-x) = c\,p(-x) = c\,p(x) = (cp)(x) \implies cp \in W_1$.
  Hence $W_1$ is a subspace of $P_n$. $\blacksquare$

- **(b)** Let $W_2 = \{p \in P_n : p'(0) = 0\}$:
  1. **Zero polynomial:** $0'(x) = 0 \implies 0'(0) = 0 \implies 0 \in W_2$.
  2. **Addition:** If $p, q \in W_2$, $(p+q)'(0) = p'(0) + q'(0) = 0 + 0 = 0 \implies p+q \in W_2$.
  3. **Scalar mult:** If $p \in W_2, c \in \mathbb{R}$, $(cp)'(0) = c\,p'(0) = c \cdot 0 = 0 \implies cp \in W_2$.
  Thus $W_2$ is a subspace of $P_n$.
  - **Basis (for $n \ge 2$; if $n=0,1$ just $\{1\}$):** Any $p(x) = a_0 + a_1 x + a_2 x^2 + \dots + a_n x^n \in P_n$ has $p'(x) = a_1 + 2a_2 x + \dots + n a_n x^{n-1}$, so $p'(0) = a_1$. Thus $p \in W_2 \iff a_1 = 0 \iff p(x) = a_0 + a_2 x^2 + \dots + a_n x^n$. Since $\{1, x^2, x^3, \dots, x^n\}$ spans $W_2$ and is a subset of the linearly independent standard basis $\{1,x,\dots,x^n\}$, it is a **basis for $W_2$**:
    $$\text{Basis for } W_2 = \{1, x^2, x^3, \dots, x^n\} \quad (\text{or } \{1\} \text{ if } n \le 1).$$

- **(c)** Horizontal tangent at $x=1$ means $p'(1) = 0$, so $W_3 = \{p \in P_n : p'(1) = 0\}$.
  1. **Zero polynomial:** $p(x) = 0 \implies p'(x) = 0 \implies p'(1) = 0 \implies 0 \in W_3$ ($W_3 \neq \emptyset$).
  2. **Addition:** Let $p, q \in W_3$, so $p'(1) = 0$ and $q'(1) = 0$. By linearity of differentiation, $(p+q)'(1) = p'(1) + q'(1) = 0 + 0 = 0 \implies p+q \in W_3$.
  3. **Scalar mult:** Let $p \in W_3$ and $k \in \mathbb{R}$. Then $(kp)'(1) = k\,p'(1) = k(0) = 0 \implies kp \in W_3$.
  By the Subspace Test, $W_3$ is a subspace of $P_n$. $\blacksquare$

---

### Q3.4 `[PROOF / COUNTEREXAMPLE]` Matrix Subspaces in $M_{3\times 3}(\mathbb{R})$
**Source:** *Quiz 6 Problems 1, 4, 5, 6 (+ Official Sol)*

> Determine whether each subset $W$ of $V = M_{3\times 3}(\mathbb{R})$ is a subspace of $V$. Justify.
> - **(a) (P1):** $W =$ set of all $3 \times 3$ real **magic squares** (every row, column, and both main diagonals sum to the same number).
> - **(b) (P4):** $W = \{A \in V \mid \det(A) = 0\}$.
> - **(c) (P5):** $W = \{A \in V \mid A^T = A\}$ (symmetric matrices).
> - **(d) (P6):** $W = \{A \in V \mid A^T = -A\}$ (skew-symmetric matrices).

**Solution:**
- **(a) YES (Subspace):**
  1. Zero matrix $O = [0]_{3\times 3}$ has all row, column, and diagonal sums equal to $0 \implies O \in W$.
  2. Let $A \in W$ have magic sum $s_1$ and $B \in W$ have magic sum $s_2$. Then every row sum of $A+B$ is $\sum_{j=1}^3 (a_{ij}+b_{ij}) = s_1+s_2$, every column sum is $\sum_{i=1}^3 (a_{ij}+b_{ij}) = s_1+s_2$, and both diagonal sums are also $s_1+s_2$. Hence $A+B \in W$.
  3. For $k \in \mathbb{R}$, every row, column, and diagonal sum of $kA$ equals $k s_1$, so $kA \in W$.
  Thus $W$ is a subspace of $M_{3\times 3}(\mathbb{R})$.

- **(b) NO (Not a subspace):**
  While $O \in W$ ($\det(O)=0$) and $W$ is closed under scalar multiplication ($\det(kA) = k^3\det(A) = 0$), **$W$ is NOT closed under addition**:
  Take $A = \begin{bmatrix}1&0&0\\0&1&0\\0&0&0\end{bmatrix}$ ($\det A = 0$) and $B = \begin{bmatrix}0&0&0\\0&0&0\\0&0&1\end{bmatrix}$ ($\det B = 0$). Both $A, B \in W$, yet $A + B = I_3$, and $\det(I_3) = 1 \neq 0$, so $A + B \notin W$. *(Note: Quiz 6 key wrote a tiny typo $0\cdot 1\cdot 1$ instead of $1\cdot 1\cdot 0$ for $\det A$; fixed here.)*

- **(c) YES (Subspace):**
  1. $O^T = O \implies O \in W$.
  2. If $A, B \in W$, $(A+B)^T = A^T + B^T = A + B \implies A+B \in W$.
  3. If $A \in W, k \in \mathbb{R}$, $(kA)^T = kA^T = kA \implies kA \in W$.

- **(d) YES (Subspace):**
  1. $O^T = O = -O \implies O \in W$.
  2. If $A, B \in W$, $(A+B)^T = A^T + B^T = (-A) + (-B) = -(A+B) \implies A+B \in W$.
  3. If $A \in W, k \in \mathbb{R}$, $(kA)^T = kA^T = k(-A) = -(kA) \implies kA \in W$.

---

### Q3.5 `[PROOF]` Function Subspace via Integral Condition
**Source:** *Quiz 6 Problem 7 (+ Official Sol)*

> Let $V = C([a, b])$ be all continuous functions on $[a, b]$. Is $W = \left\{f \in V \,\middle|\, \int_a^b f(x)\,dx = 0\right\}$ a subspace of $V$? Justify.

**Solution:** **YES (Subspace).**
1. Zero function $0(x) = 0$ satisfies $\int_a^b 0\,dx = 0 \implies 0 \in W$.
2. If $f, g \in W$, $\int_a^b (f(x)+g(x))\,dx = \int_a^b f(x)\,dx + \int_a^b g(x)\,dx = 0 + 0 = 0 \implies f+g \in W$.
3. If $f \in W, k \in \mathbb{R}$, $\int_a^b kf(x)\,dx = k\int_a^b f(x)\,dx = k\cdot 0 = 0 \implies kf \in W$. $\blacksquare$

---

## Part 4: Span, Linear Independence, Bases & Dimension

### Q4.1 `[PROOF]` $\text{Span}\{v_1, \dots, v_r\}$ Is the Smallest Subspace
**Source:** *Fall 2022 FE Q8(a),(b) [5+5 Marks]*

> If $\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_r$ are vectors in a vector space $U$, prove:
> - **(a)** The set $W$ of all linear combinations of $\mathbf{v}_1, \dots, \mathbf{v}_r$ is a subspace of $U$.
> - **(b)** $W$ is the smallest subspace of $U$ that contains $\mathbf{v}_1, \dots, \mathbf{v}_r$.

**Solution:**
- **(a) $W$ is a subspace of $U$:**
  - *Nonempty:* $\mathbf{0} = 0\mathbf{v}_1 + \dots + 0\mathbf{v}_r \in W$ (and each $\mathbf{v}_i \in W$).
  - *Addition:* Let $\mathbf{x} = \sum_{i=1}^r c_i\mathbf{v}_i \in W$ and $\mathbf{y} = \sum_{i=1}^r d_i\mathbf{v}_i \in W$. Then:
    $$\mathbf{x} + \mathbf{y} = \sum_{i=1}^r (c_i + d_i)\mathbf{v}_i \in W.$$
  - *Scalar multiplication:* For any $k \in \mathbb{R}$,
    $$k\mathbf{x} = \sum_{i=1}^r (kc_i)\mathbf{v}_i \in W.$$
  By the Subspace Test, $W$ is a subspace of $U$.

- **(b) $W$ is the smallest subspace containing $\mathbf{v}_1, \dots, \mathbf{v}_r$:**
  First, $W$ contains every $\mathbf{v}_i$ because $\mathbf{v}_i = 0\mathbf{v}_1 + \dots + 1\mathbf{v}_i + \dots + 0\mathbf{v}_r$.
  Next, let $W'$ be *any* subspace of $U$ that contains $\mathbf{v}_1, \dots, \mathbf{v}_r$. Because $W'$ is closed under scalar multiplication and addition, $W'$ must contain every linear combination $c_1\mathbf{v}_1 + \dots + c_r\mathbf{v}_r$. Thus $W \subseteq W'$. Therefore $W$ is contained in every such subspace, making it the smallest. $\blacksquare$

---

### Q4.2 `[CONCEPT / CALC]` Trigonometric Span & Spanning Matrices for $M_{nn}$
**Source:** *Fall 2022 Midterm Q8(b), Q10 [10 Marks]*

> - **(a) (F22 Mid Q10):** Let $V$ be the subspace of $F(-\infty,\infty)$ given by $V = \text{span}\{\sin x, \cos x\}$. Show that for any given value of $\theta$, $\mathbf{f}_1 = \cos(x+\theta)$ and $\mathbf{g}_1 = \sin(x+\theta)$ belong to $V$.
> - **(b) (F22 Mid Q8b):** In words, describe a set of matrices that spans $M_{nn}$.

**Solution:**
- **(a)** Using the angle-addition identities:
  $$\begin{aligned}
  \mathbf{f}_1(x) &= \cos(x + \theta) = (\cos\theta)\cos x + (-\sin\theta)\sin x, \\
  \mathbf{g}_1(x) &= \sin(x + \theta) = (\cos\theta)\sin x + (\sin\theta)\cos x.
  \end{aligned}$$
  Since $\theta$ is fixed, $\cos\theta$ and $\sin\theta$ are constants (scalars). Both $\mathbf{f}_1$ and $\mathbf{g}_1$ are expressed as linear combinations of $\sin x$ and $\cos x$, so $\mathbf{f}_1 \in V$ and $\mathbf{g}_1 \in V$. $\blacksquare$

- **(b)** The standard basis set of $n^2$ matrices $E_{ij}$ ($1 \le i, j \le n$), where **each matrix $E_{ij}$ has $1$ in the $(i, j)$-th entry and $0$ in all other entries**, spans $M_{nn}$ (since any $n \times n$ matrix $A = [a_{ij}]$ is uniquely written as $\sum_{i=1}^n \sum_{j=1}^n a_{ij} E_{ij}$).

---

### Q4.3 `[CALC]` Linear Combinations & Spanning Sets in $\mathbb{R}^2$ and $\mathbb{R}^3$
**Source:** *Quiz 7 Problems 1–8 (+ Official Sol)*

> Solve each linear-combination / spanning problem:
> 1. **(P1)** Find scalars $a, b$ such that $a(3,2) + b(-1,4) = (7,-6)$.
> 2. **(P2)** Do $\mathbf{v}=(1,2,3), \mathbf{w}=(2,3,4), \mathbf{u}=(3,4,5)$ span $\mathbb{R}^3$?
> 3. **(P3)** Find scalars $a, b$ such that $a(2,1) + b(-1,3) = (5,0)$.
> 4. **(P4)** Can $\mathbf{u}=(4,-2)$ be expressed as a linear combination of $\mathbf{v}=(1,2)$ and $\mathbf{w}=(3,-1)$?
> 5. **(P5)** Do $\mathbf{v}=(1,0,1), \mathbf{w}=(0,1,1), \mathbf{u}=(1,1,0)$ span $\mathbb{R}^3$?
> 6. **(P6)** Can $\mathbf{u}=(6,-3)$ be expressed as a linear combination of $\mathbf{v}=(1,2)$ and $\mathbf{w}=(2,-1)$?
> 7. **(P7)** Can $\mathbf{u}=(5,1)$ be expressed as a linear combination of $\mathbf{v}=(2,1)$ and $\mathbf{w}=(4,2)$?
> 8. **(P8)** Do $\mathbf{v}=(1,1,0), \mathbf{w}=(0,1,1), \mathbf{u}=(1,0,1)$ span $\mathbb{R}^3$?

**Solutions:**
1. **(P1):** $3a - b = 7$ and $2a + 4b = -6 \implies 14a = 22 \implies \mathbf{a = \frac{11}{7},\; b = -\frac{16}{7}}$.
2. **(P2):** Put vectors as columns of $A = \begin{bmatrix}1&2&3\\2&3&4\\3&4&5\end{bmatrix}$. $\det(A) = 1(15-16)-2(10-12)+3(8-9) = -1+4-3 = 0$. Since $\det(A)=0$ (note $\mathbf{v}-2\mathbf{w}+\mathbf{u}=\mathbf{0}$), **No, they do not span $\mathbb{R}^3$**.
3. **(P3):** $2a - b = 5$ and $a + 3b = 0 \implies a = -3b \implies -7b = 5 \implies \mathbf{a = \frac{15}{7},\; b = -\frac{5}{7}}$.
4. **(P4):** Solve $a+3b=4,\; 2a-b=-2 \implies 7a=-2 \implies a = -\frac{2}{7},\; b = \frac{10}{7}$. Solution exists $\implies$ **Yes**.
5. **(P5):** $A = \begin{bmatrix}1&0&1\\0&1&1\\1&1&0\end{bmatrix}$, $\det(A) = 1(0-1) + 1(0-1) = -2 \neq 0 \implies$ **Yes, they span $\mathbb{R}^3$** (in fact a basis).
6. **(P6):** Solve $a+2b=6,\; 2a-b=-3 \implies 5a=0 \implies a=0, b=3$. Solution exists $\implies$ **Yes**.
7. **(P7):** Solve $2a+4b=5,\; a+2b=1$. Multiplying the 2nd by $2$ gives $2a+4b=2 \neq 5$ ($0 = 3$, contradiction) $\implies$ **No**.
8. **(P8):** $A = \begin{bmatrix}1&0&1\\1&1&0\\0&1&1\end{bmatrix}$, $\det(A) = 1(1-0) + 1(1-0) = 2 \neq 0 \implies$ **Yes, they span $\mathbb{R}^3$**.

---

### Q4.4 `[T/F]` Concept Checks on Span and Sets Containing $\mathbf{0}$
**Sources:** *Fall 2022 Mid Q8(a)(ii); Spring 2022 FE Q4(b), Q4(d)*

> Always True or Sometimes False? Justify:
> - **(a)** *If $\text{span}(S_1) = \text{span}(S_2)$, then $S_1 = S_2$.* *(F22 Mid Q8a(ii), Sp22 FE Q4d)*
> - **(b)** *A set that contains the zero vector is linearly dependent.* *(Sp22 FE Q4b)*

**Solution:**
- **(a) SOMETIMES FALSE.** Counterexample in $\mathbb{R}^2$: $S_1 = \{(1,0), (0,1)\}$ and $S_2 = \{(1,0), (0,1), (1,1)\}$ both satisfy $\text{span}(S_1) = \text{span}(S_2) = \mathbb{R}^2$, even though $S_1 \neq S_2$.
- **(b) ALWAYS TRUE.** Suppose $S = \{\mathbf{0}, \mathbf{v}_1, \dots, \mathbf{v}_r\}$. Then the nontrivial linear combination:
  $$1\cdot\mathbf{0} + 0\mathbf{v}_1 + \dots + 0\mathbf{v}_r = \mathbf{0}$$
  has a nonzero coefficient ($1 \neq 0$), so $S$ is linearly dependent.

---

### Q4.5 `[PROOF]` Two-Vector Independence Criterion & Difference Vectors
**Sources:** *Fall 2022 FE Q2(b) [4 Marks]; Spring 2022 Mid Q7(a) [5 Marks]*

> - **(a) (F22 FE Q2b):** Prove: A set with exactly two vectors $\{\mathbf{u}, \mathbf{v}\}$ is linearly independent if and only if neither vector is a scalar multiple of the other.
> - **(b) (Sp22 Mid Q7a):** Prove that for any vectors $\mathbf{a}, \mathbf{b}, \mathbf{c}$, the vectors $(\mathbf{a}-\mathbf{b})$, $(\mathbf{b}-\mathbf{c})$, and $(\mathbf{c}-\mathbf{a})$ form a linearly dependent set.

**Solution:**
- **(a)** Equivalently prove the contrapositive: $\{\mathbf{u},\mathbf{v}\}$ is linearly dependent $\iff$ one is a scalar multiple of the other.
  - *($\Rightarrow$)* Suppose $\{\mathbf{u}, \mathbf{v}\}$ is LD. Then $c_1\mathbf{u} + c_2\mathbf{v} = \mathbf{0}$ for scalars $c_1, c_2$ not both $0$. If $c_1 \neq 0$, then $\mathbf{u} = \left(-\frac{c_2}{c_1}\right)\mathbf{v}$; if $c_2 \neq 0$, then $\mathbf{v} = \left(-\frac{c_1}{c_2}\right)\mathbf{u}$. Either way, one is a scalar multiple of the other.
  - *($\Leftarrow$)* Suppose without loss of generality $\mathbf{u} = k\mathbf{v}$ for some $k \in \mathbb{R}$. Then $1\cdot\mathbf{u} + (-k)\mathbf{v} = \mathbf{0}$ with coefficient $1 \neq 0$, so $\{\mathbf{u},\mathbf{v}\}$ is LD. $\blacksquare$

- **(b)** Consider the linear combination with coefficients $c_1 = 1,\; c_2 = 1,\; c_3 = 1$:
  $$1(\mathbf{a}-\mathbf{b}) + 1(\mathbf{b}-\mathbf{c}) + 1(\mathbf{c}-\mathbf{a}) = (\mathbf{a}-\mathbf{a}) + (-\mathbf{b}+\mathbf{b}) + (-\mathbf{c}+\mathbf{c}) = \mathbf{0}.$$
  Since $(1, 1, 1) \neq (0, 0, 0)$ is a nontrivial solution, the set $\{\mathbf{a}-\mathbf{b},\, \mathbf{b}-\mathbf{c},\, \mathbf{c}-\mathbf{a}\}$ is linearly dependent. $\blacksquare$

---

### Q4.6 `[PROOF]` Adding a Vector Outside Span & General Linear Independence Equivalence
**Source:** *Spring 2022 Midterm Q7(b) [5 Marks], Q8 [5+5 Marks]*

> - **(a) (Sp22 Mid Q7b):** Prove that if $\{\mathbf{a}, \mathbf{b}\}$ is a linearly independent set, and $\mathbf{c} \notin \text{span}\{\mathbf{a}, \mathbf{b}\}$, then $\{\mathbf{a}, \mathbf{b}, \mathbf{c}\}$ is also linearly independent.
> - **(b) (Sp22 Mid Q8):** Given a set $S$ with two or more vectors:
>   - (i) Prove that if $S$ is linearly independent, then no vector in $S$ is expressible as a linear combination of the other vectors in $S$.
>   - (ii) Prove that if no vector in $S$ is expressible as a linear combination of the other vectors in $S$, then $S$ is linearly independent.

**Solution:**
- **(a)** Suppose $k_1\mathbf{a} + k_2\mathbf{b} + k_3\mathbf{c} = \mathbf{0}$.
  - If $k_3 \neq 0$, we could divide by $k_3$ to get $\mathbf{c} = \left(-\frac{k_1}{k_3}\right)\mathbf{a} + \left(-\frac{k_2}{k_3}\right)\mathbf{b} \in \text{span}\{\mathbf{a}, \mathbf{b}\}$, contradicting $\mathbf{c} \notin \text{span}\{\mathbf{a}, \mathbf{b}\}$.
  - Therefore $k_3 = 0$, leaving $k_1\mathbf{a} + k_2\mathbf{b} = \mathbf{0}$. Because $\{\mathbf{a}, \mathbf{b}\}$ is linearly independent, $k_1 = k_2 = 0$.
  Thus $k_1 = k_2 = k_3 = 0$, so $\{\mathbf{a}, \mathbf{b}, \mathbf{c}\}$ is linearly independent. $\blacksquare$

- **(b) General theorem (proved for finite $S = \{\mathbf{v}_1, \dots, \mathbf{v}_r\}$, $r \ge 2$ — by contrapositive of each direction):**
  - *(i) ($\Rightarrow$):* Assume $S$ is LI. Suppose for contradiction some $\mathbf{v}_i$ is a linear combination of the others: $\mathbf{v}_i = \sum_{j \neq i} c_j \mathbf{v}_j$. Moving $\mathbf{v}_i$ to the RHS gives:
    $$c_1\mathbf{v}_1 + \dots + (-1)\mathbf{v}_i + \dots + c_r\mathbf{v}_r = \mathbf{0},$$
    which has coefficient $-1 \neq 0$, contradicting that $S$ is LI. Thus no vector in $S$ can be a linear combination of the others.
  - *(ii) ($\Leftarrow$):* Prove contrapositive: suppose $S$ is linearly dependent. Then there exist scalars $k_1, \dots, k_r$, not all zero, such that $k_1\mathbf{v}_1 + \dots + k_r\mathbf{v}_r = \mathbf{0}$. Pick any index $i$ with $k_i \neq 0$ and solve for $\mathbf{v}_i$:
    $$\mathbf{v}_i = \sum_{j \neq i} \left(-\frac{k_j}{k_i}\right)\mathbf{v}_j,$$
    showing that $\mathbf{v}_i$ IS expressible as a linear combination of the other vectors in $S$. Contrapositively, if no vector is a linear combination of the others, $S$ must be linearly independent. $\blacksquare$

---

### Q4.7 `[PROOF]` Orthogonal Set of Nonzero Vectors Is Linearly Independent
**Sources:** *Spring 2023 FE Q8 [10 Marks]; Quiz 11 Problem 4(a) (+ Official Sol)*

> Let $S = \{\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_n\}$ be an orthogonal set of nonzero vectors in an inner product space $V$. Prove that $S$ is linearly independent.

**Solution:**
Suppose $c_1\mathbf{v}_1 + c_2\mathbf{v}_2 + \dots + c_n\mathbf{v}_n = \mathbf{0}$. Fix any $k \in \{1, \dots, n\}$ and take the inner product of both sides with $\mathbf{v}_k$:
$$\langle c_1\mathbf{v}_1 + \dots + c_k\mathbf{v}_k + \dots + c_n\mathbf{v}_n,\, \mathbf{v}_k\rangle = \langle \mathbf{0}, \mathbf{v}_k\rangle = 0.$$
By linearity and orthogonality ($\langle \mathbf{v}_i, \mathbf{v}_k\rangle = 0$ for all $i \neq k$), every term vanishes except the $k$-th:
$$c_k \langle \mathbf{v}_k, \mathbf{v}_k\rangle = 0 \implies c_k \|\mathbf{v}_k\|^2 = 0.$$
Since $\mathbf{v}_k \neq \mathbf{0}$, $\|\mathbf{v}_k\|^2 > 0$, forcing $c_k = 0$. Since $k$ was arbitrary, $c_1 = c_2 = \dots = c_n = 0$, so $S$ is linearly independent. $\blacksquare$

---

### Q4.8 `[PROOF]` Size Bounds: $> n$ Vectors Is LD & $< n$ Vectors Doesn't Span
**Sources:**
- *Spring 2023 Mid Q6 [10 Marks] & Spring 2023 FE Q4 [10 Marks]* ($S = \{\mathbf{v}_1,\dots,\mathbf{v}_r\} \subset \mathbb{R}^n$, $r > n \implies S$ is not LI)
- *Spring 2024 FE Q2 [8 Marks] & Spring 2025 FE Solution P3(a),(b)* (General finite-dim $V$ with basis $\{\mathbf{v}_1,\dots,\mathbf{v}_n\}$)

> Let $V$ be a finite-dimensional vector space with basis $S = \{\mathbf{v}_1, \dots, \mathbf{v}_n\}$ (or $V = \mathbb{R}^n$ directly). Prove:
> - **(a)** Any set $S' = \{\mathbf{w}_1, \dots, \mathbf{w}_m\}$ with $m > n$ vectors is linearly dependent.
> - **(b)** Any set $S' = \{\mathbf{w}_1, \dots, \mathbf{w}_m\}$ with $m < n$ vectors does not span $V$.

**Solution:**
- **(a) Case $V = \mathbb{R}^n$ (Spring 23 Mid/FE):**
  Consider $k_1\mathbf{w}_1 + \dots + k_m\mathbf{w}_m = \mathbf{0}$ with $\mathbf{w}_j = (w_{1j}, \dots, w_{nj})^T$. Equating components gives a **homogeneous linear system of $n$ equations in $m$ unknowns** ($k_1, \dots, k_m$). Since $m > n$ (more unknowns than equations), the system has free variable(s) and hence a **nontrivial solution**. Thus $\{\mathbf{w}_1, \dots, \mathbf{w}_m\}$ is linearly dependent.

- **(a) General $V$ (Spring 24 FE / Spring 25 FE P3a):**
  Since $\{\mathbf{v}_1, \dots, \mathbf{v}_n\}$ is a basis for $V$, each $\mathbf{w}_j$ can be written as $\mathbf{w}_j = \sum_{i=1}^n a_{ij}\mathbf{v}_i$. Substitute into $k_1\mathbf{w}_1 + \dots + k_m\mathbf{w}_m = \mathbf{0}$:
  $$\sum_{j=1}^m k_j \left(\sum_{i=1}^n a_{ij}\mathbf{v}_i\right) = \sum_{i=1}^n \left(\sum_{j=1}^m a_{ij}k_j\right)\mathbf{v}_i = \mathbf{0}.$$
  Because $\{\mathbf{v}_1, \dots, \mathbf{v}_n\}$ is linearly independent, every coefficient must be $0$:
  $$\sum_{j=1}^m a_{ij}k_j = 0 \qquad (i = 1, 2, \dots, n).$$
  This is a homogeneous system of $n$ equations in $m > n$ unknowns $k_1, \dots, k_m$, which always has a **nontrivial solution**. Hence $S'$ is linearly dependent. $\blacksquare$

- **(b) General $V$ (Spring 25 FE P3b):**
  Suppose for contradiction that $S' = \{\mathbf{w}_1, \dots, \mathbf{w}_m\}$ ($m < n$) spans $V$. Then each basis vector $\mathbf{v}_j \in S$ ($j=1,\dots,n$) can be written as $\mathbf{v}_j = \sum_{i=1}^m a_{ij}\mathbf{w}_i$. Consider the equation $k_1\mathbf{v}_1 + \dots + k_n\mathbf{v}_n = \mathbf{0}$:
  $$\sum_{j=1}^n k_j \left(\sum_{i=1}^m a_{ij}\mathbf{w}_i\right) = \sum_{i=1}^m \left(\sum_{j=1}^n a_{ij}k_j\right)\mathbf{w}_i = \mathbf{0}.$$
  Setting each coefficient of $\mathbf{w}_i$ equal to zero yields a homogeneous system $\sum_{j=1}^n a_{ij}k_j = 0$ ($i=1,\dots,m$) of **$m$ equations in $n > m$ unknowns**. This system has a nontrivial solution $(k_1,\dots,k_n) \neq \mathbf{0}$, which gives a nontrivial dependence $\sum_{j=1}^n k_j\mathbf{v}_j = \mathbf{0}$, contradicting that the basis $\{\mathbf{v}_1,\dots,\mathbf{v}_n\}$ is linearly independent. Therefore $S'$ cannot span $V$. $\blacksquare$

---

### Q4.9 `[PROOF + FILL-IN]` The Plus / Minus Basis Theorems
**Sources:** *Fall 2022 FE Q4(a),(b) [5+5 Marks]; Spring 2022 Midterm Q9 [10 Marks]*

> Let $S$ be a finite set of vectors in a finite-dimensional vector space $V$ ($V \neq \{\mathbf{0}\}$):
> - **(a) (Minus Theorem):** If $S$ spans $V$ but is not a basis for $V$, then $S$ can be **reduced** to a basis for $V$ by **removing** appropriate vectors from $S$. *(Also Sp22 Mid Q9: $S$ finite, $\text{span}(S)=V$, $S$ LD $\implies S$ has a proper subset $B \subset S$ that is a basis for $V$.)*
> - **(b) (Plus Theorem):** If $S$ is a linearly independent set that is not already a basis for $V$, then $S$ can be **enlarged** (or **extended**) to a basis for $V$ by **inserting** appropriate vectors into $S$.

**Solution:**
- **(a) Proof (Reducing / Minus Theorem):**
  Since $S$ spans $V$ and is not a basis, $S$ must be linearly dependent. By the characterization theorem (Q4.6(b)), some vector $\mathbf{v} \in S$ is a linear combination of the other vectors in $S$. Removing $\mathbf{v}$ yields a proper subset $S_1 = S \setminus \{\mathbf{v}\}$ that still spans $V$ (any linear combination involving $\mathbf{v}$ can replace $\mathbf{v}$ by its expression in $S_1$).
  - If $S_1$ is linearly independent, then $B = S_1 \subset S$ is a basis for $V$ and we stop.
  - Otherwise, repeat this removal step. Since $S$ is finite and $V \neq \{\mathbf{0}\}$ (so a spanning set cannot become empty), this process must terminate after finitely many steps at a linearly independent subset $B \subset S$ that still spans $V$—a basis for $V$. $\blacksquare$

- **(b) Proof (Extending / Plus Theorem):**
  Let $\dim(V) = n$. Since $S$ is linearly independent and not already a basis for $V$, $S$ does not span $V$. Thus there exists some vector $\mathbf{w}_1 \in V$ such that $\mathbf{w}_1 \notin \text{span}(S)$. Let $S_1 = S \cup \{\mathbf{w}_1\}$.
  - Claim: $S_1$ is linearly independent (if $c_1\mathbf{v}_1+\dots+c_r\mathbf{v}_r + d\mathbf{w}_1 = \mathbf{0}$, then $d$ must be $0$, else $\mathbf{w}_1 \in \text{span}(S)$; and $d=0 \implies c_1=\dots=c_r=0$ because $S$ is LI).
  - If $S_1$ spans $V$, then $S_1$ is a basis and we stop. Otherwise, repeat by picking $\mathbf{w}_2 \notin \text{span}(S_1)$.
  - Because $V$ is $n$-dimensional, no linearly independent set in $V$ can contain more than $n$ vectors (Theorem Q4.8(a)). Hence this process must terminate after at most $n - |S|$ insertions at a linearly independent set that spans $V$—a basis for $V$. $\blacksquare$

---

### Q4.10 `[PROOF]` The Half-Test for Bases & Subspace Dimension Theorem
**Sources:**
- *Spring 2022 FE Q5(a),(b) [5+5 Marks]*
- *Spring 2024 FE Q4 [10 Marks]*

> - **(a) (Half-Test / Sp22 FE Q5a, Sp24 FE Q4):** Prove: If $V$ is an $n$-dimensional vector space and $S$ is a set in $V$ with exactly $n$ vectors, then $S$ is a basis for $V$ if **either** $S$ spans $V$ **or** $S$ is linearly independent.
> - **(b) (Sp22 FE Q5b):** Prove: If $W$ is a subspace of a finite-dimensional vector space $V$, then $\dim(W) \le \dim(V)$; moreover, if $\dim(W) = \dim(V)$, then $W = V$.

**Solution:**
- **(a) Proof of Half-Test:**
  Let $|S| = n$ in an $n$-dimensional space $V$.
  - *Suppose $S$ spans $V$:* If $S$ were linearly dependent, by the Minus Theorem (Q4.9a) we could remove at least one vector from $S$ to obtain a basis of $V$ having $< n$ vectors, contradicting $\dim(V) = n$ (every basis of $V$ has size $n$). Hence $S$ must be linearly independent, so $S$ is a basis.
  - *Suppose $S$ is linearly independent:* If $S$ did not span $V$, we could find $\mathbf{v} \notin \text{span}(S)$ and form a linearly independent set $S \cup \{\mathbf{v}\}$ with $n + 1$ vectors, contradicting Q4.8(a) (no LI set in $V$ has $> n$ vectors). Hence $S$ must span $V$, so $S$ is a basis. $\blacksquare$

- **(b) Proof of Subspace Dimension Theorem:**
  Let $\dim(V) = n$.
  - If $W = \{\mathbf{0}\}$, then $\dim(W) = 0 \le n$.
  - If $W \neq \{\mathbf{0}\}$, pick any nonzero $\mathbf{v}_1 \in W$ (linearly independent). Either $\{\mathbf{v}_1\}$ spans $W$, or we can successively add $\mathbf{v}_k \in W \setminus \text{span}\{\mathbf{v}_1,\dots,\mathbf{v}_{k-1}\}$, keeping the set linearly independent inside $W \subseteq V$. Since $V$ has no linearly independent set of size $> n$, this process must stop at some basis $B$ of $W$ with $|B| \le n$, proving $\dim(W) \le \dim(V)$.
  - If $\dim(W) = \dim(V) = n$, any basis $B$ of $W$ is a linearly independent set of $n$ vectors inside $V$. By the Half-Test (part (a)), $B$ is also a basis for $V$, so $W = \text{span}(B) = V$. $\blacksquare$

---

### Q4.11 `[CALC]` Checking Bases ($\mathbb{R}^3$, $P_2$, Trig Space) & Extending to Bases
**Sources:** *Quiz 8 P1–P8; Quiz 9 P1–P3; Spring 2024 FE Q9(b) [4 Marks]; Spring 2023 FE Q5(b) [6 Marks]*

> **(A) $\mathbb{R}^3$ Basis Checks (Quiz 8 P3, P4, P7, P8):** Determine whether each set of 3 vectors is a basis for $\mathbb{R}^3$:
> 1. *(P3)* $\{(1,6,4),\,(2,4,-1),\,(-1,2,5)\}$
> 2. *(P4)* $\{(1,0,1),\,(-2,1,4),\,(-1,1,5)\}$
> 3. *(P7)* $\{(1,0,1),\,(-2,1,4),\,(0,3,1)\}$
> 4. *(P8)* $\{(2,3,1),\,(4,1,1),\,(0,-7,1)\}$
>
> **(B) $P_2$ Basis Checks (Quiz 8 P5, P6; Sp24 FE Q9b):** Determine whether each set is a basis for $P_2$:
> 5. *(Quiz 8 P5)* $\{1-3x+2x^2,\; 1+x+4x^2,\; 1-7x\}$
> 6. *(Quiz 8 P6 & Sp24 FE Q9b)* $\{4+6x+x^2,\; -1+4x+2x^2,\; 5+2x-x^2\}$
>
> **(C) Trigonometric Vector Space (Sp23 FE Q5b; Quiz 8 P1, P2):**
> 7. Let $V$ be spanned by $S = \{\mathbf{v}_1, \mathbf{v}_2, \mathbf{v}_3\} = \{\cos^2 x,\; \sin^2 x,\; \cos 2x\}$.
>    - (i) Show that $S$ is not a basis for $V$.
>    - (ii) Find a basis for $V$ (Quiz 8 P1 asks for one containing $\cos 2x$; Quiz 8 P2 asks for one containing $\sin^2 x$).
>
> **(D) Prove Linear Independence & Extend to a Basis for $\mathbb{R}^3$ (Quiz 9 P1–P3):**
> 8. *(P1)* $S = \{(1,0,1)^T,\,(2,1,3)^T\}$
> 9. *(P2)* $S = \{(1,2,0)^T,\,(3,5,1)^T\}$
> 10. *(P3)* $S = \{(2,1,-1)^T,\,(-1,3,4)^T\}$

**Solutions:**
**(A) $\mathbb{R}^3$ Basis Checks** (by Half-Test: 3 vectors form a basis iff $\det(A) \neq 0$):
1. $\det\begin{bmatrix}1&2&-1\\6&4&2\\4&-1&5\end{bmatrix} = 1(22)-2(22)-1(-22) = 0 \implies$ **No** (note $\mathbf{v}_3 = \mathbf{v}_1 - \mathbf{v}_2$).
2. $\det\begin{bmatrix}1&-2&-1\\0&1&1\\1&4&5\end{bmatrix} = 1(5-4)+2(0-1)-1(0-1) = 1-2+1 = 0 \implies$ **No** (note $\mathbf{v}_3 = \mathbf{v}_1+\mathbf{v}_2$; Quiz 8 key had `-(0+1)` typo inside parentheses, result $0$ is right).
3. $\det\begin{bmatrix}1&-2&0\\0&1&3\\1&4&1\end{bmatrix} = 1(1-12)+2(0-3) = -17 \neq 0 \implies$ **Yes**.
4. $\det\begin{bmatrix}2&4&0\\3&1&-7\\1&1&1\end{bmatrix} = 2(1+7)-4(3+7) = -24 \neq 0 \implies$ **Yes**.

**(B) $P_2$ Basis Checks** ($\dim(P_2)=3$, check coordinate determinant in $\{1, x, x^2\}$):
5. Coordinate matrix $A = \begin{bmatrix}1&1&1\\-3&1&-7\\2&4&0\end{bmatrix}$, $\det(A) = 1(28)-1(14)+1(-14) = 0 \implies$ **No** (not a basis; $2p_1 - p_2 = p_3$).
6. Coordinate matrix $A = \begin{bmatrix}4&-1&5\\6&4&2\\1&2&-1\end{bmatrix}$, $\det(A) = 4(-8)+1(-8)+5(8) = 0 \implies$ **No** (not a basis; $p_1 - p_2 = p_3$).

**(C) Trigonometric Space:**
7. **(i)** Using the identity $\cos 2x = \cos^2 x - \sin^2 x$, we have the nontrivial relation:
   $$1\cdot\cos^2 x + (-1)\cdot\sin^2 x + (-1)\cdot\cos 2x = 0.$$
   Hence $S$ is **linearly dependent** and cannot be a basis for $V$.
   **(ii)** Because $\cos 2x$ (or $\cos^2 x$) is a linear combination of the other two, removing any one redundant vector preserves the span $V$ (by the Minus Theorem):
   - *Basis containing $\cos^2 x, \sin^2 x$ (Sp23 FE Q5b):* $\{\cos^2 x, \sin^2 x\}$. Linear independence: $c_1\cos^2 x + c_2\sin^2 x = 0 \implies$ at $x=0$: $c_1=0$; at $x=\frac{\pi}{2}$: $c_2=0$.
   - *Basis containing $\cos 2x$ (Quiz 8 P1):* $\{\cos^2 x, \cos 2x\}$ or $\{\sin^2 x, \cos 2x\}$. Check LI of $\{\sin^2 x, \cos 2x\}$: $a\sin^2 x + b\cos 2x = 0 \implies$ at $x=0$: $b=0$; at $x=\frac{\pi}{2}$: $a=0$. (Similarly $\cos^2 x$ and $\cos 2x$ are not scalar multiples.)

**(D) Prove LI & Extend to $\mathbb{R}^3$:**
8. *(P1)* $a(1,0,1)^T + b(2,1,3)^T = \mathbf{0} \implies b=0$ (from 2nd row), then $a=0$ (from 1st row) $\implies$ LI. Add $\mathbf{w} = (x,y,z)^T$: $\det\begin{bmatrix}1&2&x\\0&1&y\\1&3&z\end{bmatrix} = -x - y + z$. Choosing $\mathbf{w}=(0,0,1)^T$ gives $\det = 1 \neq 0 \implies$ Basis: $\{(1,0,1)^T,\,(2,1,3)^T,\,(0,0,1)^T\}$.
9. *(P2)* $a(1,2,0)^T + b(3,5,1)^T = \mathbf{0} \implies b=0$ (3rd row), then $a=0 \implies$ LI. Add $\mathbf{w}=(x,y,z)^T$: $\det\begin{bmatrix}1&3&x\\2&5&y\\0&1&z\end{bmatrix} = 2x - y - z$. Choosing $\mathbf{w}=(0,0,1)^T$ gives $\det = -1 \neq 0 \implies$ Basis: $\{(1,2,0)^T,\,(3,5,1)^T,\,(0,0,1)^T\}$. *(Note: Quiz 9 key forgot the minus sign in $\det$, writing $+1$, though $-1 \neq 0$ still makes $(0,0,1)^T$ valid!)*
10. *(P3)* $a(2,1,-1)^T + b(-1,3,4)^T = \mathbf{0} \implies 2a-b=0$ and $a+3b=0 \implies a=b=0 \implies$ LI. Add $\mathbf{w}=(x,y,z)^T$: $\det\begin{bmatrix}2&-1&x\\1&3&y\\-1&4&z\end{bmatrix} = 7x - 7y + 7z$. Choosing $\mathbf{w}=(0,0,1)^T$ gives $\det = 7 \neq 0 \implies$ Basis: $\{(2,1,-1)^T,\,(-1,3,4)^T,\,(0,0,1)^T\}$.

---

## Part 5: Row Space, Column Space, Null Space, Rank–Nullity & Consistency

### Q5.1 `[PROOF]` Structure of General Solution to $A\mathbf{x} = \mathbf{b}$
**Source:** *Spring 2022 Midterm Q4 [10 Marks]*

> Let $A\mathbf{x} = \mathbf{b}$ be any consistent system of linear equations and let $\mathbf{x}_1$ be a fixed solution. Show that every solution to the system can be written in the form $\mathbf{x} = \mathbf{x}_1 + \mathbf{x}_0$, where $\mathbf{x}_0$ is a solution of the homogeneous system $A\mathbf{x} = \mathbf{0}$. Show also that every vector of this form is a solution.

**Solution:**
1. **Every solution has the form $\mathbf{x}_1 + \mathbf{x}_0$:**
   Let $\mathbf{x}$ be any solution to $A\mathbf{x} = \mathbf{b}$. Define $\mathbf{x}_0 = \mathbf{x} - \mathbf{x}_1$. Then:
   $$A\mathbf{x}_0 = A(\mathbf{x} - \mathbf{x}_1) = A\mathbf{x} - A\mathbf{x}_1 = \mathbf{b} - \mathbf{b} = \mathbf{0},$$
   so $\mathbf{x}_0$ is a solution of $A\mathbf{x} = \mathbf{0}$ (i.e., $\mathbf{x}_0 \in \text{Null}(A)$), and $\mathbf{x} = \mathbf{x}_1 + \mathbf{x}_0$.
2. **Every vector $\mathbf{x}_1 + \mathbf{x}_0$ is a solution:**
   Suppose $\mathbf{x} = \mathbf{x}_1 + \mathbf{x}_0$ where $A\mathbf{x}_1 = \mathbf{b}$ and $A\mathbf{x}_0 = \mathbf{0}$. Then:
   $$A\mathbf{x} = A(\mathbf{x}_1 + \mathbf{x}_0) = A\mathbf{x}_1 + A\mathbf{x}_0 = \mathbf{b} + \mathbf{0} = \mathbf{b}. \quad \blacksquare$$

---

### Q5.2 `[PROOF]` Consistency Criterion via Column Space
**Sources:** *Spring 2023 FE Q2(a) [7 Marks]; Spring 2025 FE Solution P4(b)*

> Prove that a system of linear equations $A\mathbf{x} = \mathbf{b}$ is consistent if and only if $\mathbf{b}$ is in the column space of $A$.

**Solution:**
Write $A = [\mathbf{c}_1 \;\; \mathbf{c}_2 \;\; \cdots \;\; \mathbf{c}_n]$ in terms of its columns $\mathbf{c}_1, \dots, \mathbf{c}_n$, and $\mathbf{x} = [x_1, x_2, \dots, x_n]^T$. By the column-combination view of matrix multiplication:
$$A\mathbf{x} = x_1\mathbf{c}_1 + x_2\mathbf{c}_2 + \dots + x_n\mathbf{c}_n.$$
Thus:
- **($\Rightarrow$)** If $A\mathbf{x} = \mathbf{b}$ is consistent, there exists some vector $\mathbf{x} = [x_1,\dots,x_n]^T$ such that $\mathbf{b} = x_1\mathbf{c}_1 + \dots + x_n\mathbf{c}_n$, which is a linear combination of the columns of $A$; hence $\mathbf{b} \in \text{Col}(A)$.
- **($\Leftarrow$)** If $\mathbf{b} \in \text{Col}(A)$, then by definition of $\text{Col}(A) = \text{span}\{\mathbf{c}_1,\dots,\mathbf{c}_n\}$, there exist scalars $x_1,\dots,x_n$ such that $\mathbf{b} = x_1\mathbf{c}_1 + \dots + x_n\mathbf{c}_n = A\mathbf{x}$. Hence $\mathbf{x} = [x_1,\dots,x_n]^T$ is a solution, so $A\mathbf{x} = \mathbf{b}$ is consistent. $\blacksquare$

---

### Q5.3 `[PROOF]` Consistency for All $\mathbf{b} \iff A$ Invertible & Master Theorem Cycle
**Sources:** *Spring 2022 FE Q8(a),(b) [7+3 Marks]; Spring 2024 Mid Part A Q2 [10 Marks]; Spring 2024 FE Q1 [12 Marks]; Spring 2023 Mid Q7 [10 Marks]*

> - **(A) (Sp22 FE Q8; Sp24 Mid A Q2):** Let $A$ be an $n \times n$ matrix. Prove that $A\mathbf{x} = \mathbf{b}$ is consistent for **every** $n \times 1$ vector $\mathbf{b}$ if and only if $A$ is invertible (non-singular).
> - **(B) (Sp24 FE Q1; Sp23 Mid Q7):** Prove the Master Theorem cycle $(a)\Rightarrow(b)\Rightarrow(c)\Rightarrow(d)\Rightarrow(a)$ for an $n \times n$ matrix $A$:
>   - *(a)* $A\mathbf{x} = \mathbf{0}$ has only the trivial solution.
>   - *(b)* $\text{RREF}(A) = I_n$.
>   - *(c)* $A$ is expressible as a product of elementary matrices.
>   - *(d)* $A$ is invertible (non-singular).

**Solution:**
**(A) Proof of Consistency for all $\mathbf{b} \iff A$ Invertible:**
- **($\Rightarrow$) (Sp22 FE Q8a / Sp24 Mid A Q2):** Suppose $A\mathbf{x} = \mathbf{b}$ is consistent for every $\mathbf{b} \in \mathbb{R}^n$. In particular, for each standard basis vector $\mathbf{e}_j$ ($j=1,\dots,n$), there exists a solution $\mathbf{c}_j \in \mathbb{R}^n$ such that $A\mathbf{c}_j = \mathbf{e}_j$. Form the $n \times n$ matrix $C = [\mathbf{c}_1 \;\; \mathbf{c}_2 \;\; \cdots \;\; \mathbf{c}_n]$. Then:
  $$AC = [A\mathbf{c}_1 \;\; A\mathbf{c}_2 \;\; \cdots \;\; A\mathbf{c}_n] = [\mathbf{e}_1 \;\; \mathbf{e}_2 \;\; \cdots \;\; \mathbf{e}_n] = I_n.$$
  Hence $\det(A)\det(C) = \det(I_n) = 1 \neq 0$, so $\det(A) \neq 0$ and $A$ is invertible (with $A^{-1} = C$).
  *(Rank/Col-space view: consistency for all $\mathbf{b}$ means $\text{Col}(A) = \mathbb{R}^n$, so $\text{rank}(A) = n$, hence $\text{nullity}(A) = 0$ and $A$ is invertible.)*
- **($\Leftarrow$) (Sp22 FE Q8b):** If $A$ is invertible, then for any $\mathbf{b} \in \mathbb{R}^n$, take $\mathbf{x} = A^{-1}\mathbf{b}$. Then $A\mathbf{x} = A(A^{-1}\mathbf{b}) = I_n\mathbf{b} = \mathbf{b}$, so $A\mathbf{x} = \mathbf{b}$ is consistent. $\blacksquare$

**(B) Proof of Master Theorem Cycle:**
- **$(a) \Rightarrow (b)$:** If $A\mathbf{x} = \mathbf{0}$ has only the trivial solution $\mathbf{x} = \mathbf{0}$, then $\text{RREF}(A)$ has no free variables, meaning every one of the $n$ columns is a pivot column. Since $\text{RREF}(A)$ is $n \times n$ with $n$ leading $1$'s (one in every row and column, and $0$'s above/below pivots), $\text{RREF}(A) = I_n$.
- **$(b) \Rightarrow (c)$:** Reducing $A$ to $\text{RREF}(A) = I_n$ applies a finite sequence of elementary row operations corresponding to elementary matrices $E_1, \dots, E_k$, so $E_k \cdots E_2 E_1 A = I_n$. Since each elementary matrix is invertible and its inverse is also elementary, $A = E_1^{-1} E_2^{-1} \cdots E_k^{-1}$ is a product of elementary matrices.
- **$(c) \Rightarrow (d)$:** Each elementary matrix is invertible, and a finite product of invertible matrices is invertible (with $(E_1^{-1}\cdots E_k^{-1})^{-1} = E_k \cdots E_1$). Thus $A$ is invertible.
- **$(d) \Rightarrow (a)$:** If $A$ is invertible and $A\mathbf{x} = \mathbf{0}$, multiplying on the left by $A^{-1}$ gives $\mathbf{x} = A^{-1}(A\mathbf{x}) = A^{-1}\mathbf{0} = \mathbf{0}$. So only the trivial solution exists. $\blacksquare$

---

### Q5.4 `[PROOF]` Dimension of Row Space Equals Dimension of Column Space & $\text{rank}(A) = \text{rank}(A^T)$
**Source:** *Spring 2023 FE Q1(a),(b) [7+3 Marks]*

> - **(a)** Prove: If $A$ is any matrix, then the row space and column space of $A$ have the same dimension ($\dim(\text{Row}(A)) = \dim(\text{Col}(A))$).
> - **(b)** For a matrix $A$ (asked for square $A$ in the exam), show that $A$ and $A^T$ have the same rank.

**Solution:**
- **(a)** Let $R = \text{RREF}(A)$, obtained from $A$ via elementary row operations, and let $r$ be the number of nonzero rows (pivots) in $R$.
  1. **Row space dimension:** Elementary row operations do not change the row space of a matrix, so $\text{Row}(A) = \text{Row}(R)$. The $r$ nonzero rows of $R$ are linearly independent (each pivot $1$ sits in a column where all other rows have $0$) and span $\text{Row}(R)$. Hence $\dim(\text{Row}(A)) = r$.
  2. **Column space dimension:** Elementary row operations preserve the solution set of the homogeneous system $A\mathbf{x} = \mathbf{0} \iff R\mathbf{x} = \mathbf{0}$. Equivalently, any linear dependence relation among the columns $\mathbf{a}_1, \dots, \mathbf{a}_n$ of $A$,
     $$x_1\mathbf{a}_1 + \dots + x_n\mathbf{a}_n = \mathbf{0},$$
     holds **if and only if** the exact same relation holds among the columns $\mathbf{r}_1, \dots, \mathbf{r}_n$ of $R$:
     $$x_1\mathbf{r}_1 + \dots + x_n\mathbf{r}_n = \mathbf{0}.$$
     In $R$, the $r$ pivot columns are the standard basis vectors $\mathbf{e}_1, \dots, \mathbf{e}_r$ (with trailing $0$'s), which are linearly independent and span all columns of $R$. Therefore, the corresponding $r$ pivot columns of $A$ are also linearly independent and every other column of $A$ is a linear combination of them—forming a basis of $\text{Col}(A)$. Hence $\dim(\text{Col}(A)) = r$.
  3. Combining (1) and (2), $\dim(\text{Row}(A)) = r = \dim(\text{Col}(A))$. $\blacksquare$

- **(b)** Notice the rows of $A^T$ are the columns of $A$, and the columns of $A^T$ are the rows of $A$, so $\text{Col}(A^T) = \text{Row}(A)$. Using part (a):
  $$\text{rank}(A^T) = \dim(\text{Col}(A^T)) = \dim(\text{Row}(A)) = \dim(\text{Col}(A)) = \text{rank}(A). \quad \blacksquare$$

---

### Q5.5 `[CALC]` Basis for $\text{Row}(A)$ Consisting Entirely of Row Vectors of $A$
**Source:** *Spring 2023 FE Q9 [10 Marks]*

> For the matrix $A = \begin{bmatrix} 1 & 0 & 0 & 0 & 0 \\ 0 & 1 & -3 & -2 & 0 \\ 10 & -5 & 15 & 10 & 0 \\ 22 & -10 & 18 & 8 & 0 \end{bmatrix}$, find a basis for the row space of $A$ consisting **entirely of row vectors from $A$**.

**Solution:**
Recall that finding a basis of $\text{Row}(A)$ out of original rows of $A$ is equivalent to finding a basis of $\text{Col}(A^T)$ out of columns of $A^T$! Row-reduce $A^T$:
$$A^T = \begin{bmatrix} 1 & 0 & 10 & 22 \\ 0 & 1 & -5 & -10 \\ 0 & -3 & 15 & 18 \\ 0 & -2 & 10 & 8 \\ 0 & 0 & 0 & 0 \end{bmatrix}
\xrightarrow{\substack{R_3 \leftarrow R_3 + 3R_2 \\ R_4 \leftarrow R_4 + 2R_2}}
\begin{bmatrix} 1 & 0 & 10 & 22 \\ 0 & 1 & -5 & -10 \\ 0 & 0 & 0 & -12 \\ 0 & 0 & 0 & -12 \\ 0 & 0 & 0 & 0 \end{bmatrix}
\xrightarrow{\text{RREF}}
\begin{bmatrix} \mathbf{1} & 0 & 10 & 0 \\ 0 & \mathbf{1} & -5 & 0 \\ 0 & 0 & 0 & \mathbf{1} \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{bmatrix}.$$
The pivot columns of $A^T$ are **Columns 1, 2, and 4** (notice Column 3 $= 10\,\text{Col}_1 - 5\,\text{Col}_2$, i.e., $\mathbf{r}_3 = 10\mathbf{r}_1 - 5\mathbf{r}_2$ in $A$).
Therefore, a basis for $\text{Row}(A)$ consisting entirely of original rows of $A$ is $\{\mathbf{r}_1, \mathbf{r}_2, \mathbf{r}_4\}$:
$$\text{Basis for Row}(A) = \big\{(1, 0, 0, 0, 0),\;\; (0, 1, -3, -2, 0),\;\; (22, -10, 18, 8, 0)\big\}.$$

---

### Q5.6 `[CALC]` Null Space Bases, Nullity & Rank
**Source:** *Quiz 10 Problems 3–6 (+ Official Sol; missing computations for P4–P6 filled in & verified)*

> Find a basis for the null space of each matrix $A$, and state its nullity / rank:
> 1. *(P3)* $A = \begin{bmatrix} 1 & -1 & 3 \\ 5 & -4 & -4 \\ 7 & -6 & 2 \end{bmatrix}$ *(find basis for $\text{Null}(A)$ & nullity)*
> 2. *(P4)* $A = \begin{bmatrix} 2 & -3 & 1 \\ 4 & -5 & -2 \\ 6 & -9 & -1 \end{bmatrix}$ *(find basis for $\text{Null}(A)$ & nullity)*
> 3. *(P5)* $A = \begin{bmatrix} 1 & 2 & -1 & 3 \\ 2 & 4 & -2 & 6 \\ 3 & 6 & -3 & 9 \end{bmatrix}$ *(find basis for $\text{Null}(A)$ & rank)*
> 4. *(P6)* $A = \begin{bmatrix} 1 & 0 & 2 & -1 \\ 0 & 1 & 3 & 2 \\ 0 & 3 & 9 & 6 \end{bmatrix}$ *(find basis for $\text{Null}(A)$ & rank)*

**Solutions:**
1. **(P3):**
   $A \xrightarrow{\substack{R_2 \leftarrow R_2 - 5R_1 \\ R_3 \leftarrow R_3 - 7R_1}} \begin{bmatrix}1&-1&3\\0&1&-19\\0&1&-19\end{bmatrix} \xrightarrow{\text{RREF}} \begin{bmatrix}1&0&-16\\0&1&-19\\0&0&0\end{bmatrix}$.
   Solve $A\mathbf{x} = \mathbf{0}$: $x_3 = t$ (free), $x_2 = 19t$, $x_1 = 16t$.
   - **Basis for $\text{Null}(A)$:** $\left\{\begin{bmatrix}16\\19\\1\end{bmatrix}\right\}$, **$\text{nullity}(A) = 1$**.

2. **(P4)** *(Note: Official PDF wrote "Same as problem 3" for the method, **not** the answer — solving it gives a trivial null space!)*:
   $$A = \begin{bmatrix}2&-3&1\\4&-5&-2\\6&-9&-1\end{bmatrix} \xrightarrow{\substack{R_2 \leftarrow R_2 - 2R_1 \\ R_3 \leftarrow R_3 - 3R_1}} \begin{bmatrix}2&-3&1\\0&1&-4\\0&0&-4\end{bmatrix} \xrightarrow{\text{RREF}} \begin{bmatrix}1&0&0\\0&1&0\\0&0&1\end{bmatrix} = I_3.$$
   Every column is a pivot column ($\text{rank}(A) = 3$), so $A\mathbf{x} = \mathbf{0}$ has only $\mathbf{x} = \mathbf{0}$.
   - **$\text{Null}(A) = \{\mathbf{0}\}$**, **basis:** $\emptyset$ (the empty set; $\{\mathbf{0}\}$ is $0$-dimensional), **$\text{nullity}(A) = 0$**.

3. **(P5):** Rows 2 and 3 are $2R_1$ and $3R_1$, so:
   $$\text{RREF}(A) = \begin{bmatrix}1&2&-1&3\\0&0&0&0\\0&0&0&0\end{bmatrix}.$$
   Free variables: $x_2 = r,\; x_3 = s,\; x_4 = t$, with $x_1 = -2r + s - 3t$:
   $$\mathbf{x} = r\begin{bmatrix}-2\\1\\0\\0\end{bmatrix} + s\begin{bmatrix}1\\0\\1\\0\end{bmatrix} + t\begin{bmatrix}-3\\0\\0\\1\end{bmatrix}.$$
   - **Basis for $\text{Null}(A)$:** $\left\{\begin{bmatrix}-2\\1\\0\\0\end{bmatrix},\; \begin{bmatrix}1\\0\\1\\0\end{bmatrix},\; \begin{bmatrix}-3\\0\\0\\1\end{bmatrix}\right\}$, **$\text{rank}(A) = 1$** ($\text{nullity}(A) = 3$).

4. **(P6):** Row 3 is $3R_2$, so:
   $$\text{RREF}(A) = \begin{bmatrix}1&0&2&-1\\0&1&3&2\\0&0&0&0\end{bmatrix}.$$
   Free variables: $x_3 = s,\; x_4 = t$, with $x_1 = -2s + t$, $x_2 = -3s - 2t$:
   $$\mathbf{x} = s\begin{bmatrix}-2\\-3\\1\\0\end{bmatrix} + t\begin{bmatrix}1\\-2\\0\\1\end{bmatrix}.$$
   - **Basis for $\text{Null}(A)$:** $\left\{\begin{bmatrix}-2\\-3\\1\\0\end{bmatrix},\; \begin{bmatrix}1\\-2\\0\\1\end{bmatrix}\right\}$, **$\text{rank}(A) = 2$** ($\text{nullity}(A) = 2$).

---

### Q5.7 `[CALC]` Rank–Nullity Dimension Table Problems
**Sources:** *Spring 2024 FE Q9(a) [6 Marks]; Quiz 10 Problems 1, 2, 7, 8 (+ Official Sol)*

> Use the Rank–Nullity Theorem ($\text{rank}(A) + \text{nullity}(A) = n$ for an $m \times n$ matrix, and $\text{rank}(A^T) = \text{rank}(A)$) to find the requested dimensions:
> - **Case 1 (Sp24 FE Q9a(i) & Quiz 10 P1):** $A$ is $5 \times 9$ with $\text{rank}(A) = 2$. Find $\dim\text{Row}(A)$, $\dim\text{Col}(A)$, $\dim\text{Null}(A)$, and $\dim\text{Null}(A^T)$.
> - **Case 2 (Sp24 FE Q9a(ii) & Quiz 10 P8):** $A$ is $6 \times 2$ with $\text{rank}(A) = 2$. Find $\dim\text{Row}(A)$, $\dim\text{Col}(A)$, $\dim\text{Null}(A)$ (Sp24 FE), and for $A^T$ ($2 \times 6$) find $\dim\text{Row}(A^T), \dim\text{Col}(A^T), \dim\text{Null}(A^T)$ (Quiz 10 P8).
> - **Case 3 (Quiz 10 P2):** $A$ is $6 \times 8$ with $\text{rank}(A) = 3$. Find $\dim\text{Row}(A)$, $\dim\text{Col}(A)$, $\dim\text{Null}(A)$, and $\dim\text{Null}(A^T)$.
> - **Case 4 (Quiz 10 P7):** $A$ is $9 \times 5$ with $\text{rank}(A) = 2$. Find $\dim\text{Row}(A^T)$, $\dim\text{Col}(A^T)$, $\dim\text{Null}(A^T)$.

**Solutions:**
| Case | Size of $A$ | $\text{rank}(A)$ | $\dim\text{Row}(A)$ | $\dim\text{Col}(A)$ | $\dim\text{Null}(A) = n - r$ | $\dim\text{Row}(A^T) = \dim\text{Col}(A^T)$ | $\dim\text{Null}(A^T) = m - r$ |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **Case 1** | $5 \times 9$ | $2$ | $2$ | $2$ | $9 - 2 = \mathbf{7}$ | $2$ | $5 - 2 = \mathbf{3}$ |
| **Case 2** | $6 \times 2$ | $2$ | $2$ | $2$ | $2 - 2 = \mathbf{0}$ | $2$ | $6 - 2 = \mathbf{4}$ |
| **Case 3** | $6 \times 8$ | $3$ | $3$ | $3$ | $8 - 3 = \mathbf{5}$ | $3$ | $6 - 3 = \mathbf{3}$ |
| **Case 4** | $9 \times 5$ | $2$ | $2$ | $2$ | $5 - 2 = \mathbf{3}$ | $2$ | $9 - 2 = \mathbf{7}$ |

---

## Part 6: Linear Transformations, Standard Matrices, Kernel & Range

### Q6.1 `[PROOF / T-F]` Linear Transformation Theorems & Counterexamples
**Source:** *Spring 2023 FE Q6(c),(d),(e) [2 each], Q2(b) [3 Marks]*

> Evaluate and prove/justify each statement:
> - **(a) (Sp23 FE Q6c):** Let $T: M_{nn} \to \mathbb{R}$ be given by $T(A) = \det(A)$. True or False: $T$ is a linear transformation.
> - **(b) (Sp23 FE Q6d):** If $T: V \to W$ is a linear transformation, prove $T$ is one-to-one if and only if $\ker(T) = \{\mathbf{0}\}$.
> - **(c) (Sp23 FE Q6e):** Every possible linear transformation between Euclidean spaces ($\mathbb{R}^n \to \mathbb{R}^m$) can be represented by some matrix.
> - **(d) (Sp23 FE Q2b):** Using Q5.2 ($A\mathbf{x}=\mathbf{b}$ consistent $\iff \mathbf{b}\in\text{Col}(A)$), explain why for $T_A(\mathbf{x}) = A\mathbf{x}$, $\dim(R(T_A)) = \text{rank}(A)$.

**Solution:**
- **(a) FALSE (for $n \ge 2$).** Let $A = B = I_2 \in M_{2\times 2}$. Then:
  $$T(A + B) = \det(2I_2) = 4, \qquad T(A) + T(B) = \det(I_2) + \det(I_2) = 1 + 1 = 2 \neq 4.$$
  Since $T(A+B) \neq T(A) + T(B)$, $T$ fails additivity (and also fails homogeneity: $\det(cA) = c^n \det(A) \neq c\det(A)$ for $n \ge 2$).
  *(Edge case note: for $n = 1$, $T([a]) = a$ IS linear; for general $n \ge 2$ the statement is False.)*

- **(b) ALWAYS TRUE — Proof:**
  - *($\Rightarrow$)* Suppose $T$ is one-to-one. First, $T(\mathbf{0}) = \mathbf{0}$ (by $T(0\mathbf{v}) = 0T(\mathbf{v}) = \mathbf{0}$), so $\mathbf{0} \in \ker(T)$. If $\mathbf{v} \in \ker(T)$, then $T(\mathbf{v}) = \mathbf{0} = T(\mathbf{0})$. Since $T$ is one-to-one, $\mathbf{v} = \mathbf{0}$. Hence $\ker(T) = \{\mathbf{0}\}$.
  - *($\Leftarrow$)* Suppose $\ker(T) = \{\mathbf{0}\}$, and assume $T(\mathbf{u}) = T(\mathbf{v})$ for some $\mathbf{u}, \mathbf{v} \in V$. By linearity:
    $$T(\mathbf{u} - \mathbf{v}) = T(\mathbf{u}) - T(\mathbf{v}) = \mathbf{0} \implies \mathbf{u} - \mathbf{v} \in \ker(T) = \{\mathbf{0}\} \implies \mathbf{u} - \mathbf{v} = \mathbf{0} \implies \mathbf{u} = \mathbf{v}.$$
    Thus $T$ is one-to-one. $\blacksquare$

- **(c) ALWAYS TRUE — Proof:**
  Let $T: \mathbb{R}^n \to \mathbb{R}^m$ be linear, and let $\{\mathbf{e}_1, \dots, \mathbf{e}_n\}$ be the standard basis of $\mathbb{R}^n$. Every $\mathbf{x} = (x_1,\dots,x_n)^T \in \mathbb{R}^n$ equals $x_1\mathbf{e}_1 + \dots + x_n\mathbf{e}_n$. By linearity:
  $$T(\mathbf{x}) = x_1 T(\mathbf{e}_1) + x_2 T(\mathbf{e}_2) + \dots + x_n T(\mathbf{e}_n) = \big[\,T(\mathbf{e}_1) \;\; T(\mathbf{e}_2) \;\; \cdots \;\; T(\mathbf{e}_n)\,\big]\mathbf{x} = [T]\mathbf{x}.$$
  So every linear map $\mathbb{R}^n \to \mathbb{R}^m$ is matrix multiplication by its $m \times n$ standard matrix $[T]$. $\blacksquare$

- **(d) Explanation:**
  The range of $T_A$ is $R(T_A) = \{\mathbf{b} \in \mathbb{R}^m : \mathbf{b} = A\mathbf{x} \text{ for some } \mathbf{x} \in \mathbb{R}^n\}$, which is precisely the set of $\mathbf{b}$ for which $A\mathbf{x} = \mathbf{b}$ is consistent. By Q5.2, $A\mathbf{x} = \mathbf{b}$ is consistent $\iff \mathbf{b} \in \text{Col}(A)$. Hence $R(T_A) = \text{Col}(A)$, so:
  $$\dim(R(T_A)) = \dim(\text{Col}(A)) = \text{rank}(A). \quad \blacksquare$$

---

### Q6.2 `[CALC]` Finding the Standard Matrix $[T]$ from Standard Basis Images
**Sources:** *Spring 2022 FE Q9(a)–(c) [10 Marks]; Spring 2025 FE Solution P7(b)*

> Let $T: \mathbb{R}^3 \to \mathbb{R}^2$ be a linear transformation with:
> - **Version A (Sp22 FE Q9):** $T(\mathbf{e}_1) = (1, 1),\; T(\mathbf{e}_2) = (3, 0),\; T(\mathbf{e}_3) = (4, 7)$. Find: (a) $T(2,4,6)$, (b) $T(x,y,z)$, (c) the matrix of $T$.
> - **Version B (Sp25 FE P7b):** $T(\mathbf{e}_1) = (1, 1),\; T(\mathbf{e}_2) = (3, 0),\; T(\mathbf{e}_3) = (4, -7)$. Find $[T]$.

**Solution:**
- **Version A:**
  - *(a)* $T(2,4,6) = 2T(\mathbf{e}_1) + 4T(\mathbf{e}_2) + 6T(\mathbf{e}_3) = 2(1,1) + 4(3,0) + 6(4,7) = (2+12+24,\; 2+0+42) = \mathbf{(38, 44)}$.
  - *(b)* $T(x,y,z) = x(1,1) + y(3,0) + z(4,7) = \mathbf{(x + 3y + 4z,\; x + 7z)}$.
  - *(c)* $[T] = \big[\,T(\mathbf{e}_1) \;\; T(\mathbf{e}_2) \;\; T(\mathbf{e}_3)\,\big] = \mathbf{\begin{bmatrix} 1 & 3 & 4 \\ 1 & 0 & 7 \end{bmatrix}}$.
- **Version B (Sp25 FE P7b):**
  - $[T] = \mathbf{\begin{bmatrix} 1 & 3 & 4 \\ 1 & 0 & -7 \end{bmatrix}}$.

---

### Q6.3 `[CALC]` Formula and Matrix of $T$ from a Custom Basis
**Source:** *Fall 2022 FE Q6(a)–(c) [5+2+3 Marks]*

> Consider the basis $S = \{\mathbf{v}_1, \mathbf{v}_2, \mathbf{v}_3\}$ for $\mathbb{R}^3$, where $\mathbf{v}_1 = (1, 1, 1)$, $\mathbf{v}_2 = (1, 1, 0)$, and $\mathbf{v}_3 = (1, 0, 0)$. Let $T: \mathbb{R}^3 \to \mathbb{R}^2$ be the linear transformation such that:
> $$T(\mathbf{v}_1) = (1, 0), \qquad T(\mathbf{v}_2) = (2, -1), \qquad T(\mathbf{v}_3) = (4, 3).$$
> - **(a)** Find a formula for $T(x_1, x_2, x_3)$.
> - **(b)** Use your formula from part (a) to find $T(1, -5, 0)$.
> - **(c)** Find the matrix of $T$.

**Solution:**
- **(a)** Write an arbitrary $\mathbf{x} = (x_1, x_2, x_3) \in \mathbb{R}^3$ as $\mathbf{x} = c_1\mathbf{v}_1 + c_2\mathbf{v}_2 + c_3\mathbf{v}_3$:
  $$(x_1, x_2, x_3) = c_1(1,1,1) + c_2(1,1,0) + c_3(1,0,0) = (c_1+c_2+c_3,\; c_1+c_2,\; c_1).$$
  Equating components gives back-substitution immediately:
  - $c_1 = x_3$
  - $c_2 = x_2 - c_1 = x_2 - x_3$
  - $c_3 = x_1 - (c_1+c_2) = x_1 - x_2$.

  Now apply linearity of $T$:
  $$\begin{aligned}
  T(x_1, x_2, x_3) &= c_1 T(\mathbf{v}_1) + c_2 T(\mathbf{v}_2) + c_3 T(\mathbf{v}_3) \\
  &= x_3(1, 0) + (x_2 - x_3)(2, -1) + (x_1 - x_2)(4, 3) \\
  &= \big(x_3 + 2x_2 - 2x_3 + 4x_1 - 4x_2,\;\; 0 - x_2 + x_3 + 3x_1 - 3x_2\big) \\
  &= \mathbf{(4x_1 - 2x_2 - x_3,\;\; 3x_1 - 4x_2 + x_3)}.
  \end{aligned}$$
  *(Sanity check: $T(1,1,1) = (4-2-1, 3-4+1) = (1,0)$; $T(1,1,0) = (2,-1)$; $T(1,0,0) = (4,3)$. $\checkmark$)*

- **(b)** $T(1, -5, 0) = \big(4(1) - 2(-5) - 0,\;\; 3(1) - 4(-5) + 0\big) = \mathbf{(14, 23)}$.

- **(c)** Reading the coefficients of $x_1, x_2, x_3$ (or evaluating $T(\mathbf{e}_1), T(\mathbf{e}_2), T(\mathbf{e}_3)$):
  $$[T] = \mathbf{\begin{bmatrix} 4 & -2 & -1 \\ 3 & -4 & 1 \end{bmatrix}}.$$

---

### Q6.4 `[CALC]` Finding $\ker(T_A)$ for a Matrix Transformation
**Source:** *Spring 2025 FE Solution Problem 5*

> Let $T_A: \mathbb{R}^4 \to \mathbb{R}^3$ be the linear transformation defined by $A = \begin{bmatrix} 1 & 4 & 5 & 2 \\ 2 & 1 & 3 & 0 \\ -1 & 3 & 2 & 2 \end{bmatrix}$. Calculate $\ker(T_A)$.

**Solution (Official Key):**
Row-reduce the augmented matrix $[A \mid \mathbf{0}]$ to RREF:
$$\begin{bmatrix} 1 & 4 & 5 & 2 & 0 \\ 2 & 1 & 3 & 0 & 0 \\ -1 & 3 & 2 & 2 & 0 \end{bmatrix}
\xrightarrow{\substack{R_2 \leftarrow R_2 - 2R_1 \\ R_3 \leftarrow R_3 + R_1}}
\begin{bmatrix} 1 & 4 & 5 & 2 & 0 \\ 0 & -7 & -7 & -4 & 0 \\ 0 & 7 & 7 & 4 & 0 \end{bmatrix}
\xrightarrow{\substack{R_3 \leftarrow R_3 + R_2 \\ R_2 \leftarrow -\frac{1}{7}R_2}}
\begin{bmatrix} 1 & 4 & 5 & 2 & 0 \\ 0 & 1 & 1 & \frac{4}{7} & 0 \\ 0 & 0 & 0 & 0 & 0 \end{bmatrix}
\xrightarrow{R_1 \leftarrow R_1 - 4R_2}
\begin{bmatrix} 1 & 0 & 1 & -\frac{2}{7} & 0 \\ 0 & 1 & 1 & \frac{4}{7} & 0 \\ 0 & 0 & 0 & 0 & 0 \end{bmatrix}.$$
Let $x_3 = s, x_4 = t$ (free variables). Then $x_1 = -s + \frac{2}{7}t$ and $x_2 = -s - \frac{4}{7}t$:
$$\ker(T_A) = \text{span}\left\{\begin{bmatrix}-1\\-1\\1\\0\end{bmatrix},\;\; \begin{bmatrix}\frac{2}{7}\\-\frac{4}{7}\\0\\1\end{bmatrix}\right\} \qquad (\dim(\ker T_A) = 2).$$

---

### Q6.5 `[CALC]` Bases and Dimensions of $\ker(T)$ and $R(T)$
**Source:** *Spring 2024 FE Q6 [12 Marks]*

> Let $T: \mathbb{R}^3 \to \mathbb{R}^3$ be the matrix transformation $T(\mathbf{x}) = A\mathbf{x}$ defined by:
> $$T(x_1, x_2, x_3) = (x_1 + x_2 + 2x_3,\;\; x_1 + x_3,\;\; 2x_1 + x_2 + 3x_3).$$
> Find bases for the kernel and range of $T$. Hence, state $\dim(\ker(T))$ and $\dim(R(T))$.

**Solution:**
Extract the standard matrix $A$ of $T$ and row-reduce it to RREF:
$$A = \begin{bmatrix} 1 & 1 & 2 \\ 1 & 0 & 1 \\ 2 & 1 & 3 \end{bmatrix}
\xrightarrow{\substack{R_2 \leftarrow R_2 - R_1 \\ R_3 \leftarrow R_3 - 2R_1}}
\begin{bmatrix} 1 & 1 & 2 \\ 0 & -1 & -1 \\ 0 & -1 & -1 \end{bmatrix}
\xrightarrow{\substack{R_2 \leftarrow -R_2 \\ R_3 \leftarrow R_3 + R_2 \\ R_1 \leftarrow R_1 - R_2}}
\begin{bmatrix} \mathbf{1} & 0 & 1 \\ 0 & \mathbf{1} & 1 \\ 0 & 0 & 0 \end{bmatrix}.$$
- **Kernel ($\ker(T) = \text{Null}(A)$):** Solving $A\mathbf{x} = \mathbf{0}$ gives $x_1 = -x_3,\; x_2 = -x_3$ with $x_3 = t$ free:
  $$\mathbf{x} = t\begin{bmatrix}-1\\-1\\1\end{bmatrix} \implies \textbf{Basis for }\ker(T) = \left\{\begin{bmatrix}-1\\-1\\1\end{bmatrix}\right\}, \quad \mathbf{\dim(\ker(T)) = 1}.$$
- **Range ($R(T) = \text{Col}(A)$):** Pivot columns of $\text{RREF}(A)$ are Columns 1 and 2, so the first two columns of the **original** matrix $A$ form a basis for $\text{Col}(A) = R(T)$:
  $$\textbf{Basis for }R(T) = \left\{\begin{bmatrix}1\\1\\2\end{bmatrix},\;\; \begin{bmatrix}1\\0\\1\end{bmatrix}\right\}, \quad \mathbf{\dim(R(T)) = 2}.$$
  *(Check Dimension Theorem: $\dim(\ker(T)) + \dim(R(T)) = 1 + 2 = 3 = \dim(\mathbb{R}^3)$. $\checkmark$)*

---

### Q6.6 `[CALC / CONCEPT]` Polynomial Multiplication Transformation $T(p(x)) = x\,p(x)$
**Source:** *Fall 2022 FE Q10(a)–(c) [3+4+3 Marks]*

> Let $T: P_2 \to P_3$ be the linear transformation given by $T(p(x)) = x\,p(x)$.
> - **(a)** Which of $x$, $0$, and $(1-x)$ are in $\ker(T)$?
> - **(b)** Is $T$ an onto transformation? Why or why not?
> - **(c)** What is the dimension of $\ker(T)$? Can you suggest a basis for it?

**Solution:**
- **(a)** A polynomial $p(x) \in P_2$ is in $\ker(T)$ iff $T(p(x)) = x\,p(x) = 0$ (the zero polynomial in $P_3$):
  - $T(x) = x^2 \neq 0 \implies x \notin \ker(T)$.
  - $T(0) = x\cdot 0 = 0 \implies \mathbf{0 \in \ker(T)}$.
  - $T(1-x) = x - x^2 \neq 0 \implies (1-x) \notin \ker(T)$.
  Only **$0$** is in $\ker(T)$.

- **(b) NO, $T$ is NOT onto.** Two clean justifications:
  - *Direct counterexample:* Every output $T(a_0 + a_1 x + a_2 x^2) = a_0 x + a_1 x^2 + a_2 x^3$ has constant term $0$. Hence any polynomial in $P_3$ with nonzero constant term, e.g., $q(x) = 1 \in P_3$, has no preimage under $T$.
  - *Dimension argument:* $\dim(P_2) = 3 < 4 = \dim(P_3)$, so $\dim(R(T)) \le 3 < \dim(P_3)$, making it impossible for $R(T)$ to equal $P_3$.

- **(c)** For any $p(x) = a_0 + a_1 x + a_2 x^2$, $T(p(x)) = a_0 x + a_1 x^2 + a_2 x^3 = 0 \iff a_0 = a_1 = a_2 = 0 \iff p(x) = 0$.
  Hence $\ker(T) = \{0\}$ (the trivial zero subspace), so:
  $$\mathbf{\dim(\ker(T)) = 0}, \qquad \text{and its basis is the } \textbf{empty set } \emptyset.$$
  *(Note: By Rank–Nullity for linear maps, $\dim(\ker(T)) + \dim(R(T)) = 0 + 3 = 3 = \dim(P_2)$.)*

---

## Appendix: Files Scanned & Excluded Topics

All **25 unique files** (out of 29 total, accounting for 4 exact MD5 duplicates) in `past assessments/` were examined:
- **Exams & Solutions:** `finalterm_solution.pdf` (Sp25 FE), `LA+FE+Fall+22.pdf`, `LA+FE.pdf` (Sp22 FE), `LA+FE+Spring+24.pdf`, `LA+Mid+Fall+22.pdf`, `LA Mid Spring 23.pdf`, `LA Mid Spring 24 (Final).pdf` (+ dup `LA+Mid+Spring+24+%28Final%29.pdf`), `LA Mid Spring 26 (Final) (1).pdf`, `LA+Midterm.pdf` (Sp22 Mid), `LA+Spring+23+FE.pdf`, `MID+A+Solution.docx`, `MID+B+Solution.docx`.
- **Quizzes (all 13 unique):** `quiz1` (+ dup), `quiz2`, `quiz3`, `quiz4`, `quiz5`, `quiz6`, `quiz7` (+ dup), `quiz8`, `quiz9`, `quiz10`, `quiz11` (+ dup), `quiz13`, `quiz14`.

**Excluded as Outside Midterm II Scope:**
- **Pre-Midterm I (Chapters 1–2):** Solving linear systems / parameter conditions / $LU$ decomposition / elementary matrix calculations / matrix algebra ($AX=XB$, $AB=BA$, $A^{r+s}$) / determinant identities & cofactor rules / Cramer's rule proof ($D_k$) / skew-symmetric diagonal $=0$ (`quiz1`–`quiz5`, Mid Part A sections, `MID+A+Solution.docx`, `LA Mid Spring 26` Part B Q1–Q2 & Q4). *(Master Theorem / consistency bridges are kept in Q5.3.)*
- **Post-Midterm II / Final-Only (Chapters 6.3 & 7):** Gram–Schmidt process & orthonormal bases (`LA+FE` Q3, Q4(c), `LA+Spring+24` Q7, `LA+Spring+23` Q10, `finalterm_solution` P6, P7(a), P10(a), `quiz11` P3, P4(b), P7, P8), eigenvalues, eigenvectors, nilpotent eigenvalues & diagonalization (`LA+FE` Q1, Q2, Q6; `LA+FE+Fall+22` Q5, Q9; `LA+Spring+23+FE` Q6(a),(b), Q7, Q10; `LA+FE+Spring+24` Q8(a), Q10; `finalterm_solution` P8, P10(b); `quiz13`, `quiz14`).
