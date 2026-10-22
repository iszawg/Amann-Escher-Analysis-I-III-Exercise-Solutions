# Chapter I — Foundations

## 2. Sets

Complements below are taken relative to the ambient set under discussion. For the family identities, the index sets are nonempty, as in the book's definition of a family.

### Exercise 1

Assume $X\subseteq Y$ and $Y\subseteq Z$. To prove $X\subseteq Z$, take any $x\in X$. The first inclusion gives $x\in Y$, and the second then gives $x\in Z$. Since $x$ was arbitrary, $X\subseteq Z$.

### Exercise 2

Let $X,Y,Z$ be subsets of a common set. Each identity follows by testing membership of an arbitrary element $x$.

**(i) Commutativity.**

\[
x\in X\cup Y\iff (x\in X)\lor(x\in Y)\iff(x\in Y)\lor(x\in X)\iff x\in Y\cup X,
\]

and similarly,

\[
x\in X\cap Y\iff (x\in X)\land(x\in Y)\iff(x\in Y)\land(x\in X)\iff x\in Y\cap X.
\]

Thus $X\cup Y=Y\cup X$ and $X\cap Y=Y\cap X$.

**(ii) Associativity.**

\[
x\in X\cup(Y\cup Z)\iff (x\in X)\lor(x\in Y)\lor(x\in Z)\iff x\in(X\cup Y)\cup Z,
\]

and

\[
x\in X\cap(Y\cap Z)\iff (x\in X)\land(x\in Y)\land(x\in Z)\iff x\in(X\cap Y)\cap Z.
\]

Hence both operations are associative.

**(iii) Distributivity.**

\[
\begin{aligned}
x\in X\cup(Y\cap Z)
&\iff (x\in X)\lor\bigl((x\in Y)\land(x\in Z)\bigr)\\
&\iff\bigl((x\in X)\lor(x\in Y)\bigr)\land\bigl((x\in X)\lor(x\in Z)\bigr)\\
&\iff x\in(X\cup Y)\cap(X\cup Z),
\end{aligned}
\]

by distributivity of logical “or” over “and”. The other identity follows from the dual logical law:

\[
\begin{aligned}
x\in X\cap(Y\cup Z)
&\iff (x\in X)\land\bigl((x\in Y)\lor(x\in Z)\bigr)\\
&\iff\bigl((x\in X)\land(x\in Y)\bigr)\lor\bigl((x\in X)\land(x\in Z)\bigr)\\
&\iff x\in(X\cap Y)\cup(X\cap Z).
\end{aligned}
\]

**(iv) Characterizing inclusion.** If $X\subseteq Y$, then every element of $Y$ is already in $X\cup Y$, so $X\cup Y=Y$; every element of $X$ is in $X\cap Y$, so $X\cap Y=X$. Conversely, if $X\cup Y=Y$, then $x\in X$ implies $x\in X\cup Y=Y$, hence $X\subseteq Y$. If $X\cap Y=X$, then $x\in X$ implies $x\in X\cap Y$, and therefore $x\in Y$. Thus

\[
X\subseteq Y\iff X\cup Y=Y\iff X\cap Y=X.
\]

### Exercise 3

Let $\{A_\alpha;\alpha\in I\}$ and $\{B_\beta;\beta\in J\}$ be families of subsets of a fixed set. We verify each identity by element membership.

**(i) Associativity for indexed families.** For intersections,

\[
\begin{aligned}
x\in\left(\bigcap_{\alpha\in I}A_\alpha\right)\cap\left(\bigcap_{\beta\in J}B_\beta\right)
&\iff (\forall\alpha\in I:\ x\in A_\alpha)\land(\forall\beta\in J:\ x\in B_\beta)\\
&\iff \forall(\alpha,\beta)\in I\times J:\ x\in A_\alpha\cap B_\beta\\
&\iff x\in\bigcap_{(\alpha,\beta)\in I\times J}(A_\alpha\cap B_\beta).
\end{aligned}
\]

For unions,

\[
\begin{aligned}
x\in\left(\bigcup_{\alpha\in I}A_\alpha\right)\cup\left(\bigcup_{\beta\in J}B_\beta\right)
&\iff (\exists\alpha\in I:\ x\in A_\alpha)\lor(\exists\beta\in J:\ x\in B_\beta)\\
&\iff \exists(\alpha,\beta)\in I\times J:\ x\in A_\alpha\cup B_\beta\\
&\iff x\in\bigcup_{(\alpha,\beta)\in I\times J}(A_\alpha\cup B_\beta).
\end{aligned}
\]

