This section studies when limits of sequences of functions preserve continuity and differentiability.

### Exercise 1

**(a)** Let $$\varepsilon>0$$. Uniform convergence gives an index $$N$$ such that

$$
\|f_N-f\|_\infty<\frac{\varepsilon}{3}.
$$

Since $$f_N$$ is uniformly continuous, there is a $$\delta>0$$ such that $$d(x,y)<\delta$$ implies

$$
\|f_N(x)-f_N(y)\|<\frac{\varepsilon}{3}.
$$

For such $$x,y$$, the triangle inequality yields

$$
\begin{aligned}
\|f(x)-f(y)\|
&\leq \|f(x)-f_N(x)\|+\|f_N(x)-f_N(y)\|+\|f_N(y)-f(y)\|\\
&<\varepsilon.
\end{aligned}
$$

Thus $$f$$ is uniformly continuous.

**(b)** Let $$(f_m)$$ be Cauchy in $$\mathrm{BUC}(X,E)$$ with the supremum norm. For every fixed $$x$$, the sequence $$(f_m(x))$$ is Cauchy in the Banach space $$E$$. Define $$f(x):=\lim_{m\to\infty}f_m(x)$$. Given $$\varepsilon>0$$, choose $$M$$ so that

$$
\|f_m-f_\ell\|_\infty<\varepsilon
\qquad(m,\ell\geq M).
$$

Letting $$\ell\to\infty$$ pointwise gives $$\|f_m-f\|_\infty\leq\varepsilon$$ for every $$m\geq M$$. Hence $$f_m\to f$$ uniformly. The function $$f$$ is bounded: choose one such $$m$$, so that $$\|f-f_m\|_\infty<1$$; then

$$
\|f\|_\infty\leq \|f-f_m\|_\infty+\|f_m\|_\infty<\infty.
$$

Part (a) shows that the uniform limit $$f$$ is uniformly continuous. Therefore $$f\in\mathrm{BUC}(X,E)$$, and the Cauchy sequence converges in that space. Thus $$\mathrm{BUC}(X,E)$$ is Banach.

**(c)** If $$X$$ is compact, every continuous function $$f:X\to E$$ is bounded because its image is compact. It is also uniformly continuous by the Heine–Cantor theorem. Hence every member of $$C(X,E)$$ belongs to $$\mathrm{BUC}(X,E)$$, and the reverse inclusion is part of the definition. Therefore

$$
\mathrm{BUC}(X,E)=C(X,E).
$$

### Exercise 2

For each $$j$$, put $$a_j:=\lim_{k\to\infty}x_{jk}$$, which exists by (i). Fix $$k$$. Condition (ii) says that $$(x_{jk})_{j\in\mathbb N}$$ is Cauchy in $$E$$, so it has a limit; write

$$
b_k:=\lim_{j\to\infty}x_{jk}.
$$

We first show that $$(a_j)$$ is Cauchy. Given $$\varepsilon>0$$, apply (ii) with $$\varepsilon/2$$ and let $$N$$ be the resulting index. For $$m,n\geq N$$, the bound holds for every $$k$$. Taking $$k\to\infty$$ gives

$$
|a_m-a_n|\leq\frac{\varepsilon}{2}<\varepsilon.
$$

Since $$E$$ is complete, there is an $$a\in E$$ with $$a_j\to a$$.

It remains to compare this limit with $$b_k$$. Given $$\varepsilon>0$$, use (ii) with $$\varepsilon/4$$, obtaining $$N_0$$. Choose $$j\geq N_0$$ with $$|a_j-a|<\varepsilon/4$$. By (i), for all sufficiently large $$k$$,

$$
|x_{jk}-a_j|<\frac{\varepsilon}{4}.
$$

For each such $$k$$, condition (ii) gives $$|x_{mk}-x_{jk}|<\varepsilon/4$$ for every $$m\geq N_0$$. Letting $$m\to\infty$$ shows $$|b_k-x_{jk}|\leq\varepsilon/4$$. Thus

