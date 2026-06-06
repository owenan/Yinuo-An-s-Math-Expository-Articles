## The Evenly Spaced Integer Topology

Define a topology on the integers $\mathbb{Z}$, called the **evenly spaced integer topology**, by declaring a subset $U \subset \mathbb{Z}$ to be an open set if and only if it is a union of arithmetic sequences $S(a,b)$ for $a \neq 0$, or is empty, where:

$$S(a,b) = \{an+b \mid n \in \mathbb{Z}\} = a\mathbb{Z}+b$$

Equivalently, $U$ is open if and only if for every $x \in U$ there is some non-zero integer $a$ such that $S(a,x) \subset U$.

For clarity, we will refer to these as **Definition 1** and **Definition 2**, respectively.

## Proof of Equivalence

To establish that these definitions are equivalent, we verify both directions of the implication.

### Direction 1: Definition 1 $\implies$ Definition 2

Assume $U$ is open according to Definition 1. This means $U$ is a union of arithmetic sequences:

$$U = \bigcup_{i \in I} S(a_i, b_i)$$

> **Note:** If $U$ is the empty set ($\emptyset$), Definition 2 is satisfied vacuously. Therefore, we assume $U$ is non-empty.

Now, choose any integer $x \in U$. We need to prove that there is some sequence centered at $x$ that fits entirely inside $U$. Since $x$ is in the union $U$, it must belong to at least one specific arithmetic sequence in that union, say $S(a_k, b_k)$.

- **Showing $S(a_k, b_k) \subset S(a_k, x)$:** Let $x, y \in S(a_k, b_k)$. There exist $m, n \in \mathbb{Z}$ such that:
    
    $$a_k m + b_k = x \quad \text{and} \quad a_k n + b_k = y$$
    
    Solving for $b_k$ gives $b_k = x - a_k m$. Substituting this into the expression for $y$:
    
    $$y = a_k n + (x - a_k m) = a_k(n - m) + x$$
    
    This proves that $y \in S(a_k, x)$, hence $S(a_k, b_k) \subset S(a_k, x)$.
    
- **Showing $S(a_k, x) \subset S(a_k, b_k)$:** Now, let $z \in S(a_k, x)$, meaning $z = a_k l + x$ for some integer $l$. Substituting the original expression for $x$:
    
    $$z = a_k l + (a_k m + b_k) = a_k(l + m) + b_k$$
    
    Since $l$ and $m$ are integers, $(l + m)$ is also an integer. Therefore, $z$ must belong to $S(a_k, b_k)$, proving $S(a_k, x) \subset S(a_k, b_k)$.
    

Because both sets contain each other, they are completely identical:

$$S(a_k, b_k) = S(a_k, x)$$

Since $S(a_k, b_k)$ is one of the pieces making up $U$, it is entirely contained within $U$. By choosing $a = a_k$, we have successfully found a non-zero integer $a$ such that $S(a, x) \subset U$.

Thus, any set satisfying Definition 1 satisfies Definition 2.

### Direction 2: Definition 2 $\implies$ Definition 1

Now, assume $U$ is open according to Definition 2. This means that for every $x \in U$, there is some non-zero integer $a_x$ such that $S(a_x, x) \subset U$. We need to show that $U$ can be written as a union of arithmetic sequences.

Let's look at what happens if we take the union of all these individual sequences for every single point $x \in U$:

$$V = \bigcup_{x \in U} S(a_x, x)$$

- **$V \subset U$:** Since every individual sequence $S(a_x, x)$ is guaranteed to be a subset of $U$, combining them all together won't give us anything outside of $U$.
    
- **$U \subset V$:** Conversely, every point $x \in U$ is automatically a member of its own centered sequence $S(a_x, x)$. Because every point of $U$ is inside at least its own sequence, the union must cover all of $U$.
    

Since $V \subset U$ and $U \subset V$, the two sets must be exactly identical:

$$U = \bigcup_{x \in U} S(a_x, x)$$

Because we have expressed $U$ as a union of arithmetic sequences, it perfectly satisfies Definition 1.

## Verification of Topological Axioms

The axioms for a topology are easily verified:

- **Inclusion of $\emptyset$ and $\mathbb{Z}$:** $\emptyset$ is open by definition, and $\mathbb{Z}$ is just the sequence $S(1,0)$, making it open as well.
    
- **Arbitrary Unions:** Any union of open sets is open. For any collection of open sets $\{U_i\}$ and an element $x$ in their union $U$, any of the numbers $a_i$ for which $S(a_i, x) \subset U_i$ also demonstrates that $S(a_i, x) \subset U$.
    
- **Finite Intersections:** The intersection of two (and hence finitely many) open sets is open. Let $U_1$ and $U_2$ be open sets and let $x \in U_1 \cap U_2$ (with non-zero integers $a_1$ and $a_2$ establishing membership). Set $a$ to be the least common multiple ($\text{lcm}$) of $a_1$ and $a_2$. Then:
    
    $$S(a, x) \subset S(a_i, x) \subset U_i \implies S(a, x) \subset U_1 \cap U_2$$
    

## Notable Properties & Furstenberg's Proof of Infinite Primes

This topology has two remarkable properties that can be used to prove the infinitude of prime numbers:

### Property 1: Finite Non-Empty Sets Are Not Open

Since any non-empty open set contains an infinite sequence, a finite non-empty set cannot be open. Put another way, the complement of a finite non-empty set cannot be a closed set.

### Property 2: Basis Sets are Clopen

The basis sets $S(a,b)$ are both open and closed (**clopen**). They are open by definition, and we can write $S(a,b)$ as the complement of an open set as follows:

$$S(a,b) = \mathbb{Z} \setminus \bigcup_{j=1}^{a-1} S(a, b+j)$$

### Furstenberg's Proof

The only integers that are not integer multiples of prime numbers are $-1$ and $+1$. Thus, we can write:

$$\mathbb{Z} \setminus \{-1, +1\} = \bigcup_{p \text{ is prime}} S(p,0)$$

- By **Property 1**, the set on the left-hand side ($\mathbb{Z} \setminus \{-1, +1\}$) cannot be closed because its complement, $\{-1, +1\}$, is a finite non-empty set.
    
- On the other hand, by **Property 2**, each set $S(p,0)$ is closed.
    

If there were only finitely many prime numbers, then the right-hand side would be a **finite union of closed sets**, and hence closed. This creates a contradiction, as a set cannot be simultaneously non-closed and closed.

Therefore, there must be infinitely many prime numbers.
