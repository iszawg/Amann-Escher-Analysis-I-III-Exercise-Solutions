The solutions below use the Stone–Weierstrass theorem and the Bernstein polynomial identities developed in this section. Two statements in the printed exercises need qualification: the norm cited in Exercise 1 omits the zeroth derivative, and Exercise 10(a) calls a zero-mean subspace an algebra. Both issues are identified where they occur.

### Exercise 1

Let $$r\in\mathbb N$$ be the differentiability order. There is a misprint in the definition cited from Exercise V.2.10: it gives $$\|f\|_{BC^r}=\max_{1\leq j\leq r}\|f^{(j)}\|_\infty$$. This expression vanishes on every constant function, so it is only a seminorm and cannot make $$BC^r(X,\mathbb K)$$ a Banach space. In what follows, use the usual norm that includes the function itself:

$$
\|f\|_r:=\max_{0\leq j\leq r}\|f^{(j)}\|_\infty.
$$

For $$r=0$$ this is the supremum norm on $$BC(X,\mathbb K)$$.

Pointwise addition and scalar multiplication preserve bounded derivatives. The Leibniz rule gives, for $$0\leq j\leq r$$,

$$
(fg)^{(j)}
=\sum_{\ell=0}^{j}\binom{j}{\ell}f^{(\ell)}g^{(j-\ell)}.
$$

Every term on the right is bounded and continuous, so $$fg\in BC^r(X,\mathbb K)$$. Also, the constant function $$1$$ belongs to this space and $$\|1\|_r=1$$. Thus it is an algebra with unity.

The same formula yields

$$
\|fg\|_r
\leq \max_{0\leq j\leq r}\sum_{\ell=0}^{j}\binom{j}{\ell}
\|f^{(\ell)}\|_\infty\|g^{(j-\ell)}\|_\infty
\leq 2^r\|f\|_r\|g\|_r.
$$

Consequently multiplication is continuous. Indeed,

$$
\|fg-\widetilde f\widetilde g\|_r
\leq 2^r\bigl(\|f-\widetilde f\|_r\|g\|_r
+\|\widetilde f\|_r\|g-\widetilde g\|_r\bigr),
$$

which tends to zero when $$f\to\widetilde f$$ and $$g\to\widetilde g$$ in this norm.

For completeness, let $$(f_n)$$ be Cauchy in $$\|\cdot\|_r$$. For each $$j=0,\ldots,r$$, the sequence $$(f_n^{(j)})$$ is uniformly Cauchy in $$BC(X,\mathbb K)$$, hence converges uniformly to some bounded continuous function $$g_j$$. On any small line segment contained in $$X$$, the fundamental theorem of calculus gives

$$
f_n^{(j)}(x)-f_n^{(j)}(x_0)
=(x-x_0)\int_0^1 f_n^{(j+1)}\bigl(x_0+t(x-x_0)\bigr)\,dt
\qquad (j<r).
$$

Uniform convergence lets us pass to the limit in this identity. It follows successively that $$g_j'=g_{j+1}$$ for $$j<r$$. Hence $$g_0\in BC^r(X,\mathbb K)$$, with derivatives $$g_j$$, and $$f_n\to g_0$$ in $$\|\cdot\|_r$$. This proves completeness.

The norm is submultiplicative when $$r=0$$, since $$\|fg\|_\infty\leq\|f\|_\infty\|g\|_\infty$$. For every $$r\geq1$$, submultiplicativity fails in general. Take $$X=(-1,1)$$ and $$f(x)=x$$. Then $$\|f\|_r=1$$, while $$\|f^2\|_r\geq\|2x\|_\infty=2$$. Therefore, for arbitrary open $$X$$, the usual space is a Banach algebra at order $$r=0$$. Higher orders are Banach spaces with continuous multiplication, but this maximum norm is not generally an algebra norm.

### Exercise 2

For each $$j=0,\ldots,k$$, define the continuous nonzero linear (or conjugate-linear, depending on the inner-product convention) functional

