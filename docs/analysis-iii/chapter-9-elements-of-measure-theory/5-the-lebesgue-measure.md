# Chapter IX — Elements of Measure Theory

## 5. The Lebesgue measure

These notes address Exercises 1–21. We use $$\mathcal L(n)$$ for the Lebesgue sigma-algebra on $$\mathbb R^n$$, $$\mathcal B^n$$ for its Borel sigma-algebra, and $$\lambda_n$$ for Lebesgue measure. Inline formulas use GitBook's double-dollar syntax. As usual, a product of nonnegative extended numbers is zero if either factor is zero.

### Exercise 1

First suppose that $$U\subset\mathbb R^m$$ and $$V\subset\mathbb R^n$$ are open. Each is a countable disjoint union of half-open dyadic cubes: use maximal dyadic cubes contained in the open set. Products of these cubes are disjoint half-open rectangles. Since Lebesgue measure agrees with volume on rectangles, countable additivity gives

$$
\lambda_{m+n}(U\times V)=\lambda_m(U)\lambda_n(V).
$$

This remains valid for infinite values by monotone limits of finite sums.

If $$N\subset\mathbb R^m$$ is null, then $$N\times\mathbb R^n$$ is null. Indeed, cover $$N$$ by open sets of arbitrarily small measure, multiply by each bounded open cube $$(-k,k)^n$$, use the open-set formula, and take the countable union over $$k$$. The analogous statement holds with the factors interchanged. In particular every subset of either product is Lebesgue measurable by completeness.

For arbitrary $$A\in\mathcal L(m)$$ and $$B\in\mathcal L(n)$$, choose Borel sets $$A_0\subset A$$ and $$B_0\subset B$$ with $$A\setminus A_0$$ and $$B\setminus B_0$$ null. Then $$A\times B$$ differs from the Borel set $$A_0\times B_0$$ by a subset of a null set, and is measurable. The product formula holds for Borel sets by the usual uniqueness theorem for sigma-finite measures: for fixed Borel $$A_0$$ of finite measure, compare the two measures in the second variable on half-open rectangles, then exhaust $$A_0$$ by bounded pieces and use monotone convergence. Equivalently, first apply this argument to bounded Borel sets in each variable. Null differences do not change either side, including the case of an infinite factor. Thus

$$
\lambda_{m+n}(A\times B)=\lambda_m(A)\lambda_n(B).
$$

All generating rectangles are therefore in $$\mathcal L(m+n)$$, so $$\mathcal L(m)\otimes\mathcal L(n)\subset\mathcal L(m+n)$$.

### Exercise 2

The first inclusion follows from $$\mathcal B^m\subset\mathcal L(m)$$ and $$\mathcal B^n\subset\mathcal L(n)$$; the second is Exercise 1. Both are strict, for positive dimensions.

Choose a Lebesgue measurable non-Borel subset $$N\subset\mathbb R^m$$, contained in a Borel null set. Then $$N\times\mathbb R^n$$ belongs to $$\mathcal L(m)\otimes\mathcal L(n)$$. It is not in $$\mathcal B^m\otimes\mathcal B^n$$: every section of a set in this product sigma-algebra is Borel, while a fixed second-coordinate section is $$N$$.

Choose a non-Lebesgue-measurable $$V\subset\mathbb R^n$$. The set $$\{0\}\times V$$ lies in the null set $$\{0\}\times\mathbb R^n$$ and is therefore in $$\mathcal L(m+n)$$. It cannot belong to $$\mathcal L(m)\otimes\mathcal L(n)$$, since its section at 0 is $$V$$ and every such section of a product-measurable set is Lebesgue measurable. The section assertions follow by checking rectangles and then using closure under complements and countable unions.

### Exercise 3

A $$C^1$$ manifold admits local parametrizations $$\phi:U\subset\mathbb R^m\to\mathbb R^n$$. Cover each parameter domain by countably many closed cubes whose slightly larger neighborhoods lie in $$U$$. On each such cube, the bounded derivative makes $$\phi$$ Lipschitz.

