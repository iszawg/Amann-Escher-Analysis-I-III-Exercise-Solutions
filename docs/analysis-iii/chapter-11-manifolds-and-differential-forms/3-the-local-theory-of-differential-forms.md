# Chapter XI — Manifolds and Differential Forms

## 3. The local theory of differential forms

These solutions address Exercises 1–13. Forms and coefficients are smooth unless otherwise stated. In Exercise 5 the printed criterion is pointwise, but it does not ensure a global factorization by smooth 1-forms. Exercise 12(vi), as printed, equates a vector field with a scalar; the corresponding commutator identity is proved below.

### Exercise 1

Write $$dx^{ijk}=dx_i\wedge dx_j\wedge dx_k$$ and $$dx^{1234}=dx_1\wedge dx_2\wedge dx_3\wedge dx_4$$. Expanding and removing repeated factors gives

$$
\gamma=\alpha\wedge\beta=-x_2\sin x_2\,dx^{123}+\cos x_3\,dx^{124}.
$$

Now $$h^*dx_3=x_4dx_3+x_3dx_4$$, while $$h^*dx_i=dx_i$$ for $$i=1,2,4$$. Therefore

$$
h^*\gamma=-x_2x_4\sin x_2\,dx^{123}
+\bigl(\cos(x_3x_4)-x_2x_3\sin x_2\bigr)dx^{124}.
$$

At the origin both the coefficient of $$dx^{123}$$ and the argument of the cosine vanish, so $$h^*\gamma(0)=dx^{124}$$. Evaluation on $$(e_1,e_2,e_3+e_4)$$ gives **1**.

For the derivatives, $$d\alpha=0$$ and

$$
d\beta=-\cos x_2\,dx^{123}+\sin x_3\,dx^{234}.
$$

The graded product rule then yields

$$
d\gamma=d\alpha\wedge\beta-\alpha\wedge d\beta
=-\sin x_3\,dx^{1234}.
$$

Finally, naturality of the exterior derivative and the pullback of the volume form give

$$
d(h^*\gamma)=h^*(d\gamma)=-x_4\sin(x_3x_4)\,dx^{1234}.
$$

### Exercise 2

The book uses $$f_3(r,\varphi,\vartheta)=(r\cos\varphi\sin\vartheta,r\sin\varphi\sin\vartheta,r\cos\vartheta)$$. Differentiating its components,

$$
\begin{aligned}
f_3^*dx&=\cos\varphi\sin\vartheta\,dr-r\sin\varphi\sin\vartheta\,d\varphi+r\cos\varphi\cos\vartheta\,d\vartheta,\\
f_3^*dy&=\sin\varphi\sin\vartheta\,dr+r\cos\varphi\sin\vartheta\,d\varphi+r\sin\varphi\cos\vartheta\,d\vartheta,\\
f_3^*dz&=\cos\vartheta\,dr-r\sin\vartheta\,d\vartheta.
\end{aligned}
$$

Wedge the last two expressions, keeping the order $$(dr,d\varphi,d\vartheta)$$, to obtain

$$
\begin{aligned}
f_3^*(dy\wedge dz)={}&-r\cos\varphi\sin\vartheta\cos\vartheta\,dr\wedge d\varphi
-r\sin\varphi\,dr\wedge d\vartheta\\
&-r^2\cos\varphi\sin^2\vartheta\,d\varphi\wedge d\vartheta.
\end{aligned}
$$

Wedging with $$f_3^*dx$$ gives

$$
f_3^*dx\wedge f_3^*(dy\wedge dz)=-r^2\sin\vartheta\,dr\wedge d\varphi\wedge d\vartheta.
$$

The minus sign agrees with the Jacobian in the book: the angular variables are ordered $$\varphi,\vartheta$$.

### Exercise 3

Assume the state functions are sufficiently differentiable on their physical domain, with $$T>0$$. Since

