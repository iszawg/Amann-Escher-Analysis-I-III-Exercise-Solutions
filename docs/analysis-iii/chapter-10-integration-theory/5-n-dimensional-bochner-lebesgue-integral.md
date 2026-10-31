# Chapter X — Integration Theory

## 5. The n-dimensional Bochner–Lebesgue integral

These solutions address Exercises 1–13. Lebesgue measure is denoted by $$\lambda$$; $$E$$ is a Banach space, and equality of elements of an $$L^p$$ space means equality almost everywhere. On a compact interval, $$\operatorname{Var}(f,[a,b])$$ is the supremum of the sums of the norms of successive increments over all finite partitions. Exercise 5 requires a distinction between functions and equivalence classes. In Exercise 8(a), the printed completeness claim needs an additional hypothesis; Exercise 10 also requires its cumulative integral to be finite in order to define the stated Stieltjes measure.

### Exercise 1

Assume $$E\ne\{0\}$$ and choose $$e\in E$$ with $$\|e\|=1$$. For $$1\le p<q<\infty$$, choose $$\alpha$$ with $$1/q\le\alpha<1/p$$ and set

$$
f(x)=\mathbf1_{(0,1)}(x)x^{-\alpha}e.
$$

The criterion $$\int_0^1x^{-s}\,dx<\infty\iff s<1$$ gives $$f\in L^p\setminus L^q$$. When $$p<q=\infty$$, choose any $$0<\alpha<1/p$$; the same function belongs to $$L^p$$ and is not essentially bounded.

For $$1\le q<p<\infty$$, choose $$1/p<\alpha\le1/q$$ and let $$f(x)=\mathbf1_{(1,\infty)}(x)x^{-\alpha}e$$. Now $$\int_1^\infty x^{-s}\,dx<\infty$$ exactly when $$s>1$$, so $$f\in L^p\setminus L^q$$. Finally, for $$p=\infty$$ and finite $$q$$, the constant function $$e$$ is bounded but not in $$L^q(\mathbb R,E)$$. Thus all distinct pairs are covered. If $$E=\{0\}$$, every space is zero and the printed non-inclusion is false.

### Exercise 2

Since the support of $$f$$ is a compact subset of the open interval $$J$$, there are $$c<d$$ in $$J$$ such that the support is contained in $$(c,d)$$. The derivative is continuous on $$[c,d]$$ and vanishes off the support, hence is Lebesgue integrable on $$J$$. The fundamental theorem of calculus for Banach-valued continuously differentiable functions gives

$$
\int_J f'(t)\,dt=\int_c^d f'(t)\,dt=f(d)-f(c)=0.
$$

The equality between the classical and Lebesgue integrals applies to the continuous derivative on the compact interval.

### Exercise 3

Let $$s$$ and $$t$$ be arbitrary lower and upper staircase functions for $$f$$ on $$[0,1]$$. They are Lebesgue integrable, with their classical integrals equal to their Lebesgue integrals. Since $$s\le f\le t$$ and bounded measurable $$f$$ is integrable,

$$
\int_0^1s\le\int_{[0,1]}f\,d\lambda\le\int_0^1t.
$$

Taking the supremum over $$s$$ and the infimum over $$t$$ yields the lower and upper Riemann integral bounds. The proof also applies to bounded real-valued measurable functions without the nonnegativity assumption.

### Exercise 4

**(a)** Refining partitions shows that variation is subadditive and absolutely homogeneous, so $$BV(I,E)$$ is a vector space. If $$I=[a,b]$$ and $$f$$ is locally Lipschitz, compactness yields a global Lipschitz constant $$L$$ on $$I$$. Every partition then gives a sum at most $$L(b-a)$$; in particular $$C^{1-}(I,E)\subset BV(I,E)$$. For a function of bounded variation, $$\|f(x)\|\le\|f(a)\|+\operatorname{Var}(f,I)$$, proving boundedness.

**(b)** For a partition $$a=x_0<\cdots<x_m=b$$, additivity of the Bochner integral and the integral triangle inequality give

$$
\sum_{i=1}^m\|F(x_i)-F(x_{i-1})\|
\le\sum_{i=1}^m\int_{x_{i-1}}^{x_i}\|f(t)\|\,dt
=\|f\|_1.
$$

Taking the supremum over partitions gives the claim.

