# Chapter X — Integration Theory

## 4. Lebesgue spaces

These solutions address Exercises 1–18. Unless the exercise says otherwise, $$(X,\mathcal A,\mu)$$ is a complete sigma-finite measure space and $$E$$ is a Banach space over $$\mathbb K$$. Functions are identified when they agree almost everywhere. A simple function in the book has finite-measure nonzero support. We write $$\mathbf1_A$$ for the indicator of $$A$$. In the exercises about Radon measures, a sigma-compact space means a locally compact, sigma-compact metric space, as in Section X.1.

### Exercise 1

The sum and scalar multiples of finite-support simple functions are again such functions, so their equivalence classes form a vector subspace of $$L^p$$. Given $$f\in L^p$$, choose simple $$s_j\to f$$ almost everywhere. Put $$A_j=\{\|s_j\|\le 2\|f\|\}$$ and $$t_j=\mathbf1_{A_j}s_j$$. These are still simple with finite-measure nonzero support. At points where $$s_j\to f$$, one has $$t_j\to f$$: this is immediate if $$f\ne0$$, and otherwise $$t_j=0$$. Also $$\|t_j-f\|^p\le3^p\|f\|^p$$. Dominated convergence gives $$\|t_j-f\|_p\to0$$.

### Exercise 2

**(i)** Translation preserves Lebesgue measure and null sets, hence it is well defined on equivalence classes and $$\|\tau_a f\|_p=\|f\|_p$$ for every $$p\in[1,\infty]$$. Moreover $$\tau_a\tau_b=\tau_{a+b}$$ and $$\tau_a^{-1}=\tau_{-a}$$. Thus these maps form the asserted group homomorphism. Their operator norm is 1 provided $$E\ne\{0\}$$; for the zero space it is 0.

**(ii)** First let $$g\in C_c(\mathbb R^n,E)$$. Uniform continuity and a common compact support for $$\tau_a g-g$$ when $$|a|\le1$$ show that $$\|\tau_a g-g\|_p\to0$$. For arbitrary $$f\in L^p$$, choose such a $$g$$ with $$\|f-g\|_p<\varepsilon$$. Since translations are isometries,

$$
\|\tau_a f-f\|_p\le2\varepsilon+\|\tau_a g-g\|_p.
$$

Let $$a\to0$$ and then $$\varepsilon\to0$$.

**(iii)** Let $$\rho\ge0$$ be a smooth compactly supported function of integral 1 and set $$\rho_\varepsilon(y)=\varepsilon^{-n}\rho(y/\varepsilon)$$. For a bounded representative of $$f$$, the convolution $$g_\varepsilon=\rho_\varepsilon*f$$ is bounded and uniformly continuous, since

$$
\|g_\varepsilon(\cdot+h)-g_\varepsilon\|_{\sup}
\le\|f\|_\infty\|\rho_\varepsilon(\cdot+h)-\rho_\varepsilon\|_1.
$$

Fubini and the triangle inequality give

$$
\|g_\varepsilon-f\|_\infty
\le\int\rho_\varepsilon(y)\|\tau_y f-f\|_\infty\,dy\longrightarrow0.
$$

The functions $$g_\varepsilon$$ are therefore Cauchy in the essential supremum norm. For a continuous function this equals its ordinary supremum norm, because every nonempty open set has positive Lebesgue measure. Completeness of $$BUC$$ gives a uniform limit $$g\in BUC$$. The same convergence in $$L^\infty$$ shows that $$f=g$$ almost everywhere.

### Exercise 3

For a relatively compact open set $$U$$, $$\mu(U)<\infty$$. If $$\overline U\subset X_{j_1}\cup\cdots\cup X_{j_m}$$, then

$$
\|\mathbf1_U f\|_p\le\sum_{k=1}^m\|\mathbf1_{X_{j_k}}f\|_p.
$$

Compactness supplies such a finite subcover. This proves **(i)**, and also shows that each local seminorm for another cover is controlled by finitely many of the original ones. Since $$d_p$$ convergence is exactly convergence in every $$q_{j,p}$$, **(iv)** follows.

