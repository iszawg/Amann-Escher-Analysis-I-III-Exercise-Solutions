# Chapter IX — Elements of Measure Theory

## 4. Measurable sets

These notes address Exercises 1–10. Inline formulas use GitBook's double-dollar syntax. We write $$\mathcal A(\mu^*)$$ for the Carathéodory measurable sets. The book uses left-continuous measure-generating functions and defines Hausdorff measure without a normalization factor: covering costs are powers of diameters.

### Exercise 1

Let $$A,B\subset X$$ have $$d(A,B)>0$$. The open set

$$
U=\{x\in X:d(x,A)<d(A,B)/2\}
$$

contains $$A$$ and is disjoint from $$B$$. It is Borel, hence $$\mu^*$$-measurable by hypothesis. Applying the Carathéodory equality to $$D=A\cup B$$ gives

$$
\mu^*(A\cup B)=\mu^*((A\cup B)\cap U)+\mu^*((A\cup B)\setminus U)
=\mu^*(A)+\mu^*(B).
$$

Thus $$\mu^*$$ is metric. If either set is empty, the same equality is immediate.

### Exercise 2

The induced outer measure is

$$
\mu^*(E)=\inf\{\nu(C):E\subset C,\ C\in\mathcal A\}.
$$

For $$E\in\mathcal A$$, choosing $$C=E$$ and using monotonicity of $$\nu$$ give $$\mu^*(E)=\nu(E)$$. To see that $$E$$ is $$\mu^*$$-measurable, take any $$D\subset X$$. For every measurable $$C\supset D$$,

$$
\mu^*(D\cap E)+\mu^*(D\setminus E)
\le\nu(C\cap E)+\nu(C\setminus E)=\nu(C).
$$

Taking the infimum over $$C$$ gives the nontrivial Carathéodory inequality; the reverse follows from subadditivity. Consequently $$\mathcal A\subset\mathcal A(\mu^*)$$ and $$\mu|_{\mathcal A}=\nu$$.

The measures need not have the same domain. For example, take Lebesgue measure restricted to the Borel sets of $$\mathbb R$$. The induced measure is complete, and contains every subset of the Cantor set, a Borel null set. Some of those subsets are not Borel: the Cantor set has continuum many points, while there are only continuum many Borel sets. Thus the extension can be strict. In general the two measures are equal precisely when their domains are equal.

### Exercise 3

**Lebesgue–Stieltjes outer measure.** Let $$d(A,B)>0$$ and choose $$\delta<d(A,B)$$. In any covering of $$A\cup B$$ by bounded intervals $$[a_j,b_j)$$, subdivide each interval into finitely many left-closed intervals of length less than $$\delta$$. Their costs add exactly to the original cost, because the differences of $$F$$ telescope. Each piece meets at most one of $$A,B$$. Assign the pieces meeting $$A$$ to one cover and those meeting $$B$$ to another; discard the rest. Their total costs do not exceed that of the original cover. Taking infima gives

$$
\mu_F^*(A)+\mu_F^*(B)\le\mu_F^*(A\cup B).
$$

The other inequality follows from subadditivity. This argument also covers an infinite right-hand side, since in that case the inequality is automatic.

**Hausdorff outer measure.** Let $$s>0$$. For $$0<\varepsilon<d(A,B)$$, every open set of diameter less than $$\varepsilon$$ meets at most one of $$A,B$$. Splitting any admissible cover therefore shows

$$
\mathcal H_\varepsilon^s(A)+\mathcal H_\varepsilon^s(B)
\le\mathcal H_\varepsilon^s(A\cup B).
$$

As $$\varepsilon\downarrow0$$ the left side tends to $$\mathcal H_*^s(A)+\mathcal H_*^s(B)$$, including infinite values. Subadditivity gives equality. In particular, by Theorem 4.3 all Borel subsets of $$\mathbb R^n$$ are $$\mathcal H^s$$-measurable; this includes the stated case $$s=n$$.

### Exercise 4

Denote the inner measure from the exercise by $$\mu_*$$. If $$A\in\mathcal A(\mu^*)$$ and $$D\subset X$$ satisfies $$\mu^*(D\setminus A)<\infty$$, then

$$
\mu^*(D)=\mu^*(D\cap A)+\mu^*(D\setminus A).
$$

