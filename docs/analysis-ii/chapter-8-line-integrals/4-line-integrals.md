# Chapter VIII — Line Integrals

## 4. Line integrals

These are detailed solutions to Exercises 1–14. Inline formulas use GitBook's double-dollar syntax. Exercise 14 requires a distinction between free and based loop homotopy.

### Exercise 1

Use the helix from Section VIII.1, with radius $$R>0$$ and pitch $$2\pi h$$:

$$
\gamma(t)=(R\cos t,R\sin t,ht),\qquad t_0\leq t\leq t_0+2\pi.
$$

Along it, $$dx=-R\sin t\,dt$$, $$dy=R\cos t\,dt$$ and $$dz=h\,dt$$. Thus the integral is

$$
\begin{aligned}
\int_{t_0}^{t_0+2\pi}
\bigl[-R^3\cos(2t)\sin t+3hRt\cos t
+4hR^2\cos t\sin t\bigr]dt.
\end{aligned}
$$

The first and third terms integrate to zero over a period. Since an antiderivative of $$t\cos t$$ is $$t\sin t+\cos t$$, the value is

$$
\boxed{6\pi hR\sin t_0}.
$$

In particular it is zero for the winding from $$t=0$$ to $$t=2\pi$$. The result depends on the starting point; the problem does not specify one.

### Exercise 2

Parametrize the positively oriented circle by $$\gamma(t)=(R\cos t,R\sin t)$$, $$0\leq t\leq2\pi$$. Its distance from the origin is constantly $$R$$ and

$$
x\,dy-y\,dx=R^2(\cos^2t+\sin^2t)\,dt=R^2\,dt.
$$

Therefore

$$
\boxed{\int_\Gamma\alpha=2\pi R^2\varphi(R)}.
$$

Only values of $$\varphi$$ at positive radii are used on this circle.

### Exercise 3

The form is exact:

$$
d(x^2y^3)=2xy^3\,dx+3x^2y^2\,dy.
$$

The endpoints of the path are $$(\alpha,\alpha^2/2)$$ and $$(\beta,\beta^2/2)$$. The fundamental theorem gives

$$
\boxed{\int_\Gamma 2xy^3\,dx+3x^2y^2\,dy
=\frac{\beta^8-\alpha^8}{8}}.
$$

### Exercise 4

Let $$\Phi(x,y)=(u,v)=(x^2+y^2-1,2y)$$ and

$$
\omega=\frac{u\,dv-v\,du}{u^2+v^2}.
$$

Exercise 3.3 gives $$\alpha=\Phi^*\omega$$. With $$s=\pm1$$, parametrize $$\Gamma_s$$ by $$(s+\cos t,\sin t)$$ for $$0\leq t\leq2\pi$$. Its image under $$\Phi$$ is

$$
(u,v)=(1+2s\cos t,2\sin t).
$$

This ellipse avoids the origin. Move its center from $$(1,0)$$ to $$(0,0)$$ by replacing the first coordinate with $$r+2s\cos t$$, $$0\leq r\leq1$$. These ellipses also avoid the origin: if the second coordinate is zero, the first is $$r\pm2\ne0$$. The form $$\omega$$ is closed away from the origin, so its integral is invariant under this homotopy. On the centered ellipse,

$$
u\,dv-v\,du=4s\,dt,\qquad u^2+v^2=4.
$$

Consequently

$$
\boxed{\frac1{2\pi}\int_{\Gamma_s}\alpha=s},
$$

as required.

### Exercise 5

The integral is always real-linear, but in general it is **not** a $$C^q(X)$$-module homomorphism. Indeed, the question does not specify a $$C^q(X)$$-module structure on the target $$\mathbb R$$, and even supplying one cannot make the assertion true in general.

Take $$X=\mathbb R$$ and the path $$\gamma(t)=t$$ for $$0\leq t\leq1$$. Let $$I(\alpha)=\int_\gamma\alpha$$. If $$I$$ were a module homomorphism for any unital module structure on $$\mathbb R$$, multiplication by $$x$$ on that one-dimensional real vector space would be multiplication by some scalar $$c$$. Since

$$
I(dx)=1,\qquad I(x\,dx)=\frac12,\qquad I(x^2\,dx)=\frac13,
$$

