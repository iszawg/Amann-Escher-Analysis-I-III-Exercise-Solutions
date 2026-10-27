# Chapter VIII — Line Integrals

## 1. Curves and their lengths

These are detailed solutions to Exercises 1–8. Inline formulas use GitBook's double-dollar syntax.

### Exercise 1

Let the disc have radius $$R>0$$ and roll to the right without slipping. Use the rotation angle $$t$$ as parameter, so the center is at $$(Rt,R)$$ after the disc has turned through angle $$t$$. If the point has initial position $$(a,b)$$ relative to the center, clockwise rotation gives

$$
\gamma(t)=\bigl(Rt+a\cos t+b\sin t,\ R-a\sin t+b\cos t\bigr),
\qquad 0\le t\le2\pi.
$$

This also describes a point on an extension of the disc: its distance from the center may be any $$\rho=\sqrt{a^2+b^2}\ge0$$. Differentiating,

$$
\dot\gamma(t)=\bigl(R-a\sin t+b\cos t,\ -a\cos t-b\sin t\bigr).
$$

Write $$a=\rho\cos\theta$$ and $$b=\rho\sin\theta$$ when $$\rho>0$$. Then

$$
|\dot\gamma(t)|^2
=R^2+\rho^2+2R\rho\sin(\theta-t),
$$

so the length for one full turn is

$$
L=\int_0^{2\pi}\sqrt{R^2+\rho^2+2R\rho\sin u}\,du.
$$

The phase $$\theta$$ has disappeared because the integrand is integrated over a full period. In terms of the complete elliptic integral of the second kind

$$
E(m):=\int_0^{\pi/2}\sqrt{1-m\sin^2 v}\,dv,
$$

the same length is

$$
L=4(R+\rho)\,E\!\left(\frac{4R\rho}{(R+\rho)^2}\right).
$$

Indeed, shift the angle in the integral and use

$$
R^2+\rho^2+2R\rho\sin u
=(R+\rho)^2-4R\rho\sin^2\!\left(\frac{u-\pi/2}{2}\right).
$$

For a point at the disc's center, $$\rho=0$$ and $$L=2\pi R$$. For a point on the rim, $$\rho=R$$, the path is a cycloid arch and $$L=8R$$, since $$E(1)=1$$.

### Exercise 2

**(i)** For

$$
\gamma(t)=(\cos t+t\sin t,\ \sin t-t\cos t),
\qquad 0\le t\le\pi,
$$

the derivatives simplify to

$$
\dot\gamma(t)=(t\cos t,\ t\sin t),
\qquad
|\dot\gamma(t)|=t.
$$

Thus

$$
L(\gamma)=\int_0^\pi t\,dt=\frac{\pi^2}{2}.
$$

**(ii)** For $$\gamma(t)=t^{-2}(\cos t,\sin t)$$ on $$[1,\infty)$$, the radial and angular derivative terms are orthogonal:

$$
\dot\gamma(t)
=-2t^{-3}(\cos t,\sin t)+t^{-2}(-\sin t,\cos t),
\qquad
|\dot\gamma(t)|=\frac{\sqrt{t^2+4}}{t^3}.
$$

The improper length integral converges. With $$u=1/t$$,

$$
L(\gamma)
=\int_1^\infty\frac{\sqrt{t^2+4}}{t^3}\,dt
=\int_0^1\sqrt{1+4u^2}\,du
=\frac{\sqrt5}{2}+\frac14\operatorname{arsinh}(2).
$$

Equivalently, $$\operatorname{arsinh}(2)=\log(2+\sqrt5)$$.

**(iii)** For $$\gamma(t)=(t^3,3t^2/2)$$,

$$
\dot\gamma(t)=(3t^2,3t),
\qquad
|\dot\gamma(t)|=3|t|\sqrt{1+t^2}.
$$

Define

$$
F(t)=
\begin{cases}
\bigl((1+t^2)^{3/2}-1\bigr),&t\ge0,\\
-\bigl((1+t^2)^{3/2}-1\bigr),&t<0.
\end{cases}
$$

On either side of zero, $$F'(t)=3|t|\sqrt{1+t^2}$$; the one-sided derivatives at zero are both zero. Hence

