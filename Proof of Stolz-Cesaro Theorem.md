**The First Form of the Stolz-Cesàro Theorem**
If $(b_n)_{n=1}^\infty$ is a sequence of positive real numbers such that $\sum_{n=1}^\infty b_n=\infty$, then for any sequence $(a_n)_{n=1}^\infty\subset\mathbb{R}$, we have the following inequalities:


$$\begin{aligned}{\lim\sup}_{n\to\infty}\frac{a_1+a_2+\cdots+a_n}{b_1+b_2+\cdots+b_n}\le{\lim\sup}_{n\to\infty}\frac{a_n}{b_n};\quad(1)\\{\lim\inf}_{n\to\infty}\frac{a_1+a_2+\cdots+a_n}{b_1+b_2+\cdots+b_n}\ge{\lim\inf}_{n\to\infty}\frac{a_n}{b_n}.\quad(2)\end{aligned}$$


We first prove (1).

**Lemma (Equivalent form of limit superior)**
Let $\{a_n\}$ be a sequence and $l\in\mathbb{R}$. Then the first proposition below implies the second proposition.

1. ${\lim\sup}_{n\to\infty}a_n=l$
2. For any $\epsilon>0$, there exists $N\in\mathbb{N}$ such that $a_n<l+\epsilon$ for all $n\ge N$.

**Proof**
Assume ${\lim\sup}_{n\to\infty}a_n=l$. If we let $s_n=\sup_{i\ge n}a_i$, then $\lim_{n\to\infty}s_n=l$.
Thus, for any $\epsilon>0$, there exists $N\in\mathbb{N}$ such that $l-\epsilon<s_n<l+\epsilon$ for all $n\ge N$.
That is to say, $\sup\{a_i:i\ge n\}<l+\epsilon$. Therefore,


$$a_n\le\sup_{i\ge n}a_i<l+\epsilon\implies a_n<l+\epsilon$$


$\square$

According to the Lemma, let $L={\lim\sup}_{n\to\infty}(a_n/b_n)$. Then for a fixed $l>L$, there exists $k\in\mathbb{N}$ such that:


$$\frac{a_n}{b_n}\le l,\,\,\forall n>k\tag{3}$$


Using (3), we obtain:


$$a_1+a_2+\cdots+a_n\le a_1+\cdots+a_k+l(b_{k+1}+b_{k+2}+\cdots+b_n),\quad\forall n>k\tag{4}$$


If we denote $a_1+\cdots+a_n$ as $A_n$ and $b_1+\cdots+b_n$ as $B_n$, the above inequality is equivalent to:


$$A_n\le A_k+l(B_n-B_k)$$


Dividing both sides by $B_n$, we get:


$$\frac{A_n}{B_n}\le l+\frac{A_k-lB_k}{B_n}\tag{5}$$


Because $B_n\to\infty$ by the given assumption, by fixing $k$ and taking the limit superior ($\lim\sup$) on both sides of (5), we get:


$${\lim\sup}_{n\to\infty}(A_n/B_n)\le l$$


That is to say, we have obtained:


$${\lim\sup}_{n\to\infty}\frac{a_1+\cdots+a_n}{b_1+\cdots+b_n} \le l,\,\,\forall l> L$$


which is equivalent to:


$${\lim\sup}_{n\to\infty}\frac{a_1+\cdots+a_n}{b_1+\cdots+b_n}\le L$$


For the proof of (2), we consider $(-a_n)_{n=1}^\infty$. According to the proven (1), we have:


$${\lim\sup}_{n\to\infty}\frac{(-a_1)+\cdots+(-a_n)}{b_1+\cdots+b_n}\le {\lim\sup}_{n\to\infty}\left(\frac{-a_n}{b_n}\right)$$


Because $\sup(-a)=-\inf(a)$, we can deduce (2), which is:


$${\lim\inf}_{n\to\infty}\frac{a_1+a_2+\cdots+a_n}{b_1+b_2+\cdots+b_n}\ge{\lim\inf}_{n\to\infty}\frac{a_n}{b_n}$$


$\square$

