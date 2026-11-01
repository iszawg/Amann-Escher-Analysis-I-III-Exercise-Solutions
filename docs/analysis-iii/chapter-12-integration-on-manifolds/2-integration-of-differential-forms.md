# Chapter XII — Integration on Manifolds

## 2. Integration of differential forms

These solutions address Exercises 1–6. We use $$\iota_v$$ for contraction with $$v$$ and $$\mathcal L_v$$ for the Lie derivative. Unless otherwise stated, a flow is assumed to exist for all times; compact support guarantees this on a manifold **without boundary**. With boundary, the vector field must also generate a flow preserving the boundary.

### Exercise 1

The printed conclusion needs a factor $$f$$: under the hypotheses the correct statement is

$$
\boxed{\lim_{j\to\infty}\int_M f_j\omega=\int_M f\omega.}
$$

Indeed, write $$\omega=a\omega_M$$, where $$\omega_M$$ is the volume form and $$a\in L^1(M,\lambda_M)$$. Because the sequence is countable and its essential suprema are uniformly bounded, there is a single null set outside which $$|f_j|\le C$$ for every $$j$$ and $$f_j\to f$$. There, $$|f|\le C$$ and

$$
|f_ja-fa|\le2C|a|\in L^1(M,\lambda_M),\qquad f_ja\to fa.
$$

The dominated convergence theorem therefore gives the displayed formula; in fact $$\int_M|f_j-f|\,|a|\,d\lambda_M\to0$$.

The conclusion as printed, with $$\int_M\omega$$ on the right, is false. For example, take $$M=S^1$$ with its positive volume form and $$f_j=f=0$$. Every left-hand integral is zero, while $$\int_M\omega=2\pi$$. The printed conclusion follows if, for instance, $$f=1$$ almost everywhere.

### Exercise 2

Use the outward orientation of the sphere $$M=a+RS^2$$, where $$a=(a_1,a_2,a_3)$$. At $$p=a+Rn$$, $$|n|=1$$, the form

$$
\omega=x^2\,dy\wedge dz+y^2\,dz\wedge dx+z^2\,dx\wedge dy
$$

is the flux form of $$V=(x^2,y^2,z^2)$$. Hence its restriction is $$(V\cdot n)dS$$, with

$$
V\cdot n=\sum_{i=1}^3(a_i+Rn_i)^2n_i.
$$

By reflection symmetry, $$\int_{S^2}n_i\,dS=\int_{S^2}n_i^3\,dS=0$$. Rotational symmetry and $$\sum_i n_i^2=1$$ give $$\int_{S^2}n_i^2\,dS=4\pi/3$$. Since the radius-$$R$$ area element is $$R^2dS$$,

$$
\boxed{\int_M\omega=\frac{8\pi R^3}{3}(a_1+a_2+a_3).}
$$

The opposite orientation reverses the answer. As a check, the divergence of $$V$$ is $$2(x+y+z)$$; integrating it over the ball gives the same expression.

### Exercise 3

Let $$\chi_t$$ be the flow of $$v$$. For every $$p\in M$$, the chain rule and the flow equation give

$$
\frac{d}{dt}(\chi_t^*f)(p)
=\frac{d}{dt}f(\chi_t(p))
=(df)_{\chi_t(p)}v(\chi_t(p))
=\chi_t^*(\mathcal L_vf)(p).
$$

If the derivative is zero, $$\chi_t^*f$$ is constant in $$t$$ and equals $$f$$ at $$t=0$$, proving (i) implies (ii). Differentiating (ii) at zero gives (iii). Finally, if $$\mathcal L_vf=0$$, the displayed equation gives (i). Thus all three statements are equivalent.

The proof only uses the existence of the flow for the times in question. In particular, compact support alone does not give a two-sided flow on an arbitrary manifold with boundary: on $$[0,\infty)$$, a compactly supported field equal to $$\partial_x$$ near 0 immediately leaves the manifold in negative time.

