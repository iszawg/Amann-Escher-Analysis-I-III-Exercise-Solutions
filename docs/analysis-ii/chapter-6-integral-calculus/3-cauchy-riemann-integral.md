# Chapter VI — Integral Calculus in One Variable

## 3. The Cauchy–Riemann Integral

Throughout, let $$I=[\alpha,\beta]$$ be a compact interval, let $$E$$ be a Banach space, and use the definitions of staircase and jump continuous functions from the section. All integrals of jump continuous functions below are Cauchy–Riemann integrals. In Exercise 10, the term Riemann integral has the meaning given in Remark 3.5(a).

### Exercise 1

For the first three integrals, the integrands are staircase functions, so we split the interval at their jump points.

**(i)** On $$[k/n,(k+1)/n)$$, where $$k=0,\ldots,n-1$$, we have $$\lfloor nx\rfloor=k$$. Therefore

$$
\int_0^1\frac{\lfloor nx\rfloor}{n}\,dx
=\sum_{k=0}^{n-1}\frac{k}{n}\frac1n
=\frac{1}{n^2}\frac{n(n-1)}2
=\frac{n-1}{2n}.
$$

The value at $$x=1$$ does not affect the integral.

**(ii)** On $$[\sqrt{k/n},\sqrt{(k+1)/n})$$, where $$k=0,\ldots,n-1$$, we have $$\lfloor nx^2\rfloor=k$$. Hence

$$
\int_0^1\frac{\lfloor nx^2\rfloor}{n^2}\,dx
=\frac1{n^{5/2}}\sum_{k=0}^{n-1}k\bigl(\sqrt{k+1}-\sqrt{k}\bigr).
$$

To simplify the sum, shift the index in its first term:

$$
\begin{aligned}
\sum_{k=0}^{n-1}k\bigl(\sqrt{k+1}-\sqrt{k}\bigr)
&=\sum_{j=1}^{n}(j-1)\sqrt j-\sum_{j=1}^{n-1}j\sqrt j\\
&=(n-1)\sqrt n-\sum_{j=1}^{n-1}\sqrt j.
\end{aligned}
$$

Thus

$$
\int_0^1\frac{\lfloor nx^2\rfloor}{n^2}\,dx
=\frac{(n-1)\sqrt n-\sum_{j=1}^{n-1}\sqrt j}{n^{5/2}}.
$$

**(iii)** The integrand is $$n$$ times the integrand in (ii), so

$$
\int_0^1\frac{\lfloor nx^2\rfloor}{n}\,dx
=\frac{(n-1)\sqrt n-\sum_{j=1}^{n-1}\sqrt j}{n^{3/2}}.
$$

**(iv)** The function $$\operatorname{sign}x$$ is $$-1$$ for $$x<0$$ and $$1$$ for $$x>0$$. Since $$|x|$$ is a primitive on each side of zero and the integral is additive across zero,

$$
\int_\alpha^\beta \operatorname{sign}x\,dx=|\beta|-|\alpha|.
$$

This also covers intervals lying wholly on either side of zero.

### Exercise 2

**(i)** Let $$f$$ be the function from Exercise VI.1.2. On each of the two intervals indexed by $$n\geq1$$, $$f$$ has value $$1/(n+2)$$, and each interval has length $$1/n-1/(n+1)$$. The intervals are symmetric about zero, while endpoint values do not affect the integral. Consequently,

$$
\begin{aligned}
\int_{-1}^1 f(x)\,dx
&=2\sum_{n=1}^\infty \frac1{n+2}\left(\frac1n-\frac1{n+1}\right)\\
&=2\sum_{n=1}^\infty\frac1{n(n+1)(n+2)}.
\end{aligned}
$$

The identity

$$
\frac1{n(n+1)(n+2)}
=\frac12\left(\frac1{n(n+1)}-\frac1{(n+1)(n+2)}\right)
$$

makes the series telescope to $$1/4$$. Therefore

$$
\int_{-1}^1 f(x)\,dx=\frac12.
$$

