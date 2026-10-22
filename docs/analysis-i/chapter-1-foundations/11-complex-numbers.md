# Chapter I — Foundations

## 11. The Complex Numbers

### Exercise 1

**(a)** Write $$z=x+iy$$ and $$w=u+iv$$, with $$x,y,u,v\in\mathbb R$$. If $$w^2=z$$, then

$$
u^2-v^2=x,\qquad 2uv=y,\qquad u^2+v^2=|z|.
$$

Consequently,

$$
u^2=\frac{|z|+x}{2},\qquad v^2=\frac{|z|-x}{2}.
$$

Since $$z\notin(-\infty,0]$$, we have $$|z|+x>0$$. Thus there is exactly one possible choice with $$u>0$$, namely $$u=\sqrt{(|z|+x)/2}$$. Then $$v=y/(2u)$$ is uniquely determined, and these values satisfy $$w^2=z$$. This proves existence and uniqueness.

**(b)** The preceding calculation gives

$$
\operatorname{Re}\sqrt z=\sqrt{\frac{|z|+\operatorname{Re}z}{2}}.
$$

Also, $$2uv=\operatorname{Im}z$$, so the imaginary part of $$w$$ has the sign of $$\operatorname{Im}z$$ (and is zero when that part is zero). Therefore

$$
\sqrt z=
\sqrt{\frac{|z|+\operatorname{Re}z}{2}}
+i\,\operatorname{sign}(\operatorname{Im}z)
\sqrt{\frac{|z|-\operatorname{Re}z}{2}}.
$$

**(c)** Substitution into the formula gives

$$
\sqrt i=\frac{1+i}{\sqrt2}.
$$

The two roots of $$w^2=i$$ are $$\frac{1+i}{\sqrt2}$$ and $$-\frac{1+i}{\sqrt2}$$.

### Exercise 2

For $$z_1=(12+5i)/(2+3i)$$, multiplication by the conjugate of the denominator gives

$$
z_1=\frac{(12+5i)(2-3i)}{13}=3-2i.
$$

Hence

$$
\overline{z_1}=3+2i,\quad |z_1|=\sqrt{13},\quad
\operatorname{Re}z_1=3,\quad \operatorname{Im}z_1=-2,
$$

and

$$
\frac1{z_1}=\frac{3+2i}{13},\quad
\operatorname{Re}(1/z_1)=\frac3{13},\quad
\operatorname{Im}(1/z_1)=\frac2{13}.
$$

For $$z_2=\sqrt i=(1+i)/\sqrt2$$, we have

$$
\overline{z_2}=\frac{1-i}{\sqrt2},\quad |z_2|=1,\quad
\operatorname{Re}z_2=\operatorname{Im}z_2=\frac1{\sqrt2}.
$$

Since $$1/z_2=\overline{z_2}$$, its real and imaginary parts are $$1/\sqrt2$$ and $$-1/\sqrt2$$, respectively.

### Exercise 3

Write $$z=x+iy$$.

**(a)** Squaring the two sides of the defining inequality gives $$|z-1|^2\le|z+1|^2$$, which simplifies to $$x\ge0$$. Thus $$A$$ is the closed right half-plane.

**(b)** The two inequalities are equivalent to

$$
|z+1|\le|z-i|\iff x+y\le0,\qquad
|z-i|\le|z-1|\iff x\le y.
$$

Thus $$B=\{x+iy:x+y\le0,\ x\le y\}$$, the closed wedge with vertex $$0$$ between the rays $$y=x$$ and $$y=-x$$ pointing to the left.

**(c)** Using $$z\overline z=x^2+y^2$$ and $$z+\overline z=2x$$, the equation becomes

$$
3(x^2+y^2)-12x+9=0
\iff (x-2)^2+y^2=1.
$$

Therefore $$C$$ is the circle with center $$2$$ and radius $$1$$.

### Exercise 4

The fourth roots of unity are

$$
z\in\{1,i,-1,-i\},
$$

and the cube roots of unity are

$$
z\in\left\{1,\frac{-1+i\sqrt3}{2},\frac{-1-i\sqrt3}{2}\right\}.
$$

These follow by factoring $$z^4-1=(z^2-1)(z^2+1)$$ and $$z^3-1=(z-1)(z^2+z+1)$$.

### Exercise 5

