# Chapter X — Integration Theory

## 8. The substitution rule

These solutions address Exercises 1–7. We use $$\lambda_n$$ for Lebesgue measure, $$\omega_n=\pi^{n/2}/\Gamma(1+n/2)$$ for the volume of the unit ball, and $$J_\Phi=|\det D\Phi|$$ for the absolute Jacobian. Equalities involving nonnegative integrals allow the value $$+\infty$$. Exercises 6 and 7 contain apparent slips in the printed hint and domain, respectively; they are explained below.

### Exercise 1

Let $$G$$ be real symmetric and positive definite. By the spectral theorem, there is an orthogonal matrix $$U$$ such that

$$
U^TGU=\operatorname{diag}(\lambda_1,\ldots,\lambda_n),
\qquad \lambda_j>0.
$$

Set $$x=Uy$$. The absolute Jacobian is $$|\det U|=1$$, so Tonelli's theorem and the one-dimensional Gaussian integral yield

$$
\begin{aligned}
\int_{\mathbb R^n}e^{-(Gx\mid x)}\,dx
&=\int_{\mathbb R^n}\prod_{j=1}^ne^{-\lambda_j y_j^2}\,dy\\
&=\prod_{j=1}^n\left(\int_{\mathbb R}e^{-\lambda_j y_j^2}\,dy_j\right)
=\prod_{j=1}^n\frac{\sqrt\pi}{\sqrt{\lambda_j}}
=\frac{\pi^{n/2}}{\sqrt{\det G}}.
\end{aligned}
$$

The positive square root is intended. Equivalently, the substitution $$z=G^{1/2}x$$ maps the integral to the standard Gaussian integral with Jacobian $$(\det G)^{-1/2}$$.

### Exercise 2

Write $$\sigma=\operatorname{Re}p>n/2$$ and use the real logarithm to define $$(1+|x|^2)^{-p}$$. The integrand is absolutely integrable: near infinity its modulus is comparable to $$|x|^{-2\sigma}$$, and $$2\sigma>n$$.

The gamma integral, with a positive real change of scale, gives

$$
(1+|x|^2)^{-p}=\frac1{\Gamma(p)}\int_0^\infty
 t^{p-1}e^{-t(1+|x|^2)}\,dt.
$$

The double integral is absolutely convergent, since the modulus of the integrand has integral

$$
\int_0^\infty t^{\sigma-1}e^{-t}
 \left(\int_{\mathbb R^n}e^{-t|x|^2}\,dx\right)dt
=\pi^{n/2}\int_0^\infty t^{\sigma-1-n/2}e^{-t}\,dt<\infty.
$$

Fubini and the Gaussian integral therefore give

$$
\begin{aligned}
\int_{\mathbb R^n}(1+|x|^2)^{-p}\,dx
&=\frac{\pi^{n/2}}{\Gamma(p)}
 \int_0^\infty t^{p-n/2-1}e^{-t}\,dt\\
&=\pi^{n/2}\frac{\Gamma(p-n/2)}{\Gamma(p)}.
\end{aligned}
$$

The last gamma integral is valid because $$\operatorname{Re}(p-n/2)>0$$.

### Exercise 3

On the interior of $$D$$, set

$$
(x,y)=\Phi(s,t)=\bigl(s(1-t),st\bigr),\qquad 0<s,t<1.
$$

This is a smooth bijection with smooth inverse $$s=x+y$$, $$t=y/(x+y)$$, and $$|\det D\Phi(s,t)|=s$$. The boundary of the triangle has measure zero; where the displayed expression is undefined there, assign any finite values without affecting integrability.

Assume first that $$s\mapsto s^{p+q-1}f(s)$$ is integrable. The substitution rule and Tonelli give

$$
\begin{aligned}
\int_D |x^{p-1}y^{q-1}f(x+y)|\,dx\,dy
&=\int_0^1\!\int_0^1
 s^{p+q-1}|f(s)|(1-t)^{p-1}t^{q-1}\,dt\,ds\\
&=B(p,q)\int_0^1s^{p+q-1}|f(s)|\,ds<\infty.
\end{aligned}
$$

