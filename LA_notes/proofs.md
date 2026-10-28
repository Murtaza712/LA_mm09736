# Linear Algebra Proofs

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

---

### Proof of Part (a): $\mathbf{u} \cdot \mathbf{v} = \mathbf{v} \cdot \mathbf{u}$ (Symmetry)

By definition of the Euclidean inner product:
$$\mathbf{u} \cdot \mathbf{v} = u_1 v_1 + u_2 v_2 + \dots + u_n v_n$$

Since multiplication of real numbers is commutative ($u_i v_i = v_i u_i$ for all real numbers $u_i, v_i$):
$$= v_1 u_1 + v_2 u_2 + \dots + v_n u_n$$
$$= \mathbf{v} \cdot \mathbf{u}$$

$$\blacksquare$$

---

### Proof of Part (b): $(\mathbf{u} + \mathbf{v}) \cdot \mathbf{w} = \mathbf{u} \cdot \mathbf{w} + \mathbf{v} \cdot \mathbf{w}$ (Additivity)

First, compute the vector addition:
$$\mathbf{u} + \mathbf{v} = (u_1 + v_1, \; u_2 + v_2, \; \dots, \; u_n + v_n)$$

Now, compute the inner product with $\mathbf{w}$:
$$(\mathbf{u} + \mathbf{v}) \cdot \mathbf{w} = (u_1 + v_1)w_1 + (u_2 + v_2)w_2 + \dots + (u_n + v_n)w_n$$

By the distributive property of real numbers ($(u_i + v_i)w_i = u_i w_i + v_i w_i$):
$$= (u_1 w_1 + v_1 w_1) + (u_2 w_2 + v_2 w_2) + \dots + (u_n w_n + v_n w_n)$$

Regrouping terms by vector components:
$$= (u_1 w_1 + u_2 w_2 + \dots + u_n w_n) + (v_1 w_1 + v_2 w_2 + \dots + v_n w_n)$$
$$= \mathbf{u} \cdot \mathbf{w} + \mathbf{v} \cdot \mathbf{w}$$

$$\blacksquare$$

---

### Proof of Part (c): $(k\mathbf{u}) \cdot \mathbf{v} = k(\mathbf{u} \cdot \mathbf{v})$ (Homogeneity)

First, compute scalar multiplication:
$$k\mathbf{u} = (k u_1, \; k u_2, \; \dots, \; k u_n)$$

Now, compute the inner product with $\mathbf{v}$:
$$(k\mathbf{u}) \cdot \mathbf{v} = (k u_1)v_1 + (k u_2)v_2 + \dots + (k u_n)v_n$$

By the associative and commutative properties of real multiplication ($(k u_i)v_i = k(u_i v_i)$):
$$= k(u_1 v_1) + k(u_2 v_2) + \dots + k(u_n v_n)$$

Factoring out the common scalar $k$:
$$= k(u_1 v_1 + u_2 v_2 + \dots + u_n v_n)$$
$$= k(\mathbf{u} \cdot \mathbf{v})$$

$$\blacksquare$$

---

### Proof of Part (d): $\mathbf{v} \cdot \mathbf{v} \ge 0$, and $\mathbf{v} \cdot \mathbf{v} = 0 \iff \mathbf{v} = \mathbf{0}$ (Positivity)

By definition of the Euclidean inner product:
$$\mathbf{v} \cdot \mathbf{v} = v_1 v_1 + v_2 v_2 + \dots + v_n v_n = v_1^2 + v_2^2 + \dots + v_n^2$$

1. **Non-negativity ($\mathbf{v} \cdot \mathbf{v} \ge 0$):**
   The square of any real number is non-negative ($v_i^2 \ge 0$ for all $i = 1, 2, \dots, n$).
   Because the sum of non-negative real numbers is non-negative:
   $$\mathbf{v} \cdot \mathbf{v} = v_1^2 + v_2^2 + \dots + v_n^2 \ge 0$$

2. **Zero condition ($\mathbf{v} \cdot \mathbf{v} = 0 \iff \mathbf{v} = \mathbf{0}$):**
   A sum of squares of real numbers equals zero:
   $$v_1^2 + v_2^2 + \dots + v_n^2 = 0$$
   if and only if **every individual term is zero**:
   $$v_1 = 0, \quad v_2 = 0, \quad \dots, \quad v_n = 0$$
   which holds if and only if:
   $$\mathbf{v} = (0, 0, \dots, 0) = \mathbf{0}$$

$$\blacksquare$$

---

## Theorem 4.1.4: Properties of Length (Norm) in $\mathbb{R}^n$

