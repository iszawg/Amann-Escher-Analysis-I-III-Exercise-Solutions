# Chapter VII — Multivariable Differential Calculus

## 5. Higher derivatives

These are detailed solutions to Exercises 1–21. We write $$\partial^q f(x)[h_1,\ldots,h_q]$$ for the $$q$$th Fréchet derivative evaluated on its directions. In Exercise 15(iii), the formula in the printed exercise has two incorrect direction vectors; the correct product rule and a counterexample to the printed version are given below.

### Exercise 1

Let $$A\in\mathcal L(E,F)$$. For every $$x,h\in E$$, linearity gives the exact identity

$$
A(x+h)-A(x)-Ah=0.
$$

Thus $$\partial A(x)=A$$ for every $$x$$. This derivative is constant, so $$A$$ is continuously differentiable and its second derivative vanishes. Repeating the same argument shows that all higher derivatives vanish as well. Hence $$A\in C^\infty(E,F)$$ and $$\partial^2 A=0$$.

### Exercise 2

Write $$z=(z_1,\ldots,z_m)\in E_1\times\cdots\times E_m$$. Multilinearity gives the finite expansion

$$
\varphi(x+z)
=\sum_{I\subseteq\{1,\ldots,m\}}\varphi(w_1^I,\ldots,w_m^I),
\qquad
w_i^I=
\begin{cases}
z_i,&i\in I,\\
x_i,&i\notin I.
\end{cases}
$$

The summand indexed by $$I$$ is a continuous polynomial of degree $$|I|$$ in $$z$$: it is linear in each coordinate $$z_i$$ for $$i\in I$$ and independent of the other coordinates. Continuous polynomials on Banach spaces are smooth, and a polynomial of degree at most $$m$$ has zero derivative of order $$m+1$$. The displayed finite sum therefore proves

$$
\varphi\in C^\infty(E_1\times\cdots\times E_m,F),
\qquad
\partial^{m+1}\varphi=0.
$$

### Exercise 3

For a twice differentiable radial function $$u(x)=v(r)$$, where $$r=|x|>0$$, the chain rule gives

$$
\partial_j u(x)=v'(r)\frac{x_j}{r},
\qquad
\Delta u(x)=v''(r)+\frac{m-1}{r}v'(r).
$$

Indeed, differentiating the first formula once more and summing over $$j$$ gives the second. For $$m=2$$ and $$v(r)=\log r$$, we have $$v'(r)=r^{-1}$$ and $$v''(r)=-r^{-2}$$, hence

$$
\Delta g_2(x)=-r^{-2}+r^{-1}r^{-1}=0.
$$

For $$m>2$$ and $$v(r)=r^{2-m}$$,

$$
v'(r)=(2-m)r^{1-m},
\qquad
v''(r)=(2-m)(1-m)r^{-m},
$$

so

$$
\Delta g_m(x)
=(2-m)\bigl((1-m)+(m-1)\bigr)r^{-m}=0.
$$

Thus each stated function is harmonic away from the origin.

### Exercise 4

For every coordinate $$j$$, the ordinary product rule applied twice yields

$$
\partial_j^2(fg)
=g\,\partial_j^2 f+2(\partial_j f)(\partial_j g)+f\,\partial_j^2 g.
$$

Summing over $$j=1,\ldots,m$$ and using $$\nabla f\cdot\nabla g=\sum_j(\partial_jf)(\partial_jg)$$ proves

$$
\Delta(fg)=g\Delta f+2(\nabla f\mid\nabla g)+f\Delta g.
$$

### Exercise 5

**(a)** On $$D=(0,\infty)\times(-\pi,\pi)$$, the map $$g(r,\phi)=(r\cos\phi,r\sin\phi)$$ takes values in $$\mathbb R^2\setminus H$$. Every point outside the nonpositive horizontal axis has exactly one polar representation with $$r>0$$ and $$-\pi<\phi<\pi$$. The inverse is

$$
(x,y)\longmapsto\bigl(\sqrt{x^2+y^2},\operatorname{Arg}(x+iy)\bigr),
\qquad -\pi<\operatorname{Arg}(x+iy)<\pi.
$$

