# Chapter X — Integration Theory

## 1. Measurable functions

These notes solve Exercises 1–19. Unless explicitly stated otherwise, $$(X,\mathcal A,\mu)$$ is a complete sigma-finite measure space and $$E$$ is a Banach space, as assumed at the beginning of this section. A $$\mu$$-simple function has finite range, measurable level sets, and support of finite measure. We write $$\overline{\mathbb R}=[-\infty,\infty]$$. For extended-valued functions, sums are used only when defined pointwise, and $$0(\pm\infty)=0$$.

### Exercise 1

Let $$H$$ be separable and choose a countable dense set $$\{e_j\}$$ in its closed unit ball. For every $$v\in H$$, continuity of the inner product and the Cauchy–Schwarz inequality give

$$
\|v\|=\sup_j |(v\mid e_j)|.
$$

The upper bound is Cauchy–Schwarz; for $$v\ne0$$, approximate $$v/\|v\|$$ by the $$e_j$$ to get equality. Thus weak measurability makes $$\|f\|$$ measurable as a countable supremum. This proves (a).

For (b), if $$f$$ is strongly measurable, take simple functions $$s_k\to f$$ almost everywhere. Each scalar function $$(s_k\mid e)$$ is simple, and its limit is $$(f\mid e)$$, so $$f$$ is weakly measurable.

Conversely, for each fixed $$h\in H$$ the function $$f-h$$ is weakly measurable, hence $$\|f-h\|$$ is measurable by (a). Choose a countable dense set $$\{h_j\}$$ in $$H$$. For every open $$U\subset H$$,

$$
f^{-1}(U)=\bigcup_{\substack{j,\,r\in\mathbb Q_{>0}\\ B(h_j,r)\subset U}}\{x:\|f(x)-h_j\|<r\}.
$$

The union is countable, so $$f$$ is Borel measurable. Its range is separable because it is a subset of the separable metric space $$H$$. The measurable-function criterion, together with completeness and sigma-finiteness, now proves strong measurability.

### Exercise 2

**(a) True.** An admissible function on the real line is jump continuous on every compact interval. On each compact interval it is a uniform limit of step functions. Those step functions have Borel level sets and finite range; after restriction to the interval they are Borel measurable. Consequently the restriction of the admissible function is Borel measurable and has separable range, contained in the closure of the countable union of the approximants' ranges. Exhausting the line by compact intervals shows that the entire function is Borel measurable and has separable range.

For completeness of the argument with the incomplete Borel–Lebesgue measure $$\beta_1$$, approximate directly, without invoking the complete-space criterion. For each $$k$$ choose a step function on $$[-k,k]$$ whose uniform error is less than $$1/k$$, and extend it by zero outside that interval. Each extension has finite range, Borel level sets, and bounded support, so it is $$\beta_1$$-simple. The extensions converge pointwise to $$f$$.

**(b) False** when $$E\ne\{0\}$$. Fix $$e\ne0$$ and put $$f=e\chi_{\mathbb Q}$$. The functions $$e\chi_{\{q_1,\ldots,q_k\}}$$ are $$\beta_1$$-simple and converge pointwise to $$f$$. But $$f$$ has no one-sided limit at any point, because the rationals and irrationals are both dense; it is not admissible. If $$E=\{0\}$$, both spaces contain only the zero function.

### Exercise 3

Let $$\nu=\mu|_{\mathcal A|_A}$$. If $$s$$ is simple on $$A$$, extend it by zero to $$X$$. Its nonzero level sets are the same measurable subsets of $$A$$ and have finite $$\mu$$-measure. Conversely, restricting a simple function on $$X$$ to $$A$$ gives a $$\nu$$-simple function. This establishes the first equivalence, including the zero level set by taking complements in the relevant domain.

If $$f|_A$$ is $$\nu$$-measurable, extend its simple approximants by zero. A $$\nu$$-null exceptional set is a $$\mu$$-null subset of $$X$$, so the extensions converge almost everywhere to $$\chi_A f$$. Conversely, restrict simple approximants to $$\chi_A f$$ to $$A$$; the intersection of the exceptional set with $$A$$ is $$\nu$$-null. This proves the second equivalence.