### Statement
> If $\mathbf{u}$ and $\mathbf{v}$ are vectors in $\mathbb{R}^n$ and $k$ is any scalar ($k \in \mathbb{R}$), then:
> * **(a) Non-negativity:** $\|\mathbf{u}\| \ge 0$
> * **(b) Zero Condition:** $\|\mathbf{u}\| = 0$ if and only if $\mathbf{u} = \mathbf{0}$
> * **(c) Homogeneity:** $\|k\mathbf{u}\| = |k| \|\mathbf{u}\|$
> * **(d) Triangle Inequality:** $\|\mathbf{u} + \mathbf{v}\| \le \|\mathbf{u}\| + \|\mathbf{v}\|$

Let $\mathbf{u} = (u_1, u_2, \dots, u_n)$ and $\mathbf{v} = (v_1, v_2, \dots, v_n)$. 
By definition, the Euclidean norm (length) of a vector is:
$$\|\mathbf{u}\| = \sqrt{\mathbf{u} \cdot \mathbf{u}} = \sqrt{u_1^2 + u_2^2 + \dots + u_n^2}$$

---

### Proof of Part (a): $\|\mathbf{u}\| \ge 0$

By definition:
$$\|\mathbf{u}\| = \sqrt{u_1^2 + u_2^2 + \dots + u_n^2}$$

Since $u_i^2 \ge 0$ for each component $i = 1, \dots, n$, the sum of squares is non-negative:
$$u_1^2 + u_2^2 + \dots + u_n^2 \ge 0$$

The principal (non-negative) square root of a non-negative real number is always non-negative:
$$\|\mathbf{u}\| \ge 0$$

$$\blacksquare$$

---

### Proof of Part (b): $\|\mathbf{u}\| = 0 \iff \mathbf{u} = \mathbf{0}$

$$\|\mathbf{u}\| = 0 \iff \sqrt{u_1^2 + u_2^2 + \dots + u_n^2} = 0$$

Squaring both sides:
$$\iff u_1^2 + u_2^2 + \dots + u_n^2 = 0$$

Because each $u_i^2 \ge 0$, a sum of non-negative real numbers can only equal zero if every individual term is zero:
$$\iff u_1 = 0, \quad u_2 = 0, \quad \dots, \quad u_n = 0$$
$$\iff \mathbf{u} = (0, 0, \dots, 0) = \mathbf{0}$$

$$\blacksquare$$

---

### Proof of Part (c): $\|k\mathbf{u}\| = |k| \|\mathbf{u}\|$

Let $\mathbf{u} = (u_1, u_2, \dots, u_n)$. The scaled vector is:
$$k\mathbf{u} = (ku_1, ku_2, \dots, ku_n)$$

Applying the definition of the norm:
$$\|k\mathbf{u}\| = \sqrt{(ku_1)^2 + (ku_2)^2 + \dots + (ku_n)^2}$$
$$= \sqrt{k^2 u_1^2 + k^2 u_2^2 + \dots + k^2 u_n^2}$$

Factor out the common term $k^2$:
$$= \sqrt{k^2 (u_1^2 + u_2^2 + \dots + u_n^2)}$$

Using the square root property $\sqrt{a \cdot b} = \sqrt{a} \cdot \sqrt{b}$, and noting that $\sqrt{k^2} = |k|$:
$$= \sqrt{k^2} \cdot \sqrt{u_1^2 + u_2^2 + \dots + u_n^2}$$
$$= |k| \|\mathbf{u}\|$$

$$\blacksquare$$

---

### Proof of Part (d): $\|\mathbf{u} + \mathbf{v}\| \le \|\mathbf{u}\| + \|\mathbf{v}\|$ (The Triangle Inequality)

Start with the left-hand side squared using the inner product relationship $\|\mathbf{x}\|^2 = \mathbf{x} \cdot \mathbf{x}$:
$$\|\mathbf{u} + \mathbf{v}\|^2 = (\mathbf{u} + \mathbf{v}) \cdot (\mathbf{u} + \mathbf{v})$$

Expanding using the distributive and symmetry properties of the dot product (Theorem 4.1.2):
$$= \mathbf{u} \cdot \mathbf{u} + \mathbf{u} \cdot \mathbf{v} + \mathbf{v} \cdot \mathbf{u} + \mathbf{v} \cdot \mathbf{v}$$
$$= \|\mathbf{u}\|^2 + 2(\mathbf{u} \cdot \mathbf{v}) + \|\mathbf{v}\|^2$$

By the properties of real numbers, any number is less than or equal to its absolute value ($x \le |x|$):
$$\le \|\mathbf{u}\|^2 + 2|\mathbf{u} \cdot \mathbf{v}| + \|\mathbf{v}\|^2$$

