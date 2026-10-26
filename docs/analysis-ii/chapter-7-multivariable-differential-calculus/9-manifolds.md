# Chapter VII — Multivariable Differential Calculus

## 9. Manifolds

These are detailed solutions to Exercises 1–18. Inline mathematics is enclosed by two dollar signs on each side of a formula; displayed calculations put the same delimiter on separate lines.

### Exercise 1

Let $$x,y\in H$$. Since $$\varphi$$ is an isometry and $$\varphi(0)=0$$,

$$
\|\varphi(x)\|=\|\varphi(x)-\varphi(0)\|=\|x\|.
$$

The real polarization identity therefore gives

$$
(\varphi(x)\mid\varphi(y))
=\frac{\|\varphi(x)\|^2+\|\varphi(y)\|^2-\|\varphi(x)-\varphi(y)\|^2}{2}
=(x\mid y).
$$

For additivity, expand the squared norm and use this inner-product identity:

$$
\begin{aligned}
\|\varphi(x+y)-\varphi(x)-\varphi(y)\|^2
={}&\|x+y\|^2+\|x\|^2+\|y\|^2\\
&-2(x+y\mid x)-2(x+y\mid y)+2(x\mid y)=0.
\end{aligned}
$$

Thus $$\varphi(x+y)=\varphi(x)+\varphi(y)$$. Similarly, for every $$\lambda\in\mathbb R$$,

$$
\|\varphi(\lambda x)-\lambda\varphi(x)\|^2
=\|\lambda x\|^2+\lambda^2\|x\|^2-2\lambda(\lambda x\mid x)=0,
$$

so $$\varphi(\lambda x)=\lambda\varphi(x)$$. This proves (a).

For every $$x,y\in H$$, the defining property of the adjoint yields

$$
(\varphi^*\varphi x\mid y)=(\varphi x\mid\varphi y)=(x\mid y).
$$

Hence $$\varphi^*\varphi=\operatorname{id}_H$$, proving (b). In particular, $$\varphi$$ is injective. Since $$H$$ is finite-dimensional and its domain and codomain have the same dimension, $$\varphi$$ is also surjective. It is a linear isometry, so $$\varphi\in\mathcal L_{\mathrm{aut}}(H)$$. If $$u=\varphi(x)$$ and $$v=\varphi(y)$$, then

$$
\|\varphi^{-1}(u)-\varphi^{-1}(v)\|=\|x-y\|=\|u-v\|.
$$

Thus $$\varphi^{-1}$$ is an isometry, proving (c).

### Exercise 2

The printed list contains a false equivalence: condition (iii), by itself, is not sufficient when $$n\ge2$$. For example,

$$
A=\operatorname{diag}(2,1/2,1,\ldots,1)
$$

has $$|\det A|=1$$, but it does not preserve lengths: $$|Ae_1|=2\ne1=|e_1|$$. Thus the five statements are not all equivalent as printed. For $$n=1$$, condition (iii) does imply that $$A$$ is an isometry.

The remaining conditions are equivalent. If $$A$$ is an isometry, then

$$
(Ax\mid Ay)=(x\mid y)\qquad(x,y\in\mathbb R^n),
$$

so $$A^{\mathsf T}A=I$$ and $$A\in O(n)$$. Conversely, $$A^{\mathsf T}A=I$$ implies

$$
|Ax|^2=(A^{\mathsf T}Ax\mid x)=|x|^2,
$$

so $$A$$ is an isometry. The columns of $$A$$ are orthonormal exactly when $$A^{\mathsf T}A=I$$. Since a square matrix with orthonormal columns is invertible, this identity also gives $$AA^{\mathsf T}=I$$, which says its rows are orthonormal. The reverse implication follows in the same way. Finally, taking determinants in $$A^{\mathsf T}A=I$$ gives $$|\det A|=1$$. This proves that (i), (ii), (iv), and (v) are equivalent and that they imply (iii).

