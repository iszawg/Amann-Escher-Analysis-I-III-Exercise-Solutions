# Chapter XI — Manifolds and Differential Forms

## 5. Riemannian metrics

These solutions address Exercises 1–15. Unless explicitly stated otherwise, metrics are positive definite. For hypersurfaces we use the book's sign convention $$L=d\nu$$ and $$h(v,w)=\langle d\nu(v),w\rangle$$. Several exercises need qualifications about positive definiteness, induced metrics, orientation, or connectedness; these are stated where they arise.

### Exercise 1

Let $$G=\pi_1^*g_1+\pi_2^*g_2$$. Under the canonical identification

$$
T_{(p,q)}(M_1\times M_2)\cong T_pM_1\oplus T_qM_2,
$$

we have

$$
G_{(p,q)}((v_1,v_2),(w_1,w_2))
=g_1(v_1,w_1)+g_2(v_2,w_2).
$$

**(i)** This is smooth and symmetric. If it pairs $$(v_1,v_2)$$ to zero with every $$(w_1,w_2)$$, taking the second and then the first test vector to be zero shows $$v_1=v_2=0$$ by nondegeneracy of the factors. Thus $$G$$ is a **pseudo-Riemannian** metric. It is Riemannian when both factor metrics are positive definite. The printed assertion with arbitrary pseudo-Riemannian factors is false: for instance $$g_1=-dx^2$$ and $$g_2=dy^2$$ give $$G=-dx^2+dy^2$$.

**(ii), (iii)** The maps $$p\mapsto(p,q)$$ and $$q\mapsto(p,q)$$ are smooth embeddings, with the displayed slices as images. The assumption $$\partial M_1=\varnothing$$ ensures that the product is a manifold with boundary in the book's category. Their tangent spaces are respectively $$T_pM_1\oplus\{0\}$$ and $$\{0\}\oplus T_qM_2$$; they intersect trivially and their sum is the whole tangent space, proving (iii).

**(iv)** Assume both factors are oriented and orient the product by putting a positive basis of $$M_1$$ before one of $$M_2$$. With positive orthonormal bases in the two factors, their concatenation is a positive orthonormal basis for $$G$$. Both sides of

$$
\omega_{M_1\times M_2}=\pi_1^*\omega_{M_1}\wedge\pi_2^*\omega_{M_2}
$$

evaluate to 1 on that basis, proving the identity. The same argument works for pseudo-Riemannian volume forms using pseudo-orthonormal bases and the book's normalization. Without the product orientation a sign must be supplied.

### Exercise 2

**(a)** At each point of a hypersurface, the Euclidean normal space is a line. It has exactly two unit vectors, and exactly one of them makes $$(\nu,v_1,\ldots,v_m)$$ positive for a positive tangent basis. This choice is independent of the positive basis. It also varies smoothly: in a positive coordinate chart the normalized generalized cross product of the tangent coordinate vectors gives it; on overlaps uniqueness makes the local definitions agree. Thus the positive unit normal exists and is unique.

**(b)** The orientation must be specified to determine a sign. With the upward normal for a graph and outward normals for the other examples, the following formulas hold; reversing the orientation negates them.

- For $$F(x,y)=(x,y,f(x,y))$$,
  $$\displaystyle\nu=\frac{(-f_x,-f_y,1)}{\sqrt{1+f_x^2+f_y^2}}.$$
- For $$\mathbb R\times S^1=\{(t,\cos\theta,\sin\theta)\}$$,
  $$\nu=(0,\cos\theta,\sin\theta).$$
- For $$S^2$$, $$\nu(p)=p$$.
- For the ring torus, $$0<r<a$$, use
  $$F(u,v)=((a+r\cos v)\cos u,(a+r\cos v)\sin u,r\sin v).$$
  Its outward normal is $$\nu=(\cos v\cos u,\cos v\sin u,\sin v)$$.

Indeed, the graph formula is perpendicular to $$F_x,F_y$$; the cylinder and sphere formulas are unit gradients of defining functions. For the torus,

$$
F_u\times F_v=r(a+r\cos v)\nu,
$$

so the displayed normal is unit and agrees with the parametrization's orientation.

### Exercise 3

**(i)–(iii)** By Exercise 2, $$\nu$$ is smooth and has unit length, hence it defines a smooth map $$M\to S^m$$. For $$v\in T_pM$$, differentiate $$\langle\nu,\nu\rangle=1$$ in direction $$v$$:

