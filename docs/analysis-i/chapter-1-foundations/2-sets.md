# Chapter I — Foundations

## 2. Sets

Complements below are taken relative to the ambient set under discussion. For the family identities, the index sets are nonempty, as in the book's definition of a family.

### Exercise 1

Assume $$X\subseteq Y$$ and $$Y\subseteq Z$$. To prove $$X\subseteq Z$$, take any $$x\in X$$. The first inclusion gives $$x\in Y$$, and the second then gives $$x\in Z$$. Since $$x$$ was arbitrary, $$X\subseteq Z$$.

### Exercise 2

Let $$X,Y,Z$$ be subsets of a common set. Each identity follows by testing membership of an arbitrary element $$x$$.

**(i) Commutativity.**

For unions,
$$
\begin{aligned}
x\in X\cup Y
&\iff (x\in X)\lor(x\in Y)\\
&\iff (x\in Y)\lor(x\in X)\\
&\iff x\in Y\cup X.
\end{aligned}
$$

For intersections, the same argument gives
$$
\begin{aligned}
x\in X\cap Y
&\iff (x\in X)\land(x\in Y)\\
&\iff (x\in Y)\land(x\in X)\\
&\iff x\in Y\cap X.
\end{aligned}
$$
Thus $$X\cup Y=Y\cup X$$ and $$X\cap Y=Y\cap X$$.

**(ii) Associativity.**

For unions,
$$
\begin{aligned}
x\in X\cup(Y\cup Z)
&\iff (x\in X)\lor(x\in Y)\lor(x\in Z)\\
&\iff x\in(X\cup Y)\cup Z.
\end{aligned}
$$

For intersections,
$$
\begin{aligned}
x\in X\cap(Y\cap Z)
&\iff (x\in X)\land(x\in Y)\land(x\in Z)\\
&\iff x\in(X\cap Y)\cap Z.
\end{aligned}
$$
Hence both operations are associative.

**(iii) Distributivity.**

By distributivity of logical “or” over “and”,
$$
\begin{aligned}
x\in X\cup(Y\cap Z)
&\iff (x\in X)\lor\bigl((x\in Y)\land(x\in Z)\bigr)\\
&\iff \bigl((x\in X)\lor(x\in Y)\bigr)
       \land\bigl((x\in X)\lor(x\in Z)\bigr)\\
&\iff x\in(X\cup Y)\cap(X\cup Z).
\end{aligned}
$$

The other identity follows from the dual logical law:
$$
\begin{aligned}
x\in X\cap(Y\cup Z)
&\iff (x\in X)\land\bigl((x\in Y)\lor(x\in Z)\bigr)\\
&\iff \bigl((x\in X)\land(x\in Y)\bigr)
       \lor\bigl((x\in X)\land(x\in Z)\bigr)\\
&\iff x\in(X\cap Y)\cup(X\cap Z).
\end{aligned}
$$

**(iv) Characterizing inclusion.** If $$X\subseteq Y$$, then every element of $$Y$$ is already in $$X\cup Y$$, so $$X\cup Y=Y$$; every element of $$X$$ is in $$X\cap Y$$, so $$X\cap Y=X$$. Conversely, if $$X\cup Y=Y$$, then $$x\in X$$ implies $$x\in X\cup Y=Y$$, hence $$X\subseteq Y$$. If $$X\cap Y=X$$, then $$x\in X$$ implies $$x\in X\cap Y$$, and therefore $$x\in Y$$. Thus
$$
X\subseteq Y
\iff X\cup Y=Y
\iff X\cap Y=X.
$$

### Exercise 3

Let $$A$$ be a family of subsets of a fixed set, indexed by $$I$$, and $$B$$ a family indexed by $$J$$. We verify each identity by element membership.

**(i) Associativity for indexed families.**

For intersections,
$$
\begin{aligned}
x&\in\left(\bigcap_{\alpha\in I}A_\alpha\right)
       \cap\left(\bigcap_{\beta\in J}B_\beta\right)\\