Both maps are continuous on their domains, so this restriction of $$g$$ is a homeomorphism.

**(b)** Given any point $$z=(x,y)\in\mathbb R^2$$, choose $$r=\sqrt{x^2+y^2}$$ and a polar angle $$\phi$$. Then $$z=g(r,\phi)$$; for the origin take $$r=0$$. Therefore $$\operatorname{im}(g)=\mathbb R^2$$.

**(c)** Let $$v=f\circ g$$, with $$r>0$$, and write $$c=\cos\phi$$ and $$s=\sin\phi$$. The chain rule gives

$$
v_r=c f_x+s f_y,
\qquad
v_{rr}=c^2f_{xx}+2csf_{xy}+s^2f_{yy},
$$

and

$$
v_{\phi\phi}
=r^2(s^2f_{xx}-2csf_{xy}+c^2f_{yy})-r(c f_x+s f_y),
$$

where all derivatives of $$f$$ are evaluated at $$g(r,\phi)$$. Consequently the first-order terms cancel in $$v_{rr}+r^{-1}v_r+r^{-2}v_{\phi\phi}$$, and the coefficients of $$f_{xx},f_{xy},f_{yy}$$ reduce respectively to $$c^2+s^2,0,s^2+c^2$$. Thus

$$
(\Delta f)\circ g
=\frac{\partial^2(f\circ g)}{\partial r^2}
+\frac1r\frac{\partial(f\circ g)}{\partial r}
+\frac1{r^2}\frac{\partial^2(f\circ g)}{\partial\phi^2}
$$

on $$g^{-1}(X)$$.

### Exercise 6

For $$p(x,y)=y|x|^2+y^3$$, the Laplacian in the $$x$$ variables and the second derivative in $$y$$ are

$$
\Delta_x p=2ny,
\qquad
\partial_y^2p=6y.
$$

Therefore, in $$\mathbb R^{n+1}$$,

$$
\Delta p=2(n+3)y.
$$

### Exercise 7

Let $$e_1,\ldots,e_n$$ be the standard orthonormal basis of $$\mathbb R^n$$. Twice applying the chain rule gives

$$
\partial_j^2(u\circ A)(x)
=\partial^2u(Ax)[Ae_j,Ae_j].
$$

Since $$A$$ is orthogonal, $$Ae_1,\ldots,Ae_n$$ is also an orthonormal basis. The trace of the bilinear form $$\partial^2u(Ax)$$ is independent of the orthonormal basis used to compute it. Summing the last identity over $$j$$ therefore gives

$$
\Delta(u\circ A)(x)=\Delta u(Ax)=((\Delta u)\circ A)(x).
$$

### Exercise 8

**(a)** Let $$u_n$$ be a Cauchy sequence in $$BC^k(X,E)$$. For each multiindex $$\alpha$$ with $$|\alpha|\le k$$, the sequence $$\partial^\alpha u_n$$ is Cauchy in the supremum norm, so it converges uniformly to some bounded continuous function $$v_\alpha:X\to E$$. Put $$u=v_0$$.

If $$|\alpha|<k$$, then for any coordinate vector $$e_j$$ and any sufficiently short segment contained in $$X$$, the fundamental theorem of calculus gives

$$
\partial^\alpha u_n(x+te_j)-\partial^\alpha u_n(x)
=\int_0^t\partial^{\alpha+e_j}u_n(x+se_j)\,ds.
$$

Uniform convergence lets us pass to the limit on both sides. Hence

$$
v_\alpha(x+te_j)-v_\alpha(x)
=\int_0^t v_{\alpha+e_j}(x+se_j)\,ds,
$$

so $$\partial_jv_\alpha=v_{\alpha+e_j}$$. Induction on $$|\alpha|$$ shows that $$u\in BC^k(X,E)$$ and $$\partial^\alpha u=v_\alpha$$ for every $$|\alpha|\le k$$. The uniform convergence of all these derivatives is exactly convergence in $$\|\cdot\|_{k,\infty}$$. Thus $$BC^k(X,E)$$ is complete.

