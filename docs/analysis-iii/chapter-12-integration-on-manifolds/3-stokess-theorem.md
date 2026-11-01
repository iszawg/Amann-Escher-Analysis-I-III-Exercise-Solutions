# Chapter XII — Integration on Manifolds

## 3. Stokes’s theorem

These solutions address Exercises 1–14. We use the book's convention $$\Delta=d\delta+\delta d$$, so the scalar Laplacian is $$\operatorname{div}\operatorname{grad}$$ and $$-\delta$$ is the formal adjoint of $$d$$ in the Riemannian case. Boundary orientations use the outward-normal-first convention. Several printed assertions require qualifications; counterexamples and corrected statements are given below.

### Exercise 1

Assume $$M$$ is nonempty, compact, oriented, and without boundary. Choose a connected component $$C$$; it is compact and has no boundary. If $$d\omega$$ had no zero on $$C$$, write $$d\omega=f\omega_C$$ with respect to a positive volume form. The continuous function $$f$$ would have one strict sign on connected $$C$$, and therefore $$\int_Cd\omega\ne0$$. Stokes's theorem gives instead

$$
\int_Cd\omega=\int_{\partial C}\omega=0.
$$

This contradiction proves that $$d\omega$$ vanishes somewhere on each component. Nonemptiness is needed to assert the existence of a point.

### Exercise 2

Let $$i:S^2\hookrightarrow\mathbb R^3\setminus\{0\}$$ be inclusion and $$\sigma=\rho^*\omega_{S^2}$$. Since $$d\omega_{S^2}=0$$ for dimensional reasons,

$$
d\sigma=\rho^*(d\omega_{S^2})=0.
$$

If $$\sigma=d\eta$$, then, since $$\rho\circ i=\operatorname{id}_{S^2}$$,

$$
4\pi=\int_{S^2}\omega_{S^2}=\int_{S^2}i^*\sigma
=\int_{S^2}d(i^*\eta)=0
$$

by Stokes's theorem. Hence $$\sigma$$ is not exact.

### Exercise 3

The conclusion is that $$f$$ is **constant on each connected component**; global constancy also requires connectedness. Since $$f$$ and $$\operatorname{grad}f$$ are compactly supported, the divergence theorem gives

$$
\int_M\Delta f\,d\lambda_M=\int_M\operatorname{div}(\operatorname{grad}f)\,d\lambda_M=0.
$$

The continuous function $$\Delta f$$ is nonnegative, so it is identically zero. The product rule now yields

$$
\Delta(f^2)=2f\Delta f+2|\operatorname{grad}f|^2=2|\operatorname{grad}f|^2.
$$

The left side also has integral zero, and positivity implies $$\operatorname{grad}f=0$$ everywhere. Thus $$f$$ is constant on each component; on a noncompact component this constant must be zero because $$f$$ has compact support.

Without connectedness the printed global claim is false: on the disjoint union of two circles, take $$f=0$$ on one and $$f=1$$ on the other. It is smooth and compactly supported and has $$\Delta f=0$$.

### Exercise 4

For $$i=1,2,3$$ apply the Euclidean divergence theorem to $$V_i=z e_i$$. Since $$\operatorname{div}(z e_i)=\partial_i z=\delta_{i3}$$,

$$
\int_{\Gamma}z\nu_i\,d\lambda_\Gamma
=\int_M\operatorname{div}(z e_i)\,dx
=\delta_{i3}\operatorname{vol}(M).
$$

Combining the components proves

$$
\boxed{\int_\Gamma z\nu\,d\lambda_\Gamma=\operatorname{vol}(M)e_3.}
$$

Equivalently, these are Stokes's theorem applied to $$z\,dy\wedge dz$$, $$z\,dz\wedge dx$$, and $$z\,dx\wedge dy$$. The formula is geometric and does not require the body to lie below the plane $$z=0$$; the physical pressure interpretation does.

### Exercise 5

The differential equations printed in Exercise XI.6.5(ii) are, for fixed $$c>0$$,

