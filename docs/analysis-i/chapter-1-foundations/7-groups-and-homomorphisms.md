# Chapter I — Foundations

## 7. Groups and Homomorphisms

### Exercise 1

The left cosets of $$N$$ cover $$G$$ because $$g\in gN$$ for every $$g\in G$$. If two left cosets intersect, say $$gn=hm$$ with $$n,m\in N$$, then $$h=gnm^{-1}$$ and hence $$hN=gN$$; thus the cosets are equal or disjoint, so they partition $$G$$. For every $$g\in G$$, the map $$N\to gN$$ given by $$n\mapsto gn$$ is a bijection, so every coset has $$\operatorname{Num}(N)$$ elements. Since the set of cosets is $$G/N$$, counting the elements of this partition gives

$$
\operatorname{Num}(G)=\operatorname{Num}(G/N)\,\operatorname{Num}(N).
$$

In particular, $$\operatorname{Num}(N)$$ divides $$\operatorname{Num}(G)$$.

### Exercise 2

**(c)** Composition of bijections is associative, the identity is $$\operatorname{id}_X$$, and the inverse of $$f\in S_X$$ is its inverse function $$f^{-1}$$. Thus $$S_X$$ is a group. If $$X$$ has at least three elements, choose distinct $$x,y,z\in X$$ and let $$f$$ interchange $$x,y$$ while fixing the other elements, and let $$g$$ interchange $$y,z$$ while fixing the others. Then $$(f\circ g)(x)=y$$ but $$(g\circ f)(x)=z$$, so $$f\circ g\ne g\circ f$$ and $$S_X$$ is not Abelian in this case.

**(d)** Define the operation on $$G^X$$ pointwise by $$(fg)(x)=f(x)g(x)$$. Associativity follows at each $$x\in X$$ from associativity in $$G$$. The constant function $$x\mapsto e$$ is the identity, and the inverse of $$f$$ is the function $$x\mapsto f(x)^{-1}$$. Hence $$G^X$$ is a group. The same argument, coordinate by coordinate, proves that $$G^m$$ with the stated operation is a group.

### Exercise 3

If $$H_\alpha$$ are subgroups of $$G$$, their intersection contains the identity. If $$x,y\in\bigcap_\alpha H_\alpha$$, then every $$H_\alpha$$ contains $$xy$$ and $$x^{-1}$$; hence the intersection is a subgroup. This proves the claim in Example 7.3(b).

If each $$H_\alpha$$ is normal and $$x\in G$$, then for $$n\in\bigcap_\alpha H_\alpha$$ we have $$xnx^{-1}\in H_\alpha$$ for every $$\alpha$$. Thus $$xnx^{-1}\in\bigcap_\alpha H_\alpha$$, so the intersection is normal. With the usual convention that an empty intersection is $$G$$, the claim also holds for an empty family.

### Exercise 4

Let $$\varphi:G\to G'$$ be a homomorphism. Its image contains the identity $$e'=\varphi(e)$$. If $$\varphi(g),\varphi(h)\in\operatorname{im}(\varphi)$$, then

$$
\varphi(g)\varphi(h)=\varphi(gh),\qquad \varphi(g)^{-1}=\varphi(g^{-1}),
$$

so the image is closed under products and inverses. Therefore $$\operatorname{im}(\varphi)$$ is a subgroup of $$G'$$.

It need not be normal. For example, include $$H=\{e,(12)\}$$ into $$S_3$$. This is a homomorphism whose image is not normal: conjugating $$(12)$$ by $$(123)$$ gives a different transposition, which is not in $$H$$.

### Exercise 5

