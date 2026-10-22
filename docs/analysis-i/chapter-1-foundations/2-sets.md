# Chapter I — Foundations

## 2. Sets

Complements below are taken relative to the ambient set under discussion. For the family identities, the index sets are nonempty, as in the book's definition of a family.

### Exercise 1

Assume X ⊆ Y and Y ⊆ Z. To prove X ⊆ Z, take any x ∈ X. The first inclusion gives x ∈ Y, and the second then gives x ∈ Z. Since x was arbitrary, X ⊆ Z.

### Exercise 2

Let X,Y,Z be subsets of a common set. Each identity follows by testing membership of an arbitrary element x.

**(i) Commutativity.**

x ∈ X ∪ Y ⇔ (x ∈ X) ∨ (x ∈ Y) ⇔ (x ∈ Y) ∨ (x ∈ X) ⇔ x ∈ Y ∪ X,

and similarly,

x ∈ X ∩ Y ⇔ (x ∈ X) ∧ (x ∈ Y) ⇔ (x ∈ Y) ∧ (x ∈ X) ⇔ x ∈ Y ∩ X.

Thus X ∪ Y = Y ∪ X and X ∩ Y = Y ∩ X.

**(ii) Associativity.**

x ∈ X ∪ (Y ∪ Z) ⇔ (x ∈ X) ∨ (x ∈ Y) ∨ (x ∈ Z) ⇔ x ∈ (X ∪ Y) ∪ Z,

and

x ∈ X ∩ (Y ∩ Z) ⇔ (x ∈ X) ∧ (x ∈ Y) ∧ (x ∈ Z) ⇔ x ∈ (X ∩ Y) ∩ Z.

Hence both operations are associative.

**(iii) Distributivity.**

x ∈ X ∪ (Y ∩ Z) ⇔ (x ∈ X) ∨ ((x ∈ Y) ∧ (x ∈ Z)) ⇔ ((x ∈ X) ∨ (x ∈ Y)) ∧ ((x ∈ X) ∨ (x ∈ Z)) ⇔ x ∈ (X ∪ Y) ∩ (X ∪ Z),

by distributivity of logical “or” over “and”. The other identity follows from the dual logical law:

x ∈ X ∩ (Y ∪ Z) ⇔ (x ∈ X) ∧ ((x ∈ Y) ∨ (x ∈ Z)) ⇔ ((x ∈ X) ∧ (x ∈ Y)) ∨ ((x ∈ X) ∧ (x ∈ Z)) ⇔ x ∈ (X ∩ Y) ∪ (X ∩ Z).

**(iv) Characterizing inclusion.** If X ⊆ Y, then every element of Y is already in X ∪ Y, so X ∪ Y = Y; every element of X is in X ∩ Y, so X ∩ Y = X. Conversely, if X ∪ Y = Y, then x ∈ X implies x ∈ X ∪ Y = Y, hence X ⊆ Y. If X ∩ Y = X, then x ∈ X implies x ∈ X ∩ Y, and therefore x ∈ Y. Thus

X ⊆ Y ⇔ X ∪ Y = Y ⇔ X ∩ Y = X.

### Exercise 3

Let {A\_α; α ∈ I} and {B\_β; β ∈ J} be families of subsets of a fixed set. We verify each identity by element membership.

**(i) Associativity for indexed families.** For intersections,

x ∈ (⋂{A\_α : α ∈ I}) ∩ (⋂{B\_β : β ∈ J}) ⇔ (∀ α ∈ I: x ∈ A\_α) ∧ (∀ β ∈ J: x ∈ B\_β) ⇔ ∀ (α,β) ∈ I × J: x ∈ A\_α ∩ B\_β ⇔ x ∈ ⋂{A\_α ∩ B\_β : (α,β) ∈ I × J}.

For unions,

