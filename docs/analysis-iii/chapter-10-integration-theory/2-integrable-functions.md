# Chapter X — Integration Theory

## 2. Integrable functions

These notes address Exercises 1–15. Unless stated otherwise, $$(X,\mathcal A,\mu)$$ is a complete sigma-finite measure space and $$E$$ is a Banach space, as in the section. The notation $$\mathcal L^1$$ denotes actual functions rather than equivalence classes, and $$\|f\|_1=\int_X\|f\|\,d\mu$$ is a seminorm. A simple function has finite range and finite-measure nonzero support. In Exercises 3 and 12 we also use the nonnegative extended integral and its monotone convergence theorem from Section X.3; the remaining arguments do not depend on those exercises.

### Exercise 1

Let $$\nu$$ be the restriction of $$\mu$$ to the trace sigma-algebra on $$A$$. If $$s$$ is $$\nu$$-simple on $$A$$, its zero extension $$\widetilde s$$ is $$\mu$$-simple; conversely, restricting a $$\mu$$-simple function to $$A$$ is $$\nu$$-simple. For such functions the definition of the integral gives

$$
\int_X\widetilde s\,d\mu=\int_A s\,d\nu,
\qquad \|\widetilde s\|_{1,\mu}=\|s\|_{1,\nu}.
$$

If $$f|_A$$ is integrable, extend an approximating $$L^1(\nu)$$-Cauchy sequence of simple functions by zero. It converges almost everywhere to $$\chi_Af$$ and is $$L^1(\mu)$$-Cauchy. Conversely, if $$\chi_Af$$ is integrable, restrict its defining approximants to $$A$$; restriction does not increase their $$L^1$$ distances and preserves almost-everywhere convergence. Thus the two integrability statements are equivalent. Passing to the limit in the displayed integral identity proves the required equality.

### Exercise 2

Uniform convergence makes $$(f_j)$$ Cauchy in the seminorm: for every $$j,k$$,

$$
\|f_j-f_k\|_1\le \mu(X)\sup_{x\in X}\|f_j(x)-f_k(x)\|.
$$

Completeness of $$\mathcal L^1$$ gives an integrable limit $$g$$ in this seminorm. A subsequence converges to $$g$$ almost everywhere, while the whole sequence converges pointwise to $$f$$; hence $$f=g$$ almost everywhere. The invariance of integrability under almost-everywhere equality yields $$f\in\mathcal L^1$$ and $$\|f_j-f\|_1\to0$$. Finally,

$$
\left\|\int_X f_j\,d\mu-\int_X f\,d\mu\right\|
\le\|f_j-f\|_1\longrightarrow0.
$$

This also covers $$\mu(X)=0$$.

### Exercise 3

Every admissible nonnegative simple $$\varphi\le f$$ almost everywhere has $$\int\varphi\,d\mu\le\int f\,d\mu$$ by monotonicity. For the reverse inequality, sigma-finiteness and measurability give nonnegative simple functions $$s_n\uparrow f$$ almost everywhere. For example, exhaust $$X$$ by finite-measure sets and use dyadic rounding and truncation there. After changing the approximants on a null set if necessary, they satisfy $$s_n\le f$$ almost everywhere. Monotone convergence for the nonnegative extended integral gives

$$
\int_X s_n\,d\mu\uparrow\int_X f\,d\mu.
$$

Thus the supremum is at least the right-hand side. The extended integral agrees with the finite integral for an integrable nonnegative function, proving equality.

### Exercise 4

Here the measure is defined on $$\mathcal P(X)$$, with $$\delta_a(B)=1$$ if $$a\in B$$ and zero otherwise. For any $$f:X\to\mathbb R$$, the simple function $$s=f(a)\chi_{\{a\}}$$ agrees with $$f$$ outside the null set $$X\setminus\{a\}$$. Hence every such $$f$$ is integrable and

$$
\mathcal L^1(X,\delta_a,\mathbb R)=\mathbb R^X,
\qquad \int_X f\,d\delta_a=f(a).
$$

### Exercise 5

For the measure from IX.4.10, $$\mu_F=\sum_{k\in\mathbb Z}p_k\delta_{a_k}$$ on $$\mathcal P(\mathbb R)$$, and the complement of the atoms is null. Set $$J=\{k:p_k>0\}$$. Then

$$
\mathcal L^1(\mathbb R,\mu_F,\mathbb K)
=\left\{f:\mathbb R\to\mathbb K:
\sum_{k\in J}p_k|f(a_k)|<\infty\right\},
\qquad
\int_{\mathbb R}f\,d\mu_F=\sum_{k\in J}p_k f(a_k).
$$

The series on the right converges absolutely; no condition is imposed at zero-mass atoms or away from the atoms. To prove sufficiency, use finite sums $$s_n=\sum_{k\in J,\,|k|\le n}f(a_k)\chi_{\{a_k\}}$$. These are simple, converge to $$f$$ almost everywhere, and are Cauchy in $$L^1$$ because their distances are tails of the displayed nonnegative series. Their integrals are the corresponding partial sums. Conversely, if $$f$$ is integrable, monotonicity applied to any finite collection of positive-mass atoms gives

