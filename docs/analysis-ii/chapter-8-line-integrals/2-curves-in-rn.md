# Chapter VIII — Line Integrals

## 2. Curves in $$\mathbb{R}^n$$

These are detailed solutions to Exercises 1–10. Inline formulas use GitBook's double-dollar syntax. For plane curves, curvature is signed as in Proposition 2.10; the usual nonnegative curvature is its absolute value.

### Exercise 1

Let

$$
u(t)=(\cos t,\sin t),\qquad n(t)=(-\sin t,\cos t),
$$

so that $$u'=n$$ and $$n'=-u$$. With $$\gamma(t)=r(t)u(t)$$, we get

$$
\dot\gamma=\dot r\,u+r\,n,\qquad
\ddot\gamma=(\ddot r-r)u+2\dot r\,n.
$$

Since $$(u,n)$$ is a positively oriented orthonormal basis,

$$
\det(\dot\gamma,\ddot\gamma)
=\dot r(2\dot r)-r(\ddot r-r)
=2\dot r^{\,2}-r\ddot r+r^2.
$$

Also,

$$
|\dot\gamma|^2=\dot r^{\,2}+r^2>0.
$$

The signed curvature formula therefore gives

$$
\kappa(t)
=\frac{\det(\dot\gamma(t),\ddot\gamma(t))}{|\dot\gamma(t)|^3}
=\frac{2\dot r(t)^2-r(t)\ddot r(t)+r(t)^2}
{\bigl(r(t)^2+\dot r(t)^2\bigr)^{3/2}}.
$$

### Exercise 2

Apply the polar-coordinate formula from Exercise 1 to each curve. In all three cases, the sign below follows the given direction of parametrization.

**(i) Limacon of Pascal.** Here $$r(t)=1+2\cos t$$, $$\dot r=-2\sin t$$, and $$\ddot r=-2\cos t$$. Thus

$$
2\dot r^{\,2}-r\ddot r+r^2
=8\sin^2t+2\cos t(1+2\cos t)+(1+2\cos t)^2
=9+6\cos t,
$$

while

$$
r^2+\dot r^{\,2}
=(1+2\cos t)^2+4\sin^2t
=5+4\cos t.
$$

Therefore

$$
\kappa(t)=\frac{9+6\cos t}{(5+4\cos t)^{3/2}}.
$$

**(ii) Logarithmic spiral.** Let $$r(t)=e^{\lambda t}$$. Then $$\dot r=\lambda r$$ and $$\ddot r=\lambda^2r$$, so the numerator is $$(1+\lambda^2)r^2$$ and the denominator is $$(1+\lambda^2)^{3/2}r^3$$. Hence

$$
\kappa(t)=\frac{e^{-\lambda t}}{\sqrt{1+\lambda^2}}.
$$

This includes $$\lambda=0$$, the unit circle.

**(iii) Cycloid.** Write

$$
x(t)=R(t-\sin t),\qquad y(t)=R(1-\cos t),\qquad R>0.
$$

Then

$$
\dot x=R(1-\cos t),\quad
\dot y=R\sin t,\quad
\ddot x=R\sin t,\quad
\ddot y=R\cos t.
$$

Consequently,

$$
|\dot\gamma|^2
=2R^2(1-\cos t),\qquad
\det(\dot\gamma,\ddot\gamma)=-R^2(1-\cos t).
$$

The cycloid has cusps at $$t=0$$ and $$t=2\pi$$, where curvature is not defined. At the regular points $$0<t<2\pi$$,

$$
\kappa(t)=-\frac{1}{4R\sin(t/2)}.
$$

The unsigned curvature is $$1/(4R\sin(t/2))$$ on this interval.

### Exercise 3

Let $$v=|\dot\gamma|$$ and $$D=\det(\dot\gamma,\ddot\gamma)=\dot x\ddot y-\ddot x\dot y$$. The unit tangent and its positively rotated unit normal are

$$
e_1=\frac{(\dot x,\dot y)}{v},\qquad
e_2=\frac{(-\dot y,\dot x)}{v}.
$$

By the signed-curvature formula, $$\kappa=D/v^3$$. The center of curvature, which parametrizes the evolute, is

$$
m=\gamma+\frac{1}{\kappa}e_2.
$$

Since $$1/\kappa=v^3/D$$, this becomes

