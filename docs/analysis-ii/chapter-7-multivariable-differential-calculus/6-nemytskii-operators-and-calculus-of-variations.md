# Chapter VII — Multivariable Differential Calculus

## 6. Nemytskii operators and the calculus of variations

These are detailed solutions to Exercises 1–12. For inline mathematics, this page uses GitBook’s `$$...$$` syntax; displayed calculations use the same delimiters on separate lines.

### Exercise 1

Let $$I=[\alpha,\beta]$$ and define the Nemytskii map $$N_\varphi:C(I,E)\to C(I,F)$$ by

$$
N_\varphi(u)(s)=\varphi(s,u(s)).
$$

Since $$\varphi\in C^{0,1}(I\times E,F)$$, the Nemytskii theorem gives $$N_\varphi\in C^1(C(I,E),C(I,F))$$ and

$$
DN_\varphi(u)h(s)=\partial_2\varphi(s,u(s))h(s).
$$

Now define the integral operator $$K:C(I,F)\to C(I,F)$$ by

$$
(Kv)(t)=\int_\alpha^\beta k(t,s)v(s)\,ds.
$$

It is linear and bounded, because

$$
\|Kv\|_{C(I,F)}\le (\beta-\alpha)\|k\|_{C(I\times I)}\|v\|_{C(I,F)}.
$$

It maps into $$C(I,F)$$: uniform continuity of $$k$$ on the compact set $$I\times I$$ implies that $$Kv(t)$$ varies continuously with $$t$$. The operator in the exercise is the composition $$\Phi=K\circ N_\varphi$$. Hence $$\Phi\in C^1(C(I,E),C(I,F))$$, and the chain rule gives

$$
D\Phi(u)h(t)=K(DN_\varphi(u)h)(t)
=\int_\alpha^\beta k(t,s)\,\partial_2\varphi(s,u(s))h(s)\,ds.
$$

This is the asserted formula for every $$t\in I$$.

### Exercise 2

Both iterated integrals exist because $$f$$ is continuous on the compact rectangle $$I\times J$$. Choose partitions of $$I$$ and $$J$$ with mesh tending to zero, and choose tags $$s_i\in I_i$$ and $$t_j\in J_j$$. The corresponding rectangular Riemann sum is

$$
S=\sum_{i,j} f(s_i,t_j)\,|I_i|\,|J_j|.
$$

If we first integrate in $$s$$ and then in $$t$$, these same sums are grouped by $$j$$; if we integrate in $$t$$ and then in $$s$$, they are grouped by $$i$$. The sums are identical, and continuity on a compact set makes them converge in $$E$$ to the respective iterated integrals. Therefore

$$
\int_J\left(\int_I f(s,t)\,ds\right)dt
=\int_I\left(\int_J f(s,t)\,dt\right)ds.
$$

This is the Riemann-integral form of Fubini’s theorem for a continuous function on a compact rectangle.

### Exercise 3

The left side integrates over the triangular region $$\alpha\le \tau\le t\le s$$. Reversing the order of integration on that region gives

$$
\begin{aligned}
\int_\alpha^s\left(\int_\alpha^t f(\tau)\,d\tau\right)dt
&=\int_\alpha^s\left(\int_\tau^s dt\right)f(\tau)\,d\tau\\
&=\int_\alpha^s(s-\tau)f(\tau)\,d\tau.
\end{aligned}
$$

Renaming the dummy variable $$\tau$$ as $$t$$ proves the claimed identity. It also follows directly by differentiating both sides with respect to $$s$$ and checking that both vanish at $$s=\alpha$$.

### Exercise 4

Fix $$ (x,y)\in\mathbb R^2\setminus(I\times J)$$. Since $$I\times J$$ is compact, a neighborhood of $$(x,y)$$ has positive distance from every $$(s,t)\in I\times J$$. Thus the logarithm in the integrand is smooth in $$(x,y)$$ there, and its first two derivatives can be passed under the integral sign.

Put $$r^2=(x-s)^2+(y-t)^2$$. At points where $$r>0$$,

$$
\begin{aligned}
\partial_x^2\log r^2&=\frac{2}{r^2}-\frac{4(x-s)^2}{r^4},\\
\partial_y^2\log r^2&=\frac{2}{r^2}-\frac{4(y-t)^2}{r^4}.
\end{aligned}
$$

Adding these equations and using $$r^2=(x-s)^2+(y-t)^2$$ yields

$$
\Delta_{x,y}\log\bigl((x-s)^2+(y-t)^2\bigr)=\frac{4}{r^2}-\frac{4r^2}{r^4}=0.
$$

Consequently,

