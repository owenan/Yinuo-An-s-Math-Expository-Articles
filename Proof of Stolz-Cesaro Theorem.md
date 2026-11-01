# The Stolz–Cesàro Theorem and Applications

## The First Form of the Stolz–Cesàro Theorem

If $(b_n)_{n=1}^\infty$ is a sequence of positive real numbers such that $\sum_{n=1}^\infty b_n = \infty$, then for any sequence $(a_n)_{n=1}^\infty \subset \mathbb{R}$, we have the following inequalities:

$$
\begin{aligned}
\limsup_{n \to \infty} \frac{a_1 + a_2 + \cdots + a_n}{b_1 + b_2 + \cdots + b_n} &\le \limsup_{n \to \infty} \frac{a_n}{b_n}, \quad (1) \\
\liminf_{n \to \infty} \frac{a_1 + a_2 + \cdots + a_n}{b_1 + b_2 + \cdots + b_n} &\ge \liminf_{n \to \infty} \frac{a_n}{b_n}. \quad (2)
\end{aligned}
$$

We first prove $(1)$.

---

### Lemma (Equivalent Form of Limit Superior)

Let $\{a_n\}$ be a sequence and $l \in \mathbb{R}$. Then the first statement below implies the second:

1. $\limsup_{n \to \infty} a_n = l$
2. For any $\epsilon > 0$, there exists $N \in \mathbb{N}$ such that $a_n < l + \epsilon$ for all $n \ge N$.

#### Proof of Lemma

Assume $\limsup_{n \to \infty} a_n = l$. Let $s_n = \sup_{i \ge n} a_i$, which implies $\lim_{n \to \infty} s_n = l$.

Thus, for any $\epsilon > 0$, there exists $N \in \mathbb{N}$ such that $l - \epsilon < s_n < l + \epsilon$ for all $n \ge N$. That is:

$$
\sup \{a_i : i \ge n\} < l + \epsilon.
$$

Therefore:

$$
a_n \le \sup_{i \ge n} a_i < l + \epsilon \implies a_n < l + \epsilon. \quad \square
$$

---

### Proof of Theorem (1) and (2)

According to the Lemma, let $L = \limsup_{n \to \infty} (a_n / b_n)$. For a fixed $l > L$, there exists $k \in \mathbb{N}$ such that:

$$
\frac{a_n}{b_n} \le l, \quad \forall n > k \tag{3}
$$

Using $(3)$, we obtain:

$$
a_1 + a_2 + \cdots + a_n \le a_1 + \cdots + a_k + l(b_{k+1} + b_{k+2} + \cdots + b_n), \quad \forall n > k \tag{4}
$$

Letting $A_n = a_1 + \cdots + a_n$ and $B_n = b_1 + \cdots + b_n$, inequality $(4)$ is equivalent to:

$$
A_n \le A_k + l(B_n - B_k)
$$

Dividing both sides by $B_n$:

$$
\frac{A_n}{B_n} \le l + \frac{A_k - lB_k}{B_n} \tag{5}
$$

Because $B_n \to \infty$ by hypothesis, fixing $k$ and taking the limit superior on both sides of $(5)$ gives:

$$
\limsup_{n \to \infty} \frac{A_n}{B_n} \le l
$$

Since this holds for every $l > L$, we conclude:

$$
\limsup_{n \to \infty} \frac{a_1 + \cdots + a_n}{b_1 + \cdots + b_n} \le L
$$

For $(2)$, consider $(-a_n)_{n=1}^\infty$. Applying $(1)$ to this sequence:

$$
\limsup_{n \to \infty} \frac{(-a_1) + \cdots + (-a_n)}{b_1 + \cdots + b_n} \le \limsup_{n \to \infty} \left( -\frac{a_n}{b_n} \right)
$$

Using the identity $\limsup (-x_n) = -\liminf x_n$:

$$
-\liminf_{n \to \infty} \frac{a_1 + \cdots + a_n}{b_1 + \cdots + b_n} \le -\liminf_{n \to \infty} \frac{a_n}{b_n}
$$

Multiplying by $-1$ reverses the inequality:

$$
\liminf_{n \to \infty} \frac{a_1 + a_2 + \cdots + a_n}{b_1 + b_2 + \cdots + b_n} \ge \liminf_{n \to \infty} \frac{a_n}{b_n}. \quad \square
$$

---

