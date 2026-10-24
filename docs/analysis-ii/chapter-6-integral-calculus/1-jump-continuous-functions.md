# 1. Jump Continuous Functions

Throughout, let $$I=[\alpha,\beta]$$ be a compact interval and let $$E$$ be a Banach space, as in the section. A function is jump continuous when its finite one-sided limits exist at the relevant points; the limits need not equal its values at the points.

### Exercise 1

By Theorem 1.4, $$S(I,\mathbb K)$$ is complete in the supremum norm. It remains to check multiplication and the algebra norm.

Take $$f,g\in S(I,\mathbb K)$$. At any point where a one-sided limit is required, both $$f$$ and $$g$$ have one-sided limits, so

$$
\lim_{y\to x\pm0} f(y)g(y)
=\left(\lim_{y\to x\pm0}f(y)\right)
\left(\lim_{y\to x\pm0}g(y)\right).
$$

Thus $$fg\in S(I,\mathbb K)$$. Pointwise multiplication is associative and distributive because multiplication in $$\mathbb K$$ has these properties. Also,

$$
\|fg\|_\infty
=\sup_{x\in I}|f(x)g(x)|
\leq \|f\|_\infty\|g\|_\infty.
$$

The constant function $$\mathbf 1(x)=1$$ is jump continuous and satisfies $$\mathbf 1f=f\mathbf 1=f$$. Hence $$S(I,\mathbb K)$$ is a unital Banach algebra.

### Exercise 2

Write the value on each of the two intervals indexed by $$n$$ as $$1/(n+2)$$, with $$f(0)=0$$.

**(a)** The function is not a staircase function. For every integer $$n\geq2$$, the left and right limits at $$x=1/n$$ are

$$
\lim_{x\to(1/n)^-}f(x)=\frac1{n+2},
\qquad
\lim_{x\to(1/n)^+}f(x)=\frac1{n+1}.
$$

They differ, so each $$1/n$$ is a discontinuity. A staircase function can be discontinuous only at the finitely many points of one of its partitions. Since there are infinitely many such points $$1/n$$, $$f\notin T([-1,1],\mathbb R)$$.

**(b)** The function is jump continuous. Away from $$0$$, it is constant between the successive points $$\pm1/n$$, so all one-sided limits there exist. As $$x\to0$$, the interval index $$n$$ tends to infinity and the values $$1/(n+2)$$ tend to $$0$$. Consequently,

$$
\lim_{x\to0^-}f(x)=\lim_{x\to0^+}f(x)=0.
$$

Thus $$f\in S([-1,1],\mathbb R)$$, even though it is not a staircase function.

### Exercise 3

The set $$SC(I,E)$$ is a vector subspace: sums and scalar multiples of functions with finitely many discontinuities still have only finitely many discontinuities. It is not closed in $$S(I,E)$$.

Use the function $$f$$ from Exercise 2. It has a discontinuity at every $$1/n$$ for $$n\geq2$$, so $$f\notin SC([-1,1],\mathbb R)$$. For each positive integer $$N$$, define

$$
g_N(x)=
\begin{cases}
f(x),& |x|\geq 1/N,\\
0,& |x|<1/N.
\end{cases}
$$

Outside the central interval, only finitely many of the intervals defining $$f$$ occur. Inside it, $$g_N$$ is constant. Thus $$g_N$$ is a staircase function and in particular belongs to $$SC([-1,1],\mathbb R)$$. On $$|x|<1/N$$ the values of $$f$$ have absolute value at most $$1/(N+2)$$, so

$$
\|g_N-f\|_\infty\leq\frac1{N+2}\longrightarrow0.
$$

Therefore a sequence in $$SC([-1,1],\mathbb R)$$ converges in $$S([-1,1],\mathbb R)$$ to a function outside $$SC([-1,1],\mathbb R)$$. It is a vector subspace, but not a closed one.

### Exercise 4

Assume first that $$f\in S(I,E)$$. By Theorem 1.2, choose staircase functions $$s_n$$ such that

