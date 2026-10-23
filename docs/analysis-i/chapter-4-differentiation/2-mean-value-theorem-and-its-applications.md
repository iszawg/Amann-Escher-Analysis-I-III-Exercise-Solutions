# Chapter IV — Differentiation in One Variable

## 2. The Mean Value Theorem and its Applications

### Exercise 1

For $$x\ne0$$, repeated differentiation shows that every derivative has the form

$$
f^{(k)}(x)=P_k(1/x)e^{-1/x^2},
$$

where $$P_k$$ is a polynomial. Indeed, differentiating a polynomial in $$1/x$$ times $$e^{-1/x^2}$$ again produces a polynomial in $$1/x$$ times the same exponential.

For every integer $$m\ge0$$,

$$
|x|^{-m}e^{-1/x^2}\longrightarrow0\qquad(x\to0),
$$

because, on setting $$t=1/x^2$$, this is a polynomial power of $$t$$ multiplied by $$e^{-t}$$ as $$t\to\infty$$. Thus each expression $$P_k(1/x)e^{-1/x^2}$$ tends to zero. Define its value at zero to be zero. Inductively, if $$f^{(k)}(0)=0$$, then

$$
\frac{f^{(k)}(h)-f^{(k)}(0)}{h}
=\frac{P_k(1/h)}{h}e^{-1/h^2}\longrightarrow0.
$$

Hence $$f^{(k+1)}(0)=0$$, and this derivative is continuous at zero by the same exponential estimate. Starting with $$k=0$$ proves that $$f\in C^\infty(\mathbb R)$$ and $$f^{(k)}(0)=0$$ for every $$k\in\mathbb N$$.

For $$x\ne0$$, $$f(x)=e^{-1/x^2}>0=f(0)$$. Therefore zero is a global minimum, and it is isolated (in fact, every punctured neighborhood of zero consists of points with strictly larger values).

### Exercise 2

In Example 1.17, $$f(t)=e^{-1/t}$$ for $$t>0$$ and $$f(t)=0$$ for $$t\le0$$. On $$[0,\infty)$$ this function is strictly increasing, and $$f(1)=e^{-1}$$.

If $$x\le0$$, then $$1-x\ge1$$, so $$f(1-x)\ge f(1)$$. The argument of the outer occurrence of $$f$$ is nonpositive, and consequently $$F(x)=0$$. If $$x\ge1$$, then $$1-x\le0$$ and

$$
F(x)=e^e f(f(1))=e^e f(e^{-1})=e^e e^{-e}=1.
$$

For $$0\le x\le1$$, the function $$f(1-x)$$ strictly decreases as $$x$$ increases. Thus $$f(1)-f(1-x)$$ strictly increases from zero to $$e^{-1}$$. Applying the strictly increasing function $$f$$ to this argument shows that $$F$$ is strictly increasing on $$[0,1]$$. These facts give the claimed piecewise values as well.

### Exercise 3

Let

$$
L:=\lim_{x\to a+}f'(x)\in\mathbb R.
$$

For each $$h\in(0,b-a]$$, the mean value theorem applied on $$[a,a+h]$$ gives a point $$c_h\in(a,a+h)$$ such that

$$
\frac{f(a+h)-f(a)}{h}=f'(c_h).
$$

As $$h\downarrow0$$, also $$c_h\to a+$$, so the right difference quotient tends to $$L$$. Hence the right derivative of $$f$$ at $$a$$ exists and equals $$L$$. This proves the endpoint claim $$f'(a)=\lim_{x\to a+}f'(x)$$.

There is a gap in the stronger conclusion as the exercise is printed: continuity of $$f$$ and differentiability on $$(a,b)$$ do not imply that $$f'$$ is continuous there, and differentiability at $$b$$ is not assumed. For example, choose $$c\in(a,b)$$ and let $$f(x)=(x-c)^2\sin(1/(x-c))$$ for $$x\ne c$$, with $$f(c)=0$$. This function is continuous on $$[a,b]$$ and differentiable on $$(a,b)$$; its derivative has a finite limit at $$a$$, but at $$c$$ it equals zero while, for $$x\ne c$$,

