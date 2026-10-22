# Chapter II — Convergence

## 3. Normed Vector Spaces

### Exercise 1

Let $$T\in\operatorname{Aut}(E)$$ and define $$\|x\|_T:=\|Tx\|$$. Since $$T$$ is injective, $$\|x\|_T=0$$ exactly when $$Tx=0$$, that is, exactly when $$x=0$$. For $$\lambda\in\mathbb K$$,

$$
\|\lambda x\|_T=\|T(\lambda x)\|=\|\lambda Tx\|=|\lambda|\,\|Tx\|=|\lambda|\,\|x\|_T.
$$

Also,

$$
\|x+y\|_T=\|Tx+Ty\|\le\|Tx\|+\|Ty\|=\|x\|_T+\|y\|_T.
$$

Thus $$\|\cdot\|_T$$ is a norm. If $$\alpha\in\mathbb K^\times$$, then $$x\mapsto\alpha x$$ is an automorphism, so this result applies; explicitly, $$\|\alpha x\|=|\alpha|\,\|x\|$$ is a norm.

### Exercise 2

The reverse triangle inequality gives

$$
\bigl|\|x_n\|-\|x\|\bigr|\le\|x_n-x\|\longrightarrow0.
$$

Therefore $$\|x_n\|\to\|x\|$$ in $$[0,\infty)$$.

### Exercise 3

Let $$X$$ be the nonempty set from the section and let $$u:X\to E$$. The boundedness of $$u$$ means that its image $$u(X)$$ is bounded in the metric induced by the norm. If there is an $$r>0$$ such that $$\|u(x)\|\le r$$ for every $$x\in X$$, then

$$
\|u(x)-u(y)\|\le\|u(x)\|+\|u(y)\|\le2r
$$

for all $$x,y\in X$$, so $$u(X)$$ is bounded. Conversely, if $$u(X)$$ is bounded, it lies in a ball with some center $$z\in E$$ and finite radius $$r$$. Then

$$
\|u(x)\|\le\|u(x)-z\|+\|z\|\le r+\|z\|,
$$

so the image is bounded in norm. Finally, $$\|u\|_\infty:=\sup_{x\in X}\|u(x)\|$$ is finite exactly when the values $$\|u(x)\|$$ have a uniform finite bound. This proves the equivalence of (i)–(iv).

### Exercise 4

In an inner product space, expansion gives

$$
\|x+y\|^2=\|x\|^2+2\operatorname{Re}(x|y)+\|y\|^2,
\qquad
\|x-y\|^2=\|x\|^2-2\operatorname{Re}(x|y)+\|y\|^2.
$$

Adding these identities proves

$$
2\bigl(\|x\|^2+\|y\|^2\bigr)=\|x+y\|^2+\|x-y\|^2.
$$

### Exercise 5

For the form to be Hermitian, each weight must be real: testing on the standard basis vectors $$e_k$$ shows that $$\lambda_k=\overline{\lambda_k}$$. Positivity requires $$\lambda_k>0$$, since

$$
(e_k|e_k)_\lambda=\lambda_k.
$$

Conversely, if every $$\lambda_k$$ is a positive real number, then the form is sesquilinear and Hermitian, and

$$
(x|x)_\lambda=\sum_{k=1}^m\lambda_k|x_k|^2\ge0,
$$

with equality exactly when $$x=0$$. Hence it is a scalar product precisely when $$\lambda_k\in(0,\infty)$$ for every $$k$$.

### Exercise 6

Set $$a=\|x\|>0$$, $$b=\|y\|>0$$, and $$c=(x|y)/(ab)$$. The Cauchy–Schwarz inequality gives $$-1\le c\le1$$. The triangle inequality proves the upper bound. If $$c\le0$$, then the lower bound is immediate because its left side is nonpositive. If $$0<c\le1$$, then

$$
\begin{aligned}
\|x+y\|^2-c^2(a+b)^2
&=a^2+b^2+2abc-c^2(a+b)^2\\
&=(1-c)\bigl((a^2+b^2)(1+c)+2abc\bigr)\ge0.
\end{aligned}
$$

Taking square roots proves the lower bound. Equality in either bound holds exactly when $$c=1$$, which by the equality case of Cauchy–Schwarz means that $$y=t x$$ for some real $$t>0$$.

### Exercise 7

