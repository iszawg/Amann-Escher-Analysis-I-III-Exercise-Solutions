# Chapter VI — Integral Calculus in One Variable

## 8. Improper integrals

### Exercise 1

#### (i)

For $$x\ge 1$$,

$$
\frac{|\sin x|}{x^2}\le \frac{1}{x^2}.
$$

Since $$\int_1^\infty x^{-2}\,dx=1$$, the comparison test shows that
$$\int_1^\infty \frac{\sin x}{x^2}\,dx$$ converges absolutely.

#### (ii)

The quotient $$\sin x/x$$ has the continuous extension $$1$$ at $$x=0$$, so there is no singularity at the lower endpoint. To handle infinity, fix $$T>0$$ and integrate by parts:

$$
\int_T^R\frac{\sin x}{x}\,dx
=\left[-\frac{\cos x}{x}\right]_T^R-\int_T^R\frac{\cos x}{x^2}\,dx.
$$

As $$R\to\infty$$, the boundary term at $$R$$ tends to zero, and the last integral converges absolutely because $$|\cos x|/x^2\le 1/x^2$$. Thus the improper integral converges.

It does not converge absolutely. For every integer $$k\ge1$$,

$$
\int_{k\pi}^{(k+1)\pi}\frac{|\sin x|}{x}\,dx
\ge \frac{1}{(k+1)\pi}\int_{k\pi}^{(k+1)\pi}|\sin x|\,dx
=\frac{2}{(k+1)\pi}.
$$

The sum of these lower bounds diverges, so $$\int_0^\infty |\sin x|/x\,dx=\infty$$.

#### (iii)

With the substitution $$t=1/x$$,

$$
\int_1^\infty\frac{\sin(1/x)}{x}\,dx
=\int_0^1\frac{\sin t}{t}\,dt.
$$

The integrand on the right extends continuously to $$1$$ at zero. Hence this integral converges, and the same substitution with absolute values shows that it converges absolutely.

### Exercise 2

#### (i)

Set $$u=\arcsin x$$, so that $$du=dx/\sqrt{1-x^2}$$. Passing to the endpoint limits gives

$$
\int_0^1\frac{\arcsin x}{\sqrt{1-x^2}}\,dx
=\int_0^{\pi/2}u\,du
=\frac{\pi^2}{8}.
$$

In particular, the improper integral exists.

#### (ii)

Integration by parts on $$[1,R]$$ yields

$$
\int_1^R\frac{\log x}{x^2}\,dx
=\left[-\frac{\log x}{x}\right]_1^R+\int_1^R\frac{dx}{x^2}.
$$

Since $$\log R/R\to0$$, the limit is $$1$$.

#### (iii)

This integral converges absolutely: near zero, $$|\log x|$$ is integrable, and for $$x\ge1$$,

$$
\frac{\log x}{1+x^2}\le \frac{\log x}{x^2},
$$

whose integral over $$[1,\infty)$$ converges. Write

$$
J:=\int_0^1\frac{\log x}{1+x^2}\,dx.
$$

In the integral over $$[1,\infty)$$, substitute $$x=1/t$$. This gives

$$
\int_1^\infty\frac{\log x}{1+x^2}\,dx
=-\int_0^1\frac{\log t}{1+t^2}\,dt=-J.
$$

The two parts cancel, so the value is $$0$$.

#### (iv)

For a real parameter $$n$$, the integral near zero is finite exactly when $$n>-1$$, since

$$
\int_0^1x^n\,dx<\infty\quad\Longleftrightarrow\quad n>-1.
$$

At infinity, the exponential factor dominates every fixed power: for sufficiently large $$x$$, $$x^n\le e^{x/2}$$, so $$x^ne^{-x}\le e^{-x/2}$$. Thus the integral converges exactly when $$n>-1$$. For an integer $$n\ge1$$, integration by parts gives

$$
\int_0^\infty x^ne^{-x}\,dx
=n\int_0^\infty x^{n-1}e^{-x}\,dx,
$$

because $$x^ne^{-x}$$ vanishes at both endpoints. The base case is $$\int_0^\infty e^{-x}\,dx=1$$, so the value is $$n!$$ for every integer $$n\ge0$$.

### Exercise 3

The logarithmic singularities at the endpoints are integrable: since $$\sin x\sim x$$ as $$x\downarrow0$$ and $$\sin x\sim\pi-x$$ as $$x\uparrow\pi$$, the integrand differs from $$\log x$$ or $$\log(\pi-x)$$ by a bounded function near the respective endpoint.

Let