For **(ii)**, $$t\mapsto t/(1+t)$$ is increasing and subadditive, so $$d_p$$ satisfies the triangle inequality. It separates points because the $$X_j$$ cover $$X$$. If $$(f_k)$$ is $$d_p$$-Cauchy, then $$\mathbf1_{X_j}f_k$$ converges in $$L^p$$ to some $$g_j$$. The limits agree almost everywhere on overlaps. Patching the countably many representatives, after removing the union of the exceptional null sets, gives a measurable $$f$$ with $$\mathbf1_{X_j}f=g_j$$ almost everywhere. Thus $$f_k\to f$$ in every seminorm and hence in $$d_p$$.

For **(iii)**, restriction gives $$q_{j,p}(f)\le\|f\|_p$$, while finite measure and Hölder give

$$
q_{j,1}(f)\le\mu(X_j)^{1-1/p}q_{j,p}(f),
$$

with the usual interpretation for $$p=\infty$$. Both inclusions are continuous. To see density, choose an increasing relatively compact open exhaustion $$U_m$$. For $$f\in L^{p,\mathrm{loc}}$$, the functions $$\mathbf1_{U_m}f$$ belong to $$L^p$$ and eventually agree with $$f$$ on each fixed compact set of the exhaustion. For $$f\in L^{1,\mathrm{loc}}$$, the bounded functions $$\mathbf1_{U_m\cap\{\|f\|\le m\}}f$$ belong to every $$L^p$$ and converge to $$f$$ locally in $$L^1$$ by dominated convergence. This also proves density of $$L^{p,\mathrm{loc}}$$ in $$L^{1,\mathrm{loc}}$$.

### Exercise 4

**(i)** For $$0<\theta<1$$ and finite $$p,q,r$$, apply Hölder to $$\|f\|^{(1-\theta)r}\|f\|^{\theta r}$$, with exponents $$p/((1-\theta)r)$$ and $$q/(\theta r)$$. The exponents are conjugate and give

$$
\|f\|_r\le\|f\|_p^{1-\theta}\|f\|_q^\theta,
\qquad \frac1r=\frac{1-\theta}{p}+\frac\theta q.
$$

When an exponent is infinite, take the corresponding factor outside the integral as an essential supremum; the endpoint values of $$\theta$$ are immediate. If $$p=q=\infty$$, the inequality is equality.

**(ii)** The intersection is complete: a Cauchy sequence converges separately in $$L^p$$ and $$L^q$$, and the two limits agree almost everywhere, as can be checked on a countable finite-measure exhaustion using convergence in measure.

For the sum, the infimum defines a seminorm. To show it separates points, restrict to each finite-measure set $$A$$ in a sigma-finite exhaustion. Hölder implies

$$
\|\mathbf1_A f\|_1\le
\bigl(\mu(A)^{1-1/p}+\mu(A)^{1-1/q}\bigr)\|f\|_{L^p+L^q}.
$$

Thus zero sum seminorm implies $$f=0$$ on every such set. For completeness, take a sequence $$(f_n)$$ with $$\sum_n\|f_n\|_{L^p+L^q}<\infty$$ and choose decompositions $$f_n=g_n+h_n$$ whose cost is at most $$\|f_n\|_{L^p+L^q}+2^{-n}$$. The series $$\sum g_n$$ and $$\sum h_n$$ converge in their respective Banach spaces, so $$\sum f_n$$ converges in the sum norm. The standard summable-series criterion now proves completeness.

The first embedding follows from (i). For $$p\le r\le q$$, split $$f\in L^r$$ into $$g=f\mathbf1_{\{\|f\|>\|f\|_r\}}$$ and $$h=f-g$$ when $$\|f\|_r>0$$. For finite $$r$$, direct integration gives $$\|g\|_p\le\|f\|_r$$ and $$\|h\|_q\le\|f\|_r$$, including the endpoints $$q=\infty$$ and $$p=r$$. The cases $$r=\infty$$ or zero norm are immediate. Hence $$L^r\hookrightarrow L^p+L^q$$ continuously. Finally, the displayed local $$L^1$$ estimate proves the last embedding when $$X$$ and $$\mu$$ satisfy the local assumptions of Exercise 3; without those assumptions that last space has not been defined.

### Exercise 5

Let $$M=\|f\|_\infty$$. For $$q\ge p$$,

$$
\|f\|_q^q\le M^{q-p}\|f\|_p^p,
$$

