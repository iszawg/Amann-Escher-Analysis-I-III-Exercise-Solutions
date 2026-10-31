# Chapter IX — Elements of Measure Theory

## 3. Outer measures

These notes address Exercises 1–11. Inline formulas use GitBook's double-dollar syntax. We use $$\mathcal H_*^s$$ for the Hausdorff outer measure defined in the text, with no normalization factor, and $$\lambda_n^*$$ for Lebesgue outer measure. Exercise 7 is false as printed; a counterexample is given below.

### Exercise 1

**(a)** An intersection of two open intervals in $$\mathbb R^n$$ is the product of the coordinatewise intersections, hence is again an open interval (possibly empty).

**(b)** The cover index in the printed hypothesis should run from $$0$$ to $$k$$, as in the conclusion. Let $$I\subset\bigcup_{j=0}^k I_j$$. If $$I$$ has zero volume there is nothing to prove. Otherwise write its endpoints as $$a_i<b_i$$. In each coordinate cut $$[a_i,b_i]$$ at every endpoint of an $$I_j$$ that lies strictly between $$a_i$$ and $$b_i$$. The resulting grid divides $$[a,b]$$ into finitely many closed rectangles with disjoint interiors, and the sum of their volumes is $$\prod_i(b_i-a_i)=\operatorname{vol}_n(I)$$ by repeated distributivity.

For every grid rectangle choose a point in its interior. It lies in $$I$$ and therefore in some $$I_j$$. Since no boundary coordinate of $$I_j$$ lies inside a grid cell, the entire interior of that cell lies in $$I_j$$. Assign the cell to one such $$I_j$$. For each fixed $$j$$, the sum of the volumes of its assigned cells is at most $$\operatorname{vol}_n(I_j)$$: insert their endpoints into a grid on the closure of $$I_j$$ and sum its nonnegative cell volumes. Summing over $$j$$ proves the required inequality. This is a finite geometric argument and does not use Proposition 3.3.

### Exercise 2

**(a)** If $$x<y$$, then $$(-\infty,x)\subset(-\infty,y)$$, so $$F_\mu$$ is increasing. If $$x_j\uparrow x$$, the intervals $$(-\infty,x_j)$$ increase to $$(-\infty,x)$$. Continuity of the measure from below gives $$F_\mu(x_j)\to F_\mu(x)$$, proving left continuity. The assumed finiteness makes $$F_\mu$$ real-valued, so it is measure-generating.

As $$j\to\infty$$ the sets $$(-\infty,-j)$$ decrease to the empty set, and their first member has finite measure. Continuity from above gives $$F_\mu(-j)\to0$$. Monotonicity extends this limit to all $$x\to-\infty$$.

**(b)** Since $$0\in(-\infty,x)$$ exactly when $$x>0$$,

$$
F_{\delta_0}(x)=\begin{cases}0,&x\le0,\\1,&x>0.\end{cases}
$$

The value at zero reflects the left-open ray and makes this function left-continuous.

### Exercise 3

For $$x<y$$, additivity of the improper integral gives $$F_f(y)-F_f(x)=\int_x^y f(\xi)\,d\xi\ge0$$. Thus $$F_f$$ is increasing. Local integrability and the absolute continuity of the integral with respect to interval length show that $$\int_y^x f\to0$$ as $$y\uparrow x$$, so $$F_f$$ is left-continuous and real-valued. Proposition 3.5 then gives

$$
\mu_{F_f}^*([a,b))=F_f(b)-F_f(a)=\int_a^b f(\xi)\,d\xi.
$$

### Exercise 4

Write $$D_\varepsilon^s(A)$$ for the infimum in part (a), using arbitrary covering sets of diameter at most $$\varepsilon$$. Empty sets may be removed. For $$s=0$$, count each nonempty covering set as cost one; this is the convention needed to agree with the book's counting measure.