For a cube of side $$L$$ and a Lipschitz constant $$K$$, divide it into $$j^m$$ small cubes. Each image has diameter at most $$K\sqrt m\,L/j$$ and lies in an $$n$$-cube of comparable side length. Their total $$n$$-volume is at most $$Cj^{m-n}$$, which tends to zero because $$m<n$$. Thus each parametrized cube has outer measure zero. For $$m=0$$, each local image is a singleton and the same conclusion holds.

The manifold is a subspace of second-countable $$\mathbb R^n$$ and hence Lindelöf, so countably many chart neighborhoods cover it. Their countably many parametrized cubes are null, proving $$\lambda_n(M)=0$$.

### Exercise 4

Every compact subset of $$\mathbb R^n$$ is closed. Inner regularity therefore gives

$$
\lambda_n(A)=\sup_{K\subset A,\ K\text{ compact}}\lambda_n(K)
\le \sup_{F\subset A,\ F\text{ closed}}\lambda_n(F)
\le\lambda_n(A).
$$

This also covers infinite measure.

### Exercise 5

Additivity implies $$g(q)=qg(1)$$ for every positive rational $$q$$. If $$g$$ is increasing, sandwich any positive $$x$$ between rational sequences tending to $$x$$ to obtain $$g(x)=xg(1)$$.

Alternatively, suppose $$g$$ is bounded on bounded sets. Choose $$M$$ with $$|g(t)|\le M$$ for $$0<t\le1$$. Given $$\varepsilon>0$$, choose an integer $$N>M/\varepsilon$$. If $$0<h\le1/N$$, then

$$
N|g(h)|=|g(Nh)|\le M,
$$

so $$g(h)\to0$$ as $$h\downarrow0$$. Additivity now gives continuity at every positive point from both sides. Approximation by positive rationals yields the same formula. No sign assumption on $$g$$ is needed in this case.

### Exercise 6

For an additive function $$g:\mathbb R\to\mathbb R$$, rational homogeneity holds. If $$g\in S$$, choose $$s_0$$ with $$g(s_0)\ne s_0g(1)$$. The vectors $$(1,g(1))$$ and $$(s_0,g(s_0))$$ are linearly independent over $$\mathbb R$$. Their rational linear combinations are dense in $$\mathbb R^2$$, because $$\mathbb Q^2$$ is dense and the linear map with these two columns is invertible. Each such combination lies on the graph of $$g$$. This proves (a).

For (b), extend the independent set $$\{1,\sqrt2\}$$ to a Hamel basis of $$\mathbb R$$ over $$\mathbb Q$$. Define a rational-linear map by assigning 0 to 1, 1 to $$\sqrt2$$, and 0 to every other basis vector. Then $$g(\sqrt2)=1\ne\sqrt2\,g(1)$$, so $$g\in S$$. The basis construction uses choice.

### Exercise 7

Let $$J=[a',b')\subset\mathbb R^{n-1}$$, interpreted coordinatewise; it may be empty. Exercise 1 gives measurability of $$A\times J$$ in the Lebesgue case, and the Borel case follows from the product topology. The map $$A\mapsto\mu(A\times J)$$ is a measure, since products with $$J$$ preserve disjoint unions. For $$t\in\mathbb R$$,

$$
\mu_1(A+t)=\mu\bigl((A\times J)+(t,0,\ldots,0)\bigr)=\mu_1(A).
$$

For local finiteness, a bounded open interval $$I$$ has $$I\times J$$ contained in a compact rectangle. That rectangle has finite $$\mu$$-measure: finitely many finite-measure neighborhoods cover it. Hence $$\mu_1(I)<\infty$$. If $$J$$ is empty, $$\mu_1$$ is simply the zero measure.

### Exercise 8

The basis cannot be finite, or even countable. The rational span of a countable set is countable: it is a countable union of finite-tuples of rational coefficients and basis elements. But $$\mathbb R$$ is uncountable. Hence every Hamel basis of $$\mathbb R$$ over $$\mathbb Q$$ is uncountable.

### Exercise 9

