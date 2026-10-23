# Chapter II — Convergence

## 7. Series

### Exercise 1

**(a)** This is a geometric series with ratio $$-1/2$$, so

$$
\sum_{k=0}^{\infty}\frac{(-1)^k}{2^k}
=\frac{1}{1+1/2}=\frac23.
$$

**(b)** For $$k\ge1$$,

$$
\frac{1}{4k^2-1}
=\frac12\left(\frac{1}{2k-1}-\frac{1}{2k+1}\right).
$$

The partial sum through $$N$$ is

$$
\sum_{k=1}^{N}\frac{1}{4k^2-1}
=\frac12\sum_{k=1}^{N}\left(\frac1{2k-1}-\frac1{2k+1}\right)
=\frac12\left(1-\frac1{2N+1}\right).
$$

Letting $$N\to\infty$$ gives

$$
\sum_{k=1}^{\infty}\frac{1}{4k^2-1}=\frac12.
$$

### Exercise 2

**(a)** Rationalizing the numerator gives

$$
\frac{\sqrt{k+1}-\sqrt{k}}{\sqrt{k}}
=\frac{1}{\sqrt{k}(\sqrt{k+1}+\sqrt{k})}.
$$

For $$k\ge1$$, $$\sqrt{k+1}\le\sqrt2\sqrt{k}$$, so this term is at least $$1/((1+\sqrt2)k)$$. Comparison with the harmonic series shows that the series diverges.

**(b)** The numbers $$\sqrt{k+1}-\sqrt{k}$$ decrease to zero. The Leibniz criterion therefore gives convergence. It is not absolute convergence, since

$$
\sum_{k=0}^{N}\left|(-1)^k(\sqrt{k+1}-\sqrt{k})\right|
=\sqrt{N+1}\longrightarrow\infty.
$$

**(c)** Put $$a_k:=k!/k^k$$. Then

$$
\frac{a_{k+1}}{a_k}=\left(\frac{k}{k+1}\right)^k\longrightarrow e^{-1}<1,
$$

so the ratio test proves convergence.

**(d)** Write

$$
b_k:=\frac{(k+1)^{k-1}}{k^k}
=\frac1k\left(1+\frac1k\right)^{k-1}.
$$

Then $$b_k\to0$$, and

$$
\frac{b_{k+1}}{b_k}
=\left(\frac{k(k+2)}{(k+1)^2}\right)^k<1.
$$

Thus the terms $$(-1)^k b_k$$ satisfy the Leibniz criterion. The convergence is conditional: since $$b_k\ge1/k$$, the series of absolute values diverges.

### Exercise 3

At the start of hour $$n$$, the band has length $$n$$ meters. During that hour the snail crawls $$5$$ centimeters, increasing its fraction of the band by

$$
\frac{0.05}{n}=\frac{1}{20n}.
$$

The subsequent uniform stretch preserves that fraction. After $$N$$ hours the snail's fraction of the band is therefore

$$
\frac1{20}\sum_{n=1}^{N}\frac1n.
$$

The harmonic partial sums are unbounded, so this fraction reaches $$1$$ after finitely many hours. The snail reaches the right end.

### Exercise 4

Let $$s:=\sum_{k=0}^{\infty}a_k$$. The partial sums converge to $$s$$, and

$$
r_n=\sum_{k=n}^{\infty}a_k=s-\sum_{k=0}^{n-1}a_k\longrightarrow s-s=0.
$$

Hence $$(r_n)$$ is a null sequence.

### Exercise 5

Convergence of $$\sum_k x_k$$ implies $$x_k\to0$$. Since $$(x_k)$$ is decreasing, it follows that $$x_k\ge0$$. For $$m:=\lceil n/2\rceil$$, monotonicity gives

$$
0\le n x_n\le 2\sum_{k=m}^{n}x_k\le2\sum_{k=m}^{\infty}x_k.
$$

The last expression tends to zero as $$n\to\infty$$, so $$k x_k\to0$$.

### Exercise 6

If $$\sum_k x_k<\infty$$, then $$0\le x_k/(1+x_k)\le x_k$$, so $$\sum_k x_k/(1+x_k)<\infty$$.

Conversely, suppose $$\sum_k x_k/(1+x_k)<\infty$$. Its terms tend to zero, so eventually $$x_k/(1+x_k)\le1/2$$. For those indices,

$$
x_k=\frac{x_k/(1+x_k)}{1-x_k/(1+x_k)}\le2\frac{x_k}{1+x_k}.
$$

Thus the tail of $$\sum_k x_k$$ converges, and adding its finitely many initial terms proves $$\sum_k x_k<\infty$$.

### Exercise 7

**(a)(i)** For every $$d\ge0$$,

$$
\frac{d}{1+d}\ge\frac12\min\{d,1\}.
$$

Since $$\sum_k d_k=\infty$$, also $$\sum_k\min\{d_k,1\}=\infty$$: either infinitely many $$d_k\ge1$$, or eventually $$d_k<1$$ and the two sequences then agree. Consequently $$\sum_k d_k/(1+d_k)$$ diverges. The hypothesis is needed for this conclusion; for example, $$d_k=0$$ for all $$k$$ makes the series converge.