$$
L_j(x):=(x\mid x_j).
$$

It is nonzero because $$x_j\ne0$$. Its kernel is a closed hyperplane with empty interior: if $$L_j(x)=0$$, arbitrarily small perturbations in the direction $$x_j$$ leave the kernel. Thus $$\mathbb K^n\setminus\ker L_j$$ is open and dense. The set in the exercise is

$$
\bigcap_{j=0}^{k}\bigl(\mathbb K^n\setminus\ker L_j\bigr).
$$

A finite intersection of open dense sets is open and dense. To see density directly, intersect any nonempty open set successively with each open dense factor; at every step the intersection remains nonempty and open. This proves the claim.

### Exercise 3

**(a)** The assertion is false. In $$\mathbb R$$, both $$\mathbb Q$$ and $$\mathbb R\setminus\mathbb Q$$ are dense, but their intersection is empty and hence not dense.

**(b)** The assertion is true. A finite intersection of open sets is open. For density, let $$U$$ be any nonempty open subset of $$M$$. Since the first dense open set meets $$U$$, their intersection is nonempty and open. Intersecting this set successively with each remaining dense open set keeps it nonempty and open. Thus every nonempty open $$U$$ meets the finite intersection, which is exactly density.

### Exercise 4

Assume $$n\geq1$$, as required for the uncountability claim. The Euclidean space $$\mathbb K^n$$ is complete. Since every $$D_k$$ is open and dense, the Baire category theorem implies that

$$
D=\bigcap_{k\in\mathbb N}D_k
$$

is dense in $$\mathbb K^n$$. This proves (a).

For (b), suppose instead that $$D$$ were countable, and list its elements as $$(x_m)_{m\in\mathbb N}$$, repeating elements if $$D$$ is finite. When $$n\geq1$$, each singleton $$\{x_m\}$$ is closed with empty interior, so $$\mathbb K^n\setminus\{x_m\}$$ is open and dense. Baire's theorem applied to the combined countable family of open dense sets $$D_k$$ and $$\mathbb K^n\setminus\{x_m\}$$ says that

$$
\left(\bigcap_{k\in\mathbb N}D_k\right)
\cap
\left(\bigcap_{m\in\mathbb N}(\mathbb K^n\setminus\{x_m\})\right)
$$

is nonempty. The first intersection is $$D$$, while the second removes every element in the assumed enumeration of $$D$$. This is a contradiction. Hence $$D$$ is uncountable.

### Exercise 5

For $$k\in\mathbb N^\times$$, let

$$
D_k:=\{x\in\mathbb R:\omega_f(x)<1/k\},
$$

where $$\omega_f(x)$$ is the local oscillation of $$f$$ at $$x$$. Each $$D_k$$ is open: if the oscillation at $$x$$ is less than $$1/k$$, some neighborhood of $$x$$ has image diameter less than $$1/k$$, and every sufficiently nearby point has a smaller neighborhood inside it. Each rational point is a continuity point, so $$\mathbb Q\subseteq D_k$$. Therefore every $$D_k$$ is dense.

At a point, continuity is equivalent to zero local oscillation. Thus every irrational discontinuity has $$\omega_f(x)>0$$ and is excluded from some $$D_k$$ (choose $$k$$ with $$1/k\leq\omega_f(x)$$). Under the proposed behavior this gives

$$
\bigcap_{k\in\mathbb N^\times}D_k=\mathbb Q.
$$

But Exercise 4(b) says that a countable intersection of open dense subsets of $$\mathbb R$$ is uncountable. Since $$\mathbb Q$$ is countable, this is impossible. No such function exists.

### Exercise 6

Let $$\Phi:\mathbb K^n\to V$$ be the coordinate map

$$
\Phi(\alpha_1,\ldots,\alpha_n)=\sum_{j=1}^{n}\alpha_jb_j.
$$

The proposed set is $$\Phi(D^n)$$. Since $$D$$ is countable, the finite product $$D^n$$ is countable, and its image is countable.

