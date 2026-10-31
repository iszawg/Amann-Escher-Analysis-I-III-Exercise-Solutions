# Chapter IX — Elements of Measure Theory

## 2. Measures

These are detailed solutions to Exercises 1–13. Complements are relative to $$X$$. We write $$\mathcal N_\mu$$ for the measurable $$\mu$$-null sets and $$(\mathcal A_\mu,\bar\mu)$$ for the completion of $$(\mathcal A,\mu)$$. Inline formulas use GitBook's double-dollar syntax.

### Exercise 1

The generated family is $$\mathcal A=\{\varnothing,A,A^c,X\}$$, with repetitions removed when $$A=\varnothing$$ or $$A=X$$. In fact, this family is a $$\sigma$$-algebra containing $$A$$ and must be contained in every such $$\sigma$$-algebra.

For a disjoint sequence $$(B_j)$$ in $$\mathcal A$$, if every $$B_j$$ is empty, both sides of countable additivity are zero. Otherwise their union is nonempty and at least one summand is $$\infty$$, so both sides equal $$\infty$$. Also $$\mu(\varnothing)=0$$. Thus $$\mu$$ is a measure. Its only null set is $$\varnothing$$, whose only subset is measurable. Hence the measure is complete.

### Exercise 2

**The formula as printed needs a finiteness qualification.** If $$A_1=A_2=X=\mathbb N$$ and $$\mu$$ is counting measure, its right side contains $$\infty+\infty-\infty$$, which is undefined, while its left side is $$\infty$$. The following proof applies when $$\mu(\bigcup_{j=1}^n A_j)<\infty$$, equivalently when each $$\mu(A_j)<\infty$$.

For every nonempty $$I\subset\{1,\ldots,n\}$$ put

$$
C_I=\left(\bigcap_{i\in I}A_i\right)\setminus\left(\bigcup_{i\notin I}A_i\right).
$$

These measurable sets are disjoint and partition the union: $$C_I$$ consists of points belonging to exactly the sets indexed by $$I$$. Write $$m_I=\mu(C_I)$$. All $$m_I$$ are finite. For each nonempty $$J$$, finite additivity gives

$$
\mu\left(\bigcap_{j\in J}A_j\right)=\sum_{I\supset J}m_I.
$$

Substituting in the alternating sum and grouping by $$I$$, the coefficient of $$m_I$$ is

$$
\sum_{k=1}^{|I|}(-1)^{k+1}\binom{|I|}{k}=1,
$$

by the binomial theorem. The sum is therefore $$\sum_{I\ne\varnothing}m_I=\mu(\bigcup_j A_j)$$, as claimed. Without finiteness one may instead use the equivalent equality obtained by moving all even-order terms to the left; that equality involves only addition and remains meaningful in $$[0,\infty]$$.

### Exercise 3

Take $$A_j=\{m\in\mathbb N:m\ge j\}$$. These tails decrease and every one is infinite, so $$\mathcal H^0(A_j)=\infty$$ for all $$j$$. Their intersection is empty, however. Thus the limit of the measures is $$\infty$$ and the measure of the intersection is zero. This shows why continuity from above requires a finite-measure starting set.

### Exercise 4

By the book's definition of an additive set function, $$\mu(\varnothing)=0$$. Let $$(A_j)$$ be pairwise disjoint and set $$S_n=\bigcup_{j=0}^n A_j$$. The sets $$S_n$$ increase to $$\bigcup_{j=0}^\infty A_j$$. Continuity from below and finite additivity yield

$$
\mu\left(\bigcup_{j=0}^\infty A_j\right)
=\lim_{n\to\infty}\mu(S_n)
=\lim_{n\to\infty}\sum_{j=0}^n\mu(A_j)
=\sum_{j=0}^\infty\mu(A_j).
$$

This holds also when the limit is infinite, and proves countable additivity.

### Exercise 5

Clearly $$\mu_B(\varnothing)=0$$. If the measurable sets $$A_j$$ are pairwise disjoint, then so are $$A_j\cap B$$, and intersection distributes over their union. Therefore

$$
\mu_B\left(\bigcup_j A_j\right)
=\mu\left(\bigcup_j(A_j\cap B)\right)
=\sum_j\mu(A_j\cap B)=\sum_j\mu_B(A_j).
$$

