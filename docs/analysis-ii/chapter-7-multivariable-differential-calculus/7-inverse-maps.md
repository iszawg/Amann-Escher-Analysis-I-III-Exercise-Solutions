# Chapter VII — Multivariable Differential Calculus

## 7. Inverse maps

These are detailed solutions to Exercises 1–8. Inline mathematics uses GitBook’s `$$...$$` syntax; displayed calculations use the same delimiters on separate lines.

### Exercise 1

Let $$f\in\operatorname{Diff}^1_{\mathrm{loc}}(X,Y)$$, and fix $$x_0\in X$$. Put $$y_0=f(x_0)$$. By definition, there are open neighborhoods $$U\subseteq X$$ of $$x_0$$ and $$V\subseteq Y$$ of $$y_0$$ such that $$f|_U:U\to V$$ is a $$C^1$$ diffeomorphism. The identities

$$
f^{-1}|_V\circ f|_U=\operatorname{id}_U,
\qquad
f|_U\circ f^{-1}|_V=\operatorname{id}_V
$$

and the chain rule give

$$
D f^{-1}(y_0)\,D f(x_0)=I_E,
\qquad
D f(x_0)\,D f^{-1}(y_0)=I_F.
$$

Thus $$D f(x_0):E\to F$$ has bounded linear inverse $$D f^{-1}(y_0):F\to E$$. Therefore $$D f(x_0)\in\operatorname{Lis}(E,F)$$ and

$$
D f^{-1}(y_0)=\bigl(D f(x_0)\bigr)^{-1}.
$$

### Exercise 2

Assume first that $$X\ne\varnothing$$ and choose $$f\in\operatorname{Diff}^1_{\mathrm{loc}}(X,\mathbb R^m)$$. For any $$x_0\in X$$, Exercise 1 shows that

$$
D f(x_0):\mathbb R^n\longrightarrow\mathbb R^m
$$

is a linear isomorphism. A linear isomorphism between finite-dimensional vector spaces forces their dimensions to agree, so $$n=m$$.

There is a minor empty-domain caveat in the printed statement: if $$X=\varnothing$$ is allowed, the unique empty map satisfies the local condition vacuously for any $$m,n$$. Thus the conclusion holds as intended for nonempty $$X$$; literally, the empty-domain case is an exception.

### Exercise 3

Write points in the target as $$(u,v)$$.

**(a)** For $$f(x,y)=(x+a,y+b)$$, translation gives

$$
Y=\mathbb R^2,
\qquad
f^{-1}(u,v)=(u-a,v-b).
$$

Both maps are smooth on all of $$\mathbb R^2$$. Hence $$f\in\operatorname{Diff}^{\infty}_{\mathrm{loc}}(\mathbb R^2,\mathbb R^2)$$ and $$f\in\operatorname{Diff}^{\infty}(\mathbb R^2,Y)$$.

**(b)** Here $$f(x,y)=(x^2-x-2,3y)$$. The first component has minimum $$-9/4$$ at $$x=1/2$$, and the second component ranges over $$\mathbb R$$. Thus

$$
Y=[-9/4,\infty)\times\mathbb R.
$$

For $$(u,v)\in Y$$ the preimages are

$$
\left(\frac{1+\sqrt{4u+9}}2,\frac v3\right)
\quad\text{and}\quad
\left(\frac{1-\sqrt{4u+9}}2,\frac v3\right),
$$

coinciding only at $$u=-9/4$$. So there is no single-valued inverse on $$Y$$. Also,

$$
D f(x,y)=
\begin{pmatrix}2x-1&0\\0&3\end{pmatrix}
$$

is singular on the line $$x=1/2$$. More directly, points on either side of $$x=1/2$$ sufficiently close to it have the same first component, so $$f$$ is not injective on any neighborhood of a point on that line. Thus it is not even a local homeomorphism there, and is neither locally nor globally a diffeomorphism onto $$Y$$ for any $$q\ge0$$.

**(c)** Identify $$\mathbb R^2$$ with $$\mathbb C$$ by $$z=x+iy$$. Then $$f(x,y)=(x^2-y^2,2xy)$$ is the complex squaring map $$z\mapsto z^2$$ on $$\mathbb C\setminus\{0\}$$. Every nonzero complex number has a square root, so

$$
Y=\mathbb R^2\setminus\{(0,0)\}.
$$

