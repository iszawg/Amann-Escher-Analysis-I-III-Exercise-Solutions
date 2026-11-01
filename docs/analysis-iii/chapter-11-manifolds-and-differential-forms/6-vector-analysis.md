# Chapter XI — Manifolds and Differential Forms

## 6. Vector analysis

These solutions address Exercises 1–11. We use the book's convention $$\Delta=d\delta+\delta d$$, which is the sum of second partial derivatives in Euclidean coordinates. For a vector field, $$\boldsymbol\Delta=\Theta^{-1}\Delta\Theta$$. In pseudo-Riemannian signature, the sign convention for the book's Hodge star matters; Exercise 4 spells it out. Exercise 5 contains several independent inconsistencies, and Exercise 10 has a misprinted torus.

### Exercise 1

In local coordinates $$x^1,x^2$$, with $$g=(g_{ij})$$ and $$G=\det(g_{ij})$$, the Laplace–Beltrami operator is

$$
\Delta u=\frac1{\sqrt G}\sum_{i,j=1}^2
\partial_i\!\left(\sqrt G\,g^{ij}\partial_j u\right).
$$

**(i)** For $$F(\varphi,z)=(\cos\varphi,\sin\varphi,z)$$, the coordinate tangent vectors are orthonormal. Thus

$$
\Delta u=u_{\varphi\varphi}+u_{zz}.
$$

**(ii)** Write $$A=2+\cos\alpha$$. For the given torus parametrization, the two tangent vectors are perpendicular, with squared lengths 1 and $$A^2$$. Hence $$\sqrt G=A$$ and

$$
\boxed{\Delta u=u_{\alpha\alpha}-\frac{\sin\alpha}{2+\cos\alpha}u_\alpha
+\frac1{(2+\cos\alpha)^2}u_{\beta\beta}.}
$$

This expression holds in the given chart; the angles are periodic on the whole torus.

**(iii)** For the graph $$F(x,y)=(x,y,f(x,y))$$, put $$W=1+f_x^2+f_y^2$$. The metric and its inverse are

$$
(g_{ij})=\begin{pmatrix}1+f_x^2&f_xf_y\\f_xf_y&1+f_y^2\end{pmatrix},\quad
(g^{ij})=\frac1W\begin{pmatrix}1+f_y^2&-f_xf_y\\-f_xf_y&1+f_x^2\end{pmatrix},\quad G=W.
$$

Thus, for the coordinate representative of $$u$$,

$$
\boxed{\Delta u=\frac1{\sqrt W}\left[
\partial_x\!\left(\frac{(1+f_y^2)u_x-f_xf_yu_y}{\sqrt W}\right)
+\partial_y\!\left(\frac{(1+f_x^2)u_y-f_xf_yu_x}{\sqrt W}\right)\right].}
$$

Expanding the derivatives gives the equivalent expression

$$
\begin{aligned}
\Delta u={}&\frac{(1+f_y^2)u_{xx}-2f_xf_yu_{xy}+(1+f_x^2)u_{yy}}W\\
&-\frac{(1+f_y^2)f_{xx}-2f_xf_yf_{xy}+(1+f_x^2)f_{yy}}{W^2}(f_xu_x+f_yu_y).
\end{aligned}
$$

### Exercise 2

The printed expression must be understood as a sum of **partial operators**: pullback of functions alone does not define $$\pi_j^*\Delta_{M_j}$$ on arbitrary functions on the product. For $$u\in C^\infty(M_1\times M_2)$$, define

$$
\begin{aligned}
(\Delta_1^{\mathrm{part}}u)(p,q)&=\Delta_{M_1}(u(\cdot,q))(p),\\
(\Delta_2^{\mathrm{part}}u)(p,q)&=\Delta_{M_2}(u(p,\cdot))(q).
\end{aligned}
$$

In product coordinates the metric matrix is block diagonal and $$\sqrt G=\sqrt{G_1}\sqrt{G_2}$$. In the divergence formula for $$\Delta$$, the factor $$\sqrt{G_2}$$ is constant under the $$M_1$$ derivatives and conversely. The two blocks therefore give

$$
\boxed{\Delta_{M_1\times M_2}u=\Delta_1^{\mathrm{part}}u+\Delta_2^{\mathrm{part}}u.}
$$

In particular, if $$u=a(p)b(q)$$, the answer is $$(\Delta_{M_1}a)b+a(\Delta_{M_2}b)$$. The assumption that one factor has empty boundary ensures that the product is a manifold with boundary in the book's category.

### Exercise 3

For an isometric diffeomorphism $$f:M\to N$$, pullback commutes with $$d$$ and with the codiﬀerential $$\delta$$. The latter follows from the isometry and the two Hodge stars in the definition of $$\delta$$: an orientation reversal changes both stars' signs, and those signs cancel. This remains true componentwise on disconnected manifolds. Consequently, for every $$r$$-form $$\alpha$$ on $$N$$,

