# Chapter I — Foundations

## 12. Vector Spaces, Affine Spaces and Algebras

### Exercise 1

**(a)** Regard the field $$K$$ as a vector space over itself. A subspace $$U$$ is either $$\{0\}$$ or contains some $$u\ne0$$. In the latter case, every $$x\in K$$ has the form $$x=(x/u)u$$, so $$x\in U$$. Thus the only subspaces are $$\{0\}$$ and $$K$$.

**(b)** Every complex number has a unique representation $$a+bi$$ with $$a,b\in\mathbb R$$. Hence $$\{1,i\}$$ is a basis of $$\mathbb C$$ over $$\mathbb R$$, and $$\dim_{\mathbb R}\mathbb C=2$$.

### Exercise 2

**(a)** For each $$k$$, the projection

$$
\operatorname{pr}_k:E_1\times\cdots\times E_m\to E_k,
\qquad (x_1,\ldots,x_m)\mapsto x_k,
$$

is linear, since vector operations in the product are defined coordinatewise. Its kernel and image are

$$
\ker(\operatorname{pr}_k)=\{(x_1,\ldots,x_m):x_k=0\},
\qquad \operatorname{im}(\operatorname{pr}_k)=E_k.
$$

The canonical injection

$$
\iota_k:E_k\to E_1\times\cdots\times E_m,
\qquad x\mapsto(0,\ldots,0,x,0,\ldots,0),
$$

is also linear. It has kernel $$\{0\}$$ and image

$$
\operatorname{im}(\iota_k)=\{(x_1,\ldots,x_m):x_j=0\text{ for }j\ne k\}.
$$

**(b)** The map $$\iota_k:E_k\to\operatorname{im}(\iota_k)$$ is a linear bijection. Its inverse is the restriction of $$\operatorname{pr}_k$$ to $$\operatorname{im}(\iota_k)$$. Therefore $$E_k\cong\operatorname{im}(\iota_k)$$.

### Exercise 3

For $$T(x,y)=(x-y,y-x)$$, vectors $$(x,y),(u,v)\in\mathbb R^2$$, and scalars $$a,b\in\mathbb R$$,

$$
\begin{aligned}
T(a(x,y)+b(u,v))
&=T(ax+bu,ay+bv)\\
&=(ax+bu-ay-bv,ay+bv-ax-bu)\\
&=a(x-y,y-x)+b(u-v,v-u)\\
&=aT(x,y)+bT(u,v).
\end{aligned}
$$

Thus $$T$$ is linear. Next,

$$
T(x,y)=0\iff x=y,
$$

Every value is of the form $$(t,-t)$$, and every such pair is attained because $$T(t,0)=(t,-t)$$. Consequently,

$$
\ker(T)=\{(t,t):t\in\mathbb R\}=\operatorname{span}\{(1,1)\},
\qquad
\operatorname{im}(T)=\{(t,-t):t\in\mathbb R\}=\operatorname{span}\{(1,-1)\}.
$$

### Exercise 4

Commutativity of the diagram means $$Q\circ T=S\circ P$$. Let $$u,v\in E_1$$. Since $$P$$ is surjective, choose $$x,y\in E$$ with $$P(x)=u$$ and $$P(y)=v$$. Then

$$
S(u+v)=S(P(x+y))=Q(T(x+y))=Q(Tx)+Q(Ty)=S(u)+S(v).
$$

For $$\lambda\in K$$,

$$
S(\lambda u)=S(P(\lambda x))=Q(T(\lambda x))=\lambda Q(Tx)=\lambda S(u).
$$

Thus $$S$$ is linear.

### Exercise 5

For $$f,g\in E^X$$ and $$\lambda,\mu\in K$$, the operations in $$E^X$$ are pointwise, so

$$
\delta_{x_0}(\lambda f+\mu g)
=(\lambda f+\mu g)(x_0)
=\lambda f(x_0)+\mu g(x_0)
=\lambda\delta_{x_0}(f)+\mu\delta_{x_0}(g).
$$

Therefore $$\delta_{x_0}$$ is linear.

### Exercise 6

The statement as printed says $$\dim(E\times F)=\dim(E)\dim(F)$$, which is false in general: for $$E=F=K$$, the product has dimension $$2$$, while the displayed right-hand side is $$1$$.

The correct formula is

$$
\dim(E\times F)=\dim(E)+\dim(F).
$$

Indeed, let $$e_1,\ldots,e_n$$ be a basis of $$E$$ and $$f_1,\ldots,f_r$$ a basis of $$F$$. Then

$$
(e_1,0),\ldots,(e_n,0),(0,f_1),\ldots,(0,f_r)
$$

