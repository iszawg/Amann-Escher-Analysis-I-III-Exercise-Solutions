# Chapter X — Integration Theory

## 7. The convolution

These solutions address Exercises 1–15. Unless otherwise indicated, functions are scalar-valued on $$\mathbb R^n$$, integrals use Lebesgue measure, and $$\tau_a f(x)=f(x-a)$$. Equalities between $$L^p$$ functions are understood almost everywhere. For a pair merely in $$L^0$$, the book defines its convolution only when the defining integral is absolutely convergent for almost every output point. Exercises 5, 8, and 12 need corrections to their printed hypotheses; the derivative interpretation in Exercise 10 also matters.

### Exercise 1

Let $$b=\mathbf1_{[-a,a]}$$. The intersection of $$[-a,a]$$ and $$[x-a,x+a]$$ has length $$(2a-|x|)_+$$, where $$t_+=\max(t,0)$$. Consequently

$$
(b*b)(x)=(2a-|x|)_+.
$$

For a third factor, integrate the triangular function over $$[x-a,x+a]$$. Equivalently, twice integrate its piecewise constant second derivative, or evaluate the elementary integrals on the intervals cut out by $$-3a,-a,a,3a$$. This gives

$$
(b*b*b)(x)=\frac12\bigl((3a-|x|)_+^2-3(a-|x|)_+^2\bigr)
=\begin{cases}
3a^2-x^2,&|x|\le a,\\
\frac12(3a-|x|)^2,&a\le|x|\le3a,\\
0,&|x|\ge3a.
\end{cases}
$$

For example, on $$0\le x\le a$$ the integral is $$\int_{x-a}^0(2a+t)\,dt+\int_0^{x+a}(2a-t)\,dt=3a^2-x^2$$; on $$a\le x\le3a$$ the remaining interval gives the second expression. Evenness supplies the negative side.

### Exercise 2

Let $$1<p<\infty$$ and $$1/p+1/p'=1$$. Hölder's inequality, translation and reflection invariance give, for every $$x$$,

