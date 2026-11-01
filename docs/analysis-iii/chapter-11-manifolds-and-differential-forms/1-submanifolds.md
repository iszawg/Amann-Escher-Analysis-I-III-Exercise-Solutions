# Chapter XI — Manifolds and Differential Forms

## 1. Submanifolds

These solutions address Exercises 1–10. As in the beginning of the section, $$M$$ and $$N$$ are smooth manifolds without boundary of dimensions $$m$$ and $$n$$, respectively. A separate symbol such as $$B$$ denotes a submanifold with boundary. We write $$\mathbb H^k=\{u\in\mathbb R^k:u_k\ge0\}$$; boundary means the intrinsic manifold boundary, not the topological boundary in an ambient space. Exercise 10 requires a correction under the book's definition of subordinate partitions of unity.

### Exercise 1

Let $$f:M\to N$$ be a submersion and $$p\in M$$. Surjectivity of $$T_pf$$ implies $$m\ge n$$. Choose charts around $$p$$ and $$f(p)$$, shrink the source chart so that its image under $$f$$ lies in the target chart, and write the resulting coordinate map as $$F:O\subset\mathbb R^m\to\mathbb R^n$$. At $$a$$, the coordinate of $$p$$, the derivative $$DF(a)$$ has rank $$n$$. After permuting the source coordinates, its first $$n$$ columns form an invertible matrix.

Define

$$
H(x_1,\ldots,x_m)=\bigl(F_1(x),\ldots,F_n(x),x_{n+1},\ldots,x_m\bigr).
$$

Its derivative at $$a$$ is invertible. The inverse function theorem therefore makes $$H$$ a diffeomorphism on a neighborhood of $$a$$. In the new source coordinates $$(z,w)=H(x)\in\mathbb R^n\times\mathbb R^{m-n}$$, the target coordinates of $$f$$ are exactly

$$
F(H^{-1}(z,w))=z.
$$

The formula is initially valid on an open neighborhood of $$H(a)$$. Shrink this neighborhood to a product of balls $$A\times D$$ and restrict the target chart to $$A$$. If one wants the domains written exactly as in the exercise, choose diffeomorphisms $$A\to\mathbb R^n$$ and $$D\to\mathbb R^{m-n}$$; use the first one in both source and target coordinates. The resulting local representative is the projection $$(x,y)\mapsto x$$ on all of $$\mathbb R^n\times\mathbb R^{m-n}$$. The zero-dimensional factors are understood as singletons.

### Exercise 2

Let $$f:M\to N$$ be an immersion and $$p\in M$$. Then $$m\le n$$. In source and target charts, write $$F=(F_1,F_2):O\subset\mathbb R^m\to\mathbb R^m\times\mathbb R^{n-m}$$, after permuting target coordinates so that $$DF_1(a)$$ is invertible at the coordinate $$a$$ of $$p$$. By the inverse function theorem, $$F_1$$ is a diffeomorphism on a smaller neighborhood. Use

$$
u=F_1(x),\qquad h(u)=F_2(F_1^{-1}(u))
$$

as the new source coordinate and the resulting graph function. On a product neighborhood of $$(F_1(a),F_2(a))$$, the target coordinate change

$$
(u,v)\longmapsto(u,v-h(u))
$$

is a smooth diffeomorphism, with inverse $$(u,w)\mapsto(u,w+h(u))$$. Hence the local expression of $$f$$ is $$u\mapsto(u,0)$$.

As in Exercise 1, choose a product of balls around the image point and reparametrize its two factors by Euclidean spaces, choosing the second reparametrization to send zero to zero. Restricting the source accordingly gives the canonical injection $$\mathbb R^m\to\mathbb R^m\times\mathbb R^{n-m}$$ exactly. This is a local assertion: an immersion need not be a global embedding.

### Exercise 3

Let $$f:M\to N$$ be a diffeomorphism. Its tangent map is an isomorphism, so $$\dim M=\dim N=m$$. Choose a chart $$(\psi,V)$$ of $$N$$ around $$f(p)$$ and set

$$
U=f^{-1}(V),\qquad \varphi=\psi\circ f|_U.
$$

Then $$(\varphi,U)$$ is a chart of $$M$$ and

$$
\psi\circ f\circ\varphi^{-1}=\operatorname{id}_{\psi(V)}.
$$

If desired, shrink $$V$$ so that $$\psi(V)$$ is a ball and compose both charts with the same diffeomorphism from that ball onto $$\mathbb R^m$$. The local representative is then the identity on $$\mathbb R^m$$.

