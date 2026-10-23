# Chapter III — Continuous Functions

## 3. Compactness

### Exercise 1

Assume first that each $$X_j$$ is nonempty and compact. It suffices to prove the result for two factors and then use induction. Let $$\mathcal U$$ be an open cover of $$X_1\times X_2$$. For each $$x\in X_1$$, the fiber $$\{x\}\times X_2$$ is compact, so finitely many members of $$\mathcal U$$ cover it. By the product topology, each point of the fiber has a basic open rectangle around it contained in one of those cover members. Compactness of $$X_2$$ lets us choose finitely many such rectangles $$V_{x,i}\times W_{x,i}$$ whose $$W_{x,i}$$ cover $$X_2$$. The finite intersection $$V_x=\bigcap_i V_{x,i}$$ is a neighborhood of $$x$$ and $$V_x\times X_2$$ is covered by the corresponding finitely many members of $$\mathcal U$$. The neighborhoods $$V_x$$ cover $$X_1$$; compactness of $$X_1$$ gives finitely many of them covering $$X_1$$. Collecting their finite families from $$\mathcal U$$ gives a finite subcover of $$X_1\times X_2$$.

Conversely, suppose $$X_1\times\cdots\times X_n$$ is compact and nonempty. Each projection $$\pi_j:X_1\times\cdots\times X_n\to X_j$$ is continuous and surjective. Therefore $$X_j=\pi_j(X_1\times\cdots\times X_n)$$ is compact.

If empty metric spaces are allowed, the statement as printed needs the nonemptiness qualification: for example, $$\varnothing\times\mathbb R=\varnothing$$ is compact although $$\mathbb R$$ is not. With all factors nonempty, the two implications above prove the claim.

### Exercise 2

Suppose first that $$Y$$ is closed in the compact metric space $$X$$. Let $$\{V_\alpha\}$$ be an open cover of $$Y$$ in its relative topology. For each $$\alpha$$ choose an open set $$U_\alpha\subseteq X$$ with $$V_\alpha=U_\alpha\cap Y$$. The sets $$\{U_\alpha\}\cup\{X\setminus Y\}$$ form an open cover of $$X$$. Compactness gives a finite subcover; after discarding $$X\setminus Y$$ if it was selected, the remaining finitely many $$U_\alpha$$ still cover $$Y$$. Their corresponding $$V_\alpha$$ give a finite subcover of $$Y$$, so $$Y$$ is compact.

Conversely, suppose $$Y$$ is compact and fix $$x\in X\setminus Y$$. For each $$y\in Y$$, the balls $$B(y,d(x,y)/3)$$ and $$B(x,d(x,y)/3)$$ are disjoint. The first family covers $$Y$$, so finitely many balls $$B(y_j,d(x,y_j)/3)$$ cover $$Y$$. Let $$r=\min_j d(x,y_j)/3>0$$. Then $$B(x,r)$$ is disjoint from every selected ball and hence from $$Y$$. Thus every point of $$X\setminus Y$$ has an open neighborhood disjoint from $$Y$$, proving that $$Y$$ is closed. Therefore $$Y$$ is compact if and only if it is closed in $$X$$.

### Exercise 3

**(a)** A homeomorphism maps open sets to open sets: if $$O\subseteq X$$ is open, then $$f(O)=(f^{-1})^{-1}(O)$$ is open in $$Y$$. If $$U$$ is a neighborhood of $$x$$, it contains an open set $$O$$ with $$x\in O\subseteq U$$. Hence $$f(U)$$ contains the open neighborhood $$f(O)$$ of $$f(x)$$. So $$f(U)$$ is a neighborhood of $$f(x)$$. Applying the same argument to $$f^{-1}$$ proves that every neighborhood of $$f(x)$$ is $$f(U)$$ for some neighborhood $$U$$ of $$x$$. Therefore

$$
\mathcal U_Y(f(x))=\{f(U):U\in\mathcal U_X(x)\}.
$$