For distinct primes $$p_1,\ldots,p_k$$, suppose $$\sum_i q_i\log p_i=0$$ with rational coefficients. Clearing denominators gives integers $$z_i$$ with $$\prod_i p_i^{z_i}=1$$. Unique factorization forces all $$z_i=0$$, hence all $$q_i=0$$. This proves (a).

The set of primes is countable, so the rational span of $$M$$ is countable, whereas $$\mathbb R$$ is uncountable. Thus $$M$$ does not span $$\mathbb R$$ and is not a basis.

### Exercise 10

Suppose the measurable basis $$B$$ has positive measure. Steinhaus's theorem says that $$B-B$$ contains an open interval around zero, and therefore its rational linear span is all of $$\mathbb R$$.

On the other hand, every finite rational combination of elements of $$B-B$$ has, in its unique basis expansion, coefficients whose sum is zero. A fixed basis vector has coefficient sum 1, so it cannot lie in that span. This contradiction proves $$\lambda_1(B)=0$$. The argument also covers the case of infinite measure.

### Exercise 11

Every $$x\in[0,2]$$ has $$x/2\in[0,1]$$. Choose a ternary expansion

$$
\frac{x}{2}=\sum_{j=1}^{\infty}a_j3^{-j},\qquad a_j\in\{0,1,2\}.
$$

For each digit choose $$u_j,v_j\in\{0,1\}$$ with $$u_j+v_j=a_j$$. Then

$$
x=\sum_{j=1}^{\infty}2u_j3^{-j}+\sum_{j=1}^{\infty}2v_j3^{-j}\in C+C.
$$

The reverse inclusion is immediate from $$C\subset[0,1]$$. Endpoints are included using the expansion $$1=0.222\ldots_3$$ when necessary.

### Exercise 12

Take $$A=C$$, the Cantor set. It has measure zero, and $$1-C=C$$ by reflection symmetry. Exercise 11 therefore yields

$$
C-C=C+C-1=[-1,1],
$$

which is a neighborhood of zero. This shows why the positive-measure hypothesis in Steinhaus's theorem is sufficient but not necessary.

### Exercise 13

Order the rationally independent subsets of $$C$$ by inclusion. The union of a chain is independent, since any finite linear dependence would already occur in one member of the chain. Zorn's lemma gives a maximal independent $$B\subset C$$. If some $$c\in C$$ were outside $$\operatorname{span}_{\mathbb Q}B$$, adjoining it would preserve independence, contrary to maximality. Thus $$C\subset\operatorname{span}_{\mathbb Q}B$$.

By Exercise 11, $$[0,2]=C+C$$ lies in this span. Every real number is a rational multiple of a number in $$[0,2]$$ (with a sign change if needed), so the span is all of $$\mathbb R$$. Hence $$B$$ is a basis. Since $$B\subset C$$ and $$C$$ is null, completeness of Lebesgue measure makes $$B$$ measurable and null.

### Exercise 14

Let $$R$$ contain exactly one representative of each coset of $$\mathbb R^n/\mathbb Q^n$$. Then $$(R-R)\cap\mathbb Q^n=\{0\}$$. If $$R$$ were measurable and had positive measure, Steinhaus's theorem would make $$R-R$$ a neighborhood of zero, containing a nonzero rational vector, a contradiction. Thus $$R$$ would be null. But

$$
\mathbb R^n=\bigcup_{q\in\mathbb Q^n}(R+q),
$$

and translation invariance would make the right side a countable union of null sets. This contradiction proves $$R\notin\mathcal L(n)$$.

### Exercise 15

Both $$G=\mathbb Q+\sqrt2\,\mathbb Z$$ and $$G_1=\mathbb Q+2\sqrt2\,\mathbb Z$$ contain zero and are closed under subtraction, so they are subgroups. Moreover $$G_1$$ has index 2 in $$G$$: the integer coefficient of $$\sqrt2$$ is uniquely determined, and its parity distinguishes $$G_1$$ from $$G_2=\sqrt2+G_1$$.

