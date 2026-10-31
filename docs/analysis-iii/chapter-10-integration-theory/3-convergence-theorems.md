# Chapter X — Integration Theory

## 3. Convergence theorems

These solutions address Exercises 1–7. Unless otherwise stated, $$(X,\mathcal A,\mu)$$ is a complete sigma-finite measure space and $$E$$ is a Banach space. Integrals of nonnegative extended-real functions may be infinite; for an $$E$$-valued integrable function, $$\|f\|_1=\int_X\|f\|\,d\mu$$. See the textbook for the full statements.

### Exercise 1

Take Lebesgue measure on $$X=\mathbb R$$ and set $$f_j=\mathbf 1_{[j,j+1]}$$ for $$j\ge1$$ and $$g=1$$. Then $$0\le f_j\le g$$ everywhere, while $$g$$ is not integrable. Every fixed point belongs to only finitely many of the intervals, so $$\limsup_j f_j=0$$ everywhere. On the other hand, every $$f_j$$ has integral 1. Consequently,

$$
\limsup_{j\to\infty}\int_{\mathbb R}f_j\,d\lambda=1>0
=\int_{\mathbb R}\limsup_{j\to\infty}f_j\,d\lambda.
$$

Thus mere domination by a measurable function does not give the reverse Fatou inequality; the integrability of the dominating function matters.

### Exercise 2

By density of integrable simple functions, choose an integrable simple $$s$$ such that $$\|f-s\|_1<\varepsilon$$. Its nonzero support $$A=\{s\ne0\}$$ has finite measure. If $$B\in\mathcal A$$ contains $$A$$, then $$s=0$$ on $$B^c$$, and therefore

$$
\left\|\int_X f\,d\mu-\int_B f\,d\mu\right\|
=\left\|\int_{B^c}(f-s)\,d\mu\right\|
\le\int_{B^c}\|f-s\|\,d\mu
\le\|f-s\|_1<\varepsilon.
$$

The same finite-measure set $$A$$ works for every such $$B$$.

### Exercise 3

Every subsequence of $$(f_j)$$ still converges to $$f$$ in measure. By the subsequence principle (Exercise 1.15), it has a further subsequence converging to $$f$$ almost everywhere. In particular, take such a subsequence of the original sequence. Since the countably many domination inequalities hold outside a common null set, passage to the pointwise limit gives $$\|f\|\le g$$ almost everywhere. The domination theorem then gives $$f\in\mathcal L^1(X,\mu,E)$$.

Suppose that $$\|f_j-f\|_1$$ does not tend to zero. There are a number $$\delta>0$$ and a subsequence $$(f_{j_k})$$ with $$\|f_{j_k}-f\|_1\ge\delta$$ for every $$k$$. Extract a further subsequence converging to $$f$$ almost everywhere. Its differences from $$f$$ are bounded in norm by $$2g$$ almost everywhere, so dominated convergence yields

$$
\int_X\|f_{j_{k_\ell}}-f\|\,d\mu\longrightarrow0,
$$

contradicting the lower bound. Hence $$f_j\to f$$ in $$\mathcal L^1$$. Finally,

$$
\left\|\int_X f_j\,d\mu-\int_X f\,d\mu\right\|
\le\|f_j-f\|_1\longrightarrow0.
$$

### Exercise 4

We use the finite Lebesgue integrals of the given real-valued functions, allowing their extended-real representatives to be changed on null sets. For (i), $$g-f\ge0$$ almost everywhere and is integrable. Positivity and linearity give $$\int_Xg\,d\mu-\int_Xf\,d\mu=\int_X(g-f)\,d\mu\ge0$$.

For (ii), $$-|f|\le f\le |f|$$ almost everywhere. Applying (i) to both inequalities proves

$$
\left|\int_X f\,d\mu\right|\le\int_X|f|\,d\mu.
$$

For (iii), the measurable functions $$f\wedge g$$ and $$f\vee g$$ are integrable: for example, the identities

$$
f\wedge g=\frac{f+g-|f-g|}{2},\qquad
f\vee g=\frac{f+g+|f-g|}{2}
$$

hold almost everywhere, and $$|f-g|$$ is integrable because $$|f-g|\le|f|+|g|$$. Moreover,

$$
-(|f|+|g|)\le f\wedge g\le f\vee g\le |f|+|g|
$$

almost everywhere. Integrating these inequalities using (i) gives the asserted chain.

### Exercise 5

Put $$a=\liminf_j\int_X f_j\,d\mu$$, with values in $$[0,\infty]$$. If $$a=\infty$$ the inequality is immediate. Otherwise choose a subsequence $$(f_{j_k})$$ whose integrals converge to $$a$$. It still converges to $$f$$ in measure, so a further subsequence converges to $$f$$ almost everywhere. Fatou's lemma for that further subsequence yields

$$
\int_X f\,d\mu
\le\liminf_{\ell\to\infty}\int_X f_{j_{k_\ell}}\,d\mu
=a.
$$

This argument does not require the functions or their integrals to be finite in advance.

### Exercise 6

