# Chapter II — Convergence

## 4. Monotone Sequences

### Exercise 1

Let $$M:=\max\{a_1,\ldots,a_k\}>0$$. Then

$$
M^n\le a_1^n+\cdots+a_k^n\le kM^n.
$$

Taking $$n$$th roots gives

$$
M\le\bigl(a_1^n+\cdots+a_k^n\bigr)^{1/n}\le k^{1/n}M.
$$

For fixed $$k$$, $$k^{1/n}=\exp((\log k)/n)\to\exp(0)=1$$. The squeeze theorem therefore proves

$$
\lim_{n\to\infty}\bigl(a_1^n+\cdots+a_k^n\bigr)^{1/n}=M.
$$

### Exercise 2

For $$n\ge2$$,

$$
\left(1-\frac1n\right)^n
=\frac{\left(1-\frac1{n^2}\right)^n}{\left(1+\frac1n\right)^n}.
$$

Bernoulli's inequality yields

$$
1-\frac1n
=1-n\frac1{n^2}
\le\left(1-\frac1{n^2}\right)^n\le1,
$$

so the numerator tends to $$1$$. The denominator tends to $$e$$ by the definition of $$e$$ in the section. Therefore

$$
\left(1-\frac1n\right)^n\longrightarrow\frac1e.
$$

### Exercise 3

The case $$r=0$$ is immediate. Suppose first that $$r=p/q>0$$, where $$p,q\in\mathbb N^\times$$, and set

$$
a_n:=\left(1+\frac rn\right)^n.
$$

Along the subsequence $$n=pj$$,

$$
a_{pj}
=\left(1+\frac1{qj}\right)^{pj}
=\left(\left(1+\frac1{qj}\right)^{qj}\right)^{p/q}
\longrightarrow e^{p/q},
$$

using the definition of $$e$$ and Exercise 2.7, which gives continuity of positive rational powers.

To pass from this subsequence to the full sequence, write $$n=pj+t$$ with $$0\le t<p$$. A direct calculation gives

$$
\frac{a_{pj+t}}{a_{pj}}
=\left(1+\frac r{pj+t}\right)^t
\left(1-\frac{rt}{(pj+t)(pj+r)}\right)^{pj}.
$$

The first factor tends to $$1$$. For the second, put

$$
\delta_j:=\frac{rt}{(pj+t)(pj+r)}.
$$

Since $$t$$ ranges over a finite set, $$pj\delta_j\to0$$. Bernoulli's inequality gives

$$
1-pj\delta_j\le(1-\delta_j)^{pj}\le1,
$$

so this factor also tends to $$1$$. Hence $$a_n/a_{pj}\to1$$ and $$a_n\to e^r$$.

Now let $$r=-s<0$$ with $$s>0$$ rational. For all sufficiently large $$n$$,

$$
\left(1-\frac sn\right)^n
=\frac{\left(1-\frac{s^2}{n^2}\right)^n}{\left(1+\frac sn\right)^n}.
$$

Bernoulli's inequality shows that the numerator tends to $$1$$, while the positive case shows that the denominator tends to $$e^s$$. Thus

$$
\left(1+\frac rn\right)^n\longrightarrow\frac1{e^s}=e^r.
$$

### Exercise 4

There is a small issue with the printed hypothesis. The condition $$x_0\ge a$$ does not always imply that the whole sequence is decreasing. For example, if $$a=1/4$$ and $$x_0=1/4$$, then $$x_1=5/8>x_0$$. The stronger condition $$x_0\ge\sqrt a$$ makes the whole sequence decreasing.

For every $$x_n>0$$, the arithmetic-geometric mean inequality gives

$$
x_{n+1}=\frac12\left(x_n+\frac a{x_n}\right)\ge\sqrt a.
$$

Thus $$x_n\ge\sqrt a$$ for all $$n\ge1$$. For those indices,

$$
x_{n+1}\le x_n
\quad\Longleftrightarrow\quad
\frac a{x_n}\le x_n
\quad\Longleftrightarrow\quad
a\le x_n^2,
$$

so the tail $$\{x_n\}_{n\ge1}$$ is decreasing and bounded below by $$\sqrt a$$. It converges to some $$L\ge\sqrt a$$. Passing to the limit in the recurrence gives

$$
L=\frac12\left(L+\frac aL\right),
$$

hence $$L^2=a$$ and therefore $$L=\sqrt a$$. Under the printed assumption, the sequence still converges to $$\sqrt a$$; only the claim that it is decreasing starting at $$x_0$$ can fail.

### Exercise 5

Define $$f(t):=a/(1+t)$$ for $$t>0$$ and let

$$
F(t):=f(f(t))=\frac{a(1+t)}{1+t+a}.
$$

The function $$F$$ is increasing on $$(0,\infty)$$, and

$$
F(t)-t=\frac{a-t-t^2}{1+t+a}.
$$