**(b)** Suppose $$u_n\in BUC^k(X,E)$$ and $$u_n\to u$$ in $$BC^k(X,E)$$. For every $$|\alpha|\le k$$, $$\partial^\alpha u_n\to\partial^\alpha u$$ uniformly. A uniform limit of uniformly continuous functions is uniformly continuous, so every derivative $$\partial^\alpha u$$ is uniformly continuous. Therefore $$u\in BUC^k(X,E)$$, proving this is a closed vector subspace. A closed subspace of the Banach space in (a) is Banach.

### Exercise 9

For $$|\beta|\le k$$, constant coefficients and commutation of continuous partial derivatives give

$$
\partial^\beta(A(\partial)u)
=\sum_{|\alpha|\le q}a_\alpha\,\partial^{\alpha+\beta}u.
$$

It follows that

$$
\|A(\partial)u\|_{k,\infty}
\le \left(\sum_{|\alpha|\le q}|a_\alpha|\right)\|u\|_{k+q,\infty}.
$$

Thus $$A(\partial)$$ is a bounded linear map from $$BC^{k+q}(X,\mathbb K)$$ to $$BC^k(X,\mathbb K)$$. If $$u\in BUC^{k+q}(X,\mathbb K)$$, every derivative on the right is uniformly continuous, so the image belongs to $$BUC^k(X,\mathbb K)$$ and the same estimate proves boundedness there.

### Exercise 10

**(a)** Write

$$
k(t,x)=t^{-m/2}\exp\!\left(-\frac{|x|^2}{4t}\right).
$$

Direct differentiation gives

$$
\partial_t k
=k\left(-\frac{m}{2t}+\frac{|x|^2}{4t^2}\right),
\qquad
\partial_{x_j}^2 k
=k\left(-\frac1{2t}+\frac{x_j^2}{4t^2}\right).
$$

Summing the second formula over $$j$$ shows that $$\Delta_x k=\partial_t k$$. Hence $$(\partial_t-\Delta)k=0$$ on $$(0,\infty)\times\mathbb R^m$$.

**(b)** Put $$z=v\cdot x-tc$$. Since $$|v|=1$$,

$$
\partial_t^2w=c^2g''(z),
\qquad
\Delta_xw=|v|^2g''(z)=g''(z).
$$

Therefore the wave operator satisfies

$$
\Box w=(c^2-1)g''(v\cdot x-tc).
$$

### Exercise 11

Assume **(i)**. Fix $$a,x\in X$$ and set $$\gamma(t)=f(a+t(x-a))$$ for $$0\le t\le1$$. This is a differentiable convex function of one real variable. For a differentiable convex function, its secant slopes from zero are at least its right derivative at zero, so

$$
f(x)-f(a)=\gamma(1)-\gamma(0)\ge\gamma'(0)=\partial f(a)(x-a).
$$

This proves **(ii)**.

Assume **(ii)** and fix $$a\in X$$ and $$h\in E$$. For small $$t>0$$, apply (ii) with $$x=a+th$$ and use the second-order expansion at $$a$$:

$$
\frac{t^2}{2}\partial^2f(a)[h,h]+o(t^2)
=f(a+th)-f(a)-t\,\partial f(a)h\ge0.
$$

Divide by $$t^2$$ and let $$t\downarrow0$$ to obtain **(iii)**.

Assume **(iii)**. On any segment in $$X$$, the same function $$\gamma$$ has

$$
\gamma''(t)=\partial^2f(a+t(x-a))[x-a,x-a]\ge0.
$$

Thus $$\gamma'$$ is nondecreasing, which implies that $$\gamma$$ is convex. Convexity on every segment is exactly **(i)**. This proves the equivalence of (i)–(iii). When $$E=\mathbb R^m$$, the identity

$$
\partial^2 f(a)[h,h]=(Hf(a)h\mid h)
$$

shows that **(iii)** is equivalent to positive semidefiniteness of the Hessian, giving **(iv)**.

### Exercise 12

The critical point equations are

$$
x^2+\alpha y=0,
\qquad
y^2-\alpha x=0.
$$

If $$\alpha=0$$, they give only $$(0,0)$$. If $$\alpha\ne0$$, substitution of $$y=-x^2/\alpha$$ into the second equation yields

