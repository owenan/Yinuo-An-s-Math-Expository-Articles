Author: Owen An
## Proof Outline

We will first prove that the mathematical constant $e$ can be expressed as an infinite simple continued fraction (i.e., an infinite continued fraction where all numerators are $1$). Then, we will prove that all infinite simple continued fractions are irrational numbers.

## Beginning of the Proof

We now prove that:

$$e=\[2,1,2,1,1,4,1,1,6,1,1,8,\cdots\](1)$$

In fact, if we slightly transform the continued fraction on the right-hand side based on $1+\frac1{0+\frac1{1+\cdots}}=2+\cdots$, we obtain $e=\[1,0,1,1,2,1,1,4,1,1,8,1,1,10,1,1,\cdots\]$. This expression exhibits a much clearer pattern, making it easier to define rigorously.

## Properties of Continued Fractions

A fundamental property of continued fractions is that its $n$-th convergent $\[a_0,a_1,\cdots,a_n\]$ equals $\frac{p_n}{q_n}$, where $p_n$ and $q_n$ are recursively defined as:

$$p_n=a_np_{n-1}+p_{n-2},\quad q_n=a_nq_{n-1}+q_{n-2}$$

with the initial conditions $p_0=a_0, q_0=1, p_1=a_0a_1+1, q_1=a_1$. We will now prove that this is a valid definition. First, let us introduce a few properties that will be used in proving our lemmas.

Through direct calculation, we can obtain:

$$[a_0]=\frac{a_0}{1},\quad [a_0,a_1]=\frac{a_1a_0+1}{a_1},\quad [a_0,a_1,a_2]=\frac{a_2a_1a_0+a_2+a_0}{a_2a_1+1}$$

By expanding according to the definition, we can easily discover the following properties of continued fractions for $1\le n\le N$:

$$[a_0,a_1]=a_0+\frac1{a_1}\tag{1.1}$$

$$[a_0,a_1,\cdots,a_{n-1},a_n]=[a_0,a_1,\cdots,a_{n-2},a_{n-1}+\frac1{a_n}](1.2)$$
$$[a_0,a_1,\cdots,a_n]=a_0+\frac1{[a_1,\cdots,a_n]}=[a_0,[a_1,\cdots,a_n]](1.3)$$

Applying these properties repeatedly:

$$[a_0,a_1,\cdots,a_n]=[a_0,[a_1,\cdots,a_n]]=[a_0,[a_1,[a_2,\cdots,a_n]]]$$

$$=[a_0,[a_1+\frac1{[a_2,\cdots,a_n]}]]=[a_0,a_1+\frac1{[a_2,\cdots,a_n]}]=[a_0,a_1,[a_2,\cdots,a_n]]$$

By repeatedly utilizing this type of manipulation, we ultimately obtain for $1\le m<n\le N$:

$$[a_0,a_1,\cdots,a_n]=[a_0,a_1,\cdots,a_{m-1},[a_m,a_{m+1},\cdots,a_n]]$$

We now prove the theorem mentioned above:

**Lemma 1** If $p_n$ and $q_n$ are defined as follows:

$$p_0=a_0,\quad p_1=a_1a_0+1,\quad p_n=a_np_{n-1}+p_{n-2} \quad (2\le n\le N)(2.1)$

$$q_0=1,\quad q_1=a_1,\quad q_n=a_nq_{n-1}+q_{n-2} \quad (2\le n\le N)(2.2)$$

Then:

$$[a_0,a_1,\cdots,a_n]=\frac{p_n}{q_n}(2.3)$$

_Proof._ From the expressions mentioned above:

$$[a_0]=\frac{a_0}{1},\quad [a_0,a_1]=\frac{a_1a_0+1}{a_1}$$

Let us assume by induction that the statement holds for $n\le m$, where $m<N$. Then:

$$[a_0,a_1,\cdots,a_{m-1},a_{m}]=\frac{p_m}{q_{m}}=\frac{a_mp_{m-1}+p_{m-2}}{a_mq_{m-1}+q_{m-2}}$$

By applying $(1.2)$, we can perform the following calculation:

$$[a_0,a_1,\cdots,a_{m-1},a_m,a_{m+1}]=[a_0,a_1,\cdots,a_{m-1},a_m+\frac1{a_{m+1}}]$$