For (b), matrix multiplication preserves orthogonality: if $$A,B\in O(n)$$, then

$$
(AB)^{\mathsf T}(AB)=B^{\mathsf T}A^{\mathsf T}AB=B^{\mathsf T}B=I.
$$

Also $$I\in O(n)$$ and $$A^{-1}=A^{\mathsf T}\in O(n)$$. Therefore $$O(n)$$ is a matrix group.

### Exercise 3

Let $$\psi\in\operatorname{Diff}^q(\mathbb R^n,\mathbb R^n)$$, and let $$M$$ be an $$m$$-dimensional $$C^q$$ submanifold. Fix $$p\in M$$. By the definition of submanifold, there are open neighborhoods $$U$$ of $$p$$ and $$V$$ of $$\varphi(p)$$ and a $$C^q$$ diffeomorphism $$\varphi:U\to V$$ such that

$$
\varphi(U\cap M)=V\cap(\mathbb R^m\times\{0\}).
$$

Set $$U'=\psi(U)$$ and define $$\widetilde\varphi=\varphi\circ\psi^{-1}:U'\to V$$. This is a $$C^q$$ diffeomorphism, and

$$
\widetilde\varphi\bigl(U'\cap\psi(M)\bigr)
=\varphi(U\cap M)
=V\cap(\mathbb R^m\times\{0\}).
$$

Thus $$\psi(M)$$ has the required local form around $$\psi(p)$$. As $$p$$ was arbitrary, $$\psi(M)$$ is an $$m$$-dimensional $$C^q$$ submanifold of $$\mathbb R^n$$.

### Exercise 4

Fix $$p\in M$$ and $$q\in N$$. Choose local diffeomorphisms $$\varphi$$ and $$\psi$$ that flatten the two submanifolds near these points:

$$
\varphi(U\cap M)=V\cap(\mathbb R^m\times\{0_{k-m}\}),\qquad
\psi(W\cap N)=Z\cap(\mathbb R^n\times\{0_{\ell-n}\}),
$$

where $$U\subseteq\mathbb R^k$$ and $$W\subseteq\mathbb R^\ell$$ are open neighborhoods, and $$V,Z$$ are open. The product map

$$
\Phi:U\times W\longrightarrow V\times Z,\qquad
\Phi(x,y)=(\varphi(x),\psi(y))
$$

is a $$C^q$$ diffeomorphism. Under the natural identification of coordinates,

$$
\Phi\bigl((U\times W)\cap(M\times N)\bigr)
=(V\times Z)\cap
\bigl(\mathbb R^{m+n}\times\{0_{k+\ell-m-n}\}\bigr).
$$

The points $$p,q$$ were arbitrary. Hence $$M\times N$$ is an $$(m+n)$$-dimensional $$C^q$$ submanifold of $$\mathbb R^{k+\ell}$$.

### Exercise 5

Identify $$\mathcal L(\mathbb R^n)$$ with the vector space $$\mathbb R^{n\times n}$$. Then

$$
\mathcal L_{\mathrm{aut}}(\mathbb R^n)
=\{A\in\mathbb R^{n\times n}:\det A\ne0\}.
$$

The determinant is continuous, so this set is open in $$\mathbb R^{n\times n}$$. Every open subset of a finite-dimensional vector space is a smooth submanifold of the same dimension. Therefore $$\mathcal L_{\mathrm{aut}}(\mathbb R^n)$$ is a smooth submanifold of $$\mathcal L(\mathbb R^n)$$, of dimension $$n^2$$.

### Exercise 6

Write the two components of $$f$$ as $$f_1,f_2$$. Their linear combination simplifies to

$$
f_2(x,y,z)-3f_1(x,y,z)=y-x^2.
$$

Thus $$f(x,y,z)=0$$ implies $$y=x^2$$. Substituting into $$f_1=0$$ gives $$z=x^3$$. Conversely, these two identities make both components of $$f$$ vanish. Hence

$$
f^{-1}(0)=\{(t,t^2,t^3):t\in\mathbb R\}.
$$

This is the graph of the smooth map $$t\mapsto(t^2,t^3)$$ from $$\mathbb R$$ to $$\mathbb R^2$$, so it is an embedded smooth curve. Explicitly, the ambient map

$$
\Phi(x,y,z)=(x,y-x^2,z-x^3)
$$

is a global smooth diffeomorphism, with inverse $$\Phi^{-1}(u,v,w)=(u,v+u^2,w+u^3)$$, and it sends $$f^{-1}(0)$$ to $$\mathbb R\times\{0\}\times\{0\}$$.

### Exercise 7

**(a)** The equations $$f(x,y,z,u)=0$$ are

$$
xz=y^2,\qquad yu=z^2,\qquad xu=yz.
$$

At a solution with $$x\ne0$$, the first and third equations give

$$
z=\frac{y^2}{x},\qquad u=\frac{y^3}{x^2}.
$$

Consequently the zero set in the open region $$x\ne0$$ is the graph

$$
(x,y)\longmapsto\left(x,y,\frac{y^2}{x},\frac{y^3}{x^2}\right),
\qquad (x,y)\in\{x\ne0\}.
$$

The second equation then holds automatically. At a solution with $$u\ne0$$, use the second and third equations instead:

$$
y=\frac{z^2}{u},\qquad x=\frac{z^3}{u^2}.
$$

The zero set in $$u\ne0$$ is therefore the graph

$$
(z,u)\longmapsto\left(\frac{z^3}{u^2},\frac{z^2}{u},z,u\right).
$$

Every nonzero solution belongs to one of these two regions. Indeed, if $$x=u=0$$, then $$xz=y^2$$ and $$yu=z^2$$ force $$y=z=0$$. The two graph descriptions cover $$f^{-1}(0)\setminus\{0\}$$ and show locally that it is a smooth two-dimensional submanifold of $$\mathbb R^4$$.

**(b)** Write the three rows of the derivative matrix $$Df(x,y,z,u)$$ as

$$
\begin{aligned}
r_1&=(2z,2u,2x,2y),\\
r_2&=(2u,-2z,-2y,2x),\\
r_3&=(-2x,-2y,2z,2u).
\end{aligned}
$$

Direct calculation shows that these rows are pairwise orthogonal and that

$$
|r_1|^2=|r_2|^2=|r_3|^2
=4(x^2+y^2+z^2+u^2).
$$

Thus $$Df$$ has rank $$3$$ at every nonzero point. If $$a\ne0$$, then $$0\notin g^{-1}(a)$$ because $$g(0)=0$$. Therefore every point of $$g^{-1}(a)$$ is a regular point of $$g$$, so the regular value theorem makes $$g^{-1}(a)$$ a $$4-3=1$$ dimensional smooth submanifold of $$\mathbb R^4$$, that is, an embedded curve.

### Exercise 8

Let

$$
F(x,y)=|x|^2-y^2.
$$

The answers are: (a) no, (b) yes, and (c) yes. To see this, note that

$$
DF(x,y)(h,s)=2(x\mid h)-2ys,
$$

so the gradient of $$F$$ vanishes only at the origin. The set in (c) is the regular level set with the origin removed, and (b) is an open subset of it. Both are smooth $$n$$-dimensional submanifolds.

More explicitly, (b) is the graph

$$
\{(x,|x|):x\in\mathbb R^n\setminus\{0\}\},
$$

and (c) is the regular level set $$F^{-1}(0)\setminus\{0\}$$. The gradient calculation gives a local submanifold chart at every point of (c).

The full cone $$K=F^{-1}(0)$$ is not a submanifold at the origin. Away from the origin it has dimension $$n$$, so if it were a manifold at the origin its dimension there would also have to be $$n$$. A sufficiently small neighborhood of the origin in $$K$$ with the origin removed has two connected components when $$n\ge2$$, one with $$y>0$$ and one with $$y<0$$. A punctured ball in an $$n$$-dimensional manifold is connected for $$n\ge2$$, a contradiction. When $$n=1$$, the punctured cone neighborhood has four components (the four rays $$y=\pm x$$), whereas a punctured one-dimensional ball has two. So the origin is not a manifold point in this case either.

### Exercise 9

Define $$q(x)=(x\mid Ax)$$. Since $$A$$ is symmetric,

$$
Dq(x)h=(h\mid Ax)+(x\mid Ah)=2(h\mid Ax),
\qquad \nabla q(x)=2Ax.
$$

If $$q(x)=1$$, then $$Ax\ne0$$; otherwise $$q(x)=0$$. Thus $$1$$ is a regular value of $$q$$. Its level set is a smooth hypersurface of $$\mathbb R^n$$, of dimension $$n-1$$.

For a sketch, diagonalize $$A$$ in an orthonormal basis. In dimension two the equation becomes

$$
\lambda_1 s^2+\lambda_2 t^2=1.
$$

Depending on the eigenvalues, this is an ellipse, a hyperbola, a pair of parallel lines, or the empty set. For example, positive eigenvalues give an ellipse, opposite signs give a hyperbola, and $$\lambda_1>0,\lambda_2=0$$ gives the two lines $$s=\pm1/\sqrt{\lambda_1}$$.

In dimension three the equation becomes

$$
\lambda_1 s_1^2+\lambda_2 s_2^2+\lambda_3 s_3^2=1.
$$

Its nonempty possibilities include ellipsoids, one- or two-sheeted hyperboloids, and their cylindrical degeneracies when an eigenvalue is zero. For instance, all positive eigenvalues give an ellipsoid; one positive and two negative eigenvalues give a two-sheeted hyperboloid; two positive and one negative give a one-sheeted hyperboloid. If all eigenvalues are nonpositive, the level set is empty. The regular-value argument applies to every nonempty case, including the degenerate cylinders and pairs of planes.

### Exercise 10

The determinant is multiplicative. Hence $$\det(AB)=\det A\det B=1$$ for $$A,B\in SO(n)$$; also $$I\in SO(n)$$ and $$\det(A^{-1})=(\det A)^{-1}=1$$. Thus $$SO(n)$$ is a subgroup of $$O(n)$$.

To compute its dimension, first consider

$$
\mathcal F:\mathbb R^{n\times n}\longrightarrow\mathbb R_{\mathrm{sym}}^{n\times n},
\qquad \mathcal F(A)=A^{\mathsf T}A.
$$

Then $$O(n)=\mathcal F^{-1}(I)$$ and

$$
D\mathcal F(A)B=A^{\mathsf T}B+B^{\mathsf T}A.
$$

If $$A\in O(n)$$ and $$S$$ is symmetric, choose $$B=\tfrac12 AS$$. This gives

$$
D\mathcal F(A)B=\tfrac12 S+\tfrac12 S^{\mathsf T}=S.
$$

Therefore $$I$$ is a regular value, and

$$
\dim O(n)=n^2-\frac{n(n+1)}2=\frac{n(n-1)}2.
$$

On $$O(n)$$, the determinant takes values in the discrete set $$\{-1,1\}$$. Consequently $$SO(n)=\{A\in O(n):\det A=1\}$$ is an open subset of $$O(n)$$, hence a smooth submanifold with the same dimension:

$$
\boxed{\dim SO(n)=\frac{n(n-1)}2.}
$$

### Exercise 11

**(a)** Repeatedly applying the recursion gives, for $$n\ge3$$,

$$
\begin{aligned}
f_n(y^1,\ldots,y^n)=y^1\bigg(&
\cos y^2\prod_{j=3}^{n}\sin y^j,\
\sin y^2\prod_{j=3}^{n}\sin y^j,\\
&\cos y^3\prod_{j=4}^{n}\sin y^j,\ \ldots,\
\cos y^{n-1}\sin y^n,\ \cos y^n\bigg).
\end{aligned}
$$

An empty product is understood to equal $$1$$. For $$n=2$$ this reduces to the given formula.

**(b)(i)** Write $$f_n(y)=y^1\omega_n(y^2,\ldots,y^n)$$. At dimension two,

$$
\omega_2=(\cos y^2,\sin y^2),\qquad |\omega_2|=1.
$$

The recursion gives

$$
\omega_{n+1}=(\omega_n\sin y^{n+1},\cos y^{n+1}),
$$

so $$|\omega_{n+1}|^2=|\omega_n|^2\sin^2y^{n+1}+\cos^2y^{n+1}=1$$ whenever $$|\omega_n|=1$$. Induction proves both $$|f_n(1,y^2,\ldots,y^n)|=1$$ and $$|f_n(y)|=|y^1|$$.

**(b)(ii)** For $$n=2$$, the usual polar parametrization with $$y^2\in(0,2\pi)$$ covers the plane except for the nonnegative first coordinate ray. This is precisely $$H_2$$. For the induction step, take $$x\notin H_{n+1}$$. Then $$r=|x|>0$$, and the first $$n$$ coordinates of $$x$$ are not all zero. Set

$$
y^{n+1}=\arccos(x_{n+1}/r)\in(0,\pi).
$$

The first $$n$$ coordinates have norm $$r\sin y^{n+1}$$. After dividing them by $$\sin y^{n+1}$$, the resulting vector has norm $$r$$ and lies outside $$H_n$$. By induction it has a unique representation by $$f_n$$ with first coordinate $$r$$. The recursion then represents the original vector by $$f_{n+1}$$. Conversely, the second coordinate of a point in the image is zero only when $$y^2=\pi$$, since all the sine factors $$\sin y^3,\ldots,\sin y^{n+1}$$ are positive. In that case the first coordinate is negative, so the image avoids $$H_{n+1}$$. This proves

$$
f_n(V_n)=\mathbb R^n\setminus H_n.
$$

The same induction also proves uniqueness of all the coordinates in $$V_n$$.

**(b)(iii)** Allowing the angular variables to take their boundary values supplies the missing cut and the polar axes. If the first coordinate $$y^1$$ is zero, the image is the origin regardless of the angles. For any nonzero point, choose its radius and the usual closed-range spherical angles recursively, taking the azimuth to be $$0$$ or $$2\pi$$ on the cut. These parameters belong to $$\overline{V_n}$$, so

$$
f_n(\overline{V_n})=\mathbb R^n.
$$

**(b)(iv)** Part (ii) and the uniqueness argument show that $$g_n=f_n|_{V_n}$$ is a continuous bijection from $$V_n$$ onto $$\mathbb R^n\setminus H_n$$. Part (v) below shows that its derivative is invertible at every point of $$V_n$$. The inverse function theorem therefore gives a continuous local inverse near every image point. Since the map is globally one-to-one, these local inverses agree with its set-theoretic inverse; hence the global inverse is continuous. Thus $$g_n$$ is topological, and together with its immersion property it is a smooth embedding.

**(b)(v)** For $$n=2$$, direct calculation gives

$$
\det Df_2(y^1,y^2)=y^1.
$$

For the induction step, write $$r=y^1$$, $$\theta=y^{n+1}$$, and $$f_n(r,z)=r\omega(z)$$ with $$|\omega(z)|=1$$. Differentiating $$\omega\cdot\omega=1$$ shows that every angular derivative of $$\omega$$ is perpendicular to $$\omega$$. In coordinates adapted to the radial direction $$\omega$$, the two columns corresponding to $$r,\theta$$ have radial and last-coordinate block

$$
\begin{pmatrix}
\sin\theta&r\cos\theta\\
\cos\theta&-r\sin\theta
\end{pmatrix},
\qquad\det=-r.
$$

Each of the other $$n-1$$ angular columns is scaled by $$\sin\theta$$ relative to the corresponding angular columns for $$f_n$$. The radial two-dimensional block contributes a factor $$-r$$. Equivalently, comparing the radial and angular factors gives

$$
\det Df_{n+1}(r,z,\theta)
=-r\sin^{n-1}\theta\,\det Df_n(r,z).
$$

Applying this recurrence inductively yields

$$
\det Df_n(y)
=(-1)^n(y^1)^{n-1}
\sin^{n-2}(y^n)\sin^{n-3}(y^{n-1})\cdots\sin(y^3).
$$

All factors are nonzero on $$V_n$$, as needed in (iv).

### Exercise 12

The cylindrical coordinate map is

$$
f(r,\varphi,z)=(r\cos\varphi,r\sin\varphi,z).
$$

For $$V=(0,\infty)\times(0,2\pi)\times\mathbb R$$, every point outside the closed half-plane $$H_3=\mathbb R_+\times\{0\}\times\mathbb R$$ has a unique radius $$r=\sqrt{x^2+y^2}>0$$, a unique angle $$\varphi\in(0,2\pi)$$, and the given third coordinate. Thus $$g=f|_V$$ is a bijection from $$V$$ onto $$\mathbb R^3\setminus H_3$$. Its inverse is smooth there, and

$$
\det Df(r,\varphi,z)
=\det\begin{pmatrix}
\cos\varphi&-r\sin\varphi&0\\
\sin\varphi&r\cos\varphi&0\\
0&0&1
\end{pmatrix}
=r>0.
$$

Therefore $$g$$ is a smooth embedding, proving (a).

For (b), $$g(1,\varphi,z)=(\cos\varphi,\sin\varphi,z)$$ is one-to-one on $$(0,2\pi)\times\mathbb R$$. Its inverse angle is continuous on the cylinder with the meridian $$\{(1,0,z):z\in\mathbb R\}$$ removed, and its derivative has independent columns

$$
(-\sin\varphi,\cos\varphi,0),\qquad(0,0,1).
$$

It is therefore a smooth embedding. Part (c) is the image calculation in (a). For (d), every point $$x\in\mathbb R^3$$ has cylindrical coordinates with $$r\ge0$$ and $$\varphi\in[0,2\pi]$$; when $$r=0$$ the angle is arbitrary. These parameters lie in $$\overline V$$, and thus $$f(\overline V)=\mathbb R^3$$.

### Exercise 13

**(a)** Define

$$
F(x,y,z)=\frac{x^2}{a^2}+\frac{y^2}{b^2}-1.
$$

Then $$M_{a,b}=F^{-1}(0)$$ and

$$
\nabla F(x,y,z)=\left(\frac{2x}{a^2},\frac{2y}{b^2},0\right).
$$

On $$M_{a,b}$$, $$x$$ and $$y$$ cannot both vanish, so this gradient is never zero. The regular value theorem shows that $$M_{a,b}$$ is a smooth hypersurface of $$\mathbb R^3$$, of dimension $$2$$.

**(b)** Each parametrization is one-to-one on $$W=(0,2\pi)\times\mathbb R$$: $$f_1$$ removes the elliptical generator at angle $$0$$, and $$f_2$$ removes the different generator at angle $$0$$ in its shifted parametrization. Their images cover the whole cylinder, so $$U_1\cup U_2=M_{a,b}$$. Their derivatives have rank two everywhere; for example,

$$
\partial_\varphi f_1=(-a\sin\varphi,b\cos\varphi,0),\qquad
\partial_z f_1=(0,0,1),
$$

and the first vector never vanishes. The same argument applies to $$f_2$$. The inverse angle coordinate is continuous on each image after removing its missing generator. Thus $$\varphi_j=(f_j|_W)^{-1}:U_j\to W$$ is a smooth chart, and the two charts form an atlas.

To compute the transition map, observe that

$$
f_2(\varphi,z)=f_1(\varphi+\pi/2,z),
$$

where the angle in the right-hand side is taken modulo $$2\pi$$. For $$\varphi\in(0,2\pi)\setminus\{3\pi/2\}$$, the representative in $$(0,2\pi)$$ is

$$
(\varphi_1\circ\varphi_2^{-1})(\varphi,z)
=
\begin{cases}
(\varphi+\pi/2,z),&0<\varphi<3\pi/2,\\
(\varphi-3\pi/2,z),&3\pi/2<\varphi<2\pi.
\end{cases}
$$

The excluded angle $$3\pi/2$$ is exactly where the point lies on the generator omitted from $$U_1$$. Both branches are smooth on the overlap, as required for a transition function.

### Exercise 14

Suppose an atlas of the nonempty compact manifold $$M$$ consisted of one chart $$\varphi: M\to V$$. Since this single chart covers $$M$$, its domain is all of $$M$$, and $$V$$ is a nonempty open subset of $$\mathbb R^m$$. The chart is a homeomorphism, so compactness of $$M$$ implies compactness of $$V$$. But a nonempty open subset of $$\mathbb R^m$$ cannot be compact when $$m\ge1$$: compact subsets are closed, so $$V$$ would be both open and closed in the connected space $$\mathbb R^m$$. It would have to equal $$\mathbb R^m$$, which is not compact. This contradiction proves that at least two charts are needed.

### Exercise 15

As printed, this exercise does not specify particular functions $$\rho$$ and $$\sigma$$ in Example 9.11(e), so the asserted conclusion cannot be deduced from the stated hypotheses. For a counterexample, take

$$
J=(-2\pi,2\pi),\qquad \rho(t)=2+\cos t,\qquad \sigma(t)=\sin t.
$$

Here $$\rho(t)>0$$ and $$(\dot\rho(t),\dot\sigma(t))=(-\sin t,\cos t)\ne(0,0)$$. The image of the rotation map is

$$
\left\{(x,y,z):
\bigl(\sqrt{x^2+y^2}-2\bigr)^2+z^2=1
\right\},
$$

the standard smooth torus. It is a smooth submanifold of $$\mathbb R^3$$; equivalently, it is the regular level set on $$\{x^2+y^2>0\}$$ of

$$
G(x,y,z)=\bigl(\sqrt{x^2+y^2}-2\bigr)^2+z^2.
$$

On the level set $$G=1$$ in $$\{x^2+y^2>0\}$$, its gradient can vanish only if $$z=0$$ and $$\sqrt{x^2+y^2}=2$$, which would give $$G=0$$. Thus $$1$$ is a regular value and the torus is a smooth submanifold.

Thus the requested conclusion cannot follow from the stated example alone. The warning in Example 9.11(e) does yield nonmanifold rotation images when the meridian crosses itself. For instance, with $$J=(-\pi/2,3\pi/2)$$, $$\rho(t)=2+\sin t$$, and $$\sigma(t)=\sin(2t)$$, the meridian has a transverse self-intersection at $$t=0$$ and $$t=\pi$$. Rotating it produces two distinct surface sheets with different tangent planes along the circle $$x^2+y^2=4,\ z=0$$. A submanifold has a unique tangent plane at every point, so this particular image is not a submanifold. The textbook needs to name such a choice of meridian for this to be the intended exercise.

### Exercise 16

Set $$u(t)=(-\sin t,\cos t)$$. Then $$|u(t)|=|u'(t)|=1$$ and $$(u(t)\mid u'(t))=0$$. Since $$g(t)=\sin(2t)u(t)$$,