### Exercise 4

The book uses

$$
\sigma=\sum_{j=1}^n dp_j\wedge dq_j,\qquad
\{f,H\}=\sum_j(f_{p_j}H_{q_j}-f_{q_j}H_{p_j}).
$$

Consequently

$$
\operatorname{sgrad}H
=\sum_j\left(-H_{p_j}\frac\partial{\partial q_j}+H_{q_j}\frac\partial{\partial p_j}\right)
$$

and, for any smooth $$f$$,

$$
\mathcal L_{\operatorname{sgrad}H}f
=\sum_j(-H_{p_j}f_{q_j}+H_{q_j}f_{p_j})=\{f,H\}.
$$

Exercise 3 therefore proves the equivalence. The compact support of $$H$$ makes its symplectic gradient compactly supported and hence complete on $$\mathbb R^{2n}$$. Finally, $$\{H,H\}=0$$ by antisymmetry, so $$H$$ is a first integral of its own symplectic gradient.

### Exercise 5

Let $$\chi_t$$ be the flow of $$v$$. The results below hold for a complete field, and locally for any smooth field wherever its flow is defined.

**(i)** Pullback preserves form degree and depends smoothly on $$t$$, so differentiating at zero produces an $$r$$-form when $$\alpha$$ has degree $$r$$. For a function $$f$$,

$$
\mathcal L_vf=\left.\frac d{dt}f\circ\chi_t\right|_{t=0}=df(v)=v(f),
$$

the previous definition.

**(ii), (iii)** Each pullback commutes with $$d$$ and preserves the exterior product. Differentiating these identities at $$t=0$$ gives

$$
\mathcal L_v(d\alpha)=d(\mathcal L_v\alpha),\qquad
\mathcal L_v(\alpha\wedge\beta)=(\mathcal L_v\alpha)\wedge\beta+\alpha\wedge(\mathcal L_v\beta).
$$

**(iv)** We prove Cartan's formula locally. Both $$\mathcal L_v$$ and $$D=d\iota_v+\iota_vd$$ are degree-zero derivations of the exterior algebra: the graded product rules for $$d$$ and $$\iota_v$$ make the cross terms cancel. On functions $$f$$,

$$
Df=\iota_vdf=v(f)=\mathcal L_vf.
$$

Both operators commute with $$d$$; for $$D$$ this follows from $$d^2=0$$. Thus they also agree on coordinate differentials $$dx^i=d(x^i)$$. Since local forms are sums of products of functions and coordinate differentials, the derivation property proves

$$
\boxed{\mathcal L_v\alpha=d(\iota_v\alpha)+\iota_v(d\alpha).}
$$

The local identities agree on overlaps and hence hold globally.

**(v)** A volume form has top degree, so $$d\omega_M=0$$. By (iv) and the definition of divergence,

$$
\mathcal L_v\omega_M=d(\iota_v\omega_M)=(\operatorname{div}v)\omega_M.
$$

**(vi): the printed identity is false for a general metric.** The correct identity is

$$
\boxed{\mathcal L_v(\Theta w)=\Theta[v,w]+(\mathcal L_vg)(w,\cdot).}
$$

To see this, evaluate both sides on any vector field $$u$$. Differentiating the tensorial pullback gives

$$
(\mathcal L_v(\Theta w))(u)
=v(g(w,u))-g(w,[v,u])
=(\mathcal L_vg)(w,u)+g([v,w],u).
$$

Thus the printed equality follows whenever $$\mathcal L_vg=0$$, for example when $$v$$ is a Killing field; for a fixed $$w$$ the weaker condition $$(\mathcal L_vg)(w,\cdot)=0$$ suffices.

For a compactly supported counterexample, take $$M=\mathbb R$$ with $$g=dx^2$$, choose a smooth compactly supported $$\eta$$ equal to 1 near zero, and set $$v=\eta x\partial_x$$, $$w=\eta\partial_x$$. Near zero,

