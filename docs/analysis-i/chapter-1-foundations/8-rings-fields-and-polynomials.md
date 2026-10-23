# Chapter I — Foundations

## 8. Rings, Fields and Polynomials

### Exercise 1

**(a)** Since $$a$$ and $$b$$ commute, we can expand and cancel consecutive terms:

$$
(a-b)\sum_{j=0}^{n}a^j b^{n-j}
=\sum_{j=0}^{n}a^{j+1}b^{n-j}-\sum_{j=0}^{n}a^j b^{n+1-j}
=a^{n+1}-b^{n+1}.
$$

**(b)** Apply part (a) with $$b=1$$. This gives

$$
a^{n+1}-1=(a-1)\sum_{j=0}^{n}a^j.
$$

### Exercise 2

Let $$S=\sum_{k\in\mathbb N}X^k$$, the formal power series whose every coefficient is $$1_R$$. Multiplication by $$X$$ shifts the coefficients one place to the right, so the constant coefficient of $$(1-X)S$$ is $$1_R$$ and every positive-degree coefficient is $$1_R-1_R=0$$. Thus $$(1-X)S=1$$. The same coefficient calculation gives $$S(1-X)=1$$; here $$X$$ commutes with every power of itself and with the coefficients $$1_R$$. Hence

$$
(1-X)\sum_{k\in\mathbb N}X^k
=\left(\sum_{k\in\mathbb N}X^k\right)(1-X)=1
$$

in $$R[[X]]$$.

### Exercise 3

Let $$p,q\in K[X]$$ be nonzero, with leading terms $$a_mX^m$$ and $$b_nX^n$$. Their product has coefficient $$a_mb_n$$ at degree $$m+n$$. Since $$K$$ is a field, $$a_mb_n\ne0$$. Thus $$pq\ne0$$, so $$K[X]$$ has no zero divisors.

### Exercise 4

Suppose a finite field $$K$$ had an order making it an ordered field. Then $$1>0$$, and adding $$1$$ repeatedly gives

$$
0<1<1+1<1+1+1<\cdots.
$$

These are infinitely many distinct elements of $$K$$, contradicting finiteness. Therefore no finite field can be ordered.

### Exercise 5

**(a)** The operations on $$R[[X_1,\ldots,X_m]]$$ are defined coefficientwise by finite sums. The zero series and additive inverse are defined coefficientwise, so the series form an Abelian group under addition. Convolution multiplication is associative because, for each fixed multi-index $$\alpha$$, both $$(pq)r$$ and $$p(qr)$$ sum the same finitely many terms $$p_\beta q_\gamma r_\delta$$ with $$\beta+\gamma+\delta=\alpha$$. Distributivity follows by distributing these finite sums. The series with coefficient $$1_R$$ at $$0$$ and zero elsewhere is a multiplicative identity. If $$R$$ is commutative, then the convolution product is commutative by interchanging the two summation indices. This proves the ring and commutativity assertions.

The sum or product of two finitely supported coefficient families is again finitely supported, so $$R[X_1,\ldots,X_m]$$ is a subring. The map

$$
R\longrightarrow R[X_1,\ldots,X_m],\qquad a\longmapsto aX^0
$$

preserves addition, multiplication and the unity, and is bijective onto the constant polynomials. Hence it is an isomorphism onto that subring.

**(b)** Let $$R$$ be commutative. Evaluation is additive by distributing finite sums. For multiplication, the coefficient of each monomial in $$pq$$ is a finite convolution sum; evaluating and regrouping these finite sums gives

$$
(pq)(x)=\left(\sum_\alpha p_\alpha x^\alpha\right)
\left(\sum_\beta q_\beta x^\beta\right)=p(x)q(x).
$$

Also the constant polynomial $$1$$ evaluates to the constant function $$1$$. Thus evaluation is a ring homomorphism into the function ring $$R^{R^m}$$.

### Exercise 6

**(a)** If $$1\in I$$, then every $$r\in R$$ satisfies $$r=r1\in RI=I$$, so $$I=R$$. Conversely, if $$I=R$$, then $$1\in I$$. Therefore $$I$$ is proper exactly when $$1\notin I$$.

**(b)** The sets $$\{0\}$$ and $$K$$ are ideals. If an ideal $$I$$ of the field $$K$$ contains some nonzero $$a$$, then $$a^{-1}a=1\in I$$, so part (a) gives $$I=K$$. There are no other ideals.

**(c)** The kernel of a ring homomorphism is an additive subgroup. If $$x\in\ker(\varphi)$$ and $$r\in R$$, then

