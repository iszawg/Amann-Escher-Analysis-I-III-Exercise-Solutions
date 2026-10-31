# Chapter VIII — Line Integrals

## 5. Holomorphic functions

These solutions cover Exercises 1–18. We write $$D(a,r)=\{z:|z-a|<r\}$$ and orient circles counterclockwise. Inline formulas use GitBook's double-dollar syntax. Exercises 3(b), 15(c), 17(b)'s hint, and 18 need qualifications about their printed wording.

### Exercise 1

Write $$f=u+iv$$ and put $$A=\partial_W f=(f_x-if_y)/2$$ and $$B=\bar\partial_W f=(f_x+if_y)/2$$.

(a) Complex conjugation commutes with real differentiation, so $$\bar\partial_W\bar f=\overline{\partial_W f}$$ and $$\partial_W\bar f=\overline{\bar\partial_W f}$$.

(b) Real differentiability gives $$f(z+h)-f(z)=Ah+B\bar h+o(|h|)$$. The quotient by $$h$$ has the same limit along the real and imaginary axes exactly when $$B=0$$; in that case it tends to $$A$$. This is the Cauchy–Riemann criterion.

(c) If the second real derivatives exist and the mixed derivatives commute (in particular for $$C^2$$ functions), expansion yields

$$
4\partial_W\bar\partial_W f=(\partial_x-i\partial_y)(\partial_x+i\partial_y)f=f_{xx}+f_{yy}=\Delta f,
$$

and the operators commute. The same conclusion for a merely twice Fréchet differentiable function follows from symmetry of its second derivative.

(d) From $$A=(u_x+v_y+i(v_x-u_y))/2$$ and $$B=(u_x-v_y+i(v_x+u_y))/2$$,

$$
|A|^2-|B|^2=u_xv_y-u_yv_x
=\det\begin{pmatrix}u_x&u_y\\v_x&v_y\end{pmatrix}
=\det\begin{pmatrix}A&B\\\bar B&\bar A\end{pmatrix}.
$$

### Exercise 2

Since $$z=x+iy$$ and $$\bar z=x-iy$$, their real differentials are $$dz=dx+i\,dy$$ and $$d\bar z=dx-i\,dy$$. Hence $$dx=(dz+d\bar z)/2$$ and $$dy=(dz-d\bar z)/(2i)$$. Substitution gives

$$
df=f_x\,dx+f_y\,dy=(\partial_W f)\,dz+(\bar\partial_W f)\,d\bar z.
$$

Here $$f'\,dz$$ in the holomorphic case means the real differential, because $$\bar\partial_W f=0$$ and $$f'=\partial_W f$$.

### Exercise 3

(a) In this exercise $$C^1(V,\mathbb C)$$ in the local primitive and in (iii) denotes complex continuously differentiable functions. If $$\alpha=df$$ locally with such an $$f$$, then $$\alpha=f'\,dz$$; uniqueness of the coefficient makes these local derivatives agree, defining a holomorphic $$a$$ on $$U$$. Thus (i) implies (iii).

If (iii) holds, $$a$$ is real differentiable and Cauchy–Riemann gives $$a_y=ia_x$$. Consequently

$$
d(a\,dz)=d(a\,dx+ia\,dy)=(ia_x-a_y)\,dx\wedge dy=0,
$$

which is (ii). Conversely, if (ii) holds, closedness gives $$a_y=ia_x$$, so $$a$$ is holomorphic by Exercise 1. Every point has a disc contained in $$U$$; on that disc the Cauchy integral theorem gives a primitive $$F$$ of $$a$$. Then $$dF=a\,dz=\alpha$$, proving (i). Equivalently, the local Poincaré lemma applies to the closed form and its primitive satisfies the Cauchy–Riemann equations.

(b) Direct multiplication shows $$\alpha=dz/z$$ on $$\mathbb C^\times$$. Its coefficient is holomorphic, so (a) applies. But

$$
\int_{|z|=1}\alpha=\int_0^{2\pi}i\,dt=2\pi i\ne0,
$$

so no single-valued global primitive $$F$$ with $$dF=\alpha$$ exists. The printed question says instead $$\alpha=f\,dz$$: literally that equality holds with $$f(z)=1/z$$, and is not the definition of global exactness. The intended primitive equation is $$\alpha=df=f'\,dz$$.

### Exercise 4

(a) Since $$u$$ is harmonic, its first partials are continuously differentiable. The equations $$v_x=-u_y$$ and $$v_y=u_x$$ therefore make $$v\in C^2$$, and