$$
0=2\langle (T_p\nu)v,\nu(p)\rangle.
$$

Thus $$(T_p\nu)v\in\nu(p)^\perp=T_pM$$, where both tangent spaces are identified with linear subspaces of $$\mathbb R^{m+1}$$. Consequently $$L(p)=T_p\nu$$ is an endomorphism of $$T_pM$$.

**(iv), (v)** Let $$F=i\circ\varphi^{-1}$$ and write $$\nu$$ also for its coordinate representation. Since $$\langle\nu,F_k\rangle=0$$, differentiation gives

$$
h_{jk}=\langle\partial_j\nu,F_k\rangle
=-\langle\nu,\partial_j\partial_kF\rangle.
$$

The right side is symmetric in $$j,k$$ by equality of mixed partials. Hence $$h(v,w)=h(w,v)$$ and $$L(p)$$ is self-adjoint for the induced inner product. The formula also shows the coefficients of $$h$$ are smooth, so they define a smooth covariant 2-tensor.

### Exercise 4

Use the outward normals in Exercise 2 and the upward normal for the horizontal plane. With $$h_{ij}=-\langle\nu,F_{ij}\rangle$$:

- **Plane:** $$\nu$$ is constant, so $$h=0$$.
- **Unit sphere:** $$\nu(p)=p$$, so $$d\nu=\operatorname{id}$$ on each tangent space and $$h=g_{S^2}$$.
- **Cylinder:** for $$F(t,\theta)=(t,\cos\theta,\sin\theta)$$,
  $$h=(d\theta)^2$$, since $$F_{tt}=F_{t\theta}=0$$ and $$F_{\theta\theta}=-\nu$$.
- **Ring torus:** with the parametrization of Exercise 2,

$$
h=(a+r\cos v)\cos v\,(du)^2+r\,(dv)^2.
$$

Indeed $$F_{uu}=(-(a+r\cos v)\cos u,-(a+r\cos v)\sin u,0)$$, $$F_{vv}=-r\nu$$, and $$F_{uv}$$ is orthogonal to $$\nu$$. For reference the first fundamental form is $$(a+r\cos v)^2(du)^2+r^2(dv)^2$$. All these second fundamental forms change sign if the chosen normal is reversed. The angular formulas are local and agree on overlapping charts.

### Exercise 5

The stated equality requires $$g=i^*\langle\cdot,\cdot\rangle$$, the metric induced by the indicated Euclidean embedding. In that case the chain rule gives

$$
\dot{\widetilde\gamma}(t)=T_{\gamma(t)}i\,\dot\gamma(t),\qquad
|\dot{\widetilde\gamma}(t)|^2=g_{\gamma(t)}(\dot\gamma(t),\dot\gamma(t)).
$$

Integrating the nonnegative square roots yields the desired equality. For an arbitrary Riemannian metric, the right side defines intrinsic length, but need not equal the Euclidean length of this embedding. For example, take $$M=\mathbb R$$ with $$g=4dx^2$$, its usual embedding, and $$\gamma(t)=t$$ on $$[0,1]$$. The Euclidean length is 1 and the metric length is 2.

Also, equality of the total length with $$|I|$$ alone does not imply unit speed at every point. The usual local notion of arc-length parametrization requires $$g(\dot\gamma,\dot\gamma)=1$$, equivalently equality of length with parameter difference on every subinterval.

### Exercise 6

Use the usual **unit-speed** interpretation and the positive normal of the chosen orientation. In the plane with its standard orientation, $$\nu=e_3$$ and

$$
\det(\dot\gamma,\ddot\gamma,\nu)=\dot x\,\ddot y-\dot y\,\ddot x,
$$

the usual signed planar curvature of a unit-speed curve. Reversing the plane's orientation reverses this sign.

For the sphere take its outward orientation, $$b=\sqrt{1-z^2}>0$$, and

$$
\gamma(s)=(b\cos(s/b),b\sin(s/b),z),\quad
\dot\gamma=(-\sin(s/b),\cos(s/b),0),\quad
\ddot\gamma=-\frac1b(\cos(s/b),\sin(s/b),0).
$$

Since $$\nu=\gamma$$,

$$
\kappa_g=\det(\dot\gamma,\ddot\gamma,\gamma)=\frac zb.
$$