Now, apply the **Cauchy-Schwarz Inequality** ($|\mathbf{u} \cdot \mathbf{v}| \le \|\mathbf{u}\| \|\mathbf{v}\|$):
$$\le \|\mathbf{u}\|^2 + 2\|\mathbf{u}\| \|\mathbf{v}\| + \|\mathbf{v}\|^2$$

Notice the perfect square identity on the right side ($a^2 + 2ab + b^2 = (a+b)^2$):
$$= (\|\mathbf{u}\| + \|\mathbf{v}\|)^2$$

Putting the entire inequality chain together:
$$\|\mathbf{u} + \mathbf{v}\|^2 \le (\|\mathbf{u}\| + \|\mathbf{v}\|)^2$$

Since both $\|\mathbf{u} + \mathbf{v}\|$ and $(\|\mathbf{u}\| + \|\mathbf{v}\|)$ are non-negative, taking the positive square root of both sides preserves the inequality:
$$\|\mathbf{u} + \mathbf{v}\| \le \|\mathbf{u}\| + \|\mathbf{v}\|$$

$$\blacksquare$$

---

## Theorem 4.1.5: Properties of Distance in $\mathbb{R}^n$

### Statement
> If $\mathbf{u}, \mathbf{v}$, and $\mathbf{w}$ are vectors in $\mathbb{R}^n$ and $k$ is any scalar, then:
> * **(a) Non-negativity:** $d(\mathbf{u}, \mathbf{v}) \ge 0$
> * **(b) Zero Condition / Identity:** $d(\mathbf{u}, \mathbf{v}) = 0$ if and only if $\mathbf{u} = \mathbf{v}$
> * **(c) Symmetry:** $d(\mathbf{u}, \mathbf{v}) = d(\mathbf{v}, \mathbf{u})$
> * **(d) Triangle Inequality:** $d(\mathbf{u}, \mathbf{v}) \le d(\mathbf{u}, \mathbf{w}) + d(\mathbf{w}, \mathbf{v})$

Let $\mathbf{u} = (u_1, u_2, \dots, u_n)$ and $\mathbf{v} = (v_1, v_2, \dots, v_n)$ be vectors in $\mathbb{R}^n$.
By definition, the Euclidean distance between $\mathbf{u}$ and $\mathbf{v}$ is given by the norm of their difference:
$$d(\mathbf{u}, \mathbf{v}) = \|\mathbf{u} - \mathbf{v}\| = \sqrt{(u_1 - v_1)^2 + (u_2 - v_2)^2 + \dots + (u_n - v_n)^2}$$

---

### Proof of Part (a): $d(\mathbf{u}, \mathbf{v}) \ge 0$ (Non-negativity)

**Method 1 (Using Norm Properties):**
By definition of distance:
$$d(\mathbf{u}, \mathbf{v}) = \|\mathbf{u} - \mathbf{v}\|$$
Let $\mathbf{x} = \mathbf{u} - \mathbf{v}$. By Theorem 4.1.4(a), the norm of any vector in $\mathbb{R}^n$ is non-negative:
$$\|\mathbf{x}\| \ge 0 \implies \|\mathbf{u} - \mathbf{v}\| \ge 0$$
Therefore:
$$d(\mathbf{u}, \mathbf{v}) \ge 0$$

**Method 2 (Component-wise):**
$$d(\mathbf{u}, \mathbf{v}) = \sqrt{(u_1 - v_1)^2 + (u_2 - v_2)^2 + \dots + (u_n - v_n)^2}$$
Since $(u_i - v_i)^2 \ge 0$ for each $i = 1, 2, \dots, n$, the sum of squares is non-negative:
$$\sum_{i=1}^{n} (u_i - v_i)^2 \ge 0$$
Because the principal square root of a non-negative number is non-negative:
$$d(\mathbf{u}, \mathbf{v}) \ge 0$$

$$\blacksquare$$

---

### Proof of Part (b): $d(\mathbf{u}, \mathbf{v}) = 0 \iff \mathbf{u} = \mathbf{v}$ (Zero Condition)

**Method 1 (Using Norm Properties):**
By definition:
$$d(\mathbf{u}, \mathbf{v}) = 0 \iff \|\mathbf{u} - \mathbf{v}\| = 0$$
By Theorem 4.1.4(b), the norm of a vector is zero if and only if the vector itself is the zero vector:
$$\|\mathbf{u} - \mathbf{v}\| = 0 \iff \mathbf{u} - \mathbf{v} = \mathbf{0}$$
Adding $\mathbf{v}$ to both sides:
$$\iff \mathbf{u} = \mathbf{v}$$

