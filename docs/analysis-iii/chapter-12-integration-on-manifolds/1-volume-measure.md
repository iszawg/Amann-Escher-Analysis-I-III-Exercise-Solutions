# Chapter XII — Integration on Manifolds

## 1. Volume measure

These solutions address Exercises 1–16. Unless another metric is specified, submanifolds of Euclidean space carry the induced metric, and $$\lambda_M$$ is their Riemann–Lebesgue volume measure. Several printed formulas in Exercises 5, 8, 14, and 16 need corrections; the statements and counterexamples below distinguish these from the intended results.

### Exercise 1

Let $$f:M\to N$$ be a $$C^1$$ diffeomorphism. In a pair of compatible charts its coordinate representative and its inverse are locally Lipschitz, since their derivatives are continuous. Locally Lipschitz maps send Lebesgue-null sets to null sets; a countable cover extends this to all chart pieces. Hence $$f$$ and $$f^{-1}$$ both send manifold null sets to null sets.

If $$A$$ is measurable, write it as a Borel set together with a subset of a null set, using completeness of the volume measure. The homeomorphism $$f$$ sends the Borel part to a Borel set, and the remaining part to a subset of a null set. Thus $$f(A)$$ is measurable. Applying the same argument to $$f^{-1}$$ gives the converse. No assumption that $$f$$ is an isometry is needed.

### Exercise 2

For $$F(t,\varphi)=(\cosh t\cos\varphi,\cosh t\sin\varphi,\sinh t)$$, direct differentiation gives

$$
\langle F_t,F_t\rangle=\cosh(2t),\quad
\langle F_\varphi,F_\varphi\rangle=\cosh^2t,\quad
\langle F_t,F_\varphi\rangle=0.
$$

Thus, for the orientation induced by the ordered coordinates $$(t,\varphi)$$,

$$
F^*\omega_H=\cosh t\sqrt{\cosh(2t)}\,dt\wedge d\varphi.
$$

The opposite orientation changes the sign, while the volume density is unchanged. The region $$0<z<1$$ is $$0<t<\operatorname{arsinh}1$$. With $$z=\sinh t$$,

$$
\begin{aligned}
\operatorname{vol}\{0<z<1\}
&=2\pi\int_0^1\sqrt{1+2z^2}\,dz\\
&=\pi\left(\sqrt3+\frac{\operatorname{arsinh}\sqrt2}{\sqrt2}\right).
\end{aligned}
$$

The missing angular seam has zero area.

### Exercise 3

Parametrize $$Z=S^1\times(-1,1)$$ by $$(\cos\varphi,\sin\varphi,z)$$. The area density is 1, and the squared Euclidean norm of the point is $$1+z^2$$. Consequently

$$
\int_Z|x|^2\,d\lambda_Z
=\int_0^{2\pi}\int_{-1}^1(1+z^2)\,dz\,d\varphi
=\frac{16\pi}{3}.
$$

### Exercise 4

Use $$x=\sin\theta\cos\varphi$$, $$y=\sin\theta\sin\varphi$$, $$z=\cos\theta$$ and $$d\lambda_{S^2}=\sin\theta\,d\theta\,d\varphi$$. Then

$$
\begin{aligned}
\int_{S^2}x^2y^2z^2\,d\lambda_{S^2}
&=\left(\int_0^{2\pi}\cos^2\varphi\sin^2\varphi\,d\varphi\right)
\left(\int_0^\pi\sin^5\theta\cos^2\theta\,d\theta\right)\\
&=\frac\pi4\cdot\frac{16}{105}=\boxed{\frac{4\pi}{105}}.
\end{aligned}
$$

For the second integral use symmetry and the substitution $$u=\cos\theta$$, giving $$2\int_0^1(1-u^2)^2u^2\,du=16/105$$.

### Exercise 5

Assume $$R>0$$. Interpret the solid as the part of the ball inside the cylinder: $$V_R=\{x^2+y^2+z^2\le R^2,\ x^2+y^2\le Rx\}$$. With $$x=\rho\cos\varphi$$, $$y=\rho\sin\varphi$$, its projection is