&\iff \left(\forall\alpha\in I,\ x\in A_\alpha\right)
       \land\left(\forall\beta\in J,\ x\in B_\beta\right)\\
&\iff \forall(\alpha,\beta)\in I\times J,\;
       x\in A_\alpha\cap B_\beta\\
&\iff x\in\bigcap_{(\alpha,\beta)\in I\times J}
       \left(A_\alpha\cap B_\beta\right).
\end{aligned}
$$

For unions,
$$
\begin{aligned}
x&\in\left(\bigcup_{\alpha\in I}A_\alpha\right)
       \cup\left(\bigcup_{\beta\in J}B_\beta\right)\\
&\iff \left(\exists\alpha\in I,\ x\in A_\alpha\right)
       \lor\left(\exists\beta\in J,\ x\in B_\beta\right)\\
&\iff \exists(\alpha,\beta)\in I\times J,\;
       x\in A_\alpha\cup B_\beta\\
&\iff x\in\bigcup_{(\alpha,\beta)\in I\times J}
       \left(A_\alpha\cup B_\beta\right).
\end{aligned}
$$
The second equivalence uses the fact that both index sets are nonempty.

**(ii) Distributivity for indexed families.** For the first identity, if $$x$$ belongs to every set in family $$A$$, or to every set in family $$B$$, then $$x$$ belongs to at least one of the sets in those families for every pair of indices. Conversely, suppose that for every $$\alpha\in I$$ and $$\beta\in J$$, $$x$$ belongs to at least one of $$A_\alpha$$ and $$B_\beta$$. If $$x$$ did not belong to every set in family $$A$$, choose $$\alpha_0\in I$$ such that $$x\notin A_{\alpha_0}$$. If it also did not belong to every set in family $$B$$, choose $$\beta_0\in J$$ such that $$x\notin B_{\beta_0}$$. Then $$x$$ belongs to neither set for the pair $$(\alpha_0,\beta_0)$$, a contradiction. Therefore $$x$$ belongs to every set in family $$A$$ or to every set in family $$B$$, proving
$$
\left(\bigcap_{\alpha\in I}A_\alpha\right)
\cup
\left(\bigcap_{\beta\in J}B_\beta\right)
=
\bigcap_{(\alpha,\beta)\in I\times J}
\left(A_\alpha\cup B_\beta\right).
$$

For the other identity, membership on the left means that $$x$$ belongs to some set in family $$A$$ and some set in family $$B$$. Choose indices $$\alpha_0$$ and $$\beta_0$$ for these sets. This is equivalent to saying that $$x$$ belongs to both selected sets for some pair of indices, so
$$
\left(\bigcup_{\alpha\in I}A_\alpha\right)
\cap
\left(\bigcup_{\beta\in J}B_\beta\right)
=
\bigcup_{(\alpha,\beta)\in I\times J}
\left(A_\alpha\cap B_\beta\right).
$$

**(iii) De Morgan's laws.** By the definition of complement,
$$
\begin{aligned}
x&\in\left(\bigcup_{\alpha\in I}A_\alpha\right)^{\mathrm c}\\
&\iff \neg\left(\exists\alpha\in I,\ x\in A_\alpha\right)\\
&\iff \forall\alpha\in I,\ x\notin A_\alpha\\
&\iff x\in\bigcap_{\alpha\in I}A_\alpha^{\mathrm c}.
\end{aligned}
$$

Similarly,
$$
\begin{aligned}
x&\in\left(\bigcap_{\alpha\in I}A_\alpha\right)^{\mathrm c}\\
&\iff \neg\left(\forall\alpha\in I,\ x\in A_\alpha\right)\\
&\iff \exists\alpha\in I,\ x\notin A_\alpha\\
&\iff x\in\bigcup_{\alpha\in I}A_\alpha^{\mathrm c}.
\end{aligned}
$$

### Exercise 4

