# Chapter III — Continuous Functions

## 2. The Fundamentals of Topology

### Exercise 1

Here $$M'$$ denotes the set of limit points of $$M$$.

**(a)** For $$M=(0,1]$$ in $$\mathbb R$$,

$$
\overline M=[0,1],\qquad \mathring M=(0,1),\qquad \partial M=\{0,1\},\qquad M'=[0,1].
$$

**(b)** For $$M=(0,1]\times\{0\}$$ in $$\mathbb R^2$$,

$$
\overline M=[0,1]\times\{0\},\qquad \mathring M=\varnothing,\qquad \partial M=M'=[0,1]\times\{0\}.
$$

The segment has empty interior in the plane, and its only added closure point is its left endpoint.

**(c)** For $$M=\{1/n:n\in\mathbb N^\times\}$$ in $$\mathbb R$$,

$$
\overline M=M\cup\{0\},\qquad \mathring M=\varnothing,\qquad \partial M=M\cup\{0\},\qquad M'=\{0\}.
$$

Each point $$1/n$$ is isolated in $$M$$, while the sequence $$1/n$$ converges to $$0$$.

**(d)** The rationals are dense in $$\mathbb R$$ and contain no interval, so

$$
\overline{\mathbb Q}=\mathbb R,\qquad \mathring{\mathbb Q}=\varnothing,\qquad \partial\mathbb Q=\mathbb Q'=\mathbb R.
$$

**(e)** The irrationals are also dense and contain no interval. Hence

$$
\overline{\mathbb R\setminus\mathbb Q}=\mathbb R,\qquad \mathring{(\mathbb R\setminus\mathbb Q)}=\varnothing,\qquad \partial(\mathbb R\setminus\mathbb Q)=(\mathbb R\setminus\mathbb Q)'=\mathbb R.
$$

### Exercise 2

Write $$S=\mathbb Q\cap(-\sqrt2,\sqrt2)$$, where $$\mathbb Q$$ carries the subspace metric from $$\mathbb R$$. Since $$(-\sqrt2,\sqrt2)$$ is open in $$\mathbb R$$, its intersection with $$\mathbb Q$$ is open in $$\mathbb Q$$. Also,

$$
\mathbb Q\setminus S=\mathbb Q\cap\bigl(( -\infty,-\sqrt2)\cup(\sqrt2,\infty)\bigr)
$$

is open in $$\mathbb Q$$. Thus $$S$$ is both open and closed in $$\mathbb Q$$. The irrational endpoints are not points of $$\mathbb Q$$, which is why this bounded interval is also closed relative to $$\mathbb Q$$.

### Exercise 3

**(a)** In the discrete metric, $$B(x,1/2)=\{x\}$$. Every singleton is open, and every subset of $$X$$ is a union of singletons. Therefore every subset is open and the induced topology is $$\mathcal P(X)$$.

**(b)** If $$X$$ has at least two points, then for any $$x\in X$$,

$$
B(x,1)=\{x\},\qquad \overline B(x,1)=X.
$$

So the open and closed balls need not agree.

### Exercise 4

Let $$D=B_{\mathbb R^2}(0,1)$$ and $$L=[0,1)\times\{0\}$$. The closure of $$L$$ in $$\mathbb R^2$$ is $$[0,1]\times\{0\}$$, whose intersection with $$D$$ is exactly $$L$$. Thus $$L$$ is closed relative to $$D$$. Consequently $$S=D\setminus L$$ is open relative to the open set $$D$$, hence open in $$\mathbb R^2$$. Therefore

$$
\mathring S=S.
$$

### Exercise 5

For any $$x\in X$$,

$$
x\in\mathring A
\quad\Longleftrightarrow\quad
\text{some neighborhood of }x\text{ is contained in }A
\quad\Longleftrightarrow\quad
x\notin\overline{X\setminus A}.
$$

