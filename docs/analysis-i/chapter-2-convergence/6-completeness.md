# Chapter II — Convergence

## 6. Completeness

### Exercise 1

Let $$C:=\max\{\|(\alpha,\beta)\|,\|(\beta,\alpha)\|\}$$. For $$m>n$$, the triangle inequality gives

$$
\|s_m-s_n\|
\le C\sum_{k=n+1}^{m}\frac1{k^2}
\le C\int_n^\infty\frac{dt}{t^2}
=\frac Cn.
$$

Thus $$(s_n)$$ is a Cauchy sequence in $$\mathbb R^2$$. Since $$\mathbb R^2$$ is complete, $$(s_n)$$ converges.

### Exercise 2

Write $$c:=d(x_1,x_0)$$. The hypothesis and induction imply

$$
d(x_{k+1},x_k)\le c\alpha^k,\qquad k\ge0.
$$

For $$m>n$$, the triangle inequality therefore gives

$$
d(x_m,x_n)\le\sum_{k=n}^{m-1}d(x_{k+1},x_k)
\le c\sum_{k=n}^{m-1}\alpha^k
\le\frac{c\alpha^n}{1-\alpha}.
$$

The last bound tends to zero as $$n\to\infty$$, so $$(x_n)$$ is Cauchy. Completeness of $$X$$ implies that $$(x_n)$$ converges in $$X$$.

### Exercise 3

Call an index $$n$$ a peak if $$x_n\ge x_m$$ for every $$m>n$$. If there are infinitely many peaks, list them in increasing order as $$(n_j)$$. Then $$x_{n_{j+1}}\le x_{n_j}$$, so $$(x_{n_j})$$ is nonincreasing.

Otherwise, there are only finitely many peaks. Choose $$n_1$$ larger than all of them. Since $$n_1$$ is not a peak, some $$n_2>n_1$$ satisfies $$x_{n_2}>x_{n_1}$$. Repeating this choice produces a strictly increasing subsequence. In either case, the original sequence has a monotone subsequence.

### Exercise 4

**(a)** Let $$(x_n)$$ be Cauchy in a closed subset $$D$$ of a complete metric space $$M$$. It is also Cauchy in $$M$$, so it converges to some $$x\in M$$. Since $$D$$ is closed and every $$x_n\in D$$, its limit $$x$$ belongs to $$D$$. Thus $$D$$ is complete in the induced metric.

**(b)** A closed subspace $$F$$ of a Banach space $$E$$ is closed in the complete metric space underlying $$E$$. Part (a) shows that $$F$$ is complete in the induced metric. With its induced norm it is a normed vector space, hence a Banach space.

**(c)** First, $$\ell^\infty$$ is complete. Let $$(x^{(j)})$$ be Cauchy in the supremum norm. For each coordinate $$k$$, $$(x_k^{(j)})_j$$ is Cauchy in $$\mathbb K$$, so it has a limit $$x_k$$. Write $$x=(x_k)$$. Choose $$J$$ such that $$\|x^{(j)}-x^{(\ell)}\|_\infty<1$$ whenever $$j,\ell\ge J$$. Letting $$\ell\to\infty$$ coordinatewise shows that $$|x_k-x_k^{(J)}|\le1$$ for every $$k$$. Hence $$x$$ is bounded and belongs to $$\ell^\infty$$.

Given $$\varepsilon>0$$, choose $$J$$ so that $$\|x^{(j)}-x^{(\ell)}\|_\infty<\varepsilon/2$$ for all $$j,\ell\ge J$$. For fixed $$j\ge J$$, take $$\ell\to\infty$$ in each coordinate to obtain $$|x_k^{(j)}-x_k|\le\varepsilon/2$$ for all $$k$$. Thus $$\|x^{(j)}-x\|_\infty\le\varepsilon/2<\varepsilon$$, proving convergence in $$\ell^\infty$$.

The subspaces $$c$$ and $$c_0$$ are closed in $$\ell^\infty$$. Indeed, suppose that $$x^{(j)}\to x$$ uniformly and each $$x^{(j)}$$ is convergent. Given $$\varepsilon>0$$, choose $$j$$ with $$\|x^{(j)}-x\|_\infty<\varepsilon/3$$, and then choose $$K$$ so that $$|x_p^{(j)}-x_q^{(j)}|<\varepsilon/3$$ whenever $$p,q\ge K$$. It follows that $$|x_p-x_q|<\varepsilon$$ for $$p,q\ge K$$. Thus $$x$$ is a Cauchy sequence of scalars and therefore converges, so $$x\in c$$.

