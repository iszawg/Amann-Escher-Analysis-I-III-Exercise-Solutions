# Chapter VII — Multivariable Differential Calculus

## 2. Differentiability

Exercises follow the numbering in the textbook.

### Exercise 1

Write the function as $$f(x,y)=A(x)^y+(\log x)G(x,y)$$, where $$A(x)=(((x^x)^x)^x)$$ and $$G$$ is the nested trigonometric expression in the question. All these functions are smooth on $$x,y>0$$. For the first term,

$$
\partial_2\bigl(A(x)^y\bigr)=A(x)^y\log A(x).
$$

At $$x=1$$, we have $$A(1)=1$$, so this derivative is zero. In the second term, $$x$$ is fixed when taking $$\partial_2$$; hence

$$
\partial_2\bigl((\log x)G(x,y)\bigr)=(\log x)\,\partial_2G(x,y),
$$

which also vanishes at $$x=1$$ because $$\log 1=0$$. Therefore

$$
\boxed{\partial_2 f(1,y)=0\qquad(y>0).}
$$

### Exercise 2

Let $$v=(a,b)$$ and $$r=\sqrt{a^2+b^2}$$. Since $$f(0,0)=0$$, compute

$$
D_vf(0,0)=\lim_{t\to0}\frac{f(ta,tb)}{t}.
$$

If $$b>0$$, the sign of $$tb$$ changes with $$t$$, and the two branches of the definition give $$f(ta,tb)=tr$$ on both sides of zero. If $$b<0$$, they give $$f(ta,tb)=-tr$$ on both sides. When $$b=0$$, the middle branch gives $$f(ta,0)=ta$$. Thus every directional derivative exists and

$$
D_vf(0,0)=
\begin{cases}
\sqrt{a^2+b^2},&b>0,\\
-\sqrt{a^2+b^2},&b<0,\\
a,&b=0.
\end{cases}
$$

However, a derivative at the origin would be a linear map, so its directional derivatives would satisfy additivity. Here

$$
D_{(1,0)}f(0,0)=1,\qquad D_{(0,1)}f(0,0)=1,
\qquad D_{(1,1)}f(0,0)=\sqrt2\ne2.
$$

Therefore $$f$$ is not differentiable at $$(0,0)$$, even though all its directional derivatives there exist.

### Exercise 3

Put $$r=\sqrt{x^2+y^2}$$. Away from the origin, $$f(x,y)=x^3/r$$ is smooth. At the origin,

$$
|f(x,y)|=\frac{|x|^3}{r}\le r^2,
$$

so $$|f(x,y)|/r\le r\to0$$. This is precisely the differentiability condition at the origin with derivative the zero linear map. Thus $$f$$ is differentiable at every point. Its derivative at the origin is zero; for $$(x,y)\ne(0,0)$$ its gradient is

$$
\nabla f(x,y)=\left(\frac{3x^2}{r}-\frac{x^4}{r^3},\,-\frac{x^3y}{r^3}\right).
$$

### Exercise 4

For the coordinate directions,

$$
f(t,0)=f(0,t)=0,
$$

so $$\partial_1f(0,0)=\partial_2f(0,0)=0$$. For an arbitrary vector $$v=(a,b)$$,

$$
\frac{f(ta,tb)}{t}
=\frac{|t|}{t}\,\frac{ab}{\sqrt{a^2+b^2}}
\qquad(v\ne0).
$$

The two-sided limit exists exactly when $$ab=0$$. In that case it is zero. In particular, it fails for every direction with both coordinates nonzero.

The printed claim in part (b), that the limit fails for every $$v\in\mathbb R^2\setminus\{e_1,e_2\}$$, is false as written: for example, $$v=2e_1$$ is not either of the two excluded vectors, but its directional derivative exists. The exact statement supported by the calculation is that $$D_vf(0,0)$$ fails to exist when $$v\notin\mathbb Re_1\cup\mathbb Re_2$$.

If $$f$$ were differentiable at the origin, its derivative would have to be the zero map because both coordinate partial derivatives are zero. But along $$v=(1,1)$$ the difference quotient has no limit. Hence $$f$$ is not differentiable at $$(0,0)$$.

### Exercise 5

The Jacobi matrix has one row for each output component and one column for each input variable.

**(i)** For $$f(x,y,z)=3x^2y+e^{xz^2}+4z^3$$,

$$
\partial f(x,y,z)=
\begin{bmatrix}
6xy+z^2e^{xz^2}&3x^2&2xz e^{xz^2}+12z^2
\end{bmatrix}.
$$

**(ii)** For $$f(x,y)=(xy,\cosh(xy),\log(1+x^2))$$,

$$
\partial f(x,y)=
\begin{bmatrix}
y&x\\
y\sinh(xy)&x\sinh(xy)\\
\dfrac{2x}{1+x^2}&0
\end{bmatrix}.
$$

**(iii)** For $$f(x,y,z)=(\log(1+x^2+z^2),z^2+y^2-x^2,\sin(xz))$$,