**(b)(i)** Let $$F$$ be closed in $$X$$. Since $$X$$ is compact, $$F$$ is compact. Its continuous image $$f(F)$$ is compact in the metric space $$Y$$, hence closed. Thus $$f$$ is a closed map.

**(ii)** If $$f$$ is also bijective, then for every closed $$F\subseteq X$$,

$$
((f^{-1})^{-1})(F)=f(F)
$$

is closed in $$Y$$. The closed-set criterion for continuity shows that $$f^{-1}:Y\to X$$ is continuous. Thus $$f$$ is a homeomorphism.

### Exercise 4

Suppose first that $$X$$ is compact and let $$\mathcal F$$ be a family of closed subsets of $$X$$ with the finite intersection property. If $$\bigcap_{F\in\mathcal F}F=\varnothing$$, then the open complements $$X\setminus F$$ cover $$X$$. Compactness gives a finite subcover, so the corresponding finite intersection of members of $$\mathcal F$$ is empty, a contradiction.

Conversely, suppose every family of closed subsets with the finite intersection property has nonempty intersection. Given an open cover $$\{U_\alpha\}_{\alpha\in A}$$ of $$X$$ with no finite subcover, the closed sets $$F_\alpha=X\setminus U_\alpha$$ have the finite intersection property: every finite intersection is nonempty because the corresponding finite collection of open sets does not cover $$X$$. The assumed property gives $$\bigcap_{\alpha\in A}F_\alpha\ne\varnothing$$, contradicting that $$\{U_\alpha\}$$ covers $$X$$. Hence every open cover has a finite subcover, and $$X$$ is compact.

### Exercise 5

For any finite collection of the closed sets $$A_j$$, their intersection is the last set in that collection, because $$A_j\supseteq A_{j+1}$$. It is nonempty by hypothesis. Thus $$\{A_j:j\in\mathbb N\}$$ has the finite intersection property. Since $$A_0$$ is compact and each $$A_j$$ is closed in $$A_0$$, Exercise 4 gives

$$
\bigcap_{j=0}^{\infty}A_j\ne\varnothing.
$$

### Exercise 6

Choose bases of the finite-dimensional spaces $$E$$ and $$F$$, and let $$|[x]|$$ and $$|[y]|$$ denote the Euclidean norms of their coordinate vectors. Equivalence of norms in finite dimensions provides constants $$c_E,C_F>0$$ such that

$$
|[x]|\le c_E^{-1}\|x\|_E,\qquad \|y\|_F\le C_F|[y]|.
$$

Let $$M$$ be the matrix of $$A$$ in these bases. Then, for every $$x\in E$$,

$$
\|Ax\|_F\le C_F|M[x]|\le C_F\|M\|_2|[x]|
\le \frac{C_F\|M\|_2}{c_E}\|x\|_E.
$$

Thus $$A$$ is Lipschitz continuous.

### Exercise 7

Identify $$\mathbb R^{n\times n}$$ with $$\mathbb R^{n^2}$$. The set of orthogonal matrices is

$$
O(n)=\{A\in\mathbb R^{n\times n}:A^{\mathsf T}A=I\}.
$$

The map $$A\mapsto A^{\mathsf T}A$$ is continuous, so $$O(n)$$ is the inverse image of the closed singleton $$\{I\}$$ and is closed. Each column of an orthogonal matrix has Euclidean norm $$1$$, so every entry has absolute value at most $$1$$; hence $$O(n)$$ is bounded. The Heine–Borel theorem now implies that $$O(n)$$ is compact.

### Exercise 8

Let $$C_n$$ be the union of the $$2^n$$ closed intervals remaining after $$n$$ steps, and let $$C=\bigcap_{n=0}^{\infty}C_n$$.

**(a)** Each $$C_n$$ is closed in $$[0,1]$$, so $$C$$ is closed and bounded and therefore compact. If a nondegenerate interval were contained in $$C$$, it would be contained in one of the component intervals of every $$C_n$$. Those component intervals have length $$3^{-n}$$, which tends to zero. This is impossible for an interval of positive length. Thus $$C$$ has empty interior.