### Exercise 4

Suppose $$f:\mathbb R\to\overline{\mathbb R}$$ is increasing. For each real $$a$$, the set $$\{x:f(x)>a\}$$ is an upper set: it is empty, all of $$\mathbb R$$, or an interval of the form $$(c,\infty)$$ or $$[c,\infty)$$. Each is Borel. These strict superlevel sets characterize extended-real measurability, so $$f$$ is Borel measurable. A decreasing function is handled in the same way, or by applying the increasing case to $$-f$$.

### Exercise 5

For $$f,g:X\to\overline{\mathbb R}$$ measurable, the density of the rationals in the extended order gives

$$
[f<g]=\bigcup_{q\in\mathbb Q}\bigl([f<q]\cap[g>q]\bigr).
$$

This includes cases involving either infinity. The right side is measurable. Interchanging $$f$$ and $$g$$ and taking complements shows that $$[f\le g]$$ is measurable. Finally,

$$
[f=g]=[f\le g]\cap[g\le f],\qquad [f\ne g]=[f<g]\cup[g<f].
$$

All four sets belong to $$\mathcal A$$.

### Exercise 6

Let $$u=\liminf_j f_j$$ and $$v=\limsup_j f_j$$. Both are measurable: they are built from countable suprema and infima. A sequence in the extended real line converges to an element of $$\overline{\mathbb R}$$ exactly when $$u=v$$, including the cases of limits $$\pm\infty$$. Hence $$K=[u=v]$$ is measurable by Exercise 5.

### Exercise 7

**(a) True.** If $$f$$ is measurable, the functions $$f^+=\max(f,0)$$ and $$f^-=\max(-f,0)$$ are measurable. Conversely, if both parts are measurable, then $$f=f^+-f^-$$ is defined pointwise: the two parts never simultaneously take the value $$+\infty$$. Therefore $$f$$ is measurable.

**(b) False in general.** Choose a nonmeasurable subset $$V$$ of a complete sigma-finite measure space, for example a non-Lebesgue-measurable subset of $$[0,1]$$, and set $$f=1$$ on $$V$$ and $$f=-1$$ on $$V^c$$. Then $$|f|=1$$ is measurable, but $$[f>0]=V$$ is not. The forward implication is nevertheless always true.

### Exercise 8

**(a)** The full space $$\overline{\mathbb R}^X$$ has all the required closure properties. For measurable functions, scalar multiplication and any everywhere-defined sum are measurable: use extended-real Borel arithmetic, or approximate by finite truncations. For countable suprema,

$$
\left[\sup_j f_j>a\right]=\bigcup_j[f_j>a]\qquad(a\in\mathbb R),
$$

so the supremum is measurable. The zero function shows nonemptiness.

**(b)** Each nonempty Baire function space contains the zero function, since it is closed under multiplication by zero. Thus their intersection is nonempty; each required closure property is inherited from every member of the family. For an empty family, the intersection is the whole space, already covered by (a).

### Exercise 9

Write $$\mathcal S=\mathcal S(X,\mu,\mathbb R)$$. By Exercise 8, $$\mathcal L^0(X,\mu,\overline{\mathbb R})$$ is a Baire function space containing $$\mathcal S$$, so $$\sigma(\mathcal S)$$ is contained in it.

Conversely, every Baire function space is closed under countable infima, since $$\inf_j u_j=-\sup_j(-u_j)$$. It is therefore closed under pointwise limits whenever these exist in $$\overline{\mathbb R}$$: a limit equals $$\sup_k\inf_{j\ge k}u_j$$.

Let $$f$$ be measurable. By the nonnegative approximation theorem, there are increasing sequences of nonnegative $$\mu$$-simple functions $$s_j\uparrow f^+$$ and $$t_j\uparrow f^-$$ pointwise. Their limits lie in $$\sigma(\mathcal S)$$. Since $$f^+-f^-$$ is defined everywhere, closure under multiplication and defined addition yields $$f\in\sigma(\mathcal S)$$. Sigma-finiteness is used in the approximation theorem to give the simple approximants finite-measure support.