$$=\frac{(a_m+\frac1{a_{m+1}})p_{m-1}+p_{m-2}}{(a_m+\frac1{a_{m+1}})q_{m-1}+q_{m-2}}=\frac{a_{m+1}(a_mp_{m-1}+p_{m-2})+p_{m-1}}{a_{m+1}(a_mq_{m-1}+q_{m-2})+q_{m-1}}$$

$$=\frac{a_{m+1}p_m+p_{m-1}}{a_{m+1}q_m+q_{m-1}}=\frac{p_{m+1}}{q_{m+1}}$$

The formula is proven. $\square$

Let the target sequence be:

$$[1,0,1,1,2,1,1,4,1,1,8,1,1,10,1,1,\cdots]=[a_0,a_1,a_2,\cdots]$$

That is, $a_{3i+1}=2i$ and $a_{3i}=a_{3i+2}=1$.

$$\begin{gathered}p_{3n}=p_{3n-1}+p_{3n-2},\quad q_{3n}=q_{3n-1}+q_{3n-2},\\p_{3n+1}=2np_{3n}+p_{3n-1},\quad q_{3n+1}=2nq_{3n}+q_{3n-1},\\p_{3n+2}=p_{3n+1}+p_{3n},\quad q_{3n+2}=q_{3n+1}+q_{3n}.\end{gathered}$$

To prove the infinite continued fraction expansion $(1)$ for the mathematical constant $e$, we must show that $\lim_{i\to\infty}\frac{p_i}{q_i}=e$.

First, we define the following integrals:

$$\begin{gathered}A_{n}=\int_0^1\frac{x^n(x-1)^n}{n!}e^xdx,\\B_{n}=\int_0^1\frac{x^{n+1}(x-1)^n}{n!}e^xdx,\\C_{n}=\int_0^1\frac{x^n(x-1)^{n+1}}{n!}e^xdx.\end{gathered}$$

**Lemma 2** For $n\ge 0$, $A_n=q_{3n}e-p_{3n}$, $B_n=p_{3n+1}-q_{3n+1}e$, and $C_n=p_{3n+2}-q_{3n+2}e$.

_Proof._ Based on our previously defined recurrence relations:

$$\begin{gathered}p_{3n}=p_{3n-1}+p_{3n-2},\quad q_{3n}=q_{3n-1}+q_{3n-2},\\p_{3n+1}=2np_{3n}+p_{3n-1},\quad q_{3n+1}=2nq_{3n}+q_{3n-1},\\p_{3n+2}=p_{3n+1}+p_{3n},\quad q_{3n+2}=q_{3n+1}+q_{3n}.\end{gathered}$$

We **only need** to show that $A_0=e-1$, $B_0=1$, and $C_0=2-e$, along with the following three recurrence relations:

$$\begin{aligned}&A_{n}=-B_{n-1}-C_{n-1}\quad(2)\\&B_{n}=-2nA_n+C_{n-1}\quad(3)\\&C_{n}=B_n-A_n\quad(4)\end{aligned}$$

Why are these conditions sufficient?

First, the values of $A_0, B_0, C_0$ show that the formulas hold for $n=0$. Assuming the formulas hold for $n=m-1$, applying $(2)$ gives:

$$A_{m}=-B_{m-1}-C_{m-1}=-p_{3m-2}+q_{3m-2}e-p_{3m-1}+q_{3m-1}e=(q_{3m-2}+q_{3m-1})e-(p_{3m-2}+p_{3m-1})$$

Substituting the recurrence relations directly yields $A_m=q_{3m}e-p_{3m}$.

Similarly, we can derive $B_m=p_{3m+1}-q_{3m+1}e$ and $C_m=p_{3m+2}-q_{3m+2}e$.

Thus, using these three initial values, the three recurrence relations, and the properties derived from our definition of continued fraction convergents, Lemma 2 holds for all natural numbers (including $0$). We now proceed to prove these conditions.

According to the definitions of $A_n, B_n,$ and $C_n$, it is straightforward to verify that the values of $A_0, B_0,$ and $C_0$ match our assertions.

The proof of $(4)$ is trivial.

