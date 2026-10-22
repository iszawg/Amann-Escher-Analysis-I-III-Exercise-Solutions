# Chapter I — Foundations

## 5. The Natural Numbers

### Exercise 1

**(a)** Let $$S_n=\sum_{k=0}^{n}a_k$$ and $$T_n=\sum_{k=0}^{n}b_k$$. We prove the first identity by induction on $$n$$. It is immediate for $$n=0$$. If it holds through $$n$$, associativity and commutativity give

$$
S_{n+1}+T_{n+1}
=(S_n+a_{n+1})+(T_n+b_{n+1})
=(S_n+T_n)+(a_{n+1}+b_{n+1})
=\sum_{k=0}^{n+1}(a_k+b_k).
$$

The product identity is proved in the same way, using associativity and commutativity of multiplication:

$$
\left(\prod_{k=0}^{n+1}a_k\right)\left(\prod_{k=0}^{n+1}b_k\right)
=\left(\prod_{k=0}^{n}a_k\right)\left(\prod_{k=0}^{n}b_k\right)(a_{n+1}b_{n+1})
=\prod_{k=0}^{n+1}(a_kb_k).
$$

For the double-sum identity, distributivity implies by induction on the number of terms that

$$
\left(\sum_{j=0}^{m}a_j\right)z=\sum_{j=0}^{m}(a_jz),
\qquad
a\left(\sum_{k=0}^{n}b_k\right)=\sum_{k=0}^{n}(ab_k).
$$

Applying these two finite distributive laws successively yields

$$
\left(\sum_{j=0}^{m}a_j\right)\left(\sum_{k=0}^{n}b_k\right)
=\sum_{j=0}^{m}\sum_{k=0}^{n}a_jb_k,
$$

which is the sum over all pairs $$0\le j\le m$$ and $$0\le k\le n$$.

**(b)** Let $$\diamond$$ be associative with identity $$e$$, and define $$a^0=e$$ and $$a^{r+1}=a^r\diamond a$$. The identity $$e^r=e$$ follows by induction: it holds for $$r=0$$, and $$e^{r+1}=e^r\diamond e=e\diamond e=e$$.

For fixed $$n$$, induction on $$m$$ gives

$$
a^n\diamond a^m=a^{n+m}.
$$

The base case is $$a^n\diamond e=a^n$$. If the identity holds for $$m$$, then

$$
a^n\diamond a^{m+1}
=(a^n\diamond a^m)\diamond a
=a^{n+m}\diamond a
=a^{n+m+1}.
$$

Now induction on $$m$$ gives $$\left(a^n\right)^m=a^{nm}$$: the case $$m=0$$ is $$e=a^0$$, and

$$
\left(a^n\right)^{m+1}
=\left(a^n\right)^m\diamond a^n
=a^{nm}\diamond a^n
=a^{nm+n}.
$$

Finally, suppose $$a\diamond b=b\diamond a$$. Induction on $$r$$ proves $$a^r\diamond b^r=(a\diamond b)^r$$. It is true for $$r=0$$. Also, induction using associativity shows that $$a$$ commutes with every power $$b^r$$. Thus in the induction step we may regroup the factors as follows:

$$
a^{r+1}\diamond b^{r+1}
=(a^r\diamond a)\diamond(b^r\diamond b)
=(a^r\diamond b^r)\diamond(a\diamond b)
=(a\diamond b)^r\diamond(a\diamond b)
=(a\diamond b)^{r+1}.
$$

### Exercise 2

**(a)** For $$n=0$$, both sides are zero. If the formula holds for $$n$$, then

$$
\sum_{k=0}^{n+1}k
=\frac{n(n+1)}{2}+(n+1)
=\frac{(n+1)(n+2)}{2}.
$$

Thus the formula holds for every $$n\in\mathbb N$$.

**(b)** The formula is true for $$n=0$$. Assuming it holds for $$n$$, we obtain

$$
\begin{aligned}
\sum_{k=0}^{n+1}k^2
&=\frac{n(n+1)(2n+1)}{6}+(n+1)^2\\
&=\frac{(n+1)(n+2)(2n+3)}{6}.
\end{aligned}
$$

This is the claimed formula with $$n+1$$ in place of $$n$$.

### Exercise 3