### Exercise 10

Let $$\mathcal B=\sigma(C(\mathbb R^n,\mathbb R))$$. Borel measurable functions form a Baire function space containing the continuous functions, so all members of $$\mathcal B$$ are Borel measurable. Conversely, $$1\in\mathcal B$$. If $$U$$ is open and not the whole space, the continuous functions

$$
u_k(x)=\min\{1,k\,\operatorname{dist}(x,U^c)\}
$$

increase to $$\chi_U$$; the cases $$U=\varnothing$$ and $$U=\mathbb R^n$$ are immediate. Let $$\mathcal D=\{A:\chi_A\in\mathcal B\}$$. It contains every open set, is closed under complements because $$\chi_{A^c}=1-\chi_A$$, and is closed under countable unions because $$\chi_{\cup_j A_j}=\sup_j\chi_{A_j}$$. Hence $$\mathcal D$$ contains every Borel set.

A nonnegative extended Borel function is the increasing pointwise limit of finite linear combinations of Borel indicators, obtained by dyadic rounding and truncation. Applying this to the positive and negative parts proves that every extended-real Borel function belongs to $$\mathcal B$$.

The right-hand side in the exercise uses the book's **extended-real** definition: inverse images of real open sets and of each infinity must be Borel. By Exercise 17(c)–(e), this is exactly Borel measurability as a map into $$\overline{\mathbb R}$$. Therefore the two sides agree.

The distinction between definitions matters here: $$\beta_n$$ is not complete. A real-valued function which is merely an almost-everywhere limit of $$\beta_n$$-simple functions can fail to be Borel measurable. For instance, the indicator of a non-Borel subset of a Borel null set is zero almost everywhere but is not Borel measurable. Thus one should not justify this particular extended-real equality by applying the complete-space equivalence to $$\beta_n$$.

### Exercise 11

Let $$V\subset[0,1]$$ be non-Lebesgue-measurable. For each $$x\in V$$, the singleton indicator $$\chi_{\{x\}}$$ is measurable. Their supremum is $$\chi_V$$, which is not measurable. Thus uncountability cannot replace countability in the supremum theorem.

### Exercise 12

**(a)** For each positive integer $$m$$ choose measurable $$A_m$$ with $$\mu(A_m^c)<1/m$$ on which the sequence converges uniformly. Put $$K=\bigcup_m A_m$$. Then $$K^c\subset A_m^c$$ for every $$m$$, so $$\mu(K^c)=0$$. The sequence converges at every point of $$K$$. Define $$f$$ to be its limit on $$K$$ and zero outside. The functions $$\chi_K f_j$$ are measurable and converge pointwise to $$f$$, proving $$f$$ measurable. By construction $$f_j\to f$$ almost everywhere. Uniform convergence on each $$A_m$$ also identifies the limit there with $$f$$.

**(b)** On $$[0,1-\eta]$$, $$\sup x^j=(1-\eta)^j\to0$$. Given $$\delta>0$$, choose $$0<\eta<\min(1,\delta)$$. The complement has measure $$\eta<\delta$$, so convergence is almost uniform. The pointwise limit is zero on $$[0,1)$$ and one at $$1$$.

Suppose convergence were uniform on the complement of a null set $$N$$. That complement meets every interval $$(1-\eta,1)$$, so for every fixed $$j$$ the supremum of $$x^j$$ over its points below 1 equals 1. Hence the supremum of the error from the pointwise limit is at least 1 for every $$j$$, a contradiction. This holds whether or not $$1\in N$$.

### Exercise 13

**(a)** Let $$K$$ be a measurable full-measure set on which $$f_j\to f$$. For $$k\ge1$$ set

$$
D_k=K\cap\bigcup_{j\ge k}\{x:\|f_j(x)-f(x)\|\ge\varepsilon\}.
$$