This is constant and is zero on the equator. Reversing the direction of traversal changes its sign, so the printed formula needs the displayed direction (or an equivalent orientation convention). Reversing the normal also changes the sign.

The book's preceding definition based only on equality of total lengths is weaker than unit speed. For example, on the same circle and $$I=[0,2\pi b]$$, replace $$s/b$$ by $$s/b+\varepsilon\sin(s/b)$$ with $$0<\varepsilon<1$$. The resulting curve traverses the circle once and has total length $$2\pi b=|I|$$, but its speed is $$1+\varepsilon\cos(s/b)$$ and the determinant in the exercise is multiplied by its cube. Thus the displayed constant-curvature claim also needs the unit-speed assumption.

### Exercise 7

Put $$n=m+1$$, $$R=|x|$$, $$y_i=x_i/R$$, and $$\Omega=dx_1\wedge\cdots\wedge dx_n$$. The sphere form is the restriction of $$\sum_i(-1)^{i-1}y_i\,dy_1\wedge\cdots\wedge\widehat{dy_i}\wedge\cdots\wedge dy_n$$. Direct differentiation gives

$$
dy_j=R^{-1}dx_j-R^{-3}x_j\sum_kx_k\,dx_k.
$$

We compute each coefficient explicitly. Let $$J=(1,\ldots,\widehat i,\ldots,n)$$, let $$e_j$$ be the standard basis, and put $$u=x/R$$. Since

$$
D\rho_x(e_j)=R^{-1}\left(e_j-\frac{x_j}{R^2}x\right),
$$

the coefficient of $$dx_J$$ in the pullback is the determinant

$$
\begin{aligned}
(\rho^*\omega_{S^{n-1}})_x(e_{j_1},\ldots,e_{j_{n-1}})
&=\det\bigl(u,D\rho_x e_{j_1},\ldots,D\rho_x e_{j_{n-1}}\bigr)\\
&=R^{-n}\det\left(x,e_{j_1}-\frac{x_{j_1}}{R^2}x,\ldots,
 e_{j_{n-1}}-\frac{x_{j_{n-1}}}{R^2}x\right)\\
&=R^{-n}\det(x,e_{j_1},\ldots,e_{j_{n-1}}).
\end{aligned}
$$

In the last step, multilinearity shows that every term containing one of the correction vectors is zero: it then has two columns proportional to $$x$$. Expanding the remaining determinant along its first column leaves only the $$i$$th component, with cofactor sign $$(-1)^{i+1}=(-1)^{i-1}$$. Thus its value is $$(-1)^{i-1}x_i$$, and

$$
\rho^*\omega_{S^{n-1}}=R^{-n}\sum_{i=1}^n(-1)^{i-1}x_i\,
 dx_1\wedge\cdots\wedge\widehat{dx_i}\wedge\cdots\wedge dx_n.
$$

For the two requested cases this reads

$$
\rho^*\omega_{S^2}=\frac{x_1dx_2\wedge dx_3-x_2dx_1\wedge dx_3+x_3dx_1\wedge dx_2}{R^3},
$$

and

$$
\rho^*\omega_{S^3}=\frac{x_1dx_2\wedge dx_3\wedge dx_4-x_2dx_1\wedge dx_3\wedge dx_4+x_3dx_1\wedge dx_2\wedge dx_4-x_4dx_1\wedge dx_2\wedge dx_3}{R^4}.
$$

### Exercise 8

Let $$i:M\hookrightarrow\mathbb R^N$$ and $$F=i\circ\varphi^{-1}$$ for a chart $$\varphi:U\to\varphi(U)$$. If $$y^1,\ldots,y^N$$ are Euclidean coordinates, then

$$
(\varphi^{-1})^*g=F^*\!\left(\sum_{a=1}^Ndy^a\otimes dy^a\right)
=\sum_{a=1}^N dF^a\otimes dF^a.
$$

Writing $$dF^a=\sum_j(\partial_jF^a)dx^j$$ gives

$$
(\varphi^{-1})^*g=\sum_{j,k}\left(\sum_a\partial_jF^a\partial_kF^a\right)dx^j\otimes dx^k
=\sum_{j,k}\langle F_j,F_k\rangle\,dx^j\otimes dx^k.
$$

