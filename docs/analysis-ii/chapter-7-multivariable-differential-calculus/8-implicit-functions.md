# Chapter VII — Multivariable Differential Calculus

## 8. Implicit functions

These are detailed solutions to Exercises 1–12. Inline mathematics uses GitBook’s `$$...$$` syntax; displayed calculations use the same delimiters on separate lines.

### Exercise 1

Define

$$
F(x,y,u,v)=\bigl(x^2+y^2-u^2-v,\ x^2+2y^2+3u^2+4v^2-1\bigr).
$$

At $$(x_0,y_0,u_0,v_0)=(1/2,0,1/2,0)$$, we have $$F(x_0,y_0,u_0,v_0)=0$$. The derivative with respect to the variables to be solved for is

$$
D_{(u,v)}F(x_0,y_0,u_0,v_0)
=\begin{pmatrix}-2u_0&-1\\6u_0&8v_0\end{pmatrix}
=\begin{pmatrix}-1&-1\\3&0\end{pmatrix},
\qquad
\det D_{(u,v)}F=3\ne0.
$$

The implicit function theorem therefore gives unique smooth functions $$u=u(x,y)$$ and $$v=v(x,y)$$ near $$(x_0,y_0)$$ with $$u(x_0,y_0)=1/2$$, $$v(x_0,y_0)=0$$, and $$F(x,y,u(x,y),v(x,y))=0$$.

Differentiate this identity with respect to $$x$$ and $$y$$. At the base point, the derivatives of $$F$$ with respect to $$(x,y)$$ are

$$
D_{(x,y)}F=\begin{pmatrix}2x&2y\\2x&4y\end{pmatrix}
=\begin{pmatrix}1&0\\1&0\end{pmatrix}.
$$

Thus the implicit derivative formula gives

$$
D(u,v)(x_0,y_0)
=-\bigl(D_{(u,v)}F\bigr)^{-1}D_{(x,y)}F
=-\frac13\begin{pmatrix}0&1\\-3&-1\end{pmatrix}
\begin{pmatrix}1&0\\1&0\end{pmatrix}
=\begin{pmatrix}-1/3&0\\4/3&0\end{pmatrix}.
$$

Therefore

$$
u_x= -\frac13,\qquad u_y=0,\qquad v_x=\frac43,\qquad v_y=0
\quad\text{at }(x,y)=(1/2,0).
$$

### Exercise 2

For each $$x\in X$$, write

$$
C(x):E\to F\times G,\qquad C(x)e=(A(x)e,B(x)e).
$$

The hypothesis says that $$C(x)$$ is an isomorphism. Since inversion is continuously differentiable on the open set of bounded linear isomorphisms, $$x\mapsto C(x)^{-1}$$, and hence $$\varphi(x)=C(x)^{-1}(f,g)$$, is continuously differentiable. Its defining equation is

$$
A(x)\varphi(x)=f,\qquad B(x)\varphi(x)=g.
$$

Fix $$h\in H$$ and differentiate both identities at $$x$$ in the direction $$h$$. The product rule gives

$$
\partial A(x)h\,\varphi(x)+A(x)\partial\varphi(x)h=0,
\qquad
\partial B(x)h\,\varphi(x)+B(x)\partial\varphi(x)h=0.
$$

Combining them in $$F\times G$$ and applying $$C(x)^{-1}$$ yields

$$
\partial\varphi(x)h=-C(x)^{-1}\bigl(\partial A(x)h\,\varphi(x),\ \partial B(x)h\,\varphi(x)\bigr).
$$

By definition, $$S(x)k=C(x)^{-1}(k,0)$$ and $$T(x)\ell=C(x)^{-1}(0,\ell)$$. Since $$C(x)^{-1}$$ is linear, splitting the pair gives exactly

$$
\partial\varphi(x)h
=-S(x)\bigl(\partial A(x)h\,\varphi(x)\bigr)
-T(x)\bigl(\partial B(x)h\,\varphi(x)\bigr).
$$