The sets $$D_k$$ decrease to the empty set. Because $$\mu(X)<\infty$$, continuity from above gives $$\mu(D_k)\to0$$. Choose $$k$$ with $$\mu(D_k)<\delta$$ and set $$A=K\setminus D_k$$. Then $$\mu(A^c)<\delta$$ and the required strict inequality holds for every $$j\ge k$$ on $$A$$.

**(b)** For each $$m\ge1$$ apply (a) with $$\varepsilon=1/m$$ and $$\delta/2^{m+1}$$, obtaining $$A_m$$ and $$k_m$$. On $$A=\bigcap_m A_m$$, the sequence converges uniformly to $$f$$: given a tolerance, choose $$m$$ with $$1/m$$ smaller than it. Moreover $$\mu(A^c)\le\sum_m\mu(A_m^c)<\delta$$. This is Egorov's theorem.

**(c)** On the real line with Lebesgue measure, $$f_j=\chi_{[j,j+1]}$$ converges pointwise to zero. If $$\mu(A^c)<1/2$$, no entire interval $$[j,j+1]$$ is contained in $$A^c$$. Thus $$\sup_A|f_j|=1$$ for every $$j$$, so convergence is not almost uniform.

### Exercise 14

**(a)** Given $$\varepsilon,\delta>0$$, choose $$A$$ with $$\mu(A^c)<\delta$$ and uniform convergence on $$A$$. For all sufficiently large $$j$$, the error is less than $$\varepsilon$$ on $$A$$. Therefore

$$
\mu\{\|f_j-f\|\ge\varepsilon\}\le\mu(A^c)<\delta,
$$

which proves convergence in measure.

**(b)** For every $$\varepsilon>0$$, the triangle inequality gives

$$
[\|f-g\|\ge\varepsilon]\subset
[\|f-f_j\|\ge\varepsilon/2]\cup[\|f_j-g\|\ge\varepsilon/2].
$$

Taking measures and letting $$j\to\infty$$ shows that the left set is null. The countable union of these sets for $$\varepsilon=1/m$$ is $$[f\ne g]$$, hence $$f=g$$ almost everywhere.

**(c)** Enumerate, level by level, the dyadic intervals $$I_{m,k}=[k2^{-m},(k+1)2^{-m})$$ for $$0\le k<2^m-1$$ and the last interval $$I_{m,2^m-1}=[1-2^{-m},1]$$, for $$m=1,2,\ldots$$. Define $$f_j$$ as the indicator of the corresponding interval. Their measures tend to zero, so $$f_j\to0$$ in measure. Each point belongs to exactly one interval at each level and lies outside at least one interval at each level. Thus the values 1 and 0 occur infinitely often at every point, and the sequence converges nowhere.

**(d)** The sequence $$\chi_{[j,j+1]}$$ tends pointwise to zero on $$\mathbb R$$, but for $$\varepsilon=1/2$$ the measure of its error set is always 1. It therefore does not converge to zero in measure.

### Exercise 15

Choose increasing indices $$j_k$$ such that

$$
\mu\{\|f_{j_k}-f\|\ge 2^{-k}\}<2^{-k}.
$$

This is possible by convergence in measure. Define $$B_m=\bigcup_{k\ge m}\{\|f_{j_k}-f\|\ge2^{-k}\}$$. Then $$\mu(B_m)\le\sum_{k\ge m}2^{-k}\to0$$. The decreasing intersection $$N=\bigcap_m B_m$$ is null, since $$N\subset B_m$$ for every $$m$$. If $$x\notin N$$, for some $$m$$ and every $$k\ge m$$ one has $$\|f_{j_k}(x)-f(x)\|<2^{-k}$$. Thus the subsequence converges to $$f$$ almost everywhere. In fact it converges uniformly to $$f$$ outside each $$B_m$$, so it is almost uniformly convergent as well.

### Exercise 16

**(a)** For $$1\le p<\infty$$, Minkowski's inequality for finite sums, followed by passage to the limit, gives $$\|x+y\|_p\le\|x\|_p+\|y\|_p$$ and shows that $$x+y\in\ell_p$$. Homogeneity and definiteness are immediate, so this is a normed vector space.