so the upper limit is at most $$M$$. If $$M>0$$ and $$0<a<M$$, then $$A=\{\|f\|>a\}$$ has positive measure, and it has finite measure because $$f\in L^p$$. Thus $$\|f\|_q\ge a\mu(A)^{1/q}\to a$$. Let $$a\uparrow M$$. If $$M=0$$ the result is immediate.

### Exercise 6

Products are strongly measurable, and changing either representative on a null set changes the product only on a null set. Bilinearity is pointwise. For finite $$p$$, integration of $$\|\varphi f\|^p\le\|\varphi\|_\infty^p\|f\|^p$$ gives $$\|\varphi f\|_p\le\|\varphi\|_\infty\|f\|_p$$; for $$p=\infty$$ the same estimate follows from essential suprema. This bound gives joint continuity and bilinear operator norm at most 1.

### Exercise 7

Write $$h(t)=t/(1+t)$$ for $$t\ge0$$. It is increasing and subadditive: $$h(a+b)\le h(a)+h(b)$$. Thus the pointwise triangle inequality implies the triangle inequality for $$d_0$$; symmetry is immediate, and zero integral implies equality almost everywhere. The integral is finite since $$\mu(X)<\infty$$, proving **(i)**.

For **(ii)**, with $$A_j(\varepsilon)=\{\|f_j\|>\varepsilon\}$$,

$$
\frac{\varepsilon}{1+\varepsilon}\mu(A_j(\varepsilon))
\le d_0(f_j,0)
\le\varepsilon+\mu(A_j(\varepsilon)).
$$

The upper bound uses $$h(\|f_j\|)\le\varepsilon$$ on the complement. These inequalities give both implications, taking $$j\to\infty$$ and then $$\varepsilon\downarrow0$$ for the reverse implication.

### Exercise 8

**(i)–(ii)** Choose compact sets $$K_m$$ whose interiors cover $$X$$. Every compact support lies in some $$K_m$$. The continuous $$E$$-valued functions supported in $$K_m$$, with the uniform norm, embed isometrically in $$C(K_m,E)$$ by restriction. The latter is separable when $$E$$ is separable: finite covers by small-diameter sets, partitions of unity, and values from a countable dense subset of $$E$$ give a countable approximating family. A subspace of a separable metric space is separable, so each fixed-support space has a countable dense subset. Their union is dense in $$C_c(X,E)$$ in the uniform norm. This proves both scalar and vector cases.

**(iii)** For fixed $$K_m$$, uniform convergence of functions supported in $$K_m$$ implies $$L^p$$ convergence, since $$\mu(K_m)<\infty$$. The countable family just constructed is therefore $$L^p$$-dense in $$C_c(X,E)$$. Theorem 4.14 makes $$C_c$$ dense in $$L^p$$.

**(iv)** On $$[0,1]$$ with Lebesgue measure, the functions $$\mathbf1_{[0,t]}$$ for $$0<t<1$$ have pairwise $$L^\infty$$ distance 1. A separable metric space cannot contain an uncountable set with pairwise distances at least 1.

**(v)** On $$\mathbb R$$, the constant function 1 has distance at least 1 in $$L^\infty$$ from every book-simple function: its nonzero support has finite measure, so its complement has positive measure. Thus these simple functions need not be dense.

### Exercise 9

Fix $$\varepsilon>0$$ and an essentially bounded representative of $$f$$. A bounded subset of finite-dimensional $$E$$ has a finite $$\varepsilon$$-net. Partition the domain, outside a null set, into measurable sets according to a nearest point of this net, and assign that net point on each part. The resulting finite-valued measurable function $$s$$ satisfies $$\|f-s\|_\infty\le\varepsilon$$. Its nonzero support has finite measure because $$\mu(X)<\infty$$, so it is a simple function in the book's sense.

### Exercise 10

If representatives are changed on null sets, the assertion $$f\le g$$ almost everywhere is unchanged. Reflexivity and transitivity are immediate, and antisymmetry follows because $$f\le g$$ and $$g\le f$$ outside a common null set imply $$f=g$$ there. Addition preserves the order, as does multiplication by a nonnegative scalar.