Thus $$\mu_B$$ is a measure on the original $$\sigma$$-algebra $$\mathcal A$$. It is distinct in domain from the restriction of $$\mu$$ to the trace $$\sigma$$-algebra on $$B$$.

### Exercise 6

For each $$n$$ define

$$
L_n=\bigcap_{j\ge n}A_j,\qquad U_n=\bigcup_{j\ge n}A_j.
$$

Then $$L_n\uparrow\liminf_j A_j$$ and $$U_n\downarrow\limsup_j A_j$$.

**(a)** For every $$j\ge n$$, $$L_n\subset A_j$$. Consequently $$\mu(L_n)\le\inf_{j\ge n}\mu(A_j)$$. Continuity from below gives

$$
\mu(\liminf_j A_j)=\lim_n\mu(L_n)
\le\lim_n\inf_{j\ge n}\mu(A_j)=\liminf_j\mu(A_j).
$$

**(b)** Suppose $$\mu(U_k)<\infty$$ for some $$k$$. For $$n\ge k$$, $$\mu(U_n)<\infty$$, and $$\mu(A_j)\le\mu(U_n)$$ for all $$j\ge n$$. Continuity from above thus gives

$$
\mu(\limsup_j A_j)=\lim_{n\to\infty}\mu(U_n)
\ge\lim_{n\to\infty}\sup_{j\ge n}\mu(A_j)=\limsup_j\mu(A_j).
$$

**(c)** If the set sequence converges to $$A$$, its liminf and limsup both equal $$A$$. Parts (a) and (b), together with the general inequality $$\liminf\mu(A_j)\le\limsup\mu(A_j)$$, give

$$
\mu(A)\le\liminf_j\mu(A_j)\le\limsup_j\mu(A_j)\le\mu(A).
$$

Hence the numerical limit exists and equals $$\mu(A)$$. In particular the common value is finite because $$A\subset U_k$$.

### Exercise 7

The first completion $$(X,\mathcal A_\mu,\bar\mu)$$ is complete. Consequently every subset of a $$\bar\mu$$-null set already belongs to $$\mathcal A_\mu$$. In the construction of its completion, each set has the form $$E\cup M$$ with $$E\in\mathcal A_\mu$$ and $$M$$ contained in such a null set; hence it already lies in $$\mathcal A_\mu$$. The reverse inclusion is automatic. The second completed measure extends $$\bar\mu$$ and has the same domain, so the two measures coincide. Thus completing twice changes neither the measurable sets nor the measure.

### Exercise 8

The forward implication holds: if the completed measure spaces are equal, their measures agree on the original $$\mathcal A$$, so $$\mu=\nu$$ there and their null sets are equal.

The converse is false even for finite measures. On the singleton $$X=\{x\}$$ with $$\mathcal A=\mathcal P(X)$$, let $$\mu(\{x\})=1$$ and $$\nu(\{x\})=2$$. Both null families are $$\{\varnothing\}$$ and both measures are already complete, but the completed measures differ on $$X$$.

Equality of null families does imply equality of the completed **domains**: the same null sets have the same subsets, and hence the construction $$\mathcal A_\mu=\{A\cup M:A\in\mathcal A,\ M\subset N\in\mathcal N_\mu\}$$ gives $$\mathcal A_\mu=\mathcal A_\nu$$. It does not imply equality of the measures on that domain.

### Exercise 9

Define, for $$A\in\mathcal A$$,

$$
\mu(A)=\begin{cases}0,&A\in\mathcal N,\\
\infty,&A\notin\mathcal N.\end{cases}
$$

Condition (i) gives $$\mu(\varnothing)=0$$. Let $$(A_j)$$ be disjoint and write $$A=\bigcup_j A_j$$. If every $$A_j\in\mathcal N$$, condition (ii) gives $$A\in\mathcal N$$ and both sides of countable additivity are zero. If some $$A_j\notin\mathcal N$$, then $$A\notin\mathcal N$$: otherwise (iii), applied to $$A_j\subset A$$, would give a contradiction. Both sides are then $$\infty$$. This proves countable additivity, and the definition gives $$\mathcal N_\mu=\mathcal N$$.

### Exercise 10

