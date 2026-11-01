# Chapter XI — Manifolds and Differential Forms

## 2. Multilinear algebra

These solutions address Exercises 1–11. Unless stated otherwise, $$V$$ is a real oriented inner product space of dimension $$m$$, $$\omega$$ is its oriented volume form, and $$\Theta v=\langle v,\cdot\rangle$$. For a positive basis $$(b_1,\ldots,b_m)$$ with dual basis $$(\beta^1,\ldots,\beta^m)$$, put

$$
g_{ij}=\langle b_i,b_j\rangle,\qquad (g^{ij})=(g_{ij})^{-1},\qquad G=\det(g_{ij}).
$$

The Hodge star is the one defined in the book by $$\alpha\wedge\gamma=\langle *\alpha,\gamma\rangle_{m-r}\omega$$ for $$\deg\alpha=r$$. In the indefinite case this convention has a sign that differs from another commonly used convention; Exercise 9 spells it out. Exercise 5 contains a coefficient error, and Exercise 10 confuses a filtration with a grading.

### Exercise 1

For a multilinear $$r$$-form $$T$$, every term in

$$
\operatorname{Alt}(T)(v_1,\ldots,v_r)
=\frac1{r!}\sum_{\sigma\in S_r}\operatorname{sgn}(\sigma)
T(v_{\sigma(1)},\ldots,v_{\sigma(r)})
$$

is multilinear; the sum is therefore multilinear. If the arguments are permuted by $$\tau$$, reindexing by the composite permutation gives

$$
\operatorname{Alt}(T)(v_{\tau(1)},\ldots,v_{\tau(r)})
=\operatorname{sgn}(\tau)\operatorname{Alt}(T)(v_1,\ldots,v_r).
$$

Thus $$\operatorname{Alt}(T)\in\bigwedge^rV^*$$, and the formula is linear in $$T$$. Since the spaces are finite-dimensional, the map is continuous. If $$T$$ is already alternating, every term of the sum equals $$T(v_1,\ldots,v_r)$$, so $$\operatorname{Alt}(T)=T$$. Applying this to $$\operatorname{Alt}(T)$$ proves

$$
\operatorname{Alt}^2=\operatorname{Alt}.
$$

For $$r=0$$ this is the identity on the scalars. In particular, the alternator is the projection onto the alternating forms.

### Exercise 2

Let $$\alpha\in\bigwedge^rV^*$$ and $$\beta\in\bigwedge^sV^*$$. In the alternation of $$\alpha\otimes\beta$$, permuting the first $$r$$ entries within their group or the last $$s$$ within theirs changes the tensor value by the same sign as the permutation. Thus each choice of the two ordered groups contributes $$r!s!$$ identical signed terms. Dividing by $$(r+s)!$$ leaves

$$
\frac{(r+s)!}{r!s!}\operatorname{Alt}(\alpha\otimes\beta)
=\sum_{\sigma\in\operatorname{Sh}(r,s)}\operatorname{sgn}(\sigma)
\alpha(v_{\sigma(1)},\ldots,v_{\sigma(r)})
\beta(v_{\sigma(r+1)},\ldots,v_{\sigma(r+s)}),
$$

where the sum is over shuffles, meaning permutations increasing within each group. This is the book's exterior product: for decomposable forms it is the Laplace expansion of the determinant defining the wedge, and arbitrary forms follow by bilinearity and the basis of exterior forms. The formula remains valid for degree zero, where the wedge is scalar multiplication.

### Exercise 3

Assume $$\dim V=3$$ and define $$v\times w=\Theta^{-1}(\omega(v,w,\cdot))$$.

**(a), (b), and (e).** By the definition of $$\Theta$$,

$$
\langle v\times w,u\rangle=\omega(v,w,u).
$$

Linearity of $$\omega$$ and of $$\Theta^{-1}$$ makes the product bilinear; alternation of $$\omega$$ gives $$v\times v=0$$ and $$v\times w=-w\times v$$. Substituting $$u=v$$ or $$u=w$$ in the displayed equation proves orthogonality to both factors.

**(c) and (d).** If $$v,w$$ are dependent, the defining functional is zero. If they are independent, they extend to a basis $$(v,w,u)$$, and the nonzero volume form evaluates nontrivially on that basis. Hence $$v\times w\ne0$$. In this case

$$
\omega(v,w,v\times w)=\langle v\times w,v\times w\rangle>0,
$$

so $$(v,w,v\times w)$$ is a positive basis.

**(f).** For nonzero $$v,w$$, write $$w=av+w_\perp$$ with $$w_\perp\perp v$$. If $$w_\perp\ne0$$, extend the normalized vectors $$v/|v|$$ and $$w_\perp/|w_\perp|$$ to a positive orthonormal basis. The definition then gives $$|v\times w|=|v||w_\perp|$$; the same equality is immediate when $$w_\perp=0$$. Thus