$$
|b_k-a|\leq |b_k-x_{jk}|+|x_{jk}-a_j|+|a_j-a|<\varepsilon
$$

for all sufficiently large $$k$$. Consequently $$b_k\to a$$, and

$$
\lim_{j\to\infty}\left(\lim_{k\to\infty}x_{jk}\right)
=a=
\lim_{k\to\infty}\left(\lim_{j\to\infty}x_{jk}\right).
$$

### Exercise 3

First suppose that $$f_n$$ increases pointwise to $$f$$. Fix $$\varepsilon>0$$. For each $$x\in X$$, pointwise convergence gives an index $$N_x$$ such that

$$
0\leq f(x)-f_{N_x}(x)<\frac{\varepsilon}{3}.
$$

By continuity of $$f$$ and $$f_{N_x}$$, there is an open neighborhood $$U_x$$ of $$x$$ such that, for every $$y\in U_x$$,

$$
|f(y)-f(x)|<\frac{\varepsilon}{3},
\qquad
|f_{N_x}(y)-f_{N_x}(x)|<\frac{\varepsilon}{3}.
$$

It follows that

$$
0\leq f(y)-f_{N_x}(y)
=[f(y)-f(x)]+[f(x)-f_{N_x}(x)]+[f_{N_x}(x)-f_{N_x}(y)]
<\varepsilon.
$$

The neighborhoods $$\{U_x:x\in X\}$$ cover the compact space $$X$$. Choose a finite subcover $$U_{x_1},\ldots,U_{x_q}$$ and set $$N:=\max_i N_{x_i}$$. If $$n\geq N$$ and $$y\in U_{x_i}$$, monotonicity in $$n$$ gives $$f_n(y)\geq f_{N_{x_i}}(y)$$. Therefore

$$
0\leq f(y)-f_n(y)\leq f(y)-f_{N_{x_i}}(y)<\varepsilon.
$$

This bound holds for every $$y\in X$$, so the convergence is uniform. If $$f_n$$ decreases pointwise, apply the same argument to $$-f_n\uparrow -f$$. Thus the continuity of the limit and monotonicity in $$n$$ imply uniform convergence.

### Exercise 4

**(a) The continuity of the limit is necessary.** On the compact interval $$[0,1]$$, let

$$
f_n(x):=x^n.
$$

Each $$f_n$$ is continuous, and the sequence decreases pointwise. Its limit is $$f(x)=0$$ for $$0\leq x<1$$ and $$f(1)=1$$, which is discontinuous. Moreover,

$$
\|f_n-f\|_\infty=\sup_{0\leq x<1}x^n=1
$$

for every $$n$$, so convergence is not uniform.

**(b) Monotonicity in $$n$$ is necessary.** For $$n\geq1$$ define on $$[0,1]$$

$$
f_n(x):=\max\left\{1-2^{n+2}|x-2^{-n}|,0\right\}.
$$

Each $$f_n$$ is continuous, supported in the interval of radius $$2^{-n-2}$$ around $$2^{-n}$$, and has supremum $$1$$. These support intervals are pairwise disjoint and converge to $$0$$. Thus for each fixed $$x>0$$, $$f_n(x)=0$$ for all sufficiently large $$n$$; also $$f_n(0)=0$$ for every $$n$$. Hence $$f_n(x)\to0$$ pointwise, with continuous limit $$f=0$$, but

$$
\|f_n-f\|_\infty=1
$$

for every $$n$$. The sequence is not monotone in $$n$$: at $$x=2^{-m}$$ its value is $$1$$ for $$n=m$$ and $$0$$ for every $$n\ne m$$.

### Exercise 5

We first prove uniform convergence for a subsequence whose functions are all nondecreasing. Let $$\varepsilon>0$$. Since $$f$$ is continuous on the compact interval $$I=[a,b]$$, it is uniformly continuous. Choose a finite partition

$$
a=x_0<x_1<\cdots<x_q=b
$$

fine enough that $$|f(x_{i+1})-f(x_i)|<\varepsilon/3$$ for each $$i$$. Pointwise convergence at these finitely many endpoints gives an index after which

