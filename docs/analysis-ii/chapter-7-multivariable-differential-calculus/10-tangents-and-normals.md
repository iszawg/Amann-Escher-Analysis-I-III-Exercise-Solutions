# Chapter VII — Multivariable Differential Calculus

## 10. Tangents and normals

These are detailed solutions to Exercises 1–14. Inline formulas use GitBook's double-dollar syntax, and displayed calculations use the same delimiters on separate lines.

### Exercise 1

Let $$F=f\circ g_n$$ be the expression of $$f$$ in the polar chart. The first fundamental matrix is the Gram matrix of the coordinate vectors:

$$
(g_n)_{jk}=\partial_j g_n\cdot\partial_k g_n.
$$

**(a)** For $$n=2$$, the parametrization is $$g_2(r,y^2)=(r\cos y^2,r\sin y^2)$$. Its coordinate vectors are

$$
\partial_r g_2=(\cos y^2,\sin y^2),\qquad
\partial_{y^2}g_2=(-r\sin y^2,r\cos y^2).
$$

They are orthogonal and have squared lengths $$1$$ and $$r^2$$. Hence

$$
[(g_2)_{jk}]=
\begin{pmatrix}
1&0\\
0&r^2
\end{pmatrix}.
$$

For $$n\ge3$$, the convention in the book orders the angles as $$y^2,\ldots,y^n$$, with $$y^2$$ the azimuthal angle. Differentiating the standard spherical-coordinate parametrization gives pairwise orthogonal coordinate vectors, with

$$
|\partial_r g_n|=1,\qquad
|\partial_{y^k}g_n|^2
=r^2\prod_{j=k+1}^{n}\sin^2(y^j)
\quad(2\le k\le n),
$$

where an empty product is $$1$$. Thus the matrix is diagonal:

$$
[(g_n)_{jk}]
=\operatorname{diag}\left(
1,\,
r^2\prod_{j=3}^{n}\sin^2(y^j),\,
r^2\prod_{j=4}^{n}\sin^2(y^j),\,
\ldots,\,
r^2\sin^2(y^n),\,
r^2
\right).
$$

This is the stated formula.

**(b)** By definition of the gradient on the submanifold, for a coordinate tangent vector with components $$\xi=(\xi^1,\ldots,\xi^n)$$,

$$
dF(y)\xi
=\sum_{j=1}^{n}\partial_jF(y)\,\xi^j
=\left\langle T_p\varphi_n(\nabla_p f),\xi\right\rangle_p.
$$

If $$\eta$$ is the coordinate vector of $$\nabla_p f$$, the last inner product is $$\eta^{\mathsf T}[(g_n)_{jk}]\xi$$. Since the matrix is symmetric, this identity for every $$\xi$$ gives

$$
[(g_n)_{jk}]\eta
=
\begin{pmatrix}
\partial_rF\\
\partial_{y^2}F\\
\vdots\\
\partial_{y^n}F
\end{pmatrix}.
$$

Therefore, for $$n=2$$,

$$
T_p\varphi_2(\nabla_p f)
=\left(\partial_rF,\frac{1}{r^2}\partial_{y^2}F\right).
$$

For $$n\ge3$$, its local-coordinate representation is

$$
T_p\varphi_n(\nabla_p f)
=\left(
\partial_rF,\,
\frac{\partial_{y^2}F}{r^2\prod_{j=3}^{n}\sin^2(y^j)},\,
\frac{\partial_{y^3}F}{r^2\prod_{j=4}^{n}\sin^2(y^j)},\,
\ldots,\,
\frac{\partial_{y^{n-1}}F}{r^2\sin^2(y^n)},\,
\frac{\partial_{y^n}F}{r^2}
\right).
$$

The denominators are nonzero on the coordinate domain, where the polar chart is regular.

### Exercise 2

Let $$J(y)=\partial g(y)$$ be the $$n\times m$$ derivative matrix. The fundamental matrix is the Gram matrix

$$
G(y)=[g_{jk}(y)]=J(y)^{\mathsf T}J(y),
\qquad
\sqrt{g(y)}=\sqrt{\det G(y)}.
$$