$$
\partial f(x,y,z)=
\begin{bmatrix}
\dfrac{2x}{1+x^2+z^2}&0&\dfrac{2z}{1+x^2+z^2}\\
-2x&2y&2z\\
z\cos(xz)&0&x\cos(xz)
\end{bmatrix}.
$$

**(iv)** For $$f(x,y,z)=(x\sin y\cos z,x\sin y\sin z,x\cos y)$$, differentiating each component gives

$$
\partial f(x,y,z)=
\begin{bmatrix}
\sin y\cos z&x\cos y\cos z&-x\sin y\sin z\\
\sin y\sin z&x\cos y\sin z&x\sin y\cos z\\
\cos y&-x\sin y&0
\end{bmatrix}.
$$

### Exercise 6

There is a problem with the statement as printed. It places the increment $$h$$ in $$B(x_0,\varepsilon)$$ even though $$h$$ is added to $$x_0$$, where the natural increment ball would be $$B(0,\varepsilon)$$. More substantially, the displayed coordinate-difference limits do not characterize differentiability under either natural reading.

If the limits mean scalar limits in $$h^k$$ with the other coordinates fixed, their existence only asks for certain partial derivatives. Partial derivatives may all exist without differentiability. For example, define

$$
g(x,y)=
\begin{cases}
\dfrac{xy}{x^2+y^2},&(x,y)\ne(0,0),\\
0,&(x,y)=(0,0).
\end{cases}
$$

Every coordinate partial derivative exists at every point: away from the origin the function is smooth, and at the origin both coordinate partials are zero. Yet $$g(t,t)=1/2$$ for $$t\ne0$$, so $$g$$ is not even continuous at the origin and hence is not differentiable there.

If instead the displayed quotients are meant to have a joint limit as the whole increment $$h\to0$$, differentiability still does not imply those limits. Let

$$
q(x,y)=
\begin{cases}
x^2\sin(y/x^3),&x\ne0,\\
0,&x=0.
\end{cases}
$$

Since $$|q(x,y)|\le x^2\le x^2+y^2$$, the function is differentiable at the origin with derivative zero. But the quotient for the second coordinate step is

$$
\frac{q(x,y)-q(x,0)}{y}=\frac{x^2\sin(y/x^3)}{y}.
$$

Along $$y=x^4$$ this is asymptotic to $$1/x$$, so it has no joint limit as $$(x,y)\to(0,0)$$.

Consequently, Exercise 6 cannot be proved as stated. A valid criterion given in this section of the textbook is Theorem 2.10: if the partial derivatives exist in a neighborhood of $$x_0$$ and are continuous at every point there, then $$f$$ is continuously differentiable there. At a single point, the defining criterion is the existence of a linear map $$A$$ such that

$$
f(x_0+h)=f(x_0)+Ah+o(\|h\|)\qquad(h\to0).
$$

### Exercise 7

Let $$T:E\to E^*$$ be the conjugate-linear isometric bijection from the Riesz representation theorem, $$Ty=(\,\cdot\mid y)$$. The proposed form on $$E^*$$ is

$$
[f\mid g]=(T^{-1}g\mid T^{-1}f).
$$

Because $$T^{-1}$$ is conjugate linear and the inner product is linear in its first argument, for scalars $$\alpha,\beta$$,

$$
[\alpha f_1+\beta f_2\mid g]
=(T^{-1}g\mid\overline\alpha T^{-1}f_1+\overline\beta T^{-1}f_2)
=\alpha[f_1\mid g]+\beta[f_2\mid g].
$$

Conjugate symmetry follows from that of the inner product on $$E$$:

$$
\overline{[f\mid g]}=(T^{-1}f\mid T^{-1}g)=[g\mid f].
$$

Finally,

$$
[f\mid f]=\|T^{-1}f\|^2\ge0,
$$

with equality exactly when $$f=0$$. Thus this is an inner product. Since $$T$$ is an isometry, its induced norm is the dual norm, and the finite-dimensional space $$E^*$$ is complete. Hence $$E^*$$ is a Hilbert space with this inner product.

### Exercise 8

Use the Euclidean inner product and treat $$x_0\in\mathbb R^m$$ as fixed.

**(i)** For $$f(x)=(x_0\mid x)$$, the differential is $$Df(x)h=(x_0\mid h)$$, so

$$
\nabla f(x)=x_0.
$$

**(ii)** For $$x\ne0$$, differentiating $$|x|=(x\mid x)^{1/2}$$ gives

$$
D|\cdot|(x)h=\frac{(x\mid h)}{|x|},\qquad \nabla |x|=\frac{x}{|x|}.
$$

**(iii)** Since $$f(x)=|(x_0\mid x)|^2=(x_0\mid x)^2$$,

$$
Df(x)h=2(x_0\mid x)(x_0\mid h),\qquad
\nabla f(x)=2(x_0\mid x)x_0.
$$

**(iv)** For $$x\ne0$$, the chain rule yields