**(c)** Set $$v(x)=\operatorname{Var}(f,[a,x])$$. Additivity of variation over adjacent intervals implies that $$v$$ is increasing and, for $$x<y$$,

$$
v(y)-v(x)=\operatorname{Var}(f,[x,y])\ge|f(y)-f(x)|.
$$

Consequently both $$s^+=v$$ and $$s^-=v-f$$ are increasing, and $$f=s^+-s^-$$.

**(d)** A bounded monotone real function has finite one-sided limits at every interior point and the appropriate one-sided limits at the endpoints. By (c), a real BV function has these limits as well. Thus it is jump continuous, and the vector-space inclusion follows from (a).

**(e)** If $$f$$ is increasing, every partition sum telescopes to $$f(b)-f(a)$$; for a decreasing function it is $$f(a)-f(b)$$. Thus every monotone function has finite variation.

### Exercise 5

Write $$V=\operatorname{Var}(f,[a,b])$$ and $$v(t)=\operatorname{Var}(f,[a,t])$$. For $$s<t$$, additivity of variation gives $$\|f(t)-f(s)\|\le v(t)-v(s)$$. In particular $$f$$ is bounded. It is also strongly measurable: the monotone function $$v$$ has one-sided limits, and the preceding estimate shows that $$f$$ has norm-valued one-sided limits. Therefore $$f$$ is regulated and is a uniform limit of finite-valued staircase functions. Hence $$f\in L^\infty([a,b],H)$$. This argument works for any Banach space; separability of $$H$$ is not needed.

For $$0<h<b-a$$, the same estimate yields $$\|f(t+h)-f(t)\|\le v(t+h)-v(t)$$. Integrating and changing variables,

$$
\begin{aligned}
\int_a^{b-h}\|f(t+h)-f(t)\|\,dt
&\le\int_{b-h}^b v(t)\,dt-\int_a^{a+h}v(t)\,dt\\
&\le h\bigl(v(b)-v(a)\bigr)=hV.
\end{aligned}
$$

The final inequality uses monotonicity of $$v$$. The class map $$f\mapsto[f]$$ is linear because variation is subadditive. Strictly speaking it is not injective: the indicator of a single point has bounded variation but represents zero in $$L^\infty$$. Thus the printed vector-subspace statement is correct for the image of $$BV$$ in $$L^\infty$$, or after quotienting $$BV$$ by its almost-everywhere-zero functions, rather than as a literal inclusion of pointwise functions.

### Exercise 6

**(a)** Absolute continuity is stable under sums and scalar multiplication by the triangle inequality. If $$f\in BC^1(J,E)$$ and $$M=\sup_J\|f'\|<\infty$$, the mean value inequality gives $$\|f(y)-f(x)\|\le M|y-x|$$. Summing over the disjoint intervals proves absolute continuity. Applying the definition to a single interval proves continuity of every absolutely continuous function, including one-sided continuity at an endpoint in $$J$$.

**(b)** Let $$J=[a,b]$$. Choose $$\delta>0$$ from the absolute continuity condition for $$\varepsilon=1$$. Divide $$[a,b]$$ into finitely many subintervals of length less than $$\delta/2$$. On each, the variation is at most 1: the subintervals of any partition have total length below $$\delta$$. Variation is additive over the finitely many pieces, and is therefore finite.

**(c)** At stage $$n$$ of the middle-thirds Cantor construction, the Cantor function increases from 0 to 1 across the $$2^n$$ remaining closed intervals. The sum of its increases over these intervals is 1, while their total length is $$(2/3)^n\to0$$. Their interiors are pairwise disjoint, so the absolute-continuity condition with $$\varepsilon=1/2$$ fails. The Cantor function is continuous by its construction.

**(d)** For finitely many pairwise disjoint subintervals $$(\alpha_k,\beta_k)$$,

$$
\sum_k\|F(\beta_k)-F(\alpha_k)\|
\le\int_{\bigcup_k(\alpha_k,\beta_k)}\|f(t)\|\,dt.
$$

Absolute continuity of the integral of $$\|f\|\in L^1$$ makes the right side arbitrarily small when the sum of the lengths is small. This remains true on an unbounded interval. If $$\inf J=-\infty$$, the displayed primitive is understood only when its integral from $$-\infty$$ is defined; the same proof applies to a primitive based at any finite point of $$J$$.

### Exercise 7

**(a)** For $$x>0$$,

