# Chapter I — Foundations

## 3. Functions

### Exercise 1

Let f : X → Y and g : Y → V be bijective. Their composition g ◦ f is bijective, and its inverse is
$$
h:=f^{-1}\circ g^{-1}:V\to X.
$$
Indeed,
$$
\begin{aligned}
h\circ(g\circ f)
&=f^{-1}\circ g^{-1}\circ g\circ f\\
&=f^{-1}\circ\operatorname{id}_Y\circ f\\
&=\operatorname{id}_X,
\end{aligned}
$$
and
$$
\begin{aligned}
(g\circ f)\circ h
&=g\circ f\circ f^{-1}\circ g^{-1}\\
&=g\circ\operatorname{id}_Y\circ g^{-1}\\
&=\operatorname{id}_V.
\end{aligned}
$$
Thus h is the inverse of g ◦ f, proving
$$
(g\circ f)^{-1}=f^{-1}\circ g^{-1}.
$$

### Exercise 2

Let f : X → Y. In the statements about complements, Aᶜ is relative to X and A′ᶜ is relative to Y. We use the set-valued map notation for images and preimages.

**(i)** If y ∈ f(A), then y = f(x) for some x ∈ A. Since A ⊆ B, the same x belongs to B, so y ∈ f(B). Hence f(A) ⊆ f(B).

**(ii)** For y ∈ Y, membership in either side means that y = f(x) for some x belonging to at least one Aα. Therefore
$$
f\left(\bigcup_{\alpha\in I}A_\alpha\right)
=\bigcup_{\alpha\in I}f(A_\alpha).
$$

**(iii)** If y ∈ f(⋂α Aα), then y = f(x) for some x in every Aα. Thus y belongs to every f(Aα), and
$$
f\left(\bigcap_{\alpha\in I}A_\alpha\right)
\subseteq\bigcap_{\alpha\in I}f(A_\alpha).
$$

**(iv)** Take y ∈ f(X) ∖ f(A). There is an x ∈ X with f(x) = y. This x cannot be in A, since that would put y in f(A). Hence x ∈ Aᶜ and y ∈ f(Aᶜ). Therefore
$$
f(A^{\mathrm c})\supseteq f(X)\setminus f(A).
$$

For the preimage statements, let A′, B′ ⊆ Y.

**(i′)** If x ∈ f⁻¹(A′), then f(x) ∈ A′ ⊆ B′, so x ∈ f⁻¹(B′). Thus f⁻¹(A′) ⊆ f⁻¹(B′).