$$
\varphi(rx)=\varphi(r)\varphi(x)=0,\qquad
\varphi(xr)=\varphi(x)\varphi(r)=0.
$$

Thus $$R\ker(\varphi)=\ker(\varphi)R=\ker(\varphi)$$, and the kernel is an ideal.

**(d)** An intersection of ideals is an additive subgroup, since every ideal contains zero and is closed under sums and additive inverses. It is also closed under multiplication on either side by elements of $$R$$. Hence it is an ideal. With the usual convention, an empty intersection is $$R$$.

**(e)** Suppose $$a'=a+i$$ and $$b'=b+j$$ for $$i,j\in I$$. Then

$$
a'b'-ab=aj+ib+ij\in I,
$$

because $$I$$ absorbs multiplication by elements of $$R$$. Therefore $$a'b'+I=ab+I$$, so the proposed multiplication on cosets is well defined. The quotient already has an Abelian group structure under addition; associativity and distributivity of the coset multiplication follow from those laws in $$R$$. Its unity is $$1+I$$. Finally, the quotient map $$p(a)=a+I$$ preserves addition and satisfies $$p(a)p(b)=ab+I=p(ab)$$. Thus $$R/I$$ is a ring and $$p$$ is a ring homomorphism.

### Exercise 7

Use the coordinate-permutation action on multi-indices from Exercise 7.6(d). With ordinary function composition, this is $$(\sigma\cdot\alpha)_i=\alpha_{\sigma^{-1}(i)}$$. For $$p=\sum_\alpha a_\alpha X^\alpha$$, the induced action is

$$
\sigma\cdot p=\sum_\alpha a_\alpha X^{\sigma\cdot\alpha}.
$$

**(a)** The identity permutation fixes every exponent, and the action law on multi-indices gives $$\sigma\cdot(\tau\cdot p)=(\sigma\tau)\cdot p$$. Since coordinate permutations preserve addition of multi-indices,

$$
\sigma\cdot(X^\alpha X^\beta)
=X^{\sigma\cdot(\alpha+\beta)}
=X^{\sigma\cdot\alpha}X^{\sigma\cdot\beta}.
$$

By distributivity, this proves that the action respects polynomial multiplication; it also respects addition. Hence it defines an action on the polynomial ring by ring homomorphisms.

**(b)** The map $$p\mapsto\sigma\cdot p$$ has inverse $$p\mapsto\sigma^{-1}\cdot p$$ by the action law. It is therefore a bijective ring homomorphism, hence an automorphism.

**(c)** The orbit consists of all distinct permutations of the exponent vector:

1. $$S_3\cdot X_1=\{X_1,X_2,X_3\}$$.
2. $$S_3\cdot X_1^2=\{X_1^2,X_2^2,X_3^2\}$$.
3. For $$X_1^2X_2X_3^3$$ the exponent vector is a permutation of $$(2,1,3)$$, so the orbit is

   $$
   \begin{aligned}
   S_3\cdot(X_1^2X_2X_3^3)=\{&X_1^2X_2X_3^3,\ X_1^2X_2^3X_3,\ X_1X_2^2X_3^3,\\
   &X_1X_2^3X_3^2,\ X_1^3X_2X_3^2,\ X_1^3X_2^2X_3\}.
   \end{aligned}
   $$

**(d)** The action permutes the monomials and leaves their coefficients attached to the permuted exponents. A polynomial is fixed by every permutation exactly when its coefficients are constant on each orbit of multi-indices. Grouping terms by these orbits gives precisely

$$
p=\sum_{[\alpha]\in\mathbb N^m/S_m}a_{[\alpha]}
\left(\sum_{\beta\in[\alpha]}X^\beta\right),
$$

where only finitely many coefficients $$a_{[\alpha]}$$ are nonzero. This also proves the converse.

**(e)** In degree at most three, the exponent-vector orbits correspond to the partitions of $$0,1,2,3$$ into at most three parts. Thus every such symmetric polynomial is a unique linear combination over $$R$$ of

$$
1,\quad X_1+X_2+X_3,\quad
X_1^2+X_2^2+X_3^2,\quad X_1X_2+X_1X_3+X_2X_3,
$$

$$
X_1^3+X_2^3+X_3^3,\quad
\sum_{i\ne j}X_i^2X_j,\quad X_1X_2X_3.
$$

These are the orbit sums for the exponent patterns $$(),(1),(2),(1,1),(3),(2,1),(1,1,1)$$, respectively.

**(f)** A permutation of the variables permutes the subsets of $$\{1,\ldots,m\}$$ having exactly $$k$$ elements. It therefore permutes the summands in $$s_k$$, leaving their sum unchanged. Hence each elementary symmetric polynomial $$s_k$$ is fixed by $$S_m$$.