$$
\sum_{k\in H}p_k|f(a_k)|\le\int_{\mathbb R}|f|\,d\mu_F
\qquad(H\subset J\text{ finite}),
$$

so the series is finite.

### Exercise 6

Theorem 2.11(i) already supplies linearity and continuity for real-valued functions. To prove positivity in (ii), take $$f\ge0$$ and a defining sequence of real simple functions $$s_n\to f$$ almost everywhere, Cauchy in $$L^1$$. The simple functions $$s_n^+=\max(s_n,0)$$ also converge to $$f$$ almost everywhere and satisfy $$|s_n^+-s_m^+|\le|s_n-s_m|$$. Thus they define the same integral, and each $$\int s_n^+\,d\mu\ge0$$. Passing to the limit proves $$\int f\,d\mu\ge0$$.

For (iii), let $$T:E\to F$$ be bounded linear and choose simple $$s_n\to f$$ almost everywhere, Cauchy in $$L^1$$. Then $$Ts_n$$ is simple, $$Ts_n\to Tf$$ almost everywhere, and

$$
\|Ts_n-Ts_m\|_1\le\|T\|\,\|s_n-s_m\|_1.
$$

Hence $$Tf$$ is integrable. The identity $$T(\int s_n\,d\mu)=\int Ts_n\,d\mu$$ holds for each simple function. Continuity of $$T$$ and passage to the limit prove the asserted identity.

### Exercise 7

**True.** Modify $$f$$ on a null set so that $$\|f\|\le M$$ everywhere. Strong measurability gives simple functions $$s_j\to f$$ almost everywhere. Fix $$\varepsilon>0$$ and let $$B_N$$ be the set where at least one of $$s_1,\ldots,s_N$$ is within $$\varepsilon$$ of $$f$$. Then $$\mu(X\setminus B_N)\to0$$ by finite measure and almost-everywhere convergence.

For each $$n$$ choose $$N_n$$ such that $$\mu(X\setminus B_{N_n})<2^{-n}$$ with tolerance $$1/n$$, and call the corresponding set $$B_n$$. On $$B_n$$ choose the first qualifying $$s_j$$ and put the resulting function $$t_n$$ equal to zero elsewhere. It has finite range and measurable level sets, hence is simple because $$\mu(X)<\infty$$. Moreover $$\|t_n\|\le M+1$$ everywhere and $$\|t_n-f\|<1/n$$ on $$B_n$$. Therefore

$$
\|t_n-t_m\|_1\le\left(\frac1n+\frac1m\right)\mu(X)
+2(M+1)\bigl(\mu(B_n^c)+\mu(B_m^c)\bigr)\longrightarrow0.
$$

The set of points lying in infinitely many $$B_n^c$$ is null, since the sum of their measures is finite. Outside that set $$\|t_n-f\|<1/n$$ eventually. Thus the simple functions $$t_n$$ converge to $$f$$ almost everywhere and are $$L^1$$-Cauchy, which proves integrability by definition.

### Exercise 8

Set $$a_j=\int_X f_j\,d\mu$$. The sequence $$(a_j)$$ is increasing and, since $$f_j\le f$$ almost everywhere, bounded above by $$\int f\,d\mu$$. For $$k\ge j$$, positivity gives

$$
\|f_k-f_j\|_1=\int_X(f_k-f_j)\,d\mu=a_k-a_j\longrightarrow0
$$

uniformly in $$k\ge j$$ as $$j\to\infty$$. Completeness therefore gives an $$L^1$$ limit $$g$$. A subsequence converges to $$g$$ almost everywhere, and the original sequence converges to $$f$$ almost everywhere; hence $$g=f$$ almost everywhere. Continuity of the integral proves $$a_j\uparrow\int_X f\,d\mu$$.

### Exercise 9

A countable union of null sets is null, so all $$f_j$$ are nonnegative simultaneously outside one null set. The finite sums $$s_n=\sum_{j=0}^n f_j$$ are integrable and increase almost everywhere to the integrable sum $$s=\sum_{j=0}^\infty f_j$$. Applying Exercise 8 to representatives changed on the common null set and using finite linearity yields

$$
\int_X\left(\sum_{j=0}^\infty f_j\right)d\mu
=\lim_{n\to\infty}\sum_{j=0}^n\int_X f_j\,d\mu
=\sum_{j=0}^\infty\int_X f_j\,d\mu.
$$

### Exercise 10

Let $$\mu(A)>0$$. Outside a null set $$N$$, the function is positive. Thus

$$
A\setminus N=\bigcup_{n=1}^\infty\bigl(A\setminus N\bigr)\cap\{f\ge1/n\}.
$$

At least one set in this union has positive measure; otherwise their union would be null. For such an $$n$$, monotonicity gives

$$
\int_A f\,d\mu\ge\frac1n\,
\mu\bigl((A\setminus N)\cap\{f\ge1/n\}\bigr)>0.
$$

### Exercise 11