**Method 2 (Component-wise):**
$$d(\mathbf{u}, \mathbf{v}) = 0 \iff \sqrt{(u_1 - v_1)^2 + (u_2 - v_2)^2 + \dots + (u_n - v_n)^2} = 0$$
Squaring both sides:
$$\iff (u_1 - v_1)^2 + (u_2 - v_2)^2 + \dots + (u_n - v_n)^2 = 0$$
A sum of non-negative squares equals zero if and only if every term is zero:
$$\iff (u_i - v_i)^2 = 0 \quad \text{for all } i = 1, 2, \dots, n$$
$$\iff u_i - v_i = 0 \iff u_i = v_i \quad \text{for all } i = 1, 2, \dots, n$$
$$\iff \mathbf{u} = \mathbf{v}$$

$$\blacksquare$$

---

### Proof of Part (c): $d(\mathbf{u}, \mathbf{v}) = d(\mathbf{v}, \mathbf{u})$ (Symmetry)

**Method 1 (Using Norm Homogeneity):**
By definition:
$$d(\mathbf{u}, \mathbf{v}) = \|\mathbf{u} - \mathbf{v}\|$$
Factor out $-1$ from the vector difference:
$$\mathbf{u} - \mathbf{v} = -(\mathbf{v} - \mathbf{u}) = (-1)(\mathbf{v} - \mathbf{u})$$
Using Theorem 4.1.4(c) ($\|k\mathbf{x}\| = |k|\|\mathbf{x}\|$ with $k = -1$):
$$\|(-1)(\mathbf{v} - \mathbf{u})\| = |-1| \|\mathbf{v} - \mathbf{u}\| = 1 \cdot \|\mathbf{v} - \mathbf{u}\| = \|\mathbf{v} - \mathbf{u}\|$$
Since $\|\mathbf{v} - \mathbf{u}\| = d(\mathbf{v}, \mathbf{u})$:
$$d(\mathbf{u}, \mathbf{v}) = d(\mathbf{v}, \mathbf{u})$$

**Method 2 (Component-wise):**
In each component of the sum:
$$(u_i - v_i)^2 = [-(v_i - u_i)]^2 = (-1)^2 (v_i - u_i)^2 = (v_i - u_i)^2$$
Thus:
$$d(\mathbf{u}, \mathbf{v}) = \sqrt{\sum_{i=1}^{n} (u_i - v_i)^2} = \sqrt{\sum_{i=1}^{n} (v_i - u_i)^2} = d(\mathbf{v}, \mathbf{u})$$

$$\blacksquare$$

---

### Proof of Part (d): $d(\mathbf{u}, \mathbf{v}) \le d(\mathbf{u}, \mathbf{w}) + d(\mathbf{w}, \mathbf{v})$ (The Triangle Inequality for Distance)

By definition:
$$d(\mathbf{u}, \mathbf{v}) = \|\mathbf{u} - \mathbf{v}\|$$

Add and subtract the third vector $\mathbf{w}$ inside the difference:
$$\mathbf{u} - \mathbf{v} = (\mathbf{u} - \mathbf{w}) + (\mathbf{w} - \mathbf{v})$$

Taking the norm of both sides:
$$d(\mathbf{u}, \mathbf{v}) = \|(\mathbf{u} - \mathbf{w}) + (\mathbf{w} - \mathbf{v})\|$$

Let $\mathbf{a} = \mathbf{u} - \mathbf{w}$ and $\mathbf{b} = \mathbf{w} - \mathbf{v}$. By the Triangle Inequality for vector norms (Theorem 4.1.4(d), $\|\mathbf{a} + \mathbf{b}\| \le \|\mathbf{a}\| + \|\mathbf{b}\|$):
$$\|(\mathbf{u} - \mathbf{w}) + (\mathbf{w} - \mathbf{v})\| \le \|\mathbf{u} - \mathbf{w}\| + \|\mathbf{w} - \mathbf{v}\|$$

By definition of distance:
$$\|\mathbf{u} - \mathbf{w}\| = d(\mathbf{u}, \mathbf{w}) \quad \text{and} \quad \|\mathbf{w} - \mathbf{v}\| = d(\mathbf{w}, \mathbf{v})$$

Substituting these back into the inequality:
$$d(\mathbf{u}, \mathbf{v}) \le d(\mathbf{u}, \mathbf{w}) + d(\mathbf{w}, \mathbf{v})$$

$$\blacksquare$$

---

### Key Geometric Takeaways:
* $d(\mathbf{u}, \mathbf{v})$ represents the straight-line Euclidean distance between two points.
* Any detour via a third point $\mathbf{w}$ can never be shorter than the straight-line segment: $d(\mathbf{u}, \mathbf{v}) \le d(\mathbf{u}, \mathbf{w}) + d(\mathbf{w}, \mathbf{v})$.
* Equality holds if and only if $\mathbf{w}$ lies directly on the straight-line segment between $\mathbf{u}$ and $\mathbf{v}$.