To prove density, fix $$v=\sum_{j=1}^{n}\alpha_jb_j\in V$$ and $$\varepsilon>0$$. Choose $$d_j\in D$$ close enough to $$\alpha_j$$ that

$$
\sum_{j=1}^{n}|d_j-\alpha_j|\,\|b_j\|<\varepsilon.
$$

Then $$\sum_j d_jb_j$$ belongs to the proposed set and

$$
\left\|v-\sum_{j=1}^{n}d_jb_j\right\|
\leq\sum_{j=1}^{n}|d_j-\alpha_j|\,\|b_j\|<\varepsilon.
$$

Thus the set is dense in $$V$$.

### Exercise 7

If $$x,y\in M$$ are distinct, some coordinate, say the $$j$$th, satisfies $$x_j\ne y_j$$. The coordinate polynomial $$X_j$$ then has $$X_j(x)\ne X_j(y)$$, so $$A$$ separates points.

When $$\mathbb K=\mathbb R$$, every member of $$A$$ is real-valued and therefore equals its complex conjugate (in the real-valued sense). When $$\mathbb K=\mathbb C$$, write a polynomial as $$p=\sum_\alpha c_\alpha X^\alpha$$. Since every coordinate of $$x\in M\subseteq\mathbb R^n$$ is real,

$$
\overline{p(x)}
=\sum_\alpha\overline{c_\alpha}X^\alpha(x).
$$

The right-hand side is the restriction to $$M$$ of the polynomial with conjugated coefficients. Hence $$\overline p\in A$$, and $$A$$ is self-adjoint.

### Exercise 8

By the Weierstrass approximation theorem, choose polynomials $$p_n$$ with coefficients in $$\mathbb K$$ such that $$p_n\to f$$ uniformly on $$[a,b]$$. Define

$$
F_n(x):=\int_a^x p_n(t)\,dt.
$$

Each $$F_n$$ is a polynomial primitive, so $$F_n\in C^1([a,b],\mathbb K)$$, $$F_n'=p_n$$, and $$F_n(a)=0$$. The derivatives $$F_n'$$ converge uniformly to $$f$$, and the values $$F_n(a)$$ converge. Exercise V.2.11 therefore implies that $$(F_n)$$ converges uniformly to some function $$F$$. The differentiability theorem for limits in Section V.2 now gives $$F\in C^1([a,b],\mathbb K)$$ and $$F'=f$$. Thus $$f$$ has an antiderivative.

### Exercise 9

Periodicity gives $$f(0)=f(2\pi)$$. Rolle's theorem applied to $$f$$ on $$[0,2\pi]$$ gives a point $$c\in(0,2\pi)$$ with $$f'(c)=0$$.

### Exercise 10

Write an absolutely convergent trigonometric series with zero constant coefficient as

$$
f(t)=\sum_{k=1}^{\infty}\bigl(a_k\cos(kt)+b_k\sin(kt)\bigr),
\qquad
\sum_{k=1}^{\infty}(|a_k|+|b_k|)<\infty.
$$

The series converges absolutely and uniformly, so it defines a continuous $$2\pi$$-periodic function.

**(a)** As printed, the assertion that $$D_0(\mathbb R,\mathbb K)$$ is a subalgebra is false. Take $$f(t)=\cos t$$. It belongs to $$D_0$$, but

$$
f(t)^2=\cos^2t=\frac{1+\cos(2t)}2
$$

has constant coefficient $$1/2$$, so it does not belong to $$D_0$$. The set is a linear subspace, since sums and scalar multiples preserve absolute convergence and zero constant coefficient, but it is not closed under multiplication.

**(b)** Define

$$
F(t):=\sum_{k=1}^{\infty}
\left(\frac{a_k}{k}\sin(kt)-\frac{b_k}{k}\cos(kt)\right).
$$