$$
\|s_n-f\|_\infty\leq 2^{-n}\qquad(n\geq1).
$$

Set $$f_0=s_1$$ and $$f_n=s_{n+1}-s_n$$ for $$n\geq1$$. A finite sum or difference of staircase functions is a staircase function: take a common refinement of their finite partitions. Hence every $$f_n$$ belongs to $$T(I,E)$$. For $$n\geq1$$,

$$
\|f_n\|_\infty
\leq \|s_{n+1}-f\|_\infty+\|s_n-f\|_\infty
\leq 2^{-(n+1)}+2^{-n}.
$$

Also $$\|f_0\|_\infty<\infty$$. It follows that $$\sum_{n=0}^\infty\|f_n\|_\infty<\infty$$. The partial sums telescope:

$$
\sum_{n=0}^{N}f_n=s_{N+1}\longrightarrow f
\quad\text{uniformly on }I.
$$

Conversely, suppose $$f_n\in T(I,E)$$ and $$\sum_{n=0}^\infty\|f_n\|_\infty<\infty$$, with $$f=\sum_{n=0}^\infty f_n$$. The series converges uniformly, since for every $$N$$,

$$
\sup_{x\in I}\left\|\sum_{n=N+1}^\infty f_n(x)\right\|
\leq\sum_{n=N+1}^\infty\|f_n\|_\infty\longrightarrow0.
$$

Each partial sum is a staircase function, using a common refinement of the finitely many partitions involved. Theorem 1.2 now implies that its uniform limit $$f$$ is jump continuous. This proves the equivalence.

### Exercise 5

By Theorem 1.2, write $$f$$ as a uniform limit of staircase functions $$s_n$$. Let $$D(h)$$ denote the set of discontinuities of a function $$h$$. Each $$D(s_n)$$ is finite, since a staircase function is constant on the open intervals of a finite partition.

If $$x\notin\bigcup_{n=1}^\infty D(s_n)$$, then every $$s_n$$ is continuous at $$x$$. A uniform limit of functions continuous at $$x$$ is continuous at $$x$$: given $$\varepsilon>0$$, choose $$n$$ with $$\|s_n-f\|_\infty<\varepsilon/3$$, and then use continuity of $$s_n$$ at $$x$$ to make $$|s_n(y)-s_n(x)|<\varepsilon/3$$ near $$x$$. The triangle inequality gives $$|f(y)-f(x)|<\varepsilon$$ there.

Hence

$$
D(f)\subseteq\bigcup_{n=1}^\infty D(s_n).
$$

The right-hand side is a countable union of finite sets, so every jump continuous function has at most countably many discontinuities.

### Exercise 6

The Dirichlet function equals $$1$$ at rational points and $$0$$ at irrational points. Both sets are dense in every nonempty interval. Therefore, in every available one-sided neighborhood of each point of $$[0,1]$$, values of the function approach both $$0$$ and $$1$$ along sequences. No one-sided limit exists, including the right-hand limit at $$0$$ and the left-hand limit at $$1$$. Thus the Dirichlet function does not belong to $$S([0,1],\mathbb R)$$.

### Exercise 7

Let $$x=p/q\in[0,1]\cap\mathbb Q$$ be in lowest terms. We show that both one-sided limits at $$x$$ are $$0$$. Fix a positive integer $$N$$. There are only finitely many rationals in $$[0,1]$$ whose reduced denominator is at most $$N$$. Since this finite set contains no point arbitrarily close to $$x$$ other than $$x$$ itself, there is a neighborhood of $$x$$ containing no other such rational. For any distinct $$y$$ in that neighborhood, either $$y$$ is irrational and $$f(y)=0$$, or its reduced denominator exceeds $$N$$ and $$|f(y)|\leq1/(N+1)$$. Since $$N$$ can be arbitrarily large, $$f(y)\to0$$ as $$y\to x$$ from either available side.