Each target point represented by $$w\ne0$$ has the two preimages $$z$$ and $$-z$$, so the map has no global inverse. Its Jacobian determinant, however, is

$$
\det Df(x,y)=
\det\begin{pmatrix}2x&-2y\\2y&2x\end{pmatrix}
=4(x^2+y^2)>0.
$$

The inverse function theorem gives a smooth local inverse at every point. Thus $$f\in\operatorname{Diff}^{\infty}_{\mathrm{loc}}(X,\mathbb R^2)$$ but $$f\notin\operatorname{Diff}^{q}(X,Y)$$ for any $$q\ge0$$, because it is not injective.

**(d)** Put $$p=xy$$ and $$s=x^2+y^2$$. On $$X=\{(x,y):0<y<x\}$$,

$$
p>0,
\qquad
s-2p=(x-y)^2>0.
$$

The map gives $$u=\log p$$ and $$v=1/s$$, hence

$$
Y=\{(u,v)\in\mathbb R^2:v>0,\ 2ve^u<1\}.
$$

Indeed, the two inequalities are precisely $$s>2p>0$$ after substituting $$p=e^u$$ and $$s=1/v$$. Conversely, given $$(u,v)\in Y$$, set $$p=e^u$$ and $$s=1/v$$. Solving $$(x+y)^2=s+2p$$ and $$(x-y)^2=s-2p$$ gives

$$
x=\frac{\sqrt{s+2p}+\sqrt{s-2p}}2,
\qquad
y=\frac{\sqrt{s+2p}-\sqrt{s-2p}}2.
$$

Because $$s>2p>0$$ these formulas give $$0<y<x$$. They recover the unique point with that product and sum of squares. The formulas are smooth on the open set $$Y$$, so $$f\in\operatorname{Diff}^{\infty}(X,Y)$$ and is locally a smooth diffeomorphism.

### Exercise 4

View $$f$$ as the complex hyperbolic cosine:

$$
\cosh(x+iy)=\cosh x\cos y+i\sinh x\sin y.
$$

**(a)** Its partial derivatives are

$$
f_x=(\sinh x\cos y,\cosh x\sin y),
\qquad
f_y=(-\cosh x\sin y,\sinh x\cos y).
$$

Thus

$$
\det Df(x,y)
=\sinh^2x\cos^2y+\cosh^2x\sin^2y
=\sinh^2x+\sin^2y>0
$$

for every $$x>0$$. The inverse function theorem shows that $$f$$ is a local $$C^\infty$$ diffeomorphism on $$X$$.

**(b)** Since $$f(x,y+2\pi)=f(x,y)$$, distinct points such as $$(1,0)$$ and $$(1,2\pi)$$ have the same image. Hence $$f|_X$$ is not injective and is not a global diffeomorphism onto $$Y=f(X)$$.

**(c)** Set

$$
U=\{(x,y):x>0,\ 0<y<2\pi\},
\qquad
V=Y\setminus([0,\infty)\times\{0\}).
$$

If $$\cosh z=\cosh w$$, then

$$
z=w+2\pi i k\quad\text{or}\quad z=-w+2\pi i k
\qquad(k\in\mathbb Z).
$$

To see this, put $$a=e^z$$ and $$b=e^w$$ in $$a+a^{-1}=b+b^{-1}$$; factoring gives $$a=b$$ or $$a=b^{-1}$$. If both real parts are positive, the second possibility is excluded. In the first, two imaginary parts in $$(0,2\pi)$$ can differ by $$2\pi k$$ only for $$k=0$$. This proves injectivity on $$U$$.

Every image point has a preimage with some real second coordinate. Reduce that coordinate modulo $$2\pi$$ to $$[0,2\pi)$$. It is an endpoint exactly when the image is $$f(x,0)=(\cosh x,0)$$ for $$x>0$$, a point removed in the definition of $$V$$. Thus every point of $$V$$ has a preimage in $$U$$ and $$f(U)=V$$. In particular, $$V$$ is open because (a) makes $$f$$ an open map. The restriction is bijective, and its derivative is invertible everywhere by (a). Its local smooth inverses therefore combine into a smooth global inverse, so $$f|_U\in\operatorname{Diff}^{\infty}(U,V)$$.

**(d)** The image avoids $$[-1,1]\times\{0\}$$: if $$\sinh x\sin y=0$$ with $$x>0$$, then $$\sin y=0$$, and the first component is $$\pm\cosh x$$, of absolute value greater than $$1$$.