**(a), $$s>0$$.** Every open cover admissible for $$\mathcal H_\varepsilon^s$$ is also admissible for $$D_\varepsilon^s$$, so $$D_\varepsilon^s\le\mathcal H_\varepsilon^s$$. Conversely, let $$A_j$$ be an arbitrary admissible cover and fix $$\eta>0$$. For each nonempty $$A_j$$ choose an open neighbourhood $$O_j$$ with

$$
\operatorname{diam}(O_j)<\operatorname{diam}(A_j)+\eta 2^{-j-1}.
$$

This can be achieved by taking a sufficiently small metric neighbourhood. Consequently $$\operatorname{diam}(O_j)<\varepsilon+\eta$$. If the original sum is finite, the neighbourhood radii can moreover be chosen sufficiently small, separately for each $$j$$, that

$$
\sum_j\operatorname{diam}(O_j)^s\le\sum_j\operatorname{diam}(A_j)^s+\eta.
$$

Thus $$\mathcal H_{\varepsilon+\eta}^s(A)\le D_\varepsilon^s(A)+\eta$$ whenever the latter is finite; otherwise the inequality needed below is automatic. Taking first $$\eta\downarrow0$$ along a suitable sequence and then $$\varepsilon\downarrow0$$ shows that the two limiting infima agree. Equivalently, for any fixed $$\delta>0$$ choose $$\varepsilon<\delta/2$$ and $$\eta<\delta/2$$, then pass to the limits. This also handles infinite values.

For $$s=0$$, if $$A$$ has $$N$$ points, singleton covers cost at most $$N$$, and for sufficiently small $$\varepsilon$$ no covering set contains two of them. If $$A$$ is infinite, the same lower bound holds for every finite subset, however large. Hence the limit is the cardinality of $$A$$, with infinity for infinite sets, as required.

**(b)** Assume first $$s>0$$ and $$\lambda>0$$. For any admissible cover $$A\subset\bigcup_j A_j$$, the sets $$f(A_j\cap A)$$ cover $$f(A)$$ and have diameter at most $$\lambda\operatorname{diam}(A_j)$$. Part (a) gives

$$
D_{\lambda\varepsilon}^s(f(A))\le\lambda^sD_\varepsilon^s(A).
$$

Letting $$\varepsilon\downarrow0$$ proves the inequality. If $$\lambda=0$$, the image is empty or a singleton and has zero $$s$$-dimensional outer measure. For $$s=0$$ the assertion follows from $$|f(A)|\le|A|$$, taking $$\lambda^0=1$$ even when $$\lambda=0$$.

**(c)** Apply (b) to $$\phi$$ and to its inverse, both with Lipschitz constant one. The two inequalities give equality, including at $$s=0$$.

**(d)** Embed $$\mathbb R^n$$ isometrically as the first $$n$$ coordinates of $$\mathbb R^{\bar n}$$. Apply (b) to this embedding and to the coordinate projection restricted to the embedded image. Both have Lipschitz constant one, so the two outer measures agree. The counting-measure case is immediate as well.

### Exercise 5

**(a)** If $$0<s<t$$, a cover with diameters at most $$\varepsilon$$ satisfies

$$
\sum_j\operatorname{diam}(A_j)^t
\le\varepsilon^{t-s}\sum_j\operatorname{diam}(A_j)^s.
$$

By Exercise 4(a), $$D_\varepsilon^s(A)\le\mathcal H_*^s(A)$$. Hence if the latter is finite, letting $$\varepsilon\downarrow0$$ yields $$\mathcal H_*^t(A)=0$$. If $$s=0$$, finite counting measure means that $$A$$ is finite, and singleton covers show the same conclusion for every $$t>0$$.

**(b)** This is the contrapositive of (a): if $$\mathcal H_*^s(A)$$ were finite, then $$\mathcal H_*^t(A)$$ would be zero.

**(c)** Let $$d=\inf\{s>0:\mathcal H_*^s(A)=0\}$$, with the infimum of the empty set understood as $$\infty$$. Part (a) shows that the zero set is upward closed. If $$0\le s<d$$, then $$\mathcal H_*^s(A)=\infty$$: otherwise (a) would make every $$t>s$$ a zero exponent, including some $$t<d$$. If $$t>d$$, the definition of the infimum and (a) give $$\mathcal H_*^t(A)=0$$. Therefore

