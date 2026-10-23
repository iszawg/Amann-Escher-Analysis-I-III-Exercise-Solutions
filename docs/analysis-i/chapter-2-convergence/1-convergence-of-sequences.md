# Chapter II — Convergence

## 1. Convergence of Sequences

### Exercise 1

**(a)** For the discrete metric, distinct points have distance $$1$$. Thus

$$
B_X(a,r)=\begin{cases}\{a\},&0<r\le1,\\X,&r>1,\end{cases}
\qquad
\overline B_X(a,r)=\begin{cases}\{a\},&0<r<1,\\X,&r\ge1.\end{cases}
$$

**(b)** A point $$a$$ is a cluster point of $$(x_n)$$ exactly when $$x_n=a$$ for infinitely many indices. Indeed, the open ball of radius $$1$$ about $$a$$ is $$\{a\}$$.

**(c)** The sequence converges to $$a$$ exactly when it is eventually equal to $$a$$. This is the condition that all but finitely many terms lie in $$B_X(a,1)=\{a\}$$.

### Exercise 2

Write $$x=(x_1,\ldots,x_m)$$, and define $$d(x,y)=\max_{1\le j\le m}d_j(x_j,y_j)$$. Nonnegativity and symmetry follow from the component metrics. If $$d(x,y)=0$$, then every $$d_j(x_j,y_j)=0$$, hence $$x_j=y_j$$ for each $$j$$ and $$x=y$$. For any $$x,y,z$$,

$$
d(x,y)\le \max_j\bigl(d_j(x_j,z_j)+d_j(z_j,y_j)\bigr)
\le d(x,z)+d(z,y),
$$

so $$d$$ is a metric. Moreover, $$d(a,x)<r$$ holds exactly when $$d_j(a_j,x_j)<r$$ for every $$j$$; replacing $$<$$ by $$\le$$ gives the closed-ball statement. Therefore

$$
B_X(a,r)=\prod_{j=1}^m B_{X_j}(a_j,r),
\qquad
\overline B_X(a,r)=\prod_{j=1}^m\overline B_{X_j}(a_j,r).
$$

### Exercise 3

For $$n\ge1$$,

$$
|z_n-(1+i)|=\left|\left(1-\frac1n\right)(1+i)-(1+i)\right|=\frac{\sqrt2}{n}\longrightarrow0.
$$

Given $$\varepsilon>0$$, choose $$N>\sqrt2/\varepsilon$$. Then for every $$n\ge N$$,

$$
|z_n-(1+i)|=\frac{\sqrt2}{n}<\varepsilon.
$$

This is the definition of convergence, so $$z_n\to1+i$$.

### Exercise 4

These are the boundedness claims in Examples 1.9.

**(a)** If $$x,y\in B(a,r)$$, then $$d(x,y)\le d(x,a)+d(a,y)<2r$$. For $$x,y\in\overline B(a,r)$$ the same argument gives $$d(x,y)\le2r$$. Thus both balls are bounded.

**(b)** Every subset of a bounded set is bounded. For finitely many bounded sets $$Y_1,\ldots,Y_q$$, discard any empty sets and choose $$p_j\in Y_j$$ and $$M_j<\infty$$ with $$d(x,p_j)\le M_j$$ for $$x\in Y_j$$. Since there are only finitely many pairs of centers, $$D:=\max_{j,k}(M_j+d(p_j,p_k)+M_k)$$ is finite and bounds all distances between points in the union.

**(c)** If $$Y$$ is nonempty and bounded, choose $$x_0\in Y$$. A finite bound $$M$$ for distances in $$Y$$ gives $$Y\subset B_X(x_0,M+1)$$. Conversely, if $$Y\subset B_X(x_0,r)$$, then $$d(x,y)<2r$$ for $$x,y\in Y$$, so $$Y$$ is bounded. The empty set is bounded as well.

**(d)** A bounded interval $$I\subset\mathbb R$$ lies in some interval $$[a,b]$$ with finite endpoints, so $$|x-y|\le b-a$$ for all $$x,y\in I$$.

**(e)** If $$|y|\le M$$ for every $$y\in Y\subset K$$, then $$|y-z|\le2M$$ for all $$y,z\in Y$$. Conversely, if $$Y\ne\varnothing$$ has diameter at most $$D$$, choose $$y_0\in Y$$; then $$|y|\le |y-y_0|+|y_0|\le D+|y_0|$$. Thus boundedness in $$K$$ is equivalent to a uniform bound on absolute values.