$$
g'(t)=2\cos(2t)u(t)+\sin(2t)u'(t),
\qquad
|g'(t)|^2=4\cos^2(2t)+\sin^2(2t)>0.
$$

Thus $$g$$ is a smooth immersion.

To see injectivity, suppose $$g(s)=g(t)\ne0$$. The vectors $$u(s)$$ and $$u(t)$$ are unit vectors, and their scalar coefficients $$\sin(2s),\sin(2t)$$ are nonzero. Equality forces either $$u(s)=u(t)$$ with equal coefficients or $$u(s)=-u(t)$$ with opposite coefficients. The first case gives $$s=t$$ because the interval has length less than $$2\pi$$. The second would require $$s-t$$ to be an odd multiple of $$\pi$$, impossible because the interval $$(-\pi/4,\pi/2)$$ has length $$3\pi/4$$. Finally, $$g(t)=0$$ in this interval only for $$t=0$$. Hence $$g$$ is injective.

Although $$g(0)=0$$, points with parameter tending to the other endpoint also approach the origin:

$$
\lim_{t\uparrow\pi/2}g(t)=0.
$$

Their secant directions tend to the horizontal line, since $$g(t)/|g(t)|\to(-1,0)$$. In contrast, the branch through $$t=0$$ has tangent line spanned by $$g'(0)=(0,2)$$, the vertical line. A smooth embedded curve has a single tangent line at each point, and all secant directions of points approaching that point must approach that line. The two different limiting lines show that $$\operatorname{im}(g)$$ is not an embedded curve.