**Equivalent Form of the Stolz-Cesàro Theorem**
If $(y_n)_{n=1}^\infty$ is a strictly increasing sequence, and $\lim_{n\to\infty}y_n=\infty$, then for any sequence $(x_n)_{n=1}^\infty$, we have the following two inequalities:


$$\begin{aligned}\lim\sup_{n\to\infty}\frac{x_n}{y_n}&\leq\lim\sup_{n\to\infty}\frac{x_n-x_{n-1}}{y_n-y_{n-1}};\quad(6)\\\lim\inf_{n\to\infty}\frac{x_n}{y_n}&\geq\lim\inf_{n\to\infty}\frac{x_n-x_{n-1}}{y_n-y_{n-1}}.\quad(7)\end{aligned}$$


In particular, if the sequence $\left(\frac{x_n-x_{n-1}}{y_n-y_{n-1}}\right)$ has a limit (i.e., converges), then:


$$\lim_{n\to\infty}\frac{x_n}{y_n}=\lim_{n\to\infty}\frac{x_n-x_{n-1}}{y_n-y_{n-1}}$$


We begin the proof.
In fact, to prove this, we only need to substitute $a_1=x_1, b_1=y_1$, and $a_n=x_n-x_{n-1}, b_n=y_n-y_{n-1}$ (for $n\ge 2$) into **The First Form of the Stolz-Cesàro Theorem**.

**"Additive" Cesàro Theorem, Part I**
For any sequence $(a_n)_{n=1}^\infty\subset\mathbb{R}$, we have:


$${\lim\sup}_{n\to\infty}\frac{a_1+a_2+\cdots+a_n}{n}\le{\lim\sup}_{n\to\infty}a_n;$$

$${\lim\inf}_{n\to\infty}\frac{a_1+a_2+\cdots+a_n}{n}\ge{\lim\inf}_{n\to\infty}a_n$$


In particular, if the sequence $(a_n)_{n=1}^\infty$ has a limit,


$$\lim_{n\to\infty}\frac{a_1+a_2+\cdots+a_n}{n}=\lim_{n\to\infty}a_n$$


**Proof**
Simply set $b_n=1$ for all $n$ in the First Form of the Stolz-Cesàro Theorem.

**Part II**
For any sequence $(x_n)_{n=1}^\infty\subset\mathbb{R}$, we have:


$${\lim\sup}_{n\to\infty}\frac{x_n}{n}\le{\lim\sup}_{n\to\infty}(x_n-x_{n-1})$$

$${\lim\inf}_{n\to\infty}\frac{x_n}{n}\ge{\lim\inf}_{n\to\infty}(x_n-x_{n-1})$$


In particular, if the sequence $(x_n)_{n=1}^\infty$ has a limit,


$$\lim_{n\to\infty}\frac{x_n}{n}=\lim_{n\to\infty}(x_n-x_{n-1})$$


**Proof**
Simply set $y_n=n$ in the Equivalent Form of the Stolz-Cesàro Theorem.

**Multiplicative Cesàro Theorem, Part I**


$${\lim\sup}_{n\to\infty}\sqrt[n]{a_1a_2\cdots a_n}\le {\lim\sup}_{n\to\infty}a_n$$

$${\lim\inf}_{n\to\infty}\sqrt[n]{a_1a_2\cdots a_n}\ge {\lim\inf}_{n\to\infty}a_n$$


**Proof**
Let $b_n=\ln a_n$, so that $\sqrt[n]{a_1a_2\cdots a_n}=\exp\left(\frac{b_1+\cdots+b_n}{n}\right)$, and simply apply Part I of the Additive Cesàro Theorem.

**Multiplicative Cesàro Theorem, Part II**


$$\lim\sup_{n\to\infty}\sqrt[n]{x_n}\leq\lim\sup_{n\to\infty}\frac{x_n}{x_{n-1}};$$

$$\lim\inf_{n\to\infty}\sqrt[n]{x_n}\geq\lim\inf_{n\to\infty}\frac{x_n}{x_{n-1}}.$$


**Proof**
Let $a_n=\ln x_n$, so that $\sqrt[n]{x_n}=\exp\left(\frac{a_n}{n}\right)$, and simply apply Part II of the Additive Cesàro Theorem.