Now let $$x\in[0,1]\setminus\mathbb Q$$. Given $$\varepsilon>0$$, choose $$N$$ with $$1/(N+1)<\varepsilon$$. The finite set of rationals with denominator at most $$N$$ has positive distance from $$x$$. In a sufficiently small neighborhood of $$x$$, every rational therefore has denominator greater than $$N$$, and every irrational has function value zero. Thus $$f(y)<\varepsilon$$ throughout that neighborhood, so $$f(y)\to0=f(x)$$.

At every interior point both one-sided limits therefore exist (and equal zero); at the endpoints the corresponding one-sided limit exists as well. Hence this function, Thomae’s function, is jump continuous.

### Exercise 8

The function is continuous at every $$x>0$$. At $$0$$, choose

$$
x_n=\frac1{\pi/2+2\pi n},
\qquad
y_n=\frac1{3\pi/2+2\pi n}.
$$

Both sequences approach $$0$$ from the right, but $$f(x_n)=1$$ and $$f(y_n)=-1$$. Thus the right-hand limit at $$0$$ does not exist, and $$f\notin S([0,1],\mathbb R)$$.

### Exercise 9

Use the standard norm on the finite product, for example

$$
\|(v_0,\ldots,v_n)\|=\max_{0\leq j\leq n}\|v_j\|_{E_j}.
$$

If $$f\in S(I,E)$$, each coordinate projection $$\pi_j:E\to E_j$$ is continuous. Applying it to each existing one-sided limit of $$f$$ shows that $$f_j=\pi_j\circ f$$ has the corresponding one-sided limits. Thus $$f_j\in S(I,E_j)$$.

Conversely, suppose each $$f_j\in S(I,E_j)$$. For any required one-sided limit at $$x$$, let $$v_j$$ be the corresponding limit of $$f_j$$. Since there are finitely many coordinates,

$$
\left\|(f_0(y),\ldots,f_n(y))-(v_0,\ldots,v_n)\right\|
=\max_{0\leq j\leq n}\|f_j(y)-v_j\|_{E_j}\longrightarrow0.
$$

So the one-sided limit of $$f$$ exists and equals $$(v_0,\ldots,v_n)$$. Therefore $$f\in S(I,E)$$.

### Exercise 10

Fix a point and one side at which a one-sided limit of $$f$$ is required. Since $$f\in S(I,E)$$, there is a limit $$v\in E$$ with $$f(y)\to v$$ from that side. Uniform continuity of $$\varphi$$ implies continuity, so

$$
\varphi(f(y))\longrightarrow\varphi(v)
$$

from the same side. This applies at every point and side, including the relevant endpoint limits. Hence $$\varphi\circ f\in S(I,F)$$.

### Exercise 11

The claim is false. Let $$I=[0,1]$$, set $$a=1/2$$, and define

$$
f(t)=
\begin{cases}
0,&t\leq a,\\
1,&t>a,
\end{cases}
\qquad
g(t)=
\begin{cases}
a+(t-a)^2\sin\!\left(\dfrac1{t-a}\right),&t\ne a,\\
a,&t=a.
\end{cases}
$$

The function $$f$$ is a staircase function. The function $$g$$ is continuous away from $$a$$, and at $$a$$ it is continuous because

$$
|g(t)-a|\leq |t-a|^2\longrightarrow0.
$$

Also, for $$t\in[0,1]$$,

$$
|g(t)-a|\leq|t-a|^2\leq\frac14,
$$

so $$g(t)\in[1/4,3/4]\subseteq I$$. Thus $$g\in S(I,\mathbb R)$$ and $$\operatorname{im}(g)\subseteq I$$.

For sufficiently large integers $$n$$, put

$$
t_n=a+\frac1{\pi/2+2\pi n},
\qquad
u_n=a+\frac1{3\pi/2+2\pi n}.
$$

Both sequences approach $$a$$ from the right. But $$g(t_n)>a$$, so $$(f\circ g)(t_n)=1$$, while $$g(u_n)<a$$, so $$(f\circ g)(u_n)=0$$. The right-hand limit of $$f\circ g$$ at $$a$$ does not exist. Therefore $$f\circ g\notin S(I,\mathbb R)$$ in general.
