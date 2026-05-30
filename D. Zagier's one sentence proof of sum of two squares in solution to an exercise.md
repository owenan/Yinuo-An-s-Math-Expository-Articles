Exercise(D. Zagier)

Let $p$ be a prime number such that $p \equiv 1 \pmod 4$. Show that there exist $x, y \in \mathbb{Z}$ such that $x^2 + y^2 = p$ using the following argument. Define the finite set:

$$S := \{(x, y, z) \in \mathbb{Z}_{\geq 1} : x^2 + 4yz = p\}.$$

### (i)

Consider the map $f : S \to S$ defined as follows:

$$f(x, y, z) = \begin{cases} (x + 2z, z, y - x - z), & \text{if } x < y - z, \\ (2y - x, y, x - y + z), & \text{if } y - z < x < 2y, \\ (x - 2y, x - y + z, y), & \text{if } x > 2y. \end{cases}$$

Verify that this definition is well-defined, and that $f(f(x, y, z)) = (x, y, z)$ for all $(x, y, z) \in S$.

### (ii)

Show that $f : S \to S$ has a unique fixed point $(x, y, z)$—that is, a point satisfying $f(x, y, z) = (x, y, z)$. Consequently, show that the cardinality of $S$ is odd.

### (iii)

Define the map $g : S \to S$ by $g(x, y, z) = (x, z, y)$. Show that $g$ has a fixed point. Use this to show that $x^2 + y^2 = p$ has an integer solution.

## Solution

### Part 1) Well-definedness and Involution Property of $f$

- **Case 1:** If $x < y - z$, then $f(x,y,z) = (x + 2z, z, y - x - z) = (x_1, y_1, z_1)$.
    
    Here, $x_1 > 2y_1 \iff x + 2z > 2z \iff x > 0$, which holds since $x \in \mathbb{Z}_{\geq 1}$.
    
    Applying $f$ again gives the third case of the definition:
    
    $$f(f(x,y,z)) = (x_1 - 2y_1, x_1 - y_1 + z_1, y_1) = (x, y, z)$$
    
- **Case 2:** If $y - z < x < 2y$, then $f(x,y,z) = (2y - x, y, x - y + z) = (x_1, y_1, z_1)$.
    
    Here, $x_1 < 2y_1 \iff 2y - x < 2y \iff x > 0$, which holds.
    
    Additionally, $x_1 > y_1 - z_1 \iff 2y - x > y - (x - y + z) \iff 2y - x > 2y - x - z \iff z > 0$, which holds.
    
    Applying $f$ again gives the second case:
    
    $$f(f(x,y,z)) = (2y_1 - x_1, y_1, x_1 - y_1 + z_1) = (x, y, z)$$
    
- **Case 3:** If $x > 2y$, then $f(x,y,z) = (x - 2y, x - y + z, y) = (x_1, y_1, z_1)$.
    
    Clearly, $x_1 < y_1 - z_1 \iff x - 2y < (x - y + z) - y \iff x - 2y < x - 2y + z \iff z > 0$, which holds.
    
    Applying $f$ again gives the first case:
    
    $$f(f(x,y,z)) = (x_1 + 2z_1, z_1, y_1 - x_1 - z_1) = (x, y, z)$$
    

Therefore, for all $(x,y,z) \in S$, we have $f(f(x,y,z)) = (x,y,z)$.

### Part 2) Fixed Points of $f$ and Parity of $|S|$

- For the **first case**, $f(x,y,z) = (x,y,z) \iff (x,y,z) = (0,0,0)$. This contradicts $x^2 + 4yz = 0 \neq p$.
    
- For the **third case**, $f(x,y,z) = (x,y,z) \iff (x,y,z) = (0,0,0)$, which yields the same contradiction.
    
- For the **second case**, $f(x,y,z) = (x,y,z) \iff x = 2y - x \implies x = y$, and $z = x - y + z \implies x = y$. Thus, it requires $x = y$.
    
    Substituting this into the definition of $S$ gives:
    
    $$p = x^2 + 4yz = y^2 + 4yz = y(y + 4z)$$
    
    Since $p$ is a prime number and $y, z \geq 1$, we must have $y = 1$. This implies $z = 1$, which further yields $x = \frac{p-1}{4}$. Thus, there is a unique fixed point:
    
    $$(x, y, z) = \left(\frac{p-1}{4}, 1, 1\right)$$
    