The proof of $(2)$ can be obtained by integrating both sides of the following identity:

$$\frac{x^n(x-1)^n}{n!}e^x+\frac{x^n(x-1)^{n-1}}{(n-1)!}e^x+\frac{x^{n-1}(x-1)^n}{(n-1)!}e^x=\frac d{dx}\left(\frac{x^n(x-1)^n}{n!}e^x\right)$$

The proof of $(3)$ can be obtained by integrating both sides of the following identity:

$$\frac{x^{n+1}(x-1)^n}{n!}e^x+2n\frac{x^n(x-1)^n}{n!}e^x-\frac{x^{n-1}(x-1)^n}{(n-1)!}e^x=\frac d{dx}\left(\frac{x^n(x-1)^{n+1}}{n!}e^x\right)$$

The lemma is proven. $\square$

**Theorem 1**

$$e=[1,0,1,1,2,1,1,4,1,1,8,1,1,10,1,1,\cdots]$$

_Proof._ Since for any $x\in [0,1]$, we have $|x|\le 1$ and $|x-1|\le 1$:

$$\left|\frac{x^n(x-1)^n}{n!}e^x\right| \le \frac{e^x}{n!}$$

$$\left|\frac{x^{n+1}(x-1)^n}{n!}e^x\right| \le \frac{e^x}{n!}$$

$$\left|\frac{x^n(x-1)^{n+1}}{n!}e^x\right| \le \frac{e^x}{n!}$$

By integrating these inequalities using the property $\left|\int f(x)\,dx\right|\le\int|f(x)|\,dx$, we get:

$$|A_n|\le \frac{e-1}{n!},\quad |B_n|\le\frac{e-1}{n!},\quad |C_n|\le\frac{e-1}{n!}$$

As $n\to\infty$, it follows from the Squeeze Theorem that $A_n, B_n, C_n\to 0$.

According to **Lemma 2**, we have $\lim_{i\to\infty}(q_ie-p_i)=0$.

Since $q_i\ge 1$ for all $i\ge 2$, there is no case where the denominator is zero. Therefore:

$$e=\lim_{i\to\infty}\frac{p_i}{q_i}=[1,0,1,1,2,1,1,4,1,\cdots]$$

This completes the proof. $\square$

Now, we begin to prove that all infinite simple continued fractions converge to irrational numbers.

**Lemma 3** $C_k-C_{k-1}=\frac{(-1)^{k+1}}{q_kq_{k-1}}$, where $C_k = \frac{p_k}{q_k}$ represents the convergents defined in _Lemma 1_.

_Proof._ We prove this by induction. Let the proposition $P(n)$ be $p_nq_{n-1}-p_{n-1}q_n=(-1)^{n+1}$.

For $P(1)$:

Since $p_0=a_0, p_1=a_0a_1+1, q_0=1, q_1=a_1$, we have:

$$p_1q_0-p_0q_1=(a_0a_1+1)\cdot 1-a_0\cdot a_1=1=(-1)^2 \quad \checkmark$$

Assuming the proposition holds for $P(k)$, then for $P(k+1)$:

$$p_{k+1}q_k-p_kq_{k+1}=(a_{k+1}p_k+p_{k-1})q_k-p_k(a_{k+1}q_k+q_{k-1})$$

$$=p_{k-1}q_k-p_kq_{k-1}$$

$$=(-1)(p_kq_{k-1}-p_{k-1}q_k)$$

$$=(-1)(-1)^{k+1}=(-1)^{k+2}$$

$\square$

Therefore, we have the bound $|C_m-C_n|\le\sum_{i=n}^{m-1}|C_{i+1}-C_i|$.

**Lemma 4** For any simple continued fraction, the denominators of its convergents are monotonically increasing.

_Proof._ We prove this by induction. According to the definition of a simple continued fraction, all terms $a_k$ (except possibly $a_0$) are positive integers greater than or equal to $1$. Therefore:

$$q_1=a_1\ge 1=q_0$$

$$q_2=a_2a_1+1\ge a_1+1>a_1=q_1$$

Thus, we have $1=q_0\le q_1<q_2$.

Assume $q_k>q_{k-1}\ge 1$.

Then:

$$q_{k+1}=a_{k+1}q_k+q_{k-1}\ge q_k+q_{k-1}\ge q_k+1>q_k$$

