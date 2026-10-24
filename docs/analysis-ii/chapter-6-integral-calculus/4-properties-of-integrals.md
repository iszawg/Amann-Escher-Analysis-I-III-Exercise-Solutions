# Chapter VI — Integral Calculus in One Variable

## 4. Properties of Integrals

Throughout, let $$I=[\alpha,\beta]$$ with $$\alpha<\beta$$, let $$E$$ be a Banach space, and use the definitions and results of Sections VI.1–VI.4. Integrals of jump continuous functions are Cauchy–Riemann integrals. For scalar-valued functions, $$\mathbb K$$ is either $$\mathbb R$$ or $$\mathbb C$$. The norm $$\|\cdot\|_p$$ is the one in Exercise 4, and $$\|\cdot\|_\infty$$ is the supremum norm.

### Exercise 1

Let $$P$$ be the positive cone of the ordered vector space $$V$$, so $$x\leq y$$ exactly when $$y-x\in P$$. Let $$\varphi:V\to\mathbb R$$ be linear.

If $$\varphi$$ is positive, then $$x\leq y$$ implies $$y-x\in P$$ and hence

$$
\varphi(y)-\varphi(x)=\varphi(y-x)\geq0.
$$

Thus $$\varphi$$ is increasing. Conversely, if $$\varphi$$ is increasing and $$x\in P$$, then $$0\leq x$$, so

$$
0=\varphi(0)\leq\varphi(x).
$$

Therefore $$\varphi$$ is positive if and only if it is increasing, as asserted in Remark 4.7(b).

### Exercise 2

For $$f\in S(I,\mathbb K)$$, we prove

$$
\int_\alpha^\beta \overline{f(x)}\,dx
=\overline{\int_\alpha^\beta f(x)\,dx}.
$$

First suppose $$f$$ is a staircase function with value $$c_j$$ on each cell $$[\alpha_{j-1},\alpha_j)$$ of a partition. Then

$$
\int_\alpha^\beta \overline{f(x)}\,dx
=\sum_j\overline{c_j}(\alpha_j-\alpha_{j-1})
=\overline{\sum_j c_j(\alpha_j-\alpha_{j-1})}
=\overline{\int_\alpha^\beta f(x)\,dx}.
$$

For a general jump continuous $$f$$, choose staircase functions $$f_n$$ converging uniformly to $$f$$. Then $$\overline{f_n}\to\overline f$$ uniformly as well. Continuity of integration gives $$\int\overline{f_n}\to\int\overline f$$ and $$\int f_n\to\int f$$. Passing to the limit in the staircase identity proves the result. For $$\mathbb K=\mathbb R$$ this reduces to the identity itself.

### Exercise 3

Let $$D$$ be the union of the discontinuity sets of $$f_1$$ and $$f_2$$. Piecewise continuous functions have only finitely many discontinuities, so $$D$$ is finite. Since $$f_1$$ and $$f_2$$ agree away from their discontinuities, the jump continuous function $$h=f_1-f_2$$ vanishes outside $$D$$.

Set $$M=\max_{x\in D}\|h(x)\|_E$$; if $$D=\varnothing$$, then $$h=0$$ and there is nothing to prove. Given $$\eta>0$$, cover the finitely many points of $$D$$ by intervals whose total length is less than $$\eta$$. By additivity and the norm estimate for integrals,

$$
\left\|\int_\alpha^\beta h(x)\,dx\right\|_E
\leq \int_\alpha^\beta\|h(x)\|_E\,dx
\leq M\eta.
$$

As $$\eta$$ is arbitrary, $$\int h=0$$. Linearity now yields $$\int f_1=\int f_2$$. The argument includes a discontinuity at either endpoint; changing finitely many point values does not change the integral.

### Exercise 4

For $$f\in S(I,\mathbb K)$$ and $$1\leq p<\infty$$, put

$$
\|f\|_p=\left(\int_\alpha^\beta |f(x)|^p\,dx\right)^{1/p}.
$$

Write $$p'$$ for the dual exponent, with $$p'=\infty$$ when $$p=1$$.

**(i) Hölder inequality.** The triangle inequality for the integral gives

$$
\left|\int_\alpha^\beta f(x)g(x)\,dx\right|
\leq\int_\alpha^\beta|f(x)g(x)|\,dx.
$$

When $$p=1$$, boundedness of $$g$$ gives