The pointwise maximum and minimum of measurable representatives are measurable and are independent of representatives modulo null sets. They are respectively the least upper bound and greatest lower bound: for example, any common upper bound dominates both representatives outside a common null set, hence dominates their maximum there. Thus $$L^0(X,\mu,\mathbb R)$$ is a vector lattice, with $$|f|=f\vee(-f)$$.

### Exercise 11

**(i)** Counting measure has no nonempty null set. For finite $$p$$, its integral of $$|x_n|^p$$ is the sum of the series, by monotone convergence of finite partial sums; for $$p=\infty$$ the essential supremum is the ordinary supremum. This identifies the spaces and their norms.

**(ii)** For $$p<\infty$$, $$\|x\|_\infty\le\|x\|_p$$. If $$p\le q<\infty$$, then

$$
\sum_n|x_n|^q\le\|x\|_\infty^{q-p}\sum_n|x_n|^p
\le\|x\|_p^q.
$$

The case $$q=\infty$$ is the first inequality.

**(iii)** A convergent series $$\sum|x_n|^q$$ has terms tending to zero, so $$\ell^q\subset c_0$$. The inclusions are continuous by (ii). Finitely supported sequences are dense in each finite $$\ell^q$$ by truncation, and in $$c_0$$ in the supremum norm. This proves both dense embeddings; $$c_0\hookrightarrow\ell^\infty$$ is isometric.

### Exercise 12

Assume $$E\ne\{0\}$$; otherwise all inclusions are trivial. For **(i)** the constant unit-vector function belongs to $$L^\infty$$, hence to $$L^1$$ by hypothesis. Thus $$\mu(X)<\infty$$. Hölder gives $$\|f\|_p\le\mu(X)^{1/p-1/q}\|f\|_q$$, with the usual endpoint conventions.

For **(ii)**, the inclusion $$L^1\to L^\infty$$ has closed graph: convergence in either norm has a subsequence converging almost everywhere to its limit. By the closed graph theorem there is $$C$$ with $$\|f\|_\infty\le C\|f\|_1$$. Applied to unit-vector indicators, this says that every measurable set of finite positive measure has measure at least $$1/C$$. Sigma-finiteness extends the same lower bound to every positive-measure measurable set. For $$f\in L^p$$ and $$p<\infty$$, if $$A_t=\{\|f\|>t\}$$ has positive measure, then

$$
t^p/C\le t^p\mu(A_t)\le\|f\|_p^p.
$$

Consequently $$\|f\|_\infty\le C^{1/p}\|f\|_p$$. Interpolation between $$L^p$$ and $$L^\infty$$ now gives the inclusion into every $$L^q$$ with $$q\ge p$$; $$p=\infty$$ is immediate.

**(iii)** A finite interval with completed Lebesgue measure realizes the first inclusion. Counting measure on $$\mathbb N$$ is complete and sigma-finite and realizes the second, since $$\ell^1\hookrightarrow\ell^\infty$$.

### Exercise 13

Let $$0<p<1$$. **(i)** For $$a,b\ge0$$, concavity gives $$(a+b)^p\le a^p+b^p$$; apply this to the pointwise triangle inequality and integrate. **(ii)** Conversely, concavity gives $$a^p+b^p\le2^{1-p}(a+b)^p$$. Together with (i) this yields

$$
\|f+g\|_p\le(\|f\|_p^p+\|g\|_p^p)^{1/p}
\le2^{1/p-1}(\|f\|_p+\|g\|_p).
$$

**(iii)–(v)** The first inequality and homogeneity show closure under linear combinations. A nonnegative measurable function has zero integral exactly when it vanishes almost everywhere, giving the characterization of $$N$$. The quantity $$\rho([f],[g])=\int\|f-g\|^p\,d\mu$$ is representative-independent, separates classes, and satisfies the triangle inequality by (i).

**(vi)** From a $$\rho$$-Cauchy sequence choose a subsequence with $$\sum_k\rho(f_{k+1},f_k)<\infty$$. Monotone convergence makes $$\sum_k\|f_{k+1}-f_k\|^p$$ finite almost everywhere. At such points the difference series converges absolutely in $$E$$: eventually all its terms are at most 1, and then $$a\le a^p$$. Let $$f$$ be its pointwise limit, setting it to zero on the exceptional set. It is strongly measurable, and Fatou's lemma gives