$$
\Theta[v,w]=-dx,\qquad \mathcal L_v(\Theta w)=\mathcal L_{x\partial_x}dx=dx.
$$

The two sides are different.

### Exercise 6

A flow solves $$\dot x=v(x)$$ with its indicated initial point. We write the initial point as $$(x_0,y_0)$$ or $$(x_0,y_0,z_0)$$. The linear cases below have solutions for all $$t\in\mathbb R$$.

**(i)** The equations $$\dot x=x$$, $$\dot y=y$$ give the dilation flow

$$
\chi_t(x_0,y_0)=e^t(x_0,y_0).
$$

**(ii)** The equations $$\dot x=-y$$, $$\dot y=x$$ give counterclockwise rotation:

$$
\chi_t(x_0,y_0)=(x_0\cos t-y_0\sin t,\ x_0\sin t+y_0\cos t).
$$

**(iii)** The same rotation acts in the $$xy$$-plane while the height is fixed:

$$
\chi_t(x_0,y_0,z_0)=(x_0\cos t-y_0\sin t,\ x_0\sin t+y_0\cos t,\ z_0).
$$

**(iv)** The coefficient matrix is $$I+J$$, where $$J=\begin{pmatrix}0&-1\\1&0\end{pmatrix}$$. Since $$I$$ and $$J$$ commute, $$e^{t(I+J)}=e^t e^{tJ}$$, so

$$
\chi_t(x_0,y_0)=e^t(x_0\cos t-y_0\sin t,\ x_0\sin t+y_0\cos t).
$$

**(v)** The equations are $$\dot x=x+y$$, $$\dot y=x^2$$. This vector field is not complete, so there is no global flow on all of $$\mathbb R^2$$. Its maximal local flow is specified by

$$
x''=x'+x^2,\qquad x(0)=x_0,\quad x'(0)=x_0+y_0,\qquad y=x'-x.
$$

For an explicit local description, write $$x(t)=\sum_{k\ge0}a_kt^k$$. Substitution gives the convergent local power series with

$$
a_0=x_0,\qquad a_1=x_0+y_0,\qquad
 a_{k+2}=\frac{(k+1)a_{k+1}+\sum_{j=0}^k a_ja_{k-j}}{(k+2)(k+1)}.
$$

The analytic ODE theorem guarantees convergence near zero; unique continuation gives the maximal solution. The origin is an equilibrium. To see finite-time blow-up, take $$(x_0,y_0)=(1,0)$$. Then $$x(0)=x'(0)=1$$ and $$x''=x'+x^2>0$$ as long as the solution exists, so $$x,x'>0$$. Multiplying $$x''\ge x^2$$ by $$2x'$$ and integrating yields

$$
(x')^2\ge1+\frac23(x^3-1).
$$

Consequently, while the solution exists,

$$
t\le\int_1^{x(t)}\frac{du}{\sqrt{1+\frac23(u^3-1)}}
<\int_1^\infty\frac{du}{\sqrt{1+\frac23(u^3-1)}}<\infty.
$$

A global solution would have $$x(t)\ge1+t$$ and eventually violate this finite bound. On a finite time interval a bounded $$x$$ also bounds $$x'$$ by the linear inequality $$x''\le x'+C$$, so the continuation theorem shows that $$x$$ must diverge at the finite maximal time.

**(vi)** Let $$A=\begin{pmatrix}1&1\\1&-1\end{pmatrix}$$. Since $$A^2=2I$$,

$$
e^{tA}=\cosh(\sqrt2t)I+\frac{\sinh(\sqrt2t)}{\sqrt2}A.
$$

Writing $$C=\cosh(\sqrt2t)$$ and $$S=\sinh(\sqrt2t)/\sqrt2$$, and solving $$\dot z=z$$, we get

$$
\boxed{\chi_t(x_0,y_0,z_0)=\bigl((C+S)x_0+Sy_0,\ Sx_0+(C-S)y_0,\ e^tz_0\bigr).}
$$
