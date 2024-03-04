## Sets and Operations of Sets

### Sets

Relationship between Set and Elements:

- $x\in A$
- $x\notin A$

Relationship between Sets:

- $A\subset B\ \text{or}\ B\supset A:\ \forall x\in A,\ x\in B$
- $A\subsetneqq B:\ \forall x\in A, x\in B; \exists b\in B, b\notin A$

If $A\subset B$ and $B\subset A$, we say $A=B$.

Eg: $A=$ $`\{\pm1\}`$, $B=$ $`\{x:x^2-1=0\}`$ $\Rightarrow A=B$

### Operations in sets

Three fundamental operations of sets: $\cap, \cup, -$.

- Union: $A\cup B =$ $`\{x:x\in A\ \text{or}\ x\in B\}`$
- Intersection: $A\cap B = $ $`\{x:x\in A\ \text{and}\ x\in B\}`$

$A$ and $B$ are said to be disjoint if and only if $A\cap B=\varnothing$.

**Properties of $\cap$ and $\cup$:**

- $A\cap A = A,\ A\cup A = A$;
- $A\cup\varnothing = A$;
- $A\cup B = B\cup A,\ A\cap B = B\cap A$;
- $(A\cap B)\cap C = A\cap(B\cap C),\quad (A\cup B)\cup C = A\cup (B\cup C)$;
- $(A\cup B)\cap C = (A\cap C)\cup(B\cup C)$.

Subtraction: $A-B = $ $`\{x:x\in A, x\notin B\}`$, also denoted as $C_{A}B$. Let $\Omega$ denote the universe, then $C_{\Omega}B = B^C$.
**Properties of $-$:**

- $(A-B)\cap C = A\cap C - B\cap C$;
- $A - B = A\cap B^C,\ A\cap B = A - B^C$;
- If $A\subset B$, then $\forall C\in\Omega$: $A\cup C\subset B\cup C,\ A\cap C\subset B\cap C,\ A - C\subset B - C$.
- $(C - A) - B = C - (A\cup B)$;
- $A\subset B\iff A - B = \varnothing$.

*Proof:*
1. $\forall x\in A\cup C$, by definition we have $x\in A$ or $x\in C$. If $x\in A$, then according to $A\subset B$, we have $x\in B$, therefore $x\in B\cup C$. If $x\in C$, then $x\in B\cup C$. Either way, $x\in B\cup C$. Therefore $A\cup C\subset B\cup C$. With similar way we can prove the rest properties.
2. $(C-A)-B = $ $`\{x:x\in(C-A), x\notin B\}`$ $=$ $`\{x:x\in C, x\notin A, x\notin B\}`$ $=$ $`\{x:x\in C,x\notin(A\cup B)\}`$ $=$ $C-(A\cup B).\qquad\blacksquare$

Generation of Union and Intersection:

- $\displaystyle\bigcap_{\lambda\in\Lambda}A_{\lambda} = A_{\lambda_1}\cap A_{\lambda_2}\cap\cdots$
- $\displaystyle\bigcup_{\lambda\in\Lambda}A_{\lambda} = A_{\lambda_1}\cup A_{\lambda_2}\cup\cdots$

From here, we can deduct the following two equation:

- $\displaystyle S-\bigcap_{\lambda\in\Lambda}A_\lambda = \bigcup_{\lambda\in\Lambda}(S-A_\lambda)$;
- $\displaystyle S-\bigcup_{\lambda\in\Lambda}A_\lambda = \bigcap_{\lambda\in\Lambda}(S-A_\lambda)$.

*Proof:*
1. for $\displaystyle x\in S-\bigcap_{\lambda\in\Lambda}A_\lambda$, we have $x\in S$ and $\displaystyle x\notin\bigcap_{\lambda\in\Lambda}A_\lambda$. Therefore, $\displaystyle x\in\left(\bigcap_{\lambda\in\Lambda}A_\lambda\right)^C=\bigcup_{\lambda\in\Lambda}A_\lambda^C$, meaning that $\exists\lambda_0\in\Lambda$, s.t.$x\in A_{\lambda_0}^C\iff x\notin A_{\lambda_0}^C$. Since $x\in S$, we have $x\in S-A_{\lambda_0}^C$. Thus $\displaystyle x\in\bigcup_{\lambda\in\Lambda}(S-A_\lambda)$, meaning that $\displaystyle S-\bigcap_{\lambda\in\Lambda}A_\lambda\subset\bigcup_{\lambda\in\Lambda}(S-A_\lambda)$. On the other hand, for $\displaystyle x\in\bigcup_{\lambda\in\Lambda}(S-A_\lambda)$, by definition, $\exists \lambda_0\in\Lambda$, s.t. $x\in S-A_{\lambda_0}$, meaning that $x\in S$, but $x\notin A_{\lambda_0}$. Immediately we have $\displaystyle x\notin\bigcap_{\lambda\in\Lambda}A_{\lambda}$. Combining this with $x\in S$ we have $\displaystyle x\in S-\bigcap_{\lambda\in\Lambda}A_\lambda$, which is $\displaystyle\bigcup_{\lambda\in\Lambda}(S-A_\lambda)\subset S-\bigcap_{\lambda\in\Lambda}A_\lambda$. Therefore $\displaystyle S-\bigcap_{\lambda\in\Lambda}A_\lambda = \bigcup_{\lambda\in\Lambda}(S-A_\lambda)$.
2. With similar way we can prove the second property. $\blacksquare$

### Limit Superior, Limit Inferior, and Limit

For a series of sets $`\{A_n:n = 1, 2,\dots\}`$, element $x$ could be in some of these sets, and could be not in some of these sets. Denote the upper bound (also known as Limit Superior) of $`\{A_n:n = 1,2,\dots\}`$ as follows:

```math
\limsup_{n\to\infty}A_n:=\left\{x: \nexists k(x)\in\mathbb{N}_+,\ \text{s.t.}\ x\notin \bigcup_{n>k(x)}A_n\right\},
```

and similarly the lower bound (also known as Limit Inferior):
```math
\liminf_{n\to\infty}A_n:=\left\{x:\exists k(x)\in\mathbb{N}_+,\ \text{s.t.}\ x\in\bigcap_{n>k(x)}A_n\right\}.
```
Intuitively, $\displaystyle\limsup_{n\to\infty}A_n$ denotes elements that show up infinitely-many sets in $`\{A_n:n\in\mathbb{N}_+\}`$, and $\displaystyle\liminf_{n\to\infty}A_n$ denotes elements that show up in every set in $`\{A_n:n\in\mathbb{N}_+,\ n>k(x)\}`$. With these notation, the following statement is obvious:
```math
\bigcap_{n=1}^{\infty}A_n\subset\liminf_{n\to\infty}A_n\subset\limsup_{n\to\infty}A_n\subset\bigcup_{n=1}^{\infty}A_n.
```
Eg: Let $A_n$ be the following sets:
```math
A_{2n+1} = \left[0,\ 2-\frac{1}{2n+1}\right],\ n=0,1,2,\dots,\\A_{2n}=\left[0,\ 1+\frac{1}{2n}\right],\ n=1,2,\dots,
```
find the upper limit and lower limit for $`\{A_n:n\in\mathbb{N}\}`$.
*Solution:* By definition we have
```math
\limsup_{n\to\infty}A_n = [0,2),\quad\liminf_{n\to\infty}A_n=[0,1].\qquad\blacksquare
```

In fact, the upper and lower bound can be deducted from union and intersection:
```math
\limsup_{n\to\infty}A_n = \bigcap_{n=1}^{\infty}\bigcup_{m=n}^{\infty}A_m,\quad \liminf_{n\to\infty}A_n=\bigcup_{n=1}^{\infty}\bigcap_{m=n}^{\infty}A_m.
```
From there we can deduct a conclusion as follows:
```math
S-\liminf_{n\to\infty}A_n = \limsup_{n\to\infty}(S-A_n),\\
S-\limsup_{n\to\infty}A_n = \liminf_{n\to\infty}(S-A_n).
```
*Proof:* by calculation, we have
```math
\begin{align*}
S-\liminf_{n\to\infty}A_n={}&S-\bigcap_{n=1}^{\infty}\bigcup_{m=n}^{\infty}A_m\\
={}&\bigcup_{n=1}^{\infty}\left(S-\bigcup_{m=n}^{\infty}A_m\right)\\
={}&\bigcup_{n=1}^{\infty}\bigcap_{m=n}^{\infty}(S-A_m)\\
={}&\limsup_{n\to\infty}(S-A_n);\\
S-\limsup_{n\to\infty}A_n={}&S-\bigcup_{n\to\infty}^{\infty}\bigcap_{m=n}^{\infty}A_m\\
={}&\bigcap_{n=1}^{\infty}\left(S-\bigcap_{m=n}^{\infty}A_m\right)\\
={}&\bigcap_{n=1}^{\infty}\bigcup_{n=1}^{\infty}(S-A_m)\\
={}&\limsup_{n\to\infty}A_n.\qquad\qquad\qquad\blacksquare
\end{align*}
```

If $\displaystyle\limsup_{n\to\infty}A_n=\liminf_{n\to\infty}A_n=A$, we say set series $\{A_n:n\in\mathbb{N}\}$ converges. $A$ is called the limit of $`\{A_n:n = 1,2,\dots\}`$, denoted by $\displaystyle\lim_{n\to\infty}A_n=A$.

**Monotonic Set Series**
Say set series $\{A_n:n=1,2,\dots\}$ to be monotonicly increasing, if 
```math
A_n\subset A_{n+1},\quad n=1,2,3,\dots
```
and monotonicly decreasing, if
```math
A_n\supset A_{n+1},\quad n = 1, 2,3,\dots
```
Show that monotonic set seires converges.
*Proof:* Suppose $\{A_n\}_{n\in\mathbb{N}}$ monotonically increases. We want to show that
```math
\limsup_{n\to\infty}A_n = \liminf_{n\to\infty}A_n,
```
which is equivalent as 
```math
\bigcap_{n=1}^{\infty}\bigcup_{m=n}^{\infty}A_m = \bigcup_{n=1}^{\infty}\bigcap_{m=n}^{\infty}A_m. \tag{1}
```
The right hand side of (1) is
```math
\bigcup_{n=1}^{\infty}\bigcap_{m=n}^{\infty}A_m = \bigcup_{n=1}^{\infty}A_n.
```
Notice that with $A_n \subset A_{n+1}$, we have
```math
\bigcup_{m=n}^{\infty}A_m = \bigcup_{m=n+1}^{\infty}A_m,
```
which leads to 
```math
\bigcup_{m=n}^{\infty}A_m = \bigcup_{m=1}^{\infty}A_m.
```
Therefore, the left hand side of (1) becomes
```math
\bigcap_{n=1}^{\infty}\bigcup_{m=n}^{\infty}A_m=\bigcap_{n=1}^{\infty}\bigcup_{m=1}^{\infty}A_m=\bigcup_{m=1}^{\infty}A_m.
```
Thus equation (1) holds. With similar proof we can prove monotonically decreasing set seires also converges to $\displaystyle\bigcap_{n=1}^{\infty}A_n$.