$$
\Delta_M f^*\alpha=(d\delta+\delta d)f^*\alpha
=f^*(d\delta+\delta d)\alpha=f^*\Delta_N\alpha.
$$

This also covers $$r=0$$ and $$r=m$$, using the zero operators at the end degrees.

### Exercise 4

Let $$\omega$$ be the oriented pseudo-Riemannian volume form and $$s=\operatorname{sign}(\det g)\in\{\pm1\}$$, locally constant. Under the book's pseudo-Riemannian convention,

$$
*1=s\omega,\qquad *\omega=1,\qquad
\alpha\wedge*\beta=s\langle\alpha,\beta\rangle\omega.
$$

For a vector field $$v$$, the identity $$\alpha\wedge\iota_v\omega=\alpha(v)\omega$$ for all 1-forms $$\alpha$$ shows that

$$
\boxed{*\Theta v=s\,\iota_v\omega.}
$$

Therefore the printed triangular diagram commutes without a sign only when $$s=1$$. Since $$d\iota_v\omega=(\operatorname{div}v)\omega$$, the correct general formulas are

$$
\operatorname{div}v=s*d*\Theta v,\qquad
\Delta f=s*d*df.
$$

For example, on $$\mathbb R^3$$ with $$g=-dt^2+dx^2+dy^2$$, one has $$s=-1$$; for $$f=t^2$$, $$\Delta f=-2$$ but $$*d*df=2$$. Both displayed formulas in the exercise hold as printed for a Riemannian metric.

When $$m=3$$, the curl formula **does** hold without an extra sign. Indeed $$*^2=s$$ on 1-forms, so the boxed identity gives $$*(\iota_v\omega)=\Theta v$$. The defining equation $$\iota_{\operatorname{curl}v}\omega=d\Theta v$$ then yields

$$
\boxed{\operatorname{curl}v=\Theta^{-1}*d\Theta v.}
$$

All identities are local and apply componentwise if the signature changes between connected components.

### Exercise 5

This exercise needs more than a single typographical correction. We first analyze the printed definitions literally, using the pseudo-Riemannian Hodge-star convention of Remark 5.11. Put $$x^0=t$$, $$g=dt^2-\sum_i(dx^i)^2$$, and use orientation $$dt\wedge dx^1\wedge dx^2\wedge dx^3$$. Define

$$
\Sigma_1=dx^2\wedge dx^3,\quad
\Sigma_2=dx^3\wedge dx^1,\quad
\Sigma_3=dx^1\wedge dx^2,\quad
\operatorname{vol}_3=dx^1\wedge dx^2\wedge dx^3.
$$

The defining identity in Remark 5.11 gives, for cyclic $$(i,j,k)$$,

$$
*(dx^i\wedge dt)=-dx^j\wedge dx^k=-\Sigma_i.
$$

For example, $$(dx^1\wedge dt)\wedge(dx^2\wedge dx^3)=-\omega$$, whereas its squared form norm is $$-1$$ and $$s=-1$$. This also shows that the opposite sign printed in Example 5.12(a) conflicts with Remark 5.11. Under Remark 5.11 the form in this exercise is therefore

$$
F=c\left(\sum_iE_i\,dx^i\wedge dt-\sum_iB_i\Sigma_i\right).
$$

**(a)** Differentiate, remembering that $$d_x(E_i dx^i)=\sum_i(\operatorname{curl}E)_i\Sigma_i$$ and $$d_x(\sum_iB_i\Sigma_i)=(\operatorname{div}B)\operatorname{vol}_3$$:

$$
dF=c\left[dt\wedge\sum_i\bigl((\operatorname{curl}E)_i-\partial_tB_i\bigr)\Sigma_i
-(\operatorname{div}B)\operatorname{vol}_3\right].
$$

Thus $$dF=0$$ is equivalent to $$\partial_tB=\operatorname{curl}E$$ and $$\operatorname{div}B=0$$, not the displayed equation. For a concrete counterexample, take $$E=(0,x^1,0)$$ and $$B=(0,0,t)$$. Then $$dF=0$$, but $$\partial_tB+c\operatorname{curl}E=(0,0,1+c)\ne0$$.

**(b)** As printed, $$dF$$ is a 3-form and $$J$$ is a 1-form, so the equation $$dF=4\pi J$$ cannot be the intended source equation. With the book's codiﬀerential convention, direct computation gives instead

$$
\delta F=-c\left[\sum_i\bigl(\partial_tE_i+(\operatorname{curl}B)_i\bigr)dx^i
+(\operatorname{div}E)dt\right].
$$