The unique positive solution of $$t^2+t=a$$ is

$$
c:=\frac{\sqrt{1+4a}-1}{2}.
$$

Thus $$F(t)>t$$ for $$0<t<c$$ and $$F(t)<t$$ for $$t>c$$. Since $$F(c)=c$$ and $$F$$ is increasing, iteration by $$F$$ moves every positive starting value monotonically toward $$c$$. In particular, the even and odd subsequences $$x_{2n}$$ and $$x_{2n+1}$$ both converge to $$c$$. Therefore

$$
x_n\longrightarrow\frac{\sqrt{1+4a}-1}{2}.
$$

### Exercise 6

Set

$$
m_n:=\min\{x_n,x_{n+1}\},\qquad
M_n:=\max\{x_n,x_{n+1}\},\qquad
R_n:=\frac{M_n}{m_n}.
$$

The geometric mean $$x_{n+2}=\sqrt{x_nx_{n+1}}$$ lies between $$m_n$$ and $$M_n$$. Hence $$m_n$$ is nondecreasing and bounded above, while $$M_n$$ is nonincreasing and bounded below by $$m_0>0$$. Both sequences therefore converge.

The new adjacent pair consists of one endpoint of $$[m_n,M_n]$$ and its geometric mean, so

$$
R_{n+1}=\sqrt{R_n},\qquad R_n=R_0^{1/2^n}\longrightarrow1.
$$

Consequently,

$$
0\le M_n-m_n=m_n(R_n-1)\le M_0(R_n-1)\longrightarrow0.
$$

The limits of $$m_n$$ and $$M_n$$ are therefore equal. Since both $$x_n$$ and $$x_{n+1}$$ lie between them, the sequence $$x_n$$ converges.

### Exercise 7

**(a)** The section establishes $$e=\sum_{k=0}^{\infty}1/k!$$. For $$n\ge1$$,

$$
e-\sum_{k=0}^n\frac1{k!}
=\sum_{j=1}^{\infty}\frac1{(n+j)!}>0.
$$

For each $$j\ge1$$,

$$
\frac{n!}{(n+j)!}
=\prod_{\ell=1}^{j}\frac1{n+\ell}
\le\frac1{(n+1)^j},
$$

with strict inequality when $$j\ge2$$. Therefore

$$
0<n!\left(e-\sum_{k=0}^n\frac1{k!}\right)
<\sum_{j=1}^{\infty}\frac1{(n+1)^j}
=\frac1n,
$$

which proves the stated estimate.

**(b)** Suppose, for contradiction, that $$e=p/q$$ for positive integers $$p,q$$. Choose $$n\ge\max\{q,2\}$$. Then

$$
n!e-\sum_{k=0}^n\frac{n!}{k!}
$$

is an integer: $$n!e$$ is an integer because $$q\mid n!$$, and every term in the sum is an integer. Part (a) says that this integer is strictly between $$0$$ and $$1/n<1$$, which is impossible. Hence $$e$$ is irrational.

### Exercise 8

Let $$f(t):=1+1/t$$ and

$$
G(t):=f(f(t))=\frac{2t+1}{t+1}.
$$

The function $$G$$ is increasing, and

$$
G(t)-t=\frac{1+t-t^2}{t+1}.
$$

Its unique positive fixed point is

$$
g:=\frac{1+\sqrt5}{2}.
$$

Since $$x_0=1<g<x_1=2$$, the even terms $$x_{2n}$$ increase while remaining below $$g$$, and the odd terms $$x_{2n+1}$$ decrease while remaining above $$g$$. Both subsequences converge. Their limits are fixed points of $$G$$, so both equal $$g$$. Thus $$x_n\to g$$.

### Exercise 9

For $$n\ge1$$, let $$r_n:=f_{n+1}/f_n$$. The Fibonacci recurrence gives

$$
r_{n+1}
=\frac{f_{n+2}}{f_{n+1}}
=1+\frac{f_n}{f_{n+1}}
=1+\frac1{r_n},
\qquad r_1=1.
$$

Thus $$r_n=x_{n-1}$$ for the sequence in Exercise 8. It follows that

$$
\lim_{n\to\infty}\frac{f_{n+1}}{f_n}=g.
$$

### Exercise 10

Set $$d_n:=x_n-x_{n+1}$$. The recurrence gives

$$
d_{n+1}
=x_{n+1}-x_{n+2}
=-\frac13(x_n-x_{n+1})
=-\frac13d_n.
$$

Since $$d_0=4$$, we have $$d_n=4(-1/3)^n$$. Therefore

$$
x_n=x_0-\sum_{k=0}^{n-1}d_k
\longrightarrow
5-4\sum_{k=0}^{\infty}\left(-\frac13\right)^k
=5-3=2.
$$

Hence the sequence converges to $$2$$.
