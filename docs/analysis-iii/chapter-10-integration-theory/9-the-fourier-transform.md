# Chapter X — Integration Theory

## 9. The Fourier transform

These solutions address Exercises 1–13. We use the book's unitary normalization

$$
\widehat f(\xi)=(2\pi)^{-n/2}\int_{\mathbb R^n}e^{-ix\cdot\xi}f(x)\,dx,
\qquad \Lambda(\xi)=(1+|\xi|^2)^{1/2}.
$$

The inverse transform uses the plus sign and the same factor. For $$L^2$$ functions, the transform is the Plancherel extension, and equalities hold almost everywhere. We use $$\mathcal D=C_c^\infty$$ and $$\mathcal S$$ for Schwartz space. Several printed assertions need correction: Exercises 2, 5–7, 8(iv), and 9 are discussed individually below.

### Exercise 1

For $$a>0$$, with continuous values assigned at removable singularities, the transforms are

$$
\begin{aligned}
\text{(i)}\quad &\mathcal F\left(\frac{\sin ax}{x}\right)(\xi)
=\sqrt{\frac\pi2}\,\mathbf1_{[-a,a]}(\xi)\quad\text{in }L^2,\\
\text{(ii)}\quad &\mathcal F\left(\frac1{a^2+x^2}\right)(\xi)
=\frac1a\sqrt{\frac\pi2}\,e^{-a|\xi|},\\
\text{(iii)}\quad &\mathcal F(e^{-a|x|})(\xi)
=\sqrt{\frac2\pi}\,\frac a{a^2+\xi^2},\\
\text{(iv)}\quad &\mathcal F\left(\left(1-\frac{|x|}a\right)\mathbf1_{[-a,a]}(x)\right)(\xi)
=\sqrt{\frac2\pi}\,\frac{1-\cos(a\xi)}{a\xi^2},\\
\text{(v)}\quad &\mathcal F\left[\left(\frac{\sin ax}{x}\right)^2\right](\xi)
=\frac12\sqrt{\frac\pi2}\,(2a-|\xi|)_+.
\end{aligned}
$$

In (iv) the value at zero is $$a/\sqrt{2\pi}$$. In (v), the square is applied to the function before taking its transform.

For (i), direct integration gives $$\widehat{\mathbf1_{[-a,a]}}(x)=\sqrt{2/\pi}\,\sin(ax)/x$$. Applying $$\mathcal F^2h=h(-\cdot)$$ in $$L^2$$ proves the formula. The sinc function is not in $$L^1$$, so its transform here is the $$L^2$$ transform, not an absolutely convergent Lebesgue integral. A symmetric improper integral gives half the indicated interior value at $$\xi=\pm a$$; these endpoint values do not affect the $$L^2$$ result.

For (iii), splitting at zero gives

$$
\widehat{e^{-a|x|}}(\xi)=\frac1{\sqrt{2\pi}}
\left(\frac1{a+i\xi}+\frac1{a-i\xi}\right).
$$

This is the displayed expression. Apply $$\mathcal F^2h=h(-\cdot)$$ to it to obtain (ii). For (iv), integrate twice or use the convolution of two interval indicators; explicitly

$$
\frac2{\sqrt{2\pi}}\int_0^a\left(1-\frac xa\right)\cos(\xi x)\,dx
=\sqrt{\frac2\pi}\frac{1-\cos(a\xi)}{a\xi^2}.
$$

For (v), the sinc function belongs to $$L^2$$, so its square belongs to $$L^1$$. The product formula, justified by $$L^2$$ approximation and Cauchy–Schwarz, gives

$$
\mathcal F(h^2)=(2\pi)^{-1/2}\widehat h*\widehat h,
\qquad h(x)=\frac{\sin ax}{x}.
$$

The convolution of the two interval indicators is $$(2a-|\xi|)_+$$, yielding the stated constant.

### Exercise 2

**The printed claim $$f*g=0$$ is false.** By Exercise 1(v), if $$c=\tfrac12\sqrt{\pi/2}$$ then