$$
-\frac\pi2\le\varphi\le\frac\pi2,\qquad 0\le\rho\le R\cos\varphi.
$$

The vertical height inside the sphere is $$2\sqrt{R^2-\rho^2}$$. Therefore

$$
\begin{aligned}
\operatorname{vol}(V_R)
&=\int_{-\pi/2}^{\pi/2}\int_0^{R\cos\varphi}
2\rho\sqrt{R^2-\rho^2}\,d\rho\,d\varphi\\
&=\frac{2R^3}{3}\int_{-\pi/2}^{\pi/2}(1-|\sin\varphi|^3)\,d\varphi
=\frac{2R^3}{3}\left(\pi-\frac43\right).
\end{aligned}
$$

The literal intersection of the cylinder surface $$Z_R$$ with the sphere is a curve, and has zero **two-dimensional** area. The printed value in (ii) is instead the area of the spherical part of the boundary of $$V_R$$, the two caps bounded by that curve. On the sphere use

$$
(x,y,z)=R(\sin\theta\cos\varphi,\sin\theta\sin\varphi,\cos\theta).
$$

Inside the cylinder, $$|\varphi|\le\pi/2$$ and $$\sin\theta\le\cos\varphi$$. For each such $$\varphi$$ the two allowed polar intervals together contribute

$$
2R^2\int_0^{\arcsin(\cos\varphi)}\sin\theta\,d\theta
=2R^2(1-|\sin\varphi|).
$$

Integrating over $$\varphi$$ gives

$$
\operatorname{area}(\text{spherical caps})=2R^2(\pi-2)=4R^2\left(\frac\pi2-1\right).
$$

### Exercise 6

Equip $$M\times N$$ with the product metric. In product charts, its Gram matrix is block diagonal, so its volume density is the product of the volume densities of $$M$$ and $$N$$. These local identities patch to

$$
\lambda_{M\times N}=\lambda_M\otimes\lambda_N
$$

on the product Borel sets, followed by completion. Tonelli's theorem applied to 1 yields

$$
\operatorname{vol}(M\times N)=\operatorname{vol}(M)\operatorname{vol}(N).
$$

For nonempty manifolds the factors are strictly positive, possibly infinite. If one factor is empty, the product volume is zero; this handles the otherwise ambiguous expression $$0\cdot\infty$$. The product-metric assumption is essential. The boundary hypothesis ensures that the product belongs to the book's category of manifolds with boundary.

### Exercise 7

Use an angular coordinate $$\varphi$$ on $$S^1$$ and write

$$
F(\varphi,t)=(\rho(t)\cos\varphi,\rho(t)\sin\varphi,\sigma(t)).
$$

The derivatives are orthogonal and satisfy $$|F_\varphi|=\rho$$ and $$|F_t|=\sqrt{\rho'^2+\sigma'^2}=|\gamma'|$$. Thus the area density is $$\rho|\gamma'|$$. Since $$\rho>0$$ and $$\gamma$$ is an embedding, $$F$$ is an embedding; in particular there is no multiplicity in the area formula. Integrating over angle and parameter gives

$$
\operatorname{vol}(Z_\gamma^2)=2\pi\int_0^1\rho(t)|\gamma'(t)|\,dt.
$$

### Exercise 8

The printed formula is false even for $$a=b$$: its right side is $$2\pi^2a^2$$, while the sphere has area $$4\pi a^2$$. There is also an ambiguity in “semiaxes $$a\ge b$$”: the two distinct ellipsoids of revolution have semiaxes $$(a,b,b)$$ and $$(a,a,b)$$. Put $$e=\sqrt{a^2-b^2}/a$$.

For the **prolate** surface $$(a,b,b)$$ use

$$
F(\theta,\varphi)=(a\cos\theta,b\sin\theta\cos\varphi,b\sin\theta\sin\varphi).
$$

The area density is $$b\sin\theta\sqrt{a^2\sin^2\theta+b^2\cos^2\theta}$$. Substituting $$u=\cos\theta$$ and using symmetry gives

