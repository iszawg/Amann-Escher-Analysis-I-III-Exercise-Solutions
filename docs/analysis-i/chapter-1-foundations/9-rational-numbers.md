# Chapter I — Foundations

## 9. The Rational Numbers

### Exercise 1

**(a)** For $$m\in\mathbb N$$, the definition of negative powers and the inverse law give

$$
a^{-m}=(a^{-1})^m=(a^m)^{-1}=\frac{1}{a^m}.
$$

If $$m\ge n$$, then $$a^{m-n}\cdot a^n=a^m$$, so $$a^{m-n}=\frac{a^m}{a^n}$$. If $$m<n$$, then

$$
a^{m-n}=a^{-(n-m)}=\frac{1}{a^{n-m}}=\frac{a^m}{a^n}.
$$

**(b)** First, the product law $$a^k\cdot a^\ell=a^{k+\ell}$$ follows from the usual law when both exponents are nonnegative. If one exponent is negative, write it as a reciprocal and cancel powers; if both are negative, multiply their reciprocals. Iterating the product law gives $$(a^k)^\ell=a^{k\ell}$$ for nonnegative $$\ell$$. For negative $$\ell$$, use $$(a^k)^{-1}=a^{-k}$$ and apply the same law. Finally, for $$k\ge0$$, commutativity gives $$a^k\cdot b^k=(ab)^k$$. If $$k=-r<0$$, then

$$
a^{-r}\cdot b^{-r}=\frac{1}{a^r b^r}=\frac{1}{(ab)^r}=(ab)^{-r}.
$$

This proves all three rules because every nonzero element of the field is invertible.

### Exercise 2

**(a)** By Euclidean division, every integer has a unique remainder in $$\{0,1,\ldots,n-1\}$$ modulo $$n$$. Thus $$\mathbb Z_n=\mathbb Z/n\mathbb Z$$ has exactly $$n$$ residue classes. Since $$0\mathbb Z=\{0\}$$, $$\mathbb Z_0=\mathbb Z/0\mathbb Z$$ is naturally isomorphic to $$\mathbb Z$$.

**(b)** If $$n$$ is composite, write $$n=ab$$ with $$1<a<n$$ and $$1<b<n$$. The classes $$[a]$$ and $$[b]$$ are nonzero in $$\mathbb Z_n$$, while

$$
[a][b]=[ab]=[n]=[0].
$$

So $$\mathbb Z_n$$ has zero divisors.

**(c)** Let $$p$$ be prime and let $$[a]\ne[0]$$ in $$\mathbb Z_p$$. Choose the representative $$a$$ with $$1\le a<p$$. Then $$\gcd(a,p)=1$$, so Bézout's identity gives $$u,v\in\mathbb Z$$ such that $$au+pv=1$$. Modulo $$p$$, this says $$[a][u]=[1]$$. Every nonzero element is therefore invertible, and $$\mathbb Z_p$$ is a field.

### Exercise 3

**(a)** Each of the $$n$$ elements of $$X$$ can either be included in a subset or omitted. These independent choices give $$2^n$$ subsets, so $$\operatorname{Num}\mathcal P(X)=2^n$$.

**(b)** Fix $$x\in X$$, which is possible because $$n>0$$. The map

$$
A\longmapsto A\mathbin{\triangle}\{x\}
$$

toggles whether $$x$$ belongs to $$A$$. It is its own inverse and changes the cardinality's parity, so it is a bijection from $$\mathcal P_{\rm even}(X)$$ to $$\mathcal P_{\rm odd}(X)$$. Their cardinalities are equal.

### Exercise 4

Write $$a=u/v$$ and $$b=r/s$$ with $$u,v,s\in\mathbb N^\times$$, $$r\in\mathbb Z$$, and $$v,s>0$$. Since $$a>0$$, we have $$u>0$$. It suffices to choose $$n\in\mathbb N$$ such that $$nus>rv$$, because then