The finitely supported sequences with rational entries, or with rational real and imaginary parts in the complex case, form a countable set. For any $$x\in\ell_p$$, first truncate its tail so that its $$p$$-norm is small, then approximate its finitely many remaining coordinates by rational values. This gives arbitrarily close elements of the countable set, proving separability.

**(b)** For each subset $$A\subset\mathbb N$$, let $$x^A=\chi_A$$ as a bounded sequence. There are uncountably many such sequences and any two distinct ones have distance 1 in $$\ell_\infty$$. Open balls of radius $$1/3$$ about them are pairwise disjoint. A countable dense set would have to meet every one of these balls, which is impossible. Thus $$\ell_\infty$$ is not separable.

### Exercise 17

**(a)** For finite points the prescribed neighborhoods are the ordinary real neighborhoods. At $$+\infty$$ they contain a tail $$(a,\infty]$$, and at $$-\infty$$ a tail $$[-\infty,a)$$. This is precisely the stated criterion for openness, in both directions.

**(b)** The map

$$
h:\overline{\mathbb R}\longrightarrow[-1,1],\qquad h(x)=\frac{2}{\pi}\arctan x,\quad h(\pm\infty)=\pm1,
$$

is a bijection. The neighborhood criterion in (a) shows that both it and its inverse are continuous, so it is a homeomorphism. The interval $$[-1,1]$$ is compact; hence so is $$\overline{\mathbb R}$$.

**(c)** The set $$\mathbb R$$ is open in $$\overline{\mathbb R}$$, and its subspace topology is the usual one. Thus the trace of the extended Borel sigma-algebra on $$\mathbb R$$ is $$\mathcal B(\mathbb R)$$. The singleton sets $$\{\pm\infty\}$$ are closed. Consequently every extended Borel set is of the form $$B\cup F$$ with $$B\in\mathcal B(\mathbb R)$$ and $$F\subset\{-\infty,\infty\}$$, and every set of that form is Borel.

**(d)** Taking the trace in (c) gives $$\mathcal B(\overline{\mathbb R})|_{\mathbb R}=\mathcal B(\mathbb R)$$.

**(e)** If $$f$$ is measurable in the section's extended-real sense, the strict real threshold sets $$[f>a]$$ are measurable. These are inverse images of $$(a,\infty]$$, and together with complements and countable operations they generate all extended Borel inverse images; equivalently, use (c). Hence $$f$$ is $$\mathcal A$$–$$\mathcal B(\overline{\mathbb R})$$ measurable. Conversely, every threshold set is such an inverse image, so the section's threshold criterion gives $$\mu$$-measurability. Completeness and sigma-finiteness are those assumed throughout this section.

### Exercise 18

Choose a countable dense subset $$D\subset S$$. Let $$V$$ be all finite linear combinations of elements of $$D$$ with rational coefficients in the real case, or coefficients in $$\mathbb Q+i\mathbb Q$$ in the complex case. Then $$V$$ is countable. Approximate each element of $$S$$ by elements of $$D$$ and each scalar coefficient by rational scalars: every finite linear combination of elements of $$S$$ lies in $$\overline V$$. Therefore

$$
\overline{\operatorname{span}S}=\overline V.
$$

The left side is separable and is a closed linear subspace of the Banach space $$E$$, so it is complete and hence a separable Banach space. If $$S$$ is empty, the span is $$\{0\}$$ and the conclusion is immediate.

### Exercise 19

For each $$k\ge1$$ define the continuous function

$$
g_k(z)=\frac{z}{\max\{|z|,1/k\}},\qquad z\in\mathbb K.
$$

The composition $$g_k\circ f$$ is measurable; this follows by composing simple approximants to $$f$$ with $$g_k$$, noting that $$g_k(0)=0$$ preserves finite-measure support. If $$f(x)=0$$ all terms are zero. If $$f(x)\ne0$$, then for sufficiently large $$k$$ the expression equals $$f(x)/|f(x)|$$. Hence $$g_k\circ f\to\operatorname{sign}f$$ pointwise, proving that the sign function is measurable.
