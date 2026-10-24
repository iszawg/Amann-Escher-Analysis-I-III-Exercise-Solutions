# Chapter VI — Integral Calculus in One Variable

## 9. The gamma function

### Exercise 1

The functional equation $$\Gamma(z+1)=z\Gamma(z)$$ and the Gaussian integral value $$\Gamma(1/2)=\sqrt\pi$$ give, by iterating the recurrence,

$$
\begin{aligned}
\Gamma\left(n+\frac12\right)
&=\left(n-\frac12\right)\left(n-\frac32\right)\cdots\frac12\,\Gamma\left(\frac12\right)\\
&=\sqrt\pi\prod_{k=1}^n\frac{2k-1}{2}
=\frac{1\cdot3\cdots(2n-1)}{2^n}\sqrt\pi.
\end{aligned}
$$

This proves the identity for every $$n\in\mathbb N^\times$$.

### Exercise 2

Fix a compact set $$K\subset\{z\in\mathbb C:\operatorname{Re}z>0\}$$, and choose $$0<a\le b$$ with $$a\le\operatorname{Re}z\le b$$ for all $$z\in K$$. For each integer $$m\ge0$$, the proposed $$m$$th derivative of the integrand is $$t^{z-1}(\log t)^m e^{-t}$$.

On $$0<t\le1$$ its absolute value is at most $$t^{a-1}|\log t|^m$$, which is integrable at zero because $$a>0$$. On $$t\ge1$$ it is at most $$t^{b-1}(\log t)^m e^{-t}$$, which is integrable at infinity. These bounds hold uniformly for $$z\in K$$. Differentiation under the integral sign is therefore valid, locally uniformly in $$z$$, at every order. Hence $$\Gamma$$ is infinitely differentiable (indeed analytic) on the right half-plane, and

$$
\Gamma^{(m)}(z)=\int_0^\infty t^{z-1}(\log t)^m e^{-t}\,dt,
\qquad \operatorname{Re}z>0.
$$

The representation agrees with the gamma integral in (9.4), and the same conclusion on $$\mathbb C\setminus(-\mathbb N)$$ follows from the meromorphic continuation of $$\Gamma$$ and its functional equation.

### Exercise 3

Write $$C$$ for the Euler–Mascheroni constant. We use $$\Gamma(1)=1$$, the functional equation, and the logarithmic derivative formulas in Proposition 9.8.

#### (i)

By Exercise 2 with $$m=1$$ and $$z=1$$,

$$
\int_0^\infty e^{-t}\log t\,dt=\Gamma'(1).
$$

Formula (9.15) at $$z=1$$ gives $$\Gamma'(1)/\Gamma(1)=-C$$: the terms after $$-C-1$$ sum to zero. Since $$\Gamma(1)=1$$, the integral is $$-C$$.

#### (ii)

Differentiate $$\Gamma(x+1)=x\Gamma(x)$$ to obtain $$\Gamma'(x+1)=\Gamma(x)+x\Gamma'(x)$$. At $$x=1$$, this yields $$\Gamma'(2)=1-C$$. Thus, by Exercise 2,

$$
\int_0^\infty e^{-t}t\log t\,dt=\Gamma'(2)=1-C.
$$

#### (iii)

For integers $$n\ge1$$, set $$A_n=\Gamma'(n)/(n-1)!$$. The differentiated functional equation gives

