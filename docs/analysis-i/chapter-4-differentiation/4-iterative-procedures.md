# Chapter IV — Differentiation in One Variable

## 4. Iterative Procedures

### Exercise 1

Because $$q_n\to0$$, choose $$N\in\mathbb N^\times$$ such that $$q_N<1$$. The iterate $$g:=f^N$$ maps the complete metric space $$X$$ into itself and satisfies

$$
d(g(x),g(y))\le q_Nd(x,y),\qquad x,y\in X.
$$

Thus $$g$$ is a contraction. By the Banach fixed point theorem, it has a unique fixed point $$a\in X$$. Since iterates of the same map commute,

$$
g(f(a))=f(g(a))=f(a),
$$

so $$f(a)$$ is also a fixed point of $$g$$. Uniqueness gives $$f(a)=a$$. Hence $$f$$ has a fixed point.

### Exercise 2

Fix $$\lambda_0\in\Lambda$$. For each parameter $$\lambda$$, let $$x(\lambda)$$ be the unique fixed point of $$f(\cdot,\lambda)$$. Using the contraction bound with the same parameter $$\lambda$$ in both terms gives

$$
\begin{aligned}
d(x(\lambda),x(\lambda_0))
&=d(f(x(\lambda),\lambda),f(x(\lambda_0),\lambda_0))\\
&\le d(f(x(\lambda),\lambda),f(x(\lambda_0),\lambda))
  +d(f(x(\lambda_0),\lambda),f(x(\lambda_0),\lambda_0))\\
&\le \alpha d(x(\lambda),x(\lambda_0))
  +d(f(x(\lambda_0),\lambda),f(x(\lambda_0),\lambda_0)).
\end{aligned}
$$

Therefore

$$
d(x(\lambda),x(\lambda_0))\le \frac{1}{1-\alpha}
d(f(x(\lambda_0),\lambda),f(x(\lambda_0),\lambda_0)).
$$

The last term tends to zero as $$\lambda\to\lambda_0$$ because $$f$$ is continuous on $$X\times\Lambda$$. Thus $$\lambda\mapsto x(\lambda)$$ is continuous at every $$\lambda_0\in\Lambda$$.

### Exercise 3

A fixed point is a zero of

$$
h(x):=e^{x-1}-e^{1-x}-x.
$$

Its derivative satisfies

$$
h'(x)=e^{x-1}+e^{1-x}-1\ge 1,
$$

by the arithmetic-geometric mean inequality. Hence $$h$$ is strictly increasing. Also, $$h(1)=-1<0$$ and $$h(2)=e-e^{-1}-2>0$$, so the intermediate value theorem gives exactly one zero, which is the unique fixed point.

Newton's method is

$$
x_{k+1}=x_k-\frac{e^{x_k-1}-e^{1-x_k}-x_k}{e^{x_k-1}+e^{1-x_k}-1}.
$$

Starting at $$x_0=2$$ gives $$x_1\approx1.8320348516$$, $$x_2\approx1.8142682083$$, and $$x_3\approx1.8140968120$$. Thus

$$
x^*\approx1.8140967963.
$$

### Exercise 4

Let $$p(x)=x^3-2x-5$$. Its critical points are $$\pm\sqrt{2/3}$$, and $$p$$ is negative at both: the local maximum is $$\frac43\sqrt{2/3}-5<0$$, while the local minimum is $$-\frac43\sqrt{2/3}-5<0$$. Since $$p(x)\to\infty$$ as $$x\to\infty$$ and $$p(x)\to-\infty$$ as $$x\to-\infty$$, there is exactly one real zero.

Newton's method reads

$$
x_{k+1}=x_k-\frac{x_k^3-2x_k-5}{3x_k^2-2}.
$$

With $$x_0=2$$, the first iterates are $$2.1$$, $$2.0945681211$$, and $$2.0945514817$$. Therefore the real zero is approximately

$$
x\approx2.0945514815.
$$

### Exercise 5

Each equation has a unique least positive solution in the indicated interval. The approximate values can be obtained by bisection or Newton's method.

| Equation | Interval containing the least positive solution | Approximation |
| --- | --- | --- |
| $$x\tan x=1$$ | $$(0,\pi/2)$$ | $$0.8603335890$$ |
| $$x^3+e^{-x}=2$$ | $$(1,2)$$ | $$1.1926857650$$ |
| $$x-\cos^2x=0$$ | $$(0,1)$$ | $$0.6417143709$$ |
| $$2\cos x=x^2$$ | $$(0,\pi/2)$$ | $$1.0216899541$$ |