> **Lemma:** The number of fixed points of an involution has the same parity as the total number of elements in the set.

**Proof of Lemma:**

Define an equivalence relation $\sim$ on a set $A$ equipped with an involution $f$ such that for all $a, b \in A$:

$$a \sim b \iff b = a \text{ or } b = f(a)$$

We verify the properties of an equivalence relation:

- **Reflexivity:** $a \sim a$ holds trivially since $a = a$.
    
- **Transitivity:** $a \sim b \wedge b \sim c \iff (b = a \vee b = f(a)) \wedge (c = b \vee c = f(b))$.
    
    Verifying the four possible cases:
    
    1. $b = a \wedge c = b \implies a = c \implies c \sim a$
        
    2. $b = a \wedge c = f(b) \implies c = f(a) \implies a \sim c$
        
    3. $b = f(a) \wedge c = b \implies c = f(a) \implies a \sim c$
        
    4. $b = f(a) \wedge c = f(b) \implies c = f(f(a)) = a \implies a \sim c$
        

Let $A'$ be the set of all fixed points. Let $C_a$ be the equivalence class of $a$, $C = \{C_a : a \in A\}$, and $C' = \{C_a : a \in A'\}$.

Thus, we can partition the set:

$$|A| = \sum_{C_a \in C'} |C_a| + \sum_{C_a \in C \setminus C'} |C_a|$$

For any class $C_a \in C \setminus C'$, we have $|C_a| = 2$. Therefore:

$$\sum_{C_a \in C \setminus C'} |C_a| \equiv 0 \pmod 2$$

It follows that:

$$|A| \equiv \sum_{C_a \in C'} |C_a| \pmod 2 = |A'| \implies |A| \equiv |A'| \pmod 2$$

$\square$

Since $f$ has exactly $1$ fixed point (an odd number), the cardinality of $S$ is **odd**.

### Part 3) Fixed Points of $g$ and the Final Proof

Clearly, $g(g(x,y,z)) = g(x,z,y) = (x,y,z)$ for all elements, so $g$ is an involution.

> **Lemma:** An involution acting on a set with an odd number of elements has at least one fixed point.

**Proof of Lemma:**

Assume for contradiction that the involution $f$ has no fixed points on a finite set $X$.

For each $x_i \in X$, define the orbit $S_i = \{x_i, f(x_i)\}$. Since $f$ has no fixed points, $|S_i| = 2$.

We claim that if $S_i \neq S_j$, then $S_i \cap S_j = \emptyset$.

Indeed, if the intersection of the two sets is non-empty, there are $4$ possible cases, each leading to a contradiction:

1. $x_i = x_j \implies f(x_i) = f(x_j)$. This means $S_i = S_j$, a contradiction.
    
2. $x_i = f(x_j) \implies f(x_i) = x_j$. This means $S_i = S_j$, a contradiction.
    
3. $f(x_i) = x_j \implies x_i = f(x_j)$. This means $S_i = S_j$, a contradiction.
    
4. $f(x_i) = f(x_j) \implies x_i = x_j$. This means $S_i = S_j$, a contradiction.
    

Thus, the sets $S_i$ are either identical or completely disjoint. Removing duplicate sets allows us to express $X$ as a disjoint union:

$$X = \bigcup_{x_i \in X} S_i = \dot{\bigcup}_{j} S_{i_j}$$

However, this implies $|X| = \sum_j |S_{i_j}|$, meaning $|X|$ must have an even number of elements, which contradicts our premise that $|X|$ is odd. By contraposition, the proposition is proven. $\square$

In conclusion, since $|S|$ is odd, $g$ must have at least one fixed point $(x,y,z) \in S$.

A fixed point of $g$ satisfies $g(x,y,z) = (x,z,y) = (x,y,z)$, which implies $y = z$.

Substituting $y = z$ into the equation for $S$:

$$x^2 + 4y^2 = p \implies x^2 + (2y)^2 = p$$

Setting $Y = 2y$, we get $x^2 + Y^2 = p$. Thus, $x^2 + y^2 = p$ has an integer solution.