$$
|f_n(x_i)-f(x_i)|<\frac{\varepsilon}{3}
\qquad(0\leq i\leq q).
$$

For $$x\in[x_i,x_{i+1}]$$, both functions are nondecreasing, so their values lie between their endpoint values. Consequently,

$$
\begin{aligned}
f_n(x)-f(x)&\leq f_n(x_{i+1})-f(x_i)\\
&\leq |f_n(x_{i+1})-f(x_{i+1})|+f(x_{i+1})-f(x_i)<\frac{2\varepsilon}{3},\\[4pt]
f(x)-f_n(x)&\leq f(x_{i+1})-f_n(x_i)\\
&\leq f(x_{i+1})-f(x_i)+|f(x_i)-f_n(x_i)|<\frac{2\varepsilon}{3}.
\end{aligned}
$$

Thus this subsequence converges uniformly to $$f$$. For a nonincreasing subsequence, apply the same argument to its negatives.

If all $$f_n$$ have the same direction of monotonicity, this proves uniform convergence directly, and passing to the pointwise limit shows that $$f$$ has that direction. Even if the direction may vary with $$n$$, split the indices into those for which $$f_n$$ is nondecreasing and those for which it is nonincreasing. At least one set is infinite; its pointwise limit shows that $$f$$ is monotone. Each infinite subsequence converges uniformly by the partition argument above. If both sets are infinite, their two uniform estimates together give uniform convergence of the whole sequence; if one set is finite, the other contains the entire tail. In every interpretation, $$f$$ is monotone and $$f_n\to f$$ uniformly.

### Exercise 6

Uniform convergence of $$f_n$$ to zero means $$\|f_n\|_\infty\to0$$. Since multiplication by $$(-1)^n$$ does not change absolute values,

$$
\|(-1)^n f_n\|_\infty=\|f_n\|_\infty\longrightarrow0.
$$

Therefore $$(-1)^n f_n$$ converges uniformly to zero. The monotonicity assumption is not needed for this conclusion.

### Exercise 7

Let

$$
\alpha_k:=\sum_{j=0}^k g_j,
\qquad
M:=\sup_k\|\alpha_k\|_\infty<\infty.
$$

Because $$f_n(x)$$ decreases to zero for each $$x$$, every $$f_n(x)$$ is nonnegative. Summation by parts, using $$g_k=\alpha_k-\alpha_{k-1}$$, gives for $$m<n$$

$$
\sum_{k=m+1}^{n}g_k f_k
=\sum_{k=m}^{n-1}\alpha_k(f_k-f_{k+1})+\alpha_n f_n-\alpha_m f_m.
$$

For every $$x\in X$$, the triangle inequality and the monotonicity of $$f_k(x)$$ imply

$$
\begin{aligned}
\left|\sum_{k=m+1}^{n}g_k(x)f_k(x)\right|
&\leq M\sum_{k=m}^{n-1}(f_k(x)-f_{k+1}(x))+M f_n(x)+M f_m(x)\\
&=2M f_m(x).
\end{aligned}
$$

Hence

$$
\left\|\sum_{k=m+1}^{n}g_k f_k\right\|_\infty\leq 2M\|f_m\|_\infty\longrightarrow0
\qquad(m\to\infty),
$$

uniformly in $$n>m$$. If $$M=0$$, all the partial sums $$\alpha_k$$ and therefore all $$g_k$$ vanish, so the conclusion is immediate. Otherwise, the displayed estimate is the uniform Cauchy criterion for the series. Thus $$\sum_{k=0}^{\infty}g_k f_k$$ converges uniformly.

### Exercise 8

Fix $$\alpha\in(0,\pi)$$. For $$x\in[\alpha,2\pi-\alpha]$$,

$$
|1-e^{ix}|=2|\sin(x/2)|\geq2\sin(\alpha/2)>0.
$$

The finite geometric sum therefore satisfies, for every $$N$$,