$$
L(\gamma)=F(\beta)-F(\alpha).
$$

This single formula covers intervals on either side of zero and intervals that cross zero.

**(iv)** For $$\gamma(t)=(t,t^2/2)$$,

$$
\dot\gamma(t)=(1,t),
\qquad
|\dot\gamma(t)|=\sqrt{1+t^2}.
$$

An antiderivative is $$\frac12\bigl(t\sqrt{1+t^2}+\operatorname{arsinh}t\bigr)$$, so

$$
L(\gamma)
=\frac12\left[
t\sqrt{1+t^2}+\operatorname{arsinh}t
\right]_{\alpha}^{\beta}.
$$

### Exercise 3

The limacon in Example VII.9.1(c) is parametrized by

$$
\gamma(t)=(1+2\cos t)(\cos t,\sin t),
\qquad -\pi\le t\le\pi.
$$

For a polar parametrization $$r(t)(\cos t,\sin t)$$, its speed is $$\sqrt{\dot r(t)^2+r(t)^2}$$. Here $$r(t)=1+2\cos t$$ and $$\dot r(t)=-2\sin t$$, hence

$$
|\dot\gamma(t)|
=\sqrt{4\sin^2t+(1+2\cos t)^2}
=\sqrt{5+4\cos t}.
$$

Therefore

$$
L=\int_{-\pi}^{\pi}\sqrt{5+4\cos t}\,dt.
$$

For example, the composite trapezoidal rule with $$N=100$$ equal subintervals gives

$$
T_{100}
=\frac{2\pi}{100}\left[
\frac{f(-\pi)+f(\pi)}2
+\sum_{j=1}^{99}f\!\left(-\pi+\frac{2\pi j}{100}\right)
\right]
\approx 13.3648932206,
\qquad f(t)=\sqrt{5+4\cos t}.
$$

Thus the limacon's length is approximately $$13.3649$$.

### Exercise 4

Here

$$
\gamma(t)=t(\cos t,\sin t,1)
=(t\cos t,t\sin t,t),
\qquad -3\pi\le t\le3\pi.
$$

Its cylindrical height is $$z=t$$ and its distance from the $$z$$-axis is $$|t|$$, while its angular position rotates with $$t$$ (for $$t<0$$ the negative radial coordinate adds an angle of $$\pi$$). The curve passes through the origin and spirals away on each side.

Differentiation gives

$$
\dot\gamma(t)=(\cos t-t\sin t,\ \sin t+t\cos t,\ 1).
$$

The squared norm of the first two coordinates is $$1+t^2$$, so

$$
|\dot\gamma(t)|=\sqrt{t^2+2}.
$$

The speed is even. Using an antiderivative of $$\sqrt{t^2+2}$$,

$$
L(\gamma)
=2\int_0^{3\pi}\sqrt{t^2+2}\,dt
=3\pi\sqrt{9\pi^2+2}
+2\operatorname{arsinh}\!\left(\frac{3\pi}{\sqrt2}\right).
$$

### Exercise 5

We verify first that reparametrization is an equivalence relation. The identity change of parameter on each subinterval proves reflexivity. If a piece on one partition is identified with a piece on another by a $$C^q$$ diffeomorphism, the inverse diffeomorphism identifies them in the reverse direction, proving symmetry. If two successive reparametrizations use maps $$\varphi_j$$ and $$\psi_j$$ on corresponding pieces, their composition is again a $$C^q$$ diffeomorphism on each piece; this proves transitivity.

To show that the length does not depend on the representative, consider one pair of corresponding subintervals and a change of parameter $$\varphi$$ between them. A monotone bijection carries partitions of one interval bijectively to partitions of the other (with their order reversed if $$\varphi$$ is decreasing). The corresponding polygonal sums are equal, so taking suprema gives

$$
\operatorname{Var}(\gamma_j,[\alpha_{j-1},\alpha_j])
=\operatorname{Var}(\eta_j,[\beta_{j-1},\beta_j]).
$$

By additivity of variation over adjacent intervals,