$$
\inf\{s>0:\mathcal H_*^s(A)=0\}
=\sup\{s\ge0:\mathcal H_*^s(A)=\infty\}.
$$

The supremum of the empty set is taken as zero in $$[0,\infty]$$. The argument also covers $$d=0$$ and $$d=\infty$$; no assertion is made about the value at the critical exponent.

### Exercise 6

**(a)** Clearly $$\dim_H A\ge0$$. For a bounded set contained in a cube of side $$L$$, partition that cube into $$N^n$$ cubes of side $$L/N$$. Their diameters are $$\sqrt n L/N$$, so for $$s>n$$ their total $$s$$-cost tends to zero. Thus every bounded set has zero $$s$$-dimensional outer measure for $$s>n$$. An arbitrary subset of $$\mathbb R^n$$ is the countable union of its intersections with bounded cubes, and countable subadditivity gives the same result. Hence $$\dim_H A\le n$$.

**(b)** A nonempty open set contains a nondegenerate box of positive Lebesgue outer measure. For every bounded set $$E\subset\mathbb R^n$$, a closed axis-parallel cube of side $$\operatorname{diam}(E)$$ contains it. Proposition 3.3 and subadditivity therefore imply

$$
\lambda_n^*(A)\le\mathcal H_*^n(A).
$$

In particular $$\mathcal H_*^n(A)>0$$. Exercise 5(b) gives $$\mathcal H_*^s(A)=\infty$$ for all $$s<n$$, and (a) supplies the opposite bound. Thus $$\dim_H A=n$$.

**(c)** Outer-measure monotonicity gives $$\mathcal H_*^s(A)\le\mathcal H_*^s(B)$$ for each $$s$$. Every zero exponent for $$B$$ is one for $$A$$, so $$\dim_H A\le\dim_H B$$.

**(d)** Set $$d=\sup_j\dim_H A_j$$. Part (c) gives $$\dim_H(\bigcup_j A_j)\ge d$$. If $$s>d$$, Exercise 5(c) gives $$\mathcal H_*^s(A_j)=0$$ for each $$j$$. Countable subadditivity makes the outer measure of the union zero, giving the reverse inequality.

**(e)** A singleton has dimension zero: its $$s$$-dimensional outer measure is zero for every $$s>0$$. Apply (d) to a countable union of singletons; the empty set also has dimension zero.

**(f)** By Exercise 4(b), whenever $$s>\dim_H A$$ the $$s$$-dimensional outer measure of $$f(A)$$ is zero. Hence $$\dim_H f(A)\le\dim_H A$$. A constant map is covered by (e).

**(g)** Exercise 4(d) shows equality of all outer measures under the standard isometric embedding, so their zero exponents and dimensions coincide.

### Exercise 7

**The equality is false in general.** Here is a counterexample with compact subsets of $$[0,1]$$. Partition the positive integers into consecutive blocks $$B_k$$ of lengths $$L_k=2^{2^k}$$. Let $$S$$ be the union of the odd-numbered blocks and $$T$$ the union of the even-numbered blocks. Define

$$
A=\left\{\sum_{j\in S}a_j2^{-j}:a_j\in\{0,1\}\right\},\qquad
B=\left\{\sum_{j\in T}b_j2^{-j}:b_j\in\{0,1\}\right\}.
$$

Each is compact as the continuous image of a product of compact two-point spaces. Let $$N_k=\sum_{i=1}^kL_i$$. At the end of an even block, the number $$p_k$$ of positions belonging to $$S$$ among the first $$N_k$$ digits is at most $$N_{k-1}$$; consequently $$p_k/N_k\to0$$ along even $$k$$. The first $$N_k$$ digits give at most $$2^{p_k}$$ possible prefixes, and all tails are at most $$2^{-N_k}$$. Hence $$A$$ is covered by at most $$2^{p_k}$$ intervals of diameter $$2^{-N_k}$$. For any $$s>0$$ the total $$s$$-cost is at most $$2^{p_k-sN_k}\to0$$. Thus $$\dim_H A=0$$. The same argument at the ends of odd blocks gives $$\dim_H B=0$$.

