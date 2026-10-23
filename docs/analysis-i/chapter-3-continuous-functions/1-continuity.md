# Chapter III — Continuous Functions

## 1. Continuity

### Exercise 1

For each $$n\in\mathbb Z$$ and $$x\in[n-\tfrac12,n+\tfrac12)$$, we have $$\lfloor x+\tfrac12\rfloor=n$$, so

$$
\operatorname{zigzag}(x)=|n-x|.
$$

**(a)** If $$-\tfrac12\le x<\tfrac12$$, then $$\lfloor x+\tfrac12\rfloor=0$$ and $$\operatorname{zigzag}(x)=|x|$$. At $$x=\tfrac12$$, the value is also $$|1-\tfrac12|=\tfrac12=|x|$$.

**(b)** For every integer $$n$$,

$$
\lfloor x+n+\tfrac12\rfloor=\lfloor x+\tfrac12\rfloor+n,
$$

and hence $$\operatorname{zigzag}(x+n)=\operatorname{zigzag}(x)$$.

**(c)** On each interval $$[n-\tfrac12,n+\tfrac12)$$ the graph is the line segments described by $$|n-x|$$. At a shared endpoint $$x=n+\tfrac12$$, the left and right formulas both give $$\tfrac12$$. Thus the graph is a periodic triangular wave with vertices $$(n,0)$$ and $$(n+\tfrac12,\tfrac12)$$, and it is continuous everywhere.

### Exercise 2

Write $$q=m/n$$ with $$m\in\mathbb Z$$ and $$n\in\mathbb N^\times$$. The case $$m=0$$ is immediate. For $$u,v>0$$, factor the difference of $$n$$th powers to obtain

$$
|u^{1/n}-v^{1/n}|
=\frac{|u-v|}{\displaystyle\sum_{j=0}^{n-1}u^{(n-1-j)/n}v^{j/n}}.
$$

Fix $$x_0>0$$ and restrict to $$u,v\ge x_0/2$$. Every term in the denominator is at least $$(x_0/2)^{(n-1)/n}$$, so the $$n$$th-root function is continuous at $$x_0$$. Integer powers are continuous, and taking reciprocals is continuous at positive values. Since $$x^q=(x^{1/n})^m$$ (using a reciprocal when $$m<0$$), the function $$x\mapsto x^q$$ is continuous on $$(0,\infty)$$.

### Exercise 3

For every $$x\in\mathbb R$$,

$$
|\varphi(x)|=\frac{|x|}{1+|x|}<1,
$$

so $$\varphi$$ maps into $$(-1,1)$$. Solving for $$x$$ gives

$$
\varphi^{-1}(y)=\frac{y}{1-|y|},\qquad -1<y<1.
$$

Indeed, $$1+|\varphi^{-1}(y)|=1/(1-|y|)$$, so $$\varphi(\varphi^{-1}(y))=y$$. Also, $$1-|\varphi(x)|=1/(1+|x|)$$, so $$\varphi^{-1}(\varphi(x))=x$$. This proves bijectivity. The formulas for $$\varphi$$ and $$\varphi^{-1}$$ are compositions and quotients of continuous functions with positive denominators on their domains, so both are continuous.

### Exercise 4

Since $$\sqrt2\notin\mathbb Q$$, each $$x\in\mathbb Q$$ lies strictly on one side of $$\sqrt2$$. Set $$\delta=|x-\sqrt2|/2$$. Every rational $$y$$ with $$|y-x|<\delta$$ remains on the same side of $$\sqrt2$$ as $$x$$, so $$f(y)=f(x)$$. Thus $$f$$ is locally constant at every point of its domain and is continuous.

### Exercise 5

**(a)** Let $$\mathcal U_{X_j}(x)$$ denote the neighborhoods of $$x$$ in the metric space $$X_j$$. The identity map $$i:X_1\to X_2$$ is continuous exactly when the inverse image of each $$d_2$$-open set is $$d_1$$-open. Equivalently, every $$d_2$$-neighborhood of $$x$$ is a $$d_1$$-neighborhood of $$x$$, that is, $$\mathcal U_{X_1}(x)\supseteq\mathcal U_{X_2}(x)$$ for every $$x\in X$$. This is precisely that $$d_1$$ is stronger than $$d_2$$.

**(b)** The metrics $$d_1$$ and $$d_2$$ are equivalent exactly when they induce the same neighborhoods at every point. By part (a), this holds exactly when each metric is stronger than the other.

### Exercise 6

Additivity gives $$f(n)=nf(1)$$ for integers $$n$$ and then $$f(q)=qf(1)$$ for every $$q\in\mathbb Q$$. Given $$x\in\mathbb R$$, choose rationals $$q_j\to x$$. Continuity yields