For the reverse inclusion, let $$(u,v)$$ lie outside that segment and seek $$x>0$$ satisfying

$$
\frac{u^2}{\cosh^2x}+\frac{v^2}{\sinh^2x}=1.
$$

With $$t=\sinh^2x$$ this becomes

$$
t^2+(1-u^2-v^2)t-v^2=0.
$$

If $$v\ne0$$, the left side is negative at $$t=0$$ and tends to $$+\infty$$; its two roots have product $$-v^2<0$$, so it has exactly one positive root. If $$v=0$$, being outside the segment means $$|u|>1$$, and the positive solution is $$t=u^2-1$$. Choose $$x>0$$ with $$\sinh^2x=t$$. The equation yields

$$
\left(\frac{u}{\cosh x}\right)^2+
\left(\frac{v}{\sinh x}\right)^2=1,
$$

so these two quotients are the cosine and sine of some real $$y$$. Then $$f(x,y)=(u,v)$$. Consequently,

$$
Y=\mathbb R^2\setminus([-1,1]\times\{0\}).
$$

### Exercise 5

Because $$Df(x)\in\operatorname{Lis}(\mathbb R^m)$$ everywhere, the inverse function theorem makes $$f$$ a local diffeomorphism. In particular, every point $$f(x_0)$$ has an open neighborhood contained in the image of a neighborhood of $$x_0$$.

**(a)** If $$x_0$$ were a local maximum of $$|f|$$, then $$|y|$$ would have a local maximum at $$y_0=f(x_0)$$ on an open neighborhood of $$y_0$$. This cannot happen: for $$y_0\ne0$$, nearby points $$(1+t)y_0$$ with $$t>0$$ have larger norm; for $$y_0=0$$, every nearby nonzero point has larger norm. Thus $$|f|$$ has no local maximum, and in particular no maximum attained in $$X$$.

**(b)** If $$x_0$$ were a local minimum, the assumption $$f(x_0)\ne0$$ would give $$y_0=f(x_0)\ne0$$. Nearby points $$(1-t)y_0$$ with $$t>0$$ lie in the open image neighborhood and have smaller norm, a contradiction. Thus $$|f|$$ has no minimum attained in $$X$$.

### Exercise 6

For $$r\ge0$$ let $$\rho(r)=r\sqrt{1+r^2}$$. Since

$$
\rho'(r)=\frac{1+2r^2}{\sqrt{1+r^2}}>0,
$$

and $$\rho(r)\to\infty$$, this maps $$[0,\infty)$$ bijectively onto itself. The map $$f(x)=x\sqrt{1+|x|^2}$$ preserves direction and changes vector length from $$r$$ to $$\rho(r)$$. Hence $$f:H\to H$$ is bijective and $$Y=H$$.

For $$s=|y|=\rho(r)$$, solving $$s^2=r^2+r^4$$ yields

$$
r^2=\frac{\sqrt{1+4s^2}-1}{2},
\qquad
1+r^2=\frac{1+\sqrt{1+4s^2}}2.
$$

Thus

$$
f^{-1}(y)=y\sqrt{\frac{2}{1+\sqrt{1+4|y|^2}}}.
$$

The scalar factor is smooth as a function of $$|y|^2$$, including at $$y=0$$. So $$f^{-1}\in C^\infty(H,H)$$ and $$f\in\operatorname{Diff}^{\infty}(H,H)$$.

For $$h\in H$$, differentiation gives

$$
Df(x)h
=\sqrt{1+|x|^2}\,h
+\frac{\langle x,h\rangle}{\sqrt{1+|x|^2}}\,x.
$$

At $$x=0$$ this is the identity. For $$x\ne0$$, on the orthogonal complement of $$x$$ it is multiplication by $$\sqrt{1+|x|^2}$$; on the span of $$x$$ it is multiplication by

$$
\sqrt{1+|x|^2}+\frac{|x|^2}{\sqrt{1+|x|^2}}
=\frac{1+2|x|^2}{\sqrt{1+|x|^2}}.
$$

Both factors are positive, so $$Df(x)$$ is invertible, consistently with the explicit smooth inverse.

### Exercise 7

The inequality immediately implies that $$f$$ is injective. For $$x\in X$$ and $$h\in\mathbb R^m$$, apply it to $$x+th$$ and $$x$$, divide by $$|t|$$, and let $$t\to0$$. Differentiability gives