Because $$F$$ is an immersion, its derivative is injective; hence $$\sum_{j,k}g_{jk}v^jv^k=|\sum_jv^jF_j|^2>0$$ for nonzero $$v$$. The coefficients are smooth, proving that this is a Riemannian metric. Its determinant is the Gram determinant in Proposition 5.1, so the positive-coordinate volume form is $$\sqrt{\det(g_{jk})}\,dx^1\wedge\cdots\wedge dx^m$$.

The claim of independence of ambient space is valid when the two ambient realizations are related by a Euclidean isometric inclusion, such as adjoining zero coordinates. It does not apply to an arbitrary change of embedding: $$x\mapsto x$$ and $$x\mapsto(x,x^2)$$ induce $$dx^2$$ and $$(1+4x^2)dx^2$$ respectively on $$\mathbb R$$.

### Exercise 9

Let $$z=x+iy$$ with $$y>0$$, and $$C(z)=(1+iz)/(1-iz)$$. Since

$$
|1-iz|^2-|1+iz|^2=4y>0,
$$

we have $$|C(z)|<1$$. Solving for $$z$$ gives

$$
C^{-1}(w)=i\frac{1-w}{1+w},\qquad
\operatorname{Im} C^{-1}(w)=\frac{1-|w|^2}{|1+w|^2}>0.
$$

Both formulas are smooth on their domains, so $$C$$ is a diffeomorphism onto the unit disk. Moreover

$$
C'(z)=\frac{2i}{(1-iz)^2},\qquad
1-|C(z)|^2=\frac{4y}{|1-iz|^2}.
$$

Thus, writing $$w=u+iv$$,

$$
C^*\!\left(\frac{4(du^2+dv^2)}{(1-u^2-v^2)^2}\right)
=\frac{dx^2+dy^2}{y^2}.
$$

The disk metric is the Poincaré disk metric from Example 5.5(l), already shown to be isometric to the hyperboloid. Therefore the upper half-plane with the indicated metric is another model of the hyperbolic plane. The text calls it the “Klein model”; in standard terminology it is the Poincaré upper half-plane model, while the Klein disk uses different coordinates and a different metric.

### Exercise 10

For $$\chi>0$$ and angle $$\varphi\pmod{2\pi}$$, let

$$
F(\chi,\varphi)=(\cosh\chi,\sinh\chi\cos\varphi,\sinh\chi\sin\varphi).
$$

It lies on the upper sheet of $$t^2-x^2-y^2=1$$. With the metric $$g_H=-dt^2+dx^2+dy^2$$ induced on that sheet,

$$
g_H(F_\chi,F_\chi)=1,\qquad
g_H(F_\chi,F_\varphi)=0,\qquad
g_H(F_\varphi,F_\varphi)=\sinh^2\chi.
$$

Hence $$F^*g_H=d\chi^2+\sinh^2\chi\,d\varphi^2$$. For $$\chi>0$$ this is a diffeomorphism from $$(0,\infty)\times S^1$$ onto the hyperboloid with its vertex $$(1,0,0)$$ removed.

To obtain the **whole** hyperbolic plane, one must include the vertex and collapse all angles at $$\chi=0$$. More explicitly, define a map on $$\mathbb R^2$$ by

$$
H(0)=(1,0,0),\qquad
H(u)=(\cosh|u|,\,\frac{\sinh|u|}{|u|}u)\quad(u\ne0).
$$

The power series of $$\cosh|u|$$ and $$\sinh|u|/|u|$$ show smoothness at zero; the inverse is $$u=(\operatorname{arsinh}|x|/|x|)x$$, also smoothly extended at zero. Thus $$H$$ is a global diffeomorphism onto the upper hyperboloid, and its pulled-back metric is smooth and positive definite, with the displayed polar expression away from the origin. The literal half-open angular interval in the book needs this periodic identification and the collapse at the vertex; as an ordinary product it is not a global model.

### Exercise 11

The book's convention is

$$
\delta\beta=(-1)^{m(r+1)}*d*\beta,\qquad
*\delta\beta=(-1)^{r+1}d*\beta
$$

for $$\deg\beta=r$$. The second equality follows from $$*^2=(-1)^{s(m-s)}$$ on $$s$$-forms, applied with $$s=m-r+1$$. By the graded product rule,