For the first equation, $$x\tan x$$ increases strictly from zero to infinity on $$(0,\pi/2)$$. For the second, $$g(x)=x^3+e^{-x}-2$$ satisfies $$g(0)<0$$ and tends to infinity; its derivative $$g'(x)=3x^2-e^{-x}$$ is strictly increasing for $$x\ge0$$, so $$g$$ first decreases and then increases and has just one positive zero. For the third, $$x-\cos^2x$$ is negative at zero and positive at one, and its derivative $$1+\sin(2x)$$ is positive on $$(0,1)$$. For the fourth, $$2\cos x-x^2$$ decreases strictly on $$(0,\pi/2)$$ from a positive to a negative value.

### Exercise 6

Write

$$
P_n(x):=\sum_{k=0}^n\frac{x^k}{k!}.
$$

If $$n$$ is odd, then $$P_n'=P_{n-1}$$, where $$n-1$$ is even. For $$x\ge0$$ all terms in $$P_{n-1}(x)$$ are nonnegative and the constant term is one. For $$x<0$$, Taylor's theorem for $$e^x$$ with the remainder after degree $$n-1$$ gives $$e^x=P_{n-1}(x)+e^{\xi}x^n/n!$$ for some $$\xi$$ between $$0$$ and $$x$$. Since $$n$$ is odd, the remainder is negative, so $$P_{n-1}(x)>e^x>0$$. Thus $$P_n$$ is strictly increasing. Its leading term implies $$P_n(x)\to-\infty$$ as $$x\to-\infty$$, while $$P_n(0)=1$$. It therefore has exactly one real zero, and that zero is negative.

For any fixed odd $$n$$, bisect an interval $$[-R,0]$$ with $$P_n(-R)<0$$; such an $$R$$ exists because $$P_n(x)\to-\infty$$. Newton's iteration is also well-defined because $$P_{n-1}(x)>0$$:

$$
x_{j+1}=x_j-\frac{P_n(x_j)}{P_{n-1}(x_j)}.
$$

The following values illustrate the zeros for the first several odd degrees:

| $$n$$ | Approximate zero of $$P_n$$ |
| ---: | ---: |
| 1 | $$-1.000000$$ |
| 3 | $$-1.596072$$ |
| 5 | $$-2.180607$$ |
| 7 | $$-2.759003$$ |
| 9 | $$-3.333551$$ |
| 11 | $$-3.905452$$ |
| 13 | $$-4.475412$$ |
| 15 | $$-5.043887$$ |

### Exercise 7

First suppose $$f(a)<0<f(b)$$ and let $$\xi$$ be the zero of $$f$$ in $$[a,b]$$. Convexity and the endpoint signs imply that this zero is unique. If $$f(x_0)>0$$, then $$x_0>\xi$$ and $$m:=f'(x_0)>0$$. The supporting-line inequality for a differentiable convex function is

$$
f(x)\ge f(x_0)+m(x-x_0).
$$

At $$x=\xi$$ this gives $$0\ge f(x_0)+m(\xi-x_0)$$, hence $$x_1=x_0-f(x_0)/m\ge\xi$$. Also $$x_1<x_0$$, and evaluating the supporting line at $$x_1$$ shows $$f(x_1)\ge0$$. Inductively, $$\xi\le x_{n+1}<x_n$$ and $$f(x_n)\ge0$$. Thus $$x_n$$ decreases to some $$L\ge\xi$$. Since

$$
x_n-x_{n+1}=\frac{f(x_n)}m\longrightarrow0,
$$

continuity gives $$f(L)=0$$, so $$L=\xi$$.

If instead $$f(a)>0>f(b)$$, reflect the variable by setting $$g(t):=f(-t)$$ on $$[-b,-a]$$. Then $$g$$ is convex, $$g(-b)<0<g(-a)$$, and the initial condition $$f(x_0)>0$$ becomes $$g(-x_0)>0$$. The iteration for $$g$$ is exactly the reflection of the iteration for $$f$$. The first case therefore shows that $$-x_n$$ converges to the zero of $$g$$, so $$x_n$$ converges to the zero of $$f$$.

For a concave function, the guaranteed starting side is reversed: the method converges when $$f(x_0)<0$$ (and it stops immediately when $$f(x_0)=0$$). For example, if $$f(a)<0<f(b)$$, a starting point with $$f(x_0)<0$$ lies to the left of the zero and has $$m=f'(x_0)>0$$. The tangent-line inequality is now $$f(x)\le f(x_0)+m(x-x_0)$$. At each iterate between $$x_0$$ and $$\xi$$, concavity makes the secant slope to $$\xi$$ lie between zero and $$m$$; hence $$x_n\le x_{n+1}\le\xi$$. The iterates increase, remain bounded by $$\xi$$, and their limit is a zero. When $$f(a)>0>f(b)$$, the corresponding argument gives $$\xi\le x_{n+1}\le x_n$$.

