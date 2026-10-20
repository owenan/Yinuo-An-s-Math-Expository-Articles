**Theorem (Borel-Lebesgue):** A family of open intervals covering a closed interval contains a finite subfamily that covers the closed interval.

  

**Proof:** Let $S=\{U\}$ be a family of open intervals covering the closed interval $[a,b]=I_1$. If the interval $I_1$ cannot be covered by a finite number of elements (intervals) from $S$, then by bisecting $I_1$ into two intervals, we will find that at least one interval cannot be covered by a finite subfamily of $S$; we denote one such interval as $I_2$$^{[1]}$. We then repeat this procedure of bisecting the set into two on $I_2$, and so on.

  

Thus, we obtain a nested sequence of closed intervals, where none of the closed intervals can be covered by a finite subfamily of $S$. Since the length of interval $I_n$ is $\vert{}I_n\vert{}=2^{-n}\vert{}I_1\vert{}$, the sequence of intervals $\{I_n\}$ contains intervals of arbitrarily small length$^{[2]}$.

  

Applying the Nested Interval Theorem, we find there exists a point $c$ belonging to all $I_n$, $n\in\mathbb{N}$. Since $c\in I_1=[a,b]$, there exists $c\in(\alpha,\beta)=U\in S$$^{[3]}$, which means $\alpha<c<\beta$. Let $\epsilon=\min\{c-\alpha,\beta-c\}$. Thus, in the sequence of intervals we just constructed, there exists $\vert{}I_n\vert{}<\epsilon$$^{[4]}$. Since $c\in I_n$ and $\vert{}I_n\vert{}<\epsilon$, it follows that $I_n\subset U=(\alpha,\beta)$$^{[5]}$.

  

However, this contradicts the fact that $I_n$ cannot be covered by a finite subfamily of the interval family$^{[6]}$. The theorem is thus proved.

  

[1]: The reason here is that if both intervals could be covered by a finite subfamily, then the original interval could also be covered by a finite subfamily. Because the definition of "finite" implies the quantity is a natural number, and a natural number plus a natural number is obviously a natural number.

  

[2]: Here "(arbitrarily small)" means $\forall \epsilon>0$, $\exists \vert{}I_n\vert{}<\epsilon$.

  

[3]: Because $I_1\subset\bigcup_{U\in S}\{U\}$, according to the definition of a union, there exists $U\in S$ such that $I_1\subset U$.

  

[4]: We have already established that the intervals are arbitrarily small.

  

[5]: Because $c\in I_n$ and $\vert{}I_n\vert{}<\min\{c-\alpha,\beta-c\}$, therefore $c+\vert{}I_n\vert{}<c+\min\{c-\alpha,\beta-c\}\le c+(\beta-c)=\beta$ and $c-\vert{}I_n\vert{}>c-\min\{c-\alpha,\beta-c\}\ge c-(c-\alpha)=\alpha$. With $I_n=(a_n,b_n)$, clearly $b_n<c+\vert{}I_n\vert{}<\beta$ and $a_n>c-\vert{}I_n\vert{}>\alpha$, hence $I_n\subset U$.

  

[6]: By proof by contradiction.