### Exercise 4

Let $$\dim B=k$$. For $$(p,q)\in M\times B$$, take a chart of $$M$$ at $$p$$ and a submanifold chart of $$N$$ at $$q$$ for $$B$$. At a boundary point of $$B$$, these charts identify the pair locally with

$$
\mathbb R^m\times(\mathbb H^k\times\{0\})
\subset\mathbb R^m\times\mathbb R^n.
$$

A permutation of coordinates identifies this with $$\mathbb H^{m+k}\times\{0\}$$. At an interior point the same construction uses $$\mathbb R^k\times\{0\}$$. Thus $$M\times B$$ is an $$(m+k)$$-dimensional submanifold of $$M\times N$$ with boundary. The half-space coordinate vanishes exactly when $$q\in\partial B$$, giving

$$
\partial(M\times B)=M\times\partial B.
$$

In particular, if $$\partial B=\varnothing$$, the product has empty boundary. The absence of a boundary on $$M$$ matters: a product of two manifolds with boundary can have corners.

### Exercise 5

The interval $$[0,1]$$ is a one-dimensional manifold with boundary $$\{0,1\}$$. Swapping factors and applying Exercise 4 shows that the cylinder has dimension $$m+1$$ and

$$
\partial([0,1]\times M)=(\{0\}\times M)\cup(\{1\}\times M).
$$

The circle $$S^1$$ is a one-dimensional manifold without boundary, while the closed disk $$\overline B^2$$ is a two-dimensional manifold with boundary $$S^1$$. Hence the filled torus has dimension 3 and

$$
\partial(S^1\times\overline B^2)=S^1\times S^1.
$$

This boundary is a two-dimensional torus. These are product manifolds embedded in their product Euclidean spaces; any diffeomorphic geometric realization has the corresponding boundary image.

### Exercise 6

For $$r>0$$ define

$$
F:r\overline B^n\longrightarrow\overline B^n,\qquad F(x)=x/r.
$$

It is bijective, with inverse $$F^{-1}(y)=ry$$. Both are restrictions of smooth linear maps on all of $$\mathbb R^n$$, so they are smooth up to the boundary. Thus $$F$$ is a diffeomorphism of manifolds with boundary. In particular it maps $$rS^{n-1}$$ onto $$S^{n-1}$$. For $$n\ge1$$ the condition $$r>0$$ is essential: $$r=0$$ produces a singleton rather than an $$n$$-ball.

### Exercise 7

A perfect interval contains at least two points. Its finite endpoints may or may not be included; an infinite endpoint is never included. We give explicit smooth diffeomorphisms, whose inverses also extend smoothly near every included endpoint.

If the interval has no included endpoint, its target is $$(0,1)$$:

$$
\begin{array}{c|c}
J&J\longrightarrow(0,1)\\ \hline
(a,b)&(x-a)/(b-a)\\
(a,\infty)&(x-a)/(1+x-a)\\
(-\infty,b)&1/(1+b-x)\\
\mathbb R&\frac12+\frac1\pi\arctan x
\end{array}
$$

If exactly one endpoint is included, its target is $$[0,1)$$:

$$
\begin{array}{c|c}
J&J\longrightarrow[0,1)\\ \hline
[a,b)&(x-a)/(b-a)\\
(a,b]&(b-x)/(b-a)\\
[a,\infty)&(x-a)/(1+x-a)\\
(-\infty,b]&(b-x)/(1+b-x)
\end{array}
$$

For the compact interval $$[a,b]$$, the affine map $$(x-a)/(b-a)$$ is a diffeomorphism onto $$[0,1]$$. Here $$a<b$$ whenever both are finite. Each map has nonzero derivative on its domain, including at any included finite endpoint; the inverse function theorem and the displayed elementary formulas verify smoothness of the inverse. Thus every possible perfect interval is covered.

### Exercise 8

Use the metric induced by the ambient Euclidean space. Around any $$p\in B$$, a submanifold chart of the ambient manifold flattens $$B$$ to an open piece of $$\mathbb R^k\times\{0\}$$ or $$\mathbb H^k\times\{0\}$$. After shrinking to a sufficiently small Euclidean ball, the chart and its inverse are Lipschitz: their derivatives are bounded on suitable compact neighborhoods. Hence this local piece of $$B$$ is bi-Lipschitz equivalent to the corresponding Euclidean or half-space piece.