$$
\left|\sum_{k=1}^{N}e^{ikx}\right|
=\left|\frac{e^{ix}(1-e^{iNx})}{1-e^{ix}}\right|
\leq\frac{1}{\sin(\alpha/2)}
\qquad(x\in[\alpha,2\pi-\alpha]).
$$

Set $$g_k(x):=e^{ikx}$$ and $$f_k(x):=1/k$$ for $$k\geq1$$. The partial sums of $$g_k$$ are uniformly bounded by the estimate above; the positive sequence $$f_k$$ decreases to zero uniformly. Exercise 7 (with $$g_0=0$$) now gives uniform convergence of

$$
\sum_{k=1}^{\infty}\frac{e^{ikx}}{k}
$$

on $$[\alpha,2\pi-\alpha]$$.

### Exercise 9

By induction, $$\|A^k x_0\|\leq\alpha^k\|x_0\|$$ for every $$k\geq0$$. Fix $$R>0$$. On $$|z|\leq R$$, the series defining $$u$$ is dominated by

$$
\|x_0\|\sum_{k=0}^{\infty}\frac{(\alpha R)^k}{k!}
=\|x_0\|e^{\alpha R},
$$

so it converges uniformly on every bounded disk. For each $$m\geq0$$, the formally differentiated series is

$$
u^{(m)}(z)=\sum_{k=m}^{\infty}\frac{z^{k-m}}{(k-m)!}A^k x_0.
$$

It too converges uniformly for $$|z|\leq R$$, because its terms are bounded in sum by $$\alpha^m\|x_0\|e^{\alpha R}$$. Termwise differentiation of power series is therefore valid to every order. Reindexing with $$j=k-m$$ yields

$$
u^{(m)}(z)
=\sum_{j=0}^{\infty}\frac{z^j}{j!}A^{j+m}x_0
=A^m\sum_{j=0}^{\infty}\frac{z^j}{j!}A^j x_0
=A^m u(z).
$$

Thus $$u\in C^\infty(\mathbb K,E)$$ and, in particular, $$\partial^n u(z)=A^n u(z)$$ for every $$n\in\mathbb N^+$$.

### Exercise 10 — a correction to the printed statement

The displayed definition includes $$\partial^j f$$ for $$j=0,\ldots,n$$, but the printed quantity is

$$
\max_{1\leq j\leq n}\|\partial^j f\|_\infty.
$$

As printed, this is only a seminorm: every constant function has value zero, including nonzero constants. Thus part (b) cannot literally claim that this is a normed Banach space. The standard correction is

$$
\|f\|_{*,n}:=\max_{0\leq j\leq n}\|\partial^j f\|_\infty.
$$

There is also a domain qualification in (a) if $$\mathbb K=\mathbb C$$ and derivatives mean complex derivatives: for $$X=\mathbb C$$, every bounded entire function is constant, so $$BC^n(\mathbb C,E)$$ is closed in $$BC(\mathbb C,E)$$. We give the usual real-variable example and a complex-disk example below.

**(a)** Suppose first that $$\mathbb K=\mathbb R$$, $$X$$ is nonempty, and $$E\ne\{0\}$$. Choose $$c\in X$$ and a smooth function $$\chi$$ with compact support in $$X$$ that equals one near $$c$$. For a nonzero $$v\in E$$, define

$$
f(x):=\chi(x)|x-c|^{n-1/2}v.
$$

This is bounded and continuous, but it is not $$n$$-times continuously differentiable at $$c$$: near $$c$$ its $$n$$th derivative has size proportional to $$|x-c|^{-1/2}$$. Extend $$f$$ by zero to $$\mathbb R$$ and convolve it with smooth approximate identities of sufficiently small support. The resulting functions $$f_m$$ are smooth with compact support in $$X$$, so each derivative through order $$n$$ is bounded. Uniform continuity of $$f$$ gives $$\|f_m-f\|_\infty\to0$$. Thus $$f_m\in BC^n(X,E)$$ and $$f_m\to f\in BC(X,E)\setminus BC^n(X,E)$$, proving nonclosedness in this real-variable setting.