There is no general guarantee from a positive starting value in the concave case. For instance, $$f(x)=1-x^2$$ on $$[-2,0]$$ is concave and satisfies $$f(-2)<0<f(0)$$. With $$x_0=-0.1$$, the first simplified Newton step is $$x_1=-0.1-0.99/0.2=-5.05$$, outside the interval.

### Exercise 8

The line through $$(a_n,f(a_n))$$ and $$(b_n,f(b_n))$$ has slope $$\bigl(f(b_n)-f(a_n)\bigr)/(b_n-a_n)$$. Its zero is

$$
c_{n+1}=a_n-\frac{b_n-a_n}{f(b_n)-f(a_n)}f(a_n).
$$

Thus each step takes the zero of the secant line and keeps the subinterval whose endpoint values have opposite signs. In particular, $$a_n$$ is nondecreasing, $$b_n$$ is nonincreasing, and every interval $$[a_n,b_n]$$ contains a zero by the intermediate value theorem. If some $$f(c_n)=0$$, the procedure has already found a zero.

For continuous $$f$$, the regula falsi convergence theorem gives convergence of the secant intercepts $$c_n$$ to a zero. The case where the interval lengths tend to zero follows directly from nested intervals and continuity. If one endpoint is eventually fixed, the other endpoint is the secant intercept at every later step; its monotone limit is a zero by continuity and the secant formula. In the remaining case, endpoints move alternately. At every step the secant formula gives

$$
|f(a_n)|(b_n-c_{n+1})=|f(b_n)|(c_{n+1}-a_n)
$$

At successive sign changes, the negative-residual intercepts form an increasing subsequence and the positive-residual intercepts form a decreasing one. The identity compares their distances to the opposite endpoints; together with the nested brackets, it rules out distinct limits for the two subsequences. Their common limit is a zero by continuity. This alternating-endpoint case is the technical part of the general continuity-only theorem; a full proof is given in [Nguyen, “The convergence of the Regula Falsi method”](https://arxiv.org/abs/2109.03523).

If $$f(a)>0>f(b)$$, the secant-zero formula is unchanged. Reverse the endpoint update: set $$a_{n+1}=c_{n+1}$$ and $$b_{n+1}=b_n$$ when $$f(c_{n+1})\ge0$$; otherwise set $$a_{n+1}=a_n$$ and $$b_{n+1}=c_{n+1}$$.

### Exercise 9

Define, for $$x\ne0$$,

$$
g(x):=x^5e^{|x|}-\frac{x^2}{\pi}\sin\bigl(\log(x^2)\bigr)+1998.
$$

The function is continuous on $$[-3,-2]$$. Direct evaluation gives $$g(-3)\approx-2885.1063<0$$ and $$g(-2)\approx1760.2986>0$$, so it has a zero in that interval. Bisection (or a safeguarded Newton iteration) gives

$$
x\approx-2.6764301338.
$$

### Exercise 10

Since $$f$$ is a contraction, there is a constant $$q<1$$ with $$d(f(x),f(y))\le qd(x,y)$$. Taking difference quotients shows $$|f'(x)|\le q$$ wherever the derivative is defined. The derivative is continuous and never zero on the interval, so it has constant sign. Hence $$f$$ is strictly monotone and injective.

**(a)** Suppose $$f^n(x_0)=x^*$$ for some $$n\ge1$$. Since $$f(x^*)=x^*$$ and $$f$$ is injective, $$f(f^{n-1}(x_0))=f(x^*)$$ implies $$f^{n-1}(x_0)=x^*$$. Repeating this argument gives $$x_0=x^*$$, contrary to the hypothesis. Therefore $$f^n(x_0)\ne x^*$$ for every $$n\ge1$$.

**(b)** Put $$y_n=f^n(x_0)$$. By the contraction theorem, $$y_n\to x^*$$, and part (a) ensures $$y_n-x^*\ne0$$. Therefore

$$
\frac{f^{n+1}(x_0)-x^*}{f^n(x_0)-x^*}
=\frac{f(y_n)-f(x^*)}{y_n-x^*}
\longrightarrow f'(x^*),
$$

by the definition of the derivative.