**(a)(ii)** For $$k\ge1$$,

$$
0\le\frac{d_k}{1+k^2d_k}\le\frac1{k^2}.
$$

The series converges by comparison, regardless of $$\sum_k d_k$$. The hypothesis is not needed here. A possible term with $$k=0$$ is only one finite term and does not affect convergence.

**(b)** For the series $$\sum_k d_k/(1+kd_k)$$, let $$d_{2^m}=1$$ for $$m\ge1$$ and let all other terms be zero. Then $$\sum_k d_k=\infty$$, while the nonzero terms of the series in question are $$1/(1+2^m)$$, whose sum converges. In contrast, taking $$d_k=1$$ for every $$k\ge1$$ gives the divergent harmonic series $$\sum_k1/(1+k)$$.

For $$\sum_k d_k/(1+d_k^2)$$, let $$d_{2^m}=2^m$$ for $$m\ge1$$ and let all other terms be zero. Then $$\sum_k d_k=\infty$$, while the nonzero transformed terms satisfy

$$
\frac{2^m}{1+2^{2m}}\le2^{-m},
$$

so their sum converges. Taking $$d_k=1$$ for every $$k\ge1$$ instead makes every transformed term equal to $$1/2$$, so the series diverges.

### Exercise 8

The positive terms in the displayed series are exactly the terms $$1/k^2$$ for odd $$k$$ not divisible by $$3$$; the negative terms are those for even $$k$$ not divisible by $$3$$. Let $$A$$ and $$B$$ denote the sums of these positive and absolute negative terms. With $$s=\sum_{k=1}^{\infty}k^{-2}$$,

$$
A=\left(1-\frac1{3^2}\right)\left(1-\frac1{2^2}\right)s=\frac23s,
\qquad
B=\left(1-\frac1{3^2}\right)\frac1{2^2}s=\frac29s.
$$

Here the odd terms sum to $$(1-2^{-2})s$$, and restricting them to odd integers not divisible by $$3$$ removes the odd multiples of $$3$$. Similarly, $$B$$ is the sum over even integers minus the sum over multiples of $$6$$. Therefore the displayed series equals

$$
A-B=\left(\frac23-\frac29\right)s=\frac49s.
$$

### Exercise 9

For $$k\ne j$$, factor the denominator:

$$
\frac1{j^2-k^2}=\frac1{2j}\left(\frac1{j-k}+\frac1{j+k}\right).
$$

For $$N\ge j$$, let $$H_m:=\sum_{r=1}^{m}1/r$$ and $$H_0:=0$$. The partial sum through $$k=N$$, omitting the zero term at $$k=j$$, is

$$
\begin{aligned}
\sum_{\substack{0\le k\le N\\k\ne j}}\frac1{j^2-k^2}
&=\frac1{2j}\left(H_j-H_{N-j}+H_{j+N}-H_{j-1}-\frac1{2j}\right)\\
&=\frac1{2j}\left(\frac1{2j}+H_{j+N}-H_{N-j}\right).
\end{aligned}
$$

For fixed $$j$$, $$H_{j+N}-H_{N-j}\to0$$ as $$N\to\infty$$. Hence

$$
\sum_{k=0}^{\infty}x_{jk}=\frac1{4j^2}.
$$

### Exercise 10

**(a)** Set $$c_1:=\lfloor x\rfloor$$ and $$r_1:=x-c_1\in[0,1)$$. Recursively, for $$k\ge1$$, define

$$
c_{k+1}:=\lfloor(k+1)r_k\rfloor,
\qquad
r_{k+1}:=(k+1)r_k-c_{k+1}.
$$

Then $$c_{k+1}\in\{0,1,\ldots,k\}$$ and $$r_{k+1}\in[0,1)$$. Iterating the recurrence gives

$$
x=c_1+\sum_{j=2}^{n+1}\frac{c_j}{j!}+\frac{r_{n+1}}{(n+1)!}.
$$

Since the final term tends to zero, this constructs the required Cantor series.

For uniqueness under the stated restriction, suppose two such expansions first differ at index $$m$$, and suppose the coefficient of the second is larger there. The difference at that index is at least $$1/m!$$, whereas the largest possible compensating tail is

$$
\sum_{k=m+1}^{\infty}\frac{k-1}{k!}=\frac1{m!},
$$

by part (b). Equality could hold only if the first expansion has $$c_k=k-1$$ and the second has $$c_k=0$$ for every $$k>m$$, with a difference of exactly one at index $$m$$. That would make the first expansion eventually maximal, contrary to the restriction. Thus the restricted representation is unique.

**(b)** Since

$$
\frac{k-1}{k!}=\frac1{(k-1)!}-\frac1{k!},
$$

the partial sums telescope:

$$
\sum_{k=n+1}^{N}\frac{k-1}{k!}=\frac1{n!}-\frac1{N!}\longrightarrow\frac1{n!}.
$$

**(c)** If a Cantor series is eventually zero, its value is a finite sum of rational numbers and is rational. Conversely, consider the greedy expansion constructed in part (a), and put