Here $$B(p,q)=\int_0^1(1-t)^{p-1}t^{q-1}\,dt$$ is positive and finite. Conversely, if the function on $$D$$ is integrable, its pullback times the Jacobian is integrable. Fubini supplies a $$t_0\in(0,1)$$ for which its section is integrable in $$s$$; the strictly positive constant $$(1-t_0)^{p-1}t_0^{q-1}$$ shows that $$s^{p+q-1}f(s)$$ is integrable. This also establishes the required measurability even if it was not separately assumed for $$f$$. Once absolute integrability is known, Fubini without absolute values gives

$$
\int_Dx^{p-1}y^{q-1}f(x+y)\,dx\,dy
=B(p,q)\int_0^1s^{p+q-1}f(s)\,ds.
$$

### Exercise 4

Work first away from the positive real axis, where the polar map

$$
P:(0,\infty)\times(0,2\pi)\to\mathbb R^2\setminus([0,\infty)\times\{0\}),
\qquad P(r,\theta)=(r\cos\theta,r\sin\theta),
$$

is a smooth diffeomorphism. Let $$I=[\alpha,\beta]\cap(0,2\pi)$$. Because $$f$$ is Lebesgue measurable, the set

$$
A=\{(r,\theta):\theta\in I,\ 0<r\le f(\theta)\}
$$

is Lebesgue measurable. A diffeomorphism and its inverse preserve null sets locally, so $$P(A)$$ is Lebesgue measurable. The portion of the given set on the excluded axis, including the origin under any convention for its argument, is a subset of a line and is therefore measurable and null. Thus the full set is measurable, even when $$f$$ is not Borel measurable or is unbounded.

The polar substitution formula and Tonelli now imply

$$
\begin{aligned}
\lambda_2(S(\alpha,\beta,f))
&=\int_I\int_0^{f(\theta)}r\,dr\,d\theta\\
&=\frac12\int_\alpha^\beta f(\theta)^2\,d\theta.
\end{aligned}
$$

Both sides may be infinite; changing the finitely many endpoint angles does not affect the result.

### Exercise 5

Let $$g$$ be the given symmetric positive-definite bilinear form, represented in an orthonormal basis by the positive-definite matrix $$G$$. Its associated quadratic form is $$Q(x)=g(x,x)=x^TGx$$; this is the meaning of the exercise's notation $$g^{-1}([0,1])$$. Let $$A=G^{1/2}$$. Since $$Q(x)=|Ax|^2$$, the substitution $$z=Ax$$ maps the ellipsoid onto the unit ball. Therefore

$$
\lambda_n\{x:g(x,x)\le1\}
=\frac{\omega_n}{|\det A|}
=\frac{\pi^{n/2}}{\Gamma(1+n/2)\sqrt{\det G}}.
$$

The determinant is independent of the choice of orthonormal basis. In principal-axis coordinates the semiaxes have lengths $$\lambda_j^{-1/2}$$, giving the same formula.

### Exercise 6

Let $$C=\{x\in X:\det D\Phi(x)=0\}$$. It is relatively closed in $$X$$ and is a countable union of compact sets, because $$X$$ has a compact exhaustion. It is enough to prove that the image of each compact subset $$K\subset C$$ is null.

Choose a compact neighborhood $$L\subset X$$ of $$K$$ and let $$M=\sup_L\|D\Phi\|<\infty$$. Given $$\varepsilon>0$$, uniform continuity of $$D\Phi$$ on $$L$$ supplies $$\delta>0$$ such that $$\|D\Phi(x)-D\Phi(y)\|\le\varepsilon$$ whenever $$x,y\in L$$ and $$|x-y|\le\delta$$. Enclose $$K$$ in a fixed bounded cube and subdivide it into cubes of side $$\ell$$ small enough that every cube meeting $$K$$ lies in $$L$$ and has diameter less than $$\delta$$. For each such cube $$Q$$ choose $$z\in Q\cap K$$ and write $$A=D\Phi(z)$$. The segment formula gives, for $$x\in Q$$,

$$
\Phi(x)=\Phi(z)+A(x-z)+R_z(x),\qquad
|R_z(x)|\le\varepsilon|x-z|\le\sqrt n\,\varepsilon\ell.
$$