### Exercise 3

Fix any $$t_0\in J$$ and put

$$
A(t)=\int_{t_0}^t a(s)\,ds.
$$

Multiplying $$\dot x=a(t)x+b(t)$$ by the integrating factor $$e^{-A(t)}$$ gives

$$
\frac{d}{dt}\bigl(e^{-A(t)}x(t)\bigr)=e^{-A(t)}b(t).
$$

Integration shows that all solutions on $$J$$ are

$$
x(t)=e^{A(t)}\left(C+\int_{t_0}^t e^{-A(s)}b(s)\,ds\right),\qquad C\in\mathbb R.
$$

Equivalently, choosing an initial value $$x(t_0)=x_0$$ means taking $$C=x_0$$. Differentiating this formula verifies the equation, and the arbitrary constant accounts for every possible initial value.

### Exercise 4

The equation is considered on intervals that do not contain $$t=0$$ and on which $$x(t)/t\in D$$. Set $$y(t)=x(t)/t$$, so $$x(t)=t y(t)$$. Differentiating gives

$$
\dot x(t)=y(t)+t\dot y(t).
$$

Thus $$\dot x=f(x/t)$$ is equivalent to

$$
y+t\dot y=f(y)
\quad\Longleftrightarrow\quad
\dot y=\frac{f(y)-y}{t}.
$$

Conversely, if $$y$$ solves the latter equation, then $$x(t)=t y(t)$$ satisfies $$\dot x=y+t\dot y=f(y)=f(x/t)$$. This proves the claimed equivalence wherever $$t\ne0$$.

### Exercise 5

Here $$f(y)=y^2+y+1$$, so Exercise 4 transforms the equation into

$$
\dot y=\frac{y^2+1}{t}.
$$

Separating variables and integrating on an interval where $$t\ne0$$ gives

$$
\frac{dy}{1+y^2}=\frac{dt}{t},
\qquad
\arctan y=\ln|t|+C.
$$

Consequently the general solution is

$$
x(t)=t\tan\bigl(\ln|t|+C\bigr),\qquad C\in\mathbb R.
$$

Each solution is restricted to a connected interval on which $$t\ne0$$ and $$\ln|t|+C$$ avoids the poles $$\pi/2+k\pi$$ of the tangent. Substitution into the original equation confirms the formula.

### Exercise 6

Rewrite the equation as $$\dot x=-t x^2$$. The initial value $$x(0)=2$$ is nonzero, so separation is valid near zero:

$$
\frac{d}{dt}\left(\frac1{x(t)}\right)
=-\frac{\dot x(t)}{x(t)^2}=t.
$$

Integrating from $$0$$ to $$t$$ and using $$1/x(0)=1/2$$ gives

$$
\frac1{x(t)}=\frac12+\frac{t^2}{2},
\qquad
x(t)=\frac{2}{1+t^2}.
$$

The denominator never vanishes, and direct differentiation verifies the equation for every $$t\in\mathbb R$$. The vector field is locally Lipschitz, so this global solution is the unique solution of the initial value problem.

### Exercise 7

Where the real power is defined and $$x(t)\ne0$$, set $$y=x^{1-\alpha}$$. The chain rule and the Bernoulli equation give

$$
\dot y=(1-\alpha)x^{-\alpha}\dot x
=(1-\alpha)x^{-\alpha}\bigl(a(t)x+b(t)x^\alpha\bigr)
=(1-\alpha)\bigl(a(t)y+b(t)\bigr).
$$

This is linear in $$y$$. To make the reduction explicit, put $$k=1-\alpha\ne0$$ and $$A(t)=\int_{t_0}^t a(s)\,ds$$. Its general solution is

$$
y(t)=e^{kA(t)}\left(C+k\int_{t_0}^t e^{-kA(s)}b(s)\,ds\right).
$$

On any interval where this expression stays in the range needed for the chosen real power, recover $$x$$ by $$x=y^{1/k}$$. The transformation is made only on regions where it is defined; for example, for arbitrary real $$\alpha$$ it applies directly to positive solutions.