The second equivalence uses the fact that both index sets are nonempty.

**(ii) Distributivity for indexed families.** For the first identity, if $x$ belongs to every $A_\alpha$, or to every $B_\beta$, it belongs to every $A_\alpha\cup B_\beta$. Conversely, suppose $x\in A_\alpha\cup B_\beta$ for every pair $(\alpha,\beta)$. If $x$ did not belong to every $A_\alpha$, choose $\alpha_0$ with $x\notin A_{\alpha_0}$. If it also did not belong to every $B_\beta$, choose $\beta_0$ with $x\notin B_{\beta_0}$. Then $x\notin A_{\alpha_0}\cup B_{\beta_0}$, a contradiction. Therefore $x$ belongs to every $A_\alpha$ or to every $B_\beta$, proving

\[
\left(\bigcap_{\alpha\in I}A_\alpha\right)\cup\left(\bigcap_{\beta\in J}B_\beta\right)
=\bigcap_{(\alpha,\beta)\in I\times J}(A_\alpha\cup B_\beta).
\]

For the other identity, membership on the left means that $x\in A_{\alpha_0}$ for some $\alpha_0$ and $x\in B_{\beta_0}$ for some $\beta_0$. This is equivalent to $x\in A_{\alpha_0}\cap B_{\beta_0}$ for some pair, so

\[
\left(\bigcup_{\alpha\in I}A_\alpha\right)\cap\left(\bigcup_{\beta\in J}B_\beta\right)
=\bigcup_{(\alpha,\beta)\in I\times J}(A_\alpha\cap B_\beta).
\]

**(iii) De Morgan's laws.** By the definition of complement,

\[
\begin{aligned}
x\in\left(\bigcup_{\alpha\in I}A_\alpha\right)^c
&\iff \neg\bigl(\exists\alpha\in I:\ x\in A_\alpha\bigr)\\
&\iff \forall\alpha\in I:\ x\notin A_\alpha\\
&\iff x\in\bigcap_{\alpha\in I}A_\alpha^c.
\end{aligned}
\]

Similarly,

\[
\begin{aligned}
x\in\left(\bigcap_{\alpha\in I}A_\alpha\right)^c
&\iff \neg\bigl(\forall\alpha\in I:\ x\in A_\alpha\bigr)\\
&\iff \exists\alpha\in I:\ x\notin A_\alpha\\
&\iff x\in\bigcup_{\alpha\in I}A_\alpha^c.
\end{aligned}
\]

### Exercise 4

Assume $X$ and $Y$ are nonempty and $X\times Y=Y\times X$. Choose $y_0\in Y$. For any $x\in X$, the pair $(x,y_0)$ belongs to $X\times Y=Y\times X$, so its first coordinate $x$ lies in $Y$. Thus $X\subseteq Y$.

Now choose $x_0\in X$. For any $y\in Y$, $(y,x_0)\in Y\times X=X\times Y$, so $y\in X$. Hence $Y\subseteq X$, and therefore $X=Y$.

Conversely, if $X=Y$, then their Cartesian products with themselves agree, so $X\times Y=Y\times X$. We have proved

\[
X\times Y=Y\times X\iff X=Y.
\]

### Exercise 5

All complements are relative to $X$.

**(a)** By double complementation, $(A^c)^c=A$.

**(b)** A set and its complement are disjoint, so $A\cap A^c=\varnothing$.

**(c)** Every element of $X$ lies either in $A$ or in $A^c$, so $A\cup A^c=X$.

**(d)** Distributing the intersection gives

\[
(A^c\cup B)\cap A\cap B^c
=(A^c\cap A\cap B^c)\cup(B\cap A\cap B^c)=\varnothing.
\]

Thus $(A^c\cup B)\cap(A\cap B^c)=\varnothing$.

**(e)** If $x\in A^c$, it is already in the union. If $x\notin A^c$, then $x\in A$. In that case either $x\in B$, or $x\in B^c$; in the latter case $x\in A\cap B^c$. Thus every $x\in X$ belongs to $(A^c\cup B)\cup(A\cap B^c)$, and the expression equals $X$.

**(f)** Since $A^c\cup B^c=(A\cap B)^c$,

\[
(A^c\cup B^c)\cap(A\cup B)
=\bigl((A\cup B)\setminus(A\cap B)\bigr)
=(A\setminus B)\cup(B\setminus A).
\]

This is the symmetric difference of $A$ and $B$.