If, in addition, each $$x^{(j)}\in c_0$$, choose $$j$$ with $$\|x^{(j)}-x\|_\infty<\varepsilon/2$$. Since $$x^{(j)}_k\to0$$, for all sufficiently large $$k$$ we have $$|x_k|\le|x_k-x_k^{(j)}|+|x_k^{(j)}|<\varepsilon$$. Hence $$x\in c_0$$. By part (b), the closed subspaces $$c$$ and $$c_0$$ of the Banach space $$\ell^\infty$$ are Banach spaces.

**(d)** Let $$x\in\overline D$$. For each $$n\ge1$$, choose $$x_n\in D$$ with $$d(x_n,x)<1/n$$. Then $$(x_n)$$ converges to $$x$$ in $$M$$, so it is Cauchy. Completeness of $$D$$ gives a limit $$y\in D$$ for this sequence. Limits in a metric space are unique, so $$y=x$$ and $$x\in D$$. Therefore $$D$$ is closed in $$M$$.

### Exercise 5

Let $$\mathcal C$$ be the ring of rational Cauchy sequences, let $$c_0$$ be its ideal of null sequences, and let $$P$$ be the set of sequences that are eventually bounded below by a positive rational number. The order on the quotient is defined by

$$
[r]\le[s]\quad\Longleftrightarrow\quad s-r\in P\cup c_0.
$$

If $$p,q\in P$$, then $$p+q\in P$$ and $$pq\in P$$. If $$p\in P$$ and $$z\in c_0$$, then $$p+z\in P$$: eventually, $$p_n\ge1/N$$ and $$|z_n|<1/(2N)$$ for some $$N\in\mathbb N^\times$$. Also $$pz\in c_0$$, since every Cauchy sequence is bounded. Sums of elements of $$c_0$$ and products of two such elements remain in $$c_0$$.

Suppose $$[r]\le[s]$$ and $$[s]\le[t]$$. Then $$s-r,t-s\in P\cup c_0$$. The closure properties just shown imply

$$
t-r=(t-s)+(s-r)\in P\cup c_0,
$$

so $$[r]\le[t]$$. This proves transitivity.

Translation preserves the order because $$[s+u]-[r+u]=[s-r]$$. Also, if $$[r]\ge[0]$$ and $$[s]\ge[0]$$, then representatives lie in $$P\cup c_0$$, whose products again lie in $$P\cup c_0$$. Hence $$[rs]\ge[0]$$. In particular, multiplication by a nonnegative element preserves the order: if $$[r]\le[s]$$ and $$[u]\ge[0]$$, then $$[su]-[ru]=[(s-r)u]\ge[0]$$. These are the compatibility properties for an ordered ring.

### Exercise 6

**(a)** For each $$j\ge1$$, the block of terms with $$2^{j-1}<k\le2^j$$ contains $$2^{j-1}$$ terms, each at least $$1/2^j$$. Therefore

$$
x_{2^j}=\sum_{k=1}^{2^j}\frac1k\ge1+\frac j2.
$$

Thus $$(x_n)$$ is unbounded. Every Cauchy sequence in $$\mathbb R$$ is bounded, so $$(x_n)$$ is not Cauchy.

**(b)** For a fixed $$m\in\mathbb N^\times$$,

$$
0\le x_{n+m}-x_n=\sum_{k=n+1}^{n+m}\frac1k
\le\frac{m}{n+1}\longrightarrow0.
$$

### Exercise 7

For $$m>n$$, positivity and comparison with an integral give

$$
0\le x_m-x_n=\sum_{k=n+1}^{m}\frac1{k^2}
\le\int_n^m\frac{dt}{t^2}
\le\frac1n.
$$

The upper bound tends to zero as $$n\to\infty$$, so $$(x_n)$$ is Cauchy in $$\mathbb R$$. Since all its terms are rational and the metric on $$\mathbb Q$$ is induced from $$\mathbb R$$, it is also a Cauchy sequence in $$\mathbb Q$$.