$$
f'(x)=2(x-c)\sin\left(\frac1{x-c}\right)-\cos\left(\frac1{x-c}\right),
$$

which has no limit as $$x\to c$$. If the intended assumption is $$f\in C^1((a,b],\mathbb R)$$, then the mean value argument extends $$f'$$ continuously to $$a$$ and gives the stated $$C^1([a,b],\mathbb R)$$ conclusion.

### Exercise 4

Since $$f$$ is even and differentiable at zero, $$f'(0)=0$$. Define

$$
g(t):=f(\sqrt t),\qquad 0\le t\le a^2.
$$

This is continuous, and for $$t>0$$ the chain rule gives

$$
g'(t)=\frac{f'(\sqrt t)}{2\sqrt t}.
$$

Put $$u=\sqrt t$$. The mean value theorem applied to $$f'$$ on $$[0,u]$$ gives some $$\eta_u\in(0,u)$$ such that

$$
\frac{f'(u)}{2u}
=\frac{f'(u)-f'(0)}{2u}
=\frac{f''(\eta_u)}2.
$$

As $$t\downarrow0$$, we have $$u\downarrow0$$ and $$\eta_u\to0$$. Continuity of $$f''$$ implies

$$
\lim_{t\downarrow0}g'(t)=\frac{f''(0)}2.
$$

The same mean value theorem calculation applied to $$[0,u]$$ shows directly that

$$
\lim_{t\downarrow0}\frac{g(t)-g(0)}t=\frac{f''(0)}2.
$$

Thus $$g'(0)=f''(0)/2$$ and $$g'$$ is continuous at zero. Away from zero the displayed chain-rule formula is continuous, including its one-sided limit at $$a^2$$, so $$g\in C^1([0,a^2],\mathbb R)$$. Finally, evenness gives $$f(x)=f(|x|)=g(x^2)$$ for every $$x\in[-a,a]$$.

### Exercise 5

The function $$\cosh$$ maps $$[0,\infty)$$ onto $$[1,\infty)$$ and is strictly increasing there: its derivative is $$\sinh x>0$$ for $$x>0$$. Thus its restriction has an inverse $$\cosh^{-1}:[1,\infty)\to[0,\infty)$$. Likewise, $$\sinh$$ is strictly increasing on $$\mathbb R$$ because $$\cosh x>0$$, and its limits at the two ends of the real line are $$-\infty$$ and $$+\infty$$. It therefore has an inverse $$\sinh^{-1}:\mathbb R\to\mathbb R$$.

If $$y=\cosh u$$ with $$u\ge0$$, then $$e^u+e^{-u}=2y$$. Solving the resulting quadratic in $$e^u>0$$ gives $$e^u=y+\sqrt{y^2-1}$$. If $$y=\sinh u$$, solving $$e^u-e^{-u}=2y$$ gives $$e^u=y+\sqrt{y^2+1}$$. Taking logarithms yields

$$
\cosh^{-1}(y)=\log\bigl(y+\sqrt{y^2-1}\bigr),\quad y\ge1,
$$

and

$$
\sinh^{-1}(y)=\log\bigl(y+\sqrt{y^2+1}\bigr),\quad y\in\mathbb R.
$$

For $$y>1$$ and $$y\in\mathbb R$$, respectively, differentiation gives

$$
(\cosh^{-1})'(y)=\frac1{\sqrt{y^2-1}},\qquad
(\cosh^{-1})''(y)=-\frac{y}{(y^2-1)^{3/2}},
$$

$$
(\sinh^{-1})'(y)=\frac1{\sqrt{y^2+1}},\qquad
(\sinh^{-1})''(y)=-\frac{y}{(y^2+1)^{3/2}}.
$$

The derivative of $$\cosh^{-1}$$ is unbounded at the endpoint $$y=1$$, so these derivative formulas apply on its open domain $$y>1$$. The second derivatives show that $$\cosh^{-1}$$ is strictly concave on $$(1,\infty)$$. The function $$\sinh^{-1}$$ is strictly convex on $$(-\infty,0)$$ and strictly concave on $$(0,\infty)$$, with an inflection point at zero.

For the original hyperbolic functions, $$\cosh''=\cosh>0$$, so $$\cosh$$ is strictly convex on $$\mathbb R$$. Since $$\sinh''=\sinh$$, $$\sinh$$ is strictly concave on $$(-\infty,0)$$, strictly convex on $$(0,\infty)$$, and has an inflection point at zero. The graphs follow from these monotonicity and curvature properties: $$\cosh$$ is even with minimum $$1$$ at zero, $$\sinh$$ is odd through zero, $$\cosh^{-1}$$ rises from $$(1,0)$$ with a vertical tangent and is concave, and $$\sinh^{-1}$$ is odd, increasing, and changes curvature at zero.

### Exercise 6

Write

$$
f_n(x)=\sum_{k=0}^n\frac{x^k}{k!}.
$$

First suppose that $$n$$ is even. For $$x\ge0$$, every term is nonnegative and the constant term is one, so $$f_n(x)>0$$. For $$x<0$$, Taylor's theorem for the exponential at zero gives a point $$\xi$$ between $$x$$ and zero such that

$$
e^x=f_n(x)+e^\xi\frac{x^{n+1}}{(n+1)!}.
$$

Here $$n+1$$ is odd, so the remainder term is negative. Therefore $$f_n(x)>e^x>0$$. An even-index polynomial has no real zero.

Now suppose that $$n$$ is odd. Then $$f_n'(x)=f_{n-1}(x)$$, and $$n-1$$ is even, so the preceding argument gives $$f_{n-1}(x)>0$$ for every real $$x$$. Hence $$f_n$$ is strictly increasing. Also $$f_n(0)=1$$, whereas its leading term implies $$f_n(x)\to-\infty$$ as $$x\to-\infty$$. The intermediate value theorem gives a zero, and strict increase makes it unique.

### Exercise 7

**(a)** For $$x<0$$ and $$x>0$$, respectively, differentiation gives

$$
f''(x)=\frac1{4(-x)^{3/2}}>0\quad(x<0),\qquad
f''(x)=-\frac1{4x^{3/2}}<0\quad(x>0).
$$

Thus $$f$$ is convex immediately to the left of zero and concave immediately to its right. This is an inflection point under the definition in the question.

**(b)** Suppose first that $$f$$ is convex to the left of $$x_0$$ and concave to its right. For a differentiable convex function, its derivative is nondecreasing; for a differentiable concave function, its derivative is nonincreasing. Since $$f''(x_0)$$ exists, $$f'$$ is continuous at $$x_0$$. Thus for small $$h<0$$ we have $$f'(x_0+h)\le f'(x_0)$$, while for small $$h>0$$ we have $$f'(x_0+h)\le f'(x_0)$$ as well. More precisely, on the left the difference quotient

$$
\frac{f'(x_0+h)-f'(x_0)}h
$$

is nonnegative because both numerator and denominator are nonpositive. On the right it is nonpositive because the numerator is nonpositive and the denominator positive. Its two-sided limit exists and is $$f''(x_0)$$; therefore this limit is both nonnegative and nonpositive, hence zero. If the curvature order is reversed, the signs reverse and the same conclusion follows. Thus $$f''(x_0)=0$$.

**(c)** For $$f(x)=x^4$$, we have $$f''(x)=12x^2>0$$ whenever $$x\ne0$$. Every nonempty open interval contains nonzero points, and a twice differentiable concave function must have nonpositive second derivative throughout its interval. Consequently no interval on either side of any candidate point can be a concavity interval for $$x^4$$. It has no inflection points.

**(d)** Since $$f'''$$ is continuous and $$f'''(x_0)\ne0$$, it has a fixed nonzero sign in a neighborhood of $$x_0$$. By the mean value theorem, for each nearby $$x\ne x_0$$ there is a point $$\eta$$ between $$x$$ and $$x_0$$ such that

$$
f''(x)-f''(x_0)=f'''(\eta)(x-x_0).
$$

As $$f''(x_0)=0$$, this shows that $$f''$$ has opposite signs on the two sides of $$x_0$$. A positive second derivative gives convexity and a negative one gives concavity. Hence the curvature changes at $$x_0$$, so it is an inflection point.

### Exercise 8

**(a)** For $$f(x)=x^2-1/x$$ on $$x>0$$,

$$
f''(x)=2-\frac2{x^3}.
$$

This is negative for $$0<x<1$$ and positive for $$x>1$$. The unique inflection point is $$x=1$$, where $$f(1)=0$$; its coordinates are $$(1,0)$$.

**(b)** For $$f(x)=\sin x+\cos x$$,

$$
f''(x)=-\sin x-\cos x=-f(x).
$$

The zeros of $$f''$$ are $$x=-\pi/4+k\pi$$, where $$k\in\mathbb Z$$. They are simple zeros, since $$f'''(x)=-\cos x+\sin x$$ is nonzero at each such point. Thus the second derivative changes sign at every zero. The inflection points are

$$
\left(-\frac\pi4+k\pi,\,0\right),\qquad k\in\mathbb Z.
$$

**(c)** For $$x>0$$, logarithmic differentiation of $$f(x)=x^x$$ yields

$$
f'(x)=x^x(\log x+1),\qquad
f''(x)=x^x\left((\log x+1)^2+\frac1x\right)>0.
$$

The function is strictly convex on its whole domain and has no inflection points.

### Exercise 9

Because $$f(x)>0$$, it is enough to show that its logarithm is strictly increasing. Set

$$
\ell(x):=\log f(x)=x\log\left(1+\frac1x\right).
$$

Then

$$
\ell'(x)=\log\left(1+\frac1x\right)-\frac1{x+1}.
$$

For $$t>0$$ define $$q(t)=\log(1+t)-t/(1+t)$$. Since $$q(0)=0$$ and

$$
q'(t)=\frac{t}{(1+t)^2}>0,
$$

we have $$q(t)>0$$ for $$t>0$$. Taking $$t=1/x$$ shows $$\ell'(x)>0$$. Therefore $$f$$ is strictly increasing.

### Exercise 10

Fix $$x\in(a,b]$$. By the mean value theorem on $$[a,x]$$, there is some $$\xi\in(a,x)$$ such that

$$
f(x)-f(a)=f'(\xi)(x-a)\ge0.
$$

Since $$f(a)\ge0$$, this implies $$f(x)\ge0$$. At $$x=a$$ the claim is the assumed inequality.

### Exercise 11

For the first inequality, set

$$
u(x)=\log x-1+\frac1x.
$$

Then $$u(1)=0$$ and $$u'(x)=(x-1)/x^2$$. Thus $$u$$ decreases up to $$1$$ and increases after $$1$$, so $$u(x)\ge0$$ for all $$x>0$$. This is $$1-1/x\le\log x$$.

For the second inequality, set

$$
v(x)=x-1-\log x.
$$

We have $$v(1)=0$$ and $$v'(x)=(x-1)/x$$, so again $$v$$ has its global minimum at $$1$$. Hence $$v(x)\ge0$$, or $$\log x\le x-1$$.

### Exercise 12

**(a)** The pointwise maximum $$f\vee g$$ is convex. For $$z=(1-t)x+ty$$, convexity gives

$$
f(z)\le(1-t)f(x)+tf(y),\qquad
g(z)\le(1-t)g(x)+tg(y).
$$

Taking the maximum and bounding each endpoint value by the corresponding maximum gives

$$
(f\vee g)(z)\le(1-t)(f\vee g)(x)+t(f\vee g)(y).
$$

**(b)** The statement for arbitrary real $$\alpha,\beta$$ is false. For example, on $$I=\mathbb R$$ take $$f(x)=x^2$$, $$g(x)=0$$, $$\alpha=-1$$ and $$\beta=0$$. Both functions are convex, but $$\alpha f+\beta g=-x^2$$ is not convex. If $$\alpha,\beta\ge0$$, the sum is convex because a nonnegative linear combination preserves the convexity inequality.

**(c)** The product need not be convex. On $$I=\mathbb R$$ take $$f(x)=x$$ and $$g(x)=-x$$. Both are affine and hence convex, but $$f(x)g(x)=-x^2$$ is not convex.

### Exercise 13

Since $$f$$ is continuous and $$I$$ is an interval, $$f(I)$$ is an interval, so every convex combination of $$f(x)$$ and $$f(y)$$ lies in the domain of $$g$$. Let $$x,y\in I$$ and $$t\in[0,1]$$, and put $$z=(1-t)x+ty$$. Convexity of $$f$$ gives

$$
f(z)\le(1-t)f(x)+tf(y).
$$

Since $$g$$ is increasing and convex, it follows that

$$
g(f(z))\le g((1-t)f(x)+tf(y))
\le(1-t)g(f(x))+tg(f(y)).
$$

Thus $$g\circ f$$ is convex.

Here are two useful sufficient conditions for strict convexity. If $$f$$ is strictly convex and $$g$$ is strictly increasing (as well as convex), the first inequality is strict whenever $$x\ne y$$ and $$0<t<1$$, so the composition is strictly convex. Alternatively, if $$g$$ is strictly convex and increasing and $$f$$ is strictly monotone, then $$x\ne y$$ implies $$f(x)\ne f(y)$$; strict convexity of $$g$$ makes the second inequality strict. Either condition ensures that $$g\circ f$$ is strictly convex.

### Exercise 14

For $$u<v$$ write

$$
m(u,v):=\frac{f(v)-f(u)}{v-u}.
$$

Convexity implies the secant-slope inequalities

$$
m(u,v)\le m(u,w)\le m(v,w),\qquad u<v<w.
$$

**(a)** Fix $$x\in(a,b)$$. As $$h\downarrow0$$, the right secant slopes $$m(x,x+h)$$ have a limit: they are monotone as the right endpoint approaches $$x$$. For fixed $$c<x<d$$ and sufficiently small $$h>0$$, they satisfy

$$
m(c,x)\le m(x,x+h)\le m(x,d),
$$

so the limit is finite. The left secant slopes $$m(x-h,x)$$ likewise have a limit. To see that this limit is finite, choose $$c_0<c<x<d$$; for small $$h>0$$,

$$
m(c_0,c)\le m(c,x-h)\le m(x-h,x)\le m(x,d).
$$

Finally, the secant-slope inequality for $$x-h<x<x+k$$ shows $$m(x-h,x)\le m(x,x+k)$$. Passing to the one-sided limits gives

$$
\partial_-f(x)\le\partial_+f(x).
$$

**(b)** The one-sided limits in (a) are finite. The corresponding difference quotients therefore stay bounded near each interior point $$x$$, and

$$
f(x+h)-f(x)=h\,m(x,x+h)\longrightarrow0
$$

as $$h\downarrow0$$; the left-hand limit follows in the same way from $$m(x-h,x)$$. Thus $$f$$ is continuous at every point of $$(a,b)$$.

**(c)** Continuity at an endpoint need not hold. On $$[0,1]$$ define $$f(0)=1$$ and $$f(x)=0$$ for $$0<x\le1$$. If a convex combination of two points is positive, the function there is zero and the convexity inequality has a nonnegative right side; if the combination is zero, both points with positive weight are zero and equality holds. Hence this function is convex, but it is discontinuous at zero. The claim is false.

### Exercise 15

Fix $$x\in I\setminus\{a\}$$. Apply Cauchy's mean value theorem to $$\varphi$$ and $$\psi$$ on the interval with endpoints $$a$$ and $$x$$. Since $$\varphi(a)=\psi(a)=0$$ and $$\psi(x)\ne0$$, there is a point $$\xi_1$$ strictly between them such that

$$
\frac{\varphi(x)}{\psi(x)}=\frac{\varphi'(\xi_1)}{\psi'(\xi_1)}.
$$

For each $$j=1,\ldots,n$$, the hypotheses give $$\varphi^{(j)}(a)=\psi^{(j)}(a)=0$$ and $$\psi^{(j)}(\xi_j)\ne0$$. Applying Cauchy's mean value theorem to $$\varphi^{(j)}$$ and $$\psi^{(j)}$$ on the interval with endpoints $$a$$ and $$\xi_j$$ produces $$\xi_{j+1}$$ strictly between those endpoints and gives

$$
\frac{\varphi^{(j)}(\xi_j)}{\psi^{(j)}(\xi_j)}
=\frac{\varphi^{(j+1)}(\xi_{j+1})}{\psi^{(j+1)}(\xi_{j+1})}.
$$

After $$n$$ such repetitions,

$$
\frac{\varphi(x)}{\psi(x)}
=\frac{\varphi^{(n+1)}(\xi_{n+1})}{\psi^{(n+1)}(\xi_{n+1})}.
$$

The successive intervals are nested between $$a$$ and $$x$$, so $$\xi_{n+1}\in(x\wedge a,x\vee a)$$, as required. If $$n=0$$, the first application alone proves the result.

### Exercise 16

We use induction on $$n$$. For $$n=1$$, this is Rolle's theorem. Suppose the claim holds for $$n-1$$ and let $$x_0<\cdots<x_n$$ be zeros of $$f$$. Rolle's theorem on each interval $$[x_{j-1},x_j]$$ gives points

$$
\eta_j\in(x_{j-1},x_j),\qquad f'(\eta_j)=0,
\quad j=1,\ldots,n.
$$

They satisfy $$\eta_1<\cdots<\eta_n$$. The function $$f'$$ belongs to $$C^{n-2}(I,\mathbb R)$$, its derivative of order $$n-1$$ exists on the interior, and it has these $$n$$ zeros. Applying the induction hypothesis to $$f'$$ yields some $$\xi\in(\eta_1,\eta_n)\subset(x_0,x_n)$$ with

$$
f^{(n)}(\xi)=0.
$$

### Exercise 17

**(a)** Take logarithms:

$$
\log\left((1+2x)^{1/(3x)}\right)
=\frac{\log(1+2x)}{3x}\longrightarrow0.
$$

Therefore the limit is $$1$$.

**(b)** Write $$x=1+h$$. Then

$$
\frac{1+\cos(\pi x)}{x^2-2x+1}
=\frac{1-\cos(\pi h)}{h^2}\longrightarrow\frac{\pi^2}{2},
$$

using $$1-\cos u\sim u^2/2$$ as $$u\to0$$.

**(c)** The expansion $$\log(\cos u)=-u^2/2+o(u^2)$$ gives

$$
\lim_{x\to0}\frac{\log(\cos 3x)}{\log(\cos 2x)}
=\frac{9}{4}.
$$

**(d)** Taylor expansion gives

$$
\sin x=x-\frac{x^3}{6}+o(x^3),\qquad
\sin^2x=x^2\left(1-\frac{x^2}{3}+o(x^2)\right).
$$

Taking reciprocals,

$$
\frac1{\sin^2x}=\frac1{x^2}\left(1+\frac{x^2}{3}+o(x^2)\right)
=\frac1{x^2}+\frac13+o(1),
$$

so the limit is $$1/3$$.

### Exercise 18

Let $$p'=p/(p-1)$$, so $$1/p+1/p'=1$$. We first prove Hölder's inequality. For finite sequences, if either norm is zero the claim is immediate. Otherwise set

$$
A=\left(\sum_k|x_k|^p\right)^{1/p},\qquad
B=\left(\sum_k|y_k|^{p'}\right)^{1/p'}.
$$

Young's inequality $$uv\le u^p/p+v^{p'}/p'$$ for nonnegative $$u,v$$ gives

$$
\sum_k\frac{|x_k y_k|}{AB}
\le\frac1p\sum_k\frac{|x_k|^p}{A^p}
+\frac1{p'}\sum_k\frac{|y_k|^{p'}}{B^{p'}}=1.
$$

Thus $$\sum_k|x_ky_k|\le AB$$. For infinite sequences with finite right-hand side, apply this bound to every finite initial segment and let its length tend to infinity. The series $$\sum_k|x_ky_k|$$ converges, and

$$
\left|\sum_{k=0}^\infty x_ky_k\right|
\le\sum_{k=0}^\infty|x_ky_k|
\le\left(\sum_{k=0}^\infty|x_k|^p\right)^{1/p}
\left(\sum_{k=0}^\infty|y_k|^{p'}\right)^{1/p'}.
$$

For Minkowski's inequality, first work with finite sequences and put $$S=\sum_k|x_k+y_k|^p$$. If $$S=0$$ there is nothing to prove. Otherwise the triangle inequality and Hölder's inequality yield

$$
\begin{aligned}
S&\le\sum_k |x_k|\,|x_k+y_k|^{p-1}
+\sum_k |y_k|\,|x_k+y_k|^{p-1}\\
&\le\left[\left(\sum_k|x_k|^p\right)^{1/p}
+\left(\sum_k|y_k|^p\right)^{1/p}\right]
\left(\sum_k|x_k+y_k|^{(p-1)p'}\right)^{1/p'}\\
&=\left(\|x\|_p+\|y\|_p\right)S^{1/p'}.
\end{aligned}
$$

Since $$1-1/p'=1/p$$, division by $$S^{1/p'}$$ gives $$S^{1/p}\le\|x\|_p+\|y\|_p$$. Apply this to each finite initial segment and pass to the increasing limits of the sums to obtain the asserted inequality for series.

### Exercise 19

**(a)** Each $$\ell_p$$ is a linear subspace: scalar multiplication is immediate, and closure under addition follows from Minkowski's inequality in Exercise 18 for $$1<p<\infty$$, from the triangle inequality for absolute sums when $$p=1$$, and from the supremum triangle inequality when $$p=\infty$$. The norm axioms are direct: $$\|x\|_p\ge0$$, equality holds only for the zero sequence, and $$\|\alpha x\|_p=|\alpha|\|x\|_p$$. The triangle inequality is the corresponding result just established. Thus $$\ell_p$$ is a normed subspace of $$\mathbb K^{\mathbb N}$$.

**(b)** By definition, $$\|x\|_\infty=\sup_k|x_k|$$. This is finite exactly when $$x$$ is a bounded sequence. Hence $$\ell_\infty=B(\mathbb N,\mathbb K)$$.

**(c)** Suppose first that $$p<\infty$$ and $$p\le q<\infty$$. For every $$k$$, $$|x_k|\le\|x\|_p$$, and therefore

$$
\sum_k|x_k|^q
\le\|x\|_p^{q-p}\sum_k|x_k|^p
=\|x\|_p^q.
$$

Taking the $$q$$th root shows that $$\|x\|_q\le\|x\|_p$$ and proves $$x\in\ell_q$$. If $$q=\infty$$, the same bound $$|x_k|\le\|x\|_p$$ gives $$\|x\|_\infty\le\|x\|_p$$. When $$p=\infty$$ and $$p\le q\le\infty$$, necessarily $$q=\infty$$, and the assertion is equality. This proves the inclusion and norm estimate in all cases.

### Exercise 20

We prove the finite convexity inequality by induction on $$n$$. For $$n=1$$ it is equality, and for $$n=2$$ it is the definition of convexity. Assume it holds for $$n-1$$ points. Zero weights can be omitted, so suppose first that $$\lambda_n<1$$ and set $$\mu=1-\lambda_n>0$$ and

$$
y=\sum_{k=1}^{n-1}\frac{\lambda_k}{\mu}x_k.
$$

The normalized weights in this sum are nonnegative and add to one; since $$I$$ is an interval, $$y\in I$$. Also $$\sum_{k=1}^n\lambda_kx_k=\mu y+\lambda_nx_n$$. Convexity followed by the induction hypothesis gives

$$
\begin{aligned}
f\left(\sum_{k=1}^n\lambda_kx_k\right)
&\le\mu f(y)+\lambda_nf(x_n)\\
&\le\sum_{k=1}^{n-1}\lambda_kf(x_k)+\lambda_nf(x_n).
\end{aligned}
$$

If $$\lambda_n=1$$, the assertion is equality. Thus the claim holds for every finite collection of weights.

### Exercise 21

By definition,

$$
\Delta_h f(x)=\frac{f(x+h)-f(x)}h,
$$

so

$$
\Delta_h^2f(x)
=\frac{f(x+2h)-2f(x+h)+f(x)}{h^2}.
$$

The midpoint $$x+h$$ is the average of $$x$$ and $$x+2h$$. Convexity therefore gives

$$
f(x+h)\le\frac{f(x)+f(x+2h)}2.
$$

Rearranging shows that the numerator in the formula for $$\Delta_h^2f(x)$$ is nonnegative. Since $$h^2>0$$, we conclude that $$\Delta_h^2f(x)\ge0$$.
