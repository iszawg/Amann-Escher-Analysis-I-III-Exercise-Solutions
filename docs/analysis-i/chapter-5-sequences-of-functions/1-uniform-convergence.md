# Chapter V — Sequences of Functions

## 1. Uniform Convergence

### Exercise 1

**(a)** For each fixed $$x\in(0,1)$$, $$x^{1/n}\to1$$. But

$$
\sup_{0<x<1}|x^{1/n}-1|=1
$$

for every $$n$$, since $$x^{1/n}\to0$$ as $$x\downarrow0$$ with $$n$$ fixed. Thus the convergence is not uniform.

**(b)** For each fixed $$x>0$$, $$1/(1+nx)\to0$$. For every $$n$$,

$$
\sup_{0<x<1}\frac{1}{1+nx}=1,
$$

where the supremum is approached as $$x\downarrow0$$. Hence the convergence is not uniform.

**(c)** For each fixed $$x\in(0,1)$$, $$x/(1+nx)\to0$$, and

$$
0\leq \frac{x}{1+nx}\leq\frac1n,
$$

because $$nx\leq1+nx$$. The right-hand side tends to zero independently of $$x$$, so this sequence converges uniformly to zero.

### Exercise 2

For $$x\in\mathbb K$$, set $$f_n(x):=\sqrt{|x|^2+1/n^2}$$. Then

$$
0\leq f_n(x)-|x|
=\frac{1/n^2}{\sqrt{|x|^2+1/n^2}+|x|}
\leq\frac1n.
$$

At $$x=0$$ the difference equals $$1/n$$. Consequently,

$$
\sup_{x\in\mathbb K}|f_n(x)-|x||=\frac1n\longrightarrow0.
$$

Thus $$f_n$$ converges uniformly to the absolute value function on all of $$\mathbb K$$.

### Exercise 3

On the closed unit disk $$\overline{\mathbb B}_{\mathbb C}$$, the first series is norm convergent, since

$$
\sum_{n=1}^{\infty}\left\|\frac{x^n}{n^2}\right\|_\infty
=\sum_{n=1}^{\infty}\frac1{n^2}<\infty.
$$

The Weierstrass majorant criterion therefore gives uniform convergence. The second series does not even converge pointwise on the whole disk: at $$x=1$$ its terms are all equal to one, so $$\sum_{n=1}^{\infty}x^n$$ diverges. In particular, it does not converge uniformly there.

### Exercise 4

For fixed $$x\in(0,1]$$, the series can be written as

$$
\sum_{n=1}^{\infty}\frac{(-1)^n}{nx}
=\frac1x\sum_{n=1}^{\infty}\frac{(-1)^n}{n}.
$$

The alternating-series test shows that it converges pointwise, with sum $$-(\log 2)/x$$. It is not absolutely convergent at any $$x>0$$, because

$$
\sum_{n=1}^{\infty}\left|\frac{(-1)^n}{nx}\right|
=\frac1x\sum_{n=1}^{\infty}\frac1n=\infty.
$$

It is not uniformly convergent on $$(0,1]$$. Indeed, uniform convergence of a series requires its terms to tend uniformly to zero, whereas

$$
\sup_{0<x\leq1}\left|\frac{(-1)^n}{nx}\right|=\infty
$$

for every $$n$$.

### Exercise 5

Norm convergence here means $$\sum_n\|f_n\|_\infty<\infty$$, with $$X=\overline{\mathbb B}_{\mathbb K}$$.

**(a)** For every $$n$$, $$\|x^n\|_\infty=1$$, so the terms do not tend to zero in norm. The series is not norm convergent.

**(b)** Put $$t=|x|^2\in[0,1]$$. Then

$$
\|f_n\|_\infty=\max_{0\leq t\leq1}\frac{t}{(1+t)^n}.
$$

For $$n\geq2$$, differentiating gives the maximum at $$t=1/(n-1)$$, hence

$$
\|f_n\|_\infty=\frac{(n-1)^{n-1}}{n^n},
\qquad
n\|f_n\|_\infty=\left(1-\frac1n\right)^{n-1}\longrightarrow e^{-1}.
$$

By limit comparison with the harmonic series, $$\sum_n\|f_n\|_\infty$$ diverges. Thus the series is not norm convergent.

**(c)** The answer depends on whether $$\mathbb K=\mathbb R$$ or $$\mathbb C$$. If $$\mathbb K=\mathbb R$$, maximizing $$t(1-t^2)^n$$ for $$0\leq t\leq1$$ gives

$$
\|f_n\|_\infty
=\frac1{\sqrt{2n+1}}\left(1-\frac1{2n+1}\right)^n
\sim\frac{e^{-1/2}}{\sqrt{2n}}.
$$

The norms therefore have a divergent sum. If $$\mathbb K=\mathbb C$$, evaluating at $$x=i$$ gives $$|f_n(i)|=2^n$$, so the series again fails to converge in norm.

**(d)** This case also depends on the scalar field. For $$\mathbb K=\mathbb R$$,