$$
\Delta u(x,y)=\int_I\int_J \rho(s,t)\,\Delta_{x,y}\log\bigl((x-s)^2+(y-t)^2\bigr)\,dt\,ds=0.
$$

So $$u$$ is harmonic on $$\mathbb R^2\setminus(I\times J)$$.

### Exercise 5

For $$s>0$$, every derivative of $$h(s)=e^{-1/s^2}$$ is a polynomial in $$1/s$$ times $$e^{-1/s^2}$$. Since the exponential tends to zero faster than every power of $$1/s$$ as $$s\downarrow0$$, all right derivatives tend to zero at zero. On $$(-\infty,0]$$ the function and all its derivatives are zero. Inductively, $$h\in C^\infty(\mathbb R,\mathbb R)$$, with $$h^{(n)}(0)=0$$ for every $$n\ge0$$.

The function $$k(s)=h(s-\alpha)h(\beta-s)$$ is therefore smooth. It vanishes for $$s\notin(\alpha,\beta)$$ and is strictly positive for $$\alpha<s<\beta$$. In particular,

$$
C:=\int_\alpha^\beta k(s)\,ds>0.
$$

Define

$$
\theta(t)=\frac{1}{C}\int_\alpha^t k(s)\,ds,
$$

where the integral is understood with its usual orientation also when $$t\notin[\alpha,\beta]$$. The fundamental theorem of calculus gives $$\theta'(t)=k(t)/C$$, so $$\theta$$ is smooth and increasing (in the non-strict sense). If $$t\le\alpha$$, the integral is zero because $$k$$ vanishes on $$(-\infty,\alpha]$$. If $$t\ge\beta$$, it equals $$C$$ because $$k$$ vanishes on $$[\beta,\infty)$$. Hence $$\theta(t)=0$$ for $$t\le\alpha$$ and $$\theta(t)=1$$ for $$t\ge\beta$$, as required.

### Exercise 6

For each $$j=1,\ldots,m$$, define

$$
k_j(t)=h(t-\alpha_j)h(\beta_j-t),\qquad t\in\mathbb R,
$$

using the smooth function from Exercise 5, and set

$$
g(x_1,\ldots,x_m)=\prod_{j=1}^m k_j(x_j).
$$

Each factor is smooth, so $$g\in C^\infty(\mathbb R^m,\mathbb R)$$. If $$x\in A=\prod_{j=1}^m(\alpha_j,\beta_j)$$, then every factor is positive and thus $$g(x)>0$$. If $$x\notin A$$, at least one coordinate lies outside its open interval; the corresponding factor is zero, including at either endpoint. Therefore $$g(x)=0$$ for all $$x\in A^c$$.

### Exercise 7

If $$K=\varnothing$$, the choice $$f=0$$ satisfies the requirements. Now suppose $$K\ne\varnothing$$.

For each $$x\in K$$, openness of $$U$$ lets us choose an open rectangular box $$Q_x$$ with $$x\in Q_x$$ and $$\overline{Q_x}\subset U$$. By Exercise 6 there is a smooth function $$g_x$$ that is positive on $$Q_x$$ and zero outside $$Q_x$$. The boxes cover the compact set $$K$$, so finitely many, say $$Q_{x_1},\ldots,Q_{x_N}$$, cover it. Put

$$
G=\sum_{i=1}^N g_{x_i}.
$$

Then $$G\in C^\infty(\mathbb R^m,\mathbb R)$$, $$G\ge0$$, and $$G=0$$ on $$U^c$$ because each $$\overline{Q_{x_i}}\subset U$$. Moreover, every point of $$K$$ lies in some $$Q_{x_i}$$, where the corresponding summand is positive. Thus $$G>0$$ on $$K$$. By compactness,

$$
\delta:=\min_{x\in K}G(x)>0.
$$

Let $$\theta$$ be the function from Exercise 5 for the interval $$[0,\delta]$$, and define $$f=\theta\circ G$$. Then $$f$$ is smooth and takes values in $$[0,1]$$. On $$K$$ we have $$G\ge\delta$$, so $$f=1$$. On $$U^c$$ we have $$G=0$$, so $$f=0$$. This gives all three required properties.

### Exercise 8

For every admissible $$u$$, the integrand $$t\dot u(t)^2$$ is nonnegative, so $$f(u)\ge0$$. We construct admissible functions whose values approach zero. For $$\varepsilon>0$$, set

$$
L_\varepsilon=\log\frac{1+\varepsilon}{\varepsilon},\qquad
u_\varepsilon(t)=\frac{\log\frac{t+\varepsilon}{\varepsilon}}{L_\varepsilon},\quad 0\le t\le1.
$$