$$
\Delta v=-u_{yx}+u_{xy}=0.
$$

(b) The function $$g=u_x-iu_y$$ is holomorphic: its Cauchy–Riemann equations are $$u_{xx}=-u_{yy}$$ and $$-u_{yx}=-u_{xy}$$. On simply connected $$U$$ it has a primitive $$F=p+iq$$. Since $$F'=g$$, we have $$p_x=u_x$$ and $$p_y=u_y$$. Connectedness makes $$p-u$$ constant; adding a real constant to $$F$$ makes $$p=u$$. The Cauchy–Riemann equations then give $$q_x=-u_y$$ and $$q_y=u_x$$, so $$v=q$$ is the required harmonic conjugate. Any two differ by a real constant.

### Exercise 5

Suppose $$f_n$$ is holomorphic on $$U$$ and converges locally uniformly to $$f$$. Fix $$z_0\in U$$ and choose $$R>0$$ with $$\overline{D(z_0,R)}\subset U$$. Uniform convergence on the circle permits passage to the limit in Cauchy's formula:

$$
f(z)=\frac1{2\pi i}\int_{|w-z_0|=R}\frac{f(w)}{w-z}\,dw,\qquad |z-z_0|<R.
$$

The right-hand side is holomorphic in the disc, by differentiating the kernel under the integral (uniformly on smaller discs). Thus $$f$$ is holomorphic on $$U$$. Moreover, for every integer $$k\ge0$$ and $$|z-z_0|\le r<R$$,

$$
|f_n^{(k)}(z)-f^{(k)}(z)|\le
\frac{k!R}{(R-r)^{k+1}}\max_{|w-z_0|=R}|f_n(w)-f(w)|\longrightarrow0.
$$

Finitely many such smaller discs cover any compact subset of $$U$$, proving locally uniform convergence of every derivative.

### Exercise 6

Let $$d=|z-z_0|<r$$ and choose $$0<\varepsilon<\min\{\delta,r-d\}$$. Move the center of the outer circle from $$z_0$$ to $$z$$ while shrinking its radius:

$$
H(t,\theta)=z+(1-t)(z_0-z)+(r-td)e^{i\theta},\qquad 0\le t\le1.
$$

Each circle lies in the closed original disc, hence in $$U$$, and avoids $$z$$ because $$r-td>(1-t)d$$. It ends at the circle centered at $$z$$ with radius $$r-d$$. Shrink this circle to radius $$\varepsilon$$ within the original disc. Independently shrink the radius-$$\delta$$ circle to $$\varepsilon$$ inside $$D(z,\delta)$$. Concatenating these free homotopies proves the claim in $$U\setminus\{z\}$$.

### Exercise 7

For $$R>1$$ integrate $$g(z)=1/(z+i)$$ around the upper semicircle of radius $$R$$, including the diameter from $$-R$$ to $$R$$. Cauchy's formula at $$i$$ gives

$$
\int_{-R}^{R}\frac{dx}{1+x^2}+\int_{C_R}\frac{dz}{1+z^2}
=\frac{2\pi i}{2i}=\pi.
$$

On the arc $$|1+z^2|\ge R^2-1$$ and its length is $$\pi R$$, so the arc integral tends to zero. Passing to the limit yields $$\int_{-\infty}^{\infty}(1+x^2)^{-1}dx=\pi$$.

### Exercise 8

Put $$S=\sum_{k=0}^{n-1}|a_k|$$. For $$|z|\ge R=\max\{1,2S\}$$,

$$
\left|\sum_{k=0}^{n-1}a_kz^k\right|
\le S|z|^{n-1}\le\tfrac12|z|^n.
$$

The reverse and ordinary triangle inequalities give $$|z|^n/2\le|p(z)|\le3|z|^n/2\le2|z|^n$$. The constant polynomial case is immediate.

### Exercise 9

Set $$M_r=\max_{|w-z_0|=r}|f(w)|$$. For $$|z-z_0|<r_0$$, Cauchy's derivative formula and $$|w-z|\ge r-r_0$$ yield

$$
|f^{(n)}(z)|\le\frac{n!}{2\pi}\frac{2\pi rM_r}{(r-r_0)^{n+1}}
=\frac{rn!}{(r-r_0)^{n+1}}M_r.
$$

The same estimate holds on the closed smaller disc when relevant.

### Exercise 10

