# Chapter VII — Multivariable Differential Calculus

Exercises follow the numbering in the textbook. Inner products are taken to be linear in the first argument. The notes below flag a few places where the printed complex-scalar or matrix conventions need clarification.

## Exercise 1

Let $$H$$ be a finite-dimensional Hilbert space.

**(a)** In the real case, the statement is the usual representation theorem for continuous bilinear forms. Over $$\mathbb C$$, the displayed formula $$a(x,y)=(Ax\mid y)$$ represents a continuous sesquilinear form (linear in $$x$$ and conjugate-linear in $$y$$). If $$\mathcal L^2(H,\mathbb K)$$ is read as the space of complex-bilinear maps defined in this section, the printed claim is not correct: the right-hand side is conjugate-linear in $$y$$. We prove the assertion for real bilinear forms and, over $$\mathbb C$$, for the intended sesquilinear forms.

For fixed $$x\in H$$, the map $$y\mapsto a(x,y)$$ is a continuous conjugate-linear functional. By the Riesz representation theorem, there is a unique vector, denoted $$Ax$$, such that

$$
a(x,y)=(Ax\mid y)\qquad(y\in H).
$$

This defines a map $$A:H\to H$$. If $$\alpha,\beta\in\mathbb K$$ and $$x_1,x_2\in H$$, then

$$
a(\alpha x_1+\beta x_2,y)
=\alpha a(x_1,y)+\beta a(x_2,y)
=(\alpha Ax_1+\beta Ax_2\mid y).
$$

By uniqueness in the Riesz representation, $$A(\alpha x_1+\beta x_2)=\alpha Ax_1+\beta Ax_2$$. Thus $$A$$ is linear. Moreover, using $$\|u\|=\sup_{\|y\|\leq1}|(u\mid y)|$$,

$$
\|Ax\|=\sup_{\|y\|\leq1}|a(x,y)|\leq\|a\|\,\|x\|,
$$

so $$A\in\mathcal L(H)$$. This representation is unique: if $$A_1$$ and $$A_2$$ both represent $$a$$, then $$((A_1-A_2)x\mid y)=0$$ for all $$y$$, hence $$(A_1-A_2)x=0$$ for every $$x$$.

Conversely, every $$A\in\mathcal L(H)$$ defines such a form by $$a_A(x,y):=(Ax\mid y)$$, and

$$
|a_A(x,y)|\leq\|A\|\,\|x\|\,\|y\|.
$$

The two norms agree:

$$
\|A\|=\sup_{\|x\|\leq1}\|Ax\|
=\sup_{\substack{\|x\|\leq1\\\|y\|\leq1}}|a(x,y)|=\|a\|.
$$

Therefore the representation map $$a\mapsto A$$ is an isometric isomorphism.

**(b)** Now assume $$H$$ is real. If $$a$$ is symmetric, then for all $$x,y\in H$$,

$$
(Ax\mid y)=a(x,y)=a(y,x)=(Ay\mid x)=(x\mid Ay)=(A^*x\mid y).
$$

Nondegeneracy of the inner product implies $$Ax=A^*x$$ for every $$x$$, so $$A=A^*$$. Conversely, if $$A=A^*$$, then

$$
a(y,x)=(Ay\mid x)=(y\mid A^*x)=(y\mid Ax)=(Ax\mid y)=a(x,y),
$$

where the last equality uses symmetry of the real inner product. Hence $$a$$ is symmetric exactly when $$A$$ is self-adjoint.

**(c)** Suppose $$H=\mathbb R^m$$ with its Euclidean inner product, and let $$A=[A_{jk}]$$ be the standard matrix of the induced operator, so $$(Ax)_j=\sum_k A_{jk}x_k$$. Then

$$
a(x,y)=(Ax\mid y)
=\sum_{j,k=1}^m A_{jk}x_k y_j
=\sum_{j,k=1}^m A_{kj}x_j y_k.
$$

Thus the coefficient matrix in an expansion $$a(x,y)=\sum_{j,k}c_{jk}x_jy_k$$ is $$[c_{jk}]=A^{\mathsf T}$$. Accordingly, the printed formula with coefficients $$a_{jk}$$ is correct if $$[a_{jk}]$$ denotes the transpose of the standard column-vector matrix of $$A$$; if $$[a_{jk}]$$ is the standard matrix of $$A$$, its indices in that sum must be reversed.

## Exercise 2

The symmetric forms form a closed subspace of $$\mathcal L_m(E,F)$$. Indeed, suppose $$\varphi_n\in\mathcal L^m_{\mathrm{sym}}(E,F)$$ and $$\varphi_n\to\varphi$$ in the multilinear operator norm. For every permutation $$\sigma\in S_m$$ and every $$x_1,\ldots,x_m\in E$$,

$$
\varphi(x_{\sigma(1)},\ldots,x_{\sigma(m)})
=\lim_{n\to\infty}\varphi_n(x_{\sigma(1)},\ldots,x_{\sigma(m)})
=\lim_{n\to\infty}\varphi_n(x_1,\ldots,x_m)
=\varphi(x_1,\ldots,x_m).
$$