### Exercise 5

**(a)** Put $$\zeta=(1+i)/\sqrt2=e^{i\pi/4}$$. Then $$z_n=\zeta^n$$ is periodic with period $$8$$, and every value in one period occurs infinitely often. Its cluster points are

$$
\{e^{ik\pi/4}:k=0,1,\ldots,7\}.
$$

**(b)** For odd $$n$$, $$1+(-1)^n=0$$ and $$z_n=-1$$. For even $$n$$,

$$
z_n=2(n+1)^{n-1}+1\longrightarrow+\infty.
$$

Thus the only cluster point is $$-1$$.

**(c)** Along even indices, $$z_n=n/(n+1)\to1$$; along odd indices, $$z_n=-n/(n+1)\to-1$$. These are all the cluster points, since every subsequence has an even-index or odd-index subsequence. Hence the cluster-point set is $$\{-1,1\}$$.

### Exercise 6

Set $$L_k=(k^2+k-2)/2$$ and $$U_k=(k^2+3k-2)/2$$. These are integers, $$L_1=0$$, and $$U_k+1=L_{k+1}$$. Therefore the integer intervals $$[L_k,U_k]$$ partition $$\mathbb N$$, proving that each $$n\in\mathbb N$$ determines exactly one admissible $$k\in\mathbb N^\times$$. Within this block write $$n=L_k+j$$, where $$0\le j\le k$$. Then

$$
a_n=n+\frac1k-L_k=j+\frac1k.
$$

For each fixed $$j\in\mathbb N$$, choosing $$n_k=L_k+j$$ for all $$k\ge\max(1,j)$$ gives $$a_{n_k}=j+1/k\to j$$. Conversely, along any convergent subsequence the block index $$k$$ tends to infinity, so the corresponding integers $$j$$ satisfy $$j=a_n-1/k\to a$$, where $$a$$ is the subsequential limit. A convergent sequence of integers is eventually constant, so $$a\in\mathbb N$$. Thus the cluster points are exactly $$\mathbb N$$.

### Exercise 7

The function is symmetric and nonnegative, and $$d(m,n)=0$$ exactly when $$m=n$$. For the triangle inequality, if $$m=n$$ it is immediate. If $$m\ne n$$ and $$p=m$$ or $$p=n$$, it is equality. Otherwise,

$$
d(m,p)+d(p,n)=\frac1m+\frac1p+\frac1p+\frac1n\ge\frac1m+\frac1n=d(m,n).
$$

Hence $$d$$ is a metric. If $$m\ne n$$, then $$d(m,n)=1/m+1/n\le1+1/n$$; the center $$n$$ is in its own closed ball as well. Consequently $$A_n=\mathbb N^\times$$ for every $$n\in\mathbb N^\times$$.

### Exercise 8

In the metric inherited by $$X$$ from $$\mathbb C$$, a closed ball is the intersection of the corresponding ambient closed disk with $$X$$. Since every $$z\in X$$ satisfies $$|z|\le3$$,

$$
\overline B_X(0,3)=X,
\qquad
\overline B_X(2,4)=\{z\in\mathbb C:|z|\le3,\ |z-2|\le4\}.
$$

The second set is the intersection of $$X$$ with the closed disk of radius $$4$$ centered at $$2$$. In particular, it is contained in $$X=\overline B_X(0,3)$$, as required.

### Exercise 9

Let $$f(t)=t/(1+t)$$ for $$t\ge0$$. The function is increasing and

$$
\frac{a}{1+a}+\frac{b}{1+b}-\frac{a+b}{1+a+b}
=\frac{ab(a+b+2)}{(1+a)(1+b)(1+a+b)}\ge0.
$$

Thus, with $$a=d(x,y)$$ and $$b=d(y,z)$$, the triangle inequality for $$d$$ gives

$$
\delta(x,z)=f(d(x,z))\le f(a+b)\le f(a)+f(b)=\delta(x,y)+\delta(y,z).
$$

Symmetry and separation follow from those of $$d$$, so $$\delta$$ is a metric.