The set $$c_0$$ of scalar sequences converging to zero is a subspace of $$\ell^\infty$$: sums and scalar multiples of null sequences are null. To prove it is closed, let $$x^{(n)}\in c_0$$ and suppose $$x^{(n)}\to x$$ in the supremum norm. Given $$\varepsilon>0$$, choose $$n$$ such that $$\|x^{(n)}-x\|_\infty<\varepsilon/2$$. Since $$x^{(n)}\in c_0$$, there is an index $$N$$ such that $$|x_k^{(n)}|<\varepsilon/2$$ for every $$k\ge N$$. Therefore, for all $$k\ge N$$,

$$
|x_k|\le|x_k-x_k^{(n)}|+|x_k^{(n)}|<\varepsilon.
$$

Thus $$x_k\to0$$, so $$x\in c_0$$. Hence $$c_0$$ is closed in $$\ell^\infty$$.

### Exercise 8

Since the norms are equivalent, there is a constant $$K\ge1$$ such that

$$
K^{-1}\|x\|_1\le\|x\|_2\le K\|x\|_1
$$

for every $$x\in E$$. Applying this to $$x-y$$ gives

$$
K^{-1}d_1(x,y)\le d_2(x,y)\le Kd_1(x,y).
$$

In particular, for every $$r>0$$,

$$
B_{d_1}(x,r/K)\subseteq B_{d_2}(x,r)\subseteq B_{d_1}(x,Kr).
$$

Thus the two metrics induce the same topology and are equivalent.

### Exercise 9

Define

$$
d_2(x,y):=\left(\sum_{j=1}^n d_j(x_j,y_j)^2\right)^{1/2},
\qquad
d_\infty(x,y):=\max_{1\le j\le n}d_j(x_j,y_j).
$$

Nonnegativity, symmetry, and separation for $$d_2$$ follow from the corresponding properties of the component metrics. For the triangle inequality, apply the component inequalities and Minkowski's inequality in $$\mathbb R^n$$:

$$
\begin{aligned}
d_2(x,z)
&\le\left(\sum_{j=1}^n\bigl(d_j(x_j,y_j)+d_j(y_j,z_j)\bigr)^2\right)^{1/2}\\
&\le d_2(x,y)+d_2(y,z).
\end{aligned}
$$

For every $$x,y\in X$$,

$$
d_\infty(x,y)\le d_2(x,y)\le\sqrt n\,d_\infty(x,y).
$$

These inequalities show that $$d_2$$ and the product metric $$d_\infty$$ are equivalent.

### Exercise 10

**(a)** Suppose $$\sum_{j=0}^m\alpha_jx_j=0$$. Taking the inner product with $$x_i$$ and using orthogonality gives

$$
0=\left(\sum_{j=0}^m\alpha_jx_j\middle|x_i\right)=\alpha_i\|x_i\|^2.
$$

Since $$x_i\ne0$$, we have $$\alpha_i=0$$. This holds for each $$i$$, so the system is linearly independent.

**(b)** Expanding the squared norm and using orthogonality eliminates all cross terms:

$$
\left\|\sum_{k=0}^m x_k\right\|^2
=\sum_{k=0}^m\|x_k\|^2
+2\operatorname{Re}\sum_{0\le j<k\le m}(x_j|x_k)
=\sum_{k=0}^m\|x_k\|^2.
$$

This is Pythagoras' theorem.

### Exercise 11

If $$x,y\in F^\perp$$ and $$\alpha,\beta\in\mathbb K$$, then for every $$z\in F$$,

$$
(\alpha x+\beta y|z)=\alpha(x|z)+\beta(y|z)=0,
$$

so $$F^\perp$$ is a subspace. Now let $$x_n\in F^\perp$$ and $$x_n\to x$$ in $$E$$. For every $$z\in F$$, Cauchy–Schwarz gives

$$
|(x-x_n|z)|\le\|x-x_n\|\,\|z\|\longrightarrow0.
$$

Since $$(x_n|z)=0$$, it follows that $$(x|z)=0$$. Thus $$x\in F^\perp$$, proving that $$F^\perp$$ is closed.

### Exercise 12

Write $$p(x):=p_F(x)=\sum_{k=0}^m(x|u_k)u_k$$.

**(a)** For each $$j$$, orthonormality gives

$$
(x-p(x)|u_j)=(x|u_j)-\sum_{k=0}^m(x|u_k)(u_k|u_j)=0.
$$

Since the $$u_j$$ span $$F$$, this proves $$x-p(x)\in F^\perp$$.