**(g)** An element of $A\cap B$ belongs to neither $A^c$ nor $B^c$. Hence

\[
(A^c\cup B^c)\cap(A\cap B)=\varnothing.
\]

### Exercise 6

Every member $A$ of $\mathcal P(X)$ is a subset of $X$, so

\[
\bigcup_{A\in\mathcal P(X)}A\subseteq X.
\]

Conversely, for each $x\in X$, the singleton $\{x\}$ is in $\mathcal P(X)$, so $x$ belongs to the union. Therefore

\[
\bigcup_{A\in\mathcal P(X)}A=X.
\]

The empty set is itself in $\mathcal P(X)$. Any element in the intersection of all members of $\mathcal P(X)$ would therefore have to belong to $\varnothing$, which is impossible. Thus

\[
\bigcap_{A\in\mathcal P(X)}A=\varnothing.
\]

### Exercise 7

Let $X,A\subseteq U$ and $Y,B\subseteq V$.

**(a)** Assume $A\times B\ne\varnothing$ and $A\times B\subseteq X\times Y$. Then $A$ and $B$ are both nonempty. Fix $a\in A$, and choose $b_0\in B$. Since $(a,b_0)\in X\times Y$, its first coordinate gives $a\in X$. Hence $A\subseteq X$. Fixing $b\in B$ and choosing $a_0\in A$ similarly gives $b\in Y$, so $B\subseteq Y$.

Conversely, if $A\subseteq X$ and $B\subseteq Y$, then every $(a,b)\in A\times B$ also belongs to $X\times Y$. Therefore

\[
A\times B\ne\varnothing\quad\Longrightarrow\quad
\bigl(A\times B\subseteq X\times Y\iff A\subseteq X\text{ and }B\subseteq Y\bigr).
\]

**(b)** A pair $(u,v)$ belongs to the left side exactly when

\[
\bigl((u\in X\land v\in Y)\lor(u\in A\land v\in Y)\bigr),
\]

which is equivalent to $u\in X\cup A$ and $v\in Y$. This is precisely membership in $(X\cup A)\times Y$. Hence

\[
(X\times Y)\cup(A\times Y)=(X\cup A)\times Y.
\]

**(c)** A pair $(u,v)$ lies in $(X\times Y)\cap(A\times B)$ exactly when $u\in X\cap A$ and $v\in Y\cap B$. Thus

\[
(X\times Y)\cap(A\times B)=(X\cap A)\times(Y\cap B).
\]

**(d)** A pair $(u,v)$ lies in $(X\times Y)\setminus(A\times B)$ exactly when $u\in X$, $v\in Y$, and it is not the case that both $u\in A$ and $v\in B$. The last condition is equivalent to $u\notin A$ or $v\notin B$. Therefore

\[
(X\times Y)\setminus(A\times B)
=((X\setminus A)\times Y)\cup(X\times(Y\setminus B)).
\]

### Exercise 8

Let $\{A_\alpha;\alpha\in I\}$ and $\{B_\beta;\beta\in J\}$ be families of sets.

**(a)** A pair $(x,y)$ belongs to $(\bigcap_{\alpha\in I}A_\alpha)\times(\bigcap_{\beta\in J}B_\beta)$ exactly when $x\in A_\alpha$ for every $\alpha\in I$ and $y\in B_\beta$ for every $\beta\in J$. This is equivalent to saying that $(x,y)\in A_\alpha\times B_\beta$ for every $(\alpha,\beta)\in I\times J$. Hence

\[
\left(\bigcap_{\alpha\in I}A_\alpha\right)\times
\left(\bigcap_{\beta\in J}B_\beta\right)
=\bigcap_{(\alpha,\beta)\in I\times J}(A_\alpha\times B_\beta).
\]

**(b)** A pair $(x,y)$ belongs to $(\bigcup_{\alpha\in I}A_\alpha)\times(\bigcup_{\beta\in J}B_\beta)$ exactly when there are indices $\alpha_0\in I$ and $\beta_0\in J$ with $x\in A_{\alpha_0}$ and $y\in B_{\beta_0}$. Equivalently, $(x,y)$ belongs to $A_{\alpha_0}\times B_{\beta_0}$ for some pair of indices. Thus

\[
\left(\bigcup_{\alpha\in I}A_\alpha\right)\times
\left(\bigcup_{\beta\in J}B_\beta\right)
=\bigcup_{(\alpha,\beta)\in I\times J}(A_\alpha\times B_\beta).
\]