$$
\widehat f(\xi)=c(2-|\xi|)_+,
\qquad \widehat g(\xi)=\widehat f(\xi-2)=c(2-|\xi-2|)_+.
$$

The first support is $$[-2,2]$$ and the second is $$[0,4]$$; their product is strictly positive on $$(0,2)$$. The convolution theorem therefore gives

$$
\widehat{f*g}(\xi)=\sqrt{2\pi}\,c^2(2-|\xi|)_+(2-|\xi-2|)_+, 
$$

which is nonzero, and injectivity of the transform shows $$f*g\ne0$$. In fact, Fourier inversion gives $$(f*g)(0)=c^2\int_0^2\xi(2-\xi)\,d\xi=\pi/6$$. A corrected version replaces $$e^{2ix}$$ by $$e^{ibx}$$ with $$|b|\ge4$$. Then the two Fourier supports have disjoint interiors, their product vanishes everywhere, and the convolution is zero.

### Exercise 3

For $$f\in L^1(\mathbb R^n)$$, the convolution theorem gives $$\widehat{f*f}=(2\pi)^{n/2}\widehat f^{,2}$$. If $$f*f=0$$, the transform vanishes, so $$\widehat f=0$$ and injectivity gives $$f=0$$.

If $$f*f=f$$, then for every $$\xi$$,

$$
\widehat f(\xi)\bigl((2\pi)^{n/2}\widehat f(\xi)-1\bigr)=0.
$$

The continuous function $$\widehat f$$ thus takes values only in the two-point set $$\{0,(2\pi)^{-n/2}\}$$. Since $$\mathbb R^n$$ is connected, it is constant. The Riemann–Lebesgue theorem says it tends to zero at infinity, so the constant is zero and $$f=0$$.

### Exercise 4

Write $$\varphi_\varepsilon(x)=\varepsilon^{-n}\varphi(x/\varepsilon)$$ with $$\varphi\in L^1$$ and $$\int\varphi=1$$. A change of variables yields

$$
\widehat{\varphi_\varepsilon}(\xi)
=(2\pi)^{-n/2}\int e^{-i\varepsilon y\cdot\xi}\varphi(y)\,dy
\longrightarrow(2\pi)^{-n/2}
$$

for every $$\xi$$, by dominated convergence. Moreover the transforms are uniformly bounded by $$(2\pi)^{-n/2}\|\varphi\|_1$$. For each test function $$\psi\in\mathcal D(\mathbb R^n)$$, dominated convergence applied to the product with $$\psi$$ gives

$$
\langle\widehat{\varphi_{\varepsilon_j}},\psi\rangle
\longrightarrow(2\pi)^{-n/2}\int\psi(\xi)\,d\xi
=\langle(2\pi)^{-n/2}\mathbf1,\psi\rangle.
$$

This is precisely convergence in $$\mathcal D'$$ as defined in the book.

### Exercise 5

The stated identity needs both a normalization factor and reflection. Let $$\check a=\mathcal F^{-1}a=\widehat a(-\cdot)$$. For $$a,f\in\mathcal S$$, the correct formula is

$$
a(D)f=\mathcal F^{-1}(a\widehat f)
=(2\pi)^{-n/2}\,\check a*f.
$$

Indeed, $$\widehat{\check a}=a$$, and the convolution theorem gives

$$
\mathcal F\bigl((2\pi)^{-n/2}\check a*f\bigr)=a\widehat f.
$$

Applying the inverse transform proves the identity. The printed right side $$\widehat a*f$$ instead has Fourier transform $$(2\pi)^{n/2}a(-\xi)\widehat f(\xi)$$, which is generally different. For example, choose $$a(\xi)=e^{-|\xi|^2/2}$$ and any nonzero $$f\in\mathcal S$$: reflection causes no change for this even $$a$$, but the missing factor still makes the printed identity false.

### Exercise 6

There is a mismatch in the printed inner product. The set is