This equation shows explicitly that replacing $$d$$ by $$\delta$$ alone does not recover the printed source equations with the printed $$F,J$$ and arbitrary $$c$$. In addition, taking the divergence of the two printed source equations gives $$\partial_t\rho-\operatorname{div}j=0$$, not the plus-sign continuity equation in (d).

**(c)** On flat Minkowski space, $$\Delta=d\delta+\delta d$$ acts on each coefficient as $$\Box=\partial_t^2-\Delta_x$$. Hence $$\Delta F=0$$ is a second-order wave equation for each component. It does not imply the four first-order equations: take $$E=(x^1,0,0)$$ and $$B=0$$. All coefficients of $$F$$ have zero wave operator, but $$\operatorname{div}E=1$$. For arbitrary $$c$$ even the converse as printed fails with this metric: $$E=(0,\sin(x^1-ct),0)$$ and $$B=(0,0,\sin(x^1-ct))$$ solve the four displayed first-order equations, whereas $$\Box E=(1-c^2)E$$, nonzero when $$c\ne1$$.

**(d)** The condition $$dF=0$$ imposes no condition on independent fields $$j,\rho$$. Take $$E=B=j=0$$ and $$\rho=t$$. Then $$dF=0$$ but $$\partial_t\rho+\operatorname{div}j=1$$. Moreover, $$\operatorname{grad}J$$ is not the appropriate operation on a 1-form. A continuity law follows from a correctly signed source equation by applying $$\delta$$ and using $$\delta^2=0$$; it is the divergence of the associated current, not the gradient of $$J$$.

**(e)** The intended vector potential must take values in $$\mathbb R^3$$, not $$\mathbb R$$. With the literal $$F$$ above, exactness is equivalent to the existence of smooth $$A:\mathbb R\times\Omega\to\mathbb R^3$$ and $$\Phi:\mathbb R\times\Omega\to\mathbb R$$ such that

$$
\boxed{B=-\operatorname{curl}A,\qquad E=-\partial_tA-\operatorname{grad}\Phi.}
$$

Indeed, for $$P=c(\sum_iA_i dx^i-\Phi\,dt)$$,

$$
dP=c\left[\sum_i(-\partial_tA_i-\partial_i\Phi)dx^i\wedge dt
+\sum_i(\operatorname{curl}A)_i\Sigma_i\right].
$$

Conversely, every global primitive has the form $$P=c(\sum_iA_i dx^i-\Phi dt)$$, so comparison of coefficients proves the equivalence. It is global and does not assume contractibility. The printed plus sign for $$B$$ is incompatible with the literal Hodge-star definition: take $$A=(0,tx^1,0)$$ and $$\Phi=0$$. The corresponding exact $$F$$ has $$E=(0,-x^1,0)$$ and $$B=(0,0,-t)$$, which cannot satisfy the printed potential equations because they would imply $$\partial_tB+\operatorname{curl}E=0$$.

**A consistent standard formulation.** Put $$\tau=ct$$, use $$g=d\tau^2-\sum_i(dx^i)^2$$, and define directly $$F_{\rm std}=\sum_i E_i dx^i\wedge d\tau+\sum_iB_i\Sigma_i$$. Then

$$
dF_{\rm std}=0\quad\Longleftrightarrow\quad
\partial_tB+c\operatorname{curl}E=0,\quad\operatorname{div}B=0.
$$

With $$J_{\rm std}=\sum_i(j_i/c)dx^i-\rho\,d\tau$$, the equation $$\delta F_{\rm std}=4\pi J_{\rm std}$$ gives the standard source equations $$\partial_tE-c\operatorname{curl}B=-4\pi j$$ and $$\operatorname{div}E=4\pi\rho$$. Their divergence gives $$\partial_t\rho+\operatorname{div}j=0$$. The exact-potential relation in these coordinates is $$B=\operatorname{curl}A$$ and $$E=-(1/c)\partial_tA-\operatorname{grad}\Phi$$. These formulas specify all normalizations rather than treating the inconsistent printed statements as equivalent.

### Exercise 6

**(i)** An explicit choice is $$v=f\operatorname{grad}g$$. The product rule gives

$$
\operatorname{curl}(f\operatorname{grad}g)
=\operatorname{grad}f\times\operatorname{grad}g
+f\operatorname{curl}(\operatorname{grad}g)
=\operatorname{grad}f\times\operatorname{grad}g.
$$

**(ii)** When $$f$$ is nowhere zero, set $$h=\log|f|$$. The composition is smooth even if $$X$$ is disconnected, and the chain rule gives

$$
\operatorname{grad}h=\frac{\operatorname{grad}f}{f}.
$$

These explicit formulas show that contractibility is unnecessary for either assertion.

### Exercise 7

Since $$f\,df=\tfrac12d(f^2)$$, the 1-form $$\Theta(f\operatorname{grad}f)$$ is exact and hence closed. Therefore