$$
m
=(x,y)+\frac{\dot x^2+\dot y^2}{D}(-\dot y,\dot x)
=\left(
x-\frac{\dot x^2+\dot y^2}{\dot x\ddot y-\ddot x\dot y}\,\dot y,\
y+\frac{\dot x^2+\dot y^2}{\dot x\ddot y-\ddot x\dot y}\,\dot x
\right).
$$

The assumption $$\kappa\ne0$$ ensures that the denominator never vanishes.

### Exercise 4

We use the evolute formula $$m=\gamma+e_2/\kappa$$.

**(a) Parabola.** Parametrize $$y=x^2/2$$ by

$$
\gamma(t)=\left(t,\frac{t^2}{2}\right).
$$

Here $$\dot\gamma=(1,t)$$, $$|\dot\gamma|^2=1+t^2$$, and $$\det(\dot\gamma,\ddot\gamma)=1$$. Thus

$$
m
=\left(t,\frac{t^2}{2}\right)
+(1+t^2)(-t,1)
=\left(-t^3,1+\frac{3t^2}{2}\right),
$$

which is the stated semicubical parabola.

**(b) Logarithmic spiral.** Put $$u(t)=(\cos t,\sin t)$$ and $$w(t)=(-\sin t,\cos t)$$, and let $$q=\sqrt{1+\lambda^2}$$. For $$\gamma(t)=e^{\lambda t}u(t)$$,

$$
\dot\gamma=e^{\lambda t}(\lambda u+w),\qquad
e_1=\frac{\lambda u+w}{q},\qquad
e_2=\frac{\lambda w-u}{q},\qquad
\kappa=\frac{e^{-\lambda t}}{q}.
$$

Therefore

$$
m
=e^{\lambda t}u+\frac{e_2}{\kappa}
=e^{\lambda t}u+e^{\lambda t}(\lambda w-u)
=\lambda e^{\lambda t}w.
$$

With $$s=t+\pi/2$$, we have $$w(t)=u(s)$$ and obtain

$$
m=\lambda e^{\lambda(s-\pi/2)}(\cos s,\sin s),
$$

the parametrization in the exercise. If $$\lambda=0$$, the original curve is the unit circle and its evolute is the single point at the origin; the displayed formula degenerates to that point.

**(c) Cycloid.** Let $$\gamma(t)=(t-\sin t,1-\cos t)$$. At its regular points,

$$
|\dot\gamma|^2=2(1-\cos t),\qquad
\det(\dot\gamma,\ddot\gamma)=-(1-\cos t),
$$

so $$|\dot\gamma|^2/\det(\dot\gamma,\ddot\gamma)=-2$$. As in Exercise 3,

$$
m
=\gamma-2(-\sin t,1-\cos t)
=(t+\sin t,\cos t-1).
$$

This formula extends continuously over the cusp parameters and is the stated cycloid.

### Exercise 5

Let $$v(t)=|\dot\gamma(t)|$$. For the positively rotated unit normal $$e_2$$, the planar Frenet formulas in this parameter are

$$
\dot e_1=v\kappa e_2,\qquad
\dot e_2=-v\kappa e_1,\qquad
\dot\gamma=ve_1.
$$

By assumption, $$\kappa$$ and $$\dot\kappa$$ never vanish. Because $$\gamma\in C^3$$, both $$e_2$$ and $$\kappa$$ are continuously differentiable, so $$m=\gamma+\kappa^{-1}e_2$$ is a $$C^1$$ curve. Differentiating and applying the formulas above,

$$
\begin{aligned}
\dot m
&=ve_1-\frac{\dot\kappa}{\kappa^2}e_2+\frac{1}{\kappa}(-v\kappa e_1)\\
&=-\frac{\dot\kappa}{\kappa^2}e_2.
\end{aligned}
$$

Since $$\dot\kappa\ne0$$, this derivative never vanishes. This proves **(a)**: $$M$$ is regular and $$C^1$$.

For **(b)**, the tangent to $$\Gamma$$ is spanned by $$e_1$$ and the tangent to $$M$$ is spanned by $$\dot m$$, which is a nonzero multiple of $$e_2$$. The two tangents are perpendicular.

For **(c)**, the same derivative gives the speed of $$m$$:

$$
|\dot m(t)|=\frac{|\dot\kappa(t)|}{\kappa(t)^2}.
$$

Integrating over $$J$$ yields

$$
L(M)=\int_J|\dot m(t)|\,dt
=\int_J|\dot\kappa(t)|\,\kappa(t)^{-2}\,dt.
$$

### Exercise 6

Let $$u(t)=(\cos t,\sin t)$$ and $$w(t)=(-\sin t,\cos t)$$. The spiral and its velocity are

