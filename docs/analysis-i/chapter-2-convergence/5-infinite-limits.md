# Chapter II — Convergence

## 5. Infinite Limits

Write $$x_*:=\liminf_{n\to\infty}x_n$$ and $$x^*:=\limsup_{n\to\infty}x_n$$, with values in $$\overline{\mathbb R}$$.

### Exercise 1

Let

$$
a_n:=\sup_{k\ge n}x_k,
\qquad
b_n:=\inf_{k\ge n}x_k.
$$

Then $$a_n\downarrow x^*$$ and $$b_n\uparrow x_*$$. If both limits are real, then for each $$\varepsilon>0$$, eventually

$$
b_n>x_*-\varepsilon
\qquad\text{and}\qquad
a_n<x^*+\varepsilon.
$$

Every $$x_n$$ lies between the corresponding tail infimum and supremum, so $$x_*-\varepsilon<x_n<x^*+\varepsilon$$ eventually.

If $$x_*=-\infty$$, the lower bound must be replaced by the statement that for every $$K>0$$, infinitely many terms satisfy $$x_n<-K$$. If also $$x^*=-\infty$$, this strengthens to $$x_n<-K$$ eventually for every $$K>0$$. Whenever $$x^*$$ is finite, the eventual upper bound $$x_n<x^*+\varepsilon$$ remains valid. Dually, if $$x^*=+\infty$$, then for every $$K>0$$, infinitely many terms satisfy $$x_n>K$$; if also $$x_*=+\infty$$, this holds eventually. Whenever $$x_*$$ is finite, the eventual lower bound $$x_n>x_*-\varepsilon$$ remains valid. If $$x_*=-\infty$$ and $$x^*=+\infty$$, both kinds of extreme terms occur in every tail.

### Exercise 2

**(a)** Negation reverses order, so tail infima of $$(-x_n)$$ are the negatives of the tail suprema of $$(x_n)$$. Hence

$$
\liminf_{n\to\infty}(-x_n)=-x^*.
$$

Similarly, $$\limsup_{n\to\infty}(-x_n)=-x_*$$.

**(b)** For each $$n$$, the tail supremum and infimum satisfy

$$
\sup_{k\ge n}(x_k+y_k)
\le \sup_{k\ge n}x_k+\sup_{k\ge n}y_k,
$$

$$
\inf_{k\ge n}(x_k+y_k)
\ge \inf_{k\ge n}x_k+\inf_{k\ge n}y_k.
$$

Taking limits as $$n\to\infty$$ gives

$$
\limsup_{n\to\infty}(x_n+y_n)\le x^*+y^*,
\qquad
\liminf_{n\to\infty}(x_n+y_n)\ge x_*+y_*.
$$

The stated exclusions ensure that the extended-real sums on the right are defined.

**(c)** There is an omission in the printed hypotheses: they do not rule out the undefined products $$0\cdot\infty$$ in $$x_*y^*$$ or $$x^*y^*$$. For example, $$x_{2k}=1/(k+1)$$, $$x_{2k+1}=1$$, $$y_{2k}=1$$, and $$y_{2k+1}=2k+1$$ satisfy the printed conditions but give $$x_*=0$$ and $$y^*=+\infty$$. Likewise, $$x_{2k}=2k+1$$, $$x_{2k+1}=1$$, and $$y_n=1/(n+1)$$ satisfy them with $$x^*=+\infty$$ and $$y^*=0$$. The displayed chain is meaningful if these two additional cases are excluded. Under that necessary qualification, nonnegativity and the tail definitions give

$$
x_*y_*
\le \liminf_{n\to\infty}(x_ny_n)
\le x_*y^*
\le \limsup_{n\to\infty}(x_ny_n)
\le x^*y^*.
$$

Indeed, on every sufficiently late tail, $$x_n$$ and $$y_n$$ are bounded below by their tail infima and above by their tail suprema. Multiplying these nonnegative bounds gives the first and last inequalities after taking limits. For the two middle bounds, choose a subsequence along which $$x_n\to x_*$$ for the first, and a subsequence along which $$y_n\to y^*$$ for the second. On the first subsequence, $$y_n$$ is eventually at most any fixed number greater than $$y^*$$; on the second, $$x_n$$ is eventually at least any fixed number less than $$x_*$$. Taking the corresponding limits yields the claimed bounds. If a relevant endpoint is infinite, the same argument uses an arbitrary finite threshold in place of that endpoint.

**(d)** Since $$y_n\to y$$, addition of $$y_n$$ shifts both tail limits by $$y$$:

$$
\limsup_{n\to\infty}(x_n+y_n)=x^*+y,
\qquad
\liminf_{n\to\infty}(x_n+y_n)=x_*+y.
$$

If $$y>0$$, then $$y_n>0$$ eventually and multiplication preserves order, giving

$$
\limsup_{n\to\infty}(x_ny_n)=yx^*,
\qquad
\liminf_{n\to\infty}(x_ny_n)=yx_*.
$$

If $$y<0$$, multiplication reverses order, so

$$
\limsup_{n\to\infty}(x_ny_n)=yx_*,
\qquad
\liminf_{n\to\infty}(x_ny_n)=yx^*.
$$