is a basis of $$E\times F$$: each $$(x,y)$$ has a unique expansion using the two given bases, and a linear combination of these pairs can vanish only when all its coordinates in both bases vanish. Hence the product space has dimension $$n+r$$.

### Exercise 7

Define

$$
\widetilde T:E/\ker(T)\to\operatorname{im}(T),
\qquad v+\ker(T)\mapsto T(v).
$$

If $$v+\ker(T)=w+\ker(T)$$, then $$v-w\in\ker(T)$$, so $$T(v)=T(w)$$; thus $$\widetilde T$$ is well defined. It is linear, is surjective by the definition of $$\operatorname{im}(T)$$, and is injective because $$\widetilde T(v+\ker(T))=0$$ implies $$v\in\ker(T)$$. Therefore $$E/\ker(T)\cong\operatorname{im}(T)$$.

### Exercise 8

The Lagrange interpolation formula states that every polynomial $$p\in K_m[X]$$ satisfies

$$
p(X)=\sum_{j=0}^m p(x_j)\ell_j(X).
$$

Taking $$p(X)=1=X^0$$ gives

$$
\sum_{j=0}^m\ell_j(X)=1.
$$

Taking $$p(X)=(X-y)^k$$, whose degree is at most $$m$$ for $$1\le k\le m$$, gives

$$
(X-y)^k=\sum_{j=0}^m(x_j-y)^k\ell_j(X).
$$

### Exercise 9

The space $$K_m[X]$$ has dimension $$m+1$$. If $$\sum_{j=0}^m c_j\ell_j=0$$, evaluating at $$x_i$$ gives $$c_i=0$$, since $$\ell_j(x_i)=1$$ for $$j=i$$ and $$0$$ otherwise. Thus the Lagrange polynomials are linearly independent and form a basis.

The Newton polynomials are $$\omega_j(X)=\prod_{k=0}^{j-1}(X-x_k)$$, with $$\omega_0=1$$. Each $$\omega_j$$ is monic of degree $$j$$. In a nonzero linear combination, the term with largest index having nonzero coefficient has a degree that no lower-index term can cancel. Hence the Newton polynomials are linearly independent as well, and they form a basis of $$K_m[X]$$.

### Exercise 10

For each $$n\le m$$, let $$p_n$$ be the interpolation polynomial of degree at most $$n$$ taking the values $$f(x_j)$$ at $$x_0,\ldots,x_n$$. Its Lagrange form is

$$
p_n(X)=\sum_{j=0}^n f(x_j)
\prod_{\substack{0\le k\le n\\k\ne j}}
\frac{X-x_k}{x_j-x_k}.
$$

The coefficient of $$X^n$$ in this expression is

$$
\sum_{j=0}^n\frac{f(x_j)}
{\displaystyle\prod_{\substack{0\le k\le n\\k\ne j}}(x_j-x_k)}.
$$

In the Newton expansion of $$p_n$$, the only term of degree $$n$$ is $$a_n\prod_{k=0}^{n-1}(X-x_k)$$, whose leading coefficient is $$a_n$$. This proves part (a).

**(b)** In the formula from part (a), permuting $$x_0,\ldots,x_n$$ simply reorders the summands and the factors in each denominator. Thus $$f[x_0,\ldots,x_n]$$ is symmetric in its arguments.

**(c)** Write
$$
D_j:=\prod_{\substack{0\le k\le n\\k\ne j}}(x_j-x_k).
$$
For $$j=0$$, the coefficient of $$f(x_0)$$ in the numerator on the right is $$1/\prod_{k=1}^{n-1}(x_0-x_k)$$; after division by $$x_0-x_n$$ it is $$1/D_0$$. For $$j=n$$, that coefficient is $$-1/\prod_{k=1}^{n-1}(x_n-x_k)$$; after division by $$x_0-x_n$$ it is $$1/D_n$$. For $$1\le j<n$$, put $$Q_j=\prod_{1\le k<n,\ k\ne j}(x_j-x_k)$$. The coefficient before division is
$$
\frac{1}{(x_j-x_0)Q_j}-\frac{1}{(x_j-x_n)Q_j}
=\frac{x_0-x_n}{D_j}.
$$
Thus, in every case, dividing by $$x_0-x_n$$ gives the coefficient $$1/D_j$$ appearing in part (a), proving the recurrence.

$$
f[x_0,\ldots,x_n]
=\frac{f[x_0,\ldots,x_{n-1}]-f[x_1,\ldots,x_n]}
{x_0-x_n}.
$$

### Exercise 11