**(a)** If $$m=1$$, then $$J=\dot g$$ is a single column, so

$$
G=[\dot g\cdot\dot g]=[|\dot g|^2],
\qquad
\sqrt{\det G}=|\dot g|.
$$

**(b)** Let $$m=2$$ and $$n=3$$, and put $$a=\partial_1g$$ and $$b=\partial_2g$$. Then

$$
G=
\begin{pmatrix}
|a|^2&a\cdot b\\
a\cdot b&|b|^2
\end{pmatrix},
\qquad
\det G=|a|^2|b|^2-(a\cdot b)^2=|a\times b|^2.
$$

Writing $$g=(g^1,g^2,g^3)$$ and using the component formula for a cross product,

$$
|a\times b|^2
=
\left(\frac{\partial(g^2,g^3)}{\partial(y^1,y^2)}\right)^2
+
\left(\frac{\partial(g^3,g^1)}{\partial(y^1,y^2)}\right)^2
+
\left(\frac{\partial(g^1,g^2)}{\partial(y^1,y^2)}\right)^2.
$$

Taking square roots proves the asserted identity. The cross product is nonzero because $$g$$ is a parametrization, hence an immersion.

**(c)** For $$g(x)=(x,f(x))$$, its derivative has columns $$e_j+(\partial_jf)e_{n+1}$$. Consequently

$$
G=I_n+(\nabla f)(\nabla f)^{\mathsf T}.
$$

The rank-one matrix $$vv^{\mathsf T}$$ has eigenvalue $$|v|^2$$ in the direction of $$v$$ and eigenvalue $$0$$ on its orthogonal complement. Thus $$I_n+vv^{\mathsf T}$$ has determinant $$1+|v|^2$$ (also when $$v=0$$). With $$v=\nabla f(x)$$,

$$
\sqrt{g(x)}=\sqrt{\det G(x)}=\sqrt{1+|\nabla f(x)|^2}.
$$

### Exercise 3

At $$p=(0,1,0)$$, the sphere equation $$x^2+y^2+z^2=1$$ has normal vector $$p$$. Its tangent plane as a vector subspace is therefore

$$
T_pS^2=\{(a,b,c)\in\mathbb R^3:b=0\}
=\operatorname{span}\{e_1,e_3\}.
$$

The two requested charts give the following coordinate bases for this same space.

**(a)** In the spherical coordinates of Example 9.11(b),

$$
g(\varphi,\vartheta)
=(\cos\varphi\sin\vartheta,\sin\varphi\sin\vartheta,\cos\vartheta).
$$

The point corresponds to $$\varphi=\pi/2$$ and $$\vartheta=\pi/2$$. At these values,

$$
\partial_\varphi g=(-1,0,0),\qquad
\partial_\vartheta g=(0,0,-1).
$$

They span $$T_pS^2$$.

**(b)** Use the stereographic chart whose inverse is

$$
g_+(u,v)=
\left(
\frac{2u}{1+u^2+v^2},
\frac{2v}{1+u^2+v^2},
\frac{u^2+v^2-1}{1+u^2+v^2}
\right).
$$

The point $$p$$ has coordinates $$(u,v)=(0,1)$$. Direct differentiation gives

$$
\partial_u g_+(0,1)=e_1,\qquad
\partial_v g_+(0,1)=e_3.
$$

These again form a basis of $$T_pS^2$$.

### Exercise 4

Parametrize $$T^2_{2,1}$$ by

$$
\tau(t,\varphi)
=((2+\cos t)\cos\varphi,(2+\cos t)\sin\varphi,\sin t).
$$

For $$p=(\sqrt2,\sqrt2,1)$$, the radial coordinate in the first two components is $$2$$. Hence $$\cos t=0$$ and, from the third component, $$\sin t=1$$; we may take $$t=\pi/2$$. Also $$\varphi=\pi/4$$. At that parameter,

$$
\partial_t\tau
=\left(-\frac1{\sqrt2},-\frac1{\sqrt2},0\right),
\qquad
\partial_\varphi\tau=(-\sqrt2,\sqrt2,0).
$$

These independent vectors span the horizontal plane. Thus the tangent space, in tangent-part coordinates, is