$$
\int|f(x-y)g(y)|\,dy\le\|f\|_p\|g\|_{p'},\qquad
|f*g(x)|\le\|f\|_p\|g\|_{p'}.
$$

Thus the integral is defined at every point and does not depend on the chosen representatives. For continuity, the change of variables in the convolution and Hölder yield

$$
|(f*g)(x+h)-(f*g)(x)|\le\|f\|_p\,\|\tau_hg-g\|_{p'}\longrightarrow0
$$

uniformly in $$x$$, by continuity of translations in $$L^{p'}$$. To show vanishing at infinity, choose compactly supported continuous $$f_j\to f$$ in $$L^p$$ and $$g_j\to g$$ in $$L^{p'}$$. Each $$f_j*g_j$$ has compact support, and

$$
\|f*g-f_j*g_j\|_\infty\le
\|f-f_j\|_p\|g\|_{p'}+\|f_j\|_p\|g-g_j\|_{p'}\longrightarrow0.
$$

Hence $$f*g\in C_0$$. Linearity of the integral gives bilinearity, and the displayed norm bound proves joint continuity, completing both (a) and (b).

### Exercise 3

Suppose $$1/p+1/q=1+1/r$$, with reciprocals of infinity interpreted as zero. If $$r=1$$ then $$p=q=1$$, and Tonelli gives

$$
\int\!\int |f(x-y)g(y)|\,dy\,dx=\|f\|_1\|g\|_1.
$$

This proves existence almost everywhere and the inequality. If $$r=\infty$$, the exponents are conjugate: Hölder gives the bound for every $$x$$, including the endpoint pairs $$(1,\infty)$$ and $$(\infty,1)$$. For strictly interior conjugate exponents, Exercise 2 additionally gives a $$C_0$$ representative.

Now let $$1<r<\infty$$. The exponent relation implies $$p,q\le r$$ and $$p,q<\infty$$. For fixed $$x$$ apply Hölder to

$$
|f(x-y)g(y)|=
\bigl(|f(x-y)|^p|g(y)|^q\bigr)^{1/r}
|f(x-y)|^{1-p/r}|g(y)|^{1-q/r}.
$$

The three reciprocal Hölder exponents are $$1/r$$, $$1/p-1/r$$ and $$1/q-1/r$$; a zero reciprocal means that the corresponding factor is 1. Therefore

$$
\int |f(x-y)g(y)|\,dy\le
\left(\int |f(x-y)|^p|g(y)|^q\,dy\right)^{1/r}
\|f\|_p^{1-p/r}\|g\|_q^{1-q/r}.
$$

Tonelli shows that the integral inside the parentheses is finite for almost every $$x$$ and has integral $$\|f\|_p^p\|g\|_q^q$$ over $$x$$. Raising the inequality to the power $$r$$ and integrating gives

$$
\|f*g\|_r\le\|f\|_p\|g\|_q.
$$

Thus the convolution exists almost everywhere in all cases. Tonelli also ensures that null-set changes of either input do not change its equivalence class. Bilinearity and the norm bound imply that $$L^p\times L^q\to L^r$$ is jointly continuous.

### Exercise 4

Put $$K=\operatorname{supp}f$$. For every $$x$$ the integral $$\int f(x-y)g(y)\,dy$$ is absolutely convergent because its integrand is supported in the compact set $$x-K$$ and $$g$$ is locally integrable. If $$x$$ ranges over a compact set $$H$$, all relevant $$y$$ lie in the compact set $$H-K$$. The derivatives of $$f$$ up to order $$k$$ are bounded, so dominated convergence and differentiation under the integral give, for $$|\alpha|\le k$$,

$$
\partial^\alpha(f*g)(x)=\int(\partial^\alpha f)(x-y)g(y)\,dy.
$$

The same domination proves continuity of each derivative. Hence $$f*g\in C^k$$.

### Exercise 5

**The assertion as printed is not valid for arbitrary $$f\in L^1_{\mathrm{loc}}$$ and $$\varphi\in BC^\infty$$:** even the convolutions may fail to exist. For example, take $$f=1$$ and $$\varphi=1$$; all derivatives of $$f$$ of positive order vanish, but $$f*\varphi$$ is infinite at every point.

A standard corrected version assumes $$f,\partial^\alpha f\in L^1_{\mathrm{loc}}$$ with $$\partial^\alpha f$$ understood as a weak derivative and takes $$\varphi\in C_c^\infty$$. Then Exercise 4 gives smooth convolutions, and for each $$x$$, applying the weak-derivative identity to $$y\mapsto\varphi(x-y)$$ yields

$$
((\partial^\alpha f)*\varphi)(x)
=(-1)^{|\alpha|}\int f(y)\,\partial_y^\alpha\varphi(x-y)\,dy
=\int f(y)(\partial^\alpha\varphi)(x-y)\,dy
=\partial^\alpha(f*\varphi)(x).
$$

Another sufficient set of hypotheses is $$f,\partial^\alpha f\in L^1$$ in the weak sense and $$\varphi\in BC^\infty$$. All three convolutions then exist; integration by parts with a cutoff, as in Exercise 10, proves the same identities. Existence of a classical derivative almost everywhere alone must not be confused with existence of the corresponding weak derivative.

### Exercise 6

In $$\operatorname{Funct}(\mathbb R,\mathbb K)$$ take the one-dimensional subspace $$V=\operatorname{span}\{x\mapsto x\}$$. For $$a\ne0$$, the translate of its generator is $$x\mapsto x-a$$, which is not in $$V$$. Hence translations do not restrict to maps $$V\to V$$ and cannot give the stated representation on this subspace. More generally, with any $$n\ge1$$ use $$\operatorname{span}\{x\mapsto x_1\}$$ and a translation with nonzero first coordinate. This interprets the exercise in the context of the translation action: taken literally as a claim about all possible representations, it is false, since the trivial representation exists on every vector space.

### Exercise 7

Let $$1\le p<\infty$$ and $$\varepsilon>0$$. Compactness supplies a finite $$\varepsilon/3$$-net $$f_1,\ldots,f_N$$ in $$K$$. Strong continuity of translations gives a common $$\delta>0$$ such that $$\|\tau_a f_j-f_j\|_p<\varepsilon/3$$ whenever $$|a|<\delta$$ and $$1\le j\le N$$. For any $$f\in K$$ choose $$j$$ with $$\|f-f_j\|_p<\varepsilon/3$$. Since translations are isometries,

$$
\|\tau_a f-f\|_p\le
\|\tau_a(f-f_j)\|_p+\|\tau_a f_j-f_j\|_p+\|f_j-f\|_p<\varepsilon.
$$

### Exercise 8

**The statement is false as printed.** Define

$$
I=\left\{f\in L^1(\mathbb R^n):\int f(x)\,dx=0\right\}.
$$

The integral is a continuous linear functional, so $$I$$ is closed. It is proper because a nonzero nonnegative compactly supported function has positive integral, and it is nonzero: the difference of two distinct translates of such a function belongs to $$I$$. Fubini gives

$$
\int(f*g)=\left(\int f\right)\left(\int g\right),
\qquad f,g\in L^1.
$$

Thus $$I$$ is a nonzero proper closed ideal of $$(L^1,*)$$, and cannot be dense. In contrast, an ideal containing an approximate identity is dense: if $$\varphi_\varepsilon\in I$$ approximates the identity, then $$\varphi_\varepsilon*f\in I$$ and converges to $$f$$ in $$L^1$$ for every $$f\in L^1$$.

### Exercise 9

Let $$k(x)=(4\pi)^{-n/2}e^{-|x|^2/4}$$. By induction, $$\partial^\alpha k=P_\alpha k$$ for a polynomial $$P_\alpha$$. A polynomial times a Gaussian is bounded and integrable to every finite positive power, so $$\partial^\alpha k\in L^p$$ for every $$1\le p\le\infty$$; its first derivatives also have this property.

Given $$u\in L^p$$, let $$p'$$ be its conjugate exponent, including endpoints. Hölder gives a well-defined bounded convolution $$u*\partial^\alpha k$$ with norm at most $$\|u\|_p\|\partial^\alpha k\|_{p'}$$. The Gaussian and all its derivatives are in $$W^{1,p'}$$, including $$W^{1,\infty}$$. Their difference quotients converge in $$L^{p'}$$ when $$p'<\infty$$, and uniformly when $$p'=\infty$$ (their next derivatives are uniformly continuous). Applying Hölder to the difference quotients inductively yields

$$
\partial^\alpha(k*u)=(\partial^\alpha k)*u,\qquad
\|\partial^\alpha(k*u)\|_\infty\le\|\partial^\alpha k\|_{p'}\|u\|_p.
$$

Each resulting derivative is uniformly continuous: use translation continuity of $$\partial^\alpha k$$ in $$L^{p'}$$ for finite $$p'$$, or its bounded gradient for $$p'=\infty$$. Therefore $$k*u\in BUC^\infty$$.

### Exercise 10

With $$\partial^\alpha f$$ interpreted as a weak derivative in $$L^1$$, the result extends the defining integration-by-parts identity from compactly supported tests to $$\varphi\in BC^\infty$$. Choose $$\chi\in C_c^\infty$$ equal to 1 near the origin and set $$\chi_R(x)=\chi(x/R)$$. Then

$$
\int(\partial^\alpha f)\chi_R\varphi
=(-1)^{|\alpha|}\int f\,\partial^\alpha(\chi_R\varphi).
$$

The left side tends to $$\int(\partial^\alpha f)\varphi$$ by dominated convergence. In the Leibniz expansion on the right, the term without a derivative of $$\chi_R$$ tends to $$\int f\,\partial^\alpha\varphi$$. Every other term tends to zero, since $$\|\partial^\beta\chi_R\|_\infty=O(R^{-|\beta|})$$ for $$|\beta|>0$$, the relevant derivatives of $$\varphi$$ are bounded, and $$f\in L^1$$. This proves

$$
\int(\partial^\alpha f)\varphi=(-1)^{|\alpha|}\int f\,\partial^\alpha\varphi.
$$

The proof also applies when the classical derivatives are sufficiently regular to justify the compactly supported integration by parts. If $$\partial^\alpha f$$ means only a classical derivative defined almost everywhere, the weak-derivative identity is an additional requirement; for example, a compactly supported continuous function built from the Cantor function has an almost-everywhere classical derivative in $$L^1$$ but also a nonzero singular distributional derivative.

### Exercise 11

On each listed space $$V$$, translations are linear automorphisms, $$\tau_a\tau_b=\tau_{a+b}$$, and $$\tau_a^{-1}=\tau_{-a}$$. Thus $$a\mapsto\tau_a$$ is a group homomorphism onto the translation group $$T_V$$ by definition. To show injectivity, fix $$a\ne0$$ and choose a nonzero continuous bump $$\psi$$ supported in a ball of radius less than $$|a|/3$$. It belongs to every listed space, and its support is disjoint from that of $$\tau_a\psi$$. Hence $$\tau_a\psi\ne\psi$$, both pointwise and as an $$L^p$$ equivalence class. The kernel is zero, so $$\mathbb R^n\cong T_V$$.

### Exercise 12

**The stated assumptions do not suffice for associativity.** The obstruction is that existence of the four pairwise convolutions does not imply absolute integrability of the triple integrand. Here is an explicit counterexample in one dimension.

Choose a nonnegative, nonzero $$\psi\in C_c^\infty((0,1))$$ and let $$c=\log2$$. Set

$$
f(x)=e^{cx}\mathbf1_{[0,\infty)}(x),\qquad
h(x)=e^{cx},\qquad g(x)=\psi(x)-2\psi(x-1).
$$

Put $$q(y)=e^{-cy}g(y)$$ and $$Q(x)=\int_{-\infty}^xq(y)\,dy$$. Since the two terms of $$q$$ are equal and opposite after a unit translation, $$\int q=0$$. The first term is supported in $$(0,1)$$ and the second in $$(1,2)$$; thus $$Q$$ is nonnegative, nonzero, and supported in $$[0,2]$$. Direct calculation gives, for every $$x$$,

$$
(g*h)(x)=e^{cx}\int q(y)\,dy=0,\qquad
(f*g)(x)=e^{cx}Q(x).
$$

All these integrals are absolutely convergent because $$g$$ is compactly supported. The first iterated convolution is also absolutely convergent, since $$f*g$$ is compactly supported; the second is the convolution with the zero function. But

$$
((f*g)*h)(x)=e^{cx}\int Q(y)\,dy>0,
\qquad (f*(g*h))(x)=0.
$$

A sufficient extra assumption is that, for almost every $$x$$,

$$
\int\!\int |f(x-y-z)g(y)h(z)|\,dy\,dz<\infty.
$$

Fubini and a change of variables then identify both iterated convolutions with the same double integral. In particular, for $$f,g,h\in L^1$$, Tonelli shows that the integral of this nonnegative triple expression over $$x,y,z$$ is $$\|f\|_1\|g\|_1\|h\|_1<\infty$$. Hence the sufficient condition holds almost everywhere, and convolution is associative on $$L^1$$.

### Exercise 13

For a distribution $$T$$ define

$$
\langle\partial^\alpha T,\varphi\rangle
=(-1)^{|\alpha|}\langle T,\partial^\alpha\varphi\rangle,
\qquad\varphi\in\mathcal D(X).
$$

The map is linear in $$\varphi$$. If $$\varphi_j\to0$$ in the test-function sense, their supports lie in a common compact subset of $$X$$ and all derivatives converge uniformly to zero there. The same is true of $$\partial^\alpha\varphi_j$$. Continuity of $$T$$ therefore gives $$\langle\partial^\alpha T,\varphi_j\rangle\to0$$. Thus $$\partial^\alpha T$$ is a distribution. Linearity in $$T$$ follows immediately from the definition, so the derivative is a well-defined linear map on $$\mathcal D'(X)$$.

### Exercise 14

Let $$u\in W_p^m(X)$$ and $$f\in BC^m(X)$$. For every multi-index $$|\alpha|\le m$$, the weak Leibniz rule gives

$$
\partial^\alpha(fu)=\sum_{\beta\le\alpha}
\binom{\alpha}{\beta}(\partial^\beta f)(\partial^{\alpha-\beta}u).
$$

For completeness, prove this locally by approximating $$f$$ on the support of each test function by smooth functions together with their derivatives through order $$m$$; the formula for smooth multipliers follows from the distributional product rule, and the limit follows by local integrability. Each term on the right belongs to $$L^p$$ because the derivative of $$f$$ is bounded. Consequently, with a constant depending only on $$m,n$$ and the chosen equivalent Sobolev norm,

$$
\|fu\|_{W_p^m}\le C_{m,n}\|f\|_{BC^m}\|u\|_{W_p^m}.
$$

The same estimate holds for $$p=\infty$$. For fixed $$u$$, multiplication is linear in $$f$$ and bounded, hence belongs to $$\mathcal L(BC^m(X),W_p^m(X))$$.

### Exercise 15

Write $$\varphi_\varepsilon(x)=\varepsilon^{-n}\varphi(x/\varepsilon)$$ with $$\varphi\in L^1$$ and $$\int\varphi=1$$, as in the book's definition. For every test function $$\psi\in\mathcal D(\mathbb R^n)$$, a change of variables gives

$$
\langle\varphi_\varepsilon,\psi\rangle
=\int\varphi(y)\psi(\varepsilon y)\,dy.
$$

As $$\varepsilon\to0^+$$, the integrand converges pointwise to $$\varphi(y)\psi(0)$$ and is dominated by $$|\varphi(y)|\|\psi\|_\infty$$. Dominated convergence gives

$$
\langle\varphi_{\varepsilon_j},\psi\rangle\longrightarrow
\psi(0)\int\varphi=\psi(0)=\langle\delta,\psi\rangle.
$$

Thus $$\varphi_{\varepsilon_j}\to\delta$$ in the distributional sense defined in the exercise.