For every $$s>R$$, Cauchy's estimate at zero and the growth assumption give

$$
|f^{(k)}(0)|\le\frac{k!}{s^k}\max_{|z|=s}|f(z)|\le k!M s^{n-k}.
$$

Letting $$s\to\infty$$ shows $$f^{(k)}(0)=0$$ for each $$k>n$$. The Taylor expansion of an entire function therefore reduces to a polynomial of degree at most $$n$$ (including the zero polynomial).

### Exercise 11

Choose piecewise $$C^1$$ parametrizations $$\gamma_j:[a_j,b_j]\to U$$. After splitting the intervals at their finitely many corners, both iterated contour integrals become the same finite sum of integrals over rectangles with integrand

$$
f(\gamma_1(s),\gamma_2(t))\gamma_1'(s)\gamma_2'(t).
$$

This integrand is continuous on each rectangle. Fubini's theorem for continuous functions permits interchange of the real integrations, proving the equality with the specified orientations.

### Exercise 12

Continuity of $$f$$ and compactness of $$\Gamma$$ imply continuity of $$F$$ by uniform continuity on the curve times a small closed disc. If $$T$$ is any triangle with closure in $$U$$, Exercise 11 and Cauchy's theorem give

$$
\int_{\partial T}F(z)\,dz
=\int_\Gamma\left(\int_{\partial T}f(w,z)\,dz\right)dw=0.
$$

Morera's theorem makes $$F$$ holomorphic. To identify its derivative, choose a circle $$C$$ around a given $$z$$ inside $$U$$. Cauchy's formula gives, uniformly for $$w\in\Gamma$$ and small $$h$$,

$$
\frac{f(w,z+h)-f(w,z)}h
=\frac1{2\pi i}\int_C\frac{f(w,\zeta)}{(\zeta-z-h)(\zeta-z)}\,d\zeta
\longrightarrow \partial_2f(w,z).
$$

The uniform convergence permits the limit through the integral over $$\Gamma$$, and $$F'(z)=\int_\Gamma\partial_2 f(w,z)\,dw$$.

### Exercise 13

We may assume $$b\ne0$$. By Morera it is enough to show the integral around every triangle $$T$$ whose closure lies in $$U$$ is zero. If $$T$$ lies entirely on one side of $$L$$, this follows by translating the triangle slightly into that open half-plane and taking a uniform-continuity limit; a triangle contained in $$L$$ is degenerate.

If the line crosses the triangle, cut $$T$$ along $$L$$ into at most two polygons, then triangulate them. Each resulting triangle lies in one closed half-plane, so its integral is zero by the preceding argument. The internal oriented edges cancel, leaving $$\int_{\partial T}f\,dz=0$$. Morera proves holomorphy on all of $$U$$. If $$b=0$$, $$L$$ is a point and the same translation argument applies to triangles, or the removable singularity theorem applies.

### Exercise 14

(a) If the minimum at $$z_0$$ is nonzero, $$f$$ has no zeros in $$U$$ and $$1/f$$ is holomorphic. Its modulus has a global maximum at $$z_0$$. The maximum principle and connectedness make $$1/f$$, hence $$f$$, constant.

(b) Suppose there is no zero in $$U$$. Since $$\overline U$$ is compact and $$|f|$$ is continuous, its minimum occurs at some $$z_0\in\overline U$$. If $$z_0\in\partial U$$ we are done. If $$z_0\in U$$, part (a) makes $$f$$ constant in $$U$$; continuity makes it the same constant on $$\overline U$$, so the minimum is also attained on the nonempty boundary.

### Exercise 15

Let $$|\zeta|=R$$ and $$|z|<R$$. Multiplication by $$\bar\zeta-\bar z$$ gives

$$
\operatorname{Re}\frac{\zeta+z}{\zeta-z}
=\frac{R^2-|z|^2}{|\zeta-z|^2}=P_R(\zeta,z).
$$

This proves (a). For fixed $$\zeta$$ the quotient is holomorphic in $$RD$$, so its real part is harmonic, proving (b).

(c) Substituting $$\zeta=Re^{i\theta}$$ and $$z=re^{it}$$ gives

$$
P_R(Re^{i\theta},re^{it})=\frac{R^2-r^2}{R^2-2Rr\cos(\theta-t)+r^2}.
$$

This is valid for $$0\le r<R$$, the stated domain of the kernel. At $$r=R$$ it is zero for unequal angles and undefined when the two boundary points coincide; the printed endpoint must therefore be qualified.