$$
|v\times w|^2=|v|^2|w_\perp|^2
=|v|^2|w|^2-\langle v,w\rangle^2
=|v|^2|w|^2\sin^2\varphi.
$$

Taking the nonnegative square root proves the formula.

**(g).** In a positive orthonormal basis, $$e_1\times e_2=e_3$$ and cyclic permutations hold, while swapping the factors changes sign. Expanding bilinearly gives

$$
v\times w=(\xi^2\eta^3-\xi^3\eta^2)e_1
+(\xi^3\eta^1-\xi^1\eta^3)e_2
+(\xi^1\eta^2-\xi^2\eta^1)e_3.
$$

**(h)–(k).** The coordinate formula gives, for every $$d\in V$$,

$$
\langle a\times(b\times c),d\rangle
=\langle a,c\rangle\langle b,d\rangle
-\langle a,b\rangle\langle c,d\rangle.
$$

Nondegeneracy yields the Grassmann identity

$$
a\times(b\times c)=\langle a,c\rangle b-\langle a,b\rangle c.
$$

It also shows nonassociativity, for example $$(e_1\times e_1)\times e_2=0$$ but $$e_1\times(e_1\times e_2)=-e_2$$. Applying the identity and antisymmetry with $$a=v_1\times v_2$$ gives

$$
(v_1\times v_2)\times(v_3\times v_4)
=\omega(v_1,v_2,v_4)v_3-\omega(v_1,v_2,v_3)v_4.
$$

Finally, summing the Grassmann identity cyclically in $$(v_1,v_2,v_3)$$ makes each scalar-product term cancel with another, proving the Jacobi identity.

### Exercise 4

Let $$\alpha\in\bigwedge^rV^*$$ and $$\beta\in\bigwedge^{m-r}V^*$$. By the definition of $$*$$ and graded commutativity,

$$
\langle *\alpha,\beta\rangle_{m-r}\omega
=\alpha\wedge\beta
=(-1)^{r(m-r)}\beta\wedge\alpha
=(-1)^{r(m-r)}\langle *\beta,\alpha\rangle_r\omega.
$$

Symmetry of the inner product proves (a). For $$\alpha,\beta$$ both of degree $$r$$, graded commutativity and the defining identity $$\beta\wedge *\alpha=\langle\beta,\alpha\rangle_r\omega$$ yield

$$
(*\alpha)\wedge\beta=(-1)^{r(m-r)}\langle\alpha,\beta\rangle_r\omega
=(*\beta)\wedge\alpha,
$$

which proves (b). Finally, since $$\Theta$$ is an isometry and $$*\omega=1$$,

$$
*(\Theta v\wedge *\Theta w)
=*(\langle\Theta v,\Theta w\rangle_1\omega)
=\langle v,w\rangle,
$$

proving (c).

### Exercise 5

The positive basis gives $$\omega=\sqrt G\,\beta^1\wedge\cdots\wedge\beta^m$$, and the induced inner product on covectors satisfies $$\langle\beta^j,\beta^k\rangle_1=g^{jk}$$. Hence

$$
\beta^j\wedge *\beta^k
=g^{jk}\omega
=g^{jk}\sqrt G\,\beta^1\wedge\cdots\wedge\beta^m,
$$

which is (a). Write $$\eta_k=\beta^1\wedge\cdots\wedge\widehat{\beta^k}\wedge\cdots\wedge\beta^m$$ and $$*\beta^j=\sum_k c_k\eta_k$$. Since $$\beta^\ell\wedge\eta_k=0$$ for $$\ell\ne k$$ and $$\beta^k\wedge\eta_k=(-1)^{k-1}\beta^1\wedge\cdots\wedge\beta^m$$, part (a) gives

$$
*\beta^j=\sqrt G\sum_{k=1}^m(-1)^{k-1}g^{jk}
\beta^1\wedge\cdots\wedge\widehat{\beta^k}\wedge\cdots\wedge\beta^m.
$$

Now let $$m=3$$ and $$(j,k,\ell)$$ be a permutation of $$(1,2,3)$$. For each $$i$$, the defining relation gives

$$
\langle *(\beta^j\wedge\beta^k),\beta^i\rangle_1\omega
=\beta^j\wedge\beta^k\wedge\beta^i
=\frac{\operatorname{sgn}(j,k,\ell)}{\sqrt G}\,\delta_{i\ell}\omega.
$$

Since $$\langle\Theta b_\ell,\beta^i\rangle_1=\delta_{i\ell}$$, nondegeneracy implies