$$
J:=\int_0^{\pi/2}\log(\sin x)\,dx.
$$

The substitution $$x\mapsto\pi/2-x$$ shows that $$J=\int_0^{\pi/2}\log(\cos x)\,dx$$. Consequently,

$$
\begin{aligned}
2J
&=\int_0^{\pi/2}\log(\sin x\cos x)\,dx\\
&=\int_0^{\pi/2}\log\left(\frac{\sin(2x)}{2}\right)\,dx\\
&=-\frac{\pi}{2}\log2+\frac12\int_0^\pi\log(\sin u)\,du\\
&=-\frac{\pi}{2}\log2+J.
\end{aligned}
$$

In the last line we used the symmetry $$\sin(\pi-u)=\sin u$$. Hence $$J=-(\pi/2)\log2$$, and therefore

$$
\int_0^\pi\log(\sin x)\,dx=2J=-\pi\log2.
$$

### Exercise 4

For $$x\in[a,b)$$, define the finite-interval integral

$$
F(x):=\int_a^x f(t)\,dt.
$$

First suppose $$\int_a^b f$$ exists. Then $$F(x)$$ has a limit as $$x\uparrow b$$. Given $$\varepsilon>0$$, choose $$c<b$$ so that

$$
\left\|F(x)-\lim_{y\uparrow b}F(y)\right\|<\frac{\varepsilon}{2}
\qquad(c\le x<b).
$$

For $$\alpha,\beta\in[c,b)$$, additivity of finite-interval integrals gives

$$
\left\|\int_\alpha^\beta f\right\|
=\|F(\beta)-F(\alpha)\|<\varepsilon.
$$

Conversely, assume the stated tail condition. For every $$\varepsilon>0$$ there is a $$c<b$$ such that

$$
\|F(\beta)-F(\alpha)\|<\varepsilon
\qquad(\alpha,\beta\in[c,b)).
$$

Thus $$F(x)$$ is Cauchy as $$x\uparrow b$$. Since $$E$$ is Banach, $$F(x)$$ has a limit in $$E$$, which is precisely the existence of the improper integral $$\int_a^b f$$.

### Exercise 5

Use $$u=t^2$$. Then

$$
\int_0^\infty\sqrt{t}\cos(t^2)\,dt
=\frac12\int_0^\infty u^{-1/4}\cos u\,du.
$$

The integral near zero converges absolutely because $$u^{-1/4}$$ is integrable there. For $$R>S\ge1$$, integration by parts gives

$$
\int_S^R u^{-1/4}\cos u\,du
=\left[u^{-1/4}\sin u\right]_S^R
+\frac14\int_S^R u^{-5/4}\sin u\,du.
$$

The boundary term at $$R$$ tends to zero, and the remaining integral converges absolutely since $$u^{-5/4}$$ is integrable at infinity. Therefore the original improper integral converges.

### Exercise 6

#### (i)

Let

$$
F(c):=\int_a^c f(x)\,dx\qquad(c\in[a,b)).
$$

Because $$f\ge0$$, the function $$F$$ is nondecreasing, and

$$
K=\sup_{c\in[a,b)}F(c).
$$

If $$K<\infty$$, the monotone function $$F$$ has a finite limit as $$c\uparrow b$$, so $$\int_a^b f$$ exists. Conversely, if this improper integral exists, then $$F(c)$$ converges to its finite value and is bounded. Hence $$K<\infty$$.

#### (ii)

Set $$F(x):=\int_a^x f(t)\,dt$$. The hypothesis gives $$|F(x)|\le K$$ for every $$x<b$$. For $$a\le c<d<b$$, integration by parts yields

$$
\int_c^d f(x)g(x)\,dx
=F(d)g(d)-F(c)g(c)-\int_c^d F(x)g'(x)\,dx.
$$

Since $$g$$ is monotone and tends to zero, $$g(c)$$ and $$g(d)$$ tend to zero as $$c,d\uparrow b$$, and

$$
\int_c^d|g'(x)|\,dx=|g(d)-g(c)|.
$$

It follows that

$$
\left|\int_c^d fg\right|
\le K\bigl(|g(c)|+|g(d)|+|g(d)-g(c)|\bigr)\longrightarrow0
\qquad(c,d\uparrow b).
$$

The Cauchy criterion for improper integrals now proves that $$\int_a^b fg$$ converges.

### Exercise 7

Since $$f'$$ is increasing and tends to infinity, choose $$c\ge a$$ such that $$f'(x)>0$$ for all $$x\ge c$$. Then $$f$$ is strictly increasing on $$[c,\infty)$$ and tends to infinity. Write $$y=f(x)$$ on this tail and let $$x=\phi(y)$$ denote the inverse. The change of variables gives