Subtracting the finite second term, even when $$\mu^*(D)=\infty$$, shows that the expression in the supremum equals $$\mu^*(D\cap A)\le\mu^*(A)$$. Conversely, $$D=A$$ is admissible, since $$D\setminus A=\varnothing$$, and gives the value $$\mu^*(A)$$. Therefore $$\mu_*(A)=\mu^*(A)$$, including when this value is infinite.

### Exercise 5

Write $$I=[a,b]$$ and $$\Gamma=\gamma(I)$$. The image is compact and therefore Borel. We use the equivalent definition of Hausdorff outer measure with arbitrary covering sets, established in Exercise IX.3.4(a).

For any partition $$a=t_0<\cdots<t_m=b$$, put $$\Gamma_i=\gamma([t_{i-1},t_i])$$. Each $$\Gamma_i$$ is connected. If its endpoints have distinct images, orthogonal projection onto the direction of their chord maps $$\Gamma_i$$ onto a connected subset of $$\mathbb R$$ containing an interval of length $$|\gamma(t_i)-\gamma(t_{i-1})|$$. Projection is 1-Lipschitz, and the unnormalized one-dimensional Hausdorff measure of an interval is its length. Hence

$$
\mathcal H^1(\Gamma_i)\ge |\gamma(t_i)-\gamma(t_{i-1})|.
$$

The inequality is trivial for a zero-length chord. Injectivity ensures that different $$\Gamma_i$$ intersect only at common partition endpoints, and singletons have zero $$\mathcal H^1$$ measure. Finite additivity, with these null overlaps removed, yields

$$
\mathcal H^1(\Gamma)\ge\sum_{i=1}^m|\gamma(t_i)-\gamma(t_{i-1})|.
$$

Taking the supremum over partitions proves $$\mathcal H^1(\Gamma)\ge L(\gamma)$$.

For the reverse inequality, uniform continuity gives partitions with $$\max_i\operatorname{diam}(\Gamma_i)$$ arbitrarily small. For each subinterval its image diameter is at most the variation of $$\gamma$$ on that subinterval. The sum of these variations is $$L(\gamma)$$: combine near-maximizing partitions of the finitely many subintervals and use the definition of total variation. Thus these image sets form arbitrarily fine covers of total diameter at most $$L(\gamma)$$, and $$\mathcal H^1(\Gamma)\le L(\gamma)$$. Together the inequalities give $$\mathcal H^1(\Gamma)=L(\gamma)$$.

For completeness, the interval fact used above follows because every interval cover has total diameter at least its Lebesgue outer measure, while subdivision into short intervals gives the opposite bound.

### Exercise 6

At stage $$k$$ there are $$4^k$$ closed squares of side $$4^{-k}$$. They cover $$A$$ and have diameter $$\sqrt2\,4^{-k}$$. Their diameters tend to zero and their total diameter is $$\sqrt2$$, so

$$
\mathcal H^1(A)\le\sqrt2.
$$

Each retained square has one retained subsquare in every column. For every $$x\in[0,1]$$, choose at each stage a retained square whose horizontal projection contains $$x$$, nested inside the previous choice. Compactness gives a point of $$A$$ projecting to $$x$$. Hence $$\operatorname{pr}_1(A)=[0,1]$$. Since projection is 1-Lipschitz,

$$
1=\mathcal H^1([0,1])\le\mathcal H^1(A)\le\sqrt2.
$$

The dimension criterion from Exercise IX.3.5 now gives $$\dim_H A=1$$: positive finite measure at exponent 1 forces infinite measure at every smaller exponent and zero measure at every larger exponent.

### Exercise 7

Let $$C_k$$ be the union of the $$2^k$$ closed intervals of length $$3^{-k}$$ in the standard middle-thirds construction, and set $$s=\log 2/\log 3$$. Covering $$C$$ by these intervals gives

$$
\mathcal H^s(C)\le\liminf_{k\to\infty}2^k(3^{-k})^s=1.
$$

For the lower bound, consider a finite open interval cover $$I_1,\ldots,I_N$$ of $$C$$. Any bounded nonempty open subset of $$\mathbb R$$ lies in an open interval of the same diameter. Thus we may replace each covering set by such an interval and, by compactness of $$C$$, pass to a finite subcover without increasing the cost. An unbounded covering set already has infinite cost. If some interval has diameter at least 1, the sum of its $$s$$-costs is already at least 1. Otherwise, for each $$i$$ choose $$k_i\ge0$$ such that