The last equivalence says exactly that no neighborhood of $$x$$ meets $$X\setminus A$$. Hence $$\mathring A=X\setminus\overline{(X\setminus A)}$$.

### Exercise 6

Use the product metric $$d((x_j),(y_j))=\max_j d_j(x_j,y_j)$$, which induces the usual finite product topology.

**(a)** If $$x=(x_1,\ldots,x_n)\in O_1\times\cdots\times O_n$$, choose $$\varepsilon_j>0$$ such that $$B_{X_j}(x_j,\varepsilon_j)\subseteq O_j$$. With $$\varepsilon=\min_j\varepsilon_j$$, the product ball $$B_X(x,\varepsilon)$$ is contained in $$O_1\times\cdots\times O_n$$. Thus the product is open.

**(b)** For each coordinate projection $$\pi_j:X\to X_j$$, the set $$A_j$$ is closed, so $$\pi_j^{-1}(A_j)$$ is closed. Since

$$
A_1\times\cdots\times A_n=\bigcap_{j=1}^n\pi_j^{-1}(A_j),
$$

the product is a finite intersection of closed sets and is closed.

### Exercise 7

First note that $$h$$ is monotone: if $$A\subseteq B$$, then $$B=A\cup(B\setminus A)$$ and

$$
h(B)=h(A)\cup h(B\setminus A)\supseteq h(A).
$$

**(a)** Let $$\mathcal T_h=\{A^c:h(A)=A\}$$. Extensivity gives $$h(X)=X$$, and (i) gives $$h(\varnothing)=\varnothing$$, so $$X,\varnothing\in\mathcal T_h$$. If $$h(A_i)=A_i$$ for every $$i$$, monotonicity and extensivity imply

$$
\bigcap_i A_i\subseteq h\!\left(\bigcap_i A_i\right)\subseteq\bigcap_i h(A_i)=\bigcap_i A_i.
$$

Thus arbitrary intersections of fixed sets are fixed, so arbitrary unions of members of $$\mathcal T_h$$ belong to $$\mathcal T_h$$. Also, if $$h(A)=A$$ and $$h(B)=B$$, then (iii) gives $$h(A\cup B)=A\cup B$$. Taking complements shows that $$\mathcal T_h$$ is closed under finite intersections. These are the topology axioms.

**(b)** Given a topology $$\mathcal T$$, define $$h(A)=\overline A$$, the closure in that topology. Closure is extensive, sends $$\varnothing$$ to $$\varnothing$$, is idempotent, and satisfies $$\overline{A\cup B}=\overline A\cup\overline B$$. Its fixed sets are precisely the closed sets. Their complements are exactly the open sets, so $$\mathcal T_h=\mathcal T$$.

### Exercise 8

The union identity is false in general. For $$A=[0,1]$$ and $$B=[1,2]$$ in $$\mathbb R$$,

$$
(A\cup B)^\circ=(0,2),\qquad A^\circ\cup B^\circ=(0,1)\cup(1,2).
$$

The intersection identity is true: $$A^\circ\cap B^\circ$$ is open and contained in $$A\cap B$$, so it is contained in $$(A\cap B)^\circ$$. Conversely, every open subset of $$A\cap B$$ is an open subset of both $$A$$ and $$B$$, hence is contained in $$A^\circ\cap B^\circ$$. Therefore $$(A\cap B)^\circ=A^\circ\cap B^\circ$$.

### Exercise 9

For all $$x,y\in\mathbb R$$, $$\delta(x,y)<1$$, so every subset of $$\mathbb R$$ is bounded in this metric. Moreover, $$\delta$$ induces the usual topology: for $$0<r<1$$,

$$
B_\delta(x,r)=\left(x-\frac{r}{1-r},x+\frac{r}{1-r}\right).
$$

Thus each $$A_n=[n,\infty)$$ is closed, as it is closed in the usual metric. The sets are decreasing, and

$$
\bigcap_{n=0}^k A_n=[k,\infty)\ne\varnothing
$$