$$
T_pT^2_{2,1}
=\{(p,(a,b,0)):a,b\in\mathbb R\}.
$$

The corresponding affine tangent plane in $$\mathbb R^3$$ is $$z=1$$.

### Exercise 5

Let $$M$$ be an $$m$$-dimensional $$C^q$$ submanifold of $$\mathbb R^n$$ and let $$(\varphi,U)$$ be a chart around $$p$$.

**(a)** Let $$M_0$$ be open in $$M$$ and fix $$x\in M_0$$. Choose a submanifold chart around $$x$$ that sends a neighborhood of $$M$$ to an open part of $$\mathbb R^m\times\{0\}$$. Since $$M_0$$ is relatively open, an ambient open neighborhood of $$x$$ can be chosen whose intersection with $$M$$ lies in $$M_0$$. Restricting the chart to this smaller neighborhood preserves the same local form. This works at every $$x\in M_0$$, so $$M_0$$ is an $$m$$-dimensional $$C^q$$ submanifold of $$\mathbb R^n$$.

Equivalently, restrict the atlas of $$M$$ to its open subspace $$M_0$$; all chart domains and transition maps remain open and $$C^q$$.

**(b)** Regard $$U$$ as the open subset of $$M$$ that it is, and let

$$
g=i_M\circ\varphi^{-1}:\varphi(U)\longrightarrow M\subseteq\mathbb R^n
$$

be the associated parametrization. The map $$\varphi:U\to\varphi(U)$$ is a $$C^q$$ diffeomorphism by the definition of chart. For $$x=\varphi(p)$$, the chart tangential $$T_p\varphi$$ is defined as the inverse of $$T_xg$$ onto its image $$T_pM$$. The chain rule gives

$$
T_p\varphi\circ T_xg
=T_x(\varphi\circ g)
=T_x\operatorname{id}_{\varphi(U)}
=\operatorname{id}_{T_x\varphi(U)}.
$$

Thus the inverse defining the chart tangential is exactly the tangential obtained by treating $$\varphi$$ as a map between the manifolds $$U$$ and $$\varphi(U)$$.

### Exercise 6

Identify $$\mathcal L(\mathbb R^n)$$ with $$\mathbb R^{n\times n}$$. The set

$$
GL(n)=\{B\in\mathbb R^{n\times n}:\det B\ne0\}
$$

is open because the determinant is continuous. Every tangent direction at an interior point is therefore allowed. In the book's attached-point notation,

$$
T_A GL(n)
=\{(A,H):H\in\mathbb R^{n\times n}\}.
$$

Its tangent-part space is all of $$\mathbb R^{n\times n}$$.

### Exercise 7

Define

$$
F:\mathbb R^{n\times n}\longrightarrow\mathbb R_{\mathrm{sym}}^{n\times n},
\qquad F(B)=B^{\mathsf T}B.
$$

Then $$O(n)=F^{-1}(I_n)$$. Differentiating at $$I_n$$ in the direction $$H$$ gives

$$
DF(I_n)H=H^{\mathsf T}+H.
$$

At every $$B\in O(n)$$, the derivative is

$$
DF(B)H=B^{\mathsf T}H+H^{\mathsf T}B.
$$

It is onto the symmetric matrices: for any symmetric $$S$$, choose $$H=BS/2$$. Then $$DF(B)H=S$$. Hence $$I_n$$ is a regular value and the regular-value theorem identifies the tangent space with the kernel at $$I_n$$:

$$
T_{I_n}O(n)
=\{(I_n,H):H^{\mathsf T}+H=0\}.
$$

The matrices satisfying this equation are precisely the skew-symmetric matrices.

### Exercise 8

The formula printed in the book,

$$
T_{I_n}SO(n)
=\{(I_n,H):\operatorname{tr}(H)=0\},
$$

is false when $$n\ge2$$. For example, $$H=\operatorname{diag}(1,-1,0,\ldots,0)$$ has trace zero but is not skew-symmetric. A tangent vector to $$SO(n)\subset O(n)$$ must also be tangent to $$O(n)$$, and Exercise 7 shows that its tangent part must satisfy $$H^{\mathsf T}+H=0$$.