### Exercise 17

Using the stereographic projections from Example 9.14(d),

$$
\varphi_+(p)=\frac{p'}{1-p_{n+1}},
\qquad
\varphi_-(p)=\frac{p'}{1+p_{n+1}},
\qquad p=(p',p_{n+1})\in S^n,
$$

and

$$
\varphi_+^{-1}(x)=
\frac{(2x,\ |x|^2-1)}{1+|x|^2}.
$$

Substituting this point into $$\varphi_-$$ gives

$$
\begin{aligned}
(\varphi_-\circ\varphi_+^{-1})(x)
&=\frac{2x/(1+|x|^2)}
{1+(|x|^2-1)/(1+|x|^2)}\\
&=\frac{x}{|x|^2}.
\end{aligned}
$$

The transition function is therefore inversion $$x\mapsto x/|x|^2$$ on $$\mathbb R^n\setminus\{0\}$$. The origin is excluded because it corresponds under $$\varphi_+^{-1}$$ to the south pole, which is outside the domain of $$\varphi_-$$.

### Exercise 18

Let $$\varphi_\alpha:U_\alpha\to V_\alpha\subseteq\mathbb R^m$$ and $$\psi_\beta:W_\beta\to Z_\beta\subseteq\mathbb R^n$$ be charts from the given atlases. Their product map

$$
\varphi_\alpha\times\psi_\beta:
U_\alpha\times W_\beta\longrightarrow V_\alpha\times Z_\beta,
\qquad
(p,q)\longmapsto(\varphi_\alpha(p),\psi_\beta(q))
$$

is a homeomorphism onto an open subset of $$\mathbb R^{m+n}$$, since products of open sets are open. Its associated parametrization is

$$
(x,y)\longmapsto\bigl(g_\alpha(x),h_\beta(y)\bigr),
$$

where $$g_\alpha=i_M\circ\varphi_\alpha^{-1}$$ and $$h_\beta=i_N\circ\psi_\beta^{-1}$$. This map is $$C^q$$. Its derivative is block diagonal with blocks $$Dg_\alpha(x)$$ and $$Dh_\beta(y)$$; each block is injective, so the product derivative is injective. Thus each $$\varphi_\alpha\times\psi_\beta$$ is an $$(m+n)$$-dimensional $$C^q$$ chart of $$M\times N$$.

Finally, every $$(p,q)\in M\times N$$ belongs to some $$U_\alpha\times W_\beta$$ because the original chart domains cover $$M$$ and $$N$$. The product chart domains therefore cover $$M\times N$$, proving that the displayed family is an atlas.
