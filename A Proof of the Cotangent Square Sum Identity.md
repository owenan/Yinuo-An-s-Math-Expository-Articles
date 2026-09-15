# A Trigonometric Identity Involving Cotangent Squares

## Problem

Prove that, for every integer $m \geq 1$,

$$
\sum_{k=1}^{m}\cot^2\frac{k\pi}{2m+1}
=
\frac{m(2m-1)}{3}.
$$

## Proof

We begin with the following consequence of De Moivre's theorem.

### Lemma

For every integer $m \geq 0$,

$$
\sin((2m+1)x)
=
\sum_{j=0}^{m}
(-1)^j
\binom{2m+1}{2j+1}
\cos^{2m-2j}x\,
\sin^{2j+1}x.
$$

### Proof of the Lemma

By De Moivre's theorem,

$$
(\cos x+i\sin x)^{2m+1}
=
\cos((2m+1)x)+i\sin((2m+1)x).
$$

Expanding the left-hand side using the binomial theorem gives

$$
(\cos x+i\sin x)^{2m+1}
=
\sum_{k=0}^{2m+1}
\binom{2m+1}{k}
\cos^{2m+1-k}x\,
(i\sin x)^k.
$$

Only odd powers of $i$ contribute to the imaginary part. Writing $k=2j+1$, we obtain

$$
\sin((2m+1)x)
=
\sum_{j=0}^{m}
\binom{2m+1}{2j+1}
\cos^{2m-2j}x\,
i^{2j+1}\sin^{2j+1}x.
$$

Since

$$
i^{2j+1}=i(-1)^j,
$$

taking imaginary parts yields

$$
\boxed{
\sin((2m+1)x)
=
\sum_{j=0}^{m}
(-1)^j
\binom{2m+1}{2j+1}
\cos^{2m-2j}x\,
\sin^{2j+1}x
}.
$$

---

## Constructing the Polynomial

Factor out $\sin^{2m+1}x$:

$$
\begin{aligned}
\sin((2m+1)x)
&=
\sin^{2m+1}x
\sum_{j=0}^{m}
(-1)^j
\binom{2m+1}{2j+1}
\frac{\cos^{2m-2j}x}{\sin^{2m-2j}x}
\\
&=
\sin^{2m+1}x
\sum_{j=0}^{m}
(-1)^j
\binom{2m+1}{2j+1}
\cot^{2m-2j}x.
\end{aligned}
$$

Define the polynomial

$$
P(t)
=
\sum_{j=0}^{m}
(-1)^j
\binom{2m+1}{2j+1}
t^{m-j}.
$$

Then

$$
\boxed{
\sin((2m+1)x)
=
\sin^{2m+1}x\,P(\cot^2x)
}.
$$

## Finding the Roots

Let

$$
x=\frac{k\pi}{2m+1},
\qquad
1\leq k\leq m.
$$

Then

$$
\sin((2m+1)x)
=
\sin(k\pi)
=
0.
$$

Moreover,

$$
0<
\frac{k\pi}{2m+1}
<
\frac{\pi}{2},
$$

so

$$
\sin\frac{k\pi}{2m+1}\neq0.
$$

Therefore,

$$
P\left(
\cot^2\frac{k\pi}{2m+1}
\right)
=
0.
$$

Thus the $m$ numbers

$$
\cot^2\frac{\pi}{2m+1},
\cot^2\frac{2\pi}{2m+1},
\ldots,
\cot^2\frac{m\pi}{2m+1}
$$

are roots of $P(t)$.

Since $P$ has degree $m$, these are precisely all of its roots.

## Applying Vieta's Formula

Expanding $P(t)$, the leading term comes from $j=0$:

$$
a_m
=
\binom{2m+1}{1}
=
2m+1.
$$

The coefficient of $t^{m-1}$ comes from $j=1$:

$$
a_{m-1}
=
-\binom{2m+1}{3}.
$$

By Vieta's formula, the sum of the roots is

$$
-\frac{a_{m-1}}{a_m}.
$$

Hence,

$$
\begin{aligned}
\sum_{k=1}^{m}
\cot^2\frac{k\pi}{2m+1}
&=
-\frac{-\binom{2m+1}{3}}
{\binom{2m+1}{1}}
\\[4pt]
&=
\frac{(2m+1)(2m)(2m-1)}
{(2m+1)\cdot2\cdot3}
\\[4pt]
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

Hence the identity is proved. $\square$