Let $$z=x+iy$$ and $$w=a+ib$$, with all four coordinates real. Then $$\overline z=x-iy$$, so

$$
\frac{z+\overline z}{2}=x=\operatorname{Re}z,\qquad
\frac{z-\overline z}{2i}=y=\operatorname{Im}z.
$$

Also, $$z=\overline z$$ exactly when $$y=0$$, which is exactly when $$z\in\mathbb R$$. Conjugating twice returns $$x+iy$$. Since $$z+w=(x+a)+i(y+b)$$ and $$zw=(xa-yb)+i(xb+ya)$$, direct conjugation gives

$$
\overline{z+w}=\overline z+\overline w,\qquad
\overline{zw}=\overline z\,\overline w.
$$

Finally,

$$
z\overline z=(x+iy)(x-iy)=x^2+y^2,
$$

where $$x=\operatorname{Re}z$$ and $$y=\operatorname{Im}z$$. These are all the assertions of Proposition 11.3.

### Exercise 6

There are finitely many radii, so

$$
r:=\min_{0\le j\le m}r_j>0.
$$

If $$|z-a|<r$$, then $$|z-a|<r_j$$ for every $$j$$, hence $$z\in U_j$$ for every $$j$$. Therefore

$$
B(a,r)\subseteq\bigcap_{j=0}^m U_j.
$$

### Exercise 7

By the definitions of the open and closed balls,

$$
\overline B_K(a,r)\setminus B_K(a,r)=\{x\in K:|x-a|=r\}.
$$

For $$K=\mathbb R$$ this is $$\{a-r,a+r\}$$; for $$K=\mathbb C$$ it is the circle of radius $$r$$ centered at $$a$$.

### Exercise 8

Let $$\varphi:\mathbb C\to\mathbb C$$ be a field automorphism fixing every real number. Since $$\varphi(i)^2=\varphi(-1)=-1$$, we have $$\varphi(i)=i$$ or $$\varphi(i)=-i$$. Every $$z=x+iy$$ with $$x,y\in\mathbb R$$ therefore satisfies

$$
\varphi(z)=\varphi(x)+\varphi(i)\varphi(y)
=x+\varphi(i)y.
$$

In the first case $$\varphi(z)=z$$; in the second, $$\varphi(z)=\overline z$$. Both maps are field automorphisms fixing $$\mathbb R$$, so these are the only two.

### Exercise 9

The set $$S^1=\{z\in\mathbb C:|z|=1\}$$ contains $$1$$. If $$z,w\in S^1$$, then $$|zw|=|z||w|=1$$, so it is closed under multiplication. If $$z\in S^1$$, then $$z\ne0$$ and $$|z^{-1}|=1/|z|=1$$, so it is closed under inverses. Thus $$S^1$$ is a subgroup of $$\mathbb C^\times$$.

### Exercise 10

Define

$$
\Phi:\mathbb C\longrightarrow M_2(\mathbb R),\qquad
\Phi(a+ib)=
\begin{pmatrix}a&-b\\ b&a\end{pmatrix}.
$$

Its image is exactly the set $$\mathcal M$$ of matrices of the displayed form in the exercise, and it is injective because the matrix entries recover $$a$$ and $$b$$. Direct multiplication shows

$$
\Phi((a+ib)+(c+id))=\Phi(a+ib)+\Phi(c+id),
\qquad
\Phi((a+ib)(c+id))=\Phi(a+ib)\Phi(c+id).
$$

Also $$\Phi(1)=I$$. Since $$\mathbb C$$ is a field and $$\Phi$$ is an injective homomorphism, its image $$\mathcal M$$ is a field under the matrix operations; for a nonzero element its inverse is $$\Phi((a-ib)/(a^2+b^2))$$. Thus $$\Phi:\mathbb C\to\mathcal M$$ is a field isomorphism, and $$\mathcal M$$ is a subfield of $$M_2(\mathbb R)$$.

### Exercise 11

Put $$A=\sum_{k=0}^{n-1}|a_k|$$ and $$R=1+A$$. For $$\rho=|z|>R$$ and $$n\ge2$$, the triangle inequality and $$\rho>1$$ give

$$
|p(z)|
\ge \rho^n-\sum_{k=0}^{n-1}|a_k|\rho^k
\ge \rho^n-A\rho^{n-1}
=\rho^{n-1}(\rho-A).
$$