**(b)** The component intervals of $$C_n$$ are exactly the intervals whose first $$n$$ ternary digits are all in $$\{0,2\}$$. Hence a point belongs to every $$C_n$$ exactly when it has a ternary expansion

$$
x=\sum_{k=1}^{\infty}a_k3^{-k},\qquad a_k\in\{0,2\}.
$$

At endpoints, choose the expansion with digits only $$0$$ and $$2$$.

**(c)** For each $$x\in C$$ and each $$n$$, choose an endpoint $$y_n\ne x$$ of the level-$$n$$ component interval containing $$x$$. Both endpoints belong to $$C$$, and $$|y_n-x|\le 3^{-n}\to0$$. Thus every point of $$C$$ is a limit point of $$C$$.

**(d)** Write each $$x\in C$$ using its digits from (b), and set

$$
\varphi(x)=\sum_{k=1}^{\infty}a_k2^{-(k+1)}.
$$

If $$x<y$$, their first differing ternary digit is $$0$$ for $$x$$ and $$2$$ for $$y$$; the corresponding binary digits in $$\varphi(x)$$ and $$\varphi(y)$$ are $$0$$ and $$1$$. The largest possible contribution of all later binary digits is exactly the difference at that first position, so $$\varphi(x)\le\varphi(y)$$. Thus $$\varphi$$ is increasing in the non-strict sense.

For any $$t\in[0,1]$$, choose a binary expansion $$t=\sum_{k=1}^{\infty}b_k2^{-k}$$ with $$b_k\in\{0,1\}$$. The point $$x=\sum_{k=1}^{\infty}2b_k3^{-k}$$ lies in $$C$$ and satisfies $$\varphi(x)=t$$. Therefore $$\varphi$$ is surjective.

To prove continuity, choose $$n$$ so that $$2^{-n}<\varepsilon$$. Distinct level-$$n$$ component intervals are separated by gaps of length at least $$3^{-n}$$. Thus if $$x,y\in C$$ and $$|x-y|<3^{-n}$$, they lie in the same such interval and have the same first $$n$$ ternary digits. The tails in their $$\varphi$$ values differ by at most $$2^{-n}<\varepsilon$$. Hence $$\varphi$$ is continuous.

**(e)** Since $$\varphi:C\to[0,1]$$ is surjective and $$[0,1]$$ is uncountable, $$C$$ is uncountable.

**(f)** Every component of $$[0,1]\setminus C$$ is an open interval $$(a,b)$$ with endpoints in $$C$$. The ternary expansions at these two endpoints have the same prefix and then the forms $$0.222\ldots$$ and $$2.000\ldots$$; their images under $$\varphi$$ agree. Define $$f=\varphi$$ on $$C$$ and set $$f(t)=\varphi(a)=\varphi(b)$$ for $$t\in(a,b)$$. This makes $$f$$ constant on each complementary interval.

The continuous function $$\varphi$$ is uniformly continuous on the compact set $$C$$. If $$x\in C$$ and $$t\notin C$$ lies in a complementary interval $$(a,b)$$, the endpoint on the same side of $$x$$ is at distance at most $$|t-x|$$ from $$x$$. Therefore, as $$t\to x$$, the value $$f(t)$$ tends to $$\varphi(x)=f(x)$$ by uniform continuity of $$\varphi$$. On the open complementary intervals $$f$$ is constant, so it is continuous there as well. This gives the required continuous extension.

### Exercise 9

For a real-valued function on a metric space, lower continuity is equivalent to the sequential condition $$f(a)\le\liminf_{k\to\infty}f(x_k)$$ whenever $$x_k\to a$$. Its upper-continuous counterpart is $$f(a)\ge\limsup_{k\to\infty}f(x_k)$$.