$$
\begin{aligned}
\operatorname{area}(E_{a,b}^{\rm prolate})
&=4\pi ab\int_0^1\sqrt{1-e^2u^2}\,du\\
&=2\pi b^2+\frac{2\pi ab}{e}\arcsin e.
\end{aligned}
$$

For the **oblate** surface $$(a,a,b)$$, the analogous parametrization gives

$$
\operatorname{area}(E_{a,b}^{\rm oblate})
=4\pi a^2\int_0^1\sqrt{1-e^2+e^2u^2}\,du
=2\pi a^2\left(1+\frac{1-e^2}{e}\operatorname{artanh}e\right).
$$

At $$e=0$$ both closed expressions are interpreted by continuity and equal $$4\pi a^2$$. These are surface areas; the corresponding solid ellipsoids have different three-dimensional volumes.

### Exercise 9

For $$a>1$$ parametrize the ring torus by

$$
F(u,v)=((a+\cos v)\cos u,(a+\cos v)\sin u,\sin v).
$$

The coordinate vectors are orthogonal, with lengths $$a+\cos v$$ and 1. The area density is therefore $$a+\cos v>0$$, and

$$
\operatorname{vol}(T^2_{a,1})=\int_0^{2\pi}\int_0^{2\pi}(a+\cos v)\,du\,dv=4\pi^2a.
$$

### Exercise 10

The cross-section perpendicular to the $$x$$-axis is a disc of radius $$r(x)=x^{-\alpha}$$. Tonelli's theorem gives

$$
\operatorname{vol}=\pi\int_1^\infty x^{-2\alpha}\,dx
=\frac\pi{2\alpha-1}<\infty.
$$

The lateral surface is generated by $$\gamma(x)=(x,r(x))$$. Its area, by the calculation in Exercise 7, is

$$
2\pi\int_1^\infty x^{-\alpha}\sqrt{1+\alpha^2x^{-2\alpha-2}}\,dx
\ge2\pi\int_1^\infty x^{-\alpha}\,dx=\infty
$$

because $$\alpha\le1$$. The end disc at $$x=1$$ has finite area $$\pi$$, so including it does not change the conclusion.

### Exercise 11

For $$(x,y)\in M\subset\{y>0\}$$ define

$$
F((x,y),\sigma)=(x,y\sigma),\qquad \sigma\in S^1.
$$

If $$(x,u)\in R_M$$, then $$|u|>0$$. Hence

$$
F^{-1}(x,u)=((x,|u|),u/|u|)
$$

is well defined and smooth; it is visibly inverse to $$F$$. Thus $$F$$ is the required diffeomorphism, including at boundary points of $$M$$.

With $$\sigma=(\cos\varphi,\sin\varphi)$$, the Euclidean metric in coordinates $$(x,y,\varphi)$$ is

$$
dx^2+dy^2+y^2d\varphi^2,
$$

so the volume density is $$y$$. Integration and the angular factor $$2\pi$$ yield

$$
\operatorname{vol}(R_M)=2\pi\int_M y\,d\lambda_M.
$$

If $$M$$ is nonempty, its area is positive and finite. Its centroid satisfies $$S_2(M)=\operatorname{vol}(M)^{-1}\int_My\,d\lambda_M$$, so

$$
\operatorname{vol}(R_M)=2\pi S_2(M)\operatorname{vol}(M).
$$

Because $$y>0$$ on $$M$$, $$S_2(M)$$ is the distance of the centroid to the rotation axis.

### Exercise 12

The same formulas for $$F$$ and $$F^{-1}$$ prove the diffeomorphism when $$M$$ is a compact one-dimensional submanifold. In a local parametrization $$t\mapsto(x(t),y(t))$$, the surface parametrization is

$$
(t,\varphi)\longmapsto(x(t),y(t)\cos\varphi,y(t)\sin\varphi).
$$

Its two coordinate vectors are perpendicular, with lengths $$\sqrt{x'^2+y'^2}$$ and $$y$$. Therefore its area density is $$y\sqrt{x'^2+y'^2}$$. Summing over charts gives