When $$\alpha>0$$, the identically zero function is also a solution of the original equation and is not represented by this nonzero change of variables.

### Exercise 8

The constant functions $$u=0$$ and $$u=\alpha/\beta$$ are equilibria. For any nonzero solution, set $$z=1/u$$. Then

$$
\dot z=-\frac{\dot u}{u^2}=-\alpha z+\beta.
$$

Solving this linear equation gives the nonconstant family

$$
z(t)=\frac{\beta}{\alpha}+C e^{-\alpha t},
\qquad
u(t)=\frac{\alpha}{\beta+K e^{-\alpha t}},
$$

where $$K=\alpha C$$. The case $$K=0$$ is the equilibrium $$u=\alpha/\beta$$; the zero equilibrium must be added separately. The formula is valid on each maximal interval not containing a zero of its denominator. If $$K\ge0$$, it is defined for all $$t\in\mathbb R$$. If $$K<0$$, the denominator vanishes at

$$
t_* =\frac1\alpha\ln\left(\frac{-K}{\beta}\right),
$$

so there are two maximal branches, $$(-\infty,t_*)$$ and $$(t_*,\infty)$$. In the notation of the maximal interval $$J=(t_-,t_+)$$, this gives

$$
\lim_{t\to t_+}u(t)=
\begin{cases}
-\infty,&K<0\text{ on }(-\infty,t_*),\\
\alpha/\beta,&K\ge0\text{ or on }(t_*,\infty),
\end{cases}
$$

and the zero solution also has limit $$0$$ as $$t\to+\infty$$.

For a nonconstant solution,

$$
\dot u=u(\alpha-\beta u),
\qquad
\ddot u=\dot u(\alpha-2\beta u).
$$

It never reaches either equilibrium, by uniqueness, so it has no local maximum or minimum in the interior of its interval. If “turning point” means the inflection point of the logistic curve, it occurs exactly when $$u=\alpha/(2\beta)$$. This level is attained precisely for $$K>0$$, at

$$
t_{\mathrm{inf}}=\frac1\alpha\ln\left(\frac K\beta\right),
\qquad
u(t_{\mathrm{inf}})=\frac{\alpha}{2\beta}.
$$

The zero solution and the two equilibrium solutions are constant and have no isolated turning point.

### Exercise 9

On an interval where $$t\ne0$$, put $$y=x/t$$, so $$x=ty$$ and $$\dot x=y+t\dot y$$. The original equation also requires $$y\ne1$$. Substitution gives

$$
y+t\dot y=\frac{1+y}{1-y},
\qquad
t\dot y=\frac{1+y^2}{1-y}.
$$

Separating and integrating,

$$
\frac{1-y}{1+y^2}\,dy=\frac{dt}{t},
\qquad
\arctan y-\frac12\ln(1+y^2)=\ln|t|+C.
$$

Thus the general solution is given implicitly by this relation with $$y=x/t$$, or equivalently by

$$
\arctan(x/t)-\frac12\ln(t^2+x^2)=C
$$

on each branch where a continuous choice of the angle is fixed. These level curves are logarithmic spirals in the $$(t,x)$$-plane. They must avoid the singular line $$x=t$$. The substitution derivation covers $$t\ne0$$; a solution can continue through $$t=0$$ when $$x(0)\ne0$$, using the same relation with a continuous angle branch.

### Exercise 10

The maximal solution interval is the connected interval containing $$0$$ on which the explicit solution stays finite and in the domain of the vector field.

**(a)** For $$\dot x=x^{1+\alpha}$$ with $$\alpha>0$$ and initial value $$\xi>0$$, separation gives

$$
x^{-1-\alpha}\,dx=dt,
\qquad
x(t)^{-\alpha}=\xi^{-\alpha}-\alpha t.
$$

Hence