$$
f_1'(x)=2x\sin(1/x)-\cos(1/x),
$$

so $$|f_1'|\le3$$ on $$(0,1]$$. The mean value theorem and continuity at zero imply that $$f_1$$ is 3-Lipschitz on $$[0,1]$$. Its variation is therefore at most 3.

**(b)** Put $$x_k=(\pi/2+k\pi)^{-1/2}$$ for $$k\ge0$$. These points decrease to zero and

$$
f_2(x_k)=\frac{(-1)^k}{\pi/2+k\pi}.
$$

For each $$N$$, a partition containing $$x_N,\ldots,x_0$$ gives

$$
\operatorname{Var}(f_2,[0,1])\ge
\sum_{k=0}^{N-1}\left(\frac1{\pi/2+k\pi}+\frac1{\pi/2+(k+1)\pi}\right).
$$

The right side diverges with $$N$$ by comparison with the harmonic series, so $$f_2$$ is not of bounded variation.

### Exercise 8

**(a)** For disjoint measurable sets $$A_k$$, monotone convergence yields

$$
\int_{\bigcup_k A_k}f\,d\mu=\sum_k\int_{A_k}f\,d\mu.
$$

Thus $$\nu=f\,\mu$$ is a measure. It is absolutely continuous with respect to $$\mu$$, since the integral over a $$\mu$$-null set is zero.

The printed assertion that $$\nu$$ is always complete is **false**. Take completed Lebesgue measure on $$[0,1]$$ and $$f=0$$. Then every measurable set is $$\nu$$-null, but $$[0,1]$$ has subsets that are not Lebesgue measurable. Hence the zero measure on this sigma-algebra is not complete. A sufficient correction is $$f>0$$ $$\mu$$-almost everywhere: if $$\nu(A)=0$$, then $$f=0$$ $$\mu$$-almost everywhere on $$A$$, so $$\mu(A)=0$$ and all subsets of $$A$$ are measurable by completeness of $$\mu$$. More generally, completeness holds precisely when every subset of $$\{f=0\}$$ is in the sigma-algebra (using a measurable representative).

**(b)** Counting measure has no nonempty null set, so $$\nu\ll\mu$$. If $$\lambda=f\,\mu$$, evaluating at each singleton gives $$f(x)=\lambda(\{x\})=0$$ for every $$x\in[0,1]$$. Then the integral of $$f$$ is zero on the whole interval, contradicting $$\lambda([0,1])=1$$. The counting measure here is not sigma-finite; the argument does not require it to be.

### Exercise 9

If (ii) holds and $$\mu(A)=0$$, then $$\nu(A)<\varepsilon$$ for every $$\varepsilon>0$$, so $$\nu(A)=0$$.

Conversely, suppose (i) holds but (ii) fails. For some $$\varepsilon>0$$ choose measurable $$A_n$$ such that $$\mu(A_n)<2^{-n}$$ and $$\nu(A_n)\ge\varepsilon$$. Set $$B_m=\bigcup_{n\ge m}A_n$$ and $$B=\bigcap_m B_m$$. Then $$\mu(B)\le\sum_{n\ge m}2^{-n}$$ for every $$m$$, so $$\mu(B)=0$$. The sets $$B_m$$ decrease and $$\nu(B_1)<\infty$$, while $$\nu(B_m)\ge\varepsilon$$. Continuity from above gives $$\nu(B)\ge\varepsilon$$, contradicting $$\nu\ll\mu$$. Finiteness of $$\nu$$ is used here.

### Exercise 10

The definition $$F(x)=\int_{-\infty}^x f(t)\,dt$$ may be infinite: for $$f\equiv1$$ it equals $$\infty$$ everywhere. In that case it is not a real-valued measure-generating function and $$\mu_F$$ is undefined. In what follows, assume $$F(x)<\infty$$ for every $$x$$, as is necessary for the stated construction. The measures $$\mu_F$$ and $$\beta_1$$ have different natural domains; in (b), $$\mu_F\ll\beta_1$$ means absolute continuity of the restriction of $$\mu_F$$ to the Borel sigma-algebra.

**(a)** For $$a<b$$, additivity gives

$$
F(b)-F(a)=\int_{[a,b)} f\,d\lambda.
$$