$$
\gamma(t)=e^{\lambda t}u(t),\qquad
\dot\gamma(t)=e^{\lambda t}\bigl(\lambda u(t)+w(t)\bigr).
$$

Because $$u$$ and $$w$$ are orthonormal,

$$
|\lambda u+w|=\sqrt{1+\lambda^2},\qquad
|\det(u,\lambda u+w)|=1.
$$

Thus the sine of the angle between the tangent line and the radial line $$\mathbb{R}u(t)$$ is

$$
\frac{|\det(\gamma(t),\dot\gamma(t))|}
{|\gamma(t)|\,|\dot\gamma(t)|}
=\frac{1}{\sqrt{1+\lambda^2}},
$$

independent of $$t$$. Hence the angle is constant along the spiral.

### Exercise 7

For a regular space curve with $$\dot\gamma\times\ddot\gamma\ne0$$, use

$$
\kappa=\frac{|\dot\gamma\times\ddot\gamma|}{|\dot\gamma|^3},
\qquad
\tau=\frac{\det(\dot\gamma,\ddot\gamma,\dddot\gamma)}
{|\dot\gamma\times\ddot\gamma|^2}.
$$

**(a) Elliptic helix.** Let

$$
\gamma(t)=(a\cos t,b\sin t,ct),\qquad ab\ne0.
$$

Then

$$
\dot\gamma=(-a\sin t,b\cos t,c),\quad
\ddot\gamma=(-a\cos t,-b\sin t,0),\quad
\dddot\gamma=(a\sin t,-b\cos t,0).
$$

In particular,

$$
\dot\gamma\times\ddot\gamma
=(bc\sin t,-ac\cos t,ab),
$$

and

$$
|\dot\gamma|^2=a^2\sin^2t+b^2\cos^2t+c^2,\qquad
|\dot\gamma\times\ddot\gamma|^2
=a^2b^2+c^2(b^2\sin^2t+a^2\cos^2t).
$$

The triple product is

$$
\det(\dot\gamma,\ddot\gamma,\dddot\gamma)
=(\dot\gamma\times\ddot\gamma)\cdot\dddot\gamma
=abc.
$$

Therefore

$$
\kappa(t)
=\frac{\sqrt{a^2b^2+c^2(b^2\sin^2t+a^2\cos^2t)}}
{(a^2\sin^2t+b^2\cos^2t+c^2)^{3/2}},
\qquad
\tau(t)
=\frac{abc}{a^2b^2+c^2(b^2\sin^2t+a^2\cos^2t)}.
$$

**(b) The curve $$\gamma(t)=t(\cos t,\sin t,1)$$.** Its first derivatives are

$$
\begin{aligned}
\dot\gamma&=(\cos t-t\sin t,\ \sin t+t\cos t,\ 1),\\
\ddot\gamma&=(-2\sin t-t\cos t,\ 2\cos t-t\sin t,\ 0),\\
\dddot\gamma&=(-3\cos t+t\sin t,\ -3\sin t-t\cos t,\ 0).
\end{aligned}
$$

Direct calculation gives

$$
|\dot\gamma|^2=t^2+2,\qquad
\dot\gamma\times\ddot\gamma
=(t\sin t-2\cos t,\ -2\sin t-t\cos t,\ t^2+2),
$$

and hence

$$
|\dot\gamma\times\ddot\gamma|^2=t^4+5t^2+8,\qquad
\det(\dot\gamma,\ddot\gamma,\dddot\gamma)=t^2+6.
$$

It follows that

$$
\kappa(t)=\frac{\sqrt{t^4+5t^2+8}}{(t^2+2)^{3/2}},
\qquad
\tau(t)=\frac{t^2+6}{t^4+5t^2+8}.
$$

### Exercise 8

We first prove the inequality when $$L(\Gamma)=2\pi$$. Parametrize the curve by arc length as a closed curve $$\gamma:[0,2\pi]\to\mathbb{C}$$, so $$|\dot\gamma(t)|=1$$. Its Fourier coefficients are

$$
\widehat\gamma_k
=\frac{1}{2\pi}\int_0^{2\pi}\gamma(t)e^{-ikt}\,dt,
\qquad k\in\mathbb{Z}.
$$

Parseval's identity applied to $$\dot\gamma$$ gives

$$
1=\frac{1}{2\pi}\int_0^{2\pi}|\dot\gamma(t)|^2\,dt
=\sum_{k\in\mathbb{Z}}k^2|\widehat\gamma_k|^2.
$$