$$
b=\frac{r}{s}<\frac{nu}{v}=na.
$$

The positive integer $$us$$ is at least $$1$$, and the natural numbers are unbounded in $$\mathbb Z$$. Hence such an $$n$$ exists (if $$rv<0$$, any sufficiently large positive $$n$$ works as well). Thus $$\mathbb Q$$ is Archimedean.

### Exercise 5

Let $$x=p/q$$ be a rational zero, written in lowest terms with $$p\in\mathbb Z$$, $$q\in\mathbb N^\times$$, and $$\gcd(p,q)=1$$. Substituting into $$\sum_{k=0}^n a_kX^k=0$$ and multiplying by $$q^n$$ gives

$$
a_np^n=-q\sum_{k=0}^{n-1}a_kp^kq^{n-1-k}.
$$

Thus $$q\mid a_np^n$$. Since $$p$$ and $$q$$ are relatively prime, Euclid's lemma gives $$q\mid a_n$$. Write $$a_n=qc$$ for some $$c\in\mathbb Z$$. Then $$x=p/q=pc/a_n$$, so $$x\in a_n^{-1}\mathbb Z$$.

### Exercise 6

For variables $$x_1,\ldots,x_n$$, put

$$
\Delta(x_1,\ldots,x_n)=\prod_{1\le j<k\le n}(x_j-x_k).
$$

The definition in the exercise says

$$
\operatorname{sign}\sigma=\frac{\Delta(\sigma(1),\ldots,\sigma(n))}{\Delta(1,\ldots,n)}.
$$

**(a)** The factors in the numerator contain every difference between two distinct elements of $$\{1,\ldots,n\}$$ exactly once, just as in the denominator. Each numerator factor is therefore the corresponding denominator factor or its negative. The quotient is $$1$$ or $$-1$$.

**(b)** For every permutation $$\pi$$ and every tuple of distinct variables, reordering the variables gives

$$
\Delta(x_{\pi(1)},\ldots,x_{\pi(n)})=(\operatorname{sign}\pi)\Delta(x_1,\ldots,x_n).
$$

Apply this first to $$x_j=\sigma(j)$$ and the reordering $$\tau$$, then to $$x_j=j$$ and the reordering $$\sigma$$. It follows that

$$
\operatorname{sign}(\sigma\circ\tau)=(\operatorname{sign}\sigma)(\operatorname{sign}\tau).
$$

Thus $$\operatorname{sign}$$ is a homomorphism into $$\{\pm1\}$$.

**(c)** If $$n\ge2$$, part (d) shows that the image has two elements. Every fiber of a group homomorphism has the size of its kernel, so

$$
|A_n|=|\ker(\operatorname{sign})|=\frac{|S_n|}{2}=\frac{n!}{2}.
$$

For $$n=1$$, $$S_1$$ consists only of the identity, so $$A_1$$ has one element.

**(d)** The identity has sign $$1$$. A transposition swaps two variables in $$\Delta$$, changing its sign, so every transposition has sign $$-1$$. For $$n\ge2$$ a transposition exists; hence the map takes both values and is surjective.

**(e)** Every permutation is a composition of transpositions. By multiplicativity and part (d), a composition of $$N$$ transpositions has sign $$(-1)^N$$. Since the sign depends only on the permutation, any two transposition decompositions have the same parity. In particular, $$N$$ is even for an even permutation and odd for an odd permutation.

### Exercise 7

The field operations on $$\mathbb Q$$ are those constructed in Theorem 9.2. Define

$$
\mathbb Q_{\ge0}=\left\{\frac{m}{n}:m\in\mathbb N,\ n\in\mathbb N^\times\right\}.
$$

This set is well defined: if $$m/n=m'/n'$$ with positive denominators and $$m\ge0$$, then $$mn'=m'n$$ implies $$m'\ge0$$. It contains $$0$$ and $$1$$, and is closed under addition and multiplication. Every rational number $$m/n$$ either lies in this set or has its negative in it, and the only rational number whose positive and negative both lie in it is $$0$$.