**(ii)** Let $$g$$ be the function from Exercise VI.1.7: if $$x=p/q\in[0,1]$$ is rational in lowest terms, then $$g(x)=1/q$$, and $$g(x)=0$$ at irrational points. We first verify that $$g$$ is jump continuous. For each fixed $$N$$, there are only finitely many rationals in $$[0,1]$$ whose reduced denominator is at most $$N$$. Given $$x$$, choose a neighborhood of $$x$$ that contains no such rational other than possibly $$x$$ itself. For all other points $$y$$ in that neighborhood, either $$g(y)=0$$ or its reduced denominator exceeds $$N$$, so $$0\leq g(y)\leq1/(N+1)$$. Letting $$N\to\infty$$ shows that both one-sided limits at every point of $$[0,1]$$ exist and equal zero.

To compute the integral, write $$D_N$$ for that finite set of rationals with reduced denominator at most $$N$$. Cover its points by finitely many intervals of total length less than an arbitrary $$\eta>0$$, choosing the endpoints outside $$D_N$$, and include all endpoints in a partition. On the intervals covering $$D_N$$, $$g\leq1$$. On every other partition interval, $$g\leq1/(N+1)$$. Thus an upper Darboux sum is at most

$$
\eta+\frac1{N+1}.
$$

Because $$g$$ is jump continuous, it is Riemann integrable by Remark 3.5(a), and its Riemann integral equals its Cauchy–Riemann integral. Its Riemann integral lies between the lower and upper sums for any fixed partition, since each Riemann sum does. Since $$g\geq0$$, its integral is nonnegative; the upper-sum bound above, followed by $$\eta\downarrow0$$ and $$N\to\infty$$, therefore gives

$$
\int_0^1 g(x)\,dx=0.
$$

### Exercise 3

Choose staircase functions $$f_n\to f$$ uniformly, as permitted by Theorem 1.2. Since $$A$$ is bounded and linear,

$$
\|Af_n-Af\|_\infty\leq\|A\|\,\|f_n-f\|_\infty\longrightarrow0.
$$

Each $$Af_n$$ is a staircase function, so Theorem 1.2 also shows that $$Af\in S(I,F)$$. For a staircase function, the integral is a finite sum of its constant values times interval lengths. Linearity of $$A$$ therefore gives

$$
A\int_I f_n=\int_I Af_n.
$$

The integration maps are bounded, and $$A$$ is continuous. Passing to the limit as $$n\to\infty$$ proves

$$
A\int_I f=\int_I Af.
$$

### Exercise 4

The assumption $$\sum_{n=0}^\infty\|f_n\|_\infty<\infty$$ implies, by the Weierstrass M-test, that the series $$\sum_{n=0}^\infty f_n$$ converges uniformly. Its partial sums are jump continuous, and $$S(I,E)$$ is closed in the supremum norm, so its limit $$f$$ is jump continuous. By continuity and linearity of integration,

$$
\int_I f
=\lim_{N\to\infty}\int_I\sum_{n=0}^N f_n
=\lim_{N\to\infty}\sum_{n=0}^N\int_I f_n
=\sum_{n=0}^\infty\int_I f_n.
$$

The last series converges absolutely because

$$
\sum_{n=0}^\infty\left|\int_I f_n\right|
\leq (\beta-\alpha)\sum_{n=0}^\infty\|f_n\|_\infty<\infty.
$$

### Exercise 5

Define $$f^+(x)=\max\{f(x),0\}$$ and $$f^-(x)=\max\{-f(x),0\}$$. The map $$t\mapsto\max\{t,0\}$$ is Lipschitz, and applying it to staircase approximations of $$f$$ gives staircase functions converging uniformly to $$f^+$$. Thus $$f^+\in S(I,\mathbb R)$$; applying the same argument to $$-f$$ gives $$f^-\in S(I,\mathbb R)$$.