$$
dS=\frac{E_V+p}{T}\,dV+\frac{E_T}{T}\,dT,
$$

closedness of $$dS$$ gives

$$
\partial_T\!\left(\frac{E_V+p}{T}\right)
=\partial_V\!\left(\frac{E_T}{T}\right)=\frac{E_{TV}}{T}.
$$

Multiplying by $$T^2$$ and canceling $$TE_{VT}=TE_{TV}$$ proves

$$
E_V=T p_T-p.
$$

For the ideal gas $$p=RT/V$$, the right-hand side is zero. Thus $$E$$ is independent of $$V$$ on each connected volume interval, and on the usual product domain $$E=E(T)$$.

For the van der Waals equation $$p=cT/(V-b)-a/V^2$$, on a domain where the denominators are nonzero,

$$
E_V=\frac{cT}{V-b}-\left(\frac{cT}{V-b}-\frac a{V^2}\right)=\frac a{V^2}\ne0.
$$

In fact $$E=-a/V+F(T)$$ on each connected volume interval. Thus the volume dependence is nontrivial when $$a\ne0$$, as assumed in the exercise.

### Exercise 4

For $$r\ge1$$, a decomposable $$r$$-form wedges with itself to zero because each 1-form factor occurs twice. Graded commutativity therefore gives

$$
(\alpha+\beta)\wedge(\alpha+\beta)
=\bigl(1+(-1)^{r^2}\bigr)\alpha\wedge\beta
=\begin{cases}2\alpha\wedge\beta,&r\text{ even},\\0,&r\text{ odd}.\end{cases}
$$

If degree zero is included, wedge multiplication is ordinary multiplication, and the answer is instead $$(\alpha+\beta)^2$$.

### Exercise 5

**The statement needs a global qualification.** At each point the displayed equations are precisely the criterion for the 2-form to be a wedge of two covectors. They do not, in general, imply a factorization by two smooth 1-forms on all of $$X$$.

Set $$a_{ji}=-a_{ij}$$ and $$a_{ii}=0$$. If $$\alpha=u\wedge v$$ at a point, then $$a_{ij}=u_i v_j-u_j v_i$$; expansion shows that

$$
a_{ij}a_{k\ell}+a_{jk}a_{i\ell}+a_{ki}a_{j\ell}=0.
$$

Conversely, if all coefficients vanish, the pointwise form is zero and is decomposable. Otherwise choose $$a_{ij}\ne0$$. The displayed relation implies, for all $$k,\ell$$,

$$
a_{k\ell}=\frac{a_{ik}a_{j\ell}-a_{i\ell}a_{jk}}{a_{ij}}.
$$

Consequently, on the open set where $$a_{ij}\ne0$$, the smooth forms

$$
u=\sum_k a_{ik}\,dx_k,\qquad
v=\frac1{a_{ij}}\sum_k a_{jk}\,dx_k
$$

satisfy $$\alpha=u\wedge v$$. In particular, the conditions provide smooth local factors near every point where $$\alpha\ne0$$. No conclusion about smooth factorization in a neighborhood of a zero follows from this division argument.

For a global counterexample, take $$X=\mathbb R^3\setminus\{0\}$$ and

$$
\alpha=x\,dy\wedge dz+y\,dz\wedge dx+z\,dx\wedge dy.
$$

Every 2-form in dimension three satisfies the coefficient identities, and $$\alpha$$ is nowhere zero. Suppose $$\alpha=u\wedge v$$ globally. At each point its kernel is the radial line, so the independent forms $$u,v$$ both annihilate that line. Their restrictions to $$S^2$$ give a global coframe of its tangent bundle. Via the Euclidean metric either member gives a nowhere-vanishing tangent vector field on $$S^2$$, contradicting the hairy ball theorem. Hence global smooth factors need not exist.

### Exercise 6

Terms with repeated indices vanish in $$d\alpha=\sum_{i<j}da_{ij}\wedge dx_i\wedge dx_j$$. For a fixed $$i<j<k$$, the three contributing terms have signs