Let $$K=\operatorname{supp}f$$, which is compact. For $$r>0$$ write

$$
h_n(r)=\begin{cases}r,&n=1,\\
\log r,&n=2,\\
r^{2-n},&n\ge3.\end{cases}
$$

Thus the kernel used in the integral is $$H_n(y-x)=h_n(|y-x|)$$. For $$n=1$$ this equals $$|y-x|$$. This radial notation makes explicit the scalar argument in the displayed integral in the exercise.

**(a)** Fix $$y\in U$$. Since $$A\subset U^c$$ and $$U$$ is open, some $$\rho>0$$ satisfies $$|y-x|\ge\rho$$ for all $$x\in A$$. The continuous kernel is therefore bounded on the set of differences with $$x\in A\cap K$$: the distances also have an upper bound because $$K$$ is bounded. Hence, for some constant $$C_y$$,

$$
|\mathbf1_A(x)f(x)H_n(y-x)|\le C_y\|f\|_\infty\mathbf1_K(x).
$$

The right side is integrable. The left side is measurable, proving the desired integrability.

**(b)** Fix $$y_0\in U$$ and choose $$r>0$$ such that $$\overline{B(y_0,2r)}\subset U$$. For $$y\in B(y_0,r)$$ and $$x\in A$$, we have $$|y-x|\ge r$$. For each multi-index $$\alpha$$, all derivatives $$\partial_y^\alpha H_n(y-x)$$ are uniformly bounded when $$y\in B(y_0,r)$$ and $$x\in A\cap K$$: these differences lie in a bounded set separated from the origin. Thus

$$
|\mathbf1_A(x)f(x)\partial_y^\alpha H_n(y-x)|
\le C_\alpha\|f\|_\infty\mathbf1_K(x),
$$

an integrable bound independent of $$y$$. Repeated differentiation under the integral sign gives, locally and for every $$\alpha$$,

$$
\partial^\alpha F(y)=\int_A f(x)\partial_y^\alpha H_n(y-x)\,d\lambda_n(x),
\qquad F(y)=\int_A f(x)H_n(y-x)\,d\lambda_n(x).
$$

So $$F$$ is smooth. For $$n\ge2$$ the radial Laplacian formula is

$$
\Delta H_n(z)=h_n''(|z|)+\frac{n-1}{|z|}h_n'(|z|)=0
\quad(z\ne0),
$$

as direct substitution of $$\log r$$ or $$r^{2-n}$$ shows. For $$n=1$$, $$H_1(z)=|z|$$ has second derivative zero for $$z\ne0$$. Since $$y-x\ne0$$ for $$y\in U$$ and $$x\in A$$, the differentiated integral gives $$\Delta F(y)=0$$ throughout $$U$$.

### Exercise 7

Write $$C_0(\mathbb R^n,E)$$ for continuous functions vanishing at infinity. Part (i) asserts **non-inclusion**, not strict inclusion. It requires $$E\ne\{0\}$$; when $$E=\{0\}$$ both spaces contain only the zero function, and that assertion is false.

**(i)** Choose $$e\in E$$ with $$\|e\|=1$$, and put $$a_j=(3j,0,\ldots,0)$$ and $$r_j=2^{-j}$$ for $$j\ge1$$. Let $$\phi(t)=\max(1-t,0)$$ for $$t\ge0$$ and define

$$
f(x)=e\sum_{j=1}^{\infty}\phi\!\left(\frac{|x-a_j|}{r_j}\right).
$$

The closed supports are pairwise disjoint and locally finite. Thus $$f$$ is continuous and bounded by 1, while $$f(a_j)=e$$ and $$|a_j|\to\infty$$, so $$f\notin C_0$$. Translation and scaling give

$$
\int_{\mathbb R^n}\|f(x)\|\,dx
=\left(\int_{\mathbb R^n}\phi(|u|)\,du\right)
\sum_{j=1}^{\infty}r_j^n<\infty.
$$

Hence $$f\in\mathcal L^1\cap BC$$, establishing the non-inclusion.

**(ii)** Suppose $$f\in\mathcal L^1\cap BUC$$ does not vanish at infinity. Then there are $$\varepsilon>0$$ and points $$x_j\to\infty$$ with $$\|f(x_j)\|\ge\varepsilon$$. Uniform continuity provides $$r>0$$ such that $$\|f(x)-f(y)\|<\varepsilon/2$$ whenever $$|x-y|<r$$. Select a subsequence of the $$x_j$$ whose balls $$B(x_j,r)$$ are pairwise disjoint; this is possible because the points escape every bounded set. On each ball, $$\|f(x)\|\ge\varepsilon/2$$. Therefore, for every $$N$$,

$$
\int_{\mathbb R^n}\|f(x)\|\,dx
\ge\sum_{j=1}^N\int_{B(x_j,r)}\|f(x)\|\,dx
\ge N\frac{\varepsilon}{2}\lambda_n(B(0,r)),
$$

contradicting integrability as $$N\to\infty$$. Thus $$f\in C_0(\mathbb R^n,E)$$.