The series for $$F$$ converges absolutely and uniformly, and each partial sum is $$2\pi$$-periodic. Its termwise derivative series is precisely the absolutely uniformly convergent series for $$f$$. The theorem on differentiating uniformly convergent series therefore gives $$F'=f$$. The uniform limit $$F$$ is also $$2\pi$$-periodic, so it is the required periodic antiderivative.

**(c)** For real coefficients, termwise integration is justified by uniform convergence and gives

$$
\int_0^{2\pi}f(t)\,dt=0,
$$

because every sine and cosine term has integral zero. If $$f$$ had no zero in $$(0,2\pi)$$, continuity and connectedness would force it to be strictly positive everywhere on that interval or strictly negative everywhere there. In the positive case its integral is positive; in the negative case its integral is negative. Both contradict the displayed equality. Hence $$f$$ has a zero in $$(0,2\pi)$$.

**(d)** For complex-valued functions, take $$f(t)=e^{it}=\cos t+i\sin t$$. This is a trigonometric polynomial with zero constant coefficient, so it belongs to $$D_0(\mathbb R,\mathbb C)$$, but $$|f(t)|=1$$ for every $$t$$. Thus the real-valued conclusion in (c) fails over $$\mathbb C$$.

### Exercise 11

By the binomial theorem,

$$
\sum_{k=0}^{n}B_{n,k}
=\sum_{k=0}^{n}\binom nkX^k(1-X)^{n-k}
=(X+(1-X))^n=1,
$$

which proves (a).

For (b), use $$k\binom nk=n\binom{n-1}{k-1}$$ and reindex (the identity is immediate when $$n=0$$):

$$
\sum_{k=0}^{n}kB_{n,k}
=nX\sum_{k=1}^{n}\binom{n-1}{k-1}X^{k-1}(1-X)^{n-k}
=nX.
$$

For $$n=0$$ or $$n=1$$, the second sum is zero on both sides. For $$n\geq2$$, $$k(k-1)\binom nk=n(n-1)\binom{n-2}{k-2}$$, so

$$
\sum_{k=0}^{n}k(k-1)B_{n,k}
=n(n-1)X^2
\sum_{k=2}^{n}\binom{n-2}{k-2}X^{k-2}(1-X)^{n-k}
=n(n-1)X^2.
$$

For (c), expand the square and use $$k^2=k(k-1)+k$$:

$$
\begin{aligned}
\sum_{k=0}^{n}(k-nX)^2B_{n,k}
&=\sum_{k=0}^{n}k^2B_{n,k}
-2nX\sum_{k=0}^{n}kB_{n,k}
+n^2X^2\sum_{k=0}^{n}B_{n,k}\\
&=n(n-1)X^2+nX-2n^2X^2+n^2X^2\\
&=nX(1-X).
\end{aligned}
$$

### Exercise 12

Take $$n\geq1$$ and, for $$x\in[0,1]$$, set $$w_{n,k}(x):=B_{n,k}(x)$$. These weights are nonnegative and sum to one by Exercise 11(a). Thus

$$
\|B_n(f)(x)-f(x)\|
\leq\sum_{k=0}^{n}
\left\|f\left(\frac{k}{n}\right)-f(x)\right\|w_{n,k}(x).
$$

The function $$f$$ is uniformly continuous on $$[0,1]$$. Given $$\varepsilon>0$$, choose $$\delta>0$$ such that $$|u-x|<\delta$$ implies $$\|f(u)-f(x)\|<\varepsilon/2$$. Let $$M:=\max_{u\in[0,1]}\|f(u)\|$$. If $$M=0$$ the result is immediate. For the indices with $$|k/n-x|\geq\delta$$, Exercise 11(c) gives the uniform tail bound

$$
\begin{aligned}
\sum_{|k/n-x|\geq\delta}w_{n,k}(x)
&\leq\frac1{\delta^2}\sum_{k=0}^{n}\left(\frac{k}{n}-x\right)^2w_{n,k}(x)\\
&=\frac{x(1-x)}{n\delta^2}
\leq\frac1{4n\delta^2}.
\end{aligned}
$$