$$
x^4/\alpha^2=\alpha x,
$$

so the critical points are $$(0,0)$$ and $$(\alpha,\alpha)$$. The Hessian is

$$
Hf_\alpha(x,y)=
\begin{pmatrix}
6x&3\alpha\\
3\alpha&-6y
\end{pmatrix}.
$$

For $$\alpha\ne0$$, its determinant is $$-9\alpha^2<0$$ at the origin and $$-45\alpha^2<0$$ at $$(\alpha,\alpha)$$. Each Hessian is indefinite, so both points are saddle points. If $$\alpha=0$$, then $$f_0(x,0)=x^3$$ takes both signs arbitrarily close to the origin; thus the origin is not a local extremum and is a (degenerate) saddle point. There are no other critical points.

### Exercise 13

**(a)** For $$x\ne0$$, choose $$y=\tfrac32x^2$$. Then

$$
f(x,\tfrac32x^2)
=(\tfrac12x^2)(-\tfrac12x^2)
=-\tfrac14x^4<0=f(0,0).
$$

Such points approach the origin, so $$(0,0)$$ is not a local minimum.

**(b)** Along the line $$(tx_0,ty_0)$$,

$$
f(tx_0,ty_0)
=t^2(y_0-tx_0^2)(y_0-2tx_0^2).
$$

If $$y_0\ne0$$, the factor following $$t^2$$ tends to $$y_0^2>0$$ as $$t\to0$$, so the value is strictly positive for all sufficiently small nonzero $$t$$. If $$y_0=0$$, then $$x_0\ne0$$ and the expression is $$2t^4x_0^4>0$$ for every $$t\ne0$$. In either case, the restriction has a strict, isolated local minimum at $$t=0$$.

### Exercise 14

Set $$h=x-1$$ and $$k=y-1$$. For $$F(x,y)=(x-y)/(x+y)$$,

$$
F(1,1)=0,\qquad
\nabla F(1,1)=(\tfrac12,-\tfrac12),\qquad
H_F(1,1)=
\begin{pmatrix}
-\tfrac12&0\\
0&\tfrac12
\end{pmatrix}.
$$

The second-order Taylor formula is therefore

$$
F(x,y)
=\frac{h-k}{2}+\frac{k^2-h^2}{4}
+o(h^2+k^2)
\qquad ((x,y)\to(1,1)).
$$

Equivalently, replace $$h,k$$ by $$x-1,y-1$$ in this expression.

### Exercise 15

**(i)** Directly from the definition,

$$
[g,f]=\partial g\,f-\partial f\,g=-[f,g].
$$

**(ii)** Linearity of the derivative gives

$$
[\alpha f+\beta g,h]
=(\alpha\partial f+\beta\partial g)h-\partial h(\alpha f+\beta g)
=\alpha[f,h]+\beta[g,h].
$$

**(iii)** The formula printed in the exercise is not correct as written. The product rule gives

$$
\partial(\varphi f)(\psi g)
=\psi(\nabla\varphi\mid g)f+\varphi\psi\,\partial f\,g,
$$

and

$$
\partial(\psi g)(\varphi f)
=\varphi(\nabla\psi\mid f)g+\varphi\psi\,\partial g\,f.
$$

Subtracting, the correct identity is

$$
[\varphi f,\psi g]
=\varphi\psi[f,g]
+\psi(\nabla\varphi\mid g)f
-\varphi(\nabla\psi\mid f)g.
$$

In the printed formula, $$g$$ and $$f$$ in the two gradient pairings are interchanged. For example, in dimension one take $$\varphi(x)=x$$, $$\psi(x)=1$$, $$f(x)=2$$, and $$g(x)=3$$. The left side is $$[2x,3]=6$$, while the printed right side equals $$4$$. Thus the correction is necessary.

**(iv)** Write $$D$$ for the derivative. Differentiating the bracket gives

$$
D[f,g]h
=D^2f[h,g]+Df(Dg\,h)-D^2g[h,f]-Dg(Df\,h).
$$

Consequently,

