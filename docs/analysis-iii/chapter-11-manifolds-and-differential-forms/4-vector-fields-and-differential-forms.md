# Chapter XI — Manifolds and Differential Forms

## 4. Vector fields and differential forms

These solutions address Exercises 1–4. We write $$\iota_v\alpha$$ for the book's contraction $$v\mathbin{\lrcorner}\alpha$$. In Exercise 1, the inclusion of vector-field spaces needs to be interpreted as an inclusion into the space of fields **along** the submanifold; the printed global inclusion is not valid as stated.

### Exercise 1

Let $$i:N\hookrightarrow M$$ be the inclusion of a smooth submanifold into the manifold without boundary $$M$$. The correct canonical map is

$$
\mathcal V^k(N)\longrightarrow\Gamma^k(i^*TM),\qquad
v\longmapsto\bigl(p\longmapsto T_pi(v(p))\bigr).
$$

Here $$\Gamma^k(i^*TM)$$ denotes the $$C^k$$ sections of the pullback tangent bundle: its elements are vector fields **along** $$N$$, with values in $$T_pM$$ at points $$p\in N$$. At each point $$T_pi:T_pN\to T_pM$$ is injective, so the map above is injective. Its image consists exactly of the $$C^k$$ sections along $$N$$ whose values lie in $$T_pN$$. This gives the intended canonical identification.

To check regularity, choose local submanifold coordinates $$x=(x^1,\ldots,x^m)$$ on $$M$$ in which $$N$$ is represented by the first $$n$$ coordinates, with a half-space restriction in those coordinates if $$N$$ has boundary. Writing

$$
v=\sum_{j=1}^n v^j\frac\partial{\partial x^j}\Big|_N,
$$

the same field along $$N$$ has ambient coordinate components $$(v^1,\ldots,v^n,0,\ldots,0)$$. Thus its components are $$C^k$$. Conversely, an ambient-valued section along $$N$$ that is tangent to $$N$$ has its last $$m-n$$ components zero and therefore defines a $$C^k$$ vector field on $$N$$. The same reasoning applies for $$k=\infty$$.

The printed inclusion $$\mathcal V^k(N)\subset\mathcal V^k(M)$$ does **not** literally follow: the left-hand fields are defined only on $$N$$. Nor can every one necessarily be extended to all of $$M$$. For example, with $$M=\mathbb R$$ and the open submanifold $$N=(0,1)$$, the smooth field

$$
v(x)=\frac1x\frac\partial{\partial x}
$$

has no continuous extension to a field on $$\mathbb R$$, since its coefficient is unbounded near zero. Local extension near each point of $$N$$ is possible in the submanifold coordinates above; a global extension requires additional hypotheses and is not canonical in general.

### Exercise 2

The identity is pointwise and linear in both forms, so first let

$$
\alpha=\theta^1\wedge\cdots\wedge\theta^r,\qquad
\beta=\eta^1\wedge\cdots\wedge\eta^s.
$$

For covectors $$\xi^1,\ldots,\xi^t$$, expanding the determinant for the wedge along its first argument gives

$$
\iota_v(\xi^1\wedge\cdots\wedge\xi^t)
=\sum_{j=1}^t(-1)^{j-1}\xi^j(v)\,
\xi^1\wedge\cdots\wedge\widehat{\xi^j}\wedge\cdots\wedge\xi^t.
$$

Apply this to the ordered list of all $$\theta$$'s followed by all $$\eta$$'s. Terms in which the omitted factor is a $$\theta$$ sum to $$(\iota_v\alpha)\wedge\beta$$. For a factor $$\eta^j$$, its position in the combined list is $$r+j$$, so its sign is $$(-1)^r(-1)^{j-1}$$. These terms sum to $$(-1)^r\alpha\wedge(\iota_v\beta)$$. Hence

$$
\boxed{\iota_v(\alpha\wedge\beta)
=(\iota_v\alpha)\wedge\beta+(-1)^r\alpha\wedge(\iota_v\beta).}
$$