$$
A_{n+1}=\frac{\Gamma'(n+1)}{n!}
=\frac{\Gamma(n)+n\Gamma'(n)}{n!}
=\frac1n+A_n.
$$

Part (i) says $$A_1=-C$$. Iterating the recurrence gives $$A_n=\sum_{k=1}^{n-1}1/k-C$$. Applying the integral formula from Exercise 2 at $$z=n$$ proves

$$
\int_0^\infty e^{-t}t^{n-1}\log t\,dt
=(n-1)!\left(\sum_{k=1}^{n-1}\frac1k-C\right),
\qquad n\ge2.
$$

#### (iv)

Let $$\psi=\Gamma'/\Gamma$$. Since $$\Gamma''/\Gamma=\psi'+\psi^2$$, formula (9.16) at $$z=1$$ gives

$$
\psi'(1)=\sum_{k=0}^\infty\frac1{(1+k)^2}
=\sum_{j=1}^\infty\frac1{j^2}=\frac{\pi^2}{6}.
$$

Part (i) gives $$\psi(1)=-C$$, and $$\Gamma(1)=1$$. Therefore

$$
\Gamma''(1)=\Gamma(1)\bigl(\psi'(1)+\psi(1)^2\bigr)
=\frac{\pi^2}{6}+C^2.
$$

The integral formula in Exercise 2 identifies this with $$\int_0^\infty e^{-t}(\log t)^2\,dt$$, as required.

### Exercise 4

For $$\operatorname{Re}z>0$$, use the substitution $$t=e^{-s}$$ in the integral on the right. Since $$dt=-e^{-s}\,ds$$ and $$-\log t=s$$, first on truncated intervals and then by taking endpoint limits,

$$
\begin{aligned}
\int_0^1(-\log t)^{z-1}\,dt
&=\int_\infty^0 s^{z-1}(-e^{-s})\,ds\\
&=\int_0^\infty s^{z-1}e^{-s}\,ds\\
&=\Gamma(z).
\end{aligned}
$$

For positive $$s$$, the complex power means $$s^{z-1}=e^{(z-1)\log s}$$ with the real logarithm. The integral converges near zero because $$\operatorname{Re}z>0$$, and at infinity because of the exponential factor.

### Exercise 5

Let $$f,g$$ be positive log-convex functions on the same interval. Their product is positive, and

$$
\log(fg)=\log f+\log g.
$$

The sum of two convex functions is convex, so $$\log(fg)$$ is convex. Therefore $$fg$$ is log convex.

### Exercise 6

The gamma function is positive and log convex on $$(0,\infty)$$. Define

$$
h(x)=\log\frac{\Gamma(x)}{f(x)},\qquad x>0.
$$

The recurrence for $$f$$ and the functional equation for $$\Gamma$$ imply $$h(x+1)=h(x)$$. Thus both $$h$$ and $$h'$$ are 1-periodic. Also, $$h(1)=0$$.

Set $$u=\log\Gamma$$ and $$v=\log f$$. Both are differentiable and convex, so $$u'$$ and $$v'$$ are nondecreasing. Differentiating their functional equations gives

$$
u'(x+1)-u'(x)=v'(x+1)-v'(x)=\frac1x.
$$

For $$0<y\le1$$, monotonicity therefore gives

$$
0\le u'(x+y)-u'(x)\le\frac1x,
\qquad
0\le v'(x+y)-v'(x)\le\frac1x.
$$

Subtracting these increments yields

$$
-\frac1x\le h'(x+y)-h'(x)\le\frac1x.
$$

Replace $$x$$ by $$x+n$$ for an integer $$n\ge1$$. Periodicity of $$h'$$ leaves the middle expression unchanged, while the bound becomes $$1/(x+n)$$. Letting $$n\to\infty$$ shows $$h'(x+y)=h'(x)$$ for every $$0<y\le1$$. Hence $$h'$$ is constant on $$(0,\infty)$$. Since $$h$$ is 1-periodic, that constant must be zero. Thus $$h$$ is constant, and $$h(1)=0$$ forces $$h\equiv0$$. Consequently,

$$
f(x)=\Gamma(x)\qquad(x>0).
$$

### Exercise 7

Define $$H(x)=2^x\Gamma(x/2)\Gamma((x+1)/2)$$ for $$x>0$$. The logarithm of $$H$$ is the sum of the linear function $$x\log2$$ and two affine compositions of $$\log\Gamma$$. Since $$\log\Gamma$$ is convex on $$(0,\infty)$$, $$H$$ is positive and log convex.

Using $$\Gamma(z+1)=z\Gamma(z)$$,

$$
\begin{aligned}
H(x+1)
&=2^{x+1}\Gamma\left(\frac{x+1}{2}\right)
\Gamma\left(\frac{x+2}{2}\right)\\
&=2^{x+1}\Gamma\left(\frac{x+1}{2}\right)\frac{x}{2}\Gamma\left(\frac{x}{2}\right)
=xH(x).
\end{aligned}
$$

Also, $$H(1)=2\Gamma(1/2)\Gamma(1)=2\sqrt\pi$$. Hence $$H/(2\sqrt\pi)$$ satisfies all the hypotheses of Exercise 6, so $$H(x)=2\sqrt\pi\,\Gamma(x)$$. Dividing by $$2^x$$ proves the duplication formula:

$$
\Gamma\left(\frac{x}{2}\right)\Gamma\left(\frac{x+1}{2}\right)
=2^{1-x}\sqrt\pi\,\Gamma(x),\qquad x>0.
$$

### Exercise 8

The product representation of the gamma function in Proposition 9.5 gives, for $$-1<x<1$$,

$$
\log\Gamma(1+x)
=-Cx+\sum_{n=1}^\infty\left(\frac{x}{n}-\log\left(1+\frac{x}{n}\right)\right).
$$

For every $$n\ge1$$, expand the logarithm:

$$
\frac{x}{n}-\log\left(1+\frac{x}{n}\right)
=\sum_{k=2}^\infty\frac{(-1)^k}{k}\frac{x^k}{n^k}.
$$

The double series is absolutely convergent because

$$
\sum_{k=2}^\infty\frac{|x|^k}{k}\sum_{n=1}^\infty\frac1{n^k}
=\sum_{k=2}^\infty\frac{\zeta(k)|x|^k}{k}<\infty
\qquad(|x|<1).
$$

We may therefore interchange the sums. Summing first over $$n$$ yields

$$
\log\Gamma(1+x)=-Cx+\sum_{k=2}^\infty(-1)^k\frac{\zeta(k)}{k}x^k,
\qquad -1<x<1.
$$

### Exercise 9

The reflection formula (Theorem 9.6) states that

$$
\Gamma(x)\Gamma(1-x)=\frac{\pi}{\sin(\pi x)},\qquad 0<x<1.
$$

Taking logarithms and integrating over $$(0,1)$$ is legitimate: near zero, $$\Gamma(x)=\Gamma(1+x)/x$$, so $$\log\Gamma(x)=-\log x+O(1)$$; the corresponding behavior near one follows by reflection. These logarithmic endpoint singularities are integrable. Substitution $$x\mapsto1-x$$ shows that the two gamma terms have equal integrals. Therefore, writing $$I=\int_0^1\log\Gamma(x)\,dx$$, we obtain

$$
2I=\log\pi-\int_0^1\log(\sin(\pi x))\,dx.
$$

With $$u=\pi x$$, the last integral equals $$\pi^{-1}\int_0^\pi\log(\sin u)\,du=-\log2$$; the value of the latter integral was established in Exercise 3 of Section 8. Thus $$2I=\log\pi+\log2=\log(2\pi)$$, and

$$
\int_0^1\log\Gamma(x)\,dx=\frac12\log(2\pi)=\log\sqrt{2\pi}.
$$

### Exercise 10

Use the substitution $$x=a+(b-a)\sin^2\theta$$, where $$0<\theta<\pi/2$$. Then

$$
dx=2(b-a)\sin\theta\cos\theta\,d\theta,
\qquad
\sqrt{(x-a)(b-x)}=(b-a)\sin\theta\cos\theta.
$$

Applying this substitution first away from the endpoints and then taking the improper limits gives

$$
\int_a^b\frac{dx}{\sqrt{(x-a)(b-x)}}
=2\int_0^{\pi/2}d\theta=\pi.
$$

### Exercise 11

Fix $$q>0$$ and set $$w_p(t)=t^{p-1}(1-t)^{q-1}$$ for $$0<t<1$$ and $$p>0$$. If $$p$$ ranges over a compact subinterval $$[a,b]\subset(0,\infty)$$, then near zero the derivatives in $$p$$ of orders $$m=0,1,2$$ are bounded by a constant times $$t^{a-1}|\log t|^m$$. Near one they are bounded by a constant times $$(1-t)^{q-1}$$, since $$\log t$$ stays bounded there. These are integrable bounds, so differentiation under the integral sign gives

$$
B_p(p,q)=\int_0^1w_p(t)\log t\,dt,
\qquad
B_{pp}(p,q)=\int_0^1w_p(t)(\log t)^2\,dt.
$$

In particular, $$p\mapsto B(p,q)$$ is differentiable. To prove log convexity, normalize $$w_p(t)\,dt$$ to a probability measure $$d\mu_p(t)=w_p(t)\,dt/B(p,q)$$. Then

$$
\begin{aligned}
\frac{d^2}{dp^2}\log B(p,q)
&=\frac{B_{pp}(p,q)}{B(p,q)}
-\left(\frac{B_p(p,q)}{B(p,q)}\right)^2\\
&=\int_0^1(\log t)^2\,d\mu_p(t)
-\left(\int_0^1\log t\,d\mu_p(t)\right)^2\\
&=\int_0^1\left(\log t-\int_0^1\log s\,d\mu_p(s)\right)^2d\mu_p(t)\ge0.
\end{aligned}
$$

Thus $$\log B(p,q)$$ is convex in $$p$$, as required.

### Exercise 12

For $$p,q>0$$, the identity $$1=t+(1-t)$$ gives

$$
B(p,q)=B(p+1,q)+B(p,q+1).
$$

Also, integrate the derivative of $$t^p(1-t)^q$$ from zero to one. Its endpoint values vanish because $$p,q>0$$, so

$$
0=pB(p,q+1)-qB(p+1,q).
$$

Consequently, $$B(p,q+1)=\frac{q}{p}B(p+1,q)$$. Substituting this into the first identity yields

$$
B(p,q)=\left(1+\frac qp\right)B(p+1,q),
$$

and therefore

$$
B(p+1,q)=\frac{p}{p+q}B(p,q).
$$

### Exercise 13

Fix $$q>0$$ and define

$$
f(p)=B(p,q)\frac{\Gamma(p+q)}{\Gamma(q)},\qquad p>0.
$$

Exercise 11 shows that $$B(p,q)$$ is positive, differentiable and log convex in $$p$$. The gamma function is also positive, differentiable and log convex on $$(0,\infty)$$. Since $$\log f$$ is the sum of the logarithms of these two log-convex factors and a constant, $$f$$ is positive, differentiable and log convex.

By Exercise 12 and the gamma functional equation,

$$
\begin{aligned}
f(p+1)
&=B(p+1,q)\frac{\Gamma(p+q+1)}{\Gamma(q)}\\
&=\frac{p}{p+q}B(p,q)\frac{(p+q)\Gamma(p+q)}{\Gamma(q)}
=pf(p).
\end{aligned}
$$

Moreover, $$B(1,q)=\int_0^1(1-t)^{q-1}\,dt=1/q$$, so $$f(1)=B(1,q)\Gamma(q+1)/\Gamma(q)=1$$. Exercise 6 now gives $$f(p)=\Gamma(p)$$ for all $$p>0$$. Rearranging proves

$$
B(p,q)=\frac{\Gamma(p)\Gamma(q)}{\Gamma(p+q)},
\qquad p,q>0.
$$