The measure $$\eta(A)=\int_A f\,d\lambda$$ is locally finite because $$F(b)<\infty$$. Absolute continuity of the integral on each bounded interval also shows that $$F$$ is continuous and increasing, so it is a valid measure-generating function. It and the Stieltjes measure agree on half-open bounded intervals and hence, by uniqueness of locally finite Borel measures, on all Borel sets. If $$N$$ is Lebesgue-null, it lies in a Borel null set $$B$$; then $$\mu_F(B)=\eta(B)=0$$. Completeness of $$\mu_F$$ gives $$\mu_F(N)=0$$. Therefore $$\mu_F\ll\lambda$$. Under this finiteness assumption this conclusion holds even without separately assuming $$F\in W^1_1(\mathbb R,\mathbb R)$$.

**(b)** Let $$\nu=\mu_F|_{\mathcal B(\mathbb R)}$$. It is finite and absolutely continuous with respect to Borel Lebesgue measure. By Exercise 9, for each $$\varepsilon>0$$ there is $$\delta>0$$ such that a Borel set of Lebesgue measure below $$\delta$$ has $$\nu$$-measure below $$\varepsilon$$. For pairwise disjoint intervals $$(a_k,b_k)$$ with total length below $$\delta$$, the half-open intervals $$[a_k,b_k)$$ are also pairwise disjoint, and

$$
\sum_k|F(b_k)-F(a_k)|
=\sum_k\nu([a_k,b_k))
=\nu\left(\bigcup_k[a_k,b_k)\right)<\varepsilon.
$$

Thus $$F$$ is absolutely continuous on $$\mathbb R$$. The finiteness assumption on $$\mu_F$$ is sufficient for this argument, although not necessary in every example.

### Exercise 11

Let $$F(x)=\int_a^x f(t)\,dt=0$$ on $$I$$. For any bounded interval $$(u,v)\subset I$$, additivity gives $$\int_u^v f=F(v)-F(u)=0$$. Every open subset of $$I$$ is a countable disjoint union of intervals, and restriction to bounded pieces followed by dominated convergence shows that the integral of $$f$$ is zero over each such open subset. By Lebesgue regularity and integrability, the same holds for each measurable subset of $$I$$: approximate it in measure by open sets, using absolute continuity of the integral.

For each coordinate $$f_j$$, the measurable sets $$\{f_j>0\}$$ and $$\{f_j<0\}$$ therefore have zero integral of $$f_j$$. A nonnegative function with zero integral vanishes almost everywhere, so each coordinate is zero almost everywhere. There are only finitely many coordinates; hence $$f=0$$ almost everywhere. Equivalently, one may use the Lebesgue differentiation theorem, but the argument above does not require it.

### Exercise 12

Reflection preserves Lebesgue measure. For a Bochner-integrable function, the substitution $$x=-t$$ is valid first for simple functions and then by $$L^1$$ approximation. Thus

$$
\int_{-b}^{-a}f(x)\,dx=\int_a^b f(-t)\,dt.
$$

The intervals are disjoint up to their endpoints, which are null sets. If $$f$$ is odd, the two integrals cancel; if it is even, they are equal and their sum is $$2\int_a^b f(t)\,dt$$. The conclusion is unaffected by changing representatives on a null set.

### Exercise 13

At stage $$n$$ there are $$2^n$$ closed component intervals. At the next stage one open interval of length $$4^{-(n+1)}$$ is removed from each component. The removed intervals are disjoint, so

$$
\lambda(K)=1-\sum_{n=0}^\infty 2^n4^{-(n+1)}=\frac12.
$$

The set $$K=\bigcap_nK_n$$ is closed and measurable, and $$f=\mathbf1_K$$ is bounded on a finite-measure interval; hence $$f\in L^1[0,1]$$.

Each component of $$K_n$$ has length at most $$2^{-n}$$, so no nonempty open interval can be contained in every $$K_n$$. Thus $$K$$ has empty interior and its complement is open and dense. Let $$g=f$$ outside a null set $$N$$. If $$x\in K\setminus N$$, then $$g(x)=1$$. Every neighborhood of $$x$$ contains a nonempty open interval outside $$K$$, and that interval has points outside $$N$$; at such points $$g=0$$. Hence $$g$$ is discontinuous at every point of $$K\setminus N$$, a set of measure $$1/2$$. If $$g$$ were Riemann integrable, it would be bounded and continuous almost everywhere by Theorem 5.6, a contradiction. Thus no representative of $$[f]$$ is Riemann integrable.
