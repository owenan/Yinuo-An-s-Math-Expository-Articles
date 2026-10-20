Hello everyone, today we bring you a challenging problem from the _American Mathematical Monthly_ relating to integrals and infinite sums.

  

# Problem Statement:

### An infinite sum involving central binomial coefficients

Prove that,

  

$$\sum_{n=1}^\infty\frac{\binom{2n}{n}\binom{4n}{2n}}{64^n(2n-1)}=1-\frac 1\pi(\sqrt{2}+\ln(1+\sqrt{2}))$$

.

  

We now begin the proof.

  

## Proof:

### Lemma 1:

For $-1\le x\le 1$,

  

$$\sqrt{1-x}=\sum_{n=0}^\infty\binom{\frac 12}{n}(-x)^n=1-\sum_{n=1}^\infty\frac{\binom{2n}{n}}{4n}\frac{x^n}{2n-1}$$

We will attempt to prove both equalities.

  

### Proof:

**First Equality**

  

The Binomial Theorem tells us that for any complex exponent $r$:

  

$$(x+y)^r =\sum_{k=0}^\infty {r \choose k} x^{r-k} y^k$$

Applying this to the first expression (out of three), namely $(1+(-x))^{\frac 12}$, we obtain:

  

$$\sqrt{1 - x} = (1 - x)^{1/2} = \sum_{n=0}^\infty \binom{1/2}{n} (-x)^n.$$

This establishes the first equality.

  

**Second Equality**

  

First, we calculate $\binom{1/2}{n}$:

  

$$\binom{1/2}{n} = \frac{\frac{1}{2} \left(\frac{1}{2} - 1\right) \left(\frac{1}{2} - 2\right) \cdots \left(\frac{1}{2} - (n - 1)\right)}{n!}.$$

Simplifying the product in the numerator:

  

$$\frac{1}{2} \left(-\frac{1}{2}\right) \left(-\frac{3}{2}\right) \cdots \left(-\frac{2n - 3}{2}\right) = (-1)^{n-1} \frac{1 \cdot 3 \cdot 5 \cdots (2n - 3)}{2^n}.$$

Substituting this back, we get:

  

$$\binom{1/2}{n} = (-1)^{n-1} \frac{1 \cdot 3 \cdot 5 \cdots (2n - 3)}{2^n n!}.$$

Now, expressing the product $1 \cdot 3 \cdot 5 \cdots (2n - 3)$ using factorials:

  

$$1 \cdot 3 \cdot 5 \cdots (2n - 3) = \frac{(2n - 2)!}{2^{n-1} (n - 1)!}.$$

Substituting this back:

  

$$\binom{1/2}{n} = (-1)^{n-1} \frac{(2n - 2)!}{2^{2n - 1} n! (n - 1)!}.$$

Note that $\binom{2n}{n} = \frac{(2n)!}{n! n!}$ is a central binomial coefficient, so we obtain:

  

$$\binom{1/2}{n} = (-1)^{n-1} \frac{\binom{2n}{n}}{4^n (2n - 1)}.$$

Therefore,

  

$$\binom{1/2}{n} (-x)^n = (-1)^{n-1} \frac{\binom{2n}{n}}{4^n (2n - 1)} (-x)^n =-\frac{\binom{2n}{n}}{4^n (2n - 1)} x^n.$$

Summing over $n$ from 1 to $\infty$:

  

$$\sum_{n=1}^\infty \binom{1/2}{n} (-x)^n = -\sum_{n=1}^\infty \frac{\binom{2n}{n}}{4^n (2n - 1)} x^n.$$

Since $\binom{1/2}{0} (-x)^0 = 1$, we have:

  

$$\sqrt{1 - x} = 1 - \sum_{n=1}^\infty \frac{\binom{2n}{n}}{4^n (2n - 1)} x^n.$$

This establishes the second equality. $\square$

  

### Lemma 2:

$$\int_{0}^{\frac \pi 2} \sin^{4n}tdt=\frac{\pi}{2}\frac{(4n-1)!!}{(4n)!!}=\frac{\pi}{2}\frac{\binom{4n}{2n}}{16^n}$$

Any integral of the form

  

$$W_n=\int_0^\frac{\pi}{2}\sin^nx\:dx=\int_0^{\frac\pi 2}\cos^n x,n\ge 2$$