**(ii′)** For x ∈ X, f(x) belongs to ⋃α A′α exactly when it belongs to at least one A′α. Consequently
$$
f^{-1}\left(\bigcup_{\alpha\in I}A'_\alpha\right)
=\bigcup_{\alpha\in I}f^{-1}(A'_\alpha).
$$

**(iii′)** For x ∈ X, f(x) belongs to ⋂α A′α exactly when it belongs to every A′α. Hence
$$
f^{-1}\left(\bigcap_{\alpha\in I}A'_\alpha\right)
=\bigcap_{\alpha\in I}f^{-1}(A'_\alpha).
$$

**(iv′)** An element x ∈ X belongs to f⁻¹(A′ᶜ) exactly when f(x) ∉ A′, which is exactly when x ∉ f⁻¹(A′). Complements on the right are relative to X, so
$$
f^{-1}((A')^{\mathrm c})=\bigl(f^{-1}(A')\bigr)^{\mathrm c}.
$$

Finally, for C ⊆ V,
$$
\begin{aligned}
x\in(g\circ f)^{-1}(C)
&\iff g(f(x))\in C\\
&\iff f(x)\in g^{-1}(C)\\
&\iff x\in f^{-1}\bigl(g^{-1}(C)\bigr).
\end{aligned}
$$
Thus, as set-valued preimage maps, (g ◦ f)⁻¹ = f⁻¹ ◦ g⁻¹.

The one-way inclusions above can all be strict. For a single example, let X = {0,1}, Y = {a}, and let f : X → Y be the constant function. For (i), take A = ∅ and B = {0}; then f(A) = ∅ ⊊ {a} = f(B). For (iii), take A₁ = {0} and A₂ = {1}; then
$$
f(A_1\cap A_2)=\varnothing\subsetneq\{a\}=f(A_1)\cap f(A_2).
$$
For (iv), take A = {0}; then
$$
f(X)\setminus f(A)=\varnothing\subsetneq\{a\}=f(A^{\mathrm c}).
$$
For (i′), take A′ = ∅ and B′ = {a}; then f⁻¹(A′) = ∅ ⊊ X = f⁻¹(B′).

### Exercise 3

Let f : X → Y and g : Y → V.

**(a)** If f and g are injective and g(f(x)) = g(f(x′)), injectivity of g gives f(x) = f(x′), and injectivity of f then gives x = x′. Thus g ◦ f is injective.

If f and g are surjective, take any v ∈ V. Choose y ∈ Y with g(y) = v, and then choose x ∈ X with f(x) = y. It follows that (g ◦ f)(x) = v, so g ◦ f is surjective.

**(b)** If h : Y → X satisfies h ◦ f = idX, then f(x) = f(x′) implies
$$
x=h(f(x))=h(f(x'))=x',
$$
so f is injective.

Conversely, suppose f is injective and X is nonempty. Fix x₀ ∈ X and define h : Y → X by sending each y in f(X) to its unique preimage under f, and each y outside f(X) to x₀. This is well defined by injectivity and gives h(f(x)) = x for every x ∈ X. Therefore h ◦ f = idX.

There is a boundary exception in the statement as printed: if X = ∅ and Y ≠ ∅, the empty function f : ∅ → Y is injective, but no function h : Y → ∅ exists. Thus the claimed equivalence holds when X is nonempty; for X = ∅ it holds only when Y = ∅.

**(c)** If f ◦ h = idY for some h : Y → X, then for every y ∈ Y we have y = f(h(y)), so f is surjective.

Conversely, if f is surjective, choose for each y ∈ Y an element h(y) ∈ X such that f(h(y)) = y. Then h : Y → X is a function and f ◦ h = idY. This choice of one preimage for each y uses the usual axiom-of-choice convention for arbitrary sets.

### Exercise 4

We prove the three conditions equivalent.

**(a) implies (b).** For every A ⊆ X, A ⊆ f⁻¹(f(A)) by definition. If f is injective and x ∈ f⁻¹(f(A)), then f(x) = f(a) for some a ∈ A. Injectivity gives x = a ∈ A. Thus
$$
f^{-1}(f(A))=A.
$$

**(b) implies (a).** Assume the equality holds for every A ⊆ X. If f(x) = f(y), take A = {x}. Then y ∈ f⁻¹(f({x})) = {x}, so y = x. Hence f is injective.

**(a) implies (c).** The inclusion f(A ∩ B) ⊆ f(A) ∩ f(B) always holds. If y ∈ f(A) ∩ f(B), then y = f(a) = f(b) for some a ∈ A and b ∈ B. Injectivity implies a = b, so y ∈ f(A ∩ B). Therefore
$$
f(A\cap B)=f(A)\cap f(B).
$$

**(c) implies (a).** Suppose f(A ∩ B) = f(A) ∩ f(B) for all A,B ⊆ X. If distinct x,y ∈ X had f(x) = f(y), choose A = {x} and B = {y}. Then f(A ∩ B) = ∅, whereas f(A) ∩ f(B) = {f(x)}, a contradiction. Thus f is injective.

### Exercise 5

For the projection prₖ : X₁ × ··· × Xₙ → Xₖ and y ∈ Xₖ, its fiber is the set of tuples whose kth coordinate is y:
$$
\operatorname{pr}_k^{-1}(y)
=X_1\times\cdots\times X_{k-1}\times\{y\}\times X_{k+1}\times\cdots\times X_n.
$$
Equivalently, it is {x ∈ X₁ × ··· × Xₙ : xₖ = y}. If y ∉ Xₖ, the corresponding fiber is empty.

### Exercise 6

Define Φ : 𝒫(X) → {0,1}ˣ by sending each A to its characteristic function:
$$
\Phi:\mathcal P(X)\to\{0,1\}^X,\qquad A\mapsto\chi_A.
$$

To prove injectivity, suppose Φ(A) = Φ(B). Then the characteristic functions of A and B agree at every x ∈ X. Since a characteristic function equals 1 exactly on its set, x ∈ A iff x ∈ B for every x; hence A = B.

To prove surjectivity, let φ : X → {0,1} be any function and set
$$
A:=\{x\in X:\varphi(x)=1\}.
$$
For every x ∈ X, φ(x) = 1 exactly when x ∈ A, and otherwise φ(x) = 0. Therefore φ is the characteristic function of A, so φ = Φ(A). Thus Φ is surjective, and hence bijective.

### Exercise 7

Let i : A → X be the inclusion, so i(a) = a.

**(a)** For every a ∈ A,
$$
(f\circ i)(a)=f(i(a))=f(a)=(f|_A)(a).
$$
The two functions have the same domain and codomain and agree at every input, so f|A = f ◦ i.

**(b)** By the definition of preimage under the restriction,
$$
\begin{aligned}
(f|_A)^{-1}(B)
&=\{a\in A:f(a)\in B\}\\
&=A\cap\{x\in X:f(x)\in B\}\\
&=A\cap f^{-1}(B).
\end{aligned}
$$