$$
3^{-(k_i+1)}\le\operatorname{diam}(I_i)<3^{-k_i}.
$$

Distinct component intervals of $$C_{k_i}$$ have gaps at least $$3^{-k_i}$$, so $$I_i$$ meets at most one of them. Choose $$j\ge\max_i k_i$$. Each component of $$C_j$$ contains a point of $$C$$, and each $$I_i$$ meets at most $$2^{j-k_i}$$ such components. Counting gives

$$
2^j\le\sum_{i=1}^N2^{j-k_i},\qquad
1\le\sum_{i=1}^N2^{-k_i}
\le 2\sum_{i=1}^N\operatorname{diam}(I_i)^s,
$$

where $$3^s=2$$. Thus every admissible cover has cost at least $$1/2$$ and

$$
\frac12\le\mathcal H^s(C)\le1,\qquad \dim_H C=s.
$$

Finally, the stage-$$k$$ cover has total length $$(2/3)^k\to0$$. Hence $$\lambda_1^*(C)=0$$; since $$C$$ is closed, $$\lambda_1(C)=0$$.

### Exercise 8

By continuity from above, applied to the decreasing intervals $$[a,a+1/n)$$ of finite measure,

$$
\mu_F(\{a\})=\lim_{n\to\infty}\bigl(F(a+1/n)-F(a)\bigr)
=F(a+)-F(a).
$$

Here $$F(a+)$$ is the right limit. Because the book takes $$F$$ to be left-continuous, the mass is the jump to the **right** of $$a$$.

### Exercise 9

**(i)** Define $$F(t)=\mu([0,t))$$ for $$t\ge0$$ and $$F(t)=-\mu([t,0))$$ for $$t<0$$. Local finiteness and compactness imply finite measure on every bounded interval, so $$F$$ is real-valued. Additivity gives, for all $$a<b$$,

$$
F(b)-F(a)=\mu([a,b))\ge0.
$$

Thus $$F$$ is increasing. If $$t_j\uparrow t$$, then $$[t_j,t)\downarrow\varnothing$$ and these sets lie in a bounded interval of finite measure. Continuity from above gives $$F(t)-F(t_j)=\mu([t_j,t))\to0$$, so $$F$$ is left-continuous.

Proposition 3.5 gives $$\mu_F([a,b))=F(b)-F(a)=\mu([a,b))$$. These half-open intervals form a generating pi-system for $$\mathcal B^1$$, and the intervals $$[-n,n)$$ exhaust $$\mathbb R$$ with finite measure for both measures. The uniqueness theorem for sigma-finite measures therefore yields $$\mu=\mu_F|_{\mathcal B^1}$$.

If another generating function $$G$$ induces the same Borel measure, then $$G(b)-G(a)=F(b)-F(a)$$ for every $$a<b$$; consequently $$G-F$$ is constant. Conversely, adding a constant leaves every interval cost, and therefore the induced measure, unchanged.

**(ii)** Part (i) proves surjectivity after normalizing $$F(0)=0$$; the uniqueness up to a constant proves injectivity. Conversely every generating function induces a locally finite Borel measure, because each bounded half-open interval has finite measure and every point has an open neighborhood inside one. Hence the stated map is a bijection.

### Exercise 10

Let $$S=\{a_k:k\in\mathbb Z\}$$. For any $$x<y$$ inside one of the gaps $$(a_k,a_{k+1})$$, the interval $$[x,y)$$ has measure $$F(y)-F(x)=0$$. Each gap is a countable union of such intervals, so $$\mathbb R\setminus S$$ is a countable union of measurable null sets and is itself null. The completeness of $$\mu_F$$ implies that every subset of $$\mathbb R\setminus S$$ is measurable.

By Exercise 8 and left continuity, $$\mu_F(\{a_k\})=F(a_k+)-F(a_k)=p_k$$. Every subset of the countable Borel set $$S$$ is Borel. Therefore, for any $$A\subset\mathbb R$$, both $$A\cap S$$ and $$A\setminus S$$ are measurable, and countable additivity gives

$$
\mathcal A(\mu_F)=\mathcal P(\mathbb R),\qquad
\mu_F(A)=\sum_{\{k\in\mathbb Z:a_k\in A\}}p_k.
$$

The sum is allowed to be infinite; the zero term from $$A\setminus S$$ does not affect it.