For complex derivatives on the unit disk $$\mathbb D$$, a parallel example is

$$
P_N(z):=\sum_{k=1}^{N}\frac{z^k}{k^{n+1}}.
$$

Each $$P_N$$ is a polynomial whose derivatives through order $$n$$ are bounded on $$\mathbb D$$. Since $$\sum_{k=1}^{\infty}1/k^{n+1}<\infty$$, these polynomials converge uniformly on $$\mathbb D$$ to $$P(z)=\sum_{k=1}^{\infty}z^k/k^{n+1}$$. For $$0<r<1$$,

$$
P^{(n)}(r)=\sum_{k=n}^{\infty}
\frac{k(k-1)\cdots(k-n+1)}{k^{n+1}}r^{k-n}.
$$

For $$k\geq2n$$ the coefficient is at least $$2^{-n}/k$$. Hence $$P^{(n)}(r)$$ becomes unbounded as $$r\uparrow1$$, by divergence of $$\sum_{k\geq2n}r^k/k$$ in that limit. Thus $$P\notin BC^n(\mathbb D,\mathbb C)$$ although $$P_N\to P$$ uniformly, so the subspace is not closed on $$\mathbb D$$.

**(b)** Use the corrected norm $$\|\cdot\|_{*,n}$$ above. Let $$(f_m)$$ be Cauchy in this norm. For each $$j=0,\ldots,n$$, the sequence $$(\partial^j f_m)$$ is uniformly Cauchy, so it converges uniformly to a bounded function $$g_j:X\to E$$. Each $$g_j$$ is continuous, as a uniform limit of continuous functions.

Fix $$a\in X$$ and choose a ball $$B(a,r)\subset X$$. For $$x\in B(a,r)$$ and $$j<n$$, the fundamental theorem of calculus along the segment from $$a$$ to $$x$$ gives

$$
\partial^j f_m(x)-\partial^j f_m(a)
=(x-a)\int_0^1\partial^{j+1}f_m\bigl(a+t(x-a)\bigr)\,dt.
$$

Uniform convergence permits passage to the limit in this identity:

$$
g_j(x)-g_j(a)
=(x-a)\int_0^1g_{j+1}\bigl(a+t(x-a)\bigr)\,dt.
$$

Continuity of $$g_{j+1}$$ implies, as $$x\to a$$,

$$
g_j(x)-g_j(a)=g_{j+1}(a)(x-a)+o(|x-a|).
$$

Therefore $$g_j$$ is differentiable at $$a$$ with derivative $$g_{j+1}(a)$$. Since $$a$$ was arbitrary, $$g_0\in C^n(X,E)$$ and $$\partial^j g_0=g_j$$ for all $$j\leq n$$. Each derivative is bounded, so $$g_0\in BC^n(X,E)$$. Finally, uniform convergence of every derivative gives $$\|f_m-g_0\|_{*,n}\to0$$. The corrected space is complete and hence Banach.

### Exercise 11

Since $$(f_n'(x_0))$$ is uniformly convergent, it is uniformly Cauchy. Also, $$(f_n(x_0))$$ is Cauchy by assumption. The mean value estimate (Theorem IV.2.18), applied to $$f_n-f_m$$ between $$x_0$$ and any $$x\in[a,b]$$, gives

$$
\|f_n(x)-f_m(x)\|
\leq \|f_n(x_0)-f_m(x_0)\|+|x-x_0|\,\|f_n'-f_m'\|_\infty.
$$

Taking the supremum over $$x\in[a,b]$$ and using $$|x-x_0|\leq b-a$$ yields

$$
\|f_n-f_m\|_\infty
\leq \|f_n(x_0)-f_m(x_0)\|+(b-a)\|f_n'-f_m'\|_\infty\longrightarrow0
$$

as $$m,n\to\infty$$. Thus $$(f_n)$$ is uniformly Cauchy. Completeness of $$E$$ gives a pointwise limit, and the uniform Cauchy criterion shows that convergence to this limit is uniform.