Assume $$X$$ and $$Y$$ are nonempty and $$X\times Y=Y\times X$$. Choose $$y_0\in Y$$. For any $$x\in X$$, the pair $$(x,y_0)$$ belongs to $$X\times Y=Y\times X$$, so its first coordinate $$x$$ lies in $$Y$$. Thus $$X\subseteq Y$$.

Now choose $$x_0\in X$$. For any $$y\in Y$$, $$(y,x_0)\in Y\times X=X\times Y$$, so $$y\in X$$. Hence $$Y\subseteq X$$, and therefore $$X=Y$$.

Conversely, if $$X=Y$$, then their Cartesian products with themselves agree, so $$X\times Y=Y\times X$$. We have proved
$$
X\times Y=Y\times X
\iff X=Y.
$$

### Exercise 5

All complements are relative to $$X$$.

**(a)** By double complementation, $$(A^{\mathrm c})^{\mathrm c}=A$$.

**(b)** A set and its complement are disjoint, so $$A\cap A^{\mathrm c}=\varnothing$$.

**(c)** Every element of $$X$$ lies either in $$A$$ or in $$A^{\mathrm c}$$, so $$A\cup A^{\mathrm c}=X$$.

**(d)** Distributing the intersection gives
$$
\begin{aligned}
(A^{\mathrm c}\cup B)\cap A\cap B^{\mathrm c}
&=(A^{\mathrm c}\cap A\cap B^{\mathrm c})
  \cup(B\cap A\cap B^{\mathrm c})\\
&=\varnothing.
\end{aligned}
$$
Thus $$(A^{\mathrm c}\cup B)\cap(A\cap B^{\mathrm c})=\varnothing$$.

**(e)** If $$x\in A^{\mathrm c}$$, it is already in the union. If $$x\notin A^{\mathrm c}$$, then $$x\in A$$. In that case either $$x\in B$$, or $$x\in B^{\mathrm c}$$; in the latter case $$x\in A\cap B^{\mathrm c}$$. Thus every $$x\in X$$ belongs to $$(A^{\mathrm c}\cup B)\cup(A\cap B^{\mathrm c})$$, and
$$
(A^{\mathrm c}\cup B)\cup(A\cap B^{\mathrm c})=X.
$$

**(f)** Since $$A^{\mathrm c}\cup B^{\mathrm c}=(A\cap B)^{\mathrm c}$$,
$$
\begin{aligned}
(A^{\mathrm c}\cup B^{\mathrm c})\cap(A\cup B)
&=(A\cup B)\setminus(A\cap B)\\
&=(A\setminus B)\cup(B\setminus A).
\end{aligned}
$$
This is the symmetric difference of $$A$$ and $$B$$.

**(g)** An element of $$A\cap B$$ belongs to neither $$A^{\mathrm c}$$ nor $$B^{\mathrm c}$$. Hence
$$
(A^{\mathrm c}\cup B^{\mathrm c})\cap(A\cap B)=\varnothing.
$$

### Exercise 6

Every member $$A$$ of $$\mathcal P(X)$$ is a subset of $$X$$, so
$$
\bigcup_{A\in\mathcal P(X)}A\subseteq X.
$$

Conversely, for each $$x\in X$$, the singleton $$\{x\}$$ is in $$\mathcal P(X)$$, so $$x$$ belongs to the union. Therefore
$$
\bigcup_{A\in\mathcal P(X)}A=X.
$$

The empty set is itself in $$\mathcal P(X)$$. Any element in the intersection of all members of $$\mathcal P(X)$$ would therefore have to belong to $$\varnothing$$, which is impossible. Thus
$$
\bigcap_{A\in\mathcal P(X)}A=\varnothing.
$$

### Exercise 7

Let $$X,A\subseteq U$$ and $$Y,B\subseteq V$$.