The correct formula is

$$
T_{I_n}SO(n)
=\{(I_n,H):H^{\mathsf T}+H=0\}.
$$

To verify both inclusions, let $$\gamma(t)\in SO(n)$$ be a differentiable curve with $$\gamma(0)=I_n$$ and $$\gamma'(0)=H$$. Differentiating $$\gamma(t)^{\mathsf T}\gamma(t)=I_n$$ at $$0$$ yields $$H^{\mathsf T}+H=0$$. Conversely, if $$H^{\mathsf T}=-H$$, then

$$
\gamma(t)=e^{tH}
$$

satisfies $$\gamma(t)^{\mathsf T}\gamma(t)=I_n$$, since $$e^{tH^{\mathsf T}}e^{tH}=e^{-tH}e^{tH}=I_n$$. Moreover,

$$
\det\gamma(t)=\det(e^{tH})=e^{t\operatorname{tr}H}=1,
$$

because every skew-symmetric matrix has trace zero. Thus $$\gamma(t)\in SO(n)$$ and $$\gamma'(0)=H$$. This proves the corrected identity. For $$n=1$$ the printed and corrected spaces happen to agree, but the stated result fails in every dimension $$n\ge2$$.

### Exercise 9

**(a)** Since $$\psi\in\operatorname{Diff}^q(M,N)$$, both $$\psi$$ and $$\psi^{-1}$$ are differentiable. Apply the chain rule to the two identities $$\psi^{-1}\circ\psi=\operatorname{id}_M$$ and $$\psi\circ\psi^{-1}=\operatorname{id}_N$$:

$$
T_{\psi(p)}(\psi^{-1})\circ T_p\psi
=\operatorname{id}_{T_pM},
\qquad
T_p\psi\circ T_{\psi(p)}(\psi^{-1})
=\operatorname{id}_{T_{\psi(p)}N}.
$$

Thus $$T_p\psi$$ is a linear isomorphism, with inverse $$T_{\psi(p)}(\psi^{-1})$$.

**(b)** If $$M$$ and $$N$$ have dimensions $$m$$ and $$\ell$$, respectively, then $$T_pM$$ and $$T_{\psi(p)}N$$ have those finite dimensions. The isomorphism in (a) implies $$m=\ell$$.

### Exercise 10

**(a)** The map

$$
\Phi:S^1\times\mathbb R\longrightarrow
\{(x,y,z)\in\mathbb R^3:x^2+y^2=1\},
\qquad
\Phi((u,v),z)=(u,v,z)
$$

is well defined and smooth. Its inverse is $$\Phi^{-1}(x,y,z)=((x,y),z)$$, which is also smooth. Hence it is a diffeomorphism.

**(b)** Write a point of $$S^1\times S^1$$ as $$((\cos\varphi,\sin\varphi),(\cos t,\sin t))$$. Define

$$
\Phi((\cos\varphi,\sin\varphi),(\cos t,\sin t))
=((2+\cos t)\cos\varphi,(2+\cos t)\sin\varphi,\sin t).
$$

This is the standard parametrization of $$T^2_{2,1}$$. To give a smooth inverse, let $$\rho=\sqrt{x^2+y^2}$$ for a point $$(x,y,z)\in T^2_{2,1}$$. Since $$\rho=2+\cos t\ge1$$, it never vanishes, and

$$
\Phi^{-1}(x,y,z)
=\left(
\left(\frac{x}{\rho},\frac{y}{\rho}\right),
(\rho-2,z)
\right).
$$

The first factor lies in $$S^1$$, and the torus equation gives $$(\rho-2)^2+z^2=1$$, so the second factor also lies in $$S^1$$. The formulas are smooth and are inverse to one another. Thus the torus is diffeomorphic to $$S^1\times S^1$$.

**(c)** The scaling map

$$
\Phi:S^n\longrightarrow rS^n,\qquad \Phi(p)=rp
$$

is a smooth bijection with smooth inverse $$q\mapsto q/r$$. Hence $$S^n$$ and $$rS^n$$ are diffeomorphic for every $$r>0$$.

### Exercise 11

Parametrize the cylinder by $$p(\theta,z)=(\cos\theta,\sin\theta,z)$$. Let