By mathematical induction, we have proven that the denominators of the convergents are monotonically increasing (excluding the possible initial case where $q_0=q_1=1$). $\square$

**Lemma 5** For all $k\ge 4$, $q_k\ge F_{k+1}$ (where $F_k$ represents the Fibonacci sequence).

_Proof._ According to Lemma 4, the denominators of the convergents are monotonically increasing, except for the possible case where $q_0=q_1=1$.

Since $q_2>q_1\ge q_0=1$, we have $q_2\ge 2$.

We inductively assume that $q_k\ge F_{k+1}$ and $q_{k-1}\ge F_k$. We need to show that $q_{k+1}\ge F_{k+2}$.

From the recurrence definition of $q_k$:

$$q_{k+1}=a_{k+1}q_k+q_{k-1}$$

Applying the induction hypothesis:

$$q_{k+1}\ge a_{k+1}F_{k+1}+F_k$$

Since $a_{k+1}\ge 1$, we have:

$$a_{k+1}F_{k+1}+F_k\ge 1\cdot F_{k+1}+F_k=F_{k+2}$$

Therefore, $q_{k+1}\ge F_{k+2}$. $\square$

**Lemma 6** For all $k\ge 5$, $q_k>k$.

_Proof._ According to Lemma 5, we only need to show that $F_{k+1}>k$.

Assume that for $k\ge 5$, we have $F_{k+1}> k$ and $F_{k}> k-1$.

Then:

$$F_{k+2}=F_{k+1}+F_k>k+(k-1)=2k-1>k \quad (\text{since } k\ge 5)$$

$\square$

**Lemma 7** Every infinite simple continued fraction converges to a single real number.

_Proof._ Let $\epsilon>0$. For $m>n\ge\max\{5,\frac1\epsilon\}$, we have:

$$|C_m-C_n|\le|C_m-C_{m-1}|+\cdots+|C_{n+1}-C_n|$$

$$=\frac1{q_mq_{m-1}}+\cdots+\frac1{q_{n+1}q_n} \quad \text{(by Lemma 3)}$$

$$<\frac1{m(m-1)}+\cdots+\frac1{(n+1)n} \quad \text{(by Lemma 6)}$$

$$=\sum_{k=n}^{m-1}\frac{1}{k(k+1)}$$

$$=\sum_{k=n}^{m-1}\left(\frac1k-\frac1{k+1}\right)=\frac1n-\frac1m <\frac1n\le\epsilon$$

Therefore, $\{C_n\}$ is a Cauchy sequence. By the **completeness of real numbers (Cauchy convergence criterion)**, the sequence converges. $\square$

**Lemma 8** For $k\ge 2$, $p_kq_{k-2}-p_{k-2}q_k=(-1)^ka_k$.

_Proof._

$$p_kq_{k-2}-p_{k-2}q_k=(a_kp_{k-1}+p_{k-2})q_{k-2}-p_{k-2}(a_kq_{k-1}+q_{k-2})=a_k(p_{k-1}q_{k-2}-p_{k-2}q_{k-1})$$

Applying Lemma 3 to the remaining expression in the parentheses, we get:

$$p_kq_{k-2}-p_{k-2}q_k=a_{k}(-1)^k$$

$\square$

**Lemma 9** For all $k\ge 0$, $q_k>0$.

_Proof._ Since $q_0=1>0$, and the denominators of a simple continued fraction are monotonically increasing, it naturally follows that $q_k>0$ for all $k\ge 0$. $\square$

**Lemma 10** The odd-indexed convergents of a simple continued fraction are monotonically decreasing.

_Proof._ Let $k\ge 3$ be an odd number. According to Lemma 8:

$$C_k-C_{k-2}=\frac{(-1)^ka_k}{q_kq_{k-2}}=\frac{-a_k}{q_kq_{k-2}}$$

By the definition of a simple continued fraction, $a_k>0$, and by Lemma 9, $q_k, q_{k-2}>0$.

Therefore, $C_k-C_{k-2}<0 \iff C_k<C_{k-2}$. $\square$

**Lemma 11** The even-indexed convergents of a simple continued fraction are monotonically increasing.

