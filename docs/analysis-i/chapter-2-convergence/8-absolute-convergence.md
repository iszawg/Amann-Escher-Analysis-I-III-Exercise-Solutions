# Chapter II — Convergence

## 8. Absolute Convergence

### Exercise 1

**(a)** The ratio of consecutive terms satisfies

$$
\frac{(k+1)^4/3^{k+1}}{k^4/3^k}
=\frac{(1+1/k)^4}{3}\longrightarrow\frac13<1.
$$

The ratio test proves convergence.

**(b)** For $$a_k:=k/(\sqrt[3]{k}+1)^k$$,

$$
\sqrt[k]{a_k}=\frac{k^{1/k}}{\sqrt[3]{k}+1}\longrightarrow0.
$$

The root test proves convergence.

**(c)** For $$k\ge2$$,

$$
\sqrt[k]{\left(1-\frac1k\right)^{k^2}}=\left(1-\frac1k\right)^k\longrightarrow e^{-1}<1.
$$

The root test proves convergence; the initial term does not affect it.

**(d)** Let $$a_k:=\binom{2k}{k}^{-1}$$. Then

$$
\frac{a_{k+1}}{a_k}=\frac{k+1}{2(2k+1)}\longrightarrow\frac14<1,
$$

so the series converges by the ratio test.

**(e)** For $$a_k:=\binom{2k}{k}2^{-k}$$,

$$
\frac{a_{k+1}}{a_k}=\frac{2k+1}{k+1}\longrightarrow2>1.
$$

In particular, the terms do not tend to zero, so the series diverges.

**(f)** For $$a_k:=\binom{2k}{k}5^{-k}$$,

$$
\frac{a_{k+1}}{a_k}=\frac{2(2k+1)}{5(k+1)}\longrightarrow\frac45<1.
$$

The ratio test proves convergence.

### Exercise 2

For the first series, if $$a=0$$ at most its initial term is nonzero, so it converges. For $$a\ne0$$ it is geometric, with ratio

$$
\frac{a^2}{1+a^2}<1.
$$

It therefore converges for every $$a\in\mathbb R$$.

For the second series, its general term satisfies

$$
\frac{1-a^{2k}}{1+a^{2k}}\longrightarrow
\begin{cases}
1,&|a|<1,\\
0,&|a|=1,\\
-1,&|a|>1.
\end{cases}
$$

The term tends to zero exactly when $$|a|=1$$. In that case every term is zero, so the series converges; for all other real $$a$$ it diverges by the term test.

### Exercise 3

For each $$k$$, $$x_k=x_k^+-x_k^-$$ and $$|x_k|=x_k^++x_k^-$$. If both nonnegative series $$\sum_k x_k^+$$ and $$\sum_k x_k^-$$ converged, then $$\sum_k|x_k|$$ would converge, contrary to conditional convergence.

If just one of the two series converged, the identity

$$
\sum_{k=0}^{n}x_k^+-\sum_{k=0}^{n}x_k^- = \sum_{k=0}^{n}x_k
$$

and convergence of $$\sum_kx_k$$ would force the other partial sums to converge as well. Thus neither series converges; since their terms are nonnegative, both diverge to $$+\infty$$.

### Exercise 4

Write the positive terms of the given series as $$p_1,p_2,\ldots$$ and the absolute values of its negative terms as $$q_1,q_2,\ldots$$, retaining their original orders. By Exercise 3,

$$
\sum_jp_j=\sum_jq_j=+\infty,
$$

and conditional convergence implies $$p_j,q_j\to0$$.

For a prescribed $$s\in\mathbb R$$, start at partial sum $$0$$. If the current sum is at or below $$s$$, add unused positive terms until it first exceeds $$s$$; if it is above $$s$$, add unused negative terms until it first falls below $$s$$. Repeat, alternating the two types of blocks. Each block is finite because both sign subseries diverge. At the end of each block, the overshoot is at most the last term added, and these terms tend to zero. The block endpoints therefore tend to $$s$$. Partial sums within a block lie between its two endpoints, so the entire rearranged series converges to $$s$$.