$$
H^s=\{u\in L^2:\Lambda^s\widehat u\in L^2\},
$$

but the printed pairing is $$\langle\Lambda^s\widehat u,\widehat v\rangle_2$$. Its norm is $$\|\Lambda^{s/2}\widehat u\|_2$$, under which this set is generally **not complete** for $$s>0$$.

To see this, take $$0<\varepsilon<s/2$$ and define $$\widehat u(\xi)=\Lambda(\xi)^{-s/2-n/2-\varepsilon}$$. Then $$\Lambda^{s/2}\widehat u\in L^2$$ but $$\Lambda^s\widehat u\notin L^2$$. The truncated transforms $$\mathbf1_{|\xi|\le R}\widehat u$$ define elements of $$H^s$$ and form a Cauchy sequence in the printed norm. Their limit in that norm is $$u\notin H^s$$, so no limit exists in the stated space.

The standard correction is

$$
\langle u,v\rangle_{H^s}
=\langle\Lambda^s\widehat u,\Lambda^s\widehat v\rangle_2.
$$

Under this inner product, $$U_s:u\mapsto\Lambda^s\widehat u$$ is a linear isometry from $$H^s$$ onto $$L^2$$: given $$h\in L^2$$, choose $$u=\mathcal F^{-1}(\Lambda^{-s}h)$$. Consequently $$H^s$$ is Hilbert, and $$H^0=L^2$$ by Plancherel.

For $$s>t>0$$, $$\Lambda\ge1$$ gives continuous inclusions $$H^s\subset H^t\subset L^2$$. To prove density, choose $$h_j\in\mathcal S$$ with $$h_j\to\Lambda^s\widehat u$$ in $$L^2$$ and set $$u_j=\mathcal F^{-1}(\Lambda^{-s}h_j)$$. Since multiplication by $$\Lambda^{-s}$$ preserves $$\mathcal S$$, each $$u_j\in\mathcal S$$ and $$u_j\to u$$ in $$H^s$$. The same argument at exponent $$t$$ and ordinary Schwartz density in $$L^2$$ establish all the asserted dense inclusions.

For an integer $$m\ge0$$, the polynomial identity and elementary comparisons give constants $$c,C>0$$ such that

$$
c\Lambda(\xi)^{2m}\le\sum_{|\alpha|\le m}|\xi^\alpha|^2
\le C\Lambda(\xi)^{2m}.
$$

If $$u\in H^m$$, then $$\xi^\alpha\widehat u\in L^2$$ for $$|\alpha|\le m$$; its inverse transform, multiplied by $$i^{|\alpha|}$$, is the weak derivative $$\partial^\alpha u$$. Conversely, if $$u\in W^{m,2}$$, Fourier transformation of the weak derivatives yields $$\mathcal F(\partial^\alpha u)=(i\xi)^\alpha\widehat u$$ in $$L^2$$. The displayed comparison and Plancherel prove $$H^m=W^{m,2}$$ with equivalent norms.

### Exercise 7

For $$s>n/2$$, polar coordinates show $$\Lambda^{-s}\in L^2$$. Thus Cauchy–Schwarz gives

$$
\|\widehat u\|_1\le\|\Lambda^{-s}\|_2\|\Lambda^s\widehat u\|_2
=\|\Lambda^{-s}\|_2\|u\|_{H^s}.
$$

This proves (i). The inverse transform of an $$L^1$$ function belongs to $$C_0$$ by the Riemann–Lebesgue theorem. Fourier inversion in $$L^2$$ shows that this continuous function is a representative of $$u$$, and

$$
\|u\|_\infty\le(2\pi)^{-n/2}\|\Lambda^{-s}\|_2\|u\|_{H^s}.
$$

Hence the correct embedding is $$H^s\hookrightarrow C_0$$; it has dense range because $$\mathcal D\subset H^s$$ is dense in $$C_0$$.