for each finite $$k$$, whereas $$\bigcap_{n=0}^{\infty}A_n=\varnothing$$.

### Exercise 10

The listed family contains $$\varnothing$$ and $$X$$. For its four nontrivial proper sets, the distinct pairwise unions are $$\{1,3,4\}$$, $$\{2,3,4,5\}$$, or $$X$$, while the distinct pairwise intersections are $$\varnothing$$, $$\{1\}$$, or $$\{3,4\}$$. All are in $$\mathcal T$$. Since the family is finite, arbitrary unions reduce to finite unions, so $$\mathcal T$$ is a topology.

The closed sets are the complements of members of $$\mathcal T$$. The closed supersets of $$\{2,4,5\}$$ are $$X$$ and $$\{2,3,4,5\}$$. Their intersection is the smallest such closed set, so

$$
\overline{\{2,4,5\}}=\{2,3,4,5\}.
$$

### Exercise 11

The intersection $$\mathcal T_1\cap\mathcal T_2$$ is always a topology: it contains $$\varnothing$$ and $$X$$, and unions and finite intersections of its members belong to both topologies.

The union need not be a topology. On $$X=\{1,2,3\}$$, let

$$
\mathcal T_1=\{\varnothing,X,\{1\}\},\qquad
\mathcal T_2=\{\varnothing,X,\{2\}\}.
$$

Both are topologies, but $$\{1\}\cup\{2\}=\{1,2\}\notin\mathcal T_1\cup\mathcal T_2$$.

### Exercise 12

Suppose first that $$f$$ is continuous. If $$x\in\overline A$$ and $$V$$ is any open neighborhood of $$f(x)$$, then $$f^{-1}(V)$$ is an open neighborhood of $$x$$, so it meets $$A$$. Hence $$V$$ meets $$f(A)$$, proving $$f(x)\in\overline{f(A)}$$. Thus $$f(\overline A)\subseteq\overline{f(A)}$$.

Conversely, assume this inclusion holds for every $$A\subseteq X$$. For any closed $$C\subseteq Y$$, set $$A=f^{-1}(C)$$. Then

$$
f(\overline A)\subseteq\overline{f(A)}\subseteq C,
$$

so $$\overline A\subseteq f^{-1}(C)=A$$. Therefore every closed set has a closed preimage, which is equivalent to continuity.

### Exercise 13

Let $$F$$ be closed in $$Y$$. Continuity of $$g$$ and $$h$$ implies that $$g^{-1}(F)$$ is closed in $$A$$ and $$h^{-1}(F)$$ is closed in $$B$$. Since $$A$$ and $$B$$ are closed in $$X$$, these two preimages are closed in $$X$$. The compatibility on $$A\cap B$$ makes $$f$$ well-defined, and

$$
f^{-1}(F)=g^{-1}(F)\cup h^{-1}(F)
$$

is closed in $$X$$, hence closed in the subspace $$A\cup B$$. The closed-set characterization of continuity now shows that $$f$$ is continuous.

### Exercise 14

**(a)** In the discrete topology every subset of $$\mathbb R$$ is both open and closed. Thus the identity from the usual topology to the discrete topology is open and closed. It is not continuous: the preimage of the discrete-open singleton $$\{0\}$$ is $$\{0\}$$, which is not open in the usual topology.

**(b)** Every subset is open in the domain's discrete topology, so the preimage of every usual-open set is open; the identity is continuous. It is not open because $$\{0\}$$ is open in the discrete topology but not in the usual one. It is not closed because $$\mathbb Q$$ is closed in the discrete topology but is not closed in the usual topology.

### Exercise 15