If $$h\in S(I,\mathbb R)$$ is nonnegative, Remark 1.3 gives nonnegative staircase functions converging uniformly to $$h$$. Their integrals are nonnegative, and continuity of integration then yields $$\int_I h\geq0$$. Since $$f^+-f=f^-\geq0$$ and $$f^-+f=f^+\geq0$$, applying this positivity to these two functions gives

$$
\int_I f\leq\int_I f^+,
\qquad
-\int_I f\leq\int_I f^-.
$$

### Exercise 6

Suppose $$f:I\to E$$ is Riemann integrable, with integral $$e\in E$$. Apply the definition with $$\varepsilon=1$$ and choose a partition $$Z=(\alpha_0,\ldots,\alpha_n)$$ whose mesh is less than the resulting $$\delta$$. Fix one cell $$J_j=[\alpha_{j-1},\alpha_j]$$ and any $$x,y\in J_j$$. Choose two Riemann sums for this same partition that use the same between points on every other cell, and use $$x$$ and $$y$$, respectively, on $$J_j$$. Each sum is within distance $$1$$ of $$e$$, so their difference has norm less than $$2$$. Therefore

$$
(\alpha_j-\alpha_{j-1})\,\|f(x)-f(y)\|<2.
$$

Fixing one point $$y_j\in J_j$$ gives, for every $$x\in J_j$$,

$$
\|f(x)\|\leq\|f(y_j)\|+\frac{2}{\alpha_j-\alpha_{j-1}}.
$$

This is a finite bound on each cell, and the finitely many cells cover $$I$$. Hence $$f$$ is bounded, that is, $$f\in B(I,E)$$.

### Exercise 7

Write $$U(f,I,Z)$$ and $$L(f,I,Z)$$ for the upper and lower sums. If $$Z'$$ refines $$Z$$, each cell of $$Z'$$ lies in a cell of $$Z$$. On that smaller cell, the supremum of $$f$$ cannot exceed the supremum on the containing cell, and the infimum cannot be smaller. Since the lengths of the refined cells inside each original cell add up to its length, summing these inequalities gives