The countable–cocountable family $$\mathcal A$$ contains $$X$$ and is closed under complements. For a countable union, if all members are countable, the union is countable; if one is cocountable, the complement of the union is contained in its countable complement. Thus $$\mathcal A$$ is a $$\sigma$$-algebra.

The countable members form a family satisfying the three conditions of Exercise 9: they contain the empty set and are closed under countable unions and measurable subsets. The measure constructed there is exactly the prescribed one. Its null sets are the countable sets. Every subset of one is countable and therefore belongs to $$\mathcal A$$, so $$\mu$$ is complete. The assumption that $$X$$ is uncountable ensures, in particular, that $$\mu(X)=\infty$$.

### Exercise 11

**(a)(i)** Let $$A$$ be an atom and $$B\subset A$$ be measurable. If $$\mu(B)\ne0$$, the definition gives $$\mu(A\setminus B)=0$$. Additivity of the disjoint union $$A=B\mathbin{\dot\cup}(A\setminus B)$$ yields $$\mu(A)=\mu(B)$$, including when these values are infinite.

**(a)(ii)** Assume $$0<\mu(A)<\infty$$ and each measurable $$B\subset A$$ has measure zero or $$\mu(A)$$. In the second case, finite additivity gives $$\mu(A\setminus B)=\mu(A)-\mu(B)=0$$. Thus in either case the atom condition holds. Finiteness matters: when both sides have infinite measure, equality of their measures does not imply that the complement is null.

For a concrete example of the necessity of finiteness, take $$X=\{1,2\}$$ with the measure assigning $$\infty$$ to every nonempty subset. Every measurable subset has measure zero or $$\mu(X)=\infty$$, yet $$X$$ is not an atom because both singletons have infinite measure.

**(a)(iii)** Choose measurable sets $$E_j$$ of finite measure covering $$X$$. Since

$$
0<\mu(A)=\mu\left(\bigcup_j(A\cap E_j)\right)
\le\sum_j\mu(A\cap E_j),
$$

at least one $$A\cap E_j$$ has positive measure. Part (i) then gives $$\mu(A)=\mu(A\cap E_j)\le\mu(E_j)<\infty$$.

**(b) Counting measure.** Every singleton is an atom: its only subsets are itself and the empty set. A set containing distinct points $$x,y$$ is not an atom, because $$\{x\}$$ and its complement within the set both have positive counting measure. Therefore the atoms are exactly the singletons.

**The measure of Exercise 1.** Here a set has measure zero exactly when it is empty. A nonempty measurable set is an atom precisely when it has no nonempty proper measurable subset. The atoms are the nonempty members among $$A$$ and $$A^c$$. Indeed these are the minimal nonempty sets of the generated $$\sigma$$-algebra; if both are nonempty, $$X$$ splits into them and is not an atom. This also covers $$A=\varnothing$$ and $$A=X$$.

**The measure of Exercise 10.** The atoms are exactly the cocountable subsets of $$X$$. Such a set has measure $$\infty$$, since $$X$$ is uncountable. If $$B\subset A$$ is measurable, then either $$B$$ is countable and has measure zero, or $$B$$ is cocountable and $$A\setminus B\subset B^c$$ is countable and has measure zero. Countable sets have measure zero and cannot be atoms.

### Exercise 12

No. Let $$X=\{1,2\}$$, $$\mathcal A=\{\varnothing,X\}$$, and define $$\mu(\varnothing)=0$$ and $$\mu(X)=1$$. This is a measure space: a disjoint sequence contains at most one copy of $$X$$. Its only null set is empty, so it is complete. The set $$A=X$$ is an atom, since its only measurable subsets are $$\varnothing$$ and $$X$$. Nevertheless $$B=\{1\}\subset A$$ is not measurable.

Completeness makes all subsets of **null** sets measurable; it does not make all subsets of a positive atom measurable.

### Exercise 13

The sets $$A\cap N$$ and $$A\cap N^c$$ are measurable and partition $$A$$. By monotonicity, $$\mu(A\cap N)\le\mu(N)=0$$. Additivity therefore gives

$$
\mu(A)=\mu(A\cap N)+\mu(A\cap N^c)=\mu(A\cap N^c)>0.
$$

This argument remains valid if $$\mu(A)=\infty$$; in fact completeness is not needed for the stated measurable sets.