## Equivalent Form of the Stolz–Cesàro Theorem

If $(y_n)_{n=1}^\infty$ is a strictly increasing sequence and $\lim_{n \to \infty} y_n = \infty$, then for any sequence $(x_n)_{n=1}^\infty$:

$$
\begin{aligned}
\limsup_{n \to \infty} \frac{x_n}{y_n} &\le \limsup_{n \to \infty} \frac{x_n - x_{n-1}}{y_n - y_{n-1}}, \quad (6) \\
\liminf_{n \to \infty} \frac{x_n}{y_n} &\ge \liminf_{n \to \infty} \frac{x_n - x_{n-1}}{y_n - y_{n-1}}. \quad (7)
\end{aligned}
$$

In particular, if the sequence $\left(\frac{x_n - x_{n-1}}{y_n - y_{n-1}}\right)$ converges:

$$
\lim_{n \to \infty} \frac{x_n}{y_n} = \lim_{n \to \infty} \frac{x_n - x_{n-1}}{y_n - y_{n-1}}
$$

**Proof:**  
Substitute $a_1 = x_1$, $b_1 = y_1$, and for $n \ge 2$, set $a_n = x_n - x_{n-1}$ and $b_n = y_n - y_{n-1}$ into the First Form of the Stolz–Cesàro Theorem. $\square$

---

## Additive Cesàro Theorem

### Part I

For any sequence $(a_n)_{n=1}^\infty \subset \mathbb{R}$:

$$
\limsup_{n \to \infty} \frac{a_1 + a_2 + \cdots + a_n}{n} \le \limsup_{n \to \infty} a_n
$$

$$
\liminf_{n \to \infty} \frac{a_1 + a_2 + \cdots + a_n}{n} \ge \liminf_{n \to \infty} a_n
$$

In particular, if $(a_n)_{n=1}^\infty$ converges:

$$
\lim_{n \to \infty} \frac{a_1 + a_2 + \cdots + a_n}{n} = \lim_{n \to \infty} a_n
$$

**Proof:**  
Set $b_n = 1$ for all $n$ in the First Form of the Stolz–Cesàro Theorem. $\square$

---

### Part II

For any sequence $(x_n)_{n=1}^\infty \subset \mathbb{R}$:

$$
\limsup_{n \to \infty} \frac{x_n}{n} \le \limsup_{n \to \infty} (x_n - x_{n-1})
$$

$$
\liminf_{n \to \infty} \frac{x_n}{n} \ge \liminf_{n \to \infty} (x_n - x_{n-1})
$$

In particular, if $(x_n - x_{n-1})$ converges:

$$
\lim_{n \to \infty} \frac{x_n}{n} = \lim_{n \to \infty} (x_n - x_{n-1})
$$

**Proof:**  
Set $y_n = n$ in the Equivalent Form of the Stolz–Cesàro Theorem. $\square$

---

## Multiplicative Cesàro Theorem

### Part I

For any positive sequence $(a_n)_{n=1}^\infty$:

$$
\limsup_{n \to \infty} \sqrt[n]{a_1 a_2 \cdots a_n} \le \limsup_{n \to \infty} a_n
$$

$$
\liminf_{n \to \infty} \sqrt[n]{a_1 a_2 \cdots a_n} \ge \liminf_{n \to \infty} a_n
$$

**Proof:**  
Let $b_n = \ln a_n$, so that $\sqrt[n]{a_1 a_2 \cdots a_n} = \exp\left(\frac{b_1 + \cdots + b_n}{n}\right)$. Apply Part I of the Additive Cesàro Theorem and the monotonicity and continuity of the exponential function. $\square$

---

### Part II

For any positive sequence $(x_n)_{n=1}^\infty$:

$$
\limsup_{n \to \infty} \sqrt[n]{x_n} \le \limsup_{n \to \infty} \frac{x_n}{x_{n-1}}
$$

$$
\liminf_{n \to \infty} \sqrt[n]{x_n} \ge \liminf_{n \to \infty} \frac{x_n}{x_{n-1}}
$$

**Proof:**  
Let $a_n = \ln x_n$, so that $\sqrt[n]{x_n} = \exp\left(\frac{a_n}{n}\right)$. Apply Part II of the Additive Cesàro Theorem using $a_n - a_{n-1} = \ln(x_n / x_{n-1})$ along with the exponential function. $\square$