$$
\begin{aligned}
d(\alpha\wedge*\beta)
&=d\alpha\wedge*\beta+(-1)^{r-1}\alpha\wedge d*\beta\\
&=d\alpha\wedge*\beta+\alpha\wedge*\delta\beta,
\end{aligned}
$$

because $$(-1)^{r-1}=(-1)^{r+1}$$. The formula uses the book's sign convention for $$\delta$$; a common alternative defines the negative operator. For $$r=0$$ the convention $$\Omega^{-1}=0$$ makes the statement trivial.

### Exercise 12

Reversing the orientation changes the volume form to its negative. The defining relation of the Hodge star therefore changes $$*$$ to $$-*$$ in every degree. The book's formula for $$\delta$$ contains the Hodge star twice, so the two minus signs cancel:

$$
\delta_{-\mathrm{or}}\beta=(-1)^{m(r+1)}(-*)d(-*)\beta=\delta_{\mathrm{or}}\beta.
$$

More generally, two orientations may differ by a locally constant sign $$\varepsilon:M\to\{\pm1\}$$ on a disconnected manifold. Then $$*'\beta=\varepsilon*\beta$$ and $$d\varepsilon=0$$, so the same calculation proves $$\delta'=\delta$$.

### Exercise 13

At each $$p\in M$$ the differential $$T_pf$$ is a linear isometry. Therefore it takes an orthonormal basis to an orthonormal basis, and

$$
f^*\omega_N=\varepsilon\,\omega_M,\qquad \varepsilon(p)\in\{1,-1\}.
$$

The smooth ratio $$\varepsilon=(f^*\omega_N)/\omega_M$$ is locally constant and equals the orientation sign of $$T_pf$$. Hence $$f^*\omega_N=\omega_M$$ exactly when $$f$$ preserves orientation at every point. If $$M$$ is connected, $$\varepsilon$$ is constant and the displayed equality has one global choice of sign.

Without connectedness a single global sign need not exist. For example, take $$M=N=(-2,-1)\cup(1,2)$$ with the Euclidean metric and standard orientation. Let $$f(x)=-3-x$$ on the first component and $$f(x)=x$$ on the second. This is an isometric diffeomorphism, but its orientation sign is negative on the first component and positive on the second. The printed $$\pm$$ statement therefore requires connectedness or means a componentwise sign.

### Exercise 14

Let $$f:M\to N$$ be orientation-preserving and isometric. Its pullback preserves the induced inner product on forms and, by Exercise 13, $$f^*\omega_N=\omega_M$$. For arbitrary $$r$$-forms $$\alpha,\beta$$ on $$N$$,

$$
\begin{aligned}
f^*\alpha\wedge f^*(*_N\beta)
&=f^*(\alpha\wedge *_N\beta)\\
&=f^*(\langle\alpha,\beta\rangle_N\omega_N)\\
&=\langle f^*\alpha,f^*\beta\rangle_M\omega_M\\
&=f^*\alpha\wedge *_M(f^*\beta).
\end{aligned}
$$

At each point, as $$\alpha$$ varies, $$f^*\alpha$$ ranges over all $$r$$-covectors. The wedge pairing between degrees $$r$$ and $$m-r$$ is nondegenerate, so

$$
\boxed{f^*(*_N\beta)=*_M(f^*\beta).}
$$

This includes degrees 0 and $$m$$ and proves the commutative diagram.

### Exercise 15

Let $$f:M\to N$$ be an isometric diffeomorphism, without assuming it preserves orientation. By Exercise 13, write $$f^*\omega_N=\varepsilon\omega_M$$ with $$\varepsilon$$ locally constant and $$\varepsilon^2=1$$. Repeating the argument of Exercise 14 gives, in every degree,

$$
f^*(*_N\eta)=\varepsilon\,*_M(f^*\eta).
$$

For an $$r$$-form $$\beta$$, naturality of $$d$$ and $$d\varepsilon=0$$ imply

$$
\begin{aligned}
f^*(\delta_N\beta)
&=(-1)^{m(r+1)}f^*(*_N d *_N\beta)\\
&=(-1)^{m(r+1)}\varepsilon *_M d\bigl(\varepsilon *_M f^*\beta\bigr)\\
&=(-1)^{m(r+1)}*_M d *_M f^*\beta
=\delta_M(f^*\beta).
\end{aligned}
$$

Thus the diagram commutes, even when $$f$$ reverses orientation on some components. For $$r=0$$ both sides are zero by the book's convention.