**(a)** Suppose $$A\times B\ne\varnothing$$. If $$A\times B\subseteq X\times Y$$, then $$A$$ and $$B$$ are both nonempty. Fix $$a\in A$$, and choose $$b_0\in B$$. Since $$(a,b_0)\in X\times Y$$, its first coordinate gives $$a\in X$$. Hence $$A\subseteq X$$. Fixing $$b\in B$$ and choosing $$a_0\in A$$ similarly gives $$b\in Y$$, so $$B\subseteq Y$$.

Conversely, if $$A\subseteq X$$ and $$B\subseteq Y$$, then every $$(a,b)\in A\times B$$ also belongs to $$X\times Y$$. Therefore
$$
A\times B\subseteq X\times Y
\iff
A\subseteq X\text{ and }B\subseteq Y.
$$
This equivalence is asserted under the assumption $$A\times B\ne\varnothing$$. If $$A\times B=\varnothing$$, the product inclusion holds vacuously, even when one of the factor inclusions fails.

**(b)** A pair $$(u,v)$$ belongs to the left side exactly when
$$
\begin{aligned}
(u,v)\in(X\times Y)\cup(A\times Y)
&\iff \bigl((u\in X)\land(v\in Y)\bigr)
      \lor\bigl((u\in A)\land(v\in Y)\bigr)\\
&\iff (u\in X\cup A)\land(v\in Y).
\end{aligned}
$$
This is precisely membership in $$(X\cup A)\times Y$$. Hence
$$
(X\times Y)\cup(A\times Y)=(X\cup A)\times Y.
$$

**(c)** A pair $$(u,v)$$ lies in the left side exactly when
$$
\begin{aligned}
(u,v)\in(X\times Y)\cap(A\times B)
&\iff (u\in X\cap A)\land(v\in Y\cap B).
\end{aligned}
$$
Thus
$$
(X\times Y)\cap(A\times B)=(X\cap A)\times(Y\cap B).
$$

**(d)** A pair $$(u,v)$$ lies in $$(X\times Y)\setminus(A\times B)$$ exactly when $$u\in X$$, $$v\in Y$$, and it is not the case that both $$u\in A$$ and $$v\in B$$. The last condition is equivalent to $$u\notin A$$ or $$v\notin B$$. Therefore
$$
(X\times Y)\setminus(A\times B)
=\bigl((X\setminus A)\times Y\bigr)
\cup\bigl(X\times(Y\setminus B)\bigr).
$$

### Exercise 8

Let $$A$$ be a family of sets indexed by $$I$$, and $$B$$ a family of sets indexed by $$J$$.

**(a)** A pair $$(x,y)$$ belongs to the product of the intersection of all sets in family $$A$$ and the intersection of all sets in family $$B$$ exactly when $$x$$ belongs to every set in family $$A$$ and $$y$$ belongs to every set in family $$B$$. This is equivalent to saying that, for every $$\alpha\in I$$ and $$\beta\in J$$, $$(x,y)$$ belongs to the product of $$A_\alpha$$ and $$B_\beta$$. Hence
$$
\left(\bigcap_{\alpha\in I}A_\alpha\right)
\times
\left(\bigcap_{\beta\in J}B_\beta\right)
=
\bigcap_{(\alpha,\beta)\in I\times J}
\left(A_\alpha\times B_\beta\right).
$$

**(b)** A pair $$(x,y)$$ belongs to the product of the union of all sets in family $$A$$ and the union of all sets in family $$B$$ exactly when there are indices $$\alpha_0\in I$$ and $$\beta_0\in J$$ such that $$x$$ belongs to $$A_{\alpha_0}$$ and $$y$$ belongs to $$B_{\beta_0}$$. Equivalently, $$(x,y)$$ belongs to the product of those two sets for some pair of indices. Thus
$$
\left(\bigcup_{\alpha\in I}A_\alpha\right)
\times
\left(\bigcup_{\beta\in J}B_\beta\right)
=
\bigcup_{(\alpha,\beta)\in I\times J}
\left(A_\alpha\times B_\beta\right).
$$