$$
\sup_{|x|\leq1}|x(1-x^2)|=\frac{2}{3\sqrt3}<1,
$$

with the maximum attained at $$|x|=1/\sqrt3$$. Hence

$$
\|f_n\|_\infty=\left(\frac{2}{3\sqrt3}\right)^n,
$$

and the series is norm convergent by the geometric-series test. For $$\mathbb K=\mathbb C$$, the choice $$x=i$$ gives $$|x(1-x^2)|=2$$, so $$\|f_n\|_\infty\geq2^n$$ and the series is not norm convergent.

### Exercise 6

Let $$I\subset\mathbb R$$ be compact, and choose $$R\geq\sup_{x\in I}|x|$$. Taylor's theorem, using that the second derivative of cosine and the third derivative of sine have absolute value at most one, gives

$$
|1-\cos t|\leq\frac{|t|^2}{2},
\qquad
|t-\sin t|\leq\frac{|t|^3}{6}.
$$

Thus, for the summands in (a) and (b), respectively,

$$
\sup_{x\in I}|1-\cos(x/n)|\leq\frac{R^2}{2n^2},
\qquad
\sup_{x\in I}\left|n\left(\frac{x}{n}-\sin\frac{x}{n}\right)\right|
\leq\frac{R^3}{6n^2}.
$$

Both majorant series converge. The Weierstrass majorant criterion proves uniform convergence on $$I$$ for both series.

### Exercise 7

**(a)** For each $$x\in X$$,

$$
\|(f_n(x)+g_n(x))-(f(x)+g(x))\|
\leq\|f_n(x)-f(x)\|+\|g_n(x)-g(x)\|.
$$

Taking suprema shows

$$
\|f_n+g_n-(f+g)\|_\infty
\leq\|f_n-f\|_\infty+\|g_n-g\|_\infty\longrightarrow0.
$$

So $$f_n+g_n$$ converges uniformly to $$f+g$$.

**(b)** The printed claim that boundedness of *either one* of $$f,g$$ suffices is false. For example, on $$X=\mathbb R$$ let $$f_n(x)=1/n$$ and $$g_n(x)=x$$. Then $$f_n\to f=0$$ uniformly and $$g_n\to g=x$$ uniformly, and $$f$$ is bounded, but

$$
\sup_{x\in\mathbb R}|f_n(x)g_n(x)-f(x)g(x)|
=\sup_{x\in\mathbb R}\frac{|x|}{n}=\infty.
$$

The product sequence does not converge uniformly to $$fg$$. A valid sufficient condition is that **both** limit functions are bounded. In that case uniform convergence also makes $$f_n$$ bounded uniformly in $$n$$ for all sufficiently large $$n$$, and

$$
\|f_ng_n-fg\|_\infty
\leq\|f_n\|_\infty\,\|g_n-g\|_\infty
  +\|g\|_\infty\,\|f_n-f\|_\infty\longrightarrow0.
$$

If neither limit is assumed bounded, failure can occur even with $$f_n(x)=x+1/n$$ and $$g_n(x)=x$$ on $$\mathbb R$$: both converge uniformly to the unbounded function $$x$$, while $$f_ng_n-x^2=x/n$$ is unbounded for every $$n$$.

### Exercise 8

Passing to the pointwise limit in $$|f_n(x)|\geq\alpha$$ gives $$|f(x)|\geq\alpha$$ for every $$x\in X$$, so the reciprocals are well defined. For all $$n$$ and $$x$$,

$$
\left|\frac1{f_n(x)}-\frac1{f(x)}\right|
=\frac{|f_n(x)-f(x)|}{|f_n(x)|\,|f(x)|}
\leq\frac1{\alpha^2}|f_n(x)-f(x)|.
$$

Taking suprema and using the uniform convergence of $$f_n$$ to $$f$$ proves that $$1/f_n\to1/f$$ uniformly.

### Exercise 9

Uniform convergence of $$f_n$$ implies that it is uniformly Cauchy. Let $$\varepsilon>0$$. By uniform continuity of $$g$$, choose $$\delta>0$$ such that

$$
u,v\in D,\quad \|u-v\|<\delta
\quad\Longrightarrow\quad
\|g(u)-g(v)\|<\varepsilon.
$$

There is an $$N$$ such that $$\|f_n-f_m\|_\infty<\delta$$ whenever $$n,m\geq N$$. Since $$f_n(X)\subset D$$, it follows that

$$
\|g(f_n(x))-g(f_m(x))\|<\varepsilon
\qquad(x\in X,\ n,m\geq N).
$$

Thus $$g\circ f_n$$ is uniformly Cauchy. For each $$x$$, the sequence $$g(f_n(x))$$ is Cauchy in the Banach space $$F$$, so it has a limit; call the resulting function $$h:X\to F$$. Letting $$m\to\infty$$ in the uniform Cauchy estimate shows that $$g\circ f_n\to h$$ uniformly. Therefore the sequence of compositions is uniformly convergent.