$$
\operatorname{vol}(R_M)=2\pi\int_My\,d\lambda_M.
$$

For a nonempty $$M$$ its length is positive and finite, and with the planar centroid

$$
S(M)=\frac1{\operatorname{vol}(M)}\int_M(x,y)\,d\lambda_M,
$$

we obtain $$\operatorname{vol}(R_M)=2\pi S_2(M)\operatorname{vol}(M)$$. The printed integral of the identity of $$\mathbb R^3$$ over $$M\subset\mathbb R^2$$ should be read using the natural inclusion $$(x,y)\mapsto(x,y,0)$$ or the planar formula above.

### Exercise 13

For the upper half-disc of radius $$R>0$$, symmetry gives the first centroid coordinate 0. Its area is $$\pi R^2/2$$, and polar coordinates give

$$
\int_{RB^2\cap\{y>0\}}y\,dx\,dy
=\int_0^\pi\int_0^R(r\sin\theta)r\,dr\,d\theta
=\frac{2R^3}{3}.
$$

Therefore

$$
\boxed{S=\left(0,\frac{4R}{3\pi}\right).}
$$

Adding or removing the diameter and semicircular boundary does not change this area centroid. Alternatively, rotation about the diameter gives a ball; Exercise 11 gives the same answer.

### Exercise 14

Let $$\varphi:M\to N$$ be a diffeomorphism between equal-dimensional pseudo-Riemannian manifolds. Write $$J(s)>0$$ for its **absolute volume Jacobian**, characterized by

$$
\int_M h(\varphi(s))J(s)\,d\lambda_M(s)=\int_Nh(q)\,d\lambda_N(q)
$$

for nonnegative measurable $$h$$. In coordinates, $$J$$ is the absolute coordinate determinant multiplied by the ratio of the two volume densities. If signed determinants are used, orientations must first be chosen; their absolute value is $$J$$.

**(a), (c): the printed claim is false for general $$p$$.** Even in Euclidean dimension one, let $$\varphi(x)=2x$$ and $$f=\mathbf1_{(0,1)}$$. The printed map $$J_\varphi f=2f(2x)$$ satisfies, for $$1\le p<\infty$$,

$$
\|J_\varphi f\|_p=2^{1-1/p}\|f\|_p,
$$

and for $$p=\infty$$ its norm is twice that of $$f$$. It is thus not generally an isometry unless $$p=1$$. It need not even map $$L^p$$ into $$L^p$$ for $$p>1$$: take $$\varphi(x)=e^x$$ from $$\mathbb R$$ to $$(0,\infty)$$ and $$f(y)=y^{-1}\mathbf1_{[1,\infty)}(y)$$. Then $$f\in L^p$$ for $$p>1$$, but $$J_\varphi f=\mathbf1_{[0,\infty)}$$. For $$p=\infty$$, the same map and $$f=1$$ give $$J_\varphi f=e^x$$, which is unbounded.

The correct isometric isomorphism for $$1\le p<\infty$$ is

$$
(U_pf)(s)=J(s)^{1/p}f(\varphi(s)),
$$

and for $$p=\infty$$ it is $$U_\infty f=f\circ\varphi$$. For finite $$p$$ the change-of-variables formula gives

$$
\|U_pf\|_{L^p(M;E)}^p
=\int_MJ(s)\|f(\varphi(s))\|^p\,d\lambda_M(s)
=\|f\|_{L^p(N;E)}^p.
$$

For $$p=\infty$$, diffeomorphisms preserve null sets in both directions, so essential suprema are equal. The inverse is the corresponding operator for $$\varphi^{-1}$$, since the two Jacobians are reciprocal at corresponding points. Thus the maps are linear, well defined on equivalence classes, and surjective isometries. At $$p=1$$ the printed weight agrees with the positive-Jacobian formula; a signed determinant also gives an isometry when it is defined.

**(b)** This part remains true for the printed nonzero determinant weight: a diffeomorphism preserves null sets in both directions and its determinant never vanishes. Therefore $$f=0$$ almost everywhere on $$N$$ if and only if its weighted pullback vanishes almost everywhere on $$M$$.