Let $$x=r+h$$ and $$y=s+k$$ belong to $$A=R+G_1$$, with $$r,s\in R$$ and $$h,k\in G_1$$. If $$x-y\in G$$, then $$r-s=(x-y)-(h-k)\in G$$. Since $$R$$ has exactly one representative per $$G$$-coset, $$r=s$$, and hence $$x-y=h-k\in G_1$$. Therefore $$(A-A)\cap G_2=\varnothing$$.

### Exercise 16

Use the set $$A$$ from Exercise 15. The coset $$G_2=\sqrt2+G_1$$ is dense: it contains the dense set $$\sqrt2+\mathbb Q$$. If a measurable $$E\subset A$$ had positive measure, Steinhaus's theorem would make $$E-E$$ a neighborhood of zero, which must meet $$G_2$$. This contradicts Exercise 15.

Each real number has a unique representation $$r+g$$ with $$r\in R$$ and $$g\in G$$. Since $$G$$ is the disjoint union of $$G_1$$ and $$\sqrt2+G_1$$,

$$
A^c=R+G_2=A+\sqrt2.
$$

If a measurable $$E\subset A^c$$ had positive measure, then $$E-\sqrt2\subset A$$ would be measurable and have the same positive measure, already ruled out. Thus every measurable subset of either $$A$$ or $$A^c$$ is null.

### Exercise 17

The complement of the Cantor set $$C$$ in $$[0,1]$$ is a union of disjoint open intervals, and the Cantor function $$f$$ is constant on each of them. Taking $$N=C$$, we obtain $$f'(x)=0$$ at every point of $$[0,1]\setminus N$$; $$N$$ is null. This proves (a).

The function $$g(x)=x+f(x)$$ is continuous and strictly increasing, because $$f$$ is nondecreasing. It maps the endpoints to 0 and 2. It is therefore a continuous bijection from a compact space to a Hausdorff space, and hence a homeomorphism onto $$[0,2]$$.

On each component interval $$(a,b)$$ of $$[0,1]\setminus C$$, the continuous function $$f$$ is constant even at the endpoints. Consequently $$g((a,b))=(g(a),g(b))$$ has length $$b-a$$. These images are precisely the components of $$[0,2]\setminus g(C)$$, and their total length is $$\lambda_1([0,1]\setminus C)=1$$. Since $$g(C)$$ is compact,

$$
\lambda_1(g(C))=2-1=1.
$$

### Exercise 18

**(a)** In a finite-dimensional normed space, closed bounded sets are compact. Thus each point has a closed ball as a compact neighborhood.

**(b)** A closed subspace $$F$$ of a locally compact Hausdorff space is Hausdorff; intersect a compact neighborhood of $$x\in F$$ with $$F$$ to obtain a compact neighborhood in $$F$$. For an open subspace $$U$$ and $$x\in U$$, local compactness and the regularity of locally compact Hausdorff spaces supply an open neighborhood $$V$$ of $$x$$ whose compact closure is contained in $$U$$. This closure is a compact neighborhood in $$U$$.

**(c) The statement needs a metric or comparable countability hypothesis.** As printed for general locally compact spaces, it is false in both directions. The compact ordinal space $$[0,\omega_1]$$ is sigma-compact but not separable: a countable subset of countable ordinals is bounded below $$\omega_1$$, so it misses a nonempty open interval.

Conversely, let $$D$$ be the countable set of finite binary strings and let $$E=\{0,1\}^{\mathbb N}$$. Make each point of $$D$$ isolated; a basic neighborhood of $$x\in E$$ consists of $$x$$ and all sufficiently long finite prefixes of $$x$$. This defines a Hausdorff locally compact space: each such neighborhood together with its limit point is a compact convergent sequence, and distinct infinite sequences eventually have disjoint prefix tails. The countable set $$D$$ is dense, but $$E$$ is an uncountable closed discrete subspace. Every compact subset meets $$E$$ in a finite set, so the space is not sigma-compact.

For a **locally compact metric space**, the intended equivalence holds. If it is sigma-compact, each compact metric piece is separable and the union of their countable dense subsets is dense. Conversely, a separable metric space is second-countable and hence Lindelöf; select a countable cover by open sets with compact closures. Their closures cover the space, proving sigma-compactness.