Both kinds of coordinate piece have Hausdorff dimension at most $$k$$. The manifold is second countable, so these local neighborhoods admit a countable subcover. Hausdorff dimension is invariant under bi-Lipschitz maps and the dimension of a countable union is the supremum of the dimensions. Consequently $$\dim_H B\le k$$.

For $$k\ge1$$, a nonempty coordinate neighborhood, including one centered at a boundary point, contains a nonempty open $$k$$-dimensional ball in its relative interior. Its inverse image is bi-Lipschitz to that ball and has Hausdorff dimension $$k$$. Thus $$\dim_H B\ge k$$. For $$k=0$$, the countable-cover argument gives the upper bound zero and any point gives the lower bound zero. Therefore

$$
\dim_H B=k.
$$

Nonemptiness is needed for the lower bound under the usual convention for the dimension of the empty set.

### Exercise 9

Let $$\dim B=k$$ and define

$$
G:B\longrightarrow M\times N,\qquad G(p)=(p,f(p)).
$$

This map is smooth. Its differential sends $$v\in T_pB$$ to $$(v,T_pf(v))$$, where $$T_pB$$ is identified with a subspace of $$T_pM$$. The first component shows that this differential is injective. The projection $$\operatorname{pr}_M$$ restricted to $$G(B)$$ is the continuous inverse of $$G$$. Hence $$G$$ is an embedding of the manifold with boundary $$B$$.

By the embedding theorem for submanifolds with boundary, $$G(B)=\operatorname{graph}(f)$$ is a $$k$$-dimensional submanifold of $$M\times N$$ with boundary, and $$G$$ is a diffeomorphism onto its image. Diffeomorphisms preserve intrinsic boundary, so

$$
\partial\operatorname{graph}(f)
=G(\partial B)=\{(p,f(p)):p\in\partial B\}.
$$

For an explicit local picture, flatten $$B$$ in $$M$$ to $$\{(u,v):u\in\mathbb H^k,\ v=0\}$$. In a target chart the coordinate expression of $$f$$ extends smoothly from the half-space to a neighborhood in $$\mathbb R^k$$. Subtracting this extension from the target coordinate straightens the graph to $$\{(u,0,0):u\in\mathbb H^k\}$$; its boundary is obtained by setting the last coordinate of $$u$$ to zero.

### Exercise 10

Under the book's stated definition, every partition function must have **compact** support contained in its assigned cover member. With that requirement, the exercise is false in general.

Take $$X=\mathbb R$$ and the one-element cover $$\mathcal U=\{\mathbb R\}$$. Let $$\mathcal V=\{(j-2,j+2):j\in\mathbb Z\}$$, a refinement of $$\mathcal U$$. Choose a nonnegative $$\eta\in C_c^\infty((-2,2))$$ that is positive on $$[-1,1]$$, and set

$$
S(x)=\sum_{j\in\mathbb Z}\eta(x-j),\qquad
\psi_j(x)=\frac{\eta(x-j)}{S(x)}.
$$

The sums are locally finite and $$S>0$$. Thus $$(\psi_j)$$ is a smooth partition of unity subordinate to $$\mathcal V$$, each support compact and contained in its assigned interval. A partition subordinate to the one-element cover $$\mathcal U$$ would have only one function, necessarily the constant 1, whose support is all of $$\mathbb R$$ and is not compact. Therefore no such partition exists under the printed definition. The same example also contradicts the unrestricted existence assertion in Proposition 1.20 when its compact-support requirement is read literally.

The standard coarsening proof works if subordination requires only $$\operatorname{supp}\psi_\beta\subset V_\beta$$, without requiring each support to be compact. Given an assignment $$j:B\to A$$ with $$V_\beta\subset U_{j(\beta)}$$, define

$$
\pi_\alpha=\sum_{\beta:j(\beta)=\alpha}\psi_\beta.
$$

Local finiteness makes every sum locally finite and smooth; near each point only finitely many $$\pi_\alpha$$ can be nonzero. Their sum is 1, and each is nonnegative. The locally finite union of the supports in a fiber is closed, so

$$
\operatorname{supp}\pi_\alpha
\subset\bigcup_{j(\beta)=\alpha}\operatorname{supp}\psi_\beta
\subset U_\alpha.
$$

This proves the corrected statement. With the book's stronger compact-support condition, the same construction is valid if, for example, every fiber of $$j$$ contains only finitely many indices with nonzero partition functions; then each resulting support lies in a finite union of compact supports inside $$U_\alpha$$.