So $$\varphi$$ is symmetric. Now fix $$x\in X$$ and $$h\in E$$. For sufficiently small real $$t$$, $$x+th\in X$$. Since $$f$$ takes values in the symmetric subspace, every difference quotient

$$
\frac{f(x+th)-f(x)}{t}
$$

is a symmetric $$m$$-linear map. Differentiability gives convergence in $$\mathcal L_m(E,F)$$ to $$\partial f(x)h$$ as $$t\to0$$. Closedness therefore implies $$\partial f(x)h\in\mathcal L^m_{\mathrm{sym}}(E,F)$$.

## Exercise 3

Set $$B(t):=e^{tA}$$ and write its columns as $$b_1(t),\ldots,b_n(t)$$. By Example 4.8(a),

$$
\frac{d}{dt}\det B(t)
=\sum_{j=1}^n\det[b_1(t),\ldots,b'_j(t),\ldots,b_n(t)].
$$

Since $$B'(t)=B(t)A$$, the $$j$$th derivative column is $$b'_j(t)=\sum_k A_{kj}b_k(t)$$. In the determinant with column $$j$$ replaced, every term with $$k\ne j$$ has two equal columns and vanishes. The term with $$k=j$$ is $$A_{jj}\det B(t)$$. Summing over $$j$$ yields

$$
\frac{d}{dt}\det(e^{tA})=\operatorname{tr}(A)\det(e^{tA}).
$$

Define $$q(t):=e^{-t\operatorname{tr}(A)}\det(e^{tA})$$. The product rule gives $$q'(t)=0$$, and $$q(0)=1$$. Hence $$q(t)=1$$ for all real $$t$$, and at $$t=1$$,

$$
\boxed{\det(e^A)=e^{\operatorname{tr}(A)}}.
$$

The hint as printed defines the difference $$\det(e^{tA})-e^{t\operatorname{tr}(A)}$$ and says its derivative is zero. The differential equation above shows that this difference instead has derivative $$\operatorname{tr}(A)$$ times itself. The normalized product $$q(t)$$ is the quantity with zero derivative.

## Exercise 4

Let $$\mathcal Y:=\mathcal L(\mathcal L(E,F),\mathcal L(F,E))$$. For fixed $$T_1,T_2\in\mathcal L(F,E)$$, the map $$S\mapsto T_1ST_2$$ is linear, and the operator norm inequality gives

$$
\|T_1ST_2\|\leq\|T_1\|\,\|S\|\,\|T_2\|.
$$

Thus $$g(T_1,T_2)\in\mathcal Y$$ and $$\|g(T_1,T_2)\|_{\mathcal Y}\leq\|T_1\|\,\|T_2\|$$. This proves **(a)**.

For **(b)**, the assignment $$g:(T_1,T_2)\mapsto g(T_1,T_2)$$ is bilinear: composition distributes over sums and scalars in each of its two operator arguments. The estimate just obtained gives

$$
\|g(T_1,T_2)\|_{\mathcal Y}\leq\|T_1\|\,\|T_2\|,
$$

so $$g$$ is bounded as a bilinear map from $$\mathcal L(F,E)\times\mathcal L(F,E)$$ into $$\mathcal Y$$. Consequently $$g\in\mathcal L^2(\mathcal L(F,E);\mathcal Y)$$.

## Exercise 5

Assume first that $$H$$ is real. Expanding at $$x$$ in an increment $$y$$ gives

$$
a(x+y)=(A(x+y)\mid x+y)
=(Ax\mid x)+(Ax\mid y)+(Ay\mid x)+(Ay\mid y).
$$

The proposed derivative is linear in $$y$$, and the remainder satisfies

$$
|a(x+y)-a(x)-(Ax\mid y)-(Ay\mid x)|
=|(Ay\mid y)|
\leq\|A\|\,\|y\|^2.
$$

After division by $$\|y\|$$, the bound tends to zero as $$y\to0$$. This proves

$$
\boxed{\partial a(x)y=(Ax\mid y)+(Ay\mid x).}
$$

For **(b)**, because the space is real, the adjoint identity and symmetry of the inner product give

$$
(Ay\mid x)=(A^*x\mid y).
$$

Therefore

$$
\partial a(x)y=((A+A^*)x\mid y)=((A+A^*)x\mid y)_{\mathbb R^n}.
$$

By the defining property of the Euclidean gradient, $$\partial a(x)y=(\nabla a(x)\mid y)$$ for every $$y$$, so

$$
\boxed{\nabla a(x)=(A+A^*)x.}
$$

If $$H$$ is complex, the displayed formula in (a) is the real Fréchet derivative on the underlying real Hilbert space. It is generally not complex-linear in $$y$$, so it is not a complex Fréchet derivative under a convention requiring the derivative to be complex-linear; for example, $$a(z)=|z|^2$$ is not complex differentiable at nonzero $$z$$.