**(e)** For every $$n$$,

$$
\sup_{k\ge n}x_k\le\sup_{k\ge n}y_k,
\qquad
\inf_{k\ge n}x_k\le\inf_{k\ge n}y_k,
$$

because $$x_k\le y_k$$ for every $$k$$. Passing to the limits of these tail suprema and infima proves

$$
\limsup_{n\to\infty}x_n\le\limsup_{n\to\infty}y_n,
\qquad
\liminf_{n\to\infty}x_n\le\liminf_{n\to\infty}y_n.
$$

### Exercise 3

For even $$n$$, $$x_n=2^{n+1}+1$$, while for odd $$n$$, $$x_n=1$$. Therefore

$$
\liminf_{n\to\infty}x_n=1,
\qquad
\limsup_{n\to\infty}x_n=+\infty.
$$

For even $$n$$, $$x_{n+1}/x_n=1/(2^{n+1}+1)\to0$$. For odd $$n$$, $$x_{n+1}/x_n=2^{n+2}+1\to+\infty$$. Thus

$$
\liminf_{n\to\infty}\frac{x_{n+1}}{x_n}=0,
\qquad
\limsup_{n\to\infty}\frac{x_{n+1}}{x_n}=+\infty.
$$

Finally, for even $$n$$,

$$
x_n^{1/n}=(2^{n+1}+1)^{1/n}\longrightarrow2,
$$

and for odd $$n$$, $$x_n^{1/n}=1$$. Hence

$$
\liminf_{n\to\infty}x_n^{1/n}=1,
\qquad
\limsup_{n\to\infty}x_n^{1/n}=2.
$$

### Exercise 4

Put $$r_n:=x_{n+1}/x_n>0$$ and $$a:=\liminf r_n$$. If $$a>0$$, choose any $$q$$ with $$0<q<a$$. Eventually $$r_k\ge q$$, so for all sufficiently large $$n$$,

$$
x_n=x_N\prod_{k=N}^{n-1}r_k\ge x_Nq^{n-N}.
$$

Taking $$n$$th roots and then the lower limit gives $$\liminf x_n^{1/n}\ge q$$. Letting $$q\uparrow a$$ proves

$$
\liminf r_n\le\liminf x_n^{1/n}.
$$

If $$a=0$$, this inequality follows from $$x_n^{1/n}>0$$.

Now put $$b:=\limsup r_n$$. If $$b<\infty$$, take any $$q>b$$ with $$q>0$$. Eventually $$r_k\le q$$, and the same product estimate, with the inequality reversed, gives $$\limsup x_n^{1/n}\le q$$. Letting $$q\downarrow b$$ proves $$\limsup x_n^{1/n}\le b$$. If $$b=+\infty$$, this bound is immediate. Since every sequence has lower limit at most its upper limit, the full chain follows:

$$
\liminf_{n\to\infty}\frac{x_{n+1}}{x_n}
\le \liminf_{n\to\infty}x_n^{1/n}
\le \limsup_{n\to\infty}x_n^{1/n}
\le \limsup_{n\to\infty}\frac{x_{n+1}}{x_n}.
$$

### Exercise 5

For $$s<t\le0$$,

$$
\varphi(t)-\varphi(s)=\frac{t-s}{(1-t)(1-s)}>0,
$$

and for $$0\le s<t$$,

$$
\varphi(t)-\varphi(s)=\frac{t-s}{(1+t)(1+s)}>0.
$$

The negative and positive branches have values in $$[-1,0]$$ and $$[0,1]$$, respectively, so the whole map is strictly increasing. Its endpoint values are $$\varphi(-\infty)=-1$$ and $$\varphi(+\infty)=1$$, and every value between them is attained. More explicitly, for $$u\in(-1,1)$$,

$$
\varphi^{-1}(u)=\frac{u}{1-|u|},
$$

while $$\varphi^{-1}(-1)=-\infty$$ and $$\varphi^{-1}(1)=+\infty$$. Thus $$\varphi$$ is a strictly increasing bijection.

For $$x,y\in\overline{\mathbb R}$$, define $$d(x,y):=|\varphi(x)-\varphi(y)|$$. Nonnegativity and symmetry follow from the absolute value. Since $$\varphi$$ is injective, $$d(x,y)=0$$ exactly when $$x=y$$. Finally,

$$
d(x,z)=|\varphi(x)-\varphi(z)|
\le |\varphi(x)-\varphi(y)|+|\varphi(y)-\varphi(z)|
=d(x,y)+d(y,z).
$$

Therefore $$d$$ is a metric on $$\overline{\mathbb R}$$.

### Exercise 6

Both sequences have period $$4$$. Their termwise sum has period $$4$$ as well:

$$
(x_n+y_n)=(2,2,3,1,2,2,3,1,\ldots).
$$

Consequently,

$$
\limsup x_n+\limsup y_n=2+2=4,
\qquad
\limsup(x_n+y_n)=3,
$$

$$
\liminf x_n+\liminf y_n=0+0=0,
\qquad
\liminf(x_n+y_n)=1,
$$

and

$$
\liminf x_n+\limsup y_n=0+2=2.
$$