On the other hand, split the binary digits of any $$x\in[0,1]$$ between $$S$$ and $$T$$. This writes $$x=a+b$$ with $$a\in A$$ and $$b\in B$$, and conversely every such sum is in $$[0,1]$$. Hence $$A+B=[0,1]$$. The addition map $$(a,b)\mapsto a+b$$ is Lipschitz, so Exercises 6(b) and 6(f) imply

$$
1=\dim_H[0,1]=\dim_H(A+B)\le\dim_H(A\times B).
$$

Thus the printed right-hand side is zero while the left-hand side is at least one. Additional hypotheses are needed for equality.

### Exercise 8

Let $$L<\infty$$ be the length of the rectifiable path. For any $$\varepsilon>0$$, uniform continuity gives a finite partition of $$I$$ whose subintervals have images of diameter at most $$\varepsilon$$. The diameter of each subarc is at most its length, and the sum of its subarc lengths is $$L$$. These subarcs therefore cover $$\Gamma$$ at total diameter cost at most $$L$$. Exercise 4(a) gives $$\mathcal H_*^1(\Gamma)\le L$$, and Exercise 5(a) yields $$\dim_H\Gamma\le1$$.

For the lower bound, the perfect interval has distinct endpoints $$a,b$$ and injectivity gives $$\gamma(a)\ne\gamma(b)$$. Orthogonal projection onto the line through these two points is Lipschitz. The projected image is connected, because it is a continuous image of an interval, and contains both endpoint projections; it therefore contains a nondegenerate interval. Exercises 6(b), (c), and (f) yield $$1\le\dim_H\Gamma$$. Hence $$\dim_H\Gamma=1$$.

### Exercise 9

The projection of the empty set is empty, and projection preserves inclusion and arbitrary unions. Thus $$\mu^*(\varnothing)=0$$ and $$\mu^*$$ is increasing. For any sequence $$A_j\subset\mathbb R^2$$,

$$
\mu^*\left(\bigcup_j A_j\right)
=\lambda_1^*\left(\bigcup_j\operatorname{pr}_1(A_j)\right)
\le\sum_j\lambda_1^*(\operatorname{pr}_1(A_j))
=\sum_j\mu^*(A_j).
$$

So $$\mu^*$$ is an outer measure.

### Exercise 10

The sum of the values at the empty set is zero, and a sum of increasing nonnegative functions is increasing. For any sequence $$A_k\subset X$$, subadditivity of each $$\mu_j^*$$ and interchange of nonnegative double series give

$$
\mu^*\left(\bigcup_k A_k\right)
\le\sum_j\sum_k\mu_j^*(A_k)
=\sum_k\sum_j\mu_j^*(A_k)
=\sum_k\mu^*(A_k).
$$

All sums are in $$[0,\infty]$$, so the interchange remains valid when they diverge. This proves the outer-measure axioms.

### Exercise 11

If $$\lambda_n^*(A)=\infty$$, choose $$G=\mathbb R^n$$; monotonicity gives $$\lambda_n^*(G)=\infty$$. Otherwise, for each positive integer $$m$$ choose a countable open-box cover of $$A$$ whose total volume is less than $$\lambda_n^*(A)+1/m$$, and let $$U_m$$ be its union. Then $$U_m$$ is open, contains $$A$$, and by subadditivity and Proposition 3.3,

$$
\lambda_n^*(U_m)\le\lambda_n^*(A)+1/m.
$$

The set $$G=\bigcap_{m=1}^\infty U_m$$ is a $$G_\delta$$ containing $$A$$. Monotonicity gives $$\lambda_n^*(A)\le\lambda_n^*(G)\le\lambda_n^*(U_m)$$ for every $$m$$. Letting $$m\to\infty$$ proves equality.