$$
|Df(x)h|\ge\alpha|h|.
$$

Thus $$Df(x)$$ is injective, hence an isomorphism because it maps $$\mathbb R^m$$ to itself. By the inverse function theorem, $$f$$ is a local diffeomorphism and $$Y=f(X)$$ is open. It is bijective from $$X$$ onto $$Y$$ by injectivity and the definition of $$Y$$. Its local inverses agree with the global inverse wherever they overlap, so the global inverse is $$C^1$$. Therefore $$f\in\operatorname{Diff}^1(X,Y)$$.

If $$X=\mathbb R^m$$ and $$f(x_k)\to y$$, then

$$
|x_k-x_\ell|\le\frac1\alpha|f(x_k)-f(x_\ell)|,
$$

so $$(x_k)$$ is Cauchy. It converges to some $$x\in\mathbb R^m$$, and continuity gives $$f(x)=y$$. Hence $$Y$$ is closed. Since it is also nonempty and open, connectedness of $$\mathbb R^m$$ implies $$Y=\mathbb R^m$$.

### Exercise 8

Write $$F_\varepsilon=f+\varepsilon g$$.

**(a)** Suppose $$f^{-1}$$ and $$g$$ are Lipschitz, with constants $$L$$ and $$M$$. Then

$$
|x-y|=|f^{-1}(f(x))-f^{-1}(f(y))|
\le L|f(x)-f(y)|,
$$

so $$|f(x)-f(y)|\ge L^{-1}|x-y|$$. It follows that

$$
\begin{aligned}
|F_\varepsilon(x)-F_\varepsilon(y)|
&\ge |f(x)-f(y)|-|\varepsilon|\,|g(x)-g(y)|\\
&\ge \left(\frac1L-|\varepsilon|M\right)|x-y|.
\end{aligned}
$$

Choose $$\varepsilon_0>0$$ so that $$|\varepsilon|M<1/L$$ for $$|\varepsilon|<\varepsilon_0$$; if $$M=0$$, any positive $$\varepsilon_0$$ works. This is a positive lower Lipschitz bound. Applying Exercise 7 to $$F_\varepsilon:\mathbb R^m\to\mathbb R^m$$ proves it is a global $$C^1$$ diffeomorphism.

**(b)** Suppose $$g$$ vanishes outside a bounded set. Choose a closed ball $$K$$ containing that set in its interior, and define

$$
h_\varepsilon=f^{-1}\circ F_\varepsilon,
\qquad
h_\varepsilon(x)=f^{-1}\bigl(f(x)+\varepsilon g(x)\bigr).
$$

At $$\varepsilon=0$$, $$h_0=\operatorname{id}_{\mathbb R^m}$$. Outside $$K$$, $$g$$ vanishes on a neighborhood, so $$h_\varepsilon(x)=x$$ and $$Dh_\varepsilon(x)=I$$. On $$K$$, the chain rule gives

$$
Dh_\varepsilon(x)
=Df^{-1}\bigl(f(x)+\varepsilon g(x)\bigr)
\bigl(Df(x)+\varepsilon Dg(x)\bigr).
$$

This derivative is continuous in $$(x,\varepsilon)$$ for $$x\in K$$ and small $$\varepsilon$$, and equals $$I$$ at $$\varepsilon=0$$. Compactness of $$K$$ therefore gives $$\varepsilon_0>0$$ such that

$$
\sup_{x\in\mathbb R^m}\|Dh_\varepsilon(x)-I\|\le\frac12
\qquad\text{for }|\varepsilon|<\varepsilon_0.
$$

Integrating along the segment from $$y$$ to $$x$$ yields

$$
h_\varepsilon(x)-h_\varepsilon(y)
=(x-y)+\int_0^1\bigl(Dh_\varepsilon(y+t(x-y))-I\bigr)(x-y)\,dt,
$$

and hence $$|h_\varepsilon(x)-h_\varepsilon(y)|\ge\frac12|x-y|$$. Exercise 7 makes $$h_\varepsilon$$ a global $$C^1$$ diffeomorphism. Finally, $$F_\varepsilon=f\circ h_\varepsilon$$, so $$F_\varepsilon$$ is a composition of global $$C^1$$ diffeomorphisms and is itself one for $$|\varepsilon|<\varepsilon_0$$.