The printed (ii) says $$H^2\hookrightarrow C_0$$ for arbitrary dimension, which does not follow merely from the existence of some $$s>n/2$$ and is false for $$n\ge4$$. For example, a smooth compactly supported cutoff of $$\log\log(e^2/|x|)$$ near zero is unbounded but lies in $$W^{2,2}(\mathbb R^n)$$ for $$n\ge4$$: the most singular second derivatives are $$O(|x|^{-2}/\log(1/|x|))$$, whose square is locally integrable even when $$n=4$$. Exercise 6 identifies this function with an element of $$H^2$$. For $$n<4$$, the printed embedding does hold by taking $$s=2$$.

### Exercise 8

The Gaussian kernel from Section 7 is

$$
K_t(x)=k_{\sqrt t}(x)=(4\pi t)^{-n/2}e^{-|x|^2/(4t)},\qquad
\widehat{K_t}(\xi)=(2\pi)^{-n/2}e^{-t|\xi|^2}.
$$

Thus, for $$f\in L^2$$,

$$
\widehat{T(t)f}(\xi)=e^{-t|\xi|^2}\widehat f(\xi).
$$

The convolution identity first holds for $$L^1\cap L^2$$ and extends by density and Young's inequality.

**(i)–(iii)** The multiplier has modulus at most 1, so $$\|T(t)f\|_{H^\sigma}\le\|f\|_{H^\sigma}$$. Multiplication of the Gaussian multipliers gives $$T(t+s)=T(t)T(s)$$. Finally,

$$
\|T(t)f-f\|_{H^\sigma}^2
=\int\Lambda^{2\sigma}|e^{-t|\xi|^2}-1|^2|\widehat f|^2\,d\xi
\longrightarrow0
$$

by dominated convergence.

**(iv)** The printed claim $$T(t)(L^2)\subset\mathcal S$$ is false: smoothing does not force rapid spatial decay. Take $$f(x)=(1+|x|^2)^{-b}$$ with $$b>n/4$$. Then $$f\in L^2$$ and, for large $$|x|$$,

$$
T(t)f(x)\ge\int_{|y|\le1}K_t(y)f(x-y)\,dy
\ge c_t(1+|x|)^{-2b}.
$$

Thus $$T(t)f$$ is not rapidly decreasing. The valid smoothing statement is $$T(t)(L^2)\subset\bigcap_{m\ge0}H^m$$, since $$\Lambda^m e^{-t|\xi|^2}$$ is bounded. In particular, the output has a smooth representative with bounded derivatives.

**(v)** For $$t>0$$, every polynomial in $$\xi$$ times $$e^{-t|\xi|^2}\widehat f$$ lies in $$L^1$$ by Cauchy–Schwarz. Locally uniformly for $$t>0$$ the same remains true after any number of $$t$$ and $$x$$ derivatives. Differentiating the inverse Fourier integral gives $$u\in C^\infty((0,\infty)\times\mathbb R^n)$$ and

$$
\widehat{\partial_tu}=-|\xi|^2e^{-t|\xi|^2}\widehat f
=\widehat{\Delta u},
$$

so the heat equation holds pointwise.

For the initial condition define $$u(0,x)=f(x)$$. Fix $$x_0$$. In the convolution, split the integral into $$|y-x_0|<\delta$$ and its complement. For $$x$$ near $$x_0$$, continuity of $$f$$ makes $$|f(y)-f(x_0)|$$ small on the first part. On the complement, Cauchy–Schwarz bounds the integral involving $$f$$ by $$\|f\|_2\|K_t\mathbf1_{|\cdot|>\delta/2}\|_2\to0$$; the corresponding kernel mass also tends to zero. Hence $$u(t,x)\to f(x_0)$$ as $$(t,x)\to(0,x_0)$$, establishing joint continuity and the pointwise initial condition.

### Exercise 9

For the kernel printed in the exercise,

$$
p_y(x)=\sqrt{\frac2\pi}\frac{y}{x^2+y^2},\qquad
\int_{\mathbb R}p_y(x)\,dx=\sqrt{2\pi},\qquad
\widehat{p_y}(\xi)=e^{-y|\xi|}.
$$