$$
\rho(f,f_k)\le\sum_{j\ge k}\rho(f_{j+1},f_j)\longrightarrow0.
$$

In particular $$f\in L^p$$, and the original Cauchy sequence converges to it.

**(vii)** If $$A=\|f\|_p$$ and $$B=\|g\|_p$$ are positive, concavity of $$t^p$$ gives pointwise

$$
\left(\frac{f+g}{A+B}\right)^p
\ge\frac{A}{A+B}\left(\frac fA\right)^p+
\frac{B}{A+B}\left(\frac gB\right)^p.
$$

Integrating yields $$\|f+g\|_p\ge A+B$$. The zero cases are immediate.

**(viii)** The asserted failure of the norm property is general rather than universal: on a one-point measure space the expression is a norm. On two points of counting measure, take the two coordinate indicators. Each has $$p$$-quantity 1, while their sum has quantity $$2^{1/p}>2$$, violating the triangle inequality.

### Exercise 14

Put $$1/r=\sum_j1/p_j$$, allowing $$r<1$$ and using $$1/\infty=0$$. If all $$p_j=\infty$$, the essential supremum estimate proves the result. Otherwise $$r<\infty$$. Pull out the factors with $$p_j=\infty$$. For the remaining factors, generalized Hölder applied to $$|f_j|^r$$ with conjugate exponents $$p_j/r$$ gives

$$
\int\prod_j|f_j|^r\,d\mu
\le\prod_j\left(\int|f_j|^{p_j}\,d\mu\right)^{r/p_j}.
$$

An exponent equal to 1 is allowed; the other finite factors then cannot occur. Taking the $$r$$th root gives the claimed inequality, including factors with infinite exponent. Measurability follows from continuity of multiplication.

### Exercise 15

A compactly supported continuous function on a metric space is uniformly continuous: use uniform continuity on its compact support and a finite-neighborhood argument for pairs with one point outside it. It also vanishes at infinity. A uniform limit of functions vanishing at infinity has the same property: choose an approximant within $$\varepsilon/2$$ and use its compact set. Thus the closure of $$C_c$$ in $$BUC$$ lies in $$C_0$$.

Conversely, suppose $$f\in C_0$$. Given $$\varepsilon>0$$, choose compact $$K$$ with $$\|f\|<\varepsilon$$ outside $$K$$. The function $$f_\varepsilon(x)=(1-\varepsilon/\|f(x)\|)_+f(x)$$, defined as zero when $$f(x)=0$$, is continuous, satisfies $$\|f-f_\varepsilon\|\le\varepsilon$$, and has support contained in the compact set $$\{\|f\|\ge\varepsilon\}\subset K$$. Hence $$f_\varepsilon\in C_c$$. In particular the uniform approximation also establishes that every member of $$C_0$$ is uniformly continuous.

### Exercise 16

Use the convention $$\inf\varnothing=\infty$$. Let $$\lambda(t)=\mu\{\|f\|>t\}$$. It is decreasing and right-continuous, because $$\{\|f\|>t+1/n\}\uparrow\{\|f\|>t\}$$. Its generalized inverse $$f^*(u)=\inf\{s\ge0:\lambda(s)\le u\}$$ is decreasing. To prove its right continuity, let $$u_n\downarrow u$$ and $$a=\lim f^*(u_n)\le f^*(u)$$. If $$a<f^*(u)$$, choose $$a<b<c<f^*(u)$$. Eventually $$f^*(u_n)<b$$, which implies $$\lambda(c)\le u_n$$. Hence $$\lambda(c)\le u$$, contradicting $$c<f^*(u)$$. The same argument works if $$f^*(u)=\infty$$. Monotone functions are Borel measurable, proving **(i)**.

**(ii)** Inclusion of level sets gives $$\lambda_f\le\lambda_g$$, and the corresponding admissible sets in the inverse definition give $$f^*\le g^*$$.

**(iii)** Increasing level sets give $$\lambda_{f_j}(s)\uparrow\lambda_f(s)$$. Therefore $$f_j^*\uparrow h\le f^*$$. If $$h(u)<a<b<f^*(u)$$, then $$f_j^*(u)<a$$ for every $$j$$, so $$\lambda_{f_j}(b)\le u$$ for every $$j$$. Passing to the limit contradicts $$b<f^*(u)$$. Thus $$h=f^*$$, including infinite values.