$$
[[f,g],h]=D[f,g]h-Dh(Df\,g-Dg\,f).
$$

Add this formula and its two cyclic versions. Terms involving second derivatives cancel in pairs because $$D^2f,D^2g,D^2h$$ are symmetric bilinear maps. The remaining terms are

$$
\begin{aligned}
&Df(Dg\,h)-Dg(Df\,h)-Dh(Df\,g)+Dh(Dg\,f)\\
&\quad+Dg(Dh\,f)-Dh(Dg\,f)-Df(Dg\,h)+Df(Dh\,g)\\
&\quad+Dh(Df\,g)-Df(Dh\,g)-Dg(Dh\,f)+Dg(Df\,h),
\end{aligned}
$$

and cancel term by term. Hence

$$
[[f,g],h]+[[g,h],f]+[[h,f],g]=0.
$$

### Exercise 16

Define $$\rho:\mathbb R\to\mathbb R$$ by $$\rho(s)=e^{-1/s}$$ for $$s>0$$ and $$\rho(s)=0$$ for $$s\le0$$. For every integer $$N\ge0$$,

$$
\lim_{s\downarrow0}s^{-N}e^{-1/s}=0,
$$

as follows by putting $$r=1/s$$ and using $$r^Ne^{-r}\to0$$. Repeated differentiation on $$s>0$$ expresses each derivative of $$\rho$$ as a polynomial in $$1/s$$ times $$e^{-1/s}$$. The limit above shows that every such derivative tends to zero at the origin; extending each by zero proves inductively that $$\rho\in C^\infty(\mathbb R)$$. The function in the exercise is

$$
x\longmapsto \rho(1-|x|^2),
$$

so it is smooth as a composition of smooth maps.

### Exercise 17

First consider a twice differentiable map $$f:X\to F$$ and fix $$x\in X$$ and $$h_1,h_2\in\mathbb R^m$$. Put $$B=\partial^2f(x)$$. Differentiability of the map $$\partial f$$ at $$x$$ means

$$
\partial f(x+z)=\partial f(x)+B[z,\,\cdot\,]+r(z),
\qquad
\frac{\|r(z)\|}{|z|}\longrightarrow0.
$$

For sufficiently small $$s>0$$, the fundamental theorem of calculus on the two line segments gives

$$
\begin{aligned}
&f(x+sh_1+sh_2)-f(x+sh_1)-f(x+sh_2)+f(x)\\
&=\int_0^s\bigl(\partial f(x+sh_1+th_2)-\partial f(x+th_2)\bigr)h_2\,dt.
\end{aligned}
$$

In the integrand, the linear terms in the expansion of $$\partial f$$ differ by $$sB[h_1,h_2]$$. Since both remainder arguments have norm at most $$s(|h_1|+|h_2|)$$, their difference, after evaluation on $$h_2$$, is $$o(s)$$ uniformly for $$0\le t\le s$$. Dividing the integral by $$s^2$$ therefore yields the limit

$$
\lim_{s\downarrow0}
\frac{f(x+sh_1+sh_2)-f(x+sh_1)-f(x+sh_2)+f(x)}{s^2}
=B[h_1,h_2].
$$

The numerator is unchanged when $$h_1$$ and $$h_2$$ are exchanged. The same limit computed in that order is $$B[h_2,h_1]$$, so $$B$$ is symmetric.

Now proceed by induction on $$q$$. The case $$q=1$$ is immediate, and the preceding argument proves the case $$q=2$$, also for maps into any Banach space. Suppose the claim holds through order $$q-1$$. Apply the twice-differentiable case to the map

$$
x\longmapsto\partial^{q-2}f(x)\in\mathcal L^{q-2}(\mathbb R^m,F).
$$

It shows that $$\partial^q f(x)$$ is unchanged when its first two arguments are exchanged. The induction hypothesis says that, as a function of the base point, $$\partial^{q-1}f$$ is symmetric in its $$q-1$$ direction arguments; differentiating these identities shows that $$\partial^q f(x)$$ is symmetric in its last $$q-1$$ arguments. These transpositions generate all permutations of $$q$$ arguments, so $$\partial^q f(x)$$ is symmetric. This proves $$\partial^qf(x)\in\mathcal L^q_{\mathrm{sym}}(\mathbb R^m,F)$$ for every $$q\le m$$. Taking the directions to be coordinate vectors gives the asserted equality of mixed partial derivatives.