**(b)** For any $$y\in F$$, the vectors $$x-p(x)\in F^\perp$$ and $$p(x)-y\in F$$ are orthogonal. Exercise 10 therefore gives

$$
\|x-y\|^2=\|x-p(x)\|^2+\|p(x)-y\|^2\ge\|x-p(x)\|^2.
$$

Equality holds at $$y=p(x)$$, so $$\|x-p(x)\|=\inf_{y\in F}\|x-y\|$$.

**(c)** Since $$x=p(x)+(x-p(x))$$ is an orthogonal decomposition,

$$
\|x-p(x)\|^2=\|x\|^2-\|p(x)\|^2
=\|x\|^2-\sum_{k=0}^m|(x|u_k)|^2.
$$

**(d)** Sesquilinearity in the first variable shows that $$p$$ is linear. As $$p(x)\in F$$ and $$p$$ is the identity on each $$u_k$$, it is the identity on $$F$$. Consequently $$p^2=p$$.

**(e)** We have $$\operatorname{im}(p)\subseteq F$$, and $$p$$ is the identity on $$F$$, so $$\operatorname{im}(p)=F$$. Also, $$p(x)=0$$ exactly when every coefficient $$(x|u_k)$$ vanishes, which is equivalent to $$x\in F^\perp$$. Thus $$\ker(p)=F^\perp$$. Finally, every $$x\in E$$ has the decomposition $$x=p(x)+(x-p(x))\in F+F^\perp$$. Since $$F\cap F^\perp=\{0\}$$, this sum is direct:

$$
E=F\oplus F^\perp.
$$

### Exercise 13

**(a)** By Exercise 12(c),

$$
\sum_{k=0}^m|(x|u_k)|^2=\|x\|^2-\|x-p_F(x)\|^2\le\|x\|^2.
$$

**(b)** If $$x\in F$$, then Exercise 12(d) gives $$p_F(x)=x$$. Substituting into the definition of $$p_F$$ gives

$$
x=\sum_{k=0}^m(x|u_k)u_k.
$$

The vectors in this sum are pairwise orthogonal, so Exercise 10 yields

$$
\|x\|^2=\sum_{k=0}^m|(x|u_k)|^2.
$$

### Exercise 14

For $$A=[a_{jk}]$$, set

$$
S(A):=\sum_{j=1}^m\sum_{k=1}^n|a_{jk}|,\quad
R(A):=\max_{1\le j\le m}\sum_{k=1}^n|a_{jk}|,\quad
C(A):=\max_{1\le k\le n}\sum_{j=1}^m|a_{jk}|,\quad
M(A):=\max_{j,k}|a_{jk}|.
$$

**(a)** Identify $$A$$ with the vector of its $$mn$$ entries. The form

$$
(A|B):=\sum_{j=1}^m\sum_{k=1}^n a_{jk}\overline{b_{jk}}
$$

is the Euclidean inner product on this vector space. Its induced norm is exactly

$$
|A|=\left(\sum_{j=1}^m\sum_{k=1}^n|a_{jk}|^2\right)^{1/2},
$$

so $$|\cdot|$$ is a norm.

**(b)** The four functions in the question are $$S$$, $$R$$, $$C$$, and $$M$$, respectively. Each is nonnegative, absolutely homogeneous, and vanishes only at the zero matrix. The triangle inequality for $$S$$ and $$M$$ follows entrywise; for $$R$$ and $$C$$, apply the triangle inequality to each row or column sum and then take the maximum. Thus all four are norms. For every matrix,

$$
M(A)\le R(A)\le nM(A),\qquad
M(A)\le C(A)\le mM(A),\qquad
M(A)\le S(A)\le mnM(A).
$$

Therefore each of the four norms is bounded above and below by positive constant multiples of $$M$$, so they are equivalent.

### Exercise 15

Let $$T\in B(E,F)\cap\operatorname{Hom}(E,F)$$. If there were some $$x\in E$$ with $$Tx\ne0$$, linearity and homogeneity would give

$$
\|T(nx)\|=\|nTx\|=n\|Tx\|\longrightarrow\infty
$$

as $$n\to\infty$$ through the positive integers. This contradicts boundedness of the image of $$T$$. Hence $$Tx=0$$ for every $$x\in E$$, and $$T=0$$. The zero map belongs to the intersection, so

$$
B(E,F)\cap\operatorname{Hom}(E,F)=\{0\}.
$$