$$
*(\beta^j\wedge\beta^k)
=\frac{\operatorname{sgn}(j,k,\ell)}{\sqrt G}
\sum_{i=1}^3g_{\ell i}\beta^i
=\frac{\operatorname{sgn}(j,k,\ell)}{\sqrt G}\,\Theta b_\ell.
$$

**Printed coefficient.** The last equality in the cited edition has $$1/G$$ rather than $$1/\sqrt G$$ multiplying $$\Theta b_\ell$$. It is false for a general basis: for $$b_i=2e_i$$ in a positive orthonormal frame, $$G=64$$, and the correct coefficient is $$1/8$$, not $$1/64$$.

### Exercise 6

In a positive orthonormal basis with dual $$\epsilon^1,\epsilon^2,\epsilon^3$$, the Hodge formula gives

$$
*(\epsilon^1\wedge\epsilon^2)=\epsilon^3,\quad
*(\epsilon^2\wedge\epsilon^3)=\epsilon^1,\quad
*(\epsilon^3\wedge\epsilon^1)=\epsilon^2.
$$

The map $$(v,w)\mapsto\Theta^{-1}(*(\Theta v\wedge\Theta w))$$ is bilinear and alternating and takes the same values as the cross product on basis pairs. Therefore it equals $$v\times w$$ for all $$v,w\in V$$.

### Exercise 7

For any $$v\in V$$ and any permutation $$(j,k,\ell)$$ of $$(1,2,3)$$,

$$
\langle b_j\times b_k,v\rangle
=\omega(b_j,b_k,v)
=\sqrt G\,\operatorname{sgn}(j,k,\ell)\,\beta^\ell(v).
$$

By the Riesz isomorphism,

$$
b_j\times b_k
=\sqrt G\,\operatorname{sgn}(j,k,\ell)\,\Theta^{-1}\beta^\ell
=\sqrt G\,\operatorname{sgn}(j,k,\ell)
\sum_{i=1}^3g^{\ell i}b_i.
$$

The last equality follows by pairing the sum with each basis vector.

### Exercise 8

An orientation-preserving linear isometry $$A:V\to W$$ between spaces of the same dimension is an isomorphism. Its pullback preserves the induced inner products on every exterior power: for decomposable forms this follows from the determinant formula for the inner product, and bilinearity extends it to all forms. It also preserves wedges and satisfies $$A^*\omega_W=\omega_V$$.

For $$\alpha\in\bigwedge^rW^*$$ and arbitrary $$\gamma\in\bigwedge^{m-r}W^*$$, pull back the defining star identity:

$$
\begin{aligned}
A^*\alpha\wedge A^*\gamma
&=A^*(\alpha\wedge\gamma)\\
&=\langle *_W\alpha,\gamma\rangle_{m-r}\omega_V\\
&=\langle A^*(*_W\alpha),A^*\gamma\rangle_{m-r}\omega_V.
\end{aligned}
$$

Since $$A^*$$ is onto on exterior powers, $$A^*\gamma$$ ranges over all $$(m-r)$$-forms on $$V$$. Uniqueness in the definition of the Hodge star gives

$$
*_V(A^*\alpha)=A^*(*_W\alpha),
$$

which is the commutativity of the diagram.

### Exercise 9

Let $$b$$ be a nondegenerate symmetric form with $$q$$ negative squares, put $$\delta=(-1)^q=\operatorname{sgn}(\det(g_{ij}))$$, and use $$b_r$$ for the induced form on $$r$$-covectors. Let $$\Theta_b(v)=b(v,\cdot)$$ and $$D=\sqrt{|\det(g_{ij})|}$$ for a positive basis. The book defines the indefinite Hodge star by

$$
\alpha\wedge\gamma=b_{m-r}(*\alpha,\gamma)\omega,
\qquad \omega=D\,\beta^1\wedge\cdots\wedge\beta^m.
$$

In particular its convention gives

$$
*1=\delta\omega,\quad *\omega=1,\quad
**\alpha=\delta(-1)^{r(m-r)}\alpha,\quad
\alpha\wedge *\beta=\delta\,b_r(\alpha,\beta)\omega.
$$

For example, choose a positive $$b$$-orthonormal basis with squared lengths $$s_i\in\{1,-1\}$$. If $$I$$ and $$I^c$$ are complementary ordered index sets, the defining identity gives

$$
*\epsilon^I=\operatorname{sgn}(I,I^c)\left(\prod_{i\in I^c}s_i\right)\epsilon^{I^c}.
$$

Applying this twice proves the displayed double-star identity; bilinearity then gives the wedge identity. Note that the convention $$\alpha\wedge *\beta=b_r(\alpha,\beta)\omega$$ used elsewhere would multiply the book's star by $$\delta$$.

The analogues of Exercise 4 are, for $$\deg\alpha=r$$ and $$\deg\gamma=m-r$$,