For **(vi)**, for every $$s\ge0$$ and $$u\ge0$$,

$$
f^*(u)>s\quad\Longleftrightarrow\quad
\text{there exists }v>s\text{ with }\lambda(v)>u.
$$

The forward implication follows by choosing $$v$$ between $$s$$ and $$f^*(u)$$; for the reverse, monotonicity gives $$\lambda(t)>u$$ for every $$t\le v$$. Right continuity of $$\lambda$$ then shows that the set of such $$u$$ is $$[0,\lambda(s))$$, up to the irrelevant endpoint, even when its length is infinite. Hence $$\lambda_{f^*}(s)=\lambda_f(s)$$.

**(iv)** The layer-cake identity $$a^p=\int_0^\infty p t^{p-1}\mathbf1_{\{a>t\}}\,dt$$ and Tonelli's theorem give

$$
\int_X\|f\|^p\,d\mu=\int_0^\infty p t^{p-1}\lambda_f(t)\,dt
=\int_0^\infty(f^*(u))^p\,du,
$$

where the second equality applies the same identity to $$f^*$$ and uses (vi). All quantities may be infinite. Finally, **(v)** follows directly from $$f^*(0)=\inf\{s\ge0:\mu(\|f\|>s)=0\}$$, the definition of the essential supremum.

### Exercise 17

At level $$j$$ there are finitely many dyadic intervals, each of length $$2^{-j}$$. Therefore any enumeration of all of them has levels tending to infinity, and $$\|f_n\|_p=|J_n|^{1/p}\to0$$ for $$p<\infty$$. Every $$x\in[0,1]$$ belongs to at least one interval at every sufficiently fine level and also lies outside at least one interval at every sufficiently fine level. Thus the indicator sequence takes both 1 and 0 infinitely often at each point and cannot converge there.

### Exercise 18

Write $$p'$$ for the conjugate exponent and use the scalar pairing $$\int f\varphi$$. **(i)** If $$h\in L^p$$ has zero pairing with every $$\varphi\in L^{p'}$$, take $$\varphi=\overline h|h|^{p-2}$$ for $$1<p<\infty$$, with value zero at $$h=0$$. Then $$\varphi\in L^{p'}$$ and the pairing is $$\|h\|_p^p$$. For $$p=1$$ use the bounded phase $$\overline h/|h|$$ on $$\{h\ne0\}$$. Thus $$h=0$$ and weak limits are unique.

**(ii)** Hölder gives $$|\int(f_k-f)\varphi|\le\|f_k-f\|_p\|\varphi\|_{p'}\to0$$.

**(iii)** Let $$A_m$$ be an increasing finite-measure exhaustion and define $$B_N=\{\sup_k|f_k|\le N,\ |g|\le N\}$$. Almost-everywhere convergence to the finite-valued $$g$$ implies $$B_N\uparrow X$$ up to a null set. For any bounded measurable $$\varphi$$ supported in $$A_m\cap B_N$$, dominated convergence gives $$\int f_k\varphi\to\int g\varphi$$; such a test belongs to $$L^{p'}$$, including $$p'=\infty$$. Weak convergence also gives the limit $$\int f\varphi$$. Taking bounded phase tests on $$A_m\cap B_N$$ shows $$f=g$$ there. The countable union proves equality almost everywhere.

**(iv)** The Hilbert-space identity gives

$$
\|f_k-f\|_2^2=\|f_k\|_2^2+\|f\|_2^2-2\operatorname{Re}\int f_k\overline f.
$$

Weak convergence makes the last integral tend to $$\|f\|_2^2$$, and the norm hypothesis makes the right side tend to zero.

**(v)** The functions $$e_k$$ form an orthonormal sequence. Bessel's inequality says $$\sum_k|\langle\varphi,e_k\rangle|^2\le\|\varphi\|_2^2$$ for every $$\varphi\in L^2(0,2\pi)$$, so the coefficients tend to zero and $$e_k\rightharpoonup0$$. Yet $$\|e_k\|_2=1$$ for all $$k$$, so they do not converge to zero in norm. By uniqueness of the weak limit, they cannot converge in norm to any other function either.