**(a)** At $$n=2$$, $$n+1=3<4=2^n$$. If $$n\ge2$$ and $$n+1<2^n$$, then

$$
n+2\le2(n+1)<2\cdot2^n=2^{n+1}.
$$

Induction proves the inequality for all $$n\ge2$$.

**(b)** For $$n=0$$, $$a^n=1>0=n^2$$; for $$n=1$$, $$a>1$$. At $$n=2$$, $$a^2\ge9>4$$. If $$n\ge2$$ and $$a^n>n^2$$, then

$$
a^{n+1}=a\,a^n>3n^2\ge(n+1)^2,
$$

where the last inequality holds for $$n\ge2$$. This proves the claim for every $$n\in\mathbb N$$.

### Exercise 4

We use induction on the number of elements of $$A$$. If $$A=\varnothing$$, then $$\mathcal P(A)=\{\varnothing\}$$ has $$1=2^0$$ element. Suppose $$|A|=n$$ and choose $$x\notin A$$. The subsets of $$A\cup\{x\}$$ split into those not containing $$x$$ and those containing $$x$$. Each group is in bijection with $$\mathcal P(A)$$, by respectively leaving a subset unchanged or adjoining $$x$$. The two groups are disjoint, so

$$
|\mathcal P(A\cup\{x\})|=2|\mathcal P(A)|=2\cdot2^n=2^{n+1}.
$$

### Exercise 5

**(a)** We use induction on $$n$$, proving the assertion for every $$m\le n$$ at once. It holds for $$n=0$$. Assume it holds for $$n$$ and consider $$m\le n+1$$. For $$m=0$$ or $$m=n+1$$, the quotient $$\frac{(n+1)!}{m!(n+1-m)!}$$ is $$1$$. For $$1\le m\le n$$, use the given decomposition

$$
(n+1)!=n!(n+1-m)+n!m.
$$

The first summand is divisible by $$m!(n+1-m)!$$ because its quotient is $$\frac{n!}{m!(n-m)!}$$. The second is divisible by the same number because its quotient is $$\frac{n!}{(m-1)!(n+1-m)!}$$. Both quotients are integers by the induction hypothesis, so their sum is divisible by $$m!(n+1-m)!$$.

**(b)** Write $$\binom{n}{m}=0$$ when $$m>n$$, as in the question.

**(i)** For $$0\le m\le n$$, symmetry follows directly from the definition:

$$
\binom{n}{m}=\frac{n!}{m!(n-m)!}=\binom{n}{n-m}.
$$

**(ii)** For $$1\le m\le n$$, putting the two terms over a common denominator gives

$$
\binom{n}{m-1}+\binom{n}{m}
=\frac{n!m}{m!(n-m+1)!}+\frac{n!(n-m+1)}{m!(n-m+1)!}
=\frac{(n+1)!}{m!(n+1-m)!}
=\binom{n+1}{m}.
$$

**(iii)** We use induction on $$n$$. The sum is $$1=2^0$$ for $$n=0$$. Pascal's identity from (ii), together with $$\binom{n+1}{0}=\binom{n+1}{n+1}=1$$, gives

$$
\sum_{k=0}^{n+1}\binom{n+1}{k}
=2\sum_{k=0}^{n}\binom{n}{k}.
$$

Thus the sum is $$2^{n+1}$$ if it is $$2^n$$ at stage $$n$$.

**(iv)** We use induction on $$m$$. For $$m=0$$, both sides equal $$1$$. If the identity holds at $$m$$, then Pascal's identity yields

$$
\begin{aligned}
\sum_{k=0}^{m+1}\binom{n+k}{n}
&=\binom{n+m+1}{n+1}+\binom{n+m+1}{n}\\
&=\binom{n+m+2}{n+1}.
\end{aligned}
$$

### Exercise 6

By Pascal's identity, for $$L=m+n+k$$, using the convention $$\binom{L}{-1}=0$$,

$$
2\binom{L}{k}-\binom{L+1}{k}
=\binom{L+1}{k}-2\binom{L}{k-1}.
$$

Consequently,

