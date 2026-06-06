Define a topology on the integers $\mathbb Z$, called the evenly spaced integer topology, by declaring a subset $U\subset \mathbb Z$ to be an open set if and only if it is a union of arithmetic sequences $S(a,b)$ for $a\ne 0$, or is empty, where
$$S(a,b)=\{an+b|n\in\mathbb Z\}=a\mathbb Z+b$$
Equivalently, $U$ is open if and only if for every $x$ in $U$ there is some non-zero integer $a$ such that $S(a,x)\subset U$. 
We call the definitions definition 1 and definition 2 by order. We now verify the equivalence:

Definition 1 $\implies$ Definition 2
Assume $U$ is open according to **Definition 1**. This means $U$ is a union of arithmetic sequences: $$U=\bigcup_{i\in I}S(a_i,b_i)$$
(Note: If $U$ is the empty set, Definition 2 is satisfied vacuously, so we assume $U$ is non-empty)
Now, we choose any integer $x\in U$. We need to prove that there is some sequence centered at $x$ that fits entirely inside $U$.
1. Since $x$ is in the union $U$, it must belong to at least one specific arithmetic sequence in that union, let's call it $S(a_k,b_k)$.
2. Let $x,y\in S(a_k,b_k)$,  there exists $n,m\in\mathbb Z$ that $a_km+b_k=x, a_kn +b_k=y$. Therefore we have $b_k=x-a_km$, substituting this to $y$, we have $y=a_k(n-m)+x$, this proves $S(a_k,b_k)\subset S(a_k,x)$ . Now let $z\in S(a_k,x)$. Substituting the original expression for $x$, we get: $z=a_kk+(a_km+b_k)$. Factor out the $a$:$z=a_k(k+m)+b_k$. Since $k$ and $m$ are integers, $(k+m)$ is also an integer. Therefore, $z$ must belong to $S(a,b)$. This proves that $S(a,x)\subset S(a,b)$. Because both of the sets contain each other, they are completely identical:$S(a,b)=S(a,x)$. 
3. Since $S(a_k,b_k)$ is one of the pieces making up $U$, it is completely contained within $U$: 
4. By choosing $a=a_k$, we have successfully found a non-zero integer $a$ such that $S(a,x)\subset U$
Thus, any set satisfying Definition 1 satisfies Definition 2.

Definition 2$\implies$ Definition 1
Now, assume $U$ is open according to Definition 2. This means that for every $x\in U$, there is some non-zero integer $a_x$ such that $S(a_x,x)\subset U$. We need to show that $U$ can be written as a union of arithmetic sequences. 
Let's look at what happens if we take the union of all these individual sequences for every single point $x$ in $U$:
$$V=\bigcup_{x\in U} S(a_x, x)$$
1. Since every individual sequence $S(a_x,x)$ is guaranteed to be a subset of $U$, combining them all together won't give us anything outside of $U$. Therefore: $$V\subset U$$
2. Conversely, every point $x\in U$ is automatically a member of its own centered sequence $S(a_x, x)$. Because every point of $U$ is inside at least its own sequence, the union must cover all of $U$:
   $$U\subset V$$
3. Since $V\subset U$ and $U\subset V$, the two sets must be exactly identical:
   $$U=\bigcup_{x\in U}S(a_x,x)$$
Because we have expressed $U$ as a union of arithmetic sequences, it perfectly satisfies Definition 1.

The axioms for a topology are easily verified:
$\emptyset$ is open by definition, and $\mathbb Z$ is just the sequence $S(1,0)$, and so is open as well.

Any union of open sets is open: for any collection of open sets $U_i$ and $x$ in their union $U$, any of the numbers $a_i$ for which $S(a_i,x)\subset U_i$ also shows that $S(a_i,x)\subset U$.

The intersection of two (and hence finitely many) open sets is open: let $U_1$ and $U_2$ be open sets and let $x\in U_1\cap U_2$(with numbers $a_1$ and $a_2$ establishing membership). Set $a$ to be the least common multiple of $a_1$ and $a_2$. Then $S(a,x)\subset S(a_i,x)\subset U_i$.

This topology has two notable properties:

1. Since any non-empty open set contains an infinite sequence, a finite non-empty set cannot be open; put another way, the complement of a finite non-empty set cannot be a closed set.

2. The basis sets $S(a,b)$ are both open and closed: they are open by definition, and we can write $S(a,b)$ as the complement of an open set as follows:

$$
S(a,b)
=
\mathbb{Z}
\setminus
\bigcup_{j=1}^{a-1}
S(a,b+j).
$$

The only integers that are not integer multiples of prime numbers are $-1$ and $+1$, i.e.

$$
\mathbb{Z}\setminus\{-1,+1\}
=
\bigcup_{p\ \text{prime}} S(p,0).
$$

Now, by the first topological property, the set on the left-hand side cannot be closed.

On the other hand, by the second topological property, the sets $S(p,0)$ are closed. So, if there were only finitely many prime numbers, then the set on the right-hand side would be a finite union of closed sets, and hence closed. This would be a contradiction, so there must be infinitely many prime numbers.