$$
u(t,\xi)=\bigl(\xi^{-\alpha}-\alpha t\bigr)^{-1/\alpha},
\qquad
J(\xi)=\left(-\infty,\frac{\xi^{-\alpha}}{\alpha}\right)
\quad(\xi>0).
$$

If the vector field is defined at zero by $$f(0)=0$$, then $$\xi=0$$ gives the equilibrium $$u(t,0)=0$$ on all of $$\mathbb R$$. For negative $$\xi$$, the statement $$x\mapsto x^{1+\alpha}$$ as a map $$\mathbb R\to\mathbb R$$ needs a real-valued, locally Lipschitz convention for the power on negative inputs; the usual real power for arbitrary real $$\alpha$$ does not define such a map there. If $$\alpha$$ is a positive integer, the negative branches are

$$
u(t,\xi)=
\begin{cases}
-\bigl(|\xi|^{-\alpha}-\alpha t\bigr)^{-1/\alpha},
&\xi<0,\ \alpha\text{ even},\ t<|\xi|^{-\alpha}/\alpha,\\[2mm]
-\bigl(|\xi|^{-\alpha}+\alpha t\bigr)^{-1/\alpha},
&\xi<0,\ \alpha\text{ odd},\ t>-|\xi|^{-\alpha}/\alpha.
\end{cases}
$$

These intervals are the maximal ones containing $$0$$. In particular, for the usual nonnegative initial-value branch, the domain is $$\{(t,\xi):\xi=0\}\cup\{(t,\xi):\xi>0,\ t<\xi^{-\alpha}/\alpha\}$$; include the corresponding negative branch only when the stated real-power convention permits it.

**(b)** For $$\dot x=Ax$$, where $$A\in L(E)$$, the operator exponential

$$
e^{tA}=\sum_{n=0}^{\infty}\frac{t^nA^n}{n!}
$$

converges in operator norm for every real $$t$$. Termwise differentiation gives $$\frac{d}{dt}e^{tA}=Ae^{tA}$$ and $$e^{0A}=I_E$$, so the unique solution is $$u(t,\xi)=e^{tA}\xi$$ for all $$t\in\mathbb R$$. Thus

$$
D(f)=\mathbb R\times E.
$$

**(c)** For $$\dot x=1+x^2$$, separation gives

$$
\arctan x(t)=t+\arctan\xi,
\qquad
u(t,\xi)=\tan\bigl(t+\arctan\xi\bigr).
$$

The solution blows up at the first tangent poles in either time direction. Its maximal interval containing $$0$$ is

$$
J(\xi)=\left(-\frac\pi2-\arctan\xi,\ \frac\pi2-\arctan\xi\right),
$$

and therefore

$$
D(f)=\left\{(t,\xi)\in\mathbb R^2:
-\frac\pi2-\arctan\xi<t<\frac\pi2-\arctan\xi\right\}.
$$

### Exercise 11

Use the notation from the Picard–Lindelöf proof: $$I=[t_0-\alpha,t_0+\alpha]$$, $$\|f(t,x)\|\le M$$ on the chosen rectangle, and $$f$$ is Lipschitz in $$x$$ with constant $$L$$. The interval size was chosen so that $$L\alpha\le1/2$$. The successive approximations are

$$
u_0(t)=x_0,
\qquad
u_{m+1}(t)=x_0+\int_{t_0}^{t}f(s,u_m(s))\,ds.
$$

For $$m=0$$,

$$
\|u_1(t)-u_0(t)\|
=\left\|\int_{t_0}^{t}f(s,x_0)\,ds\right\|
\le M|t-t_0|.
$$

Assume inductively that

$$
\|u_{m+1}(t)-u_m(t)\|
\le \frac{M L^m|t-t_0|^{m+1}}{(m+1)!}.
$$

The Lipschitz estimate and integration from $$t_0$$ to $$t$$ (with the same absolute-value estimate when $$t<t_0$$) give