is a Wallis integral. We will prove a stronger version of Lemma 2:

  

$$W_{2p}=\frac{2p-1}{2p} \cdot \frac{2p-3}{2p-2} \cdots \frac{1}{2} W_0 = \frac{(2p-1)!!}{(2p)!!} \cdot \frac{\pi}{2} = \frac{(2p)!}{2^{2p} (p!)^2} \cdot \frac{\pi}{2},$$

$$W_{2p+1}=\frac{2p}{2p+1} \cdot \frac{2p-2}{2p-1} \cdots \frac{2}{3} W_1 = \frac{(2p)!!}{(2p+1)!!} = \frac{2^{2p}(p!)^2}{(2p+1)!},$$

and

  

$$\int_0^{\frac\pi2}\sin^nx\:dx=\int_0^{\frac\pi 2}\cos^n x$$

### Proof:

We first prove that the cosine and sine expressions are equivalent.

  

$$\int_0^{\frac\pi2}\sin^nx\,dx=\int_{\frac\pi2}^{0}\sin^n(\frac\pi2-t)\,d(\frac\pi2-t)=\int_0^{\frac\pi2}\cos^nxdx$$

Next, we apply integration by parts to $W_n$:

  

$$\int_0^\frac\pi 2\sin^n x\:dx=\int_0^\frac\pi 2(\sin^{n-2})(1-\cos^2 x)\:dx=\int_0^\frac\pi 2\sin^{n-2}x\:dx-\int_0^\frac{\pi}{2}\sin^{n-2}x\cos^2x\:dx \quad (1)$$

We apply integration by parts again to the integral on the right side of the resulting equation:

  

Let:

$v'(x)=\cos x\sin^{n-2}x$, with antiderivative $v(x)=\frac 1{n-1}\sin^{n-1}x$,

$u(x)=\cos(x)$, with derivative $u'(x)=-\sin(x)$

  

Thus, we have:

  

$$\int_0^{\frac{\pi}{2}} \sin^{n-2} x \cos^2 x \,dx = \left[ \frac{\sin^{n-1} x}{n-1} \cos x \right]_0^{\frac{\pi}{2}} + \frac{1}{n-1}\int_0^{\frac{\pi}{2}} \sin^{n-1} x \sin x \,dx = 0 + \frac{1}{n-1} W_n.$$

Substituting this back into equation (1) above, we obtain:

  

$$W_n=W_{n-2}-\frac 1{n-1}W_n$$

Therefore, for any $n\ge 2$ we have:

  

$$W_n=\frac{n-1}{n}W_{n-2}$$

.

  

Since

  

$$W_0=\int_0^\frac\pi21\:dx=\frac\pi 2,\quad W_1=\int_0^\frac\pi 2\sin x\:dx=1$$

we have

  

$$W_{2p}=\frac{2p-1}{2p} \cdot \frac{2p-3}{2p-2} \cdots \frac{1}{2} W_0 = \frac{(2p-1)!!}{(2p)!!} \cdot \frac{\pi}{2} = \frac{(2p)!}{2^{2p} (p!)^2} \cdot \frac{\pi}{2},$$

$$W_{2p+1}=\frac{2p}{2p+1} \cdot \frac{2p-2}{2p-1} \cdots \frac{2}{3} W_1 = \frac{(2p)!!}{(2p+1)!!} = \frac{2^{2p}(p!)^2}{(2p+1)!}.$$

### Main Proof:

By applying Lemma 1 and Lemma 2, and interchanging the order of summation and integration, we proceed with the following steps:

  

$$I=\sum_{n=1}^\infty\frac{{4n\choose 2n}{2n\choose n}}{64^n(2n-1)}=\sum_{n=1}^\infty \frac{2n\choose n}{4^n(2n-1)}\cdot\frac 2\pi\int_0^{\pi/2}\sin^{4n}t\:dt$$

(Using Lemma 2)

  

$$I=\frac 2\pi\int_0^{\pi/2}\sum_{n=1}^\infty\frac{2n\choose n}{4^n(2n-1)}(\sin^4 t)^n\:dt$$

(Extracting coefficients, interchanging the order of integration and summation)

  

$$I=\frac 2\pi\int_0^{\pi/2}(1-\sqrt{1-\sin^4t})\:dt$$