$$
U(f,I,Z')\leq U(f,I,Z),
\qquad
L(f,I,Z)\leq L(f,I,Z').
$$

For arbitrary partitions $$Z$$ and $$Z'$$, their common refinement $$Z\vee Z'$$ refines both. Consequently,

$$
L(f,I,Z)\leq L(f,I,Z\vee Z')
\leq U(f,I,Z\vee Z')\leq U(f,I,Z'),
$$

which proves (ii).

### Exercise 8

Set $$M=\|f\|_\infty$$. There are exactly $$m-n$$ new interior partition points when $$Z$$ is refined to $$Z'$$. Only the coarse cells containing at least one new point can change their contribution to either sum, so there are at most $$m-n$$ affected cells. Consider one such cell $$J$$, of length $$|J|\leq\Delta_Z$$. Its upper-sum decrease is nonnegative and at most

$$
|J|\sup_J f-\sum_{J_k\subset J}|J_k|\sup_{J_k}f
\leq |J|\bigl(\sup_J f-\inf_J f\bigr)
\leq 2M\Delta_Z.
$$

Summing over the affected cells proves

$$
U(f,I,Z)-U(f,I,Z')\leq2(m-n)\|f\|_\infty\Delta_Z.
$$

For the lower sums, refinement can only increase the sum. On each affected cell the increase is at most $$|J|(\sup_J f-\inf_J f)\leq2M\Delta_Z$$. Summing gives

$$
L(f,I,Z')-L(f,I,Z)\leq2(m-n)\|f\|_\infty\Delta_Z.
$$

### Exercise 9

Let

$$
\overline{\int_I}f:=\inf_Z U(f,I,Z),
\qquad
\underline{\int_I}f:=\sup_Z L(f,I,Z),
$$

where the infimum and supremum range over all partitions of $$I$$.

**(i)** For any partitions $$Z$$ and $$Z'$$, Exercise 7(ii) gives $$L(f,I,Z)\leq U(f,I,Z')$$. Taking the supremum over $$Z$$ on the left and the infimum over $$Z'$$ on the right yields

$$
\underline{\int_I}f\leq\overline{\int_I}f.
$$

**(ii)** Fix $$\varepsilon>0$$. By the definitions of infimum and supremum, choose partitions $$Z_U$$ and $$Z_L$$ such that

$$
U(f,I,Z_U)<\overline{\int_I}f+\frac\varepsilon2,
\qquad
L(f,I,Z_L)>\underline{\int_I}f-\frac\varepsilon2.
$$

Let $$r$$ be at least the number of cells in each of these two partitions, and put $$M=\|f\|_\infty$$. If $$M=0$$, the assertions hold immediately. Otherwise choose $$\delta>0$$ such that $$2rM\delta<\varepsilon/2$$. For an arbitrary partition $$Z$$ with $$\Delta_Z<\delta$$, let $$R_U=Z\vee Z_U$$. Exercise 8, applied to the refinement of $$Z$$, bounds the change in its upper sum by $$2rM\Delta_Z$$, while Exercise 7 gives $$U(f,I,R_U)\leq U(f,I,Z_U)$$. Since $$\overline{\int_I}f\leq U(f,I,Z)$$, it follows that

$$
0\leq U(f,I,Z)-\overline{\int_I}f
<\frac\varepsilon2+2rM\Delta_Z<\varepsilon.
$$

For the lower sum, set $$R_L=Z\vee Z_L$$. Refinement gives $$L(f,I,R_L)\geq L(f,I,Z_L)$$, and Exercise 8 bounds $$L(f,I,R_L)-L(f,I,Z)$$ by $$2rM\Delta_Z$$. Since $$L(f,I,R_L)\leq\underline{\int_I}f$$, we obtain

$$
0\leq\underline{\int_I}f-L(f,I,Z)
<\frac\varepsilon2+2rM\Delta_Z<\varepsilon.
$$

Both estimates hold for every sufficiently fine partition, as required.

### Exercise 10

Let $$f\in B(I,\mathbb R)$$, and write $$U(Z)=U(f,I,Z)$$ and $$L(Z)=L(f,I,Z)$$.

**(i) implies (ii).** Suppose $$f$$ is Riemann integrable with integral $$e$$. Given $$\varepsilon>0$$, choose a mesh bound from the definition of Riemann integrability and take a partition $$Z$$ below that bound. Every Riemann sum for $$Z$$ lies between $$L(Z)$$ and $$U(Z)$$, and every such sum is within $$\varepsilon$$ of $$e$$. Thus $$L(Z)\geq e-\varepsilon$$ and $$U(Z)\leq e+\varepsilon$$. By the definitions of the lower and upper integrals,

$$
e-\varepsilon\leq\underline{\int_I}f
\leq\overline{\int_I}f\leq e+\varepsilon.
$$

Letting $$\varepsilon\downarrow0$$ proves that both integrals equal $$e$$.

**(ii) implies (iii).** If the upper and lower integrals have the same value, Exercise 9(ii) shows that for every sufficiently fine partition $$Z$$, both $$U(Z)$$ and $$L(Z)$$ are within $$\varepsilon/2$$ of that value. Hence $$U(Z)-L(Z)<\varepsilon$$.

**(iii) implies (i).** A partition with $$U(Z)-L(Z)<\varepsilon$$ satisfies

$$
0\leq\overline{\int_I}f-\underline{\int_I}f
\leq U(Z)-L(Z)<\varepsilon,
$$

so the upper and lower integrals are equal; call their common value $$e$$. By Exercise 9(ii), for all sufficiently fine partitions $$Z$$,

$$
0\leq U(Z)-e<\frac\varepsilon2,
\qquad
0\leq e-L(Z)<\frac\varepsilon2.
$$

Every Riemann sum for $$Z$$ lies between $$L(Z)$$ and $$U(Z)$$, and therefore differs from $$e$$ by less than $$\varepsilon$$. This is precisely Riemann integrability with integral $$e$$. The three implications also show that whenever these conditions hold,

$$
\overline{\int_I}f=\int_I f\,dx=\underline{\int_I}f.
$$