$$
\begin{aligned}
\|u_{m+2}(t)-u_{m+1}(t)\|
&\le L\left|\int_{t_0}^{t}\|u_{m+1}(s)-u_m(s)\|\,ds\right|\\
&\le \frac{M L^{m+1}|t-t_0|^{m+2}}{(m+2)!}.
\end{aligned}
$$

This proves the hinted bound for every $$m\ge0$$. Taking the supremum over $$I$$ and using $$|t-t_0|\le\alpha$$ and $$L\alpha\le1/2$$ yields

$$
\|u_{m+1}-u_m\|_{C(I,E)}
\le \frac{M\alpha(L\alpha)^m}{(m+1)!}
\le \frac{M\alpha\,2^{-m}}{(m+1)!}.
$$

Since $$u_m\to u$$ uniformly, the telescoping series and the estimate above imply

$$
\begin{aligned}
\|u_m-u\|_{C(I,E)}
&\le \sum_{j=m}^{\infty}\|u_{j+1}-u_j\|_{C(I,E)}\\
&\le M\alpha\sum_{j=m}^{\infty}\frac{2^{-j}}{(j+1)!}\\
&<\frac{M\alpha}{2^m(m+1)!}\sum_{k=0}^{\infty}\frac{2^{-k}}{k!}
=\frac{M\alpha\sqrt e}{2^m(m+1)!}.
\end{aligned}
$$

For the last inequality, write $$j=m+k$$ and use $$ (m+k+1)!\ge(m+1)!k!$$. This is the improved error estimate in Remark 8.15(b).

### Exercise 12

Fix an arbitrary compact interval $$I\subset J$$ containing $$t_0$$. On $$I$$, continuity gives finite constants

$$
L=\max_{t\in I}\|A(t)\|,
\qquad
M=\max_{t\in I}\|A(t)x_0+b(t)\|.
$$

Define Picard iterates by

$$
u_0(t)=x_0,
\qquad
u_{n+1}(t)=x_0+\int_{t_0}^{t}\bigl(A(s)u_n(s)+b(s)\bigr)\,ds.
$$

The first difference obeys $$\|u_1(t)-u_0(t)\|\le M|t-t_0|$$. Applying the bound $$\|A(s)z\|\le L\|z\|$$ successively inside the integral gives, by induction,

$$
\|u_{n+1}(t)-u_n(t)\|
\le \frac{M L^n|t-t_0|^{n+1}}{(n+1)!}.
$$

The induction step integrates $$|s-t_0|^{n+1}$$; in particular the first repeated integral is $$\int_{t_0}^{t}\int_{t_0}^{s}d\sigma\,ds=(t-t_0)^2/2$$. Since $$|t-t_0|$$ is bounded on $$I$$, the factorial denominator shows that the series of successive differences converges uniformly. Thus $$u_n$$ converges uniformly to a continuous function $$u:I\to E$$. Passing to the limit in the integral equation is valid by uniform convergence and boundedness of $$A$$, so

$$
u(t)=x_0+\int_{t_0}^{t}\bigl(A(s)u(s)+b(s)\bigr)\,ds.
$$

The integrand is continuous, hence the fundamental theorem of calculus implies $$u\in C^1(I,E)$$, $$u(t_0)=x_0$$, and $$\dot u(t)=A(t)u(t)+b(t)$$.

For uniqueness, if $$u,v$$ are two solutions with the same initial value, their difference satisfies $$w(t)=\int_{t_0}^{t}A(s)w(s)\,ds$$. Let $$C=\max_{s\in I}\|w(s)\|$$. Iterating this relation gives

$$
\|w(t)\|\le \frac{C L^n|t-t_0|^n}{n!}
\quad\text{for every }n\ge0.
$$

The right-hand side tends to zero, so $$w=0$$ on $$I$$. Every point of the open interval $$J$$ lies in a compact subinterval of $$J$$ containing $$t_0$$. Applying this construction on such intervals and using uniqueness on overlaps gives one solution on all of $$J$$. It is unique there, so the initial value problem has a unique global solution.
