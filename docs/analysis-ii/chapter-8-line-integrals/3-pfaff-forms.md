# Chapter VIII — Line Integrals

## 3. Pfaff forms

These are detailed solutions to Exercises 1–13. Inline formulas use GitBook's double-dollar syntax.

### Exercise 1

Let $$A\in L(E,F)$$ and $$B\in L(G,E)$$. For a continuous linear functional $$\lambda\in F'$$ and a vector $$z\in G$$, the definition of the dual operator gives

$$
\langle (AB)'\lambda,z\rangle
=\lambda\bigl((A\circ B)z\bigr)
=(A'\lambda)(Bz)
=(B'A'\lambda)(z).
$$

Since this holds for every $$z\in G$$, we have

$$
(AB)'=B'A'.
$$

If $$A\in\operatorname{Lis}(E,F)$$, then both $$A$$ and $$A^{-1}$$ are continuous. Applying the identity just proved to $$A^{-1}A=I_E$$ and $$AA^{-1}=I_F$$ yields

$$
A'(A^{-1})'=I_{E'},\qquad (A^{-1})'A'=I_{F'}.
$$

Thus $$A'$$ is a continuous linear isomorphism from $$F'$$ to $$E'$$, with

$$
(A')^{-1}=(A^{-1})'.
$$

### Exercise 2

A continuously differentiable 1-form $$\alpha=P\,dx+Q\,dy$$ on an open subset of $$\mathbb R^2$$ is closed exactly when $$P_y=Q_x$$.

**(a)** Here $$P(x,y)=2xy^3$$ and $$Q(x,y)=3x^2y^2$$. Hence

$$
P_y(x,y)=6xy^2=Q_x(x,y)
$$

for all $$(x,y)\in\mathbb R^2$$. Therefore the form is closed.

**(b)** Put

$$
U(x,y)=x^2+y^2-1,\qquad V(x,y)=2y,\qquad W=U^2+V^2.
$$

The deleted points are precisely the zeros of $$(U,V)$$, so $$W>0$$ on the stated domain. In the $$(U,V)$$-plane, consider

$$
\omega=-\frac{V}{U^2+V^2}\,dU+\frac{U}{U^2+V^2}\,dV.
$$

Writing $$P(U,V)=-V/W$$ and $$Q(U,V)=U/W$$, we calculate

$$
\frac{\partial Q}{\partial U}
=\frac{V^2-U^2}{W^2}
=\frac{\partial P}{\partial V}.
$$

Thus $$\omega$$ is closed away from $$(0,0)$$. The chain rule shows that its pullback by any smooth map is also closed: the mixed second derivatives of the map cancel, and the remaining coefficient is a multiple of $$Q_U-P_V$$. For the map $$(x,y)\mapsto(U(x,y),V(x,y))$$, we have

$$
dU=2x\,dx+2y\,dy,\qquad dV=2\,dy,
$$

and consequently

$$
\begin{aligned}
\omega
&=\frac{-V\,dU+U\,dV}{W}\\
&=\frac{-4xy\,dx+2(x^2-y^2-1)\,dy}
{(x^2+y^2-1)^2+4y^2}.
\end{aligned}
$$

This is the given form, so it is closed.

### Exercise 3

Use the functions $$U=x^2+y^2-1$$ and $$V=2y$$ from Exercise 2(b). The pullback of

$$
\alpha=\frac{u\,dv-v\,du}{u^2+v^2}
$$

is

$$
\begin{aligned}
\varphi^*\alpha
&=\frac{U\,dV-V\,dU}{U^2+V^2}\\
&=\frac{2(x^2+y^2-1)\,dy
-2y(2x\,dx+2y\,dy)}
{(x^2+y^2-1)^2+4y^2}\\
&=\frac{-4xy\,dx+2(x^2-y^2-1)\,dy}
{(x^2+y^2-1)^2+4y^2}.
\end{aligned}
$$

This is exactly the 1-form in Exercise 2(b).

### Exercise 4

Write the cotangent part of $$\Theta^{-1}\alpha$$ as

$$
a=(a_1,\ldots,a_n).
$$

The canonical basis representation from the section gives

$$
\alpha=\sum_{j=1}^n a_j\,dx_j.
$$

By definition, $$\alpha$$ is closed precisely when its coefficients satisfy

$$
\partial_k a_j=\partial_j a_k
\qquad (1\le j,k\le n).
$$

The Jacobian matrix $$\partial a(x)$$ has entries $$\partial_k a_j(x)$$. Therefore these equalities for every pair $$j,k$$ say exactly that $$\partial a(x)$$ is symmetric at every $$x\in X$$.

### Exercise 5

Let

$$
\alpha=x\,dy-y\,dx,\qquad
\beta=\frac{\alpha}{x^2+y^2},
$$

and use $$x=r\cos\theta$$ and $$y=r\sin\theta$$. Differentiating these coordinate functions gives

$$
dx=\cos\theta\,dr-r\sin\theta\,d\theta,\qquad
dy=\sin\theta\,dr+r\cos\theta\,d\theta.
$$

Substitution into $$\alpha$$ yields

$$
\begin{aligned}
\varphi^*\alpha
&=(r\cos\theta)(\sin\theta\,dr+r\cos\theta\,d\theta)\\
&\quad -(r\sin\theta)(\cos\theta\,dr-r\sin\theta\,d\theta)\\
&=r^2\,d\theta.
\end{aligned}
$$

Since $$x^2+y^2=r^2$$, it follows that

$$
\varphi^*\beta=d\theta.
$$

### Exercise 6

Write $$\theta_1=s$$ and $$\theta_2=t$$. Under the given map,

$$
x=\cos s\sin t,\qquad
y=\sin s\sin t,\qquad
z=\cos t.
$$

Their differentials are

$$
\begin{aligned}
dx&=-\sin s\sin t\,ds+\cos s\cos t\,dt,\\
dy&=\cos s\sin t\,ds+\sin s\cos t\,dt,\\
dz&=-\sin t\,dt.
\end{aligned}
$$

First, the terms in $$dt$$ cancel in $$x\,dy-y\,dx$$, leaving

$$
x\,dy-y\,dx=\sin^2t\,ds.
$$

Also,

$$
-(x+y)\,dz
=\sin^2t(\cos s+\sin s)\,dt.
$$

Therefore

$$
\varphi^*\alpha
=\sin^2\theta_2\,d\theta_1
+\sin^2\theta_2(\cos\theta_1+\sin\theta_1)\,d\theta_2.
$$

### Exercise 7

Write $$\alpha=\sum_{j=1}^n a_j\,dy_j$$ on $$Y$$. Its pullback has the coordinate expression

$$
\varphi^*\alpha=\sum_{i=1}^n b_i\,dx_i,\qquad
b_i(x)=\sum_{j=1}^n a_j(\varphi(x))\,\partial_i\varphi_j(x).
$$

**(a)** If $$\alpha=df$$, then the chain rule gives

$$
\varphi^*\alpha=\varphi^*(df)=d(f\circ\varphi),
$$

so $$\varphi^*\alpha$$ is exact. Conversely, suppose $$\varphi^*\alpha=dg$$. Since $$\varphi$$ is a diffeomorphism,

$$
\alpha=(\varphi^{-1})^*(\varphi^*\alpha)
=d(g\circ\varphi^{-1}),
$$

so $$\alpha$$ is exact.

**(b)** Assume $$q\ge2$$, so that closedness is defined. Differentiating the coefficients $$b_i$$ and subtracting cancels the second derivatives of $$\varphi$$, because mixed partial derivatives commute. Reindexing the remaining sum gives

$$
\partial_k b_i-\partial_i b_k
=\sum_{j,m=1}^n
\bigl(\partial_m a_j-\partial_j a_m\bigr)(\varphi(x))\,
\partial_k\varphi_m(x)\,\partial_i\varphi_j(x).
$$

If $$\alpha$$ is closed, every factor $$\partial_m a_j-\partial_j a_m$$ vanishes, so $$\varphi^*\alpha$$ is closed. For the converse, apply this same implication to the diffeomorphism $$\varphi^{-1}$$ and the form $$\varphi^*\alpha$$. It follows that $$\alpha$$ is closed.

### Exercise 8

**(a)** Let $$\alpha=a\,dx+b\,dy$$. Then

$$
h\alpha=(ha)\,dx+(hb)\,dy.
$$

This form is closed exactly when

$$
\partial_y(ha)=\partial_x(hb).
$$

Expanding both sides and rearranging gives

$$
a h_y-b h_x+(a_y-b_x)h=0.
$$

Thus a nowhere-zero function $$h$$ is an integrating factor exactly when it satisfies the stated equation.

**(b)** Write the coefficients of $$\beta$$ as

$$
A(x,y)=(c-ex)y,\qquad B(x,y)=(a-by)x.
$$

Set $$u=xy$$ and suppose $$h(x,y)=m(u)$$. Then $$h_x=ym'(u)$$ and $$h_y=xm'(u)$$. Substituting into the criterion from part (a), we obtain

$$
\begin{aligned}
0
&=A h_y-B h_x+(A_y-B_x)h\\
&=(c-a-ex+by)\bigl(u m'(u)+m(u)\bigr).
\end{aligned}
$$

For each fixed $$u>0$$, we can set $$y=u/x$$ and choose $$x$$ sufficiently large that $$c-a-ex+bu/x\ne0$$, since $$e>0$$. Hence the differential equation must be

$$
u m'(u)+m(u)=0.
$$

Equivalently, $$(u\,m(u))'=0$$, so $$m(u)=C/u$$ for a constant $$C$$. Choosing $$C=1$$ gives the nowhere-zero function $$h(x,y)=1/(xy)$$. Indeed,

$$
h\beta=\left(\frac{c}{x}-e\right)dx
+\left(\frac{a}{y}-b\right)dy,
$$

whose first coefficient is independent of $$y$$ and whose second is independent of $$x$$. Thus $$h\beta$$ is closed, as required.

### Exercise 9

Along the graph map $$\varphi_u(t)=(t,u(t))$$, the coordinate differentials pull back to

$$
\varphi_u^*(dt)=dt,\qquad
\varphi_u^*(dx)=u'(t)\,dt.
$$

Therefore

$$
\varphi_u^*\alpha
=\bigl(u'(t)-f(t,u(t))\bigr)\,dt.
$$

This 1-form vanishes identically exactly when $$u'(t)=f(t,u(t))$$ for every $$t\in J$$. That is precisely the differential equation $$\dot x=f(t,x)$$ along the solution $$x=u(t)$$.

### Exercise 10

Pointwise addition makes $$V^q(X)=C^q(X,\mathbb R^n)$$ an abelian group. If $$a,b\in C^q(X)$$ and $$v,w\in V^q(X)$$, define $$(av)(x)=a(x)v(x)$$. Scalar multiplication of vectors is bilinear, so the module distributive and associativity laws hold pointwise; the constant function $$1$$ acts as the identity. Since pointwise products of $$C^q$$ functions are $$C^q$$, this action is well defined. The same argument applies to $$\Omega^{(q)}(X)=C^q(X,(\mathbb R^n)')$$, using scalar multiplication in the dual space. Thus both are modules over $$C^q(X)$$.

There is a qualification to the last sentence as printed. With the standard definition, a submodule of a $$C^q(X)$$-module must be closed under multiplication by every element of $$C^q(X)$$. For finite $$q$$, the sets $$V^{q+1}(X)$$ and $$\Omega^{(q+1)}(X)$$ are not generally closed under that action. For example, take $$X=\mathbb R$$, let $$v(x)=1$$, and let $$a(x)=|x|^{q+1/2}$$. Then $$v\in V^{q+1}(X)$$ and $$a\in C^q(X)$$, but $$av=a\notin V^{q+1}(X)$$. Likewise, $$a\,dx\notin\Omega^{(q+1)}(X)$$.

The valid inclusion is that $$V^{q+1}(X)$$ and $$\Omega^{(q+1)}(X)$$ are submodules when viewed over the smaller ring $$C^{q+1}(X)$$: multiplying two $$C^{q+1}$$ objects preserves that regularity.

### Exercise 11

Regard $$R$$ as a module over itself by ring multiplication.

**(a)** The set $$aR=\{ar:r\in R\}$$ contains $$0=a0$$. If $$ar,as\in aR$$, then

$$
ar-as=a(r-s)\in aR.
$$

For $$t\in R$$, commutativity gives

$$
t(ar)=a(tr)\in aR.
$$

Thus $$aR$$ is an additive subgroup of $$R$$ stable under multiplication by elements of $$R$$, hence a submodule.

**(b)** If $$a=0$$, then $$aR=\{0\}$$. If $$aR=\{0\}$$, then in particular $$a=a\cdot1=0$$. Therefore

$$
aR\ne\{0\}\quad\Longleftrightarrow\quad a\ne0.
$$

**(c)** If $$a$$ is invertible, then $$1=aa^{-1}\in aR$$, so $$aR=R$$. Conversely, if $$aR=R$$, then $$1\in aR$$, so $$1=ar$$ for some $$r\in R$$; this says that $$r$$ is an inverse of $$a$$. Hence $$aR\ne R$$ exactly when $$a$$ has no inverse.

Here $$\mathbb Z_2$$ and $$\mathbb Z_6$$ denote the residue-class rings, regarded as $$\mathbb Z$$-modules. Their submodules are exactly their additive subgroups. Since $$\mathbb Z_2$$ has prime order, it has no nontrivial proper submodule. The nontrivial proper submodules of $$\mathbb Z_6$$ are

$$
\{[0],[2],[4]\}
\quad\text{and}\quad
\{[0],[3]\}.
$$

### Exercise 12

Let $$M$$ be an $$R$$-module.

First suppose $$U\subseteq M$$ is a submodule. Then $$U$$ is an additive subgroup and is stable under multiplication by every element of $$R$$. Therefore the addition and scalar multiplication inherited from $$M$$ are operations from $$U\times U$$ and $$R\times U$$ into $$U$$. All module axioms on $$U$$ follow by restricting the corresponding axioms on $$M$$. Thus $$U$$ is an $$R$$-module with the induced operations.

Conversely, suppose the induced operations make a nonempty subset $$U$$ into an $$R$$-module. Its additive identity must be the identity $$0$$ inherited from $$M$$, and its additive inverses are the same as those in $$M$$. Hence $$U$$ is an additive subgroup of $$M$$. The scalar operation is induced from $$M$$ and has values in $$U$$, so $$R\cdot U\subseteq U$$. Thus $$U$$ is a submodule.

Now let $$\{U_\lambda:\lambda\in\Lambda\}$$ be a nonempty family of submodules of $$M$$. Every $$U_\lambda$$ contains $$0$$, so their intersection is nonempty. If $$u,v$$ lie in the intersection, then they lie in every $$U_\lambda$$, and hence $$u-v\in U_\lambda$$ for every $$\lambda$$. Similarly, for every $$r\in R$$, $$ru\in U_\lambda$$ for every $$\lambda$$. Thus the intersection is an additive subgroup stable under the action of $$R$$ and is a submodule. If the family is empty, its intersection is conventionally $$M$$, also a submodule.

### Exercise 13

Let $$T:M\to N$$ be an $$R$$-module homomorphism.

For $$u,v\in\ker T$$, additivity gives

$$
T(u-v)=T(u)-T(v)=0,
$$

so $$u-v\in\ker T$$. For $$r\in R$$,

$$
T(ru)=rT(u)=0,
$$

so $$ru\in\ker T$$. Also $$0\in\ker T$$. Therefore $$\ker T$$ is a submodule of $$M$$.

The image contains $$0=T(0)$$. If $$T(u),T(v)\in\operatorname{im}T$$, then

$$
T(u)-T(v)=T(u-v)\in\operatorname{im}T.
$$

For every $$r\in R$$,

$$
rT(u)=T(ru)\in\operatorname{im}T.
$$

Thus $$\operatorname{im}T$$ is a submodule of $$N$$.
