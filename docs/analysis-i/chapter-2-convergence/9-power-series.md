# Chapter II — Convergence

## 9. Power Series

### Exercise 1

For a power series with coefficients $$(a_k)$$, the Cauchy–Hadamard formula gives

$$
\rho=\frac{1}{\limsup_{k\to\infty}|a_k|^{1/k}}.
$$

For formulas with a zero denominator at $$k=0$$, take $$k\ge1$$; any choice of the zeroth coefficient leaves the radius unchanged.

**(a)** Here $$a_k=\sqrt{k2^k}/(k+1)^6$$, and

$$
|a_k|^{1/k}=\frac{(k2^k)^{1/(2k)}}{(k+1)^{6/k}}\longrightarrow\sqrt2.
$$

Thus $$\rho=1/\sqrt2$$.

**(b)** The ratio of consecutive absolute values satisfies

$$
\left|\frac{a_k}{a_{k+1}}\right|=\left(1+\frac1k\right)^k\longrightarrow e.
$$

The ratio formula for the radius therefore gives $$\rho=e$$.

**(c)** Since

$$
|a_k|^{1/k}=(1+k^2)^{-1/(2k)}\longrightarrow1,
$$

the radius is $$\rho=1$$.

**(d)** For $$a_k=1/\sqrt{k!}$$,

$$
\left|\frac{a_k}{a_{k+1}}\right|=\sqrt{k+1}\longrightarrow\infty.
$$

Hence $$\rho=\infty$$.

**(e)** Here $$|a_k|^{1/k}=1/k\to0$$, so $$\rho=\infty$$.

**(f)** We have

$$
|a_k|^{1/k}=1+\frac1{k^2}\longrightarrow1,
$$

so $$\rho=1$$.

### Exercise 2

The coefficients are $$a_k=k+1$$. Since $$(k+1)^{1/k}\to1$$, the Cauchy–Hadamard formula gives radius $$1$$. For $$|z|<1$$, the geometric series converges absolutely. In its Cauchy product, the coefficient of $$z^k$$ is a sum of $$k+1$$ ones, so

$$
\sum_{k=0}^{\infty}(k+1)z^k
=\left(\sum_{j=0}^{\infty}z^j\right)^2
=\frac{1}{(1-z)^2}.
$$

### Exercise 3

Set $$b_k:=(k+1)a_{k+1}$$, the coefficient of $$X^k$$ in the derived power series. Writing $$u_n:=|a_n|^{1/n}$$ gives

$$
|b_k|^{1/k}
=(k+1)^{1/k}u_{k+1}^{(k+1)/k}.
$$

The factor $$(k+1)^{1/k}$$ tends to $$1$$. Also, raising a nonnegative sequence to positive exponents tending to $$1$$ preserves its extended limsup: when the limsup is finite and positive, bound the terms eventually above and below by arbitrary constants on either side of it; for the endpoints $$0$$ and $$+\infty$$, use arbitrary positive thresholds. Consequently,

$$
\limsup_{k\to\infty}|b_k|^{1/k}
=\limsup_{n\to\infty}|a_n|^{1/n}.
$$

The Cauchy–Hadamard formula now shows that the original and derived power series have the same radius of convergence.

### Exercise 4

For each fixed $$m$$, the finite sum satisfies

$$
\sum_{k=0}^{m}a_k\left(1-\frac1n\right)^k
\longrightarrow\sum_{k=0}^{m}a_k
\qquad(n\to\infty).
$$

Given $$M>0$$, choose $$m$$ such that $$\sum_{k=0}^{m}a_k>M$$, which is possible because $$\sum_k a_k$$ diverges and all terms are positive. The finite weighted sum is then greater than $$M$$ for all sufficiently large $$n$$. Since the remaining terms in $$f_n$$ are nonnegative,

$$
f_n\ge\sum_{k=0}^{m}a_k\left(1-\frac1n\right)^k>M
$$

for all such $$n$$. Thus $$f_n\to\infty$$. The radius assumption ensures that each $$f_n$$ is finite: for $$n\ge2$$ its argument lies inside the unit disk, and for $$n=1$$ it is evaluation at zero.

### Exercise 5

The condition on the lower and upper limits implies that there are constants $$c,C>0$$ such that, for all sufficiently large $$k$$,

$$
c\le|a_k|\le C.
$$

Taking $$k$$th roots shows that $$|a_k|^{1/k}\to1$$. Hence the radius of convergence is $$\rho=1$$.

### Exercise 6

Let $$r_k:=|a_k/a_{k+1}|>0$$ and

$$
G_n:=\left(\prod_{k=0}^{n-1}r_k\right)^{1/n}
=\left|\frac{a_0}{a_n}\right|^{1/n}.
$$