Consequently convolution by the printed kernel has multiplier $$\sqrt{2\pi}\,e^{-y|\xi|}$$. Part (i) is true, with operator norm at most $$\sqrt{2\pi}$$ on $$H^\sigma$$, but (ii), (iii), and the boundary value in (v) are false as written:

$$
P(y)P(z)=\sqrt{2\pi}\,P(y+z),\qquad
P(y)f\longrightarrow\sqrt{2\pi}\,f\quad\text{in }H^\sigma.
$$

The normalized Poisson kernel is instead

$$
q_y(x)=\frac1\pi\frac{y}{x^2+y^2},\qquad
\widehat{q_y}(\xi)=(2\pi)^{-1/2}e^{-y|\xi|}.
$$

For $$Q(y)f=q_y*f$$ the multiplier is exactly $$e^{-y|\xi|}$$. The same argument as in Exercise 8 gives $$\|Q(y)\|_{H^\sigma\to H^\sigma}\le1$$, $$Q(y+z)=Q(y)Q(z)$$ and $$Q(y)f\to f$$ in $$H^\sigma$$. Further, $$\Lambda^m e^{-y|\xi|}$$ is bounded for every $$m$$, so $$Q(y)(L^2)\subset\bigcap_mH^m$$.

Part (iv) is false even after normalizing. If $$f\in C_c^\infty(\mathbb R)$$ is nonnegative and nonzero, then for sufficiently large $$|x|$$,

$$
(q_y*f)(x)=\int q_y(x-z)f(z)\,dz\ge c_y|x|^{-2}.
$$

Thus the output is not Schwartz. The printed kernel is a positive scalar multiple and gives the same counterexample.

For the corrected boundary problem, put $$u(x,y)=Q(y)f(x)$$ when $$y>0$$ and $$u(x,0)=f(x)$$. If $$f\in L^2\cap C$$, all factors $$|\xi|^m e^{-y|\xi|}\widehat f$$ are integrable, locally uniformly for $$y>0$$, by Cauchy–Schwarz. Differentiating the inverse Fourier integral shows that $$u$$ is smooth for $$y>0$$ and

$$
\mathcal F_x(\partial_x^2u+\partial_y^2u)
=(-\xi^2+|\xi|^2)e^{-y|\xi|}\widehat f=0.
$$

To prove continuity at $$(x_0,0)$$, split the convolution into $$|z-x_0|<\delta$$ and its complement. The first part is controlled by continuity of $$f$$. For $$x$$ close to $$x_0$$, the other part is bounded using $$\|f\|_2\|q_y\mathbf1_{|\cdot|>\delta/2}\|_2\to0$$, while the tail mass of $$q_y$$ tends to zero. Hence $$u(x,y)\to f(x_0)$$. With the printed $$p_y$$ instead, the same argument gives boundary value $$\sqrt{2\pi}f$$.

### Exercise 10

Each $$q_k$$ is a seminorm and the series defining $$d$$ converges, since each summand is at most $$2^{-k}$$. If $$d(f,g)=0$$, all derivatives of order zero vanish on every $$\overline X_k$$; since the sets cover $$X$$, $$f=g$$. Symmetry is immediate, and the triangle inequality follows from

$$
q_k(f-h)\le q_k(f-g)+q_k(g-h),\qquad
\frac{a+b}{1+a+b}\le\frac a{1+a}+\frac b{1+b}\quad(a,b\ge0).
$$

Let $$(f_j)$$ be $$d$$-Cauchy. For each fixed $$k$$ it is Cauchy in $$q_k$$, so each derivative $$\partial^\alpha f_j$$ with $$|\alpha|\le k$$ converges uniformly on $$\overline X_k$$. The limits agree on overlaps. Every compact subset of $$X$$ lies in some $$X_k$$, since the $$X_k$$ are increasing and cover $$X$$. Thus all derivatives converge locally uniformly on $$X$$. Applying the fundamental theorem of calculus on small line segments, first to $$f_j$$ and its first derivatives and then inductively to higher derivatives, shows that the limiting functions are the corresponding derivatives of a single $$f\in C^\infty(X)$$.

