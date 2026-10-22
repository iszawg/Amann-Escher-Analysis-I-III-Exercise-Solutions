# Chapter I — Foundations

## 2. Sets

Complements below are taken relative to the ambient set under discussion. For the family identities, the index sets are nonempty, as in the book's definition of a family.

### Exercise 1

Assume X ⊆ Y and Y ⊆ Z. To prove X ⊆ Z, take any x ∈ X. The first inclusion gives x ∈ Y, and the second then gives x ∈ Z. Since x was arbitrary, X ⊆ Z.

### Exercise 2

Let X,Y,Z be subsets of a common set. Each identity follows by testing membership of an arbitrary element x.

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
Thus X ∪ Y = Y ∪ X and X ∩ Y = Y ∩ X.

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

**(iv) Characterizing inclusion.** If X ⊆ Y, then every element of Y is already in X ∪ Y, so X ∪ Y = Y; every element of X is in X ∩ Y, so X ∩ Y = X. Conversely, if X ∪ Y = Y, then x ∈ X implies x ∈ X ∪ Y = Y, hence X ⊆ Y. If X ∩ Y = X, then x ∈ X implies x ∈ X ∩ Y, and therefore x ∈ Y. Thus
$$
X\subseteq Y
\iff X\cup Y=Y
\iff X\cap Y=X.
$$

### Exercise 3

Let A be a family of subsets of a fixed set, indexed by I, and B a family indexed by J. We verify each identity by element membership.

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

**(ii) Distributivity for indexed families.** For the first identity, if x belongs to every set in family A, or to every set in family B, then x belongs to at least one of the sets in families A and B for every pair of indices. Conversely, suppose that for every α ∈ I and β ∈ J, x belongs to at least one of the set A indexed by α and the set B indexed by β. If x did not belong to every set in family A, choose α₀ ∈ I such that x is not in the set A indexed by α₀. If it also did not belong to every set in family B, choose β₀ ∈ J such that x is not in the set B indexed by β₀. Then x belongs to neither set for the pair (α₀, β₀), a contradiction. Therefore x belongs to every set in family A or to every set in family B, proving
$$
\left(\bigcap_{\alpha\in I}A_\alpha\right)
\cup
\left(\bigcap_{\beta\in J}B_\beta\right)
=
\bigcap_{(\alpha,\beta)\in I\times J}
\left(A_\alpha\cup B_\beta\right).
$$

For the other identity, membership on the left means that x belongs to some set in family A and some set in family B. Choose indices α₀ and β₀ for these sets. This is equivalent to saying that x belongs to both selected sets for some pair of indices, so
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

Assume X and Y are nonempty and X × Y = Y × X. Choose y₀ ∈ Y. For any x ∈ X, the pair (x,y₀) belongs to X × Y = Y × X, so its first coordinate x lies in Y. Thus X ⊆ Y.

Now choose x₀ ∈ X. For any y ∈ Y, (y,x₀) ∈ Y × X = X × Y, so y ∈ X. Hence Y ⊆ X, and therefore X = Y.

Conversely, if X = Y, then their Cartesian products with themselves agree, so X × Y = Y × X. We have proved
$$
X\times Y=Y\times X
\iff X=Y.
$$

### Exercise 5

All complements are relative to X.

**(a)** By double complementation, (Aᶜ)ᶜ = A.

**(b)** A set and its complement are disjoint, so A ∩ Aᶜ = ∅.

**(c)** Every element of X lies either in A or in Aᶜ, so A ∪ Aᶜ = X.

**(d)** Distributing the intersection gives
$$
\begin{aligned}
(A^{\mathrm c}\cup B)\cap A\cap B^{\mathrm c}
&=(A^{\mathrm c}\cap A\cap B^{\mathrm c})
  \cup(B\cap A\cap B^{\mathrm c})\\
&=\varnothing.
\end{aligned}
$$
Thus (Aᶜ ∪ B) ∩ (A ∩ Bᶜ) = ∅.

**(e)** If x ∈ Aᶜ, it is already in the union. If x ∉ Aᶜ, then x ∈ A. In that case either x ∈ B, or x ∈ Bᶜ; in the latter case x ∈ A ∩ Bᶜ. Thus every x ∈ X belongs to (Aᶜ ∪ B) ∪ (A ∩ Bᶜ), and
$$
(A^{\mathrm c}\cup B)\cup(A\cap B^{\mathrm c})=X.
$$

