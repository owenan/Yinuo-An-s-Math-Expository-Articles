## 1. Using the Properties of Derivatives

Consider the function

  

$$f(t)=e^{-it}(\cos t+i\sin t), t\in\mathbb R$$

By the product rule for derivatives $(fg)'=f'g+g'f$, for $t\in\mathbb R$, we uniformly have

  

$$f'(t)=e^{-it}(i\cos t-\sin t)-ie^{-it}(\cos t+i\sin t)=0$$

Therefore, $f$ is a constant.

Moreover, since $f(0)=1$, then $f(t)=1 \forall t\in\mathbb R$. Thus, $e^{it}=\cos t+i\sin t$.

  

## 2. Through Maclaurin Series

$$\sin x=\sum_{n=0}^\infty \frac{(-1)^n}{(2n+1)!}x^{2n+1}=x-\frac{x^3}{3!}+\frac{x^5}{5!}+\cdots$$

$$\cos x=\sum_{n=0}^\infty \frac{(-1)^n}{(2n)!}x^{2n}=1-\frac{x^2}{2!}+\frac{x^4}{4!}+\cdots$$

$$e^z=\sum_{n=0}^\infty \frac{z^n}{n!}=1+z+\frac{z^2}{2!}+\frac{z^3}{3!}+\cdots$$

Substituting $z=ix$ into the last series:

  

$$e^{ix}=\sum_{n=0}^\infty\frac{(ix)^n}{n!}=1+ix+\frac{(ix)^2}{2!}+\frac{(ix)^3}{3!}+\cdots$$

$$=1+ix-\frac{x^2}{2!}-i\frac{x^3}{3!}+\frac{x^4}{4!}+i\frac{x^5}{5!}\cdots$$

$$=(1-\frac{x^2}{2!}+\frac{x^4}{4!}+\cdots)+i(x-\frac{x^3}{3!}+\frac{x^5}{5!}-\cdots)$$

$$=\cos x+i\sin x$$

## 3. Through Basic Complex Analysis (First Proposed by Bernoulli)

Through algebra, we have:

  

$$\frac{2i}{x^2+1}=\frac1{x-i}-\frac1{x+i}$$

Now, integrating both sides:

  

$$2i\arctan x+c=\log\frac{x-i}{x+i}$$

Substituting $x=\tan(y/2)$ and exponentiating both sides with base $e$: ($C=e^c$)

  

$$Ce^{iy}=\frac{\sin(y/2)-i\cos(y/2)}{\sin(y/2)+i\cos (y/2)}$$

$$=\frac{(\sin(y/2)-i\cos(y/2))^2}{\sin(y/2)^2+\cos(y/2)^2}$$

$$=(\sin (y/2)-i\cos(y/2))^2=-\cos y-i\sin y$$

$$\implies Ce^{iy}=-\cos y-i\sin y$$

Substituting $y=0 \implies C=-1$

  

Therefore,

  

$$e^{iy}=\cos y+i\sin y$$

## 4. Based on the Limit Definition of the Exponential Function

$$e^x=\lim_{n\to\infty}(1+\frac {x}n)^n$$

Thus,

  

$$e^{ix}=\lim_{n\to\infty}(1+\frac{ix}{n})^n$$

Using the polar form of complex numbers:

  

$$1+\frac{ix}{n}=\sqrt{1+\frac{x^2}{n^2}}(\cos(\arctan (\frac xn))+i\sin(\arctan(\frac xn)))$$

By De Moivre's Theorem:

  

$$(1+\frac{ix}n)^n=({1+\frac{x^2}{n^2}})^{\frac n2}(\cos(n\arctan(\frac xn))+i\sin(n\arctan(\frac xn)))$$

And,

  

$$\lim_{n\to\infty}(1+\frac{x^2}{n^2})^{\frac n2}=\lim_{n\to\infty}((1+\frac{x^2}{n^2})^{n^2})^{\frac1{2n}}=\lim_{n\to\infty}(e^{x^2})^{\frac 1{2n}}=\lim_{n\to\infty}e^{\frac{x^2}{2n}}=e^0=1$$

Let $h=x/n$, then

  

$$n\arctan (x/n)=x(\arctan h)/h=x\frac{\arctan h-\arctan0}{h}$$

$$\lim_{n\to\infty} n\arctan(x/n)=\lim_{h\to 0}x\frac{\arctan h-\arctan 0}{h}=x\arctan'(0)=x$$

Therefore,

  

$$e^{ix}=\lim_{n\to\infty}(1+\frac{ix}{n})^n=\cos x+i\sin x$$

I hope everyone enjoyed this sharing. For more knowledge sharing in mathematics and physics, please follow our official account, Science Frontier.