_Proof._ Let $k\ge 2$ be an even number. Then:

$$C_k-C_{k-2}=\frac{(-1)^ka_k}{q_kq_{k-2}}=\frac{a_k}{q_kq_{k-2}}$$

By the same reasoning as in Lemma 10, we obtain $C_k-C_{k-2}>0 \iff C_k>C_{k-2}$. $\square$

**Lemma 12** Any even-indexed convergent of a simple continued fraction is strictly less than any odd-indexed convergent.

_Proof._ By Lemma 9, $q_kq_{k-1}>0$. By Lemma 3, $C_k-C_{k-1}=\frac{(-1)^{k+1}}{q_kq_{k-1}}$.

From these two facts, for an even index $k=2s$:

$$C_{2s}<C_{2s-1}$$

For an odd index $k=2t+1$:

$$C_{2t+1}>C_{2t}$$

Now consider an arbitrary even-indexed convergent $C_{2s}$ and an odd-indexed convergent $C_{2t+1}$ ($s,t\ge0$).

- If $2s<2t+1$, then $2s\le 2t$. Thus, by Lemma 11:
    
    $$C_{2s}\le C_{2t}<C_{2t+1}$$
    
- If $2s>2t+1$, then $2s-1\ge 2t+1$. Therefore:
    
    $$C_{2s}<C_{2s-1}\le C_{2t+1}$$
    

In either case, we have $C_{2s}<C_{2t+1}$, which completes the proof. $\square$

**Lemma 13** For all $n\ge 0$, $\left|x-\frac{p_n}{q_n}\right|<\frac1{q_nq_{n+1}}$.

_Proof._ We will show that either $x\in [C_n,C_{n+1}]$ or $x\in [C_{n+1},C_n]$.

- **Odd-indexed Case:** Let $n\ge 1$ be an odd number. Since the limit of a subsequence equals the limit of the sequence itself, $x=\lim_{k\to\infty}C_{2k}$. For all $2k\ge n+1$, based on the monotonic increase of even-indexed convergents (Lemma 11) and the fact that any even-indexed convergent is strictly less than any odd-indexed convergent (Lemma 12), we have:
    
    $$C_{n+1}\le C_{2k}<C_n$$
    
    Taking the limit as $k \to \infty$ gives $x\in [C_{n+1},C_n]$.
    
- **Even-indexed Case:** For all $2k+1\ge n+1$, based on the monotonic decrease of odd-indexed convergents (Lemma 10) and Lemma 12, we can deduce:
    
    $$C_n<C_{2k+1}\le C_{n+1}$$
    
    Taking the limit gives $x\in [C_n,C_{n+1}]$.
    

Since the distance from a point inside an interval to one of its endpoints is strictly less than the total length of the interval itself:

$$\left|x-C_n\right|=\left|x-\frac{p_n}{q_n}\right|<\left|C_{n+1}-C_n\right|=\frac1{q_nq_{n+1}}$$

$\square$

**Theorem 2** Every infinite simple continued fraction converges to an irrational number.

_Proof._ According to Lemma 13:

$$\left|x-\frac{p_n}{q_n}\right|<\frac1{q_nq_{n+1}}$$

Suppose $x$ is rational, say $x = \frac{r}{s}$ for some integers $r$ and $s$ with $s > 0$. Since the continued fraction is infinite, it cannot terminate, meaning $\frac rs\ne\frac{p_n}{q_n}$ for any $n$.

Therefore:

$$0<\left|\frac{r}{s}-\frac{p_n}{q_n}\right|<\frac1{q_nq_{n+1}} \implies 0<\left|rq_n-sp_n\right|<\frac s{q_{n+1}}$$

However, since the denominators of a simple continued fraction are monotonically increasing (Lemma 4) and unbounded, we can choose an $n$ large enough such that $q_{n+1}>s$.

But if we do so, $\left|rq_n-sp_n\right|$ becomes an integer strictly between $0$ and $1$, which is impossible. Thus, no such integers $r$ and $s$ can exist.

Consequently, $x$ must be irrational. $\square$

By Theorem 1,

$$e=[2,1,2,1,1,4,1,1,6,1,1,8,\cdots]$$

By Theorem 2, $e$ is irrational. $\blacksquare$