$$
\partial_k a_{ij}\,dx_k\wedge dx_i\wedge dx_j,
\quad \partial_i a_{jk}\,dx_i\wedge dx_j\wedge dx_k,
\quad \partial_j a_{ik}\,dx_j\wedge dx_i\wedge dx_k.
$$

Using $$a_{ki}=-a_{ik}$$ and reordering proves

$$
d\alpha=\sum_{i<j<k}(\partial_k a_{ij}+\partial_i a_{jk}+\partial_j a_{ki})\,dx_i\wedge dx_j\wedge dx_k.
$$

### Exercise 7

Put $$r=\deg\alpha$$. The graded Leibniz rule and $$d^2=0$$ give

$$
d(d\alpha\wedge\beta-\alpha\wedge d\beta)
=\bigl((-1)^{r+1}-(-1)^r\bigr)d\alpha\wedge d\beta
=2(-1)^{r+1}d\alpha\wedge d\beta.
$$

If $$r=\deg\alpha$$ and $$s=\deg\beta$$ are even, differentiation of the three terms in (b) gives, respectively,

$$
\begin{aligned}
&-d\alpha\wedge d\beta\wedge\gamma-d\alpha\wedge\beta\wedge d\gamma,\\
&+d\alpha\wedge d\beta\wedge\gamma-\alpha\wedge d\beta\wedge d\gamma,\\
&+d\alpha\wedge\beta\wedge d\gamma+\alpha\wedge d\beta\wedge d\gamma.
\end{aligned}
$$

All terms cancel, so the answer to (b) is **zero**.

### Exercise 8

On $$\mathbb R^m\setminus\{0\}$$, the coefficient of the volume form in $$d\alpha$$ is the divergence of $$x/|x|^m$$:

$$
\sum_{j=1}^m\partial_j(x_j|x|^{-m})
=m|x|^{-m}-m|x|^{-m-2}\sum_{j=1}^m x_j^2=0.
$$

Thus $$d\alpha=0$$ on the stated domain. This calculation makes no assertion at the excluded origin.

### Exercise 9

The coefficient of $$dx\wedge dy\wedge dz$$ in $$d\alpha$$ is $$2z-2z=0$$. Since $$\mathbb R^3$$ is star-shaped, closedness also proves exactness by the Poincaré lemma. To find a primitive, the coefficient of $$dy\wedge dz$$ suggests starting with $$-xz^2\,dy$$. Its derivative also contributes $$-z^2\,dx\wedge dy$$. Adding $$z\,dx-e^x\,dy$$ supplies the remaining terms, so

$$
\boxed{\eta=z\,dx-(xz^2+e^x)\,dy},\qquad
 d\eta=2xz\,dy\wedge dz+dz\wedge dx-(z^2+e^x)\,dx\wedge dy=\alpha.
$$

### Exercise 10

In the coordinate bases, let $$W(x)=(\omega_x(e_i,e_j))_{i,j}$$. If $$v=\sum_i v_i e_i$$ and $$\eta=\sum_j\eta_j dx_j$$, the equation $$\Theta_\omega v=\eta$$ becomes

$$
W(x)^T v(x)=\eta(x).
$$

Nondegeneracy says that $$W(x)^T$$ is invertible at every point. Its inverse is smooth because its entries are cofactors divided by the nowhere-zero determinant. Thus $$v=(W^T)^{-1}\eta$$ is a smooth vector field, proving surjectivity and injectivity. The pointwise bilinearity of $$\omega$$ makes both the map and its inverse $$\mathcal E(X)$$-linear.

### Exercise 11

The book defines $$\sigma=\sum_{j=1}^m dp_j\wedge dq_j$$. For $$v=\sum_j(a_j\partial_{q_j}+b_j\partial_{p_j})$$,