**(g)** To obtain a term of degree $$m-k$$ in $$X$$ when expanding $$\prod_{j=1}^m(X-X_j)$$, choose $$-X_j$$ from exactly $$k$$ factors and $$X$$ from the other $$m-k$$ factors. Summing over all such choices gives coefficient $$(-1)^k s_k$$. Therefore

$$
\prod_{j=1}^m(X-X_j)=\sum_{k=0}^m(-1)^k s_kX^{m-k},\qquad s_0=1.
$$

### Exercise 8

**(a)** In the product $$p[1]^m$$, the coefficient of $$X^k$$ counts the choices of exponents $$\alpha_1,\ldots,\alpha_m\in\mathbb N$$ with sum $$k$$. Encode such a choice by a row of $$k$$ stars separated into $$m$$ groups by $$m-1$$ dividers; empty groups represent zero exponents. Choosing the divider positions among the total $$m+k-1$$ positions gives $$\binom{m+k-1}{m-1}=\binom{m+k-1}{k}$$ choices. Thus

$$
p[1]^m=\sum_{k\in\mathbb N}\binom{m+k-1}{k}X^k.
$$

**(b)** In the product $$\prod_{j=1}^m p[a_j]$$, choosing the term $$a_j^{\alpha_j}X^{\alpha_j}$$ from factor $$j$$ contributes $$a^\alpha X^{|\alpha|}$$. Grouping the finitely many terms of each total degree yields

$$
\prod_{j=1}^m p[a_j]
=\sum_{k\in\mathbb N}\left(\sum_{|\alpha|=k}a^\alpha\right)X^k.
$$

**(c)** The coefficient counted in part (a) is also the number of multi-indices $$\alpha\in\mathbb N^m$$ with $$|\alpha|=k$$. Consequently,

$$
\sum_{\substack{\alpha\in\mathbb N^m\\|\alpha|=k}}1
=\binom{m+k-1}{k}.
$$

**(d)** Add a slack coordinate $$\alpha_{m+1}=k-|\alpha|$$. This is a bijection from the multi-indices with $$|\alpha|\le k$$ to the multi-indices in $$\mathbb N^{m+1}$$ whose coordinates sum to $$k$$. Applying stars and bars with $$m+1$$ coordinates gives

$$
\sum_{\substack{\alpha\in\mathbb N^m\\|\alpha|\le k}}1
=\binom{m+k}{k}.
$$

### Exercise 9

For each subset $$A\subseteq X$$, let $$\mathbf 1_A:X\to\mathbb F_2$$ be its indicator function. The map $$A\mapsto\mathbf 1_A$$ is a bijection from $$\mathcal P(X)$$ to $$\mathbb F_2^X$$. Pointwise addition of indicator functions corresponds to symmetric difference, and pointwise multiplication corresponds to intersection:

$$
\mathbf 1_{A\triangle B}=\mathbf 1_A+\mathbf 1_B,\qquad
\mathbf 1_{A\cap B}=\mathbf 1_A\mathbf 1_B.
$$

The function ring $$\mathbb F_2^X$$ is commutative, with zero the zero function and unity the constant-one function. The bijection therefore transports this ring structure to $$\mathcal P(X)$$; its zero is $$\varnothing$$ and its unity is $$X$$.

### Exercise 10

**(a)** Put $$x=|a|$$ and $$y=|b|$$. The triangle inequality gives $$|a+b|\le x+y$$. For nonnegative $$u\le v$$,

$$
\frac{v}{1+v}-\frac{u}{1+u}
=\frac{v-u}{(1+u)(1+v)}\ge0,
$$

so $$t/(1+t)$$ is increasing on nonnegative elements. Also,

$$
\frac{x}{1+x}+\frac{y}{1+y}-\frac{x+y}{1+x+y}
=\frac{xy(2+x+y)}{(1+x)(1+y)(1+x+y)}\ge0.
$$

Combining these inequalities proves

$$
\frac{|a+b|}{1+|a+b|}\le\frac{|a|}{1+|a|}+\frac{|b|}{1+|b|}.
$$

**(b)** The assumption $$a/b<c/d$$ and positivity of $$b,d$$ imply $$bc-ad>0$$. Then

$$
\frac{a+c}{b+d}-\frac ab=\frac{bc-ad}{b(b+d)}>0,
\qquad
\frac cd-\frac{a+c}{b+d}=\frac{bc-ad}{d(b+d)}>0.
$$

Hence $$a/b<(a+c)/(b+d)<c/d$$.