The order in the question is equivalent to

$$
x\le y\quad\Longleftrightarrow\quad y-x\in\mathbb Q_{\ge0},
$$

since for $$x=m/n$$ and $$y=m'/n'$$, $$y-x=(m'n-mn')/(nn')$$. The cone properties above give reflexivity, transitivity, antisymmetry, and totality. They also show that adding the same rational to both sides preserves the order, and multiplying an inequality by a nonnegative rational preserves it. The product of two positive rationals is positive, since their product is nonnegative and nonzero in the field. Since $$1\in\mathbb Q_{\ge0}$$ and $$1\ne0$$, this makes $$\mathbb Q$$ an ordered field.

Under the embedding $$\mathbb N\to\mathbb Q$$, $$m\mapsto m/1$$, the condition $$m/1\le n/1$$ is exactly $$n-m\in\mathbb N$$. Thus this order restricts to the usual order on $$\mathbb N$$.

### Exercise 8

Write $$[q_0;\ldots,q_k]$$ for the continued fraction displayed in the exercise. For a nonnegative rational in lowest terms, write $$x=r/s$$, where $$r\in\mathbb N$$, $$s\in\mathbb N^\times$$, and $$\gcd(r,s)=1$$. Apply Euclidean division:

$$
r=q_0s+r_1,\qquad 0\le r_1<s.
$$

If $$r_1=0$$, then $$x=q_0$$ is an integer. Otherwise, repeatedly divide the previous divisor by the positive remainder:

$$
s=q_1r_1+r_2,\quad r_1=q_2r_2+r_3,\quad\ldots,\quad r_{k-1}=q_kr_k,
$$

where the positive remainders strictly decrease, so the process terminates. The division equations give

$$
\frac rs=q_0+\frac1{q_1+\dfrac1{q_2+\dfrac1{\ddots+\dfrac1{q_k}}}}.
$$

The Euclidean algorithm is unique at every step. It gives the unique canonical expansion, with $$q_k\ge2$$ when $$k\ge1$$, which is the condition $$q_k\ne1$$ stated in the exercise.

The printed definition requires $$q_0\in\mathbb N^\times$$, but its hint allows $$q_0\in\mathbb N$$. Allowing $$q_0=0$$ is necessary to represent $$x=0$$ as $$[0]$$. A terminal $$1$$ is the noncanonical alternative, since it can be absorbed into the preceding term:

$$
[q_0;\ldots,q_{k-1},1]=[q_0;\ldots,q_{k-1}+1].
$$

For example, $$2=[2]=[1;1]$$, so a terminal-one expansion is not unique among all finite expansions. The exercise's condition $$q_k\ne1$$ excludes precisely this ambiguity.

### Exercise 9

Every rational has a unique reduced representation $$p/q$$ with $$p\in\mathbb Z$$, $$q\in\mathbb N^\times$$, and $$\gcd(|p|,q)=1$$. Define its height by $$H(p/q)=|p|+q$$, and set

$$
\frac pq\prec\frac rs
\quad\Longleftrightarrow\quad
(H(p/q),p,q)<_{\mathrm{lex}}(H(r/s),r,s),
$$

where $$<_{\mathrm{lex}}$$ is lexicographic order on $$\mathbb N\times\mathbb Z\times\mathbb N^\times$$. This is a total order because reduced representations are unique. For each fixed height there are only finitely many pairs $$(p,q)$$, since $$|p|+q$$ is fixed. Given any nonempty subset of $$\mathbb Q$$, choose the least height that occurs in it; among the finitely many rationals of that height in the subset, choose the least pair $$(p,q)$$ lexicographically. This element is the subset's $$\prec$$-least element. Hence $$\prec$$ is a well order on $$\mathbb Q$$.