$$
\int_\alpha^\beta|fg|\,dx
\leq \|g\|_\infty\int_\alpha^\beta|f|\,dx
=\|f\|_1\|g\|_\infty.
$$

Now suppose $$1<p<\infty$$. If either norm on the right is zero, the inequality is immediate. Otherwise, normalize $$u=|f|/\|f\|_p$$ and $$v=|g|/\|g\|_{p'}$$. Young's inequality $$uv\leq u^p/p+v^{p'}/p'$$ gives, after integration,

$$
\int_\alpha^\beta uv\,dx
\leq \frac1p\int_\alpha^\beta u^p\,dx
+\frac1{p'}\int_\alpha^\beta v^{p'}\,dx
=\frac1p+\frac1{p'}=1.
$$

Undoing the normalization proves $$\int|fg|\leq\|f\|_p\|g\|_{p'}$$, and hence the stated inequality.

**(ii) Minkowski inequality.** For $$p=1$$, it follows by integrating $$|f+g|\leq|f|+|g|$$. Suppose $$p>1$$ and set $$h=f+g$$. If $$\|h\|_p=0$$ there is nothing to prove. Otherwise, using Hölder with exponents $$p$$ and $$p'$$,

$$
\begin{aligned}
\|h\|_p^p
&=\int |h|^p\,dx\\
&\leq\int (|f|+|g|)|h|^{p-1}\,dx\\
&\leq (\|f\|_p+\|g\|_p)
\left(\int |h|^{(p-1)p'}\,dx\right)^{1/p'}\\
&=(\|f\|_p+\|g\|_p)\|h\|_p^{p-1},
\end{aligned}
$$

because $$(p-1)p'=p$$. Dividing by $$\|h\|_p^{p-1}$$ proves Minkowski's inequality.

**(iii) The normed vector space.** Nonnegativity and absolute homogeneity follow from the definition, and Minkowski gives the triangle inequality. To prove definiteness, suppose $$f\in C(I,\mathbb K)$$ is nonzero. There is a point $$x_0$$ with $$|f(x_0)|>0$$. Continuity gives a relative interval of positive length on which $$|f(x)|\geq |f(x_0)|/2$$. Therefore $$\int |f|^p>0$$ and $$\|f\|_p>0$$. Thus $$\|\cdot\|_p$$ is a norm on $$C(I,\mathbb K)$$.

**(iv) The inner product space.** Define

$$
\langle f,g\rangle=\int_\alpha^\beta f(x)\overline{g(x)}\,dx.
$$

Linearity in the first argument follows from linearity of integration; conjugate symmetry follows from Exercise 2; and $$\langle f,f\rangle=\int|f|^2\geq0$$. The definiteness proved in (iii) shows that $$\langle f,f\rangle=0$$ only for $$f=0$$. Its induced norm is $$\|f\|_2$$, so $$C(I,\mathbb K)$$ with this inner product is an inner product space.

**(v) Comparison of the norms.** Let $$L=\beta-\alpha$$. For finite $$q\geq p$$ with $$p<q$$, apply Hölder to $$|f|^p\cdot1$$ with exponents $$q/p$$ and $$q/(q-p)$$:

$$
\int_\alpha^\beta |f|^p\,dx
\leq\left(\int_\alpha^\beta|f|^q\,dx\right)^{p/q}
L^{1-p/q}.
$$

Taking the $$p$$th root gives $$\|f\|_p\leq L^{1/p-1/q}\|f\|_q$$. If $$p=q$$ this is equality. For $$q=\infty$$, the direct bound $$\int|f|^p\leq L\|f\|_\infty^p$$ gives the same formula with $$1/q=0$$.

### Exercise 5

Exercise 4(v) gives

$$
\|f\|_p\leq (\beta-\alpha)^{1/p-1/q}\|f\|_q
\qquad(1\leq p\leq q\leq\infty),
$$

so the $$q$$-norm is stronger than the $$p$$-norm in the sense of the footnote to the exercise.

To see that the norms are not equivalent when $$p<q<\infty$$, choose an interior point $$c$$ and, for all sufficiently large $$n$$, define the continuous triangular function

$$
f_n(x)=\max\{1-n|x-c|,0\}.
$$

Its support is contained in $$I$$ and, for each finite $$r\geq1$$,

$$
\|f_n\|_r^r
=2\int_0^{1/n}(1-nt)^r\,dt
=\frac{2}{n(r+1)}.
$$

Consequently $$\|f_n\|_q/\|f_n\|_p$$ is a positive constant times $$n^{1/p-1/q}$$ and tends to infinity. No constant can therefore bound $$\|f\|_q$$ by $$\|f\|_p$$. If $$q=\infty$$, then $$\|f_n\|_\infty=1$$ while $$\|f_n\|_p\to0$$, giving the same conclusion.

### Exercise 6

Let $$c=(\alpha+\beta)/2$$ and define the step function $$u(x)=0$$ for $$x\leq c$$ and $$u(x)=1$$ for $$x>c$$. For sufficiently large $$n$$, define a continuous ramp

$$
f_n(x)=
\begin{cases}
0,&x\leq c-1/n,\\
\frac n2(x-c+1/n),&c-1/n<x<c+1/n,\\
1,&x\geq c+1/n.
\end{cases}
$$

The functions $$f_n$$ are continuous and $$|f_n-u|\leq1$$, with the difference supported on an interval of length $$2/n$$. Hence, for every finite $$p\geq1$$,

$$
\|f_n-u\|_p^p\leq\frac2n\longrightarrow0.
$$

By Minkowski, $$\|f_n-f_m\|_p\leq\|f_n-u\|_p+\|f_m-u\|_p$$, so $$(f_n)$$ is Cauchy in $$C(I,\mathbb K)$$.

If it converged in this norm to some $$g\in C(I,\mathbb K)$$, the same triangle inequality would give $$\|g-u\|_p=0$$. Thus $$g=u$$ almost everywhere. On each of the open intervals to the left and right of $$c$$, the points where this equality holds are dense. Continuity would force $$g=0$$ throughout the left interval and $$g=1$$ throughout the right interval, which is impossible at $$c$$. So this Cauchy sequence has no limit in $$C(I,\mathbb K)$$. The space is not complete for finite $$p$$, and in particular it is neither a Banach space for $$1\leq p<\infty$$ nor a Hilbert space for $$p=2$$.

### Exercise 7

Choose $$x_0\in I$$ such that $$|f(x_0)|=\|f\|_\infty$$. Since $$f(\alpha)=f(\beta)=0$$, the fundamental theorem of calculus applied to $$f^2$$ gives

$$
\begin{aligned}
\|f\|_\infty^2=f(x_0)^2
&=\int_\alpha^{x_0}f(x)f'(x)\,dx
-\int_{x_0}^\beta f(x)f'(x)\,dx.
\end{aligned}
$$

Apply Cauchy–Schwarz to each integral and then Cauchy–Schwarz to the two resulting vectors in $$\mathbb R^2$$:

$$
\begin{aligned}
\|f\|_\infty^2
&\leq\left(\int_\alpha^{x_0}f^2\right)^{1/2}
       \left(\int_\alpha^{x_0}(f')^2\right)^{1/2}
+\left(\int_{x_0}^{\beta}f^2\right)^{1/2}
       \left(\int_{x_0}^{\beta}(f')^2\right)^{1/2}\\
&\leq\left(\int_\alpha^\beta f^2\right)^{1/2}
       \left(\int_\alpha^\beta(f')^2\right)^{1/2}\\
&\leq\frac12\int_\alpha^\beta\bigl(f^2+(f')^2\bigr)\,dx.
\end{aligned}
$$

The last step is $$2ab\leq a^2+b^2$$. This proves (4.10).

If only $$f(\alpha)=0$$ is assumed, take $$x_0$$ with $$|f(x_0)|=\|f\|_\infty$$ and use

$$
f(x_0)^2=2\int_\alpha^{x_0}f(x)f'(x)\,dx.
$$

Cauchy–Schwarz and $$2ab\leq a^2+b^2$$ yield the modified estimate

$$
\|f\|_\infty^2
\leq \int_\alpha^{x_0}\bigl(f^2+(f')^2\bigr)\,dx
\leq \int_\alpha^\beta\bigl(f^2+(f')^2\bigr)\,dx.
$$

The constant is twice the one in (4.10).

### Exercise 8

Define $$F(x)=\int_\alpha^x|f'(\xi)|\,d\xi$$. Then $$F(\alpha)=0$$, $$F'=|f'|$$, and, since $$f(\alpha)=0$$,

$$
|f(x)|=\left|\int_\alpha^x f'(\xi)\,d\xi\right|
\leq F(x).
$$

It follows that

$$
\int_\alpha^\beta|f f'|\,dx
\leq\int_\alpha^\beta F F'\,dx
=\frac12 F(\beta)^2
=\frac12\left(\int_\alpha^\beta|f'|\,dx\right)^2.
$$

By Cauchy–Schwarz, $$\left(\int_\alpha^\beta|f'|\,dx\right)^2\leq(\beta-\alpha)\int_\alpha^\beta|f'|^2\,dx$$. Combining the inequalities proves the claim.

### Exercise 9

**The statement is false as printed.** The right-hand side in the supplied exercise is quadratic in $$f$$, whereas the left-hand side is linear in $$f$$. The hypotheses are preserved when $$f$$ is multiplied by any positive constant, so this mismatch can already cause failure by scaling.

Here is an explicit counterexample on $$I=[0,1]$$. For $$\varepsilon>0$$, let $$f(x)=-\varepsilon\sin(\pi x)$$. Then $$f\in C^2(I,\mathbb R)$$, $$f(0)=f(1)=0$$, and

$$
f''(x)=\varepsilon\pi^2\sin(\pi x)\geq -\varepsilon\sin(\pi x)=f(x).
$$

Also $$\max_{x\in I}f'(x)=\varepsilon\pi$$, while

$$
\frac1{\sqrt2}\int_0^1\bigl(f^2+(f')^2\bigr)\,dx
=\frac{\varepsilon^2(1+\pi^2)}{2\sqrt2}.
$$

For example, at $$\varepsilon=1/10$$ the claimed upper bound would require $$\pi/10\leq(1+\pi^2)/(200\sqrt2)$$, which is false. Thus no proof of the displayed claim can be given with the printed assumptions and right-hand side. The exercise or its hint/formula needs correction in the source.

### Exercise 10

Set $$F(x)=\int_\alpha^x f(s)\,ds$$. Since $$f$$ is continuous, $$F\in C^1(I,\mathbb R)$$, $$F(\alpha)=0$$, and $$F'=f$$. Integration by parts gives

$$
\int_\alpha^\beta f(x)g(x)\,dx
=F(\beta)g(\beta)-\int_\alpha^\beta F(x)g'(x)\,dx.
$$

If $$g$$ is constant, the desired identity holds for every $$\xi\in I$$. Otherwise, monotonicity implies that $$g'$$ has one fixed sign and

$$
\int_\alpha^\beta|g'(x)|\,dx=|g(\beta)-g(\alpha)|>0.
$$

Apply Proposition 4.16 to the continuous function $$F$$ with nonnegative weight $$|g'|$$. It gives a point $$\xi\in I$$ such that

$$
\int_\alpha^\beta F(x)|g'(x)|\,dx
=F(\xi)\int_\alpha^\beta|g'(x)|\,dx.
$$

Since $$g'$$ has a fixed sign, this is equivalent to

$$
\int_\alpha^\beta F(x)g'(x)\,dx
=F(\xi)(g(\beta)-g(\alpha)).
$$

Substitute into the integration-by-parts identity and use $$F(\beta)-F(\xi)=\int_\xi^\beta f$$:

$$
\begin{aligned}
\int_\alpha^\beta fg\,dx
&=g(\beta)F(\beta)-(g(\beta)-g(\alpha))F(\xi)\\
&=g(\alpha)F(\xi)+g(\beta)(F(\beta)-F(\xi))\\
&=g(\alpha)\int_\alpha^\xi f(x)\,dx
+g(\beta)\int_\xi^\beta f(x)\,dx.
\end{aligned}
$$

### Exercise 11

Use the substitution $$t=-x$$ on $$[-a,0]$$. It gives

$$
\int_{-a}^0 f(x)\,dx=\int_0^a f(-t)\,dt.
$$

If $$f$$ is odd, then $$f(-t)=-f(t)$$. Splitting the integral at zero therefore yields

$$
\int_{-a}^a f(x)\,dx
=-\int_0^a f(t)\,dt+\int_0^a f(t)\,dt=0.
$$

If $$f$$ is even, then $$f(-t)=f(t)$$, and the same splitting gives

$$
\int_{-a}^a f(x)\,dx
=\int_0^a f(t)\,dt+\int_0^a f(t)\,dt
=2\int_0^a f(t)\,dt.
$$

The reasoning applies to Banach-space-valued functions because substitution and integral additivity hold for their integrals as well.

### Exercise 12

For $$x>0$$, ordinary differentiation gives

$$
F'(x)=2x\sin(1/x^2)-\frac2x\cos(1/x^2).
$$

At zero,

$$
F'(0)=\lim_{h\to0^+}\frac{F(h)-F(0)}h
=\lim_{h\to0^+}h\sin(1/h^2)=0.
$$

Thus $$F$$ is differentiable on $$[0,1]$$. To show that $$F'$$ is not jump continuous, take $$x_n=(2\pi n)^{-1/2}$$. Then $$x_n\to0^+$$ and

$$
F'(x_n)=-\frac2{x_n}\longrightarrow-\infty,
$$

because $$\sin(1/x_n^2)=0$$ and $$\cos(1/x_n^2)=1$$. The right-hand limit of $$F'$$ at zero is not finite, so $$F'\notin S([0,1],\mathbb R)$$.

### Exercise 13

Since $$f\in C([a,b],\mathbb R)$$, it has an antiderivative $$A\in C^1([a,b],\mathbb R)$$. The oriented-integral convention gives, for every $$x\in[\alpha,\beta]$$,

$$
F(x)=\int_{g(x)}^{h(x)}f(\xi)\,d\xi=A(h(x))-A(g(x)).
$$

Both compositions on the right are continuously differentiable, so $$F\in C^1([\alpha,\beta],\mathbb R)$$. The chain rule yields

$$
F'(x)=f(h(x))h'(x)-f(g(x))g'(x).
$$

This formula also covers the case $$g(x)>h(x)$$, because the integral is oriented.

### Exercise 14

Let

$$
S(x)=\sum_{k=1}^n a_k\cos(kx),\qquad x\in[0,\pi].
$$

It is continuous, and for each positive integer $$k$$,

$$
\int_0^\pi\cos(kx)\,dx
=\left[\frac{\sin(kx)}k\right]_0^\pi=0.
$$

Consequently $$\int_0^\pi S(x)\,dx=0$$. If $$S$$ is identically zero, every interior point is a zero. Otherwise it must take both positive and negative values in the open interval: if it had only one sign there and were nonzero somewhere, continuity would make its integral strictly positive or strictly negative. By the intermediate value theorem, a zero lies between points of opposite signs. Hence some $$\alpha\in(0,\pi)$$ satisfies $$S(\alpha)=0$$.

### Exercise 15

**(i)** Rewrite the expression as

$$
n\sum_{k=n}^{2n-1}\frac1{k^2}
=\frac1n\sum_{j=0}^{n-1}\frac1{(1+j/n)^2}.
$$

This is the left-endpoint Riemann sum for $$x\mapsto(1+x)^{-2}$$ on $$[0,1]$$. Therefore

$$
\lim_{n\to\infty}n\left(\frac1{n^2}+\frac1{(n+1)^2}+\cdots+\frac1{(2n-1)^2}\right)
=\int_0^1\frac{dx}{(1+x)^2}
=\left[-\frac1{1+x}\right]_0^1
=\frac12.
$$

**(ii)** For integers $$p>q\geq1$$,

$$
\sum_{k=nq}^{np-1}\frac1k
=\frac1n\sum_{k=nq}^{np-1}\frac1{k/n}.
$$

This is the left-endpoint Riemann sum on $$[q,p]$$ for the continuous function $$x\mapsto1/x$$. Hence

$$
\lim_{n\to\infty}\sum_{k=nq}^{np-1}\frac1k
=\int_q^p\frac{dx}{x}
=\log p-\log q
=\log\frac pq.
$$

### Exercise 16

The function $$f$$ is continuous on the compact set $$I\times I$$, so it is uniformly continuous. For $$x,x'\in I$$, the norm estimate for integrals gives

$$
\begin{aligned}
\|g(x)-g(x')\|_E
&=\left\|\int_I\bigl(f(x,y)-f(x',y)\bigr)\,dy\right\|_E\\
&\leq\int_I\|f(x,y)-f(x',y)\|_E\,dy\\
&\leq(\beta-\alpha)\sup_{y\in I}\|f(x,y)-f(x',y)\|_E.
\end{aligned}
$$

Uniform continuity makes the supremum on the right tend to zero as $$x'\to x$$. Thus $$g$$ is continuous on $$I$$.