The functions $$x\mapsto e^x$$ and $$\operatorname{zigzag}$$ are continuous, so their product $$f$$ is continuous. For $$x\le-1/2$$, $$\operatorname{zigzag}(x)\le1/2$$ gives $$f(x)\le e^{-1/2}/2$$. On $$[-1/2,0]$$, $$\operatorname{zigzag}(x)=-x$$, and $$(-x)e^x$$ decreases from $$e^{-1/2}/2$$ to $$0$$. Since the image of the connected interval $$(-\infty,0)$$ is an interval and contains both endpoints, we get

$$
f(( -\infty,0))=[0,e^{-1/2}/2].
$$

This is not open, so $$f$$ is not an open map. For the closed set $$C=\{-(2n+1)/2:n\in\mathbb N\}$$, the zigzag factor is $$1/2$$ at each point, and

$$
f(C)=\{e^{-(2n+1)/2}/2:n\in\mathbb N\}.
$$

These values converge to $$0$$, which is not in $$f(C)$$. Hence $$f(C)$$ is not closed and $$f$$ is not a closed map.

### Exercise 16

On $$[0,1]$$ the function is constant, and on $$(1,2]$$ it is $$x-1$$; the right-hand limit at $$1$$ is $$0=f(1)$$. Thus $$f$$ is continuous.

The domain $$[0,2]$$ is compact. Every closed subset of it is compact, and its continuous image is compact, hence closed in the Hausdorff space $$[0,2]$$. Therefore $$f$$ is closed. It is not open: $$(0,1)$$ is open in the relative topology of $$[0,2]$$, but its image is $$\{0\}$$, which is not open there.

### Exercise 17

As printed, the two cases overlap when $$y=0$$: at $$(1,0)$$ they give different values, and the second gives $$2\notin[0,2)$$. Thus the displayed rule is not well-defined literally. With the apparent intended second condition $$y<0$$ (and the first condition $$y\ge0$$), the claimed properties follow.

Under that correction, $$f$$ is not continuous at $$(1,0)$$: along the lower semicircle approaching this point, $$1+x\to2$$, while $$f(1,0)=0$$. It is not open because the open upper semicircle $$U=\{(x,y)\in S^1:y>0\}$$ maps to $$\{0\}$$, which is not open in $$[0,2)$$.

To see that it is closed, let $$F$$ be closed in $$S^1$$ and let $$t_k\in f(F)$$ converge to $$t\in[0,2)$$. Choose $$z_k\in F$$ with $$f(z_k)=t_k$$. Compactness of $$S^1$$ gives a subsequence converging to some $$z\in F$$. Passing to a further subsequence, its points all lie in the upper part $$y\ge0$$ or all in the lower part $$y<0$$. In the first case, $$t=0=f(z)$$. In the second, if $$z$$ has $$y<0$$, continuity of the formula there gives $$t=f(z)$$; if $$z$$ lies on the equator, then $$z=(-1,0)$$ gives $$t=0=f(z)$$, while $$z=(1,0)$$ would force $$t_k\to2$$, contrary to $$t<2$$. Thus every convergent sequence in $$f(F)$$ has its limit in $$f(F)$$, so $$f(F)$$ is closed in the metric space $$[0,2)$$.

### Exercise 18

For any open $$O\subseteq X$$, $$p^{-1}(O)=O\times Y$$ is open, so $$p$$ is continuous. If $$U\subseteq X\times Y$$ is open, then for every $$(x,y)\in U$$ there are open sets $$V\subseteq X$$ and $$W\subseteq Y$$ with $$(x,y)\in V\times W\subseteq U$$. Thus $$V\subseteq p(U)$$, and $$p(U)$$ is open. Hence $$p$$ is open.

It need not be closed. For $$X=Y=\mathbb R$$, the set $$F=\{(x,y):xy=1\}$$ is closed, but its projection is $$\mathbb R\setminus\{0\}$$, which is not closed.

### Exercise 19

Let $$X$$ be an arbitrary topological space and let $$x_0\in X$$.