module linearity would force both $$c=1/2$$ and $$c^2=1/3$$, a contradiction. This example works for every $$q\geq0$$. For a particular degenerate curve the integral may be zero, so the counterexample disproves the general assertion rather than every individual case.

### Exercise 6

Write the form on $$X\times Y$$ as

$$
\alpha=\sum_{j=1}^n a_j(x,y)\,dx^j+
\sum_{k=1}^m b_k(x,y)\,dy^k.
$$

For fixed $$y$$, restrict it to $$X\times\{y\}$$; the $$dy^k$$ terms vanish. If $$\gamma:[A,B]\to X$$ parametrizes $$\Gamma$$, then

$$
f(y)=\int_A^B\sum_{j=1}^n a_j(\gamma(t),y)\dot\gamma^j(t)\,dt.
$$

The integrand and all its $$y$$-derivatives through order $$q$$ are continuous. Locally in $$y$$ they are uniformly continuous on the compact parameter interval, so continuity and differentiation under the integral sign give $$f\in C^q(Y)$$. In particular, for $$q\geq1$$,

$$
\boxed{\frac{\partial f}{\partial y^k}(y)
=\int_A^B\sum_{j=1}^n
\frac{\partial a_j}{\partial y^k}(\gamma(t),y)\dot\gamma^j(t)\,dt
=\int_\Gamma\sum_{j=1}^n\frac{\partial a_j}{\partial y^k}(\cdot,y)\,dx^j.}
$$

These components form $$\nabla f$$. The same reasoning applies successively to higher derivatives when $$q>1$$.

### Exercise 7

Choose a base point $$p=(p^1,\ldots,p^n)\in X$$. Integrating along the coordinate segments from $$p$$ to $$x$$ gives

$$
F(x)=\sum_{j=1}^n\int_{p^j}^{x^j}
a_j(x^1,\ldots,x^{j-1},t,p^{j+1},\ldots,p^n)\,dt.
$$

All these segments lie in the rectangle $$X$$. Since $$\alpha$$ is closed, $$\partial_k a_j=\partial_j a_k$$. For fixed $$k$$, terms with $$j<k$$ do not depend on $$x^k$$; the $$j=k$$ term contributes $$a_k(x^1,\ldots,x^k,p^{k+1},\ldots,p^n)$$. For $$j>k$$, differentiation and closedness yield

$$
\int_{p^j}^{x^j}\partial_k a_j\,dt
= a_k(x^1,\ldots,x^j,p^{j+1},\ldots,p^n)
-a_k(x^1,\ldots,x^{j-1},p^j,\ldots,p^n).
$$

The resulting sum telescopes to $$\partial_k F(x)=a_k(x)$$. Thus $$dF=\alpha$$. Any two antiderivatives differ by a constant because $$X$$ is connected, so all are $$F+C$$, $$C\in\mathbb R$$.

### Exercise 8

Put $$u=xy$$ and $$h(x,y)=m(u)$$. Equality of the mixed coefficients of $$h\alpha$$ is