**(a)** Suppose first that $$f$$ is lower continuous. If (ii) failed at $$a$$ for some $$\varepsilon>0$$, we could choose $$x_k\in B(a,1/k)$$ with $$f(x_k)\le f(a)-\varepsilon$$. Then $$x_k\to a$$ but $$\liminf f(x_k)\le f(a)-\varepsilon$$, a contradiction. Thus (ii) holds.

If (ii) holds and $$f(a)>\alpha$$, choose $$\varepsilon=(f(a)-\alpha)/2$$. The resulting neighborhood has $$f(x)>f(a)-\varepsilon>\alpha$$, proving that $$f^{-1}((\alpha,\infty))$$ is open. Conversely, if all these inverse images are open, then for any $$a$$ and $$\varepsilon>0$$ the open set $$f^{-1}((f(a)-\varepsilon,\infty))$$ is a neighborhood of $$a$$ on which the inequality in (ii) holds. Finally,

$$
f^{-1}((-\infty,\alpha])=X\setminus f^{-1}((\alpha,\infty)),
$$

so (iii) and (iv) are equivalent. This proves the equivalence.

**(b)** If $$f$$ is continuous, then both $$f$$ and $$-f$$ are lower continuous. Conversely, lower continuity of $$f$$ and $$-f$$ gives, for every sequence $$x_k\to a$$,

$$
f(a)\le\liminf f(x_k)\le\limsup f(x_k)\le f(a).
$$

Therefore $$f(x_k)\to f(a)$$, which is sequential continuity and hence continuity in a metric space.

**(c)** Let $$\chi_A$$ equal $$1$$ on $$A$$ and $$0$$ outside $$A$$. If $$A$$ is open, then every point of $$A$$ has a neighborhood on which $$\chi_A=1$$; at points outside $$A$$, the lower-continuity inequality is automatic because $$\chi_A\ge0$$. Thus $$\chi_A$$ is lower continuous. Conversely, if $$\chi_A$$ is lower continuous and $$a\in A$$, apply (ii) with $$\varepsilon=1/2$$. On the resulting neighborhood, $$\chi_A(x)>1/2$$, so $$x\in A$$. Thus every point of $$A$$ is interior and $$A$$ is open.

**(d)** Let $$m=\inf f(X)$$ and choose a sequence $$x_k\in X$$ such that $$f(x_k)\to m$$ (allowing initially $$m=-\infty$$). Compactness gives a subsequence $$x_{k_j}\to x\in X$$. Lower continuity yields

$$
f(x)\le\liminf_{j\to\infty}f(x_{k_j})=m.
$$

Since $$m\le f(x)$$, equality holds. In particular, $$m$$ cannot be $$-\infty$$, and $$x$$ is a point where $$f$$ attains its minimum.

### Exercise 10

In every bounded interval there are only finitely many rationals whose reduced denominators are at most a fixed $$N$$.

**(a)** The function $$f$$ is upper continuous. Indeed, fix $$a\in[0,1]$$ and $$\varepsilon>0$$. Choose $$N$$ so large that $$1/N<f(a)+\varepsilon$$, and choose a neighborhood of $$a$$ containing no rational of denominator at most $$N$$ other than possibly $$a$$ itself. At every point $$x$$ in that neighborhood, either $$x=a$$ or $$f(x)\le1/N<f(a)+\varepsilon$$. This is the upper-continuity condition.

**(b)** The function $$f$$ is not lower continuous at any rational $$a$$: irrational points approach $$a$$ and have value $$0<f(a)$$. It is lower continuous at every irrational $$a$$, because $$f(a)=0$$ and $$f(x)\ge0$$ for all $$x$$. Thus the statement that $$f$$ is lower continuous is false.

**(c)–(d)** Rationals in $$[0,1]$$ with reduced denominator $$2^k$$ are dense as $$k\to\infty$$, and their $$g$$-values tend to $$1$$. Rationals with reduced denominator $$3^k$$ are also dense as $$k\to\infty$$, and their $$g$$-values tend to $$-1$$. Consequently, at every $$a\in[0,1]$$,

$$
\limsup_{x\to a}g(x)=1,\qquad \liminf_{x\to a}g(x)=-1.
$$