The signed area enclosed by a positively oriented parametrization is

$$
A(\Gamma)=\frac12\int_0^{2\pi}
\operatorname{Im}\bigl(\overline{\gamma(t)}\,\dot\gamma(t)\bigr)\,dt.
$$

Using the Fourier series in this integral yields

$$
A(\Gamma)=\pi\sum_{k\in\mathbb{Z}}k|\widehat\gamma_k|^2.
$$

For every integer $$k$$, $$|k|\le k^2$$ when $$k\ne0$$, and the $$k=0$$ term contributes zero. Therefore

$$
|A(\Gamma)|
\le\pi\sum_{k\in\mathbb{Z}}|k||\widehat\gamma_k|^2
\le\pi\sum_{k\in\mathbb{Z}}k^2|\widehat\gamma_k|^2
=\pi.
$$

For a curve of arbitrary length $$L(\Gamma)>0$$, dilate it by the factor $$2\pi/L(\Gamma)$$. The dilated curve has length $$2\pi$$ and its area is multiplied by $$\bigl(2\pi/L(\Gamma)\bigr)^2$$. Applying the result just proved gives

$$
\left(\frac{2\pi}{L(\Gamma)}\right)^2|A(\Gamma)|\le\pi,
\qquad\text{hence}\qquad
4\pi|A(\Gamma)|\le L(\Gamma)^2.
$$

For positive orientation this is the stated inequality. The absolute value makes the assertion independent of the chosen orientation. Equality holds for a circle traversed once.

### Exercise 9

The speed of the curve $$t\mapsto\gamma(\lambda,t)$$ is

$$
v(\lambda,t):=|\partial_2\gamma(\lambda,t)|.
$$

The hint's displayed $$|\partial_1\gamma|$$ cannot be the speed here: $$\partial_1$$ denotes differentiation in the family parameter $$\lambda$$. We use $$v=|\partial_2\gamma|$$, the speed in $$t$$.

For fixed $$\lambda$$, let $$e_1$$ be the unit tangent and $$n$$ the unit normal of $$\Gamma_\lambda$$. Since $$\partial_1\gamma=\kappa n$$, differentiating with respect to $$t$$ gives

$$
\partial_1\partial_2\gamma
=\partial_2(\kappa n)
=(\partial_2\kappa)n+\kappa\,\partial_2n.
$$

The Frenet formula is $$\partial_2n=-v\kappa e_1$$, while $$\partial_2\gamma=ve_1$$. Differentiating the norm and using $$e_1\perp n$$,

$$
\begin{aligned}
\partial_1v
&=\frac{\langle\partial_2\gamma,\partial_1\partial_2\gamma\rangle}{v}\\
&=\frac{\langle ve_1,(\partial_2\kappa)n-v\kappa^2e_1\rangle}{v}\\
&=-\kappa^2v.
\end{aligned}
$$

Because $$\gamma\in C^3(U,\mathbb{R}^2)$$ and $$v>0$$ on the compact set $$I\times J$$, differentiation under the integral sign is valid:

$$
\ell'(\lambda)
=\frac{d}{d\lambda}\int_Jv(\lambda,t)\,dt
=-\int_J\kappa_{\Gamma_\lambda}(t)^2v(\lambda,t)\,dt.
$$

Finally, $$ds=v(\lambda,t)\,dt$$ is the arc-length element on $$\Gamma_\lambda$$. Thus

$$
\ell'(\lambda)
=-\int_0^{\ell(\lambda)}
\kappa_{\Gamma_\lambda}(s(\lambda))^2\,ds(\lambda),
$$

as required. The integral representation also shows that $$\ell'$$ is continuous.

### Exercise 10

Let the first column of $$T\in SO(2)$$ be $$u=(a,c)$$. Since $$T$$ is orthogonal, $$|u|=1$$, so there is a unique angle $$\alpha\in[0,2\pi)$$ such that

$$
a=\cos\alpha,\qquad c=\sin\alpha.
$$

The second column must be a unit vector perpendicular to $$u$$. The two possibilities are $$(-c,a)$$ and $$(c,-a)$$; the determinant condition $$\det T=1$$ selects $$(-c,a)$$. Consequently,

$$
T=
\begin{pmatrix}
\cos\alpha&-\sin\alpha\\
\sin\alpha&\cos\alpha
\end{pmatrix}.
$$

The uniqueness of $$\alpha$$ in the half-open interval $$[0,2\pi)$$ follows from the one-to-one parametrization of the unit circle by that interval.