$$
\operatorname{Var}(\gamma,I)
=\sum_{j=1}^{m}\operatorname{Var}(\gamma_j,[\alpha_{j-1},\alpha_j])
=\sum_{j=1}^{m}\operatorname{Var}(\eta_j,[\beta_{j-1},\beta_j])
=\operatorname{Var}(\eta,J).
$$

Thus $$L(\Gamma):=\operatorname{Var}(\gamma,I)$$ is well defined on the equivalence class. Since each piece is $$C^q$$ with $$q\ge1$$, Theorem 1.3 applies on every compact subinterval and yields

$$
L(\Gamma)
=\sum_{j=1}^{m}L(\Gamma_j)
=\sum_{j=1}^{m}\int_{\alpha_{j-1}}^{\alpha_j}|\dot\gamma_j(t)|\,dt.
$$

### Exercise 6

**(a)** If a piece of a closed curve is reparametrized by an orientation-preserving $$C^q$$ diffeomorphism $$t=\varphi(s)$$, then the chain rule gives

$$
\det\bigl(\gamma(\varphi(s)),(\gamma\circ\varphi)'(s)\bigr)
=\det\bigl(\gamma(\varphi(s)),\dot\gamma(\varphi(s))\bigr)\,\dot\varphi(s).
$$

The substitution rule therefore leaves its contribution to $$A(\Gamma)$$ unchanged. Subdividing or regrouping pieces also leaves the sum of integrals unchanged, by additivity of the integral. Hence the definition is independent of the chosen piecewise $$C^q$$ parametrization and partition. Reversing orientation changes the sign, as expected for oriented area.

**(b)** On the first interval, put $$x=\alpha+\beta-t$$. The path follows the graph of $$f$$ from $$(\beta,0)$$ to $$(\alpha,0)$$. On the second interval it follows the baseline from $$(\alpha,0)$$ back to $$(\beta,0)$$. Since $$f(\alpha)=f(\beta)=0$$, the two pieces join continuously and the path is closed. Under the stated assumption $$f\in C^1$$, it is piecewise $$C^1$$. If the printed $$C^q$$ is meant for arbitrary $$q>1$$ from Exercise 5, the hypothesis must be strengthened to $$f\in C^q$$.

The baseline contributes zero to the determinant integral. On the graph piece,

$$
\gamma(t)=(x,f(x)),\qquad \dot\gamma(t)=(-1,-f'(x)),
$$

so

$$
\det(\gamma(t),\dot\gamma(t))=f(x)-xf'(x).
$$

Changing variables from $$t$$ to $$x$$ gives

$$
2A(\Gamma)=\int_\alpha^\beta\bigl(f(x)-xf'(x)\bigr)\,dx.
$$

Integration by parts and the endpoint conditions give

$$
\int_\alpha^\beta xf'(x)\,dx
=[xf(x)]_\alpha^\beta-\int_\alpha^\beta f(x)\,dx
=-\int_\alpha^\beta f(x)\,dx.
$$

Consequently

$$
A(\Gamma)=\int_\alpha^\beta f(x)\,dx.
$$

**(c)** For the ellipse parametrization $$\gamma(t)=(a\cos t,b\sin t)$$,

$$
\det(\gamma(t),\dot\gamma(t))
=ab(\cos^2t+\sin^2t)=ab.
$$

It follows that

$$
A(\Gamma)=\frac12\int_0^{2\pi}ab\,dt=\pi ab.
$$

**(d)** There is a regularity issue in the printed assertion. At $$t=\pi/4$$, for example, $$\sqrt{\cos(2t)}$$ behaves like a positive constant times $$\sqrt{\pi/4-t}$$ as $$t\uparrow\pi/4$$. Its derivative is unbounded, so the displayed $$\gamma$$ is not $$C^1$$ on the closed pieces in the definition preceding Exercise 5. Thus, literally, it is not a piecewise $$C^\infty$$ parametrization as claimed.

The geometric lemniscate nevertheless has a smooth parametrization, for example

$$
\widetilde\gamma(u)
=\left(\frac{\cos u}{1+\sin^2u},
\frac{\sin u\cos u}{1+\sin^2u}\right),
\qquad 0\le u\le2\pi.
$$

The denominator is positive, and direct calculation gives

$$
(\widetilde x^2+\widetilde y^2)^2
=\widetilde x^2-\widetilde y^2,
$$

the Cartesian equation of the same lemniscate. The right lobe is traversed counterclockwise and the left lobe clockwise. In polar coordinates the locus satisfies $$r^2=\cos(2\theta)$$. The right lobe contributes

$$
\frac12\int_{-\pi/4}^{\pi/4}\cos(2\theta)\,d\theta=\frac12,
$$

and the left lobe contributes the negative of the same value. Their oriented areas cancel, so

$$
A(\Gamma)=0.
$$

The same value follows directly from the displayed path in the exercise: its determinant is $$\cos(2t)$$ on each open piece, and the two improper integrals are $$1$$ and $$-1$$ before multiplication by $$1/2$$.

### Exercise 7

Let the square have side length $$s$$. For the counterclockwise boundary with vertices $$(0,0),(s,0),(s,s),(0,s)$$, the bottom and left edges contribute zero to $$\int\det(\gamma,\dot\gamma)\,dt$$. The right edge contributes $$s^2$$, and the top edge contributes another $$s^2$$. Hence

$$
A(\Gamma)=\frac12(2s^2)=s^2.
$$

For clockwise orientation the sign reverses, so in general $$A(\Gamma)=\pm s^2$$, with the plus sign for counterclockwise traversal.

### Exercise 8

Since $$0\le f\le1$$, each term in the series for $$r$$ is bounded in absolute value by $$2^{-k}$$, and each term in $$\alpha/(2\pi)$$ has the same bound. The Weierstrass M-test gives uniform convergence of both series on $$\mathbb R$$. Their summands are continuous, so $$r$$ and $$\alpha$$ are continuous; therefore

$$
\gamma(t)=r(t)(\cos\alpha(t),\sin\alpha(t))
$$

is continuous. Also,

$$
0\le r(t)\le\sum_{k=1}^{\infty}2^{-k}=1,
$$

so $$\gamma([0,1])\subseteq B$$.

For the reverse inclusion, take a nonzero point $$(x_0,y_0)\in B$$ and choose polar coordinates $$(r_0,\alpha_0)\in[0,1]\times[0,2\pi]$$. Choose binary expansions

$$
r_0=\sum_{k=1}^{\infty}g_k2^{-k},
\qquad
\frac{\alpha_0}{2\pi}=\sum_{k=1}^{\infty}h_k2^{-k},
\qquad g_k,h_k\in\{0,1\}.
$$

Interleave their digits by setting $$a_{2k}=g_k$$ and $$a_{2k-1}=h_k$$. Define

$$
t_0=2\sum_{n=1}^{\infty}a_n3^{-n-1}.
$$

Because $$0\le a_n\le1$$,

$$
0\le t_0\le2\sum_{n=1}^{\infty}3^{-n-1}=\frac13,
$$

so $$t_0\in[0,1]$$. For each $$n\ge1$$, split the series for $$3^nt_0$$ into its integer and fractional parts:

$$
3^nt_0
=2\sum_{j=1}^{n-1}a_j3^{n-j-1}
+\frac{2a_n}{3}
+2\sum_{j=n+1}^{\infty}a_j3^{n-j-1}.
$$

The first term is an even integer. The last term lies in $$[0,1/3]$$. Thus, modulo $$2$$, $$3^nt_0$$ lies in $$[0,1/3]$$ when $$a_n=0$$ and in $$[2/3,1]$$ when $$a_n=1$$. By the defining plateaus of the 2-periodic function $$f$$,

$$
f(3^nt_0)=a_n.
$$

It follows that

$$
r(t_0)
=\sum_{k=1}^{\infty}2^{-k}a_{2k}=r_0,
\qquad
\alpha(t_0)
=2\pi\sum_{k=1}^{\infty}2^{-k}a_{2k-1}=\alpha_0.
$$

Therefore $$\gamma(t_0)=(x_0,y_0)$$. The origin is attained by taking all digits zero. Hence every point of $$B$$ belongs to $$\gamma([0,1])$$, and

$$
\gamma([0,1])=B.
$$
