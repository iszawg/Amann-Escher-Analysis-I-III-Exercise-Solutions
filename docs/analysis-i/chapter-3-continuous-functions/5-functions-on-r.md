# Chapter III — Continuous Functions

## 5. Functions on $$\mathbb{R}$$

In the following, $$I$$ is a compact interval containing more than one point.

### Exercise 1

Write $$I=[a,b]$$, where $$a<b$$, and set $$g(x)=f(x)-x$$. Since $$f(I)\subseteq I$$,

$$
g(a)=f(a)-a\ge0,\qquad g(b)=f(b)-b\le0.
$$

The intermediate value theorem gives some $$\xi\in[a,b]$$ with $$g(\xi)=0$$. Hence $$f(\xi)=\xi$$.

### Exercise 2

If $$x<y<z$$ in $$I$$, then $$f(y)$$ lies strictly between $$f(x)$$ and $$f(z)$$. Otherwise, for example if $$f(y)>\max\{f(x),f(z)\}$$, choose a value strictly between $$f(y)$$ and that maximum. The intermediate value theorem on both $$[x,y]$$ and $$[y,z]$$ would give two distinct preimages, contradicting injectivity. The case $$f(y)<\min\{f(x),f(z)\}$$ is the same.

Choose $$a<b$$ in $$I$$. If $$f(a)<f(b)$$, this betweenness property forces the same order throughout $$I$$: values to the left of $$a$$ are below $$f(a)$$, values between $$a$$ and $$b$$ lie between $$f(a)$$ and $$f(b)$$, and values to the right of $$b$$ are above $$f(b)$$. Applying the property again to triples within each of these regions shows that $$x<y$$ always implies $$f(x)<f(y)$$. Thus $$f$$ is strictly increasing. If $$f(a)>f(b)$$, the same argument shows that $$f$$ is strictly decreasing.

### Exercise 3

Each connected component $$J$$ of the open set $$D\subseteq\mathbb{R}$$ is an open interval. The restriction of $$f$$ to every compact subinterval of $$J$$ is continuous and injective, so Exercise 2 shows it is strictly monotone. The direction is consistent on overlapping subintervals; hence $$f|_J$$ is strictly monotone.

Let $$U$$ be open in $$D$$. Its intersection with each component $$J$$ is a union of open intervals. A continuous strictly monotone function maps each such interval to an open interval: its image is an interval, and neither endpoint is attained. Therefore $$f(U)$$ is open in $$\mathbb{R}$$. So $$f:D\to f(D)$$ is a continuous, open bijection. Its inverse is continuous, and $$f$$ is a homeomorphism onto its image.

### Exercise 4

Because $$\sum_{n=1}^{\infty}y_n<\infty$$ and each $$y_n>0$$, every subseries in the definition of $$f$$ converges. If $$x<y$$, choose a rational $$q\in(x,y)$$ and let $$n=\alpha^{-1}(q)$$. Then $$n\in N_y\setminus N_x$$, so

$$
f(y)-f(x)=\sum_{k\in N_y\setminus N_x}y_k\ge y_n>0.
$$

Thus $$f$$ is strictly increasing.

Now let $$x$$ be irrational and fix $$\varepsilon>0$$. Choose $$N$$ so that $$\sum_{k>N}y_k<\varepsilon$$. The finitely many rationals $$\alpha(1),\ldots,\alpha(N)$$ are all different from $$x$$, so there is a $$\delta>0$$ such that none lies between $$x$$ and any $$t$$ with $$|t-x|<\delta$$. For those $$t$$, membership in $$N_t$$ and $$N_x$$ agrees for every $$k\le N$$. Hence

$$
|f(t)-f(x)|\le\sum_{k>N}y_k<\varepsilon,
$$

which proves continuity at every irrational number.

Let $$q=\alpha(n)$$ be rational. Summability of $$(y_k)$$ gives the one-sided limits

$$
f(q-)=\sum_{\alpha(k)<q}y_k,\qquad f(q+)=\sum_{\alpha(k)\le q}y_k.
$$

Their difference is $$f(q+)-f(q-)=y_n$$. Thus $$f$$ has a jump discontinuity of size $$y_n$$ at $$q$$.

### Exercise 5

**(a)** Rationals map to themselves by the identity rule, and irrationals map to irrationals under $$x\mapsto1-x$$. Applying $$f$$ twice returns every point to itself, so $$f$$ is a bijection.

