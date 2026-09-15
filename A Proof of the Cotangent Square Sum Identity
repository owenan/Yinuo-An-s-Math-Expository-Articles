## **Problem**

Prove that

$$
\sum_{k=1}^{m}\cot^2\frac{k\pi}{2m+1}
=\frac{m(2m-1)}{3}.
$$

### **Theorem 1**

For any integer \(m\geq 0\),

$$
\sin((2m+1)x)
=
\sum_{j=0}^{m}
\binom{2m+1}{2j+1}
(\cos x)^{2m-2j}
(-1)^j
(\sin x)^{2j+1}.
$$

By **De Moivre's theorem**,

$$
(\cos x+i\sin x)^n=\cos nx+i\sin nx.
$$

Taking \(n=2m+1\), we obtain

$$
\cos((2m+1)x)+i\sin((2m+1)x)
=
(\cos x+i\sin x)^{2m+1}.
$$

Expanding the right-hand side using the binomial theorem,

$$
(a+b)^n=\sum_{k=0}^{n}\binom{n}{k}a^{n-k}b^k,
$$

gives

$$
(\cos x+i\sin x)^{2m+1}
=
\sum_{k=0}^{2m+1}
\binom{2m+1}{k}
(\cos x)^{2m+1-k}
(i\sin x)^k.
$$

We now isolate the imaginary part. Since only the odd powers of \(i\) contribute to the imaginary part,

$$
\sin((2m+1)x)
=
\sum_{j=0}^{m}
\binom{2m+1}{2j+1}
(\cos x)^{2m-2j}
(-1)^j
(\sin x)^{2j+1}.
$$

Factoring out \(\sin^{2m+1}x\), we obtain the desired expression. \(\square\)

---

Applying Theorem 1, we have

$$
\begin{aligned}
\sin((2m+1)x)
&=
\sum_{j=0}^{m}
\binom{2m+1}{2j+1}
(\cos x)^{2m-2j}
(-1)^j
(\sin x)^{2j+1}\\
&=
(\sin x)^{2m+1}
\sum_{j=0}^{m}
(-1)^j
\binom{2m+1}{2j+1}
(\cot x)^{2m-2j}.
\end{aligned}
$$

Define

$$
P(x)
=
\sum_{j=0}^{m}
(-1)^j
\binom{2m+1}{2j+1}
x^{m-j}.
$$

Then

$$
\sin((2m+1)x)
=
(\sin x)^{2m+1}P(\cot^2x).
$$

Now let

$$
x=\frac{k\pi}{2m+1},
\qquad 1\leq k\leq m.
$$

Then

$$
\sin((2m+1)x)=\sin(k\pi)=0.
$$

On the other hand,

$$
\sin x
=
\sin\frac{k\pi}{2m+1}\neq0.
$$

Therefore,

$$
P\left(\cot^2\frac{k\pi}{2m+1}\right)=0.
$$

Thus

$$
\cot^2\frac{k\pi}{2m+1},
\qquad k=1,\ldots,m,
$$

are roots of the polynomial \(P(x)\).

By **Vieta's formulas**, the sum of all roots of an \(m\)-th degree polynomial

$$
a_mx^m+a_{m-1}x^{m-1}+\cdots+a_0
$$

is

$$
-\frac{a_{m-1}}{a_m}.
$$

For \(P(x)\), the leading coefficient is

$$
a_m=\binom{2m+1}{1}=2m+1,
$$

while the coefficient of \(x^{m-1}\) is

$$
a_{m-1}
=
-\binom{2m+1}{3}.
$$

Hence,

$$
\begin{aligned}
\sum_{k=1}^{m}
\cot^2\frac{k\pi}{2m+1}
&=
-\frac{-\binom{2m+1}{3}}
{\binom{2m+1}{1}}\\
&=
\frac{(2m+1)(2m)(2m-1)}
{(2m+1)\cdot2\cdot3}\\
&=
\frac{m(2m-1)}{3}.
\end{aligned}
$$

Therefore,

$$
\boxed{
\sum_{k=1}^{m}\cot^2\frac{k\pi}{2m+1}
=
\frac{m(2m-1)}{3}
}.
$$

**This completes the proof.**
 