This function belongs to $$C^1([0,1],\mathbb R)$$, satisfies $$u_\varepsilon(0)=0$$ and $$u_\varepsilon(1)=1$$, and has derivative

$$
\dot u_\varepsilon(t)=\frac{1}{(t+\varepsilon)L_\varepsilon}.
$$

Therefore

$$
\begin{aligned}
f(u_\varepsilon)
&=\frac{1}{L_\varepsilon^2}\int_0^1\frac{t}{(t+\varepsilon)^2}\,dt\\
&=\frac{L_\varepsilon+\frac{\varepsilon}{1+\varepsilon}-1}{L_\varepsilon^2}
\longrightarrow 0\qquad(\varepsilon\downarrow0),
\end{aligned}
$$

because $$L_\varepsilon\to\infty$$. Thus the infimum is zero.

It cannot be attained. If an admissible $$u_0$$ satisfied $$f(u_0)=0$$, the continuous nonnegative function $$t\dot u_0(t)^2$$ would have integral zero and hence vanish everywhere. For every $$t>0$$ this implies $$\dot u_0(t)=0$$. The fundamental theorem of calculus would then give $$u_0(1)=u_0(0)$$, contradicting the endpoint conditions. Hence the infimum is not a minimum.

### Exercise 9

Here the Lagrangian is $$L(v)=|v|$$. It is differentiable only when $$v\ne0$$, and there

$$
\partial_v L(v)=\frac{v}{|v|}.
$$

Thus the classical Euler–Lagrange equation, on any curve with nonzero velocity, is

$$
\frac{d}{dt}\left(\frac{\dot u(t)}{|\dot u(t)|}\right)=0.
$$

The unit tangent is constant. If in addition $$|\dot u(t)|$$ is constant, then $$\dot u$$ itself is constant, so $$u$$ is affine. The endpoint conditions determine it uniquely:

$$
u(t)=a+\frac{t-\alpha}{\beta-\alpha}(b-a).
$$

When $$a\ne b$$ this is a nonzero-speed classical solution of the Euler–Lagrange equations. When $$a=b$$, the only affine constant-speed candidate is the constant curve, whose velocity is zero; the classical Euler–Lagrange equation above is undefined there. Thus, in the usual smooth sense, there is no zero-speed classical solution of that equation. The length functional is nonsmooth at zero velocity, which is why this degenerate case must be distinguished.

For $$m=2$$ write $$p=\dot u_1$$, $$q=\dot u_2$$, and $$r=\sqrt{p^2+q^2}$$. The two Euler–Lagrange equations are

$$
\frac{d}{dt}\left(\frac{p}{r}\right)=0,
\qquad
\frac{d}{dt}\left(\frac{q}{r}\right)=0.
$$

Equivalently, after differentiating and multiplying by $$r^3$$,

$$
q^2\ddot u_1-pq\ddot u_2=0,
\qquad
p^2\ddot u_2-pq\ddot u_1=0.
$$

Under the stated assumptions $$p\ne0$$ and $$q\ne0$$, these two equations are equivalent to

$$
\frac{\ddot u_1}{\dot u_1}=\frac{\ddot u_2}{\dot u_2}.
$$

### Exercise 10

For a scalar Lagrangian $$L(u,v)$$, the Euler–Lagrange equation is

$$
\partial_1L(u,\dot u)-\frac{d}{dt}\partial_2L(u,\dot u)=0.
$$

**(a)** Here $$L(u,v)=u\sqrt{1+v^2}$$. Thus

$$
\partial_1L=\sqrt{1+v^2},\qquad
\partial_2L=\frac{uv}{\sqrt{1+v^2}}.
$$

The Euler–Lagrange equation is

$$
\sqrt{1+\dot u^2}-\frac{d}{dt}\left(\frac{u\dot u}{\sqrt{1+\dot u^2}}\right)=0.
$$

Differentiating the quotient and simplifying gives the equivalent second-order equation

$$
u\ddot u=1+\dot u^2.
$$

**(b)** Now $$L(u,v)=\sqrt{(1+v^2)/u}=u^{-1/2}\sqrt{1+v^2}$$ on $$u>0$$, so

$$
\partial_1L=-\frac{\sqrt{1+v^2}}{2u^{3/2}},\qquad
\partial_2L=\frac{v}{\sqrt{u}\sqrt{1+v^2}}.
$$

The Euler–Lagrange equation reads

$$
-\frac{\sqrt{1+\dot u^2}}{2u^{3/2}}
-\frac{d}{dt}\left(\frac{\dot u}{\sqrt{u}\sqrt{1+\dot u^2}}\right)=0.
$$