Let $$K=\varphi^{-1}(N')$$. Since $$N'$$ is a subgroup, $$K$$ contains the identity and is closed under products and inverses, so it is a subgroup of $$G$$. For $$g\in G$$ and $$k\in K$$, normality of $$N'$$ gives

$$
\varphi(gkg^{-1})=\varphi(g)\varphi(k)\varphi(g)^{-1}\in N'.
$$

Thus $$gkg^{-1}\in K$$, and $$K$$ is normal in $$G$$.

### Exercise 6

**(a)** For $$L_g:X\to X$$ defined by $$L_g(x)=g\cdot x$$, the action laws give

$$
L_g\circ L_{g^{-1}}=L_{gg^{-1}}=L_e=\operatorname{id}_X,
\qquad
L_{g^{-1}}\circ L_g=L_{g^{-1}g}=\operatorname{id}_X.
$$

So $$L_g$$ is bijective and its inverse is $$L_{g^{-1}}$$.

**(b)** Define $$x\sim y$$ to mean that $$y=g\cdot x$$ for some $$g\in G$$. Reflexivity follows from $$e\cdot x=x$$. If $$y=g\cdot x$$, then $$x=g^{-1}\cdot y$$, proving symmetry. If also $$z=h\cdot y$$, then $$z=h\cdot(g\cdot x)=(hg)\cdot x$$, proving transitivity. Thus belonging to the same orbit is an equivalence relation.

**(c)** For left multiplication, set $$h\cdot g:=hg$$ for $$h\in H$$ and $$g\in G$$. Then $$e\cdot g=g$$ and $$h_1\cdot(h_2\cdot g)=(h_1h_2)\cdot g$$. For conjugation, set $$h\cdot g:=hgh^{-1}$$. Its identity law is immediate, and

$$
h_1\cdot(h_2\cdot g)
=h_1(h_2gh_2^{-1})h_1^{-1}
=(h_1h_2)g(h_1h_2)^{-1}
=(h_1h_2)\cdot g.
$$

Both are actions of $$H$$ on $$G$$.

**(d)** There is a convention issue in the printed formula. If permutation multiplication is ordinary function composition, $$(\sigma\tau)(i)=\sigma(\tau(i))$$, then the stated coordinate rule $$(\sigma\cdot\alpha)_i=\alpha_{\sigma(i)}$$ does not satisfy the left-action law. For example, with $$\sigma=(12)$$, $$\tau=(23)$$, and $$\alpha=(1,2,3)$$, it gives $$\sigma\cdot(\tau\cdot\alpha)=(3,1,2)$$ but $$(\sigma\tau)\cdot\alpha=(2,3,1)$$.

The printed rule does define a left action if multiplication in $$S_m$$ is taken in the opposite order, $$(\sigma\tau)(i)=\tau(\sigma(i))$$. With ordinary function composition, the corresponding left-action rule is

$$
(\sigma\cdot\alpha)_i=\alpha_{\sigma^{-1}(i)},\qquad 1\le i\le m.
$$

Indeed, the identity permutation leaves every coordinate unchanged, and $$(\sigma\cdot(\tau\cdot\alpha))_i=\alpha_{\tau^{-1}(\sigma^{-1}(i))}=\alpha_{(\sigma\tau)^{-1}(i)}$$, as required.

### Exercise 7

The sequence of powers $$e,g,g^2,\ldots$$ lies in the finite set $$G$$, so two powers coincide: $$g^r=g^s$$ for some $$0\le r<s$$. Multiplying by $$g^{-r}$$ gives $$g^{s-r}=e$$. Therefore a least positive such exponent $$k$$ exists.

The cyclic subgroup $$\langle g\rangle=\{e,g,\ldots,g^{k-1}\}$$ has exactly $$k$$ elements. By Exercise 1, $$k$$ divides $$m=\operatorname{Num}(G)$$. Write $$m=qk$$. Then $$g^m=(g^k)^q=e$$.

### Exercise 8

**(a)** In the operation $$\diamond$$, the elements occur as powers of $$b$$ in the order $$e,b,a,c$$; in $$\oplus$$, the powers of $$a$$ occur in the order $$e,a,b,c$$. The map

$$
e\mapsto e,\qquad b\mapsto a,\qquad a\mapsto b,\qquad c\mapsto c
$$

matches corresponding powers of these generators, so it preserves the operation and is a bijection. Thus the two groups are isomorphic.

**(b)** In the first table every nonidentity element has order $$2$$. In the second table, $$b$$ has order $$4$$. An isomorphism preserves element orders, so these groups cannot be isomorphic.

**(c)** If a group of order $$4$$ has an element of order $$4$$, it is cyclic. Otherwise, all three nonidentity elements have order $$2$$. In that case, for any elements $$x,y$$, we have $$xy=(xy)^{-1}=y^{-1}x^{-1}=yx$$, so the group is Abelian and is the Klein four group. With $$e$$ fixed as the identity, there are three cyclic operation tables, distinguished by which of $$a,b,c$$ is the unique element of order $$2$$, and one Klein four group table, where all three have order $$2$$. The displayed tables include the Klein four group and two cyclic groups. The remaining structure is the cyclic group with powers

$$
e,\ a,\ c,\ b
$$

in that order. The four structures form two isomorphism classes: the cyclic groups are all isomorphic to $$C_4$$, and the all-involutions group is isomorphic to $$C_2\times C_2$$. (Here $$e$$ is held fixed as the identity, as indicated by its notation in the tables.)

### Exercise 9

In $$S_3$$, let $$\sigma=(12)$$ and $$\tau=(23)$$. Using ordinary composition, $$\sigma\tau$$ sends $$1\mapsto2$$, $$2\mapsto3$$, and $$3\mapsto1$$, so $$\sigma\tau=(123)$$. In the reverse order, $$\tau\sigma=(132)$$. Since these permutations differ, the operation in $$S_3$$ is not commutative and $$S_3$$ is not Abelian.

### Exercise 10

For $$(g_1,h_1),(g_2,h_2)\in G\times H$$,

$$
p\big((g_1,h_1)(g_2,h_2)\big)
=p(g_1g_2,h_1h_2)
=g_1g_2
=p(g_1,h_1)p(g_2,h_2),
$$

so $$p$$ is a homomorphism. It is surjective because $$p(g,e_H)=g$$ for every $$g\in G$$. Its kernel is $$H'=\{e_G\}\times H$$.

Define

$$
\overline p:(G\times H)/H'\to G,
\qquad
\overline p\big((g,h)H'\big)=g.
$$

This is well defined: $$(g,h)H'=(g',h')H'$$ exactly when $$g=g'$$. It is a homomorphism by the product rule in $$G\times H$$, and it is bijective because it is surjective and equality of images forces equality of cosets. Thus $$(G\times H)/H'\cong G$$.

### Exercise 11

Suppose first that $$G$$ is a group. Each $$L_g$$ is bijective with inverse $$L_{g^{-1}}$$. Also $$L_e=\operatorname{id}_G$$, and associativity gives

$$
L_g\circ L_h=L_{gh}.
$$

Therefore $$L$$ contains the identity permutation and is closed under composition and inverses, so it is a subgroup of $$S_G$$.

Conversely, suppose $$L=\{L_g:g\in G\}$$ is a subgroup of $$S_G$$. By assumption, every $$L_g$$ is a bijection. Since $$L_g\circ L_h\in L$$, there is some $$k\in G$$ with $$L_g\circ L_h=L_k$$. Evaluating both sides at the identity element gives $$k=gh$$, so

$$
L_g\circ L_h=L_{gh}.
$$

Evaluating at any $$x\in G$$ now yields $$g(hx)=(gh)x$$, proving associativity. Finally, surjectivity of $$L_g$$ gives some $$h\in G$$ with $$gh=e$$. Associativity gives $$g(hg)=(gh)g=eg=g=ge$$. Since $$L_g$$ is injective, $$hg=e$$. Thus every element has a two-sided inverse, and $$G$$ is a group.