$$
e_\theta=(-\sin\theta,\cos\theta,0),\qquad e_z=(0,0,1).
$$

At $$p=p(\theta,z)$$, these form an orthonormal basis of the tangent-part space of the cylinder. The map is

$$
\nu(p(\theta,z))=(\cos\theta,\sin\theta,0).
$$

It is smooth, and differentiation in the two tangent directions gives

$$
D\nu_p(e_\theta)=e_\theta,\qquad D\nu_p(e_z)=0.
$$

The target tangent space at $$\nu(p)$$ is also spanned by $$e_\theta,e_z$$. Relative to this common orthonormal basis, $$T_p\nu$$ has matrix

$$
\begin{pmatrix}
1&0\\
0&0
\end{pmatrix}.
$$

This matrix is symmetric and has eigenvalues $$1$$ and $$0$$.

### Exercise 12

As printed, the assumption $$f\in C^1(X,\mathbb R)$$ is insufficient. It only makes the unit normal continuous; it need not even be differentiable, so $$T_p\nu$$ may not exist. For example, with $$X=\mathbb R$$ and $$f(x)=|x|^{3/2}$$, the derivative $$f'(x)=(3/2)\operatorname{sgn}(x)\sqrt{|x|}$$ is continuous but is not differentiable at $$0$$. The unit normal

$$
\nu(x,f(x))
=\frac{(-f'(x),1)}{\sqrt{1+|f'(x)|^2}}
$$

is not differentiable at the point over $$x=0$$.

Here is the corrected regularity statement and the symmetry proof. If $$f\in C^\infty$$, then the displayed formula shows $$\nu\in C^\infty(M,S^n)$$. If only $$f\in C^2$$, then $$\nu$$ is $$C^1$$, which is enough to define and prove symmetry of $$T_p\nu$$.

Write

$$
q=\nabla f(x),\qquad
W=\sqrt{1+|q|^2},\qquad
H=D^2f(x),\qquad
J(u)=(u,q\cdot u).
$$

The vector $$J(u)$$ is tangent to the graph. The upward unit normal is $$N=(-q,1)/W$$. Differentiating in the parameter direction $$h\in\mathbb R^n$$ gives

$$
DN(x)h
=\frac{(-Hh,0)}{W}
-\frac{(-q,1)(q\cdot Hh)}{W^3}.
$$

Since $$J(u)\cdot N=0$$, the second term vanishes when paired with $$J(u)$$. Therefore

$$
\left\langle J(u),DN(x)h\right\rangle
=-\frac{u^{\mathsf T}Hh}{W}
=-\frac{h^{\mathsf T}Hu}{W}
=\left\langle J(h),DN(x)u\right\rangle,
$$

because the Hessian $$H$$ is symmetric. The tangent-part spaces of the graph at $$p$$ and of the sphere at $$\nu(p)$$ are both the orthogonal complement of $$\nu(p)$$ in $$\mathbb R^{n+1}$$. Thus this identity says precisely that $$T_p\nu$$ is symmetric under that natural identification.

### Exercise 13

The statement is false for a general noncompact graph, even when it is smooth. A global normal offset needs a uniform tubular radius; a smooth graph can have unbounded curvature and therefore arbitrarily small focal distances.

For a counterexample, take $$X=\mathbb R$$ and $$f(x)=\sin(x^2)$$. Its graph is a smooth curve. Write $$p(x)=(x,f(x))$$ and choose the upward unit normal $$N(x)=(-f'(x),1)/\sqrt{1+f'(x)^2}$$. Its signed curvature is