$$
\begin{aligned}
S(m,n)
&=\sum_{k=0}^{n}2^{n-k}\left[\binom{m+n+k+1}{k}-2\binom{m+n+k}{k-1}\right]\\
&=\sum_{k=0}^{n}2^{n-k}\binom{m+n+k+1}{k}
-\sum_{j=0}^{n-1}2^{n-j}\binom{m+n+j+1}{j}\\
&=\binom{m+2n+1}{n}.
\end{aligned}
$$

In the second line, the index in the second sum is shifted by $$j=k-1$$; all terms through $$k=n-1$$ cancel.

### Exercise 7

Suppose first that $$p$$ is prime and $$p\mid mn$$. If $$p\mid m$$, the desired disjunction already holds. Otherwise, $$\gcd(p,m)=1$$, so Bézout's identity gives integers $$u,v$$ with $$up+vm=1$$. Multiplying by $$n$$ gives $$upn+vmn=n$$. Both terms on the left are divisible by $$p$$, hence $$p\mid n$$.

Conversely, if $$p>1$$ is not prime, write $$p=ab$$ with $$1<a<p$$ and $$1<b<p$$. Then $$p\mid ab$$, but neither $$p\mid a$$ nor $$p\mid b$$. Thus the stated divisibility property fails. Therefore it holds exactly for prime $$p$$.

### Exercise 8

**(a)** For each integer $$k$$ with $$2\le k\le n+1$$,

$$
(n+1)!+k=k\left(\frac{(n+1)!}{k}+1\right).
$$

The quotient is an integer greater than $$1$$, so each of the $$n$$ displayed consecutive numbers is composite. By (b), there are infinitely many primes and hence primes on both sides of any such finite block. The consecutive primes bracketing the block therefore differ by at least $$n+1$$. Since $$n$$ is arbitrary, prime gaps are arbitrarily large.

**(b)** Suppose there were only finitely many primes, say $$p_0,\ldots,p_m$$. Let

$$
q=p_0p_1\cdots p_m+1.
$$

Since $$q>1$$, it has a prime divisor. But division by any $$p_i$$ leaves remainder $$1$$, so none of the listed primes divides $$q$$. This contradicts the assumption that the list contains every prime.

### Exercise 9

The induction step fails when $$n=1$$. If $$M=\{a,b\}$$ with $$a\ne b$$, then

$$
M_a=M\setminus\{a\}=\{b\},\qquad M_b=M\setminus\{b\}=\{a\},
$$

so $$M_a\cap M_b=\varnothing$$. There is no element $$c$$ in the intersection to which the induction hypothesis can be applied. The base case for one person therefore does not establish the claim for two people.

### Exercise 10

The powers of $$2$$ modulo $$7$$ have period $$3$$, since $$2^3\equiv1\pmod 7$$. Also $$2^n\equiv1$$ or $$2\pmod 3$$ according as $$n$$ is even or odd. Thus the exponents $$2^n$$ and $$2^{n+1}$$ are congruent to $$1$$ and $$2$$ modulo $$3$$, in some order. It follows that the two powers in the expression are congruent to $$2$$ and $$4$$ modulo $$7$$, in some order. Hence

$$
1+2^{2^n}+2^{2^{n+1}}\equiv1+2+4\equiv0\pmod 7.
$$

### Exercise 11

**Existence.** Start with $$q_0=n$$ and repeatedly apply Euclidean division by $$g$$:

$$
q_j=gq_{j+1}+y_j,\qquad 0\le y_j<g.
$$

As long as $$q_j>0$$, the quotient satisfies $$q_{j+1}<q_j$$. The process therefore terminates at some $$q_{\ell+1}=0$$, with $$q_\ell>0$$. Substituting the divisions back gives

$$
n=\sum_{j=0}^{\ell}y_jg^j,
\qquad y_j\in\{0,\ldots,g-1\},\quad y_\ell>0.
$$

**Uniqueness.** Suppose there are two such representations, with highest indices $$\ell$$ and $$m$$. If, for example, $$\ell<m$$, then the first representation is at most $$g^{\ell+1}-1$$, while the second is at least $$g^m\ge g^{\ell+1}$$, a contradiction. Hence $$\ell=m$$. Reducing both representations modulo $$g$$ shows $$y_0=z_0$$, because both digits lie between $$0$$ and $$g-1$$. Subtract these equal digits and divide by $$g$$; repeating this argument gives $$y_j=z_j$$ for every $$j\le\ell$$. The representation is unique.