$$
\begin{aligned}
\operatorname{div}E&=4\pi\rho,&\operatorname{div}B&=0,\\
\partial_tB+c\operatorname{curl}E&=0,&
\partial_tE-c\operatorname{curl}B&=4\pi j.
\end{aligned}
$$

For a relatively compact piecewise smooth spatial domain $$D\Subset\Omega$$ and an oriented piecewise smooth surface $$S\Subset\Omega$$ with induced boundary orientation, Gauss's and Stokes's theorems give, at every fixed time,

$$
\begin{aligned}
\int_{\partial D}E\cdot\nu\,dS&=4\pi\int_D\rho\,dx,&
\int_{\partial D}B\cdot\nu\,dS&=0,\\
\oint_{\partial S}E\cdot d\ell&=-\frac1c\frac d{dt}\int_SB\cdot n\,dS,&
\oint_{\partial S}B\cdot d\ell&=\frac1c\frac d{dt}\int_SE\cdot n\,dS-\frac{4\pi}{c}\int_Sj\cdot n\,dS.
\end{aligned}
$$

Smoothness justifies differentiation under the integral sign. Conversely, if these identities hold for every such $$D$$ and $$S$$, applying Gauss and Stokes to the differences and shrinking balls and oriented planar discs to a point forces each continuous differential residual to vanish there. Thus the two sets of equations are equivalent under these hypotheses.