$$
\kappa(x)=\frac{f''(x)}{(1+f'(x)^2)^{3/2}}.
$$

If $$s$$ denotes arclength and $$T$$ the unit tangent, then $$dN/ds=-\kappa T$$. Consequently the normal-offset curve

$$
\Phi_\alpha(p)=p+\alpha N(p)
$$

has derivative with respect to arclength

$$
\frac{d}{ds}\Phi_\alpha
=(1-\alpha\kappa)T.
$$

For $$x_k=\sqrt{3\pi/2+2\pi k}$$, we have $$f'(x_k)=0$$, $$f''(x_k)=4x_k^2$$, and hence $$\kappa(x_k)=4x_k^2$$. Also $$\kappa'(x_k)=12x_k\ne0$$. Choose

$$
\alpha_k=\frac{1}{4x_k^2}.
$$

Then $$\alpha_k>0$$ and $$\alpha_k\to0$$, while $$1-\alpha_k\kappa(x_k)=0$$. The offset curve has a singular parametrization at $$x_k$$; because the zero of $$1-\alpha_k\kappa$$ is simple and $$\kappa(x_k)\ne0$$, its local image has an ordinary cusp. It is therefore not a smooth embedded hypersurface. Since such $$\alpha_k$$ occur arbitrarily close to zero, no $$\alpha_0>0$$ as in the exercise exists for this graph.

A valid global version follows, for example, if $$M$$ is a compact smooth embedded hypersurface. The tubular-neighborhood theorem then supplies an $$\varepsilon>0$$ such that

$$
M\times(-\varepsilon,\varepsilon)\longrightarrow\mathbb R^{n+1},
\qquad
(p,t)\longmapsto p+t\nu(p)
$$

is a diffeomorphism onto its image. Each slice $$p\mapsto p+\alpha\nu(p)$$ for $$|\alpha|<\varepsilon$$ is consequently an embedding, and its image is diffeomorphic to $$M$$. More generally, one may assume a uniform tubular radius (positive reach) directly.

### Exercise 14

Let $$Q=\operatorname{diag}(a^{-2},b^{-2},c^{-2})$$, so the ellipsoid is

$$
E=\{x\in\mathbb R^3:x^{\mathsf T}Qx\le1\}.
$$

We may take an inscribed rectangular box to be centered at the origin. Indeed, if its center is $$d$$ and its vertices are $$d+v$$, symmetry of $$E$$ puts both $$d+v$$ and $$-d+v$$ in $$E$$; their midpoint $$v$$ is in $$E$$ by convexity. Applying this to all vertices yields the centered box with the same side lengths, still contained in $$E$$.

Let its mutually orthogonal unit edge directions be $$u_1,u_2,u_3$$, and let its half-side lengths be $$h_1,h_2,h_3>0$$. Its vertices are

$$
v_\epsilon=\epsilon_1h_1u_1+\epsilon_2h_2u_2+\epsilon_3h_3u_3,
\qquad \epsilon_i\in\{-1,1\}.
$$

Every vertex satisfies $$v_\epsilon^{\mathsf T}Qv_\epsilon\le1$$. Average this inequality over the eight sign choices. All cross terms cancel, leaving

$$
\sum_{i=1}^3h_i^2c_i\le1,
\qquad c_i=u_i^{\mathsf T}Qu_i.
$$

The arithmetic-geometric mean inequality gives

$$
(h_1h_2h_3)^2c_1c_2c_3
=\prod_{i=1}^3(h_i^2c_i)
\le\left(\frac{\sum_{i=1}^3h_i^2c_i}{3}\right)^3
\le\frac1{27}.
$$

Let $$U=[u_1\ u_2\ u_3]$$. Since $$U$$ is orthogonal, the positive definite matrix $$U^{\mathsf T}QU$$ has diagonal entries $$c_1,c_2,c_3$$ and determinant

$$
\det(U^{\mathsf T}QU)=\det Q=\frac1{a^2b^2c^2}.
$$

Hadamard's determinant inequality therefore yields

$$
c_1c_2c_3\ge\frac1{a^2b^2c^2}.
$$

Combining the inequalities,

$$
h_1h_2h_3\le\frac{abc}{3\sqrt3}.
$$

The box volume is thus at most $$8abc/(3\sqrt3)$$. Equality is attained by the axis-parallel box with half-side lengths

$$
h_1=\frac a{\sqrt3},\qquad
h_2=\frac b{\sqrt3},\qquad
h_3=\frac c{\sqrt3}.
$$

Each vertex then satisfies

$$
\frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2}
=\frac13+\frac13+\frac13=1.
$$

Therefore the largest possible volume is

$$
\boxed{\frac{8abc}{3\sqrt3}}.
$$
