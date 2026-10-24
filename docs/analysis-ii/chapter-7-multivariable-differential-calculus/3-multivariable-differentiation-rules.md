# Chapter VII — Multivariable Differential Calculus

## 3. Multivariable differentiation rules

Exercises follow the numbering in the textbook. Gradients are column vectors, and $$A^*$$ denotes the Euclidean adjoint (transpose) when the spaces are real Euclidean spaces.

### Exercise 1

Let $$A:=\partial f(0)\in L(E,F)$$. First, continuity of $$f$$ at the origin and positive homogeneity give

$$
f(0)=\lim_{t\downarrow0}f(tx)=\lim_{t\downarrow0}t f(x)=0
$$

for any fixed nonzero $$x$$. Differentiability at zero means that

$$
f(h)=f(0)+Ah+r(h),\qquad \frac{\|r(h)\|}{\|h\|}\longrightarrow0\quad(h\to0).
$$

Fix $$x\ne0$$ and substitute $$h=tx$$ with $$t>0$$. Using $$f(tx)=t f(x)$$ and $$f(0)=0$$, we obtain

$$
t f(x)=tAx+r(tx),\qquad
f(x)-Ax=\frac{r(tx)}{t}.
$$

Since

$$
\left\|\frac{r(tx)}{t}\right\|
=\frac{\|r(tx)\|}{\|tx\|}\,\|x\|\longrightarrow0,
$$

we get $$f(x)=Ax$$. This also holds at $$x=0$$, so $$f=A$$ on all of $$E$$. The derivative $$A$$ is bounded and linear; hence $$f\in L(E,F)$$.

### Exercise 2

Fix $$x\in\mathbb R^m\setminus\{0\}$$ and define, for $$t>0$$,

$$
\phi(t):=t^{-\alpha}f(tx).
$$

The chain rule and the assumed Euler relation, applied at $$tx$$, yield

$$
\begin{aligned}
\phi'(t)
&=-\alpha t^{-\alpha-1}f(tx)+t^{-\alpha}\nabla f(tx)\cdot x\\
&=-\alpha t^{-\alpha-1}f(tx)
+t^{-\alpha}\frac{\nabla f(tx)\cdot(tx)}{t}\\
&=0.
\end{aligned}
$$

Thus $$\phi$$ is constant on $$(0,\infty)$$. Evaluating at $$t=1$$ gives $$t^{-\alpha}f(tx)=f(x)$$, or

$$
f(tx)=t^\alpha f(x)\qquad(t>0).
$$

This is positive homogeneity of degree $$\alpha$$.

### Exercise 3

Set $$q(u)=\sin\|u\|^2$$ for $$u\in\mathbb R^n$$. Since $$f\in C^1(X,\mathbb R^n)$$ and $$q$$ is smooth, the composition $$g=q\circ f$$ is continuously differentiable. For $$v\in\mathbb R^n$$,

$$
Dq(u)v=\cos\|u\|^2\,D(\langle u,u\rangle)v
=2\cos\|u\|^2\,\langle u,v\rangle.
$$

Applying the chain rule at $$x\in X$$,

$$
Dg(x)h=2\cos\|f(x)\|^2\,\langle f(x),Df(x)h\rangle
$$

for every $$h\in\mathbb R^m$$. Therefore

$$
\boxed{\nabla g(x)=2\cos\bigl(\|f(x)\|^2\bigr)\,Df(x)^*f(x).}
$$

In matrix notation, $$Df(x)^*$$ is the transpose of the $$n\times m$$ Jacobian matrix of $$f$$.

### Exercise 4

The chain rule gives

$$
D(f\circ A)(x)h=Df(Ax)(Ah)
$$

for every $$h\in\mathbb R^n$$. By the definition of the gradient and the adjoint,

$$
\begin{aligned}
\langle\nabla(f\circ A)(x),h\rangle
&=D(f\circ A)(x)h\\
&=\langle\nabla f(Ax),Ah\rangle\\
&=\langle A^*\nabla f(Ax),h\rangle.
\end{aligned}
$$

Because these inner products agree for every $$h$$, the vectors agree:

$$
\boxed{\nabla(f\circ A)(x)=A^*\nabla f(Ax).}
$$

### Exercise 5

Consider the map $$\Phi(x)=(x,\xi(x))$$. The chain rule applied to $$m=f\circ\Phi$$ first gives

$$
\nabla m(x)=\nabla_1 f(x,\xi(x))+D\xi(x)^*\nabla_2 f(x,\xi(x)),
$$

where $$\nabla_1 f\in\mathbb R^k$$ and $$\nabla_2 f\in\mathbb R^n$$ are the gradients in the first and second variables. In detail, for $$h\in\mathbb R^k$$,