x ∈ (⋃{A\_α : α ∈ I}) ∪ (⋃{B\_β : β ∈ J}) ⇔ (∃ α ∈ I: x ∈ A\_α) ∨ (∃ β ∈ J: x ∈ B\_β) ⇔ ∃ (α,β) ∈ I × J: x ∈ A\_α ∪ B\_β ⇔ x ∈ ⋃{A\_α ∪ B\_β : (α,β) ∈ I × J}.

The second equivalence uses the fact that both index sets are nonempty.

**(ii) Distributivity for indexed families.** For the first identity, if x belongs to every A\_α, or to every B\_β, it belongs to every A\_α ∪ B\_β. Conversely, suppose x ∈ A\_α ∪ B\_β for every pair (α,β). If x did not belong to every A\_α, choose α₀ with x ∉ A\_{α₀}. If it also did not belong to every B\_β, choose β₀ with x ∉ B\_{β₀}. Then x ∉ A\_{α₀} ∪ B\_{β₀}, a contradiction. Therefore x belongs to every A\_α or to every B\_β, proving

(⋂{A\_α : α ∈ I}) ∪ (⋂{B\_β : β ∈ J}) = ⋂{A\_α ∪ B\_β : (α,β) ∈ I × J}.

For the other identity, membership on the left means that x ∈ A\_{α₀} for some α₀ and x ∈ B\_{β₀} for some β₀. This is equivalent to x ∈ A\_{α₀} ∩ B\_{β₀} for some pair, so

(⋃{A\_α : α ∈ I}) ∩ (⋃{B\_β : β ∈ J}) = ⋃{A\_α ∩ B\_β : (α,β) ∈ I × J}.

**(iii) De Morgan's laws.** By the definition of complement,

x ∈ (⋃{A\_α : α ∈ I})ᶜ ⇔ ¬ (∃ α ∈ I: x ∈ A\_α) ⇔ ∀ α ∈ I: x ∉ A\_α ⇔ x ∈ ⋂{A\_αᶜ : α ∈ I}.

Similarly,

x ∈ (⋂{A\_α : α ∈ I})ᶜ ⇔ ¬ (∀ α ∈ I: x ∈ A\_α) ⇔ ∃ α ∈ I: x ∉ A\_α ⇔ x ∈ ⋃{A\_αᶜ : α ∈ I}.

### Exercise 4

Assume X and Y are nonempty and X × Y = Y × X. Choose y₀ ∈ Y. For any x ∈ X, the pair (x,y₀) belongs to X × Y = Y × X, so its first coordinate x lies in Y. Thus X ⊆ Y.

Now choose x₀ ∈ X. For any y ∈ Y, (y,x₀) ∈ Y × X = X × Y, so y ∈ X. Hence Y ⊆ X, and therefore X = Y.

Conversely, if X = Y, then their Cartesian products with themselves agree, so X × Y = Y × X. We have proved

X × Y = Y × X ⇔ X = Y.

### Exercise 5

All complements are relative to X.

**(a)** By double complementation, (Aᶜ)ᶜ = A.

**(b)** A set and its complement are disjoint, so A ∩ Aᶜ = ∅.

**(c)** Every element of X lies either in A or in Aᶜ, so A ∪ Aᶜ = X.

**(d)** Distributing the intersection gives

(Aᶜ ∪ B) ∩ A ∩ Bᶜ = (Aᶜ ∩ A ∩ Bᶜ) ∪ (B ∩ A ∩ Bᶜ) = ∅.

Thus (Aᶜ ∪ B) ∩ (A ∩ Bᶜ) = ∅.

**(e)** If x ∈ Aᶜ, it is already in the union. If x ∉ Aᶜ, then x ∈ A. In that case either x ∈ B, or x ∈ Bᶜ; in the latter case x ∈ A ∩ Bᶜ. Thus every x ∈ X belongs to (Aᶜ ∪ B) ∪ (A ∩ Bᶜ), and the expression equals X.

**(f)** Since Aᶜ ∪ Bᶜ = (A ∩ B)ᶜ,