$$
\Theta_\sigma v=\sum_j(b_j\,dq_j-a_j\,dp_j).
$$

If this is zero, all $$a_j,b_j$$ vanish, proving nondegeneracy; constant coefficients give $$d\sigma=0$$. For the top power, all products with a repeated index vanish, while the even-degree factors commute. Hence

$$
\sigma^m=m!\,dp_1\wedge dq_1\wedge\cdots\wedge dp_m\wedge dq_m\ne0.
$$

Finally, equating $$\Theta_\sigma v$$ with $$df$$ yields

$$
\operatorname{sgrad}f=\sum_{j=1}^m\left(-\frac{\partial f}{\partial p_j}\frac\partial{\partial q_j}+\frac{\partial f}{\partial q_j}\frac\partial{\partial p_j}\right).
$$

### Exercise 12

Write $$X_f=\operatorname{sgrad}f$$. Substitution into $$\sigma(X_f,X_g)$$ gives

$$
\{f,g\}=\sum_j(f_{p_j}g_{q_j}-f_{q_j}g_{p_j}).
$$

This proves (i). The same formula proves linearity in the second argument, skew-symmetry, and the product rule (ii), (iii), and (v), using the ordinary product rule for partial derivatives.

For the Jacobi identity, put all coordinates into a list $$z^1,\ldots,z^{2m}$$ and write $$\{f,g\}=P^{ab}f_a g_b$$ with a constant skew-symmetric matrix $$P$$. In the cyclic sum of $$\{f,\{g,h\}\}$$, the terms involving second derivatives of $$g$$ are

$$
P^{ab}P^{cd}\bigl(f_a g_{bc}h_d+h_a f_c g_{bd}\bigr).
$$

In the second term reindex $$(a,b,c,d)\mapsto(d,c,a,b)$$. Since $$P^{dc}=-P^{cd}$$ and mixed derivatives commute, it becomes the negative of the first. The terms with second derivatives of $$f$$ and $$h$$ cancel in the same way. This proves (iv).

**(vi): correction.** As printed, the right-hand side $$(X_f\mid X_g)_{\mathbb R^{2m}}$$ is a scalar function, while the left-hand side is a vector field. Even a componentwise identification cannot fix the assertion: taking $$f=g=q_1$$ gives zero on the left but 1 on the right. The natural vector-field identity, with the standard commutator convention $$[X,Y]u=X(Yu)-Y(Xu)$$, is

$$
X_{\{f,g\}}=-[X_f,X_g].
$$

Indeed $$X_f u=\{u,f\}$$. Applying the Jacobi identity to $$u,f,g$$ gives

$$
[X_f,X_g]u=\{\{u,g\},f\}-\{\{u,f\},g\}=-\{u,\{f,g\}\}=-X_{\{f,g\}}u.
$$

Equality on every smooth $$u$$ proves the vector-field identity. The sign follows from this book's definitions of $$\sigma$$ and the Poisson bracket.

### Exercise 13

Let $$\tau_j=dp_j\wedge dq_j$$. Since the $$\tau_j$$ have even degree,

$$
\sigma^{m-1}=(m-1)!\sum_{j=1}^m\tau_1\wedge\cdots\wedge\widehat{\tau_j}\wedge\cdots\wedge\tau_m.
$$

When wedged with the term omitting $$\tau_j$$, only the $$dp_j\wedge dq_j$$ component of $$df\wedge dg$$ survives. Its coefficient is $$f_{p_j}g_{q_j}-f_{q_j}g_{p_j}$$. Moving $$\tau_j$$ into place causes no sign change because each $$\tau_k$$ has even degree. Therefore

$$
df\wedge dg\wedge\sigma^{m-1}
=(m-1)!\sum_j(f_{p_j}g_{q_j}-f_{q_j}g_{p_j})\,\tau_1\wedge\cdots\wedge\tau_m
=\frac1m\{f,g\}\sigma^m.
$$