Every alternating form is a linear combination of decomposable forms in a basis, so the identity holds for arbitrary homogeneous forms. For an inhomogeneous $$\beta$$, apply it to each degree and add. For a 0-form $$f$$, the convention $$\iota_v f=0$$ makes the same formula valid when $$r=0$$ or $$s=0$$. All operations are smooth and the resulting pointwise identity is a global identity of forms.

### Exercise 3

Let $$\dim M=m$$ and $$\dim N=n$$. Suppose both are orientable and at least one has empty boundary, as in Example 4.17(b). We verify both the product atlas and the orientation claim.

Choose positively oriented charts $$(\varphi,U)$$ and $$(\psi,V)$$. Their product is a homeomorphism

$$
\varphi\times\psi:U\times V\longrightarrow\varphi(U)\times\psi(V),
\qquad (p,q)\longmapsto(\varphi(p),\psi(q)).
$$

The products cover $$M\times N$$. If the boundary-free factor is $$N$$, the image is open in $$\mathbb H^m\times\mathbb R^n$$, identified in the usual order with $$\mathbb H^{m+n}$$. If the boundary-free factor is $$M$$, a fixed permutation of the coordinates places the half-space coordinate of $$N$$ first. This identifies the image with an open subset of $$\mathbb H^{m+n}$$. When both factors are boundary-free, the images are open in Euclidean space. These conventions also cover zero-dimensional factors.

On the intersection of two product charts, before the fixed coordinate permutation the transition map is

$$
(\varphi_2\times\psi_2)\circ(\varphi_1\times\psi_1)^{-1}
=(\varphi_2\circ\varphi_1^{-1})\times(\psi_2\circ\psi_1^{-1}),
$$

with block-diagonal derivative. Consequently

$$
\det D\bigl((\varphi_2\times\psi_2)\circ(\varphi_1\times\psi_1)^{-1}\bigr)
=\det D(\varphi_2\circ\varphi_1^{-1})\,
 \det D(\psi_2\circ\psi_1^{-1})>0.
$$

The fixed coordinate permutation, when needed, conjugates every transition derivative by the same permutation matrix and does not change its determinant. Thus the product charts form an oriented atlas. Equivalently, if $$\mu$$ and $$\nu$$ are volume forms on the factors, then

$$
\pi_M^*\mu\wedge\pi_N^*\nu
$$

is a smooth nowhere-zero $$(m+n)$$-form: on a product basis its value is the product of the nonzero values of $$\mu$$ and $$\nu$$. This also proves orientability in the low-dimensional cases.

The boundary hypothesis ensures that the product is a manifold with boundary in the book's category. If both factors have boundary, corners can arise. For example, $$[0,\infty)\times[0,\infty)$$ has a corner at the origin; it is naturally a manifold with corners, and its tangent cone there is a quadrant rather than a linear image of a half-plane. Thus it is not a smooth embedded manifold with boundary at that point under the inherited smooth structure. Its product form is still nonvanishing in the manifold-with-corners setting, but that is a broader category than the one used in the example.

### Exercise 4

On a chart $$U$$ with coordinates $$x^1,\ldots,x^m$$ write

$$
\alpha=\sum_{j=1}^m a_j\,dx^j,\qquad
v=\sum_{j=1}^m v^j\frac\partial{\partial x^j}.
$$

Since the coordinate covectors and vectors are dual,

$$
\langle\alpha,v\rangle=\sum_{j=1}^m a_jv^j.
$$

Differentiating this scalar function and applying the ordinary product rule yields

$$
\boxed{d\langle\alpha,v\rangle
=\sum_{i=1}^m\sum_{j=1}^m
\left(v^j\frac{\partial a_j}{\partial x^i}
+a_j\frac{\partial v^j}{\partial x^i}\right)dx^i.}
$$

Equivalently, its value on $$w=\sum_i w^i\partial_i$$ is

$$
d\langle\alpha,v\rangle(w)
=\sum_{i,j}w^i\bigl(v^j\partial_i a_j+a_j\partial_i v^j\bigr).
$$

Although the derivatives of the individual coordinate components depend on the chart, their sum is the differential of the globally defined scalar pairing and therefore transforms as a 1-form.