Write $$S=I+\Delta$$ for the shift operator, so that $$(Sf)_n=f_{n+1}$$ and $$I=S-\Delta$$. The operators $$S$$ and $$\Delta$$ commute, so the binomial formula gives

$$
I^k=((I+\Delta)-\Delta)^k
=\sum_{j=0}^k(-1)^j\binom{k}{j}S^{k-j}\Delta^j.
$$

Applying both sides to $$f$$ and evaluating at $$n$$ gives

$$
f_n=\sum_{j=0}^k(-1)^j\binom{k}{j}\Delta^j f_{n+k-j}.
$$

### Exercise 12

The map $$\Delta_h$$ is linear. For a monomial of degree $$d\ge1$$,

$$
\Delta_h X^d=\frac{(X+h)^d-X^d}{h}
=dX^{d-1}+\text{terms of lower degree}.
$$

Thus $$\Delta_h$$ maps $$K_m[X]$$ into $$K_{m-1}[X]$$ and, by iteration, $$\Delta_h^k$$ maps $$K_m[X]$$ into $$K_{m-k}[X]$$; if $$m-k<0$$, the result is zero. Hence $$\Delta_h^k\in\operatorname{Hom}(K_m[X],K_{m-k}[X])$$.

For $$0\le k\le m$$, the coefficient of $$X^{m-k}$$ in $$\Delta_h^k X^m$$ is

$$
m(m-1)\cdots(m-k+1)=\frac{m!}{(m-k)!},
$$

with the value $$1$$ when $$k=0$$. This is the leading coefficient when it is nonzero in $$K$$. In positive characteristic it may vanish, in which case the actual degree is lower. For $$k>m$$, $$\Delta_h^kX^m=0$$.

### Exercise 13

Let $$F(n)=n(n+1)(2n+1)(3n^2+3n-1)/30$$. We prove by induction that $$\sum_{j=0}^n j^4=F(n)$$. The case $$n=0$$ holds. Assuming the formula for $$n$$, first expand the difference:

$$
\begin{aligned}
F(n+1)-F(n)
&=\frac{n+1}{30}\Bigl((n+2)(2n+3)(3n^2+9n+5)\\
&\qquad -n(2n+1)(3n^2+3n-1)\Bigr)\\
&=\frac{n+1}{30}\Bigl((6n^4+39n^3+91n^2+89n+30)\\
&\qquad -(6n^4+9n^3+n^2-n)\Bigr)\\
&=\frac{n+1}{30}\,30(n+1)^3=(n+1)^4.
\end{aligned}
$$

Therefore $$F(n+1)=F(n)+(n+1)^4$$, exactly the addition of the next term in the sum, completing the induction.


### Exercise 14

The set $$\mathbb Q(\sqrt2)=\{a+b\sqrt2:a,b\in\mathbb Q\}$$ contains zero and is closed under addition and multiplication by rational scalars, so it is a vector space over $$\mathbb Q$$. The vectors $$1$$ and $$\sqrt2$$ span it. They are linearly independent because $$\sqrt2\notin\mathbb Q$$. Therefore its dimension is $$2$$.

### Exercise 15

Suppose $$a,b\in\mathbb Q(\sqrt2)$$ and $$a+b\sqrt3=0$$. If $$b\ne0$$, then $$\sqrt3=-a/b\in\mathbb Q(\sqrt2)$$, contrary to Exercise 10.2. Thus $$b=0$$, and then $$a=0$$. Hence $$1$$ and $$\sqrt3$$ are linearly independent over $$\mathbb Q(\sqrt2)$$.

### Exercise 16

The evaluation map $$e$$ is linear. If $$e(p)=0$$, then the polynomial $$p\in K_m[X]$$ has the $$m+1$$ distinct roots $$x_0,\ldots,x_m$$. Since its degree is at most $$m$$, it must be the zero polynomial, so $$e$$ is injective.

Given $$(y_0,\ldots,y_m)\in K^{m+1}$$, the polynomial

$$
p(X)=\sum_{j=0}^m y_j\ell_j(X)
$$

satisfies $$p(x_i)=y_i$$ for every $$i$$. Thus $$e$$ is surjective, and its inverse is

$$
e^{-1}(y_0,\ldots,y_m)=\sum_{j=0}^m y_j\ell_j(X).
$$

### Exercise 17

Let $$m=T(1)\in E$$. For every $$x\in K$$, linearity gives

$$
T(x)=T(x\cdot1)=xT(1)=xm.
$$

If another element $$m'\in E$$ satisfies $$T(x)=xm'$$ for all $$x$$, then setting $$x=1$$ gives $$m'=T(1)=m$$. This proves existence and uniqueness.
