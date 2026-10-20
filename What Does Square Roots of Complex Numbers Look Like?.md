Complex numbers are defined as numbers of the form $a+ib$, where $i=\sqrt{-1}$, and $a, b$ are real numbers. We use the symbols $\mathbb{R}$ and $\mathbb{C}$ to represent the set of all real numbers and the set of all complex numbers, respectively.

  

Suppose we have a complex number, $\alpha+i\beta$. If we want to find its square root, we are essentially looking for a complex number $x+iy$ that satisfies $(x+iy)^2=\alpha+i\beta$.

  

Expanding the left side, we get $(x^2-y^2)+2xyi=\alpha+\beta i$ (Equation 1).

  

For this equality to hold, the real and imaginary parts of the complex numbers must be respectively equal. The real part is the real number component of the complex number, and the imaginary part is the real number in the imaginary component.

  

Therefore, we can obtain $x^2-y^2=\alpha$ (Equation 2) and $2xy=\beta$ (Equation 3).

  

Then, according to algebraic expansion, $(x^2+y^2)^2$ is equal to $(x^2-y^2)^2+4x^2y^2$.

  

By matching this with our previous results, we get $\alpha^2+\beta^2$.

  

Thus, we must have $x^2+y^2=\sqrt{\alpha^2+\beta^2}$ (Equation 4), where the square root here is the principal square root, meaning its result is a non-negative number.

  

By combining Equations 2, 3, and 4, we can derive Equation 6:

  

$$\begin{align} x^2&=\frac{1}{2}(\alpha+\sqrt{\alpha^2+\beta^2})\\ y^2&=\frac{1}{2}(-\alpha+\sqrt{\alpha^2+\beta^2}) \end{align}$$

Since $x^2$ being equal to any number yields two opposite roots, and $x+iy=\sqrt{\alpha+i\beta}$, we have:

  

$$x=\pm\sqrt{\frac{1}{2}(\alpha+\sqrt{\alpha^2+\beta^2})}$$

$$y=\pm\sqrt{\frac{1}{2}(-\alpha+\sqrt{\alpha^2+\beta^2})}$$

_(Note: Corrected a missing negative sign and a stray bracket from the original text's $y$ equation for mathematical accuracy.)_

  

However, because Equations 2 and 3 can imply Equation 4, but Equation 4 does not necessarily imply Equations 2 and 3, we cannot arbitrarily combine these values of $x$ and $y$. We must ensure that the sign of $\beta$ is the same as the sign of $2xy$.

  

Because when $\beta<0$, $\frac{\beta}{\vert{}\beta\vert{}}=-1$, and when $\beta\ge 0$, $\frac{\beta}{\vert{}\beta\vert{}}=1$. Therefore, we can use this to represent the sign of the $\beta$ value.

  

Thus, we have:

  

$$\sqrt{\alpha+i\beta}=\pm\left(\sqrt{\frac{\alpha+\sqrt{\alpha^2+\beta^2}}{2}}+i\frac{\beta}{\vert{}\beta\vert{}}\sqrt{\frac{-\alpha+\sqrt{\alpha^2+\beta^2}}{2}}\right)$$

The condition for this is $\beta\ne 0$.

  

When $\beta=0$, $\sqrt{\alpha+i\beta}=\pm \sqrt{\alpha}$ if $\alpha\ge 0$, and $\pm i\sqrt{-\alpha}$ if $\alpha<0$.

  

And there we go, we have found the square root of a complex number.

  

If you enjoy my content, please follow.