$$
\begin{aligned}
\Theta\boldsymbol\Delta(f\operatorname{grad}f)
&=(d\delta+\delta d)(f\,df)
=d\delta(f\,df)\\
&=d\operatorname{div}(f\operatorname{grad}f)
=\Theta\operatorname{grad}\operatorname{div}(f\operatorname{grad}f).
\end{aligned}
$$

The divergence product rule yields

$$
\operatorname{div}(f\operatorname{grad}f)
=f\Delta f+|\operatorname{grad}f|_M^2.
$$

Applying the gradient product rule and combining the two equations proves

$$
\boldsymbol\Delta(f\operatorname{grad}f)
=\operatorname{grad}\operatorname{div}(f\operatorname{grad}f)
=(\Delta f)\operatorname{grad}f+\operatorname{grad}|\operatorname{grad}f|_M^2
+f\operatorname{grad}(\Delta f).
$$

The first operator is the book's Hodge-induced vector Laplacian; the proof does not assume a flat metric.

### Exercise 8

In local coordinates write $$\alpha=\sum_k a_kdx^k$$, $$v=\sum_i v^i\partial_i$$, and $$w=\sum_j w^j\partial_j$$. The exterior derivative gives

$$
d\alpha(v,w)=\sum_{i,j}v^iw^j(\partial_i a_j-\partial_j a_i).
$$

On the other hand,

$$
\begin{aligned}
L_v\langle\alpha,w\rangle-L_w\langle\alpha,v\rangle
={}&\sum_{i,j}v^iw^j(\partial_i a_j-\partial_j a_i)\\
&+\sum_j a_j\left(\sum_i v^i\partial_i w^j-w^i\partial_i v^j\right).
\end{aligned}
$$

The last parenthesis is the $$j$$-th component of $$[v,w]$$. Subtracting $$\langle\alpha,[v,w]\rangle$$ gives the required identity. Since all terms are globally defined, the local proof holds on all of $$M$$.

### Exercise 9

Let $$\varphi:M\to N$$ be a diffeomorphism. For every $$u\in C^\infty(N)$$, the definition of pushforward and the chain rule give

$$
(\varphi_*v)(u)\circ\varphi=v(u\circ\varphi).
$$

Applying this twice and subtracting in the two orders,

$$
\begin{aligned}
[\varphi_*v,\varphi_*w](u)\circ\varphi
&=v\bigl(w(u\circ\varphi)\bigr)-w\bigl(v(u\circ\varphi)\bigr)\\
&=[v,w](u\circ\varphi)
=\bigl((\varphi_*[v,w])(u)\bigr)\circ\varphi.
\end{aligned}
$$

A vector field is determined by its action on smooth functions, so $$\varphi_*[v,w]=[\varphi_*v,\varphi_*w]$$.

### Exercise 10

The printed $$S^1\times S^2\subset\mathbb R^4$$ is inconsistent with both the superscript $$T^2$$ and the coordinates. The intended torus is

$$
T^2=S^1\times S^1\subset\mathbb R^4,
\quad (x^1,x^2,x^3,x^4)=(\cos\theta,\sin\theta,\cos\varphi,\sin\varphi),
$$

with its induced product metric. On any angular chart, restriction of the two forms gives

$$
\alpha=-x^2dx^1+x^1dx^2=d\theta,\qquad
\beta=-x^4dx^3+x^3dx^4=d\varphi.
$$

The metric in these charts is $$d\theta^2+d\varphi^2$$. Thus the forms have constant coefficients and their Hodge Laplacians vanish. Equivalently, $$d\alpha=d\beta=0$$ and $$\delta\alpha=\delta\beta=0$$ in every chart. These statements glue over the torus, so

$$
\Delta\alpha=\Delta\beta=0.
$$

The symbols $$d\theta,d\varphi$$ describe global 1-forms, although the angle functions themselves cannot be chosen globally as single-valued smooth real functions on the circles.

### Exercise 11

With the book's convention $$\sigma=\sum_{j=1}^m dp_j\wedge dq_j$$,

$$
\operatorname{sgrad}H=\sum_{j=1}^m\left(-\frac{\partial H}{\partial p_j}\frac\partial{\partial q_j}
+\frac{\partial H}{\partial q_j}\frac\partial{\partial p_j}\right).
$$

The Euclidean divergence in $$(q,p)$$ coordinates is therefore

$$
\operatorname{div}(\operatorname{sgrad}H)
=\sum_{j=1}^m\left(-\frac{\partial^2H}{\partial q_j\partial p_j}
+\frac{\partial^2H}{\partial p_j\partial q_j}\right)=0
$$

by equality of mixed partial derivatives. The divergence vanishes independently of the chosen constant orientation.