---

## Theorem 4.1.6: The Polarization Identity in $\mathbb{R}^n$

### Statement
> If $\mathbf{u}$ and $\mathbf{v}$ are vectors in $\mathbb{R}^n$ with the Euclidean inner product, then:
> $$\mathbf{u} \cdot \mathbf{v} = \frac{1}{4} \|\mathbf{u} + \mathbf{v}\|^2 - \frac{1}{4} \|\mathbf{u} - \mathbf{v}\|^2$$

---

### What is this and why does it matter?
* **Reconstructing the Dot Product from Lengths alone:**
  Notice that the left-hand side is the **inner product** $\mathbf{u} \cdot \mathbf{v}$ (which determines angles and orthogonality). The right-hand side contains **only norms (lengths)** of vectors ($\|\mathbf{u} + \mathbf{v}\|$ and $\|\mathbf{u} - \mathbf{v}\|$).
  This proves that **if you only have a tool to measure lengths, you can still compute angles and dot products!**
* **High School Algebra Connection:**
  This is the vector analog of the familiar binomial product formula:
  $$xy = \frac{1}{4}(x + y)^2 - \frac{1}{4}(x - y)^2$$
  where squaring $(x+y)$ and $(x-y)$ produces cross-terms $2xy$ and $-2xy$, whose difference leaves $4xy$.

---

### Proof

First, expand the squared norm of the sum $\|\mathbf{u} + \mathbf{v}\|^2$ using the relationship between norm and inner product ($\|\mathbf{x}\|^2 = \mathbf{x} \cdot \mathbf{x}$):
$$\|\mathbf{u} + \mathbf{v}\|^2 = (\mathbf{u} + \mathbf{v}) \cdot (\mathbf{u} + \mathbf{v})$$

Applying the distributive and symmetry properties of the Euclidean inner product (Theorem 4.1.2):
$$\|\mathbf{u} + \mathbf{v}\|^2 = \mathbf{u} \cdot \mathbf{u} + 2(\mathbf{u} \cdot \mathbf{v}) + \mathbf{v} \cdot \mathbf{v}$$

Using $\|\mathbf{u}\|^2 = \mathbf{u} \cdot \mathbf{u}$ and $\|\mathbf{v}\|^2 = \mathbf{v} \cdot \mathbf{v}$:
$$\|\mathbf{u} + \mathbf{v}\|^2 = \|\mathbf{u}\|^2 + 2(\mathbf{u} \cdot \mathbf{v}) + \|\mathbf{v}\|^2 \quad \text{--- (Equation 1)}$$

Next, expand the squared norm of the difference $\|\mathbf{u} - \mathbf{v}\|^2$:
$$\|\mathbf{u} - \mathbf{v}\|^2 = (\mathbf{u} - \mathbf{v}) \cdot (\mathbf{u} - \mathbf{v})$$
$$= \mathbf{u} \cdot \mathbf{u} - 2(\mathbf{u} \cdot \mathbf{v}) + \mathbf{v} \cdot \mathbf{v}$$
$$\|\mathbf{u} - \mathbf{v}\|^2 = \|\mathbf{u}\|^2 - 2(\mathbf{u} \cdot \mathbf{v}) + \|\mathbf{v}\|^2 \quad \text{--- (Equation 2)}$$

Now, subtract **Equation 2** from **Equation 1**:
$$\|\mathbf{u} + \mathbf{v}\|^2 - \|\mathbf{u} - \mathbf{v}\|^2 = \left( \|\mathbf{u}\|^2 + 2(\mathbf{u} \cdot \mathbf{v}) + \|\mathbf{v}\|^2 \right) - \left( \|\mathbf{u}\|^2 - 2(\mathbf{u} \cdot \mathbf{v}) + \|\mathbf{v}\|^2 \right)$$

Notice that the squared terms $\|\mathbf{u}\|^2$ and $\|\mathbf{v}\|^2$ cancel out:
$$\|\mathbf{u} + \mathbf{v}\|^2 - \|\mathbf{u} - \mathbf{v}\|^2 = 2(\mathbf{u} \cdot \mathbf{v}) - \left( -2(\mathbf{u} \cdot \mathbf{v}) \right)$$
$$\|\mathbf{u} + \mathbf{v}\|^2 - \|\mathbf{u} - \mathbf{v}\|^2 = 4(\mathbf{u} \cdot \mathbf{v})$$

Divide both sides by $4$:
$$\mathbf{u} \cdot \mathbf{v} = \frac{1}{4} \|\mathbf{u} + \mathbf{v}\|^2 - \frac{1}{4} \|\mathbf{u} - \mathbf{v}\|^2$$