For every fixed $$k$$, $$q_k(f_j-f)\to0$$. Given $$\eta>0$$ choose a finite number of terms so that the tail $$\sum_{k>N}2^{-k}<\eta/2$$; then take $$j$$ large enough that the first $$N+1$$ terms total less than $$\eta/2$$. Hence $$d(f_j,f)\to0$$, and the metric space is complete.

### Exercise 11

The inclusions are continuous for the usual test-function and Schwartz topologies: on any fixed compact set, each derivative supremum is controlled by a Schwartz seminorm, and the usual test-function convergence in a fixed compact support controls the same seminorms.

To prove density in $$C^\infty(\mathbb R^n)$$, take $$f\in C^\infty$$ and a cutoff $$\chi\in\mathcal D$$ equal to 1 on the unit ball. Put $$f_j(x)=\chi(x/j)f(x)$$. Each $$f_j\in\mathcal D\subset\mathcal S$$. On any fixed compact set, for all sufficiently large $$j$$ the cutoff is identically 1 in a neighborhood of that set, so every derivative of $$f_j-f$$ vanishes there. Thus $$f_j\to f$$ in the metric of Exercise 10, and both $$\mathcal D$$ and $$\mathcal S$$ are dense.

### Exercise 12

For $$n=1$$ and $$f\in\mathcal D(\mathbb R)$$, define

$$
F(z)=\int_{\mathbb R}e^{-izx}f(x)\,dx,\qquad z\in\mathbb C.
$$

If $$\operatorname{supp}f\subset[-R,R]$$, expanding the exponential and integrating term by term gives

$$
F(z)=\sum_{k=0}^\infty\frac{(-iz)^k}{k!}\int x^k f(x)\,dx.
$$

For $$|z|\le M$$ the sum of the absolute values is bounded by $$e^{MR}\|f\|_1$$. Thus the power series converges locally uniformly for every $$z\in\mathbb C$$, proving that $$F$$ is entire. Differentiation under the integral gives $$F^{(k)}(z)=\int(-ix)^ke^{-izx}f(x)\,dx$$.

For general $$n$$ the natural version uses $$z\in\mathbb C^n$$ and the complex-bilinear expression $$z\cdot x=\sum z_jx_j$$. The same compact-support estimate gives an entire function on $$\mathbb C^n$$, or equivalently an entire function of each coordinate separately. The printed line uses a $$\mathbb C^n$$ pairing but writes $$z\in\mathbb C$$; the one-dimensional interpretation above and this multidimensional version make the domains explicit.

### Exercise 13

Suppose $$f\in\mathcal D(\mathbb R^n)$$ and $$\widehat f\in\mathcal D(\mathbb R^n)$$. Exercise 12 extends $$\widehat f$$, up to the harmless normalization constant, to an entire function $$F$$ on $$\mathbb C^n$$. Because $$\widehat f$$ has compact support, it vanishes on a nonempty open real box $$I_1\times\cdots\times I_n$$.

Fix real $$x_2\in I_2,\ldots,x_n\in I_n$$. The entire one-variable function $$z_1\mapsto F(z_1,x_2,\ldots,x_n)$$ vanishes on $$I_1$$, hence everywhere by the identity theorem. Next fix arbitrary complex $$z_1$$ and real $$x_3\in I_3,\ldots,x_n\in I_n$$; the function of $$z_2$$ vanishes on $$I_2$$ and is therefore identically zero. Repeating this argument coordinate by coordinate gives $$F\equiv0$$ on $$\mathbb C^n$$. Thus $$\widehat f=0$$ and Fourier injectivity yields $$f=0$$, a contradiction. Therefore $$\widehat f\notin\mathcal D$$ whenever $$f\ne0$$.