$$
\int_c^R\sin(f(x))\,dx
=\int_{f(c)}^{f(R)}\sin y\,q(y)\,dy,
\qquad
q(y):=\frac{1}{f'(\phi(y))}.
$$

Because $$f'$$ is increasing, $$q$$ is nonnegative and nonincreasing; also $$q(y)\to0$$ as $$y\to\infty$$. The primitive of $$\sin y$$ is bounded, so Dirichlet's test shows that the last integral converges as $$R\to\infty$$. The integral over the finite interval $$[a,c]$$ is ordinary, proving convergence of $$\int_a^\infty\sin(f(x))\,dx$$.

### Exercise 8

There is a sign misprint in the printed conclusion: with the numerator $$f(ax)-f(bx)$$ and $$0<a<b$$, the value is

$$
f(0)\log\frac{b}{a},
$$

not $$f(0)\log(a/b)$$.

Let $$M$$ be a bound for $$\left|\int_s^t f(u)\,du\right|$$ over all $$0<s<t<\infty$$, and define $$F(t):=\int_1^t f(u)\,du$$, using oriented integrals when $$t<1$$. Then $$|F(t)|\le M$$ for all $$t>0$$. For $$R>c>0$$, substitutions in the two terms give

$$
\int_c^R\frac{f(ax)-f(bx)}{x}\,dx
=\int_{ac}^{bc}\frac{f(t)}{t}\,dt
-\int_{aR}^{bR}\frac{f(t)}{t}\,dt.
$$

The last term tends to zero as $$R\to\infty$$. Indeed, integration by parts and $$|F|\le M$$ imply

$$
\left|\int_{aR}^{bR}\frac{f(t)}{t}\,dt\right|
\le \frac{M}{bR}+\frac{M}{aR}
+M\int_{aR}^{bR}\frac{dt}{t^2}
=\frac{2M}{aR}.
$$

Thus the improper tail from $$c$$ to infinity exists and equals $$\int_{ac}^{bc}f(t)/t\,dt$$. By continuity of $$f$$ at zero,

$$
\begin{aligned}
\lim_{c\downarrow0}\int_{ac}^{bc}\frac{f(t)}{t}\,dt
&=f(0)\log\frac{b}{a},\\
\left|\int_{ac}^{bc}\frac{f(t)-f(0)}{t}\,dt\right|
&\le \sup_{0\le t\le bc}|f(t)-f(0)|\,\log\frac{b}{a}\longrightarrow0.
\end{aligned}
$$

This proves convergence at zero as well as the corrected value. It also agrees with the mean value theorem hint: $$\int_{ac}^{bc}f(t)/t\,dt=f(\xi(c))\log(b/a)$$ for some $$\xi(c)\in[ac,bc]$$.

### Exercise 9

#### (i)

For $$0<\varepsilon<1$$,

$$
\int_{-1}^{-\varepsilon}\frac{dx}{x}
+\int_\varepsilon^1\frac{dx}{x}
=\log\varepsilon-\log\varepsilon=0.
$$

Hence

$$
\operatorname{PV}\int_{-1}^1\frac{dx}{x}=0.
$$

#### (ii)

The function $$1/\sin x$$ is odd on the symmetric interval. For every $$0<\varepsilon<\pi/2$$, the two truncated integrals cancel:

$$
\int_{-\pi/2}^{-\varepsilon}\frac{dx}{\sin x}
+\int_\varepsilon^{\pi/2}\frac{dx}{\sin x}=0.
$$

Therefore

$$
\operatorname{PV}\int_{-\pi/2}^{\pi/2}\frac{dx}{\sin x}=0.
$$

#### (iii)

On $$[-1,1]\setminus\{0\}$$, partial fractions give

$$
\frac{1}{x(6+x-x^2)}
=\frac{1}{6x}+\frac{1}{15(3-x)}-\frac{1}{10(x+2)}.
$$

The Cauchy principal value of the first term is zero by part (i). The other terms are continuous on $$[-1,1]$$, so their ordinary integrals give

$$
\begin{aligned}
\operatorname{PV}\int_{-1}^1\frac{dx}{x(6+x-x^2)}
&=\frac1{15}\int_{-1}^1\frac{dx}{3-x}
-\frac1{10}\int_{-1}^1\frac{dx}{x+2}\\
&=\frac{\log2}{15}-\frac{\log3}{10}.
\end{aligned}
$$