For the first ball inclusion, if $$0<\varepsilon<1$$ take $$r_1=\varepsilon/(1-\varepsilon)$$; then $$d(x,y)<r_1$$ implies $$\delta(x,y)<\varepsilon$$. If $$\varepsilon\ge1$$, take $$r_1=1$$, since $$\delta(x,y)<1\le\varepsilon$$. For the other inclusion take $$r_2=\varepsilon/(1+\varepsilon)$$. Since $$f$$ is strictly increasing and $$f(\varepsilon)=r_2$$, $$\delta(x,y)<r_2$$ implies $$d(x,y)<\varepsilon$$. These choices prove that $$d$$ and $$\delta$$ are equivalent.

### Exercise 10

**(a)** The map $$T(x)=1/x$$ is injective on $$X=(0,1)$$, and $$d(x,y)=|T(x)-T(y)|$$. Pulling back the usual metric on $$\mathbb R$$ by an injective map gives a metric, so $$d$$ is a metric on $$X$$.

**(b)** For $$x,y\in(0,1)$$,

$$
d(x,y)=\frac{|x-y|}{xy}\ge|x-y|.
$$

Thus $$B_d(x,\varepsilon)\subset B_{|\cdot|}(x,\varepsilon)$$. In the other direction, set $$r=\min\{x/2,\varepsilon x^2/2\}$$. If $$|x-y|<r$$, then $$y>x/2$$, and

$$
d(x,y)=\frac{|x-y|}{xy}<\frac{2|x-y|}{x^2}<\frac{2r}{x^2}\le\varepsilon.
$$

Therefore $$B_{|\cdot|}(x,r)\subset B_d(x,\varepsilon)$$, proving equivalence.

**(c)** Suppose a metric $$\rho$$ on $$\mathbb R$$ were equivalent to the natural metric and restricted to $$d$$ on $$X$$. Then $$1/n\to0$$ also in $$\rho$$. The reverse triangle inequality yields $$\rho(1/n,1)\to\rho(0,1)<\infty$$. But on $$X$$,

$$
\rho(1/n,1)=d(1/n,1)=|n-1|\longrightarrow+\infty,
$$

which is a contradiction.

### Exercise 11

The sum $$\delta(x,y)=\sum_{j=1}^n d_j(x_j,y_j)$$ is symmetric and nonnegative, and it is zero exactly when every coordinate agrees. Summing the component triangle inequalities proves its triangle inequality. For the product metric $$d(x,y)=\max_j d_j(x_j,y_j)$$,

$$
d(x,y)\le\delta(x,y)\le n\,d(x,y).
$$

Hence $$B_d(x,\varepsilon/n)\subset B_\delta(x,\varepsilon)$$ and $$B_\delta(x,\varepsilon)\subset B_d(x,\varepsilon)$$ for every $$\varepsilon>0$$. Thus the metrics are equivalent.

### Exercise 12

If $$z$$ and $$w$$ lie on the same positive ray, then $$\delta(z,w)=|z-w|=\bigl||z|-|w|\bigr|$$. Otherwise $$\delta(z,w)=|z|+|w|$$. In either case,

$$
\delta(z,w)\ge\bigl||z|-|w|\bigr|,
$$

and $$\delta(z,w)=0$$ exactly when $$z=w$$. Symmetry is immediate.

It remains to check the triangle inequality for $$z,u,w$$. If $$z,w$$ lie on the same positive ray, then

$$
\delta(z,w)=\bigl||z|-|w|\bigr|
\le\bigl||z|-|u|\bigr|+\bigl||u|-|w|\bigr|
\le\delta(z,u)+\delta(u,w).
$$

If they do not lie on the same positive ray, then $$\delta(z,w)=|z|+|w|$$. At least one of the pairs $$z,u$$ and $$u,w$$ also does not lie on one positive ray. If it is $$z,u$$, then

$$
\delta(z,u)+\delta(u,w)\ge |z|+|u|+\bigl||u|-|w|\bigr|\ge |z|+|w|=\delta(z,w);
$$

the other case is symmetric. Thus $$\delta$$ is a metric on $$\mathbb C$$.

### Exercise 13

For each $$n$$, $$\operatorname{Re}x_n=0$$. If $$x_n\to x$$, then

$$
|\operatorname{Re}x|=|\operatorname{Re}(x-x_n)|\le|x-x_n|\longrightarrow0.
$$

Therefore $$\operatorname{Re}x=0$$.