$$\blacksquare$$

---

### Related Identity: The Parallelogram Equation
What happens if you **add** Equations (1) and (2) instead of subtracting them?
$$\|\mathbf{u} + \mathbf{v}\|^2 + \|\mathbf{u} - \mathbf{v}\|^2 = 2\|\mathbf{u}\|^2 + 2\|\mathbf{v}\|^2$$
* **Geometric meaning:** The sum of the squares of the lengths of the diagonals of a parallelogram equals the sum of the squares of the lengths of its four sides.

---

## Definition: Orthogonality in $\mathbb{R}^n$

> Two vectors $\mathbf{u}$ and $\mathbf{v}$ in $\mathbb{R}^n$ are called **orthogonal** (denoted $\mathbf{u} \perp \mathbf{v}$) if their Euclidean inner product is zero:
> $$\mathbf{u} \cdot \mathbf{v} = 0$$

---

## Theorem 4.1.7: Pythagorean Theorem in $\mathbb{R}^n$

### Statement
> If $\mathbf{u}$ and $\mathbf{v}$ are orthogonal vectors in $\mathbb{R}^n$ with the Euclidean inner product ($\mathbf{u} \cdot \mathbf{v} = 0$), then:
> $$\|\mathbf{u} + \mathbf{v}\|^2 = \|\mathbf{u}\|^2 + \|\mathbf{v}\|^2$$

---

### Proof

Start by expressing the left-hand side using the relationship between vector norm and inner product ($\|\mathbf{x}\|^2 = \mathbf{x} \cdot \mathbf{x}$):
$$\|\mathbf{u} + \mathbf{v}\|^2 = (\mathbf{u} + \mathbf{v}) \cdot (\mathbf{u} + \mathbf{v})$$

Expand the dot product using the distributive property (Theorem 4.1.2(b)):
$$= \mathbf{u} \cdot (\mathbf{u} + \mathbf{v}) + \mathbf{v} \cdot (\mathbf{u} + \mathbf{v})$$
$$= \mathbf{u} \cdot \mathbf{u} + \mathbf{u} \cdot \mathbf{v} + \mathbf{v} \cdot \mathbf{u} + \mathbf{v} \cdot \mathbf{v}$$

Using the symmetry property ($\mathbf{v} \cdot \mathbf{u} = \mathbf{u} \cdot \mathbf{v}$) and the definition of norm ($\mathbf{u} \cdot \mathbf{u} = \|\mathbf{u}\|^2$ and $\mathbf{v} \cdot \mathbf{v} = \|\mathbf{v}\|^2$):
$$= \|\mathbf{u}\|^2 + 2(\mathbf{u} \cdot \mathbf{v}) + \|\mathbf{v}\|^2$$

Since $\mathbf{u}$ and $\mathbf{v}$ are given to be **orthogonal**, by definition $\mathbf{u} \cdot \mathbf{v} = 0$:
$$= \|\mathbf{u}\|^2 + 2(0) + \|\mathbf{v}\|^2$$
$$= \|\mathbf{u}\|^2 + \|\mathbf{v}\|^2$$

Therefore:
$$\|\mathbf{u} + \mathbf{v}\|^2 = \|\mathbf{u}\|^2 + \|\mathbf{v}\|^2$$

$$\blacksquare$$

---

### Key Takeaways & Exam Tips:
1. **Geometric Connection to Right Triangles:**
   In $\mathbb{R}^2$ or $\mathbb{R}^3$, $\mathbf{u}$ and $\mathbf{v}$ form the perpendicular legs of a right triangle, while $\mathbf{u} + \mathbf{v}$ (or $\mathbf{u} - \mathbf{v}$) forms the hypotenuse:
   $$(\text{hypotenuse})^2 = (\text{leg}_1)^2 + (\text{leg}_2)^2$$
2. **Difference of Vectors ($\|\mathbf{u} - \mathbf{v}\|^2$):**
   Similarly, for orthogonal vectors:
   $$\|\mathbf{u} - \mathbf{v}\|^2 = \|\mathbf{u}\|^2 - 2(\mathbf{u} \cdot \mathbf{v}) + \|\mathbf{v}\|^2 = \|\mathbf{u}\|^2 + \|\mathbf{v}\|^2$$
   Hence, if $\mathbf{u} \perp \mathbf{v}$, the diagonals of the rectangle spanned by $\mathbf{u}$ and $\mathbf{v}$ have equal length:
   $$\|\mathbf{u} + \mathbf{v}\| = \|\mathbf{u} - \mathbf{v}\|$$