(Aᶜ ∪ Bᶜ) ∩ (A ∪ B) = ((A ∪ B) ∖ (A ∩ B)) = (A ∖ B) ∪ (B ∖ A).

This is the symmetric difference of A and B.

**(g)** An element of A ∩ B belongs to neither Aᶜ nor Bᶜ. Hence

(Aᶜ ∪ Bᶜ) ∩ (A ∩ B) = ∅.

### Exercise 6

Every member A of 𝒫(X) is a subset of X, so

⋃{A : A ∈ 𝒫(X)} ⊆ X.

Conversely, for each x ∈ X, the singleton {x} is in 𝒫(X), so x belongs to the union. Therefore

⋃{A : A ∈ 𝒫(X)} = X.

The empty set is itself in 𝒫(X). Any element in the intersection of all members of 𝒫(X) would therefore have to belong to ∅, which is impossible. Thus

⋂{A : A ∈ 𝒫(X)} = ∅.

### Exercise 7

Let X,A ⊆ U and Y,B ⊆ V.

**(a)** Assume A × B ≠ ∅ and A × B ⊆ X × Y. Then A and B are both nonempty. Fix a ∈ A, and choose b₀ ∈ B. Since (a,b₀) ∈ X × Y, its first coordinate gives a ∈ X. Hence A ⊆ X. Fixing b ∈ B and choosing a₀ ∈ A similarly gives b ∈ Y, so B ⊆ Y.

Conversely, if A ⊆ X and B ⊆ Y, then every (a,b) ∈ A × B also belongs to X × Y. Therefore

A × B ≠ ∅ ⇒ (A × B ⊆ X × Y ⇔ A ⊆ X and B ⊆ Y).

**(b)** A pair (u,v) belongs to the left side exactly when

((u ∈ X ∧ v ∈ Y) ∨ (u ∈ A ∧ v ∈ Y)),

which is equivalent to u ∈ X ∪ A and v ∈ Y. This is precisely membership in (X ∪ A) × Y. Hence

(X × Y) ∪ (A × Y) = (X ∪ A) × Y.

**(c)** A pair (u,v) lies in (X × Y) ∩ (A × B) exactly when u ∈ X ∩ A and v ∈ Y ∩ B. Thus

(X × Y) ∩ (A × B) = (X ∩ A) × (Y ∩ B).

**(d)** A pair (u,v) lies in (X × Y) ∖ (A × B) exactly when u ∈ X, v ∈ Y, and it is not the case that both u ∈ A and v ∈ B. The last condition is equivalent to u ∉ A or v ∉ B. Therefore

(X × Y) ∖ (A × B) = ((X ∖ A) × Y) ∪ (X × (Y ∖ B)).

### Exercise 8

Let {A\_α; α ∈ I} and {B\_β; β ∈ J} be families of sets.

**(a)** A pair (x,y) belongs to (⋂{A\_α : α ∈ I}) × (⋂{B\_β : β ∈ J}) exactly when x ∈ A\_α for every α ∈ I and y ∈ B\_β for every β ∈ J. This is equivalent to saying that (x,y) ∈ A\_α × B\_β for every (α,β) ∈ I × J. Hence

(⋂{A\_α : α ∈ I}) × (⋂{B\_β : β ∈ J}) = ⋂{A\_α × B\_β : (α,β) ∈ I × J}.

**(b)** A pair (x,y) belongs to (⋃{A\_α : α ∈ I}) × (⋃{B\_β : β ∈ J}) exactly when there are indices α₀ ∈ I and β₀ ∈ J with x ∈ A\_{α₀} and y ∈ B\_{β₀}. Equivalently, (x,y) belongs to A\_{α₀} × B\_{β₀} for some pair of indices. Thus

(⋃{A\_α : α ∈ I}) × (⋃{B\_β : β ∈ J}) = ⋃{A\_α × B\_β : (α,β) ∈ I × J}.