$$
D(|\cdot|^{-1})(x)h=-\frac{(x\mid h)}{|x|^3},\qquad
\nabla\frac1{|x|}=-\frac{x}{|x|^3}.
$$

### Exercise 9

At the origin,

$$
\lim_{h\to0}\frac{h|h|-0}{h}=\lim_{h\to0}|h|=0,
$$

so the complex derivative exists and is zero.

For $$z=x+iy\ne0$$, set $$r=\sqrt{x^2+y^2}$$. Then $$z|z|=u(x,y)+iv(x,y)$$ with $$u=xr$$ and $$v=yr$$. The Cauchy–Riemann equations require

$$
u_x=r+\frac{x^2}{r}=v_y=r+\frac{y^2}{r},
\qquad
u_y=\frac{xy}{r}=-v_x=-\frac{xy}{r}.
$$

These imply $$x^2=y^2$$ and $$xy=0$$, which force $$x=y=0$$, contradicting $$z\ne0$$. Thus the map is complex differentiable only at zero, with $$f'(0)=0$$.

### Exercise 10

Let $$r=|x|$$ and suppose first that $$k\ge1$$. At $$x=0$$,

$$
\frac{|x|\,|x|^k}{|x|}=|x|^k\longrightarrow0,
$$

so the derivative is the zero linear map. For $$x\ne0$$, apply the product and chain rules to $$F(x)=xr^k$$. For every increment $$h\in\mathbb R^m$$,

$$
DF(x)h=r^k h+k r^{k-2}(x\mid h)x.
$$

Therefore the map is differentiable everywhere, with $$DF(0)=0$$ and the displayed formula away from zero. If the convention $$0\in\mathbb N$$ is used and the case $$k=0$$ is included, interpret $$|x|^0=1$$ so that $$F(x)=x$$; then $$DF(x)=I$$ everywhere.

### Exercise 11

Write $$f=u+iv$$ with real-valued $$u,v$$. Since $$f(\mathbb C)\subset\mathbb R$$, we have $$v\equiv0$$. Complex differentiability gives the Cauchy–Riemann equations

$$
u_x=v_y=0,\qquad u_y=-v_x=0.
$$

Thus both partial derivatives of $$u$$ vanish everywhere. Along every line segment, the one-variable chain rule then shows that $$u$$ is constant. Therefore the differentiable functions in question are exactly the real constants.

### Exercise 12

At the origin none of these norms is differentiable. Indeed, if a norm $$N$$ had a linear derivative $$L$$ at zero, positive homogeneity would give $$L(x)=N(x)$$ for every $$x$$ by taking $$t\downarrow0$$ in $$N(tx)/t$$. Applying this to $$-x$$ contradicts linearity whenever $$x\ne0$$.

For $$1<p<\infty$$ and $$x\ne0$$, differentiating $$f_p(x)=(\sum_i|x_i|^p)^{1/p}$$ gives

$$
\nabla f_p(x)=\frac{(|x_1|^{p-2}x_1,\ldots,|x_m|^{p-2}x_m)}{\|x\|_p^{p-1}},
$$

where a component with $$x_i=0$$ is interpreted as zero. Hence $$f_p$$ is differentiable at every nonzero point for $$1<p<\infty$$.

For $$p=1$$, the function is differentiable exactly when every coordinate of $$x$$ is nonzero. At such points,

$$
\nabla f_1(x)=(\operatorname{sgn}x_1,\ldots,\operatorname{sgn}x_m).
$$

If some $$x_j=0$$, varying only that coordinate produces the nondifferentiable term $$|h_j|$$.

For $$p=\infty$$, write $$\|x\|_\infty=\max_i|x_i|$$. At a nonzero point there is differentiability exactly when one coordinate, say $$x_j$$, uniquely attains this maximum. In that case, the same coordinate remains maximal in a neighborhood and

$$
\nabla f_\infty(x)=\operatorname{sgn}(x_j)e_j.
$$

If two or more coordinates tie for the maximum, the maximum of their distinct active linear pieces has no linear derivative. In summary, the differentiability sets are: all nonzero $$x$$ for $$1<p<\infty$$; the points with no zero coordinates for $$p=1$$; and the points with a unique largest absolute coordinate for $$p=\infty$$.

### Exercise 13

Complex conjugation maps $$X$$ homeomorphically onto $$X^*$$, so $$X^*$$ is open. Fix $$z\in X^*$$. For small $$h$$,

$$
\frac{f^*(z+h)-f^*(z)}{h}
=\frac{\overline{f(\overline z+\overline h)-f(\overline z)}}{h}
=\overline{\frac{f(\overline z+\overline h)-f(\overline z)}{\overline h}}.
$$

As $$h\to0$$, also $$\overline h\to0$$, and the last expression tends to $$\overline{f'(\overline z)}$$. Thus $$f^*$$ is complex differentiable on $$X^*$$ and

$$
(f^*)'(z)=\overline{f'(\overline z)}.
$$