$$
f(x)=\lim_{j\to\infty}f(q_j)=\lim_{j\to\infty}q_jf(1)=xf(1).
$$

Therefore $$f$$ is linear, with slope $$f(1)$$.

### Exercise 7

Let $$S=\{1/n:n\in\mathbb N^\times\}$$. Away from $$S$$, the function is locally constant, except at $$0$$. At $$0$$, the values on the positive intervals tend to zero: for any $$\varepsilon>0$$, choose $$N$$ with $$1/N<\varepsilon$$; for sufficiently small $$x>0$$, its interval index is at least $$N$$, so $$0\le f(x)\le1/N<\varepsilon$$. Thus $$f$$ is continuous at $$0$$ as well.

At $$x=1/n$$ with $$n\ge2$$, the left-hand limit is $$1/n$$, whereas $$f(1/n)=1/(n-1)$$. At $$x=1$$, the left-hand limit is $$1$$ but $$f(1)=-1$$. Hence the discontinuities are exactly the points of $$S$$.

At every point of $$S$$, the value agrees with the right-hand limit: for $$n\ge2$$, both are $$1/(n-1)$$ at $$1/n$$, and both are $$-1$$ at $$1$$. Together with continuity elsewhere, this shows that $$f$$ is right continuous everywhere and left continuous exactly on $$\mathbb R\setminus S$$.

### Exercise 8

All the listed functions can be expressed using sums, negatives, and absolute values:

$$
f^+=\frac{f+|f|}{2},\qquad
f^-=\frac{-f+|f|}{2},\qquad
f\vee g=\frac{f+g+|f-g|}{2},\qquad
f\wedge g=\frac{f+g-|f-g|}{2}.
$$

Since absolute value, sums, and scalar multiples preserve continuity at $$x_0$$, all of $$|f|, f^+, f^-, f\vee g,$$ and $$f\wedge g$$ are continuous at $$x_0$$.

### Exercise 9

The rationals and irrationals are both dense, and $$f$$ takes the values $$1$$ and $$-1$$ on these two dense sets. Every neighborhood of any point therefore contains values of $$f$$ different from $$f(x_0)$$ by $$2$$. Thus $$f$$ is nowhere continuous.

At $$x_0=0$$, we have $$|g(x)|=|x|$$, so $$g$$ is continuous. If $$x_0\ne0$$, choose rational and irrational sequences converging to $$x_0$$. Along them, $$g$$ tends respectively to $$x_0$$ and $$-x_0$$, which differ. Thus $$g$$ is discontinuous at every nonzero point. Finally, $$|f|=1$$, $$|g(x)|=|x|$$, and $$f(x)g(x)=x$$, so $$|f|, |g|,$$ and $$f\cdot g$$ are continuous everywhere.

### Exercise 10

If $$x\in\mathbb Q$$, then $$f(x)>0$$, while every irrational sequence converging to $$x$$ has function values identically zero. Hence $$f$$ is discontinuous at each rational number.

Now let $$x\notin\mathbb Q$$ and $$\varepsilon>0$$. Choose $$N\in\mathbb N^\times$$ with $$1/N<\varepsilon$$. In the bounded interval $$[x-1,x+1]$$ there are only finitely many rational numbers whose reduced denominator is at most $$N$$. Since none equals $$x$$, choose $$\delta\in(0,1)$$ so that $$(x-\delta,x+\delta)$$ contains none of them. For any $$y$$ in this interval, either $$y$$ is irrational and $$f(y)=0$$, or $$y=m/n$$ in lowest terms with $$n>N$$ and thus $$f(y)=1/n<\varepsilon$$. Since $$f(x)=0$$, this proves continuity at every irrational number.

### Exercise 11

**(a)** Fix $$x_0\in\mathbb R$$. If $$x_0=0$$, then $$f_1(x)=f_2(x)=0$$ for all $$x$$. If $$x_0\ne0$$, the denominator $$x^2+x_0^2$$ is positive for every $$x$$, so both restrictions are quotients of continuous functions with nonzero denominator. Hence $$f_1$$ and $$f_2$$ are continuous.

**(b)** Away from $$(0,0)$$, the denominator $$x^2+y^2$$ is nonzero, so $$f$$ is continuous there. Along the sequence $$(t,t)\to(0,0)$$ with $$t\ne0$$,

$$
f(t,t)=\frac{t^2}{2t^2}=\frac12,
$$

whereas $$f(0,0)=0$$. Thus $$f$$ is discontinuous at the origin.

### Exercise 12

Use the Euclidean norms and write $$A=[a_{ij}]$$. For $$x,y\in\mathbb K^n$$, the Cauchy–Schwarz inequality gives