**Proposition 1.5.** Suppose $$f$$ and $$g$$ are continuous at $$x_0$$. Given $$\varepsilon>0$$, continuity provides neighborhoods of $$x_0$$ on which $$f$$ and $$g$$ differ from their values at $$x_0$$ by less than any prescribed positive tolerance. Intersecting these neighborhoods shows directly, by the norm triangle inequality, that $$f+g$$ and $$\lambda f$$ are continuous at $$x_0$$. For scalar-valued functions, continuity also makes $$f$$ and $$g$$ locally bounded near $$x_0$$: for example, choose a neighborhood on which $$|f(x)-f(x_0)|<1$$. Then

$$
|f(x)g(x)-f(x_0)g(x_0)|
\le |f(x)|\,|g(x)-g(x_0)|+|g(x_0)|\,|f(x)-f(x_0)|,
$$

which tends to zero as both differences are made small. If $$g(x_0)\ne0$$, choose a neighborhood on which $$|g(x)|\ge|g(x_0)|/2$$. There

$$
\left|\frac{f(x)}{g(x)}-\frac{f(x_0)}{g(x_0)}\right|
\le \frac{2}{|g(x_0)|}|f(x)-f(x_0)|+\frac{2|f(x_0)|}{|g(x_0)|^2}|g(x)-g(x_0)|,
$$

so the quotient is continuous as well. These neighborhood arguments use only the definition of continuity at a point, not sequences or a metric on $$X$$.

**Proposition 1.10.** The coordinate projections $$\pi_k:\mathbb K^m\to\mathbb K$$ are continuous, so continuity of $$f=(f_1,\ldots,f_m)$$ implies continuity of every $$f_k=\pi_k\circ f$$. Conversely, the norm topology on $$\mathbb K^m$$ is its finite product topology. A basic neighborhood of $$f(x_0)$$ contains a product $$V_1\times\cdots\times V_m$$ of coordinate neighborhoods. If each $$f_k$$ is continuous at $$x_0$$, the intersection of the finitely many neighborhoods $$f_k^{-1}(V_k)$$ is a neighborhood of $$x_0$$ mapped into that product. Hence $$f$$ is continuous at $$x_0$$. For $$\mathbb K=\mathbb C$$ and $$m=1$$, the coordinates are $$\operatorname{Re}f$$ and $$\operatorname{Im}f$$.

### Exercise 20

Fix $$n\in\mathbb N^\times$$ and suppose $$x\notin A_n$$, so $$\omega_f(x)<1/n$$. By the definition as an infimum, there is $$\varepsilon>0$$ such that $$\omega_f(x,\varepsilon)<1/n$$. For any $$y\in B(x,\varepsilon/2)$$, choose $$r=\varepsilon-d(x,y)>0$$. The triangle inequality gives $$B(y,r)\subseteq B(x,\varepsilon)$$, and therefore

$$
\omega_f(y)\le\omega_f(y,r)\le\omega_f(x,\varepsilon)<1/n.
$$

Thus $$B(x,\varepsilon/2)$$ is contained in the complement of $$A_n$$. The complement is open, so $$A_n$$ is closed.

### Exercise 21

**(i)** Suppose $$A$$ is complete and $$x\in\overline A$$. Choose a sequence $$x_k\in A$$ with $$x_k\to x$$ in $$X$$. It is Cauchy in $$A$$, so completeness gives a limit $$a\in A$$. Uniqueness of limits in a metric space yields $$x=a\in A$$. Hence $$A$$ is closed in $$X$$.

The converse can fail when $$X$$ is incomplete: take $$X=A=(0,1)$$ with the usual metric. The set $$A$$ is closed in itself but is not complete, since, for example, $$1/n$$ is Cauchy in $$A$$ and has no limit there.

**(ii)** If $$X$$ is complete and $$A$$ is closed in $$X$$, every Cauchy sequence in $$A$$ converges in $$X$$ to some point of $$X$$, and closedness puts that limit in $$A$$. Thus $$A$$ is complete. The reverse implication follows from (i).