**(d)** A closed subspace of a sigma-compact space is sigma-compact: intersect each compact piece with it. For an open subset $$U$$ of a sigma-compact metric space $$X=\bigcup_jK_j$$, set

$$
K_{j,k}=\{x\in K_j:d(x,X\setminus U)\ge 1/k\}.
$$

When $$X\setminus U$$ is nonempty, these sets are compact and their union is $$U$$. If the complement is empty, $$U=X$$. Part (b) also gives local compactness of both subspaces.

### Exercise 19

Let $$\mu_F$$ be the complete Lebesgue–Stieltjes measure induced by the increasing left-continuous function $$F$$. Its outer measure is defined by countable covers with bounded intervals $$[a,b)$$ of cost $$F(b)-F(a)$$.

For measurable $$A$$ with finite measure, choose such a cover with total cost less than $$\mu_F(A)+\varepsilon/2$$. By left continuity, enlarge each interval to an open interval $$(a_j-\delta_j,b_j)$$ with

$$
F(a_j)-F(a_j-\delta_j)<\varepsilon 2^{-j-1}.
$$

This open interval is contained in $$[a_j-\delta_j,b_j)$$, whose measure is $$F(b_j)-F(a_j-\delta_j)$$. The union is an open superset of $$A$$ of measure less than $$\mu_F(A)+\varepsilon$$. For infinite-measure $$A$$ the outer-regularity equality is immediate.

For inner regularity, first let $$A\subset[-k,k]$$ and put $$H=[-k-1,k+1]$$. This compact interval has finite measure, since it lies in a bounded half-open interval whose measure is a finite difference of $$F$$. Apply outer regularity to $$H\setminus A$$ and choose an open $$O\supset H\setminus A$$ with $$\mu_F(O)<\mu_F(H\setminus A)+\varepsilon$$. Then $$K=H\setminus O$$ is compact, lies in $$A$$, and

$$
\mu_F(K)\ge\mu_F(H)-\mu_F(O)>\mu_F(A)-\varepsilon.
$$

For arbitrary $$A$$, apply this to $$A\cap[-k,k]$$ and let $$k\to\infty$$, using continuity from below. This proves both defining equalities of regularity, including infinite measure.

### Exercise 20

For every continuous $$f:X\to\mathbb R$$, the zero set $$f^{-1}(0)$$ is closed and therefore Borel. Thus the sigma-algebra generated by these zero sets is contained in $$\mathcal B(X)$$.

Conversely, every closed $$F\subset X$$ is the zero set of the continuous function $$x\mapsto d(x,F)$$ when $$F\ne\varnothing$$; the empty set is the zero set of the constant function 1. Since closed sets generate the Borel sigma-algebra, the reverse inclusion follows.

### Exercise 21

Write $$\mathcal C=\{A\cap D:D\in\mathcal A\}$$ and let $$E\in\mathcal C$$. Since $$A\in\mathcal A$$, also $$E\in\mathcal A$$ and $$\nu(E)=\mu(E)$$. Every compact $$K\subset E$$ in the subspace $$A$$ is compact in $$X$$, and conversely every compact subset of $$X$$ contained in $$E$$ is compact in $$A$$. Inner regularity of $$\mu$$ therefore immediately gives inner regularity of $$\nu$$.

For outer regularity, every relatively open $$V\subset A$$ is measurable and contains $$E$$ only if $$\nu(V)\ge\nu(E)$$. Conversely, if $$\mu(E)<\infty$$, choose an open $$O\subset X$$ with $$E\subset O$$ and $$\mu(O)<\mu(E)+\varepsilon$$. Then $$A\cap O$$ is relatively open, contains $$E$$, and

$$
\nu(A\cap O)=\mu(A\cap O)\le\mu(O)<\nu(E)+\varepsilon.
$$

If $$\mu(E)=\infty$$, monotonicity already gives the equality of the infimum with infinity. Thus the restricted measure space is regular. Its sigma-algebra contains the Borel sets of the subspace because these are traces of Borel sets of $$X$$.