The sign of the current term is the one implied by the **printed** differential equations. In particular their divergence gives $$\partial_t\rho-\operatorname{div}j=0$$, whereas the standard physical convention uses the opposite current sign and gives $$\partial_t\rho+\operatorname{div}j=0$$. The differential-form definitions in XI.6.5 have additional sign and degree inconsistencies; see [XI.6, Exercise 5](../chapter-11-manifolds-and-differential-forms/6-vector-analysis.md#exercise-5) for a consistent formulation.

### Exercise 6

The exponent in the printed integrand matters: for $$u_p(x)=|x-p|^{-3}$$,

$$
\nabla u_p=-3\frac{x-p}{|x-p|^5},\qquad
\Delta u_p=6|x-p|^{-5}\quad(x\ne p).
$$

The answer depends on the shape of $$\Omega$$ and the points, rather than being a universal multiple of $$k$$. An exact expression is

$$
\boxed{\sum_{j=1}^k\int_{\partial\Omega}\partial_\nu|x-p_j|^{-3}\,dS
=-6\sum_{j=1}^k\int_{\mathbb R^3\setminus\Omega}|x-p_j|^{-5}\,dx.}
$$

To prove it, choose a large ball containing $$\overline\Omega$$ and apply the divergence theorem on its part outside $$\Omega$$. Its inner boundary has normal $$-\nu$$, and the contribution of the large sphere tends to zero because $$|\nabla u_p|=O(|x|^{-4})$$. The exterior integrals are finite: the points are strictly inside $$\Omega$$, and the integrand decays as $$|x|^{-5}$$ at infinity.

For example, if $$\Omega=B_R(0)$$ and $$p_1=0$$, the integral is $$-12\pi/R^2$$. In contrast, the familiar fundamental solution $$|x-p|^{-1}$$ would give $$-4\pi$$ per point, independently of the domain. This distinction prevents applying the harmonic-potential formula to the printed power $$-3$$.

### Exercise 7

Let $$A=\rho(M)=K_\infty(M)\cap S^m$$. The ray hypothesis makes $$\rho|_M$$ injective. However, the displayed signed integral depends on the **orientation of** $$M$$, which is not fixed by that hypothesis: take $$M=S^m$$ with the orientation opposite to the standard one. Then the left side is $$-\operatorname{vol}(S^m)$$ and the right side is positive.

The orientation-independent statement is

$$
\boxed{\int_M|\rho^*\omega_{S^m}|=\operatorname{vol}_{S^m}(A),}
$$

where the absolute value denotes the density associated with the pulled-back top form. Indeed, the area formula for the smooth map $$\rho|_M$$ gives the integral of its absolute Jacobian as the integral over $$S^m$$ of the number of preimages. Injectivity makes that number 1 on $$A$$ and 0 off $$A$$; critical values and the boundary image do not affect the measure. Thus the printed signed equality follows when the orientation is chosen so that $$\rho^*\omega_{S^m}$$ is nonnegative on positive tangent bases almost everywhere. For example, this holds when the radial map is an orientation-preserving diffeomorphism onto its image.

The ray hypothesis alone should not be silently replaced by a claim that $$\rho|_M$$ is everywhere a local diffeomorphism: radial tangent directions can occur. The absolute-Jacobian form of the area formula also covers such critical points.

### Exercise 8

The assertion is false without specifying the degree. The standard area form $$\omega_{S^2}$$ is closed, but Stokes's theorem would give $$\int_{S^2}\omega_{S^2}=0$$ if it were exact; in fact this integral is $$4\pi$$. Also a nonzero constant is a closed 0-form and is not exact, since there are no $$(-1)$$-forms.

The true positive-degree statement is: **every closed 1-form on $$S^2$$ is exact**; a 2-form is exact if and only if its integral is zero. To prove the first claim, let $$U_N=S^2\setminus\{N\}$$ and $$U_S=S^2\setminus\{S\}$$. Each is diffeomorphic to $$\mathbb R^2$$, so the Poincaré lemma gives $$\alpha|_{U_N}=df_N$$ and $$\alpha|_{U_S}=df_S$$. The overlap is connected, and $$d(f_N-f_S)=0$$ there. After changing one primitive by a constant, the two agree on the overlap and glue to a smooth global $$f$$ with $$df=\alpha$$.

For the 2-form criterion, necessity follows from Stokes. For sufficiency, choose a partition of unity subordinate to $$U_N,U_S$$ and split $$\beta=\beta_N+\beta_S$$ into forms supported compactly in those charts. Let $$\psi$$ be a smooth 2-form supported in the overlap with $$\int\psi=1$$. If $$\int\beta=0$$, transferring $$(\int\beta_N)\psi$$ from one summand to the other makes both integrals zero while retaining their chart-supportedness. It remains to show that a compactly supported 2-form $$f(x,y)dx\wedge dy$$ on $$\mathbb R^2$$ with integral zero has a compactly supported primitive.

Choose $$\theta\in C_c^\infty(\mathbb R)$$ with $$\int\theta=1$$, and put

$$
h(x)=\int_{\mathbb R}f(x,y)\,dy,\quad
H(x)=\int_{-\infty}^xh(s)\,ds,\quad
F(x,y)=\int_{-\infty}^y(f(x,s)-h(x)\theta(s))\,ds.
$$

Both $$H$$ and $$F$$ are compactly supported because the relevant integrals vanish. Direct differentiation gives

$$
d\bigl(-F\,dx+H\theta\,dy\bigr)=f\,dx\wedge dy.
$$

Apply this lemma in the two charts and extend the compactly supported primitives by zero. Their sum is a global primitive of $$\beta$$.

### Exercise 9

**(a)** To integrate over $$\partial B$$, the form on $$N$$ must have degree $$m-1$$. Thus the printed $$\Omega^{n-1}(N)$$ is appropriate only when $$n=m$$; no equality of the dimensions of $$M$$ and $$N$$ is otherwise needed. If $$\omega\in\Omega^{m-1}(N)$$ is closed and $$F|_{\partial B}=f$$, naturality of pullback and Stokes's theorem give

$$
\int_{\partial B}f^*\omega
=\int_{\partial B}F^*\omega
=\int_Bd(F^*\omega)=\int_BF^*(d\omega)=0.
$$

**(b)** Assume $$B\subset\mathbb R^m$$ is nonempty, compact, and $$m$$-dimensional. It has positive volume. With $$\Omega=dx^1\wedge\cdots\wedge dx^m$$, define

$$
\eta=\frac1m\sum_{j=1}^m(-1)^{j-1}x^j\,
 dx^1\wedge\cdots\wedge\widehat{dx^j}\wedge\cdots\wedge dx^m.
$$

Then $$d\eta=\Omega$$. If $$i:\partial B\hookrightarrow\mathbb R^m$$ is inclusion, the top-degree form $$i^*\eta$$ on $$\partial B$$ is closed and

$$
\int_{\partial B}i^*\eta=\int_Bd\eta=\operatorname{vol}(B)>0.
$$

A smooth retraction $$F:B\to\partial B$$ would contradict (a), applied to $$f=\operatorname{id}_{\partial B}$$ and $$\omega=i^*\eta$$. The printed restriction $$F|_B=\operatorname{id}_{\partial B}$$ must read $$F|_{\partial B}=\operatorname{id}_{\partial B}$$. Nonemptiness is necessary to exclude the empty case.

### Exercise 10

For compactly supported smooth real functions $$f,g$$, apply the divergence theorem to $$g\operatorname{grad}f$$:

$$
0=\int_M\operatorname{div}(g\operatorname{grad}f)\,d\lambda_M
=\int_M\bigl(g\Delta f+\langle\operatorname{grad}g,\operatorname{grad}f\rangle\bigr)d\lambda_M.
$$

Exchanging $$f,g$$ and using symmetry of the metric gives

$$
\int_M(\Delta f)g\,d\lambda_M=\int_Mf(\Delta g)\,d\lambda_M.
$$

For complex functions, insert a complex conjugate on the appropriate factor and use complex linearity of $$\Delta$$. The integration-by-parts argument also works for a pseudo-Riemannian metric, though its gradient pairing need not be positive.

### Exercise 11

For a positively oriented coordinate chart $$(u,v)$$ with metric determinant $$G$$, put $$w=\sqrt G$$ and write $$X=X^u\partial_u+X^v\partial_v$$. For a piecewise smooth coordinate domain $$D$$ contained in the chart, the divergence theorem becomes

$$
\boxed{\int_D\left[\partial_u(wX^u)+\partial_v(wX^v)\right]du\,dv
=\int_{\partial D}w(X^u\,dv-X^v\,du).}
$$

The right-hand side is $$\int_{\partial D}\iota_X\omega$$, i.e. the outward flux. This formula remains valid for general compactly supported fields and domains by patching charts. For the entire hyperbolic plane there is no boundary, so the integral of the divergence of a compactly supported field is zero.

**(a) Hyperboloid polar coordinates.** In the book's radial coordinate $$r>0$$ and angle $$\varphi$$,

$$
g=\frac{dr^2}{1+r^2}+r^2d\varphi^2,\qquad
w=\frac r{\sqrt{1+r^2}}.
$$

For $$X=X^r\partial_r+X^\varphi\partial_\varphi$$,

$$
\operatorname{div}X=\partial_rX^r+\frac{X^r}{r(1+r^2)}+\partial_\varphi X^\varphi.
$$

Substitute this $$w$$ into the boxed formula. The polar origin and angular seam are handled with other charts.

**(b) Poincaré disk.** On $$x^2+y^2<1$$,

$$
g=\frac{4(dx^2+dy^2)}{(1-x^2-y^2)^2},\qquad
w=\frac4{(1-x^2-y^2)^2},
$$

and therefore

$$
\operatorname{div}X=\partial_xX^x+\partial_yX^y
+\frac{4(xX^x+yX^y)}{1-x^2-y^2}.
$$

The boundary flux in the boxed formula is $$\int_{\partial D}w(X^xdy-X^ydx)$$.

**(c) Lobachevsky polar coordinates.** For $$\chi>0$$ and periodic angle $$\varphi$$,

$$
g=d\chi^2+\sinh^2\chi\,d\varphi^2,\qquad w=\sinh\chi,
$$

so

$$
\operatorname{div}X=\partial_\chi X^\chi+\coth\chi\,X^\chi+\partial_\varphi X^\varphi.
$$

The flux form is $$\sinh\chi(X^\chi d\varphi-X^\varphi d\chi)$$. The origin is a coordinate singularity, not a boundary of the hyperbolic plane.

**(d) Upper half-plane, called the Klein model in Exercise XI.5.9.** For $$y>0$$,

$$
g=\frac{dx^2+dy^2}{y^2},\qquad w=\frac1{y^2},\qquad
\operatorname{div}X=\partial_xX^x+\partial_yX^y-\frac{2X^y}{y}.
$$

Thus the flux form is $$y^{-2}(X^xdy-X^ydx)$$. In standard terminology this is the Poincaré upper half-plane. If “Klein model” instead means the usual Beltrami–Klein disk, its metric and corresponding density are

$$
g=\frac{dx^2+dy^2}{1-r^2}+\frac{(x\,dx+y\,dy)^2}{(1-r^2)^2},\quad
w=(1-r^2)^{-3/2},\qquad r^2=x^2+y^2<1.
$$

In these coordinates the divergence is

$$
\operatorname{div}X=\partial_xX^x+\partial_yX^y
+\frac{3(xX^x+yX^y)}{1-r^2},
$$

and the flux form is again $$w(X^xdy-X^ydx)$$. The determinant formula for $$w$$ follows by taking metric eigenvalues $$(1-r^2)^{-2}$$ in the radial direction and $$(1-r^2)^{-1}$$ tangentially.

### Exercise 12

On a Riemannian manifold without boundary, the compact-support Green identity gives, for each homogeneous component of $$\omega$$,

$$
\begin{aligned}
[\Delta\omega\mid\omega]_M
&=[d\delta\omega\mid\omega]_M+[\delta d\omega\mid\omega]_M\\
&=-\|\delta\omega\|_{L^2}^2-\|d\omega\|_{L^2}^2.
\end{aligned}
$$

If $$\Delta\omega=0$$, both nonnegative norms vanish. Smoothness then implies $$d\omega=\delta\omega=0$$ everywhere. Conversely, those two equations immediately imply $$\Delta\omega=0$$. For an inhomogeneous form apply the same argument degree by degree. Positive definiteness and compact support are essential to this proof.

### Exercise 13

For $$\alpha\in\Omega_c^{r-1}(M)$$ and $$\beta\in\Omega_c^r(M)$$, the graded product rule and the book's sign convention for $$\delta$$ give

$$
d(\alpha\wedge*\beta)
=d\alpha\wedge*\beta+\alpha\wedge*\delta\beta.
$$

For example, the sign follows from $$*\delta\beta=(-1)^{r+1}d*\beta$$, which cancels the product-rule factor $$(-1)^{r-1}$$. Stokes's theorem and the defining identity of the Riemannian Hodge star therefore yield

$$
\int_M\left(\langle d\alpha,\beta\rangle_r+\langle\alpha,\delta\beta\rangle_{r-1}\right)d\lambda_M
=\int_{\partial M}\alpha\wedge*\beta.
$$

This is (i). For (ii), substitute $$\alpha=\beta$$ and replace the second form in (i) by $$d\gamma$$; the required degrees become $$r$$ and $$r+1$$, giving

$$
\int_M\left(\langle d\beta,d\gamma\rangle_{r+1}+\langle\beta,\delta d\gamma\rangle_r\right)d\lambda_M
=\int_{\partial M}\beta\wedge*d\gamma.
$$

At the top degree the zero-form-space conventions make the formula valid as well.

### Exercise 14

Since $$M$$ is compact and without boundary, every smooth form has compact support and Green's duality formula says

$$
[d\alpha\mid\beta]_M=-[\alpha\mid\delta\beta]_M.
$$

Apply it twice, using symmetry of the bracket:

$$
\begin{aligned}
[\Delta\omega_1\mid\omega_2]_M
&=[d\delta\omega_1\mid\omega_2]_M+[\delta d\omega_1\mid\omega_2]_M\\
&=-[\delta\omega_1\mid\delta\omega_2]_M-[d\omega_1\mid d\omega_2]_M\\
&=[\omega_1\mid\Delta\omega_2]_M.
\end{aligned}
$$

The missing terms at degrees 0 and $$m$$ are zero. The same algebra proves symmetry of the book's bilinear bracket in the pseudo-Riemannian setting when its star and coderivative are defined with the stated convention; positivity of the bracket is only available for a Riemannian metric.