(d) If $$q=re^{it}$$ and $$r<1$$, geometric series imply

$$
P_1(1,q)=\operatorname{Re}\frac{1+q}{1-q}
=1+\sum_{n=1}^\infty(q^n+\bar q^n)
=\sum_{n\in\mathbb Z}r^{|n|}e^{int}.
$$

The series converges absolutely and uniformly in $$t$$ for fixed $$r<1$$. For (e), apply (c) and (d) with $$r$$ replaced by $$|z|/R$$ and integrate termwise over $$\theta$$. All nonconstant Fourier terms vanish, giving $$\int_0^{2\pi}P_R(Re^{i\theta},z)\,d\theta=2\pi$$.

### Exercise 16

For $$|z|<1$$, Cauchy's formula on the unit circle gives

$$
f(z)=\frac1{2\pi}\int_0^{2\pi}\frac{f(e^{i\theta})}{1-ze^{-i\theta}}\,d\theta.
$$

On the circle, direct algebra gives

$$
P_1(e^{i\theta},z)=\frac1{1-ze^{-i\theta}}+
\frac1{1-\bar z e^{i\theta}}-1.
$$

The average of $$f(e^{i\theta})/(1-\bar z e^{i\theta})$$ equals $$f(0)$$ by Cauchy's formula, since its denominator has no zero in the closed unit disc; the average of $$f(e^{i\theta})$$ is also $$f(0)$$. Their difference vanishes, and the remaining term is $$f(z)$$. This proves the Poisson formula for complex-valued holomorphic $$f$$.

### Exercise 17

(a) On each compact subset of $$D$$, the Poisson kernel and its first two derivatives in $$z=x+iy$$ are continuous and uniformly bounded as $$\theta$$ varies. Differentiation under the integral is therefore valid twice. Exercise 15(b) gives a zero Laplacian for each kernel, hence for its integral against $$g$$.

(b) Since $$D$$ is simply connected, Exercise 4 provides a harmonic conjugate of $$f$$. For $$0<r<1$$, the holomorphic function with real part $$w\mapsto f(rw)$$ is defined on $$r^{-1}D$$. Apply Exercise 16 to it and take real parts:

$$
f(rz)=\frac1{2\pi}\int_0^{2\pi}P_1(e^{i\theta},z)f(re^{i\theta})\,d\theta.
$$

As $$r\uparrow1$$, continuity on the compact closed disc gives uniform convergence of the boundary values; the left side tends to $$f(z)$$. This gives the desired formula. The differential $$dz$$ at the end of the printed hint's integral should be $$d\theta$$.

### Exercise 18

**Correction.** The printed hypothesis $$\alpha\ne\operatorname{Re}a$$ is insufficient. With the upward orientation and symmetric improper limit, the value for $$t>0$$ is

$$
\frac1{2\pi i}\lim_{T\to\infty}\int_{-T}^{T}
\frac{e^{(\alpha+is)t}}{\alpha+is-a}\,i\,ds
=\begin{cases}e^{at},&\alpha>\operatorname{Re}a,\\0,&\alpha<\operatorname{Re}a.\end{cases}
$$

To prove this, write $$a=\beta+ib$$ and truncate the vertical line at $$\alpha+i(b\pm R)$$. Close it to the left by the semicircle $$\lambda=\alpha+ib+Re^{i\theta}$$, $$\pi/2\le\theta\le3\pi/2$$, with counterclockwise orientation. For large $$R$$ the closed contour contains $$a$$ exactly when $$\beta<\alpha$$. Cauchy's integral formula gives the corresponding closed-contour integral $$2\pi i e^{at}$$ or zero.

On the arc, $$|\lambda-a|\ge R-|\alpha-\beta|$$. Its integral has absolute value at most a constant times

$$
\frac{R}{R-|\alpha-\beta|}e^{\alpha t}
\int_{\pi/2}^{3\pi/2}e^{Rt\cos\theta}\,d\theta,
$$

which tends to zero: on either half of the arc, $$-\cos\theta$$ is bounded below by a positive constant times the angular distance to the nearest endpoint. Thus the vertical integrals with endpoints centered at $$b$$ converge to the asserted values. Replacing these endpoints by $$\pm T$$ changes the integral over two intervals of bounded length, where the integrand is $$O(1/T)$$, so the stated symmetric limit is the same. In particular, for $$\alpha<\beta$$ the printed equality fails.