$$
b_{m-r}(*\alpha,\gamma)=(-1)^{r(m-r)}b_r(\alpha,*\gamma),
$$

and, for $$\alpha,\beta$$ of the same degree,

$$
(*\alpha)\wedge\beta=(*\beta)\wedge\alpha,\qquad
*(\Theta_bv\wedge *\Theta_bw)=\delta\,b(v,w).
$$

The first follows directly from $$\alpha\wedge\gamma=(-1)^{r(m-r)}\gamma\wedge\alpha$$ and the defining relation. The second follows from the wedge identity and symmetry of $$b_r$$; the last uses $$*\omega=1$$.

For the analogues of Exercise 5, the induced covector Gram matrix is still $$(g^{ij})$$. Thus

$$
\beta^j\wedge *\beta^k=\delta\,g^{jk}D\,
\beta^1\wedge\cdots\wedge\beta^m,
$$

and the same coefficient comparison as in Exercise 5 gives

$$
*\beta^j=\delta D\sum_{k=1}^m(-1)^{k-1}g^{jk}
\beta^1\wedge\cdots\wedge\widehat{\beta^k}\wedge\cdots\wedge\beta^m.
$$

If $$m=3$$ and $$(j,k,\ell)$$ is a permutation of $$(1,2,3)$$, using the defining identity with $$\gamma=\beta^i$$ instead gives

$$
*(\beta^j\wedge\beta^k)
=\frac{\operatorname{sgn}(j,k,\ell)}{D}
\sum_{i=1}^3g_{\ell i}\beta^i
=\frac{\operatorname{sgn}(j,k,\ell)}{D}\,\Theta_b b_\ell.
$$

There is no extra $$\delta$$ in this last expression under the book's definition; it follows directly by pairing both sides with each $$\beta^i$$.

### Exercise 10

The displayed equality is false with the printed definition $$\mathbb K_k[X]=\{p:\deg p\le k\}$$. These subspaces are nested: for example $$1\in\mathbb K_0[X]\cap\mathbb K_1[X]$$, so their sum inside $$\mathbb K[X]$$ is not direct. They instead form a filtration,

$$
\mathbb K_0[X]\subset\mathbb K_1[X]\subset\cdots,\qquad
\mathbb K_r[X]\,\mathbb K_s[X]\subset\mathbb K_{r+s}[X].
$$

A correct grading uses the homogeneous components $$P_k=\mathbb K X^k$$. Every polynomial has a unique finite representation $$p=\sum_{k\ge0}a_kX^k$$, whence

$$
\mathbb K[X]=\bigoplus_{k\ge0}P_k,\qquad P_rP_s\subset P_{r+s}.
$$

Multiplication is associative and ordinarily commutative. In coefficient form it is convolution:

$$
\left(\sum_i a_iX^i\right)\left(\sum_j b_jX^j\right)
=\sum_k\left(\sum_{i+j=k}a_i b_j\right)X^k.
$$

Thus the corrected algebra is graded and commutative in the ordinary sense. It is not graded **anticommutative** in the book's sign convention over $$\mathbb R$$ or $$\mathbb C$$, since the degree-one element $$X$$ has $$X^2\ne-X^2$$.

### Exercise 11

Take the standard orientation $$(e_0,e_1,e_2,e_3)$$ and the metric $$\operatorname{diag}(1,-1,-1,-1)$$, so $$\delta=-1$$. Define

$$
T_i=\epsilon^i\wedge\epsilon^0,\qquad
S_1=\epsilon^2\wedge\epsilon^3,\quad
S_2=\epsilon^3\wedge\epsilon^1,\quad
S_3=\epsilon^1\wedge\epsilon^2.
$$

The complement formula in Exercise 9, with the book's indefinite convention, gives

$$
*T_i=-S_i,\qquad *S_i=T_i\qquad(i=1,2,3).
$$

For instance, $$*(\epsilon^0\wedge\epsilon^1)=\epsilon^2\wedge\epsilon^3$$ and $$*(\epsilon^2\wedge\epsilon^3)=-\epsilon^0\wedge\epsilon^1$$. Consequently, from $$\alpha=c\sum_iE_iT_i+\sum_iH_iS_i$$ and $$\beta=-c\sum_iH_iT_i+\sum_iE_iS_i$$,

$$
*\alpha=\sum_{i=1}^3H_iT_i-c\sum_{i=1}^3E_iS_i,
\qquad
*\beta=\sum_{i=1}^3E_iT_i+c\sum_{i=1}^3H_iS_i.
$$

These formulas hold for every real $$c$$, including zero. They satisfy $$**\alpha=-\alpha$$ and $$**\beta=-\beta$$, as required for two-forms in signature $$(1,3)$$. Reversing the chosen orientation changes both displayed stars by a minus sign.