The near indices contribute at most $$\varepsilon/2$$, while the far indices contribute at most $$2M/(4n\delta^2)$$. Choose $$n$$ large enough that the latter is less than $$\varepsilon/2$$. The resulting estimate is independent of $$x$$, so

$$
\|B_n(f)-f\|_\infty\longrightarrow0.
$$

This proves convergence in $$C([0,1],E)$$ and, equivalently, uniform convergence.

### Exercise 13

**(a)** Let $$D$$ be a countable dense subset of the separable metric space $$X$$. Consider all open balls $$B(d,q)$$ with $$d\in D$$ and positive rational radius $$q\in\mathbb Q$$. There are countably many. They form a basis: if $$x\in U$$ and $$U$$ is open, choose $$\varepsilon>0$$ with $$B(x,\varepsilon)\subseteq U$$. Density gives $$d\in D$$ with $$d(x,d)<\varepsilon/3$$. Choose rational $$q$$ such that $$d(x,d)<q<\varepsilon-d(x,d)$$. Then $$x\in B(d,q)\subseteq B(x,\varepsilon)\subseteq U$$.

**(b)** Let $$\mathcal B$$ be the countable basis from (a), and let $$A\subseteq X$$. For each $$B\in\mathcal B$$ with $$B\cap A\ne\varnothing$$, choose one point $$a_B\in B\cap A$$. The set of chosen points is countable. It is dense in $$A$$: if $$x\in A$$ and $$U$$ is a relative neighborhood of $$x$$ in $$A$$, write $$U=A\cap V$$ for some open $$V\subseteq X$$. Choose $$B\in\mathcal B$$ with $$x\in B\subseteq V$$. Then $$a_B\in B\cap A\subseteq U$$.

**(c)** The space $$\mathbb R^n$$ is separable because $$\mathbb Q^n$$ is countable and dense. Part (b), applied to any subset $$A\subseteq\mathbb R^n$$ with its induced metric, shows that $$A$$ is separable.

### Exercise 14

The empty space and the one-point space have separable continuous-function spaces, so assume $$X$$ has at least two points. Let $$\mathcal B$$ be a countable basis for $$X$$, and, for each proper open set $$B\in\mathcal B$$, define

$$
d_B(x):=d(x,B^c).
$$

The function $$d_B$$ is continuous, bounded on compact $$X$$, positive at every point of $$B$$, and zero on $$B^c$$. If $$x\ne y$$, choose an open neighborhood of $$x$$ that does not contain $$y$$, then choose a basis element $$B$$ with $$x\in B$$ contained in that neighborhood. For this element, $$d_B(x)>0=d_B(y)$$. Hence the real algebra generated by the functions $$d_B$$ and the constants separates points of $$X$$.

By the real Stone–Weierstrass theorem, real polynomials in finitely many of the functions $$d_B$$ are dense in $$C(X,\mathbb R)$$. Restricting their coefficients to $$\mathbb Q$$ still gives a dense set: each such polynomial is a finite linear combination of bounded monomials, so its finitely many real coefficients can be approximated by rationals with arbitrarily small uniform error. There are only countably many choices of basis elements, exponents, and rational coefficients. Thus these rational polynomials form a countable dense subset of $$C(X,\mathbb R)$$.

For $$\mathbb K=\mathbb C$$, approximate the real and imaginary parts of any $$f\in C(X,\mathbb C)$$ by rational-coefficient polynomials in the $$d_B$$ and combine the approximants as $$p+iq$$. The resulting coefficient set $$\mathbb Q+i\mathbb Q$$ is countable, so $$C(X,\mathbb C)$$ is separable as well.

Finally, since $$X$$ is compact, every continuous scalar-valued function on $$X$$ is bounded, and uniform limits of continuous functions are continuous. The supremum norm is therefore complete, so $$C(X,\mathbb K)$$ is a separable Banach space.