By the Cauchy–Hadamard formula and $$|a_0|^{1/n}\to1$$, $$\rho=\liminf_{n\to\infty}G_n$$. Also, $$\log G_n$$ is the arithmetic mean of $$\log r_0,\ldots,\log r_{n-1}$$. If $$L:=\liminf\log r_k$$ is finite, then for every $$\varepsilon>0$$ all sufficiently late terms exceed $$L-\varepsilon$$; the fixed finite prefix vanishes after division by $$n$$, so $$\liminf\log G_n\ge L-\varepsilon$$. Letting $$\varepsilon\downarrow0$$ gives the lower bound. The same tail argument with eventual upper bounds gives $$\limsup\log G_n\le\limsup\log r_k$$. These statements also hold for infinite endpoints by using arbitrary finite bounds. Exponentiating gives

$$
\liminf_{k\to\infty}\left|\frac{a_k}{a_{k+1}}\right|
\le\rho\le
\limsup_{k\to\infty}\left|\frac{a_k}{a_{k+1}}\right|.
$$

### Exercise 7

On a disk centered at zero, both $$x$$ and $$-x$$ are in the domain. If $$f(x)=\sum_{k=0}^{\infty}a_kx^k$$, then

$$
f(x)-f(-x)=2\sum_{j=0}^{\infty}a_{2j+1}x^{2j+1},
\qquad
f(x)+f(-x)=2\sum_{j=0}^{\infty}a_{2j}x^{2j}.
$$

Uniqueness of power series representations implies that $$f$$ is even exactly when $$a_{2j+1}=0$$ for every $$j\ge0$$. Similarly, $$f$$ is odd exactly when $$a_{2j}=0$$ for every $$j\ge0$$.

### Exercise 8

For the sum, take

$$
a=\sum_{k=0}^{\infty}X^k,\qquad
b=1-\sum_{k=0}^{\infty}X^k.
$$

Both radii are $$1$$, but $$a+b=1$$ has infinite radius. Thus $$\rho_{a+b}>\max(\rho_a,\rho_b)$$.

For the product, take

$$
a=\frac{1+X}{1-X},\qquad b=\frac{1-X}{1+X}.
$$

Their expansions are $$a=1+2\sum_{k=1}^{\infty}X^k$$ and $$b=1+2\sum_{k=1}^{\infty}(-1)^kX^k$$, so both have radius $$1$$. Their product is $$ab=1$$, which has infinite radius. Hence $$\rho_{ab}>\max(\rho_a,\rho_b)$$ is also possible.

### Exercise 9

The coefficient of $$X^0$$ in $$ab=1$$ requires $$b_0=1$$. For each $$n\ge1$$, the coefficient of $$X^n$$ must vanish, so

$$
a_0b_n+a_1b_{n-1}+\cdots+a_nb_0=0.
$$

Since $$a_0=1$$, this yields the recursive algorithm

$$
b_0=1,\qquad b_n=-\sum_{j=1}^{n}a_jb_{n-j}\quad(n\ge1).
$$

It determines a unique formal power series $$b$$ and makes every coefficient of $$ab-1$$ equal to zero.

Now suppose that $$a$$ has positive radius of convergence. Write $$a=1+c$$, where $$c=\sum_{k=1}^{\infty}a_kX^k$$ has zero constant term. Choose $$r>0$$ smaller than the radius of $$a$$ and small enough that

$$
q:=\sum_{k=1}^{\infty}|a_k|r^k<1.
$$

In the formal series $$\sum_{m=0}^{\infty}(-c)^m$$, only finitely many powers contribute to any fixed coefficient, and the resulting series is the unique inverse constructed above. The absolute coefficient sums satisfy

$$
\sum_{n=0}^{\infty}|b_n|r^n
\le\sum_{m=0}^{\infty}q^m
=\frac{1}{1-q}<\infty.
$$

Therefore $$b$$ converges absolutely at $$r$$, so its radius of convergence is positive.

### Exercise 10

Comparing coefficients in $$ (1-X-X^2)b=1$$ gives $$b_0=1$$, $$b_1-b_0=0$$, and, for $$n\ge2$$,

$$
b_n-b_{n-1}-b_{n-2}=0.
$$

Thus $$b_1=1$$ and $$b_{k+1}=b_k+b_{k-1}$$ for $$k\ge1$$. The sequence is $$b_k=F_{k+1}$$, where $$F_0=0$$ and $$F_1=1$$ are the Fibonacci numbers. With $$\varphi=(1+\sqrt5)/2$$ and $$\psi=(1-\sqrt5)/2$$, Binet's formula gives

$$
b_k=\frac{\varphi^{k+1}-\psi^{k+1}}{\sqrt5},
\qquad
\lim_{k\to\infty}b_k^{1/k}=\varphi.
$$

The Cauchy–Hadamard formula now yields

$$
\rho=\frac1\varphi=\frac{\sqrt5-1}{2}.
$$