**(c)** Set $$x=a/b$$, which is nonzero. If $$x>0$$, then

$$
x+x^{-1}-2=\frac{(x-1)^2}{x}\ge0,
$$

so $$|x+x^{-1}|\ge2$$. If $$x<0$$, put $$y=-x>0$$; then $$|x+x^{-1}|=y+y^{-1}\ge2$$ by the same calculation. Since $$x+x^{-1}=a/b+b/a$$, the result follows.

### Exercise 11

If $$a\ge b$$, then $$|a-b|=a-b$$, and the displayed formulas give $$a$$ for the supremum and $$b$$ for the infimum. If $$b\ge a$$, then $$|a-b|=b-a$$, and they give $$b$$ and $$a$$, respectively. Thus in either case

$$
\sup\{a,b\}=\max\{a,b\}=\frac{a+b+|a-b|}{2},\qquad
\inf\{a,b\}=\min\{a,b\}=\frac{a+b-|a-b|}{2}.
$$

### Exercise 12

The claim is immediate for $$n=1$$. If $$a>b\ge0$$, then $$a>0$$. Powers of a nonnegative element are nonnegative, by the ordered-ring axioms. Inductively, $$a^n>b^n\ge0$$ implies

$$
a^{n+1}-b^{n+1}=(a^n-b^n)a+b^n(a-b)>0,
$$

because the first product is positive and the second is nonnegative. Hence $$a^n>b^n$$ for every $$n\in\mathbb N^\times$$. The case $$b>a$$ is symmetric. Thus $$a^n=b^n$$ forces $$a=b$$.

### Exercise 13

**Example 8.2(d).** Let $$S=\bigcap_{\alpha}S_\alpha$$, where each $$S_\alpha$$ is a subring of $$R$$. Every $$S_\alpha$$ contains $$0$$, and if $$x,y\in S$$ then every $$S_\alpha$$ contains $$x+y$$ and $$xy$$; it also contains $$-x$$. Hence $$S$$ is a subring. The empty intersection, by convention, is $$R$$.

**Example 8.2(e).** Let $$S$$ be the set of sequences in $$R^{\mathbb N}$$ that are zero except at finitely many indices. It contains the zero sequence. Sums and additive inverses have support contained in a finite union of finite supports, and the support of a product is contained in the intersection of the two supports. Thus $$S$$ is a subring.

It has no unity: if $$u\in S$$ were a multiplicative identity, multiplying by the sequence that is $$1_R$$ at index $$n$$ and zero elsewhere would force $$u(n)=1_R$$ for every $$n\in\mathbb N$$. Since $$R$$ is nontrivial, this constant-one sequence has infinite support and is not in $$S$$.

### Exercise 14

Write $$p=\sum_i p_iX^i$$ and $$q=\sum_j q_jX^j$$. All sums are finite, so we can differentiate term by term and regroup the terms with positive exponents:

$$
D(pq)=\sum_{\substack{i,j\\i+j\ge1}}p_iq_j(i+j)X^{i+j-1}
=\left(\sum_{i\ge1}ip_iX^{i-1}\right)q
+p\left(\sum_{j\ge1}jq_jX^{j-1}\right)
=qDp+pDq.
$$

Because $$K$$ is commutative, this is $$pDq+qDp$$, as required.

### Exercise 15

Divide the leading terms successively. The quotient terms are $$X^2$$, then $$-2X$$, then $$1$$:

$$
\begin{aligned}
X^5-3X^4+4X^3
&-(X^5-X^4+X^3-X^2)\\
&=-2X^4+3X^3+X^2,\\[4pt]
(-2X^4+3X^3+X^2)
&-(-2X^4+2X^3-2X^2+2X)\\
&=X^3+3X^2-2X,\\[4pt]
(X^3+3X^2-2X)
&-(X^3-X^2+X-1)\\
&=4X^2-3X+1.
\end{aligned}
$$

The terms subtracted are the divisor multiplied by $$X^2$$, $$-2X$$, and $$1$$, respectively. Therefore

$$
X^5-3X^4+4X^3
=(X^2-2X+1)(X^3-X^2+X-1)+(4X^2-3X+1).
$$

The remainder has degree at most $$2<3$$, so one can take

$$
s=X^2-2X+1,\qquad r=4X^2-3X+1.
$$

### Exercise 16

Take $$K=\mathbb F_2$$ and $$p=X^2-X\in\mathbb F_2[X]$$. This is a nonzero polynomial, but its only possible inputs are $$0$$ and $$1$$, and $$p(0)=p(1)=0$$. Therefore its polynomial function is the zero function, so the evaluation homomorphism is not injective in general.