$$
\begin{aligned}
\|A x-A y\|_2^2
&=\sum_{i=1}^m\left|\sum_{j=1}^n a_{ij}(x_j-y_j)\right|^2\\
&\le \left(\sum_{i=1}^m\sum_{j=1}^n|a_{ij}|^2\right)\|x-y\|_2^2.
\end{aligned}
$$

Thus $$A$$ is Lipschitz continuous, with Lipschitz constant at most $$\left(\sum_{i,j}|a_{ij}|^2\right)^{1/2}$$ (or any positive larger constant if $$A=0$$).

### Exercise 13

For real normed vector spaces, additivity implies $$f(qx)=qf(x)$$ for every $$q\in\mathbb Q$$ and $$x\in V$$. For $$t\in\mathbb R$$, choose rationals $$q_j\to t$$. Then $$q_jx\to tx$$, and continuity gives

$$
f(tx)=\lim_{j\to\infty}f(q_jx)=\lim_{j\to\infty}q_jf(x)=tf(x).
$$

Together with additivity, this proves real linearity. If the exercise is interpreted for complex vector spaces and asks for complex linearity, it needs the additional assumption that $$f$$ commutes with multiplication by $$i$$: complex conjugation $$f(z)=\overline z$$ is a continuous additive map $$\mathbb C\to\mathbb C$$ but is not complex linear. The argument above proves real linearity for the underlying real vector spaces.

### Exercise 14

For $$x,y\in E$$, the Cauchy–Schwarz inequality gives

$$
|(x|x_0)-(y|x_0)|\le\|x-y\|\,\|x_0\|,
\qquad
|(x_0|x)-(x_0|y)|\le\|x_0\|\,\|x-y\|.
$$

Both functions are therefore Lipschitz continuous, and hence continuous.

### Exercise 15

Let $$q(x)=(Ax|x)$$. Since $$A$$ is a linear map on a finite-dimensional normed space, Exercise 12 shows that it is bounded. For $$x$$ near $$x_0$$,

$$
|q(x)-q(x_0)|
\le \|A(x-x_0)\|\,\|x\|+\|Ax_0\|\,\|x-x_0\|
\le \|A\|\,\|x-x_0\|\bigl(\|x\|+\|x_0\|\bigr).
$$

The factor $$\|x\|+\|x_0\|$$ is bounded in a neighborhood of $$x_0$$, so the right-hand side tends to zero as $$x\to x_0$$. Thus $$q$$ is continuous.

### Exercise 16

Under the identification of $$\mathbb K^{n\times n}$$ with $$\mathbb K^{n^2}$$ by listing the entries, each coordinate function $$A\mapsto a_{jk}$$ is continuous. The determinant is the finite polynomial

$$
\det A=\sum_{\sigma\in S_n}(\operatorname{sign}\sigma)\prod_{j=1}^n a_{j,\sigma(j)}.
$$

Finite sums and products of continuous coordinate functions are continuous, so $$A\mapsto\det A$$ is continuous.

### Exercise 17

Suppose first that $$f$$ is continuous at $$x$$. Given $$\eta>0$$, choose $$\delta>0$$ such that $$d(f(y),f(x))<\eta/2$$ whenever $$y\in B(x,\delta)$$. For $$y,z\in B(x,\delta)$$, the triangle inequality gives $$d(f(y),f(z))<\eta$$. Therefore $$\omega_f(x,\delta)\le\eta$$, and since this holds for every $$\eta>0$$, $$\omega_f(x)=0$$.

Conversely, suppose $$\omega_f(x)=0$$. For any $$\eta>0$$, there is some $$\varepsilon>0$$ with $$\omega_f(x,\varepsilon)<\eta$$. Since $$x\in B(x,\varepsilon)$$, for every $$y\in B(x,\varepsilon)$$ we have

$$
d(f(y),f(x))\le\sup_{u,v\in B(x,\varepsilon)}d(f(u),f(v))
=\omega_f(x,\varepsilon)<\eta.
$$

This is continuity at $$x$$.

### Exercise 18

For $$x,y\ge0$$, one has $$|\sqrt{x}-\sqrt{y}|^2\le|x-y|$$, so the square-root function is continuous on $$\mathbb R_+$$. If it were Lipschitz with constant $$L>0$$ on all of $$\mathbb R_+$$, then for every $$x>0$$,

$$
\sqrt{x}=|\sqrt{x}-\sqrt0|\le Lx,
$$

which would imply $$1/\sqrt{x}\le L$$, impossible as $$x\downarrow0$$. Thus it is not Lipschitz on $$\mathbb R_+$$.

For $$x,y\ge a>0$$, rationalizing gives

$$
|\sqrt{x}-\sqrt{y}|=\frac{|x-y|}{\sqrt{x}+\sqrt{y}}
\le\frac{|x-y|}{2\sqrt a}.
$$

Hence the restriction to $$[a,\infty)$$ is Lipschitz continuous.