But $$-1<g(a)<1$$ for every $$a$$. The upper-continuity inequality $$g(a)\ge\limsup_{x\to a}g(x)$$ and the lower-continuity inequality $$g(a)\le\liminf_{x\to a}g(x)$$ both fail. So $$g$$ is neither upper nor lower continuous.

### Exercise 11

Suppose $$\lim_{t\to1^-}f(t)=L\in X$$ and define $$\widetilde f:[0,1]\to X$$ by $$\widetilde f(t)=f(t)$$ for $$t<1$$ and $$\widetilde f(1)=L$$. The assumed limit makes $$\widetilde f$$ continuous at $$1$$; it is continuous elsewhere by hypothesis. Since $$[0,1]$$ is compact, the continuous map $$\widetilde f$$ is uniformly continuous. Its restriction $$f$$ to $$[0,1)$$ is therefore uniformly continuous.

### Exercise 12

The function $$f(t)=(1+t^2)^{-1}$$ is uniformly continuous. Its derivative satisfies

$$
|f'(t)|=\frac{2t}{(1+t^2)^2}\le2\qquad(t>0),
$$

so the mean value theorem makes $$f$$ Lipschitz.

The function $$g(t)=t^{-2}$$ is not uniformly continuous. Take $$x_n=1/n$$ and $$y_n=2/n$$. Then $$|x_n-y_n|=1/n\to0$$, but

$$
|g(x_n)-g(y_n)|=\left|n^2-\frac{n^2}{4}\right|=\frac{3n^2}{4}\not\longrightarrow0.
$$

### Exercise 13

Let $$F$$ have finite dimension $$m$$ and choose a basis $$e_1,\ldots,e_m$$. Let $$v_k\in F$$ and suppose $$v_k\to v\in E$$. The sequence $$v_k$$ is bounded. By equivalence of norms on $$F$$, its coordinate vectors in this basis are bounded in $$\mathbb K^m$$. Bolzano–Weierstrass gives a subsequence of coordinate vectors converging to some $$a=(a_1,\ldots,a_m)$$. Hence the corresponding subsequence $$v_{k_j}$$ converges in $$F$$ to $$w=\sum_{i=1}^m a_i e_i\in F$$. It also converges in $$E$$ to $$v$$. Uniqueness of limits gives $$v=w\in F$$. Thus $$F$$ contains every limit in $$E$$ of its convergent sequences, so $$F$$ is closed.

### Exercise 14

For $$\delta>0$$, write

$$
\omega_f(x,\delta)=\sup\{|f(u)-f(v)|:u,v\in B(x,\delta)\},\qquad
\omega_f(x)=\inf_{\delta>0}\omega_f(x,\delta).
$$

Boundedness of $$f$$ makes these quantities finite. To prove upper continuity, it suffices to show that $$\{x:\omega_f(x)<\alpha\}$$ is open for each $$\alpha\in\mathbb R$$. Let $$\omega_f(x)<\alpha$$. Choose $$\delta>0$$ with $$\omega_f(x,\delta)<\alpha$$. If $$d(x,y)<\delta/2$$, set $$r=\delta-d(x,y)>0$$. The triangle inequality gives $$B(y,r)\subseteq B(x,\delta)$$, and therefore

$$
\omega_f(y)\le\omega_f(y,r)\le\omega_f(x,\delta)<\alpha.
$$

So a neighborhood of $$x$$ lies in $$\{y:\omega_f(y)<\alpha\}$$, proving that this set is open. Hence $$\omega_f$$ is upper continuous.

### Exercise 15

In the supremum norm on $$\ell^\infty$$, distinct unit vectors satisfy

$$
\|e_n-e_m\|_\infty=1\qquad(n\ne m).
$$

Thus the sequence $$(e_n)$$ has no Cauchy subsequence and hence no convergent subsequence. A compact metric space is sequentially compact, so the closed unit ball of $$\ell^\infty$$ is not compact.