### Exercise 18

If $$A$$ is positive definite, then it is injective: $$Ax=0$$ with $$x\ne0$$ would imply $$(Ax\mid x)=0$$, contradicting positive definiteness. Since $$H$$ is finite-dimensional, injectivity implies surjectivity, so $$A$$ is an automorphism. For $$y\ne0$$, put $$x=A^{-1}y$$. Self-adjointness of a positive definite operator gives

$$
(A^{-1}y\mid y)=(x\mid Ax)=(Ax\mid x)>0.
$$

Thus $$A^{-1}$$ is positive definite. If $$A$$ is negative definite, apply the same argument to $$-A$$; it follows that $$A$$ is invertible and $$A^{-1}$$ is negative definite.

### Exercise 19

**(a)** The symmetric operators form a closed linear subspace of $$\mathcal L(H)$$. For an interior point $$t$$, the difference quotients

$$
\frac{A(t+s)-A(t)}{s}
$$

are symmetric. Their limit $$\partial A(t)$$ is therefore symmetric. The same conclusion at endpoints follows from the one-sided derivative.

**(b)(i)** For every nonzero $$x\in H$$, the fundamental theorem of calculus gives

$$
((A(\tau)-A(\sigma))x\mid x)
=\int_\sigma^\tau(\partial A(t)x\mid x)\,dt>0.
$$

The strict inequality follows because the integrand is continuous and positive at every point of the nondegenerate interval. The difference is symmetric by (a), hence positive definite.

**(b)(ii)** Suppose each $$A(t)$$ is an automorphism. Differentiating $$A^{-1}(t)A(t)=I$$ yields

$$
\partial(A^{-1})(t)=-A^{-1}(t)(\partial A(t))A^{-1}(t).
$$

For $$x\ne0$$, let $$y=A^{-1}(t)x\ne0$$. Since $$A^{-1}(t)$$ is symmetric,

$$
(\partial(A^{-1})(t)x\mid x)
=-(\partial A(t)y\mid y)<0.
$$

Integrating from $$\sigma$$ to $$\tau$$ shows that $$A^{-1}(\tau)-A^{-1}(\sigma)$$ is negative definite.

### Exercise 20

Set $$C(t)=B+t(A-B)$$ for $$0\le t\le1$$. Since $$B$$ and $$A$$ are positive definite, every convex combination $$C(t)=(1-t)B+tA$$ is positive definite and hence invertible. Also $$C'(t)=A-B$$ is positive definite. Apply Exercise 19(b)(ii) to this path, with $$\sigma=0$$ and $$\tau=1$$. It gives

$$
A^{-1}-B^{-1}=C^{-1}(1)-C^{-1}(0)
$$

negative definite, as required.

### Exercise 21

We prove the multiindex Leibniz rule by induction on $$|\alpha|$$. For $$|\alpha|=0$$ it is the identity $$fg=fg$$. Suppose it holds for $$\alpha$$. Differentiate with respect to the coordinate $$x_j$$:

$$
\partial^{\alpha+e_j}(fg)
=\sum_{\beta\le\alpha}\binom{\alpha}{\beta}
\left(
\partial^{\beta+e_j}f\,\partial^{\alpha-\beta}g
+\partial^\beta f\,\partial^{\alpha-\beta+e_j}g
\right).
$$

Collect terms with the same derivative multiindex on $$f$$. Pascal’s identity for the binomial coefficients gives exactly

$$
\partial^{\alpha+e_j}(fg)
=\sum_{\gamma\le\alpha+e_j}
\binom{\alpha+e_j}{\gamma}\,
\partial^\gamma f\,\partial^{\alpha+e_j-\gamma}g.
$$

This proves the formula for every multiindex of length at most $$q$$. Each term on the right is continuous because $$f,g\in C^q(X,\mathbb K)$$, so $$fg\in C^q(X,\mathbb K)$$ as well.