**(b)** Consider any nondegenerate subinterval. It contains a nondegenerate subinterval lying wholly below or wholly above $$1/2$$. In either case, it contains two rationals $$r<s$$, and $$f(r)=r<s=f(s)$$, so $$f$$ cannot be decreasing there.

If the subinterval lies below $$1/2$$, choose an irrational $$u$$ and a rational $$v$$ in it with $$u<v$$. Then $$u+v<1$$, so $$f(u)=1-u>v=f(v)$$. If it lies above $$1/2$$, choose a rational $$u$$ and an irrational $$v$$ with $$u<v$$. Now $$u+v>1$$, and again $$f(u)=u>1-v=f(v)$$. Thus $$f$$ cannot be increasing on any nondegenerate subinterval either.

**(c)** At $$x=1/2$$, both branches tend to $$1/2$$, so $$f$$ is continuous there. For any other $$x\in[0,1]$$, take rational and irrational sequences in $$[0,1]$$ tending to $$x$$ (one-sided at an endpoint). Their images tend respectively to $$x$$ and $$1-x$$, which are distinct. Thus $$f$$ is discontinuous at every $$x\ne1/2$$.

### Exercise 6

Write $$f_n(x)=4^{-n}f_0(4^n x)$$, so $$F=\sum_{n=0}^{\infty}f_n$$. The function $$f_0=\operatorname{zigzag}$$ is the distance to the nearest integer. In particular, $$0\le f_0\le1/2$$, it is continuous and $$1$$-Lipschitz, and $$f_0(t)=|t|$$ when $$|t|\le1/2$$.

**(a)** For every $$x\in\mathbb{R}$$,

$$
0\le4^{-n}f_0(4^n x)\le\tfrac12 4^{-n}.
$$

The majorant is summable, so the series defining $$F(x)$$ converges for every $$x$$.

**(b)** Fix $$m\in\mathbb{N}^{\times}$$, $$k\in\mathbb{Z}$$, and set $$a=k4^{-m}$$ and $$h=4^{-2m-1}$$. For $$n<m$$, the Lipschitz bound gives

$$
f_n(a\pm h)-f_n(a)\ge-h.
$$

For $$m\le n\le2m$$, $$4^na$$ is an integer and $$4^nh\le1/4$$. Hence $$f_n(a)=0$$ and $$f_n(a\pm h)=h$$. For $$n\ge2m+1$$, both $$4^na$$ and $$4^n(a\pm h)$$ are integers, so $$f_n(a)=f_n(a\pm h)=0$$. Summing these contributions yields

$$
F(a\pm h)-F(a)\ge -mh+(m+1)h=h.
$$

Every nondegenerate interval contains such an $$a$$ with both $$a-h$$ and $$a+h$$ in the interval: choose $$m$$ large and take a grid point $$k4^{-m}$$ near its midpoint. Thus the function rises from $$a-h$$ to $$a$$ and also from $$a$$ to $$a+h$$. It can be neither increasing nor decreasing on that interval.

**(c)** Each $$f_n$$ is continuous, and

$$
\sup_{x\in\mathbb{R}}|f_n(x)|\le\tfrac12 4^{-n}.
$$

The Weierstrass M-test gives uniform convergence of $$\sum_{n=0}^{\infty}f_n$$. Therefore its sum $$F$$ is continuous.

### Exercise 7

For a function on $$I$$, the oscillation at $$x$$ is

$$
\omega_f(x)=\inf_{\varepsilon>0}\ \sup_{y,z\in I\cap(x-\varepsilon,x+\varepsilon)}|f(y)-f(z)|.
$$

Suppose first that $$f$$ is increasing. Its one-sided limits exist. Write $$L=f(x-)$$ and $$R=f(x+)$$; at an endpoint, interpret the unavailable one-sided value as $$f(x)$$. As $$\varepsilon\downarrow0$$, the infimum and supremum of the values of $$f$$ on $$I\cap(x-\varepsilon,x+\varepsilon)$$ tend to $$L$$ and $$R$$, respectively. The diameter of that range is its supremum minus its infimum. Consequently,

$$
\omega_f(x)=R-L=f(x+)-f(x-).
$$

If $$f$$ is decreasing, apply the increasing case to $$-f$$. Oscillation is unchanged by negating the function, and the difference of its one-sided limits becomes $$|f(x+)-f(x-)|$$. Hence in both cases

$$
\omega_f(x)=|f(x+)-f(x-)|.
$$