Since $$z\in C$$, the range of $$A$$ lies in a hyperplane. In orthonormal coordinates adapted to that hyperplane, the projection of $$A(Q-z)$$ lies in an $$(n-1)$$-dimensional box with side at most $$2\sqrt n M\ell$$. The remainder thickens it by at most $$\sqrt n\varepsilon\ell$$ in every direction. Hence, also when $$n=1$$,

$$
\lambda_n^*(\Phi(Q))\le
C_n(M+\varepsilon)^{n-1}\varepsilon\ell^n,
$$

where $$C_n$$ depends only on $$n$$. The number of subdividing cubes is at most a fixed constant times $$\ell^{-n}$$. Summing the bounds for the cubes meeting $$K$$ yields

$$
\lambda_n^*(\Phi(K))\le C_{K,L,n}(M+\varepsilon)^{n-1}\varepsilon.
$$

Letting $$\varepsilon\downarrow0$$ proves $$\lambda_n(\Phi(K))=0$$ and hence $$\lambda_n(\Phi(C))=0$$.

**Printed hint.** As displayed in the cited edition, $$\rho(r)$$ uses the norm of $$D\Phi$$ itself and is asserted to tend to zero at a critical point. This is not true in general: for $$\Phi(x_1,x_2)=(x_1,0)$$ every point is critical but $$\rho(r)=1$$. The small quantity needed in the proof is an oscillation such as $$\sup_{x\in J_0}\|D\Phi(x)-D\Phi(x_0)\|$$; the estimate also depends on a bound for $$\|D\Phi\|$$ through the other $$n-1$$ directions.

### Exercise 7

Put $$U=X\setminus C$$ and $$V=\Phi(U)$$. By the inverse function theorem $$U$$ and $$V$$ are open. The assumed injectivity of $$\Phi|_U$$ makes its local inverses agree on overlaps, so $$\Phi|_U:U\to V$$ is a $$C^1$$ diffeomorphism. Exercise 6 shows that $$\Phi(C)$$ is null; consequently

$$
\Phi(X)=V\cup\Phi(C)
$$

is Lebesgue measurable and differs from $$V$$ by a null set. Also $$J_\Phi=0$$ on $$C$$.

**(i)** The integrand must be a nonnegative measurable function on $$\Phi(X)$$. The printed phrase $$f\in L^0(X,\mathbb R^+)$$ appears to give the wrong domain: for general $$\Phi$$ it does not even define $$f$$ on $$\Phi(X)$$. Interpreting the domain as $$\Phi(X)$$, the substitution theorem on $$U\to V$$ gives

$$
\int_{\Phi(X)}f(y)\,dy
=\int_Vf(y)\,dy
=\int_U f(\Phi(x))J_\Phi(x)\,dx
=\int_X f(\Phi(x))J_\Phi(x)\,dx.
$$

The first equality uses completeness of Lebesgue measure and the nullity of $$\Phi(C)$$. On $$C$$ the weighted integrand is defined to be zero, including the convention $$0\cdot\infty=0$$ if extended values are allowed. This makes it measurable even if $$f\circ\Phi$$ is not measurable on $$C$$ by itself.

**(ii)** Let $$f:\Phi(X)\to E$$, where $$E$$ is a Banach space, and set the weighted pullback to zero on $$C$$. If $$f$$ is Bochner integrable, the vector-valued substitution theorem on $$U\to V$$ shows that its weighted pullback is integrable, with equal integrals; the null sets just identified may be ignored.

Conversely, suppose the weighted pullback is Bochner integrable on $$X$$. Its restriction to $$U$$ is integrable. Applying the vector-valued substitution theorem to the inverse diffeomorphism gives Bochner integrability of $$f|_V$$, because

$$
f(y)=\bigl(f(\Phi(\cdot))J_\Phi(\cdot)\bigr)(\Phi^{-1}(y))
\,|\det D\Phi^{-1}(y)|,\qquad y\in V.
$$

The complement $$\Phi(X)\setminus V$$ is null, so $$f$$ is Bochner integrable on $$\Phi(X)$$ as well. The same substitution formula gives the asserted equality of vector-valued integrals.