For pairwise disjoint measurable $$A_j$$, the integrable functions $$f\chi_{A_j}$$ are nonnegative and their pointwise sum is $$f\chi_{\cup_j A_j}$$. Exercise 9 gives

$$
\varphi_f\left(\bigcup_j A_j\right)
=\sum_j\varphi_f(A_j).
$$

Also $$\varphi_f(\varnothing)=0$$ and $$\varphi_f(X)=\int_X f\,d\mu<\infty$$. This proves (a). If $$N$$ is $$\mu$$-null, $$f\chi_N=0$$ almost everywhere and $$\varphi_f(N)=0$$, proving (b).

If $$f>0$$ almost everywhere, Exercise 10 says that any measurable set of positive $$\mu$$-measure has positive $$\varphi_f$$-measure. Thus every $$\varphi_f$$-null measurable set is $$\mu$$-null, proving (c). Completeness follows: every subset of a $$\varphi_f$$-null measurable set is measurable by completeness of $$\mu$$ and is again $$\varphi_f$$-null.

### Exercise 12

Replace $$f$$ by its nonnegative representative $$f^+$$; this changes neither the measure nor the asserted integrals, since the two functions differ only on a $$\mu$$-null set. Put $$\nu=\varphi_f$$. Since $$f>0$$ almost everywhere, Exercise 11 shows that $$\nu$$ and $$\mu$$ have the same null sets and that $$\nu$$ is complete. In particular, the given real-valued $$\mu$$-measurable function $$g$$ is also $$\nu$$-measurable.

For a nonnegative finite simple function $$s=\sum_{i=1}^m c_i\chi_{A_i}$$, the definition of $$\nu$$ and finite linearity give

$$
\int_X s\,d\nu=\sum_i c_i\nu(A_i)
=\int_X sf\,d\mu.
$$

For any nonnegative measurable $$h$$, approximate it increasingly by nonnegative finite simple functions and apply the monotone convergence theorem to both measures. This proves the extended equality

$$
\int_X h\,d\nu=\int_X hf\,d\mu.
$$

Taking $$h=|g|$$ shows that $$g$$ is $$\nu$$-integrable exactly when $$gf$$ is $$\mu$$-integrable, by the scalar integrability criterion. When these integrals are finite, apply the same identity to $$g^+$$ and $$g^-$$ separately and subtract. This gives $$\int g\,d\nu=\int gf\,d\mu$$. Null-set equality also ensures that the argument is unaffected by representatives.

### Exercise 13

For $$\alpha>0$$, put $$A=\{f\ge\alpha\}$$ and choose an increasing finite-measure exhaustion $$X_n$$ of $$X$$. The simple functions $$\alpha\chi_{A\cap X_n}$$ are bounded above by $$f$$ almost everywhere, so monotonicity gives $$\alpha\mu(A\cap X_n)\le\int_X f\,d\mu$$. Passing to the limit proves

$$
\alpha\mu(A)\le\int_X f\,d\mu,
\qquad
\mu\{f\ge\alpha\}\le\frac1\alpha\int_X f\,d\mu.
$$

In particular, $$A$$ has finite measure.

### Exercise 14

The printed average requires the additional assumption $$0<\mu(X)<\infty$$; if $$\mu(X)=0$$, its denominator is zero. Let $$\alpha=\mu(X)^{-1}\int_X f\,d\mu$$. Every lower bound $$a$$ of the interval $$I$$ satisfies $$f\ge a$$ and hence $$\alpha\ge a$$; similarly, $$\alpha$$ is at most every upper bound. If an endpoint is excluded and $$f$$ lies strictly on its permitted side, the nonnegative integrable difference from that endpoint is positive everywhere, so Exercise 10 makes its integral strictly positive. Therefore $$\alpha\in I$$, including for open or half-open endpoints.

Convexity and differentiability yield the supporting-line inequality

$$
\varphi(y)\ge\varphi(\alpha)+\varphi'(\alpha)(y-\alpha)
\qquad(y\in I).
$$

At an endpoint, the derivative is understood in the appropriate one-sided sense. Substitute $$y=f(x)$$ and integrate. The linear term has integral zero because of the definition of $$\alpha$$, so division by $$\mu(X)$$ gives

$$
\varphi\!\left(\frac1{\mu(X)}\int_X f\,d\mu\right)
\le\frac1{\mu(X)}\int_X\varphi(f)\,d\mu.
$$

### Exercise 15

Given $$\varepsilon>0$$, density of simple functions in $$\mathcal L^1$$ gives a simple $$s$$ with $$\|f-s\|_1<\varepsilon/2$$. Since $$s$$ has finite range, $$M=\sup_X\|s\|<\infty$$. Choose $$\delta=\varepsilon/(2(M+1))$$. For measurable $$A$$ with $$\mu(A)<\delta$$,

$$
\left\|\int_A f\,d\mu\right\|
\le\int_A\|f-s\|\,d\mu+\int_A\|s\|\,d\mu
\le\|f-s\|_1+M\mu(A)<\varepsilon.
$$

The same proof actually establishes the stronger assertion $$\int_A\|f\|\,d\mu<\varepsilon$$.