Here $$\rho-A>1$$ and $$\rho^{n-1}>R^{n-1}$$. Therefore $$|p(z)|>R^{n-1}\ge R$$, proving the stated bound when $$n\ge2$$.

As printed, the claim is false for $$n=1$$. For example, if $$p(X)=X+1$$, then $$R=2$$, but for $$z=-2.1$$ we have $$|z|>R$$ and $$|p(z)|=1.1<R$$.

### Exercise 12

Expanding both squared moduli and adding cancels the mixed terms:

$$
\begin{aligned}
|z+w|^2+|z-w|^2
&=(z+w)(\overline z+\overline w)+(z-w)(\overline z-\overline w)\\
&=2z\overline z+2w\overline w\\
&=2(|z|^2+|w|^2).
\end{aligned}
$$

### Exercise 13

For $$z=re^{i\theta}\ne0$$, where $$r>0$$,

$$
\frac1z=\frac1r e^{-i\theta}.
$$

Thus the map reflects the argument across the real axis and replaces the distance from the origin $$r$$ by $$1/r$$. Equivalently, it is reflection in the real axis followed by inversion in the unit circle. In Cartesian coordinates,

$$
x+iy\longmapsto \frac{x-iy}{x^2+y^2}.
$$

### Exercise 14

The constant term is nonzero, so a zero cannot be $$0$$. For $$z\ne0$$, divide by $$z^2$$ and set $$y=z-1/z$$. Since $$z^2+z^{-2}=y^2+2$$,

$$
\frac{z^4-2z^3-z^2+2z+1}{z^2}
=z^2+z^{-2}-2(z-z^{-1})-1
=(y-1)^2.
$$

Hence the polynomial is $$\bigl(z^2-z-1\bigr)^2$$. Its zeros are

$$
z=\frac{1+\sqrt5}{2}\quad\text{and}\quad z=\frac{1-\sqrt5}{2},
$$

each with multiplicity two.

### Exercise 15

Substitute $$X=Y-a/3$$ into $$k(X)=X^3+aX^2+bX+c$$. The quadratic term vanishes and

$$
k(Y-a/3)=Y^3+pY+q,\qquad
p=b-\frac{a^2}{3},\quad
q=\frac{2a^3}{27}-\frac{ab}{3}+c.
$$

Now suppose $$d,u,v$$ satisfy the stated equations. Then

$$
(uv)^3=u^3v^3=\frac{q^2}{4}-d^2=-\frac{p^3}{27}.
$$

If $$p\ne0$$, it follows that $$\tau=-3uv/p$$ satisfies $$\tau^3=1$$. Replacing $$u$$ by $$\tau^{-1}u$$ leaves its cube unchanged and makes $$3uv=-p$$. Also $$u^3+v^3=-q$$.

Let $$\xi$$ be a nontrivial cube root of unity, so $$\xi^3=1$$ and $$1+\xi+\xi^2=0$$. For each of the pairs

$$
(u,v),\qquad(\xi u,\xi^2v),\qquad(\xi^2u,\xi v),
$$

the cubes of the two entries sum to $$-q$$ and their product is $$uv=-p/3$$. Thus if the entries of any pair are $$U,V$$, then

$$
(U+V)^3+p(U+V)+q
=U^3+V^3+(3UV+p)(U+V)+q=0.
$$

Their elementary symmetric functions are

$$
y_1+y_2+y_3=0,\qquad
y_1y_2+y_2y_3+y_3y_1=-3uv=p,\qquad
y_1y_2y_3=u^3+v^3=-q.
$$

Thus $$Y^3+pY+q=(Y-y_1)(Y-y_2)(Y-y_3)$$, and the three values

$$
y_1=u+v,\qquad y_2=\xi u+\xi^2v,\qquad y_3=\xi^2u+\xi v
$$

are the roots of $$Y^3+pY+q$$, counted with multiplicity. The corresponding roots of the original cubic are $$X=y_j-a/3$$.

If $$p=0$$, the quotient defining $$\tau$$ is not available. In this case $$(uv)^3=0$$, so one of $$u,v$$ is zero; the same three expressions directly give the cube roots of $$-q$$. If also $$q=0$$, all three roots are $$0$$.