$$
Dm(x)h= D_1f(x,\xi(x))h+D_2f(x,\xi(x))\bigl(D\xi(x)h\bigr).
$$

For each fixed $$x$$, the equality $$m(x)=f(x,\xi(x))=\min_{y\in Y}f(x,y)$$ says that $$y=\xi(x)$$ is a minimizer. Since $$Y$$ is open, this point is an interior point. For any $$v\in\mathbb R^n$$, the one-variable function $$t\mapsto f(x,\xi(x)+tv)$$ is defined for small $$t$$ and has a local minimum at zero. Its derivative at zero is therefore zero:

$$
D_2f(x,\xi(x))v=\langle\nabla_2 f(x,\xi(x)),v\rangle=0.
$$

This holds for every $$v$$, so $$\nabla_2 f(x,\xi(x))=0$$. The term involving $$D\xi$$ vanishes, leaving

$$
\boxed{\nabla m(x)=\nabla_1 f(x,\xi(x)).}
$$

### Exercise 6

Define $$F(x_1,\ldots,x_m)=(f_1(x_1),\ldots,f_m(x_m))$$. The requested function is $$h=g\circ F$$. The Jacobian matrix of $$F$$ is diagonal, with diagonal entries $$f_j'(x_j)$$. Thus the chain rule gives, for each $$j=1,\ldots,m$$,

$$
\frac{\partial h}{\partial x_j}(x_1,\ldots,x_m)
=\partial_j g\bigl(f_1(x_1),\ldots,f_m(x_m)\bigr)f_j'(x_j).
$$

Equivalently,

$$
\boxed{
\nabla h(x_1,\ldots,x_m)=
\begin{pmatrix}
\partial_1g(F(x))f_1'(x_1)\\
\vdots\\
\partial_mg(F(x))f_m'(x_m)
\end{pmatrix}.}
$$

### Exercise 7

For fixed $$x,y\in\mathbb R$$, consider $$\psi(t)=f(x+t,y-t)$$. Its derivative is

$$
\psi'(t)=\partial_1f(x+t,y-t)-\partial_2f(x+t,y-t)=0.
$$

Hence $$\psi$$ is constant. Taking $$t=0$$ and $$t=y$$ shows that

$$
f(x,y)=f(x+y,0).
$$

Let $$H(s)=f(s,0)$$. Then $$H\in C^1(\mathbb R,\mathbb R)$$ and $$H(0)=0$$. Define

$$
q(s):=\int_0^1 H'(ts)\,dt\qquad(s\in\mathbb R).
$$

Continuity of $$H'$$ implies continuity of $$q$$. The fundamental theorem of calculus and the substitution $$u=ts$$ give

$$
s q(s)=\int_0^s H'(u)\,du=H(s)-H(0)=H(s),
$$

also when $$s=0$$. Now set $$g(x,y)=q(x+y)$$. This function is continuous and satisfies

$$
g(x,y)(x+y)=q(x+y)(x+y)=H(x+y)=f(x,y),
$$

as required.

### Exercise 8

Work in the Banach algebra $$L(E)$$ with its operator norm. For $$n\ge1$$, the map $$P_n(A)=A^n$$ is a continuous polynomial. Expanding a product with one increment $$H$$ shows that

$$
DP_n(A)H=\sum_{j=0}^{n-1}A^jHA^{n-1-j}.
$$

Indeed, the terms containing exactly one copy of $$H$$ form this sum; every remaining term in $$(A+H)^n-A^n$$ contains at least two copies of $$H$$ and is therefore $$O(\|H\|^2)$$ for fixed $$A$$. Consequently,

$$
\left\|D\left(\frac{P_n}{n!}\right)(A)\right\|
\leq\frac{\|A\|^{n-1}}{(n-1)!}.
$$

On every ball $$\|A\|\leq R$$, both the exponential series and its termwise derivative series converge uniformly, since

$$
\sum_{n=0}^{\infty}\frac{R^n}{n!}=e^R,
\qquad
\sum_{n=1}^{\infty}\frac{R^{n-1}}{(n-1)!}=e^R.
$$

The standard termwise differentiation theorem for locally uniformly convergent series of continuously differentiable maps therefore applies. It follows that $$\exp\in C^1(L(E),L(E))$$, with

$$
D\exp(A)H=\sum_{n=1}^{\infty}\frac1{n!}
\sum_{j=0}^{n-1}A^jHA^{n-1-j}.
$$

At $$A=0$$, every term vanishes except the $$n=1$$ term, which is $$H$$. Hence

$$
\boxed{\partial\exp(0)H=H\quad(H\in L(E)),\qquad
\partial\exp(0)=\operatorname{id}_{L(E)}.}
$$