3. **Generalization (Extension to $k$ mutually orthogonal vectors):**
   If $\{\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_k\}$ is a set of mutually orthogonal vectors ($\mathbf{v}_i \cdot \mathbf{v}_j = 0$ for $i \ne j$), then:
   $$\|\mathbf{v}_1 + \mathbf{v}_2 + \dots + \mathbf{v}_k\|^2 = \|\mathbf{v}_1\|^2 + \|\mathbf{v}_2\|^2 + \dots + \|\mathbf{v}_k\|^2$$

---

## Theorem 5.2.2: Solution Space of a Homogeneous System is a Subspace

### Statement
> If $A\mathbf{x} = \mathbf{0}$ is a homogeneous linear system of $m$ equations in $n$ unknowns, then the set of solution vectors is a subspace of $\mathbb{R}^n$.

---

### Proof

Let $W$ be the set of all solution vectors to the homogeneous system:
$$W = \{\mathbf{x} \in \mathbb{R}^n \mid A\mathbf{x} = \mathbf{0}\}$$

To prove that $W$ is a subspace of $\mathbb{R}^n$, we test the subspace conditions:

#### 1. Non-empty / Contains the Zero Vector ($\mathbf{0} \in W$)
There is at least one vector in $W$, namely the zero vector $\mathbf{0} \in \mathbb{R}^n$, because:
$$A\mathbf{0} = \mathbf{0}$$
Since the zero vector satisfies the homogeneous equation, $\mathbf{0} \in W$, meaning $W$ is non-empty.

#### 2. Closure under Vector Addition
Let $\mathbf{x}$ and $\mathbf{x}'$ be any two solution vectors in $W$. By definition:
$$A\mathbf{x} = \mathbf{0} \quad \text{and} \quad A\mathbf{x}' = \mathbf{0}$$

Now, test their sum $(\mathbf{x} + \mathbf{x}')$ by multiplying by $A$, using the distributive property of matrix multiplication:
$$A(\mathbf{x} + \mathbf{x}') = A\mathbf{x} + A\mathbf{x}' = \mathbf{0} + \mathbf{0} = \mathbf{0}$$

Since $A(\mathbf{x} + \mathbf{x}') = \mathbf{0}$, the vector $(\mathbf{x} + \mathbf{x}')$ is also a solution, meaning:
$$(\mathbf{x} + \mathbf{x}') \in W$$
Thus, $W$ is **closed under addition**.

#### 3. Closure under Scalar Multiplication
Let $\mathbf{x} \in W$ (so $A\mathbf{x} = \mathbf{0}$) and let $k$ be any real scalar ($k \in \mathbb{R}$). 
Test the scaled vector $(k\mathbf{x})$ by multiplying by $A$:
$$A(k\mathbf{x}) = k(A\mathbf{x}) = k(\mathbf{0}) = \mathbf{0}$$

Since $A(k\mathbf{x}) = \mathbf{0}$, the vector $k\mathbf{x}$ is also a solution, meaning:
$$k\mathbf{x} \in W$$
Thus, $W$ is **closed under scalar multiplication**.

---

### Conclusion
Since $W$ is non-empty and closed under both vector addition and scalar multiplication, by Theorem 5.2.1 (The Subspace Test), **$W$ is a valid subspace of $\mathbb{R}^n$**.

$$\blacksquare$$

---

### Key Takeaways for Exams:
1. **Where does $W$ live?** Because matrix $A$ is $m \times n$, the vector $\mathbf{x} = \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix}$ has $n$ entries. Therefore, $W$ is a subspace of **$\mathbb{R}^n$** (not $\mathbb{R}^m$).
2. **What if the system is non-homogeneous ($A\mathbf{x} = \mathbf{b}$ where $\mathbf{b} \neq \mathbf{0}$)?**
   * $\mathbf{0}$ is not a solution ($A\mathbf{0} = \mathbf{0} \neq \mathbf{b}$).
   * Closure fails: $A(\mathbf{x} + \mathbf{x}') = \mathbf{b} + \mathbf{b} = 2\mathbf{b} \neq \mathbf{b}$.
   * Therefore, the solution set to $A\mathbf{x} = \mathbf{b}$ is **NEVER a subspace** when $\mathbf{b} \neq \mathbf{0}$.

---

## Theorem: Consistency Theorem for Linear Systems ($A\mathbf{x} = \mathbf{b}$)

### Statement
> A system of linear equations $A\mathbf{x} = \mathbf{b}$ is **consistent** if and only if the vector $\mathbf{b}$ is in the column space of $A$:
> $$A\mathbf{x} = \mathbf{b} \text{ is consistent} \iff \mathbf{b} \in \text{Col}(A)$$

---

### Core Intuition: The Column View of Matrix Multiplication
When you multiply an $m \times n$ matrix $A$ by a column vector $\mathbf{x} = \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix}$, the resulting vector is **not just a collection of dot products**—it is fundamentally a **linear combination of the columns of $A$**:
$$A\mathbf{x} = \begin{bmatrix} \mathbf{c}_1 & \mathbf{c}_2 & \cdots & \mathbf{c}_n \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix} = x_1 \mathbf{c}_1 + x_2 \mathbf{c}_2 + \dots + x_n \mathbf{c}_n$$
The entries of $\mathbf{x}$ act as the **weights** scaling each column of $A$. 

Therefore, asking *"Does $A\mathbf{x} = \mathbf{b}$ have a solution?"* is mathematically identical to asking *"Can vector $\mathbf{b}$ be built by mixing the columns of $A$?"*

---

### Proof (Bidirectional $\iff$)

Let $A$ be an $m \times n$ matrix partitioned into its column vectors:
$$A = \begin{bmatrix} \mathbf{c}_1 & \mathbf{c}_2 & \cdots & \mathbf{c}_n \end{bmatrix}, \quad \text{where each } \mathbf{c}_j \in \mathbb{R}^m$$
and let $\mathbf{x} = \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix} \in \mathbb{R}^n$ and $\mathbf{b} \in \mathbb{R}^m$.