**(f)** Since Aᶜ ∪ Bᶜ = (A ∩ B)ᶜ,
$$
\begin{aligned}
(A^{\mathrm c}\cup B^{\mathrm c})\cap(A\cup B)
&=(A\cup B)\setminus(A\cap B)\\
&=(A\setminus B)\cup(B\setminus A).
\end{aligned}
$$
This is the symmetric difference of A and B.

**(g)** An element of A ∩ B belongs to neither Aᶜ nor Bᶜ. Hence
$$
(A^{\mathrm c}\cup B^{\mathrm c})\cap(A\cap B)=\varnothing.
$$

### Exercise 6

Every member A of 𝒫(X) is a subset of X, so
$$
\bigcup_{A\in\mathcal P(X)}A\subseteq X.
$$

Conversely, for each x ∈ X, the singleton {x} is in 𝒫(X), so x belongs to the union. Therefore
$$
\bigcup_{A\in\mathcal P(X)}A=X.
$$

The empty set is itself in 𝒫(X). Any element in the intersection of all members of 𝒫(X) would therefore have to belong to ∅, which is impossible. Thus
$$
\bigcap_{A\in\mathcal P(X)}A=\varnothing.
$$

### Exercise 7

Let X,A ⊆ U and Y,B ⊆ V.

**(a)** Suppose A × B ≠ ∅. If A × B ⊆ X × Y, then A and B are both nonempty. Fix a ∈ A, and choose b₀ ∈ B. Since (a,b₀) ∈ X × Y, its first coordinate gives a ∈ X. Hence A ⊆ X. Fixing b ∈ B and choosing a₀ ∈ A similarly gives b ∈ Y, so B ⊆ Y.

Conversely, if A ⊆ X and B ⊆ Y, then every (a,b) ∈ A × B also belongs to X × Y. Therefore
$$
A\times B\subseteq X\times Y
\iff
A\subseteq X\text{ and }B\subseteq Y.
$$
This equivalence is asserted under the assumption A × B ≠ ∅. If A × B = ∅, the product inclusion holds vacuously, even when one of the factor inclusions fails.

**(b)** A pair (u,v) belongs to the left side exactly when
$$
\begin{aligned}
(u,v)\in(X\times Y)\cup(A\times Y)
&\iff \bigl((u\in X)\land(v\in Y)\bigr)
      \lor\bigl((u\in A)\land(v\in Y)\bigr)\\
&\iff (u\in X\cup A)\land(v\in Y).
\end{aligned}
$$
This is precisely membership in (X ∪ A) × Y. Hence
$$
(X\times Y)\cup(A\times Y)=(X\cup A)\times Y.
$$

**(c)** A pair (u,v) lies in the left side exactly when
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

**(d)** A pair (u,v) lies in (X × Y) ∖ (A × B) exactly when u ∈ X, v ∈ Y, and it is not the case that both u ∈ A and v ∈ B. The last condition is equivalent to u ∉ A or v ∉ B. Therefore
$$
(X\times Y)\setminus(A\times B)
=\bigl((X\setminus A)\times Y\bigr)
\cup\bigl(X\times(Y\setminus B)\bigr).
$$

### Exercise 8

Let A be a family of sets indexed by I, and B a family of sets indexed by J.

**(a)** A pair (x,y) belongs to the product of the intersection of all sets in family A and the intersection of all sets in family B exactly when x belongs to every set in family A and y belongs to every set in family B. This is equivalent to saying that, for every α ∈ I and β ∈ J, (x,y) belongs to the product of the set A indexed by α and the set B indexed by β. Hence
$$
\left(\bigcap_{\alpha\in I}A_\alpha\right)
\times
\left(\bigcap_{\beta\in J}B_\beta\right)
=
\bigcap_{(\alpha,\beta)\in I\times J}
\left(A_\alpha\times B_\beta\right).
$$

**(b)** A pair (x,y) belongs to the product of the union of all sets in family A and the union of all sets in family B exactly when there are indices α₀ ∈ I and β₀ ∈ J such that x belongs to the set A indexed by α₀ and y belongs to the set B indexed by β₀. Equivalently, (x,y) belongs to the product of those two sets for some pair of indices. Thus
$$
\left(\bigcup_{\alpha\in I}A_\alpha\right)
\times
\left(\bigcup_{\beta\in J}B_\beta\right)
=
\bigcup_{(\alpha,\beta)\in I\times J}
\left(A_\alpha\times B_\beta\right).
$$