This ordering uses every positive and negative term in its original order. Any zero terms can be inserted at the start if there are finitely many, or one between successive blocks if there are infinitely many. It is therefore a permutation of the original terms.

To obtain a divergent rearrangement, start with partial sum $$0$$ and, for each $$m=1,2,\ldots$$, add unused positive terms until the sum first exceeds $$m$$, then add the next unused negative term. The positive block is finite because $$\sum_jp_j=+\infty$$. If its following negative term has magnitude $$q_j$$, the partial sum at the end of the stage exceeds $$m-q_j$$. As the stages proceed, $$q_j\to0$$, so these endpoints tend to $$+\infty$$; the intervening positive blocks are increasing. Interleave zero terms as above. This gives a permutation whose series diverges to $$+\infty$$.

### Exercise 5

Set $$S:=\sum_{k=1}^{\infty}k^{-2}$$. For the row with index $$j=0$$, the row sum is

$$
r_0=\sum_{k=1}^{\infty}\frac{-1}{k^2}=-S.
$$

For $$j\ge1$$, Exercise 7.9 gives $$r_j=\sum_{k=0,\ k\ne j}^{\infty}(j^2-k^2)^{-1}=1/(4j^2)$$. Since $$x_{jk}=-x_{kj}$$, the column sums are $$c_j=-r_j$$. Thus both iterated series converge, but their values differ:

$$
\sum_{j=0}^{\infty}r_j=-S+\frac14S=-\frac34S,
\qquad
\sum_{k=0}^{\infty}c_k=S-\frac14S=\frac34S.
$$

If the double series were summable, the double-series theorem would make these two values equal. Hence it is not summable.

### Exercise 6

**(a)** Let $$\bigl(x^{(n)}\bigr)$$ be Cauchy in $$\ell_1$$. For every coordinate $$k$$, $$\bigl(x_k^{(n)}\bigr)_n$$ is Cauchy in $$\mathbb K$$; write its limit as $$x_k$$. The sequence $$\bigl(x^{(n)}\bigr)$$ is bounded in norm, say by $$M$$. For every finite $$m$$,

$$
\sum_{k=0}^{m}|x_k|=\lim_{n\to\infty}\sum_{k=0}^{m}|x_k^{(n)}|\le M.
$$

Letting $$m\to\infty$$ shows that $$x=(x_k)\in\ell_1$$. Given $$\varepsilon>0$$, choose $$N$$ so that $$\|x^{(n)}-x^{(r)}\|_1<\varepsilon/2$$ whenever $$n,r\ge N$$. For fixed $$n\ge N$$ and finite $$m$$, coordinatewise convergence gives

$$
\sum_{k=0}^{m}|x_k^{(n)}-x_k|
=\lim_{r\to\infty}\sum_{k=0}^{m}|x_k^{(n)}-x_k^{(r)}|
\le\varepsilon/2
\qquad(m\in\mathbb N).
$$

Taking the supremum over $$m$$ gives $$\|x^{(n)}-x\|_1\le\varepsilon/2<\varepsilon$$. Therefore $$x^{(n)}\to x$$ in $$\ell_1$$, proving that $$\ell_1$$ is complete and hence a Banach space.

**(b)** For every $$x\in\ell_1$$,

$$
\|x\|_\infty=\sup_k|x_k|\le\sum_{k=0}^{\infty}|x_k|=\|x\|_1.
$$

The constant sequence $$x_k=1$$ belongs to $$\ell_\infty$$ but not to $$\ell_1$$, so the inclusion is proper.

**(c)** For the sequence $$\xi_j$$ in the hint, $$\|\xi_j\|_\infty=1$$ while $$\|\xi_j\|_1=j+1$$. Their ratio is unbounded, so no constant can bound the $$\ell_1$$-norm by the inherited $$\ell_\infty$$-norm. The two norms are not equivalent.