### Exercise 15

Use product measure $$dr\,d\lambda_{S^{n-1}}$$ on $$(0,\infty)\times S^{n-1}$$, and let $$1\le p<\infty$$. Polar coordinates give an isometric isomorphism **from the product space to** $$L^p(\mathbb R^n)$$ by

$$
(U_pg)(x)=|x|^{-(n-1)/p}g(|x|,x/|x|)\quad(x\ne0).
$$

The value at zero is arbitrary. Indeed,

$$
\int_{\mathbb R^n}|U_pg(x)|^p\,dx
=\int_{S^{n-1}}\int_0^\infty|g(r,\theta)|^p\,dr\,d\lambda_{S^{n-1}}(\theta).
$$

Its inverse sends $$f$$ to $$r^{(n-1)/p}f(r\theta)$$, with all functions understood as equivalence classes. For $$p=\infty$$ omit the weight: $$U_\infty g(x)=g(|x|,x/|x|)$$. Polar coordinates preserve null sets in both directions off the origin, so essential suprema agree. For $$n=1$$, $$S^0=\{-1,1\}$$ has counting measure and the same formulas apply.

### Exercise 16

For $$f\in C_c(\mathbb R^n)$$ the printed map is

$$
(T_0f)(\theta)(r)=r^{n-1}f(r\theta).
$$

**(a), (b)** Choose $$R$$ with $$\operatorname{supp}f\subseteq\overline{B_R}$$. The map $$\theta\mapsto T_0f(\theta)$$ is continuous into $$L^p(0,\infty)$$: uniform continuity of $$f$$ on the compact ball gives uniform convergence in $$r\in[0,R]$$ as $$\theta$$ varies, and the factor $$r^{n-1}$$ is bounded there. It is therefore strongly measurable. Moreover

$$
\int_{S^{n-1}}\|T_0f(\theta)\|_p^p\,d\theta
\le |S^{n-1}|\|f\|_\infty^p\int_0^Rr^{p(n-1)}\,dr<\infty.
$$

Thus (a) and (b) hold for the stated finite $$p$$.

**(c)** The printed extension is an isometry for $$p=1$$, but not in general for $$p>1$$ and $$n>1$$. Indeed,

$$
\|T_0f\|_p^p=\int_{S^{n-1}}\int_0^\infty |f(r\theta)|^p r^{p(n-1)}\,dr\,d\theta,
\qquad
\|f\|_{L^p(\mathbb R^n)}^p=\int_{S^{n-1}}\int_0^\infty |f(r\theta)|^p r^{n-1}\,dr\,d\theta.
$$

The weights differ. More strongly, choose a nonzero smooth bump $$\psi$$ supported in $$(0,1)$$ and let $$f_R(x)=\psi(|x|-R)$$ for $$R>1$$. On its support, $$r\ge R$$, so

$$
\frac{\|T_0f_R\|_p}{\|f_R\|_p}\ge R^{(n-1)(1-1/p)}\longrightarrow\infty.
$$

Hence no bounded extension of this printed map exists in that case.

For every $$1\le p<\infty$$, the corrected map is

$$
(T_pf)(\theta)(r)=r^{(n-1)/p}f(r\theta).
$$

The polar formula and Fubini's theorem give $$\|T_pf\|_{L^p(S^{n-1};L^p(0,\infty))}=\|f\|_{L^p(\mathbb R^n)}$$. For continuous compactly supported $$f$$, the same continuity argument as in (a) establishes strong measurability. Density of $$C_c(\mathbb R^n)$$ gives a unique isometric extension. It is onto: by the Bochner–Fubini identification, a target element has a jointly measurable representative $$G(\theta,r)$$; setting $$f(r\theta)=r^{-(n-1)/p}G(\theta,r)$$ gives an inverse equivalence class. When $$p=1$$ this is exactly the printed map. When $$n=1$$ the exponent is zero, so the printed map is also correct for all finite $$p$$.