By the definition of matrix-vector multiplication:
$$A\mathbf{x} = x_1 \mathbf{c}_1 + x_2 \mathbf{c}_2 + \dots + x_n \mathbf{c}_n \quad \text{--- (Equation 1)}$$

---

#### 1. Forward Direction ($\implies$): Assume $A\mathbf{x} = \mathbf{b}$ is consistent
1. If the system $A\mathbf{x} = \mathbf{b}$ is consistent, there exists at least one solution vector $\mathbf{x} = \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix}$ such that:
   $$A\mathbf{x} = \mathbf{b}$$
2. Substituting Equation (1) into this equality:
   $$x_1 \mathbf{c}_1 + x_2 \mathbf{c}_2 + \dots + x_n \mathbf{c}_n = \mathbf{b}$$
3. This equation explicitly shows that $\mathbf{b}$ is expressed as a linear combination of the column vectors $\mathbf{c}_1, \mathbf{c}_2, \dots, \mathbf{c}_n$.
4. By definition, the **column space** $\text{Col}(A)$ is the span of all column vectors:
   $$\text{Col}(A) = \text{span}\{\mathbf{c}_1, \mathbf{c}_2, \dots, \mathbf{c}_n\}$$
5. Since $\mathbf{b}$ is a linear combination of these columns:
   $$\mathbf{b} \in \text{Col}(A)$$

---

#### 2. Backward Direction ($\impliedby$): Assume $\mathbf{b} \in \text{Col}(A)$
1. If $\mathbf{b} \in \text{Col}(A)$, then by definition of column space, $\mathbf{b}$ can be written as a linear combination of the columns of $A$.
2. That is, there exist scalars $s_1, s_2, \dots, s_n \in \mathbb{R}$ such that:
   $$s_1 \mathbf{c}_1 + s_2 \mathbf{c}_2 + \dots + s_n \mathbf{c}_n = \mathbf{b}$$
3. Define the vector $\mathbf{s} \in \mathbb{R}^n$ by:
   $$\mathbf{s} = \begin{bmatrix} s_1 \\ s_2 \\ \vdots \\ s_n \end{bmatrix}$$
4. Multiplying $A$ by $\mathbf{s}$ using Equation (1):
   $$A\mathbf{s} = s_1 \mathbf{c}_1 + s_2 \mathbf{c}_2 + \dots + s_n \mathbf{c}_n = \mathbf{b}$$
5. Since we found an explicit vector $\mathbf{s}$ that satisfies the equation $A\mathbf{s} = \mathbf{b}$, the linear system has a solution.
6. Therefore, the system $A\mathbf{x} = \mathbf{b}$ is **consistent**.

$$\blacksquare$$

---

### Key Exam Takeaways:
1. **The "Range" of a Matrix:**
   $\text{Col}(A)$ is the output space of the transformation $T(\mathbf{x}) = A\mathbf{x}$. You can only solve for $\mathbf{b}$ if $\mathbf{b}$ lands inside the output space.
2. **Rank Connection (Augmented Matrix):**
   $A\mathbf{x} = \mathbf{b}$ is consistent $\iff \text{rank}(A) = \text{rank}([A \mid \mathbf{b}])$.
   *(Adding $\mathbf{b}$ to the matrix doesn't add any new dimensions because $\mathbf{b}$ is already inside the span of $A$'s columns).*