### Exercise 7

**(a)** For $$n\ge N$$,

$$
\frac{x_{n+1}}{y_{n+1}}\le\frac{x_n}{y_n}.
$$

Thus $$x_n/y_n\le x_N/y_N$$ for all $$n\ge N$$, so $$x_n\le(x_N/y_N)y_n$$. Comparison with the convergent series $$\sum_n y_n$$ proves that $$\sum_n x_n$$ converges.

**(b)** For $$n\ge N$$, the hypothesis gives

$$
\frac{x_{n+1}}{z_{n+1}}\ge\frac{x_n}{z_n}.
$$

Hence $$x_n/z_n\ge x_N/z_N>0$$ for all $$n\ge N$$, so $$x_n\ge(x_N/z_N)z_n$$. Since $$\sum_n z_n=\infty$$, comparison proves $$\sum_n x_n=\infty$$.

### Exercise 8

For the first series, group the terms with indices $$2k-1$$ and $$2k$$:

$$
\frac{1}{4k-2}-\frac{1}{8k}>\frac{1}{8k}.
$$

The grouped partial sums diverge to $$+\infty$$ by comparison with the harmonic series. Thus the first series diverges.

For the second series, the same grouping gives, for $$k\ge2$$,

$$
\frac{1}{6k-9}-\frac{1}{6k+6}
=\frac{15}{(6k-9)(6k+6)}.
$$

These grouped terms are positive and bounded by a constant multiple of $$k^{-2}$$, so the paired series converges. The unpaired term in each pair tends to zero, hence the original series converges. It is not absolutely convergent: its odd terms for $$k\ge2$$ have absolute values $$1/(6k-9)\ge1/(6k)$$, whose sum diverges. Therefore the second series converges conditionally.

### Exercise 9

Let $$u_0=a$$, $$u_n=a^n$$ for $$n\ge1$$, and $$v_0=-b$$, $$v_n=b^n$$ for $$n\ge1$$. The Cauchy-product coefficients are $$c_n:=\sum_{k=0}^{n}u_kv_{n-k}$$. We have $$c_0=-ab$$. For $$n\ge1$$,

$$
\begin{aligned}
c_n
&=ab^n-ba^n+ab\sum_{r=0}^{n-2}a^r b^{n-2-r}\\
&=ab^n-ba^n+ab\frac{a^{n-1}-b^{n-1}}{a-b}\\
&=0,
\end{aligned}
$$

where the sum is empty for $$n=1$$ and $$a-b=1$$. Thus the Cauchy product has only one nonzero term, $$c_0=-ab$$, and converges absolutely. In the stated example $$a=2$$ and $$b=1$$, so the product series sums to $$-2$$.

### Exercise 10

Use $$\exp(x+y)=\exp(x)\exp(y)$$ from Example 8.12(a). The exponential of a real number is real, since it is defined by a power series with real terms.

**(a)** We have $$\exp(x)=\exp(x/2)^2\ge0$$. Also $$\exp(x/2)\exp(-x/2)=\exp(0)=1$$, so $$\exp(x/2)\ne0$$. Consequently $$\exp(x)>0$$.

**(b)** If $$t>0$$, then the defining series gives $$\exp(t)=1+t+t^2/2!+\cdots>1$$. If $$x<y$$, it follows that

$$
\exp(y)=\exp(x)\exp(y-x)>\exp(x),
$$

using part (a). Thus $$\exp$$ is strictly increasing.

**(c)** Set $$c:=\exp(1)>1$$. By the addition identity, $$\exp(n)=c^n$$ and $$\exp(-n)=c^{-n}$$ for positive integers $$n$$. Given $$\varepsilon>0$$, choose $$n\ge1$$ so large that $$c^n>1/\varepsilon$$. Then $$x:=-n<0$$ and $$y:=n>0$$ satisfy

$$
\exp(x)=c^{-n}<\varepsilon,
\qquad
\exp(y)=c^n>1/\varepsilon.
$$
