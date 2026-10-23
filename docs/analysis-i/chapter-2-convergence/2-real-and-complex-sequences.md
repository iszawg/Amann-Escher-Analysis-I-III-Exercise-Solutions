# Chapter II — Convergence

## 2. Real and Complex Sequences

### Exercise 1

**(a)** Rationalizing the difference gives

$$
x_n=\sqrt{n+1}-\sqrt n
=\frac{1}{\sqrt{n+1}+\sqrt n}\longrightarrow0.
$$

Thus the sequence converges to $$0$$.

**(b)** Rationalizing as in part (a),

$$
x_n=(-1)^n\frac{\sqrt n}{\sqrt{n+1}+\sqrt n}.
$$

The fraction tends to $$1/2$$. Hence the even terms tend to $$1/2$$ and the odd terms tend to $$-1/2$$. Since these limits differ, the sequence does not converge.

**(c)** Using $$1+2+\cdots+n=n(n+1)/2$$,

$$
x_n=\frac{n(n+1)}{2(n+2)}-\frac n2
=-\frac{n}{2(n+2)}\longrightarrow-\frac12.
$$

**(d)** The numerator and denominator have limits $$2^{10}-1$$ and $$1$$, respectively. Therefore

$$
x_n=\frac{(2-1/\sqrt n)^{10}-(1+1/n^2)^{10}}{1-1/n^2-1/\sqrt n}
\longrightarrow 2^{10}-1=1023.
$$

**(e)** By the limit laws,

$$
x_n=(100+1/n)^2\longrightarrow100^2=10000.
$$

### Exercise 2

For $$n\ge4$$, the binomial expansion gives

$$
2^n=(1+1)^n\ge\binom n4.
$$

Consequently,

$$
0\le\frac{n^3}{2^n}
\le\frac{n^3}{\binom n4}
=\frac{24n^2}{(n-1)(n-2)(n-3)}\longrightarrow0.
$$

The last fraction tends to zero because its denominator has degree three while its numerator has degree two. The squeeze theorem therefore shows that $$n^3/2^n$$ is a null sequence.

### Exercise 3

Let $$a=\lim x_n>0$$. For all sufficiently large $$n$$, convergence gives $$|x_n-a|<a/2$$. It follows that $$x_n>a-a/2=a/2>0$$. Hence all but finitely many terms are positive.

### Exercise 4

Let $$\varepsilon>0$$. Choose $$N$$ such that $$|x_j-a|<\varepsilon/2$$ whenever $$j\ge N$$, and put $$C=\sum_{j=1}^{N-1}|x_j-a|$$. For $$n\ge N$$,

$$
\left|\frac1n\sum_{j=1}^n x_j-a\right|
\le\frac Cn+\frac1n\sum_{j=N}^n|x_j-a|
<\frac Cn+\frac\varepsilon2.
$$

For all sufficiently large $$n$$, $$C/n<\varepsilon/2$$. Thus the displayed average tends to $$a$$.

### Exercise 5

Equip $$\mathbb K^m$$ with the product metric $$d(u,v)=\max_{1\le j\le m}|u_j-v_j|$$, and use the corresponding coordinatewise vector operations.

**(a)** The zero sequence belongs to $$c(\mathbb K^m)$$. If $$x_n\to x$$ and $$y_n\to y$$, then

$$
d(x_n+y_n,x+y)\le d(x_n,x)+d(y_n,y)\longrightarrow0.
$$

For every scalar $$\lambda\in\mathbb K$$,

$$
d(\lambda x_n,\lambda x)=|\lambda|d(x_n,x)\longrightarrow0.
$$

So $$c(\mathbb K^m)$$ is closed under addition and scalar multiplication, and is a subspace of $$s(\mathbb K^m)$$.

**(b)** If $$x_n\to x$$, $$y_n\to y$$, and $$\lambda,\mu\in\mathbb K$$, part (a) and the limit laws give $$\lambda x_n+\mu y_n\to\lambda x+\mu y$$. Therefore

$$
\lim_{n\to\infty}(\lambda x_n+\mu y_n)
=\lambda\lim_{n\to\infty}x_n+\mu\lim_{n\to\infty}y_n,
$$

so the limit map is linear.

**(c)** The convergent scalar sequence $$\lambda_n$$ is bounded. Since $$x_n\to a$$ and $$\lambda_n\to\alpha$$,

$$
d(\lambda_nx_n,\alpha a)
\le |\lambda_n|d(x_n,a)+|\lambda_n-\alpha|d(a,0)\longrightarrow0.
$$

Hence $$\lambda_nx_n\to\alpha a$$ in $$\mathbb K^m$$.

### Exercise 6

Polynomial limit laws imply $$p(x_n)\to p(a)$$ and $$q(x_n)\to q(a)$$. Since $$q(a)\ne0$$, we have $$q(x_n)\ne0$$ for all sufficiently large $$n$$. The quotient limit law then yields

$$
r(x_n)=\frac{p(x_n)}{q(x_n)}\longrightarrow\frac{p(a)}{q(a)}=r(a).
$$

If a denominator vanishes at one of the finitely many initial terms, the expression is considered on the tail where it is defined; changing or omitting finitely many terms does not affect convergence. Taking $$q=1$$ shows that $$p(x_n)\to p(a)$$ for every polynomial $$p$$.

### Exercise 7

Write $$r=s/t$$ with $$s\in\mathbb Z$$ and $$t\in\mathbb N^\times$$. First, the positive $$t$$-th roots converge: set $$y_n=x_n^{1/t}$$ and $$y=x^{1/t}$$. The factorization in the hint gives

$$
|y_n-y|
=\frac{|x_n-x|}{\sum_{k=0}^{t-1}y_n^k y^{t-1-k}}
\le\frac{|x_n-x|}{y^{t-1}}\longrightarrow0,
$$

because every term in the denominator is positive and its $$k=0$$ term is $$y^{t-1}>0$$. Thus $$x_n^{1/t}\to x^{1/t}$$. Applying the product limit law for positive integer powers, and the reciprocal limit law for negative powers, gives

$$
x_n^r=(x_n^{1/t})^s\longrightarrow(x^{1/t})^s=x^r.
$$

This also covers $$s=0$$, when both sides are the constant sequence $$1$$.

### Exercise 8

Suppose first that $$1/x_n\to0$$. Given $$K>0$$, eventually $$1/x_n<1/K$$. Since $$x_n>0$$, this implies $$x_n>K$$.

Conversely, suppose that for every $$K>0$$ we eventually have $$x_n>K$$. Given $$\varepsilon>0$$, choose $$K>1/\varepsilon$$. Then eventually

$$
0<\frac1{x_n}<\frac1K<\varepsilon,
$$

so $$1/x_n\to0$$.

### Exercise 9

For every $$a>0$$,

$$
a+\frac1a-2=\frac{(a-1)^2}{a}\ge0.
$$

Therefore the sequence in the exercise satisfies

$$
x_n=\sum_{k=0}^n\left(a_k+\frac1{a_k}\right)\ge2(n+1).
$$

In particular, for every $$K>0$$ we have $$x_n>K$$ for all sufficiently large $$n$$. By Exercise 8, $$1/x_n\to0$$.