(Using Lemma 1)

  

$$I=1-\frac\pi 2\int_0^{\frac \pi2}\sqrt{1+\sin^2t}\cos t\:dt$$

(Using the additivity of integrals, $\sin^2t+\cos^2t=1$, and $\sqrt{ab}=\sqrt a\sqrt b$)

  

Now we use substitution. Let $x=\sin t$, yielding:

  

$$\sum_{n=1}^\infty\frac{{4n\choose 2n}{2n\choose n}}{64^n(2n-1)}=1-\frac 2\pi\int_0^1\sqrt{1+x^2}\:dx$$

We evaluate $\int\sqrt{1+x^2}\:dx$:

  

Using the substitution let $x=\tan \theta$

$dx=\sec^2\theta d\theta$

  

That is, $I_0=\int\sqrt{1+x^2}dx=\int \sqrt{1+\tan^2 \theta} \cdot \sec^2 \theta \, d\theta$

  

Applying $1+\tan^2\theta=\sec^2\theta$,

  

We have:

$I_0=\int\sec^3\theta d\theta$

  

Applying integration by parts $\int u\,dv=uv-\int v\,du$ to this integral:

  

$$u = \sec \theta, \quad dv = \sec^2 \theta \, d\theta$$

Thus $du=\tan\theta\sec\theta d\theta, \quad v=\tan\theta$

  

Applying integration by parts, we have:

  

$$I_0=\int \sec^3 \theta \, d\theta = \sec \theta \tan \theta - \int \sec \theta \tan^2 \theta \, d\theta$$

Substituting the identity $\tan^2 \theta = \sec^2 \theta - 1$:

  

$$I_0 = \sec \theta \tan \theta - \int \sec \theta (\sec^2 \theta - 1) \, d\theta$$

$$I_0= \sec \theta \tan \theta + \int \sec \theta \, d\theta$$

(Expanding and rearranging)

  

$$\int \sec^3 \theta \, d\theta = \frac{1}{2} \sec \theta \tan \theta + \frac{1}{2} \int \sec \theta \, d\theta$$

(Simplifying and dividing both sides by 2)

  

Next, let $I_1=\int\sec\theta \:d\theta$.

  

$$I_1=\int \sec \theta \, d\theta = \int \sec \theta \cdot \frac{\sec \theta + \tan \theta}{\sec \theta + \tan \theta} \, d\theta$$

$$I_1 = \int \frac{\sec^2 \theta + \sec \theta \tan \theta}{\sec \theta + \tan \theta} \, d\theta$$

(Expanding)

  

Let $u=\sec\theta+\tan\theta$, then:

  

$$du = (\sec \theta \tan \theta + \sec^2 \theta) \, d\theta$$

(Differentiating and simplifying)

  

Applying

  

$$\int \frac{du}{u} = \ln\vert{}u\vert{} + C$$

Thus

  

$$\int \sec \theta \, d\theta = \ln\vert{}\sec \theta + \tan \theta\vert{} + C$$

Substituting into $I_0$, we have:

  

$$\int \sec^3 \theta \, d\theta = \frac{1}{2} \sec \theta \tan \theta + \frac{1}{2} \ln\vert{}\sec \theta + \tan \theta\vert{} + C$$

Substituting $x = \tan \theta$ and $\sec \theta = \sqrt{1+x^2}$:

  

$$\int \sqrt{1+x^2} \, dx = \frac{1}{2} \left( x\sqrt{1+x^2} + \ln\vert{}x + \sqrt{1+x^2}\vert{} \right) + C$$

Substituting this back into

  

$$\sum_{n=1}^\infty\frac{\binom{4n}{2n}\binom{2n}{n}}{64^n(2n-1)}=1-\frac 2\pi\int_0^1\sqrt{1+x^2}\:dx$$

we get:

  

$$=1-\frac{1}{\pi}\left(x\sqrt{1+x^2}+\ln(x+\sqrt{1+x^2})\right)\bigg\vert{}_0^1$$

$$=1-\frac{1}{\pi}\left(\sqrt{2}+\ln(1+\sqrt{2})\right).$$

The proof is complete. $\blacksquare$

  

Reference: [https://doi.org/10.1080/00029890.2024.2425218](https://doi.org/10.1080/00029890.2024.2425218)