$$
r_n:=n!\left(x-\sum_{k=1}^{n}\frac{c_k}{k!}\right)\in[0,1).
$$

If $$x=p/q$$ is rational, then for every $$n\ge q$$, $$n!x$$ is an integer. The finite sum multiplied by $$n!$$ is also an integer, so $$r_n$$ is an integer in $$[0,1)$$ and must equal zero. The recurrence then makes every later coefficient zero.

There is a qualification if “represented” allows either of the two nonunique expansions from part (a). As printed, the claim is false for such an unrestricted representation: by part (b),

$$
\frac12=\sum_{k=3}^{\infty}\frac{k-1}{k!},
$$

whose coefficients are not eventually zero. This is the noncanonical expansion of the rational number $$1/2$$; its canonical terminating expansion has $$c_2=1$$ and $$c_k=0$$ for $$k\ge3$$. Thus the equivalence holds for the unique expansion selected by the restriction in part (a), while the unrestricted statement needs this exception.

### Exercise 11

For each $$j\ge0$$, monotonicity gives

$$
2^j x_{2^{j+1}}
\le\sum_{n=2^j}^{2^{j+1}-1}x_n
\le2^j x_{2^j}.
$$

Summing the upper bounds shows that convergence of $$\sum_{j\ge0}2^j x_{2^j}$$ implies convergence of $$\sum_{n\ge1}x_n$$. Summing the lower bounds shows the converse, since

$$
\sum_{j\ge0}2^j x_{2^{j+1}}
=\frac12\sum_{j\ge1}2^j x_{2^j}.
$$

The finite initial terms do not affect convergence. This proves the Cauchy condensation theorem.

### Exercise 12

For $$s\ge0$$, the sequence $$x_k=k^{-s}$$ is decreasing and nonnegative. By Exercise 11, convergence of $$\sum_{k\ge1}k^{-s}$$ is equivalent to convergence of

$$
\sum_{j\ge0}2^j(2^j)^{-s}=\sum_{j\ge0}\left(2^{1-s}\right)^j.
$$

This geometric series converges exactly when $$2^{1-s}<1$$, that is, when $$s>1$$. The rationality assumption on $$s$$ is not needed.

### Exercise 13

Existence follows by repeated Euclidean division by $$g$$. Write $$m=gq_0+y_0$$ with $$0\le y_0<g$$, then divide $$q_0$$ by $$g$$ to obtain $$q_0=gq_1+y_1$$, and continue. The remainders $$y_j\in\{0,1,\ldots,g-1\}$$ are the base-$$g$$ digits, and the quotients eventually become zero. Substitution yields $$m=\sum_{j=0}^{L}y_jg^j$$.

For uniqueness, suppose two digit expansions differ and let $$L$$ be the largest index where their digits differ. The absolute contribution of the difference at index $$L$$ is at least $$g^L$$. All lower-index terms together have absolute value at most

$$
(g-1)\sum_{j=0}^{L-1}g^j=g^L-1,
$$

so they cannot cancel it. The digits are therefore unique, once leading zeros are ignored.

### Exercise 14

The positive odd terms form the divergent series

$$
\sum_{k=1}^{\infty}\frac1{2k-1},
$$

while the absolute values of the negative even terms form the convergent series

$$
\sum_{k=1}^{\infty}\frac1{(2k)^2}.
$$

Consequently the partial sums tend to $$+\infty$$, and the series diverges. Although the signs alternate and the terms tend to zero, the absolute values are not decreasing: for example, $$|x_2|=1/4<1/3=|x_3|$$. The Leibniz criterion therefore does not apply.

### Exercise 15

**(a)** Since $$z_n\to0$$, choose an increasing sequence of indices $$(n_k)$$ such that $$z_{n_k}<k^{-3}$$. Set $$x_{n_k}:=k^{-2}$$ and set $$x_n:=n^{-2}$$ at all other indices. Then $$(x_n)$$ is positive and tends to zero, and

$$
\sum_n x_n\le\sum_{k=1}^{\infty}k^{-2}+\sum_{n=1}^{\infty}n^{-2}<\infty.
$$

Along the selected indices,

$$
\frac{x_{n_k}}{z_{n_k}}>k,
$$

so $$\limsup_{n\to\infty}x_n/z_n=+\infty$$.

**(b)** Choose an increasing subsequence of indices $$(n_k)$$ with $$n_k\ge2^k$$. Set $$y_{n_k}:=z_{n_k}^2$$ and $$y_n:=1/n$$ at all other indices. Both definitions tend to zero along their respective indices, so $$y_n\to0$$. Moreover, $$\sum_n y_n=\infty$$: the selected reciprocal terms satisfy $$\sum_k1/n_k<\infty$$, so removing them from the harmonic series leaves a divergent sum. On the selected indices,

$$
\frac{y_{n_k}}{z_{n_k}}=z_{n_k}\longrightarrow0,
$$

and nonnegativity gives $$\liminf_{n\to\infty}y_n/z_n=0$$. The two concluding comparisons in the exercise follow by taking subsequences along which these upper and lower limits are attained.