Expanding the derivative and multiplying by the positive factor $$2u^{3/2}(1+\dot u^2)^{3/2}$$ yields

$$
2u\ddot u+1+\dot u^2=0.
$$

### Exercise 11

Let $$E_1=C^1([\alpha,\beta],\mathbb R^m)$$ with its usual norm, and let

$$
U=\{u\in E_1:u(t)\in X\text{ for all }t\in[\alpha,\beta]\}.
$$

Because the image of each $$u\in U$$ is compact and $$X$$ is open, $$U$$ is open in $$E_1$$. The map

$$
\Psi:E_1\to C([\alpha,\beta],\mathbb R^m\times\mathbb R^m),\qquad
\Psi(u)(t)=(u(t),\dot u(t)),
$$

is bounded and linear. The Nemytskii theorem applied to $$L\in C^{0,2}([\alpha,\beta]\times(X\times\mathbb R^m),\mathbb R)$$ shows that the map $$v\mapsto L(\cdot,v(\cdot))$$ is twice continuously differentiable on the relevant open subset of the continuous-function space. Integration is a bounded linear functional on that space. Since $$f$$ is the composition of these maps with $$\Psi$$, the chain rule gives $$f\in C^2(U,\mathbb R)$$.

For $$h,k\in E_1$$, the first derivative is

$$
Df(u)h=\int_\alpha^\beta\bigl[\partial_2L(\cdot,u,\dot u)h+\partial_3L(\cdot,u,\dot u)\dot h\bigr]dt.
$$

Applying the chain rule once more, or differentiating this expression in direction $$k$$, gives the Hessian of $$L$$ in its pair of variables $$(u,\dot u)$$:

$$
\begin{aligned}
D^2f(u)[h,k]=\int_\alpha^\beta\bigl[&\partial_2^2L(\cdot,u,\dot u)[h,k]
+\partial_2\partial_3L(\cdot,u,\dot u)[h,\dot k]\\
&+\partial_3\partial_2L(\cdot,u,\dot u)[\dot h,k]
+\partial_3^2L(\cdot,u,\dot u)[\dot h,\dot k]\bigr]dt.
\end{aligned}
$$

The two mixed terms are transposes of each other because $$L$$ is twice continuously differentiable in $$(u,v)$$. This is the formula in the exercise, with each mixed derivative evaluated on one direction in the $$u$$ variable and one in the $$\dot u$$ variable.

Here is a sufficient second-variation condition for a strict local minimum under fixed endpoint conditions. Let $$E_0=\{h\in E_1:h(\alpha)=h(\beta)=0\}$$. Suppose $$u$$ solves the Euler–Lagrange equation, so integration by parts gives $$Df(u)h=0$$ for all $$h\in E_0$$. If there is a constant $$c>0$$ such that

$$
D^2f(u)[h,h]\ge c\|h\|_{E_1}^2\qquad(h\in E_0),
$$

then $$u$$ is a strict local minimizer among curves with the same endpoints. Indeed, continuity of $$D^2f$$ ensures that in a sufficiently small neighborhood of $$u$$,

$$
D^2f(u+sh)[h,h]\ge\frac c2\|h\|_{E_1}^2
$$

for every $$s\in[0,1]$$ and every sufficiently small $$h\in E_0$$. Taylor’s formula with integral remainder then gives

$$
f(u+h)-f(u)=\int_0^1(1-s)D^2f(u+sh)[h,h]\,ds
\ge\frac c4\|h\|_{E_1}^2>0
$$

whenever $$h\ne0$$ is small. For free endpoint conditions the same argument applies with all directions $$h\in E_1$$, provided the first variation vanishes on all of them.

### Exercise 12

The Lagrangian is $$L(q,\dot q)=\frac m2|\dot q|^2-U(q)$$, where $$m>0$$ is the particle’s mass. Its Euler–Lagrange equation is

$$
\frac{d}{dt}\partial_{\dot q}L=\partial_qL,
\qquad\text{that is,}\qquad
m\ddot q=-\nabla U(q).
$$

Along a solution, differentiate the total energy $$E(t)=\frac m2|\dot q(t)|^2+U(q(t))$$. The chain rule and the equation of motion give

$$
\begin{aligned}
\dot E(t)
&=m\dot q(t)\cdot\ddot q(t)+\nabla U(q(t))\cdot\dot q(t)\\
&=\dot q(t)\cdot\bigl(m\ddot q(t)+\nabla U(q(t))\bigr)=0.
\end{aligned}
$$

Therefore $$E(t)$$ is constant on $$[t_0,t_1]$$.