$$
(c-ex)\bigl(m(u)+u m'(u)\bigr)
=(a-by)\bigl(m(u)+u m'(u)\bigr).
$$

For each fixed $$u>0$$, the factor $$c-a-ex+bu/x$$ is not identically zero as $$x>0$$ varies. Hence $$m+um'=0$$ for every $$u>0$$, and

$$
h(x,y)=\frac{C}{xy},\qquad C\ne0.
$$

Conversely, each such function is a nowhere-zero integrating factor. It gives

$$
h\alpha=C\left[\left(\frac c x-e\right)dx+
\left(\frac a y-b\right)dy\right].
$$

By direct differentiation and connectedness, all antiderivatives are

$$
\boxed{F(x,y)=C(c\log x-ex+a\log y-by)+K,\qquad K\in\mathbb R.}
$$

### Exercise 9

Let $$\gamma:[A,B]\to X$$ be a piecewise $$C^1$$ parametrization, and write $$L=\int_A^B|\dot\gamma(t)|\,dt<\infty$$, with derivatives taken piecewise. For a continuous vector field $$g$$,

$$
\left|\int_\Gamma\sum_{j=1}^n g^j\,dx^j\right|
\leq\int_A^B|g(\gamma(t))|\,|\dot\gamma(t)|\,dt
\leq L\sup_{t\in[A,B]}|g(\gamma(t))|.
$$

**(a)** Apply the estimate to $$g=f_k-f$$. Uniform convergence of $$\gamma^*f_k=f_k\circ\gamma$$ makes its right-hand side tend to zero, proving convergence of the integrals.

**(b)** Let $$S_N=\sum_{k=1}^N f_k$$. Uniform convergence of $$\sum_k\gamma^*f_k$$ to $$\gamma^*f$$ means precisely $$S_N\circ\gamma\to f\circ\gamma$$ uniformly. Applying (a) to $$S_N$$ and using linearity for each finite sum yields

$$
\sum_{k=1}^\infty\int_\Gamma\sum_{j=1}^n f_k^j\,dx^j
=\int_\Gamma\sum_{j=1}^n f^j\,dx^j.
$$

### Exercise 10

Euler's relation for the positively homogeneous coefficient $$a_j$$ is

$$
\sum_{k=1}^n x^k\partial_k a_j(x)=\lambda a_j(x).
$$

It follows by differentiating $$a_j(tx)=t^\lambda a_j(x)$$ at $$t=1$$. Since the form is closed, $$\partial_j a_k=\partial_k a_j$$. Differentiating the proposed function therefore gives

$$
\begin{aligned}
\partial_j F(x)
&=\frac1{\lambda+1}\left(a_j(x)+\sum_{k=1}^n x^k\partial_j a_k(x)\right)\\
&=\frac1{\lambda+1}\left(a_j(x)+\sum_{k=1}^n x^k\partial_k a_j(x)\right)
=a_j(x).
\end{aligned}
$$

Thus $$dF=\alpha$$, including at the origin; the assumptions ensure the derivatives used there exist. The condition $$\lambda\ne-1$$ makes the denominator nonzero.

### Exercise 11

In this section the parameter interval is a compact nondegenerate interval $$I=[a,b]$$. The increasing affine change of parameter

$$
\varphi:[0,1]\to[a,b],\qquad \varphi(t)=a+(b-a)t,
$$

is a $$C^1$$ diffeomorphism. Since $$\gamma(a)=\gamma(b)$$, the reparametrized path satisfies $$(\gamma\circ\varphi)(0)=(\gamma\circ\varphi)(1)$$ and is a loop.

### Exercise 12

**(a)** Reparametrize the loop as $$\gamma:[0,1]\to X$$. Its image is compact and has positive distance from the closed set $$\mathbb R^n\setminus X$$, unless that set is empty, in which case choose any positive bound. Choose $$\varepsilon>0$$ smaller than this distance. Uniform continuity supplies a partition $$0=t_0<\cdots<t_N=1$$ on which $$|\gamma(t)-\gamma(t_i)|<\varepsilon/2$$ for $$t_i\leq t\leq t_{i+1}$$. Let $$p$$ be the polygonal path joining consecutive values $$\gamma(t_i)$$. Then $$p(0)=p(1)$$ and $$|p(t)-\gamma(t)|<\varepsilon$$. The straight-line homotopy

$$
H(t,s)=(1-s)\gamma(t)+sp(t)
$$

stays in $$X$$ and consists of loops, proving the claim. It even fixes the base point.

**(b)** Put $$u=a/|a|$$. For $$x\notin\mathbb R_+a$$ define

$$
H(x,s)=(1-s)x-su.
$$

If $$x$$ is not collinear with $$u$$, its component perpendicular to $$u$$ is nonzero for $$s<1$$; at $$s=1$$ the value is a negative multiple of $$u$$. If it is collinear, it is a nonpositive multiple of $$u$$ and remains so. Thus $$H$$ stays in the complement and contracts it directly to $$-u$$. Consequently the complement is contractible, and hence simply connected.

**(c)** Each segment with endpoints $$v,w$$ lies in $$\operatorname{span}\{v,w\}$$, a proper subspace of $$\mathbb R^n$$ of dimension at most two. A finite union of proper linear subspaces cannot cover $$\mathbb R^n$$: each is closed with empty interior. Choose a nonzero $$a$$ outside their union. Then no point of the ray $$\mathbb R_+a$$ belongs to the polygonal image.

**(d)** By (a), any loop in $$\mathbb R^n\setminus\{0\}$$ is homotopic there to a polygonal loop. By (c) that loop lies in the complement of some ray from the origin. Part (b) contracts it there, hence also in $$\mathbb R^n\setminus\{0\}$$. This space is path connected for $$n\geq3$$, so it is simply connected.

### Exercise 13

The statement is true, with the section's convention that a closed form has continuously differentiable coefficients. By Exercise 12(d), $$\mathbb R^n\setminus\{0\}$$ is open and simply connected when $$n\geq3$$. The theorem on closed forms in simply connected open sets therefore makes every such form exact. Equivalently, fixing $$x_0$$ and defining $$F(x)=\int_{x_0}^x\alpha$$ gives a path-independent integral and $$dF=\alpha$$.

### Exercise 14

**A distinction in the formulation.** Section 4 defines loop homotopy by requiring each intermediate path to be a loop, without explicitly fixing its base point. Exercise 14 refers to loop homotopies *of* $$S_{x_0}$$; interpreting this as requiring every intermediate loop to remain in $$S_{x_0}$$ gives the based homotopies needed below. If the earlier, free-loop definition is instead merely restricted to pairs of loops based at $$x_0$$, the proposed multiplication need not be well defined. For example, take $$X=\mathbb R^2\setminus\{(-1,0),(1,0)\}$$. It deformation retracts onto a figure eight, whose based fundamental group is the free group on generators $$a,b$$. The loops represented by $$a$$ and $$bab^{-1}$$ are freely homotopic: move the base point around the loop $$b$$. Multiplying their classes by that of $$a^{-1}$$ would give the constant loop in one case and the commutator $$bab^{-1}a^{-1}$$ in the other. The latter is a nonempty reduced word, hence is not null-homotopic. Thus (a) fails under that free-homotopy interpretation.

We now prove (a) and (b) using **based homotopies**, in which the common endpoint remains $$x_0$$ throughout. For clarity, write $$p*q$$ for traversing $$p$$ first and $$q$$ second; the book writes this path as $$q\oplus p$$.

**(a)** If $$p\simeq p'$$ and $$q\simeq q'$$ through based homotopies $$P,Q$$, then

$$
H(t,s)=\begin{cases}P(2t,s),&0\leq t\leq1/2,\\
Q(2t-1,s),&1/2\leq t\leq1,\end{cases}
$$

is a based homotopy from $$p*q$$ to $$p'*q'$$. The pieces agree at $$t=1/2$$, proving that concatenation is well defined on classes.

The paths $$(p*q)*r$$ and $$p*(q*r)$$ traverse the same three paths with different breakpoints. Interpolating their increasing piecewise-linear parameter changes gives a based homotopy, so multiplication is associative. Similarly, $$p*e$$ and $$e*p$$ are based homotopic to $$p$$ by shrinking the constant portion, where $$e$$ is the constant loop at $$x_0$$. Finally, with $$\bar p(t)=p(1-t)$$, the loop $$p*\bar p$$ contracts through the loops that traverse $$p$$ only up to time $$1-s$$ and then retrace it; the same holds for $$\bar p*p$$. Hence $$[e]$$ is the identity and $$[\bar p]$$ is the inverse of $$[p]$$. These facts establish the group axioms.

**(b)** Let $$w$$ run from $$x_0$$ to $$x_1$$. Define

$$
T([p])=[\bar w*p*w],\qquad [p]\in\pi_1(X,x_0).
$$

This is well defined by concatenating a based homotopy with the fixed paths $$\bar w,w$$. For based loops $$p,q$$ at $$x_0$$, the adjacent portion $$w*\bar w$$ in

$$
(\bar w*p*w)*(\bar w*q*w)
$$

contracts to the constant loop at $$x_0$$. After reassociation, the result is $$\bar w*(p*q)*w$$, so $$T$$ is a homomorphism. The map $$[r]\mapsto[w*r*\bar w]$$ is its inverse: both composites reduce by cancelling a path with its reverse. Thus the two based fundamental groups are isomorphic. The isomorphism depends in general on the chosen connecting path.
