# Chapter III — Continuous Functions

## 6. The Exponential and Related Functions

### Exercise 1

For $$s,t\in\mathbb{R}$$, Euler’s formula and the half-angle identities give

$$
|e^{it}-e^{is}|=2\left|\sin\frac{t-s}{2}\right|\le |t-s|.
$$

Thus $$\operatorname{cis}$$ is Lipschitz continuous with constant $$1$$. The addition formulas give

$$
|\sin t-\sin s|
=2\left|\cos\frac{t+s}{2}\sin\frac{t-s}{2}\right|
\le |t-s|
$$

and

$$
|\cos t-\cos s|
=2\left|\sin\frac{t+s}{2}\sin\frac{t-s}{2}\right|
\le |t-s|.
$$

The bound $$|\sin u|\le |u|$$ follows from Example 2.25(b). For $$\operatorname{cis}$$ the quotient of the left side by $$|t-s|$$ tends to $$1$$ as $$t-s\to0$$. For $$\sin$$, take $$s=0$$ and let $$t\to0$$; for $$\cos$$, take $$s=\pi/2$$ and let $$t\to\pi/2$$. These limits show that the Lipschitz constant is exactly $$1$$ in all three cases.

### Exercise 2

By Euler’s formula and the addition theorem for the exponential,

$$
(\cos z+i\sin z)^m=(e^{iz})^m=e^{imz}=\cos(mz)+i\sin(mz).
$$

This also holds for $$m=0$$, with both sides equal to $$1$$.

### Exercise 3

**(a)** Apply the addition formulas at $$z/2+z/2$$ and use $$\cos^2(z/2)+\sin^2(z/2)=1$$:

$$
\cos z=\cos^2(z/2)-\sin^2(z/2).
$$

Adding and subtracting this identity and $$1=\cos^2(z/2)+\sin^2(z/2)$$ gives

$$
\cos^2(z/2)=\frac{1+\cos z}{2},
\qquad
\sin^2(z/2)=\frac{1-\cos z}{2}.
$$

**(b)** The half-angle formulas imply

$$
1-\cos z=2\sin^2(z/2),\qquad
1+\cos z=2\cos^2(z/2),\qquad
\sin z=2\sin(z/2)\cos(z/2).
$$

For $$z\notin\pi\mathbb{Z}$$, the denominators in the question are nonzero, and division yields

$$
\tan(z/2)=\frac{1-\cos z}{\sin z}
=\frac{\sin z}{1+\cos z}.
$$

### Exercise 4

Write $$\cosh z=(e^z+e^{-z})/2$$ and $$\sinh z=(e^z-e^{-z})/2$$.

**(a)** Factoring a difference of squares gives

$$
\cosh^2z-\sinh^2z
=\frac{(e^z+e^{-z})^2-(e^z-e^{-z})^2}{4}=1.
$$

**(b)–(c)** Expanding and using $$e^{z+w}=e^ze^w$$ gives

$$
\cosh z\cosh w+\sinh z\sinh w
=\frac{e^{z+w}+e^{-(z+w)}}2
=\cosh(z+w)
$$

and

$$
\sinh z\cosh w+\cosh z\sinh w
=\frac{e^{z+w}-e^{-(z+w)}}2
=\sinh(z+w).
$$

**(d)** Substitute $$iz$$ into the definitions of cosine and sine:

$$
\cos(iz)=\frac{e^{iz}+e^{-iz}}2=\cosh z,
\qquad
-i\sin(iz)=-i\frac{e^{-z}-e^z}{2i}=\sinh z.
$$

**(e)** Splitting the exponential series into even and odd powers yields

$$
\cosh z=\frac{e^z+e^{-z}}2
=\sum_{k=0}^{\infty}\frac{z^{2k}}{(2k)!},
\qquad
\sinh z=\frac{e^z-e^{-z}}2
=\sum_{k=0}^{\infty}\frac{z^{2k+1}}{(2k+1)!}.
$$

### Exercise 5

For real arguments, $$\cosh$$ is even and has a minimum $$1$$ at $$0$$; its graph is U-shaped. The function $$\sinh$$ is odd and strictly increasing through the origin. The function $$\tanh$$ is odd and strictly increasing, with horizontal asymptotes $$y=\pm1$$. The function $$\coth$$ is odd and strictly decreasing on each side of its vertical asymptote $$x=0$$; its horizontal asymptotes are $$y=1$$ as $$x\to+\infty$$ and $$y=-1$$ as $$x\to-\infty$$.

**(a)** The exponential function is continuous, so $$\cosh$$ and $$\sinh$$ are continuous on $$\mathbb{C}$$. The zeros of $$\cosh z$$ are $$i\pi(\mathbb{Z}+1/2)$$, and the zeros of $$\sinh z$$ are $$i\pi\mathbb{Z}$$. Therefore their quotients $$\tanh$$ and $$\coth$$ are continuous on the domains stated in the exercise.

**(b)** For real $$x$$,

$$
\tanh x=\frac{1-e^{-2x}}{1+e^{-2x}},
\qquad
\coth x=\frac{e^{2x}+1}{e^{2x}-1}.
$$

These formulas give

$$
\lim_{x\to+\infty}\tanh x=1,\quad
\lim_{x\to-\infty}\tanh x=-1,\quad
\lim_{x\to0^+}\coth x=+\infty,\quad
\lim_{x\to0^-}\coth x=-\infty.
$$

**(c)** If $$0\le x<y$$, then

$$
\cosh y-\cosh x
=2\sinh\frac{x+y}{2}\sinh\frac{y-x}{2}>0.
$$

Thus $$\cosh$$ is strictly increasing on $$[0,\infty)$$. It is continuous, starts at $$1$$, and tends to $$+\infty$$, so its image there is $$[1,\infty)$$.

**(d)** If $$x<y$$, then

$$
\sinh y-\sinh x
=2\cosh\frac{x+y}{2}\sinh\frac{y-x}{2}>0.
$$

Hence $$\sinh$$ is strictly increasing. Its defining formula shows that it tends to $$+\infty$$ as $$x\to+\infty$$ and to $$-\infty$$ as $$x\to-\infty$$. Continuity and the intermediate value theorem show that it is onto $$\mathbb{R}$$, hence bijective.

**(e)** For $$x<y$$,

$$
\tanh y-\tanh x
=\frac{\sinh(y-x)}{\cosh x\cosh y}>0.
$$

Together with the limits in (b), continuity and the intermediate value theorem show that $$\tanh$$ is a strictly increasing bijection from $$\mathbb{R}$$ onto $$(-1,1)$$.

**(f)** For $$0<x<y$$,

$$
\coth x-\coth y
=\frac{\sinh(y-x)}{\sinh x\sinh y}>0.
$$

Thus $$\coth$$ is strictly decreasing on $$(0,\infty)$$. Its limits at the endpoints are $$+\infty$$ and $$1$$, so its image is $$(1,\infty)$$.

**(g)** Let $$x<y$$, put $$h=y-x$$ and $$m=(x+y)/2$$. The identities for hyperbolic functions give

$$
\tanh y-\tanh x
=\frac{\sinh h}{\cosh x\cosh y},
\qquad
\cosh x\cosh y
=\frac{\cosh(2m)+\cosh h}{2}
\ge \cosh^2(h/2).
$$

For $$u\ge0$$, the power series show that

$$
u\cosh u-\sinh u
=\sum_{k=1}^{\infty}\frac{2k\,u^{2k+1}}{(2k+1)!}\ge0,
$$

so $$\tanh u\le u$$. Consequently,

$$
0\le\tanh y-\tanh x
\le\frac{\sinh h}{\cosh^2(h/2)}
=2\tanh(h/2)\le h.
$$

Interchanging $$x$$ and $$y$$ proves $$|\tanh y-\tanh x|\le|y-x|$$. Since $$\tanh h/h\to1$$ as $$h\to0$$, the constant $$1$$ is sharp.

### Exercise 6

**(a)** Since $$x^x=e^{x\log x}$$ and $$x\log x\to0$$ as $$x\to0^+$$,

$$
\lim_{x\to0^+}x^x=1.
$$

**(b)** Since $$x^{1/x}=e^{(\log x)/x}$$ and $$\log x/x\to-\infty$$ as $$x\to0^+$$,

$$
\lim_{x\to0^+}x^{1/x}=0.
$$

**(c)** Set $$w=\log(1+z)$$. As $$z\to0$$, continuity of the logarithm near $$1$$ gives $$w\to0$$ and $$e^w=1+z$$. Therefore

$$
\frac{\log(1+z)}{z}
=\frac{w}{e^w-1}\longrightarrow1,
$$

using $$\lim_{w\to0}(e^w-1)/w=1$$.

### Exercise 7

The arithmetic-geometric mean inequality gives $$\sqrt{xy}\le(x+y)/2$$. Since the logarithm is increasing,

$$
\frac{\log x+\log y}{2}
=\log\sqrt{xy}
\le\log\left(\frac{x+y}{2}\right).
$$

Equality holds exactly when $$x=y$$.

### Exercise 8

**(a)** The sine power series gives

$$
\frac{\sin z}{z}
=1-\frac{z^2}{3!}+\frac{z^4}{5!}-\cdots
\longrightarrow1
\quad\text{as }z\to0.
$$

**(b)** For the principal value of the power, $$a^z=e^{z\log a}$$. Thus

$$
\frac{a^z-1}{z}
=\frac{e^{z\log a}-1}{z}
\longrightarrow\log a
\quad\text{as }z\to0,
$$

where $$\log a$$ is the principal value of the logarithm.

### Exercise 9

The map $$\nu(z)=z/|z|$$ is continuous from $$\mathbb{C}\setminus(-\infty,0]$$ to $$S^1\setminus\{-1\}$$. On any interval $$[-a,a]$$ with $$0<a<\pi$$, the restriction of $$\operatorname{cis}$$ is a continuous bijection from a compact space to a Hausdorff space. It is therefore a homeomorphism onto its image. These arcs give neighborhoods of every point of $$S^1\setminus\{-1\}$$, so the inverse

$$
\operatorname{arg}:S^1\setminus\{-1\}\longrightarrow(-\pi,\pi)
$$

is continuous. Since the principal argument on the slit plane is this inverse composed with $$\nu$$, it is continuous there. Finally,

$$
\log z=\log|z|+i\operatorname{arg}z
$$

is continuous on the same domain.

### Exercise 10

For the first identity, by definition of the principal value,

$$
z^a z^b
=e^{a\log z}e^{b\log z}
=e^{(a+b)\log z}
=z^{a+b}.
$$

The second identity in the exercise is false for principal values in general. For example, with $$z=w=-1$$ and $$a=1/2$$,

$$
z^a w^a=i^2=-1,
\qquad
(zw)^a=1^{1/2}=1.
$$

More generally, if $$\log z+\log w=\log(zw)+2\pi i k$$ for an integer $$k$$, then

$$
z^a w^a=(zw)^a e^{2\pi i k a}.
$$

Thus the claimed equality holds when the factor $$e^{2\pi i k a}$$ is $$1$$, for example when the principal arguments of $$z$$ and $$w$$ have a sum in $$(-\pi,\pi]$$, so that $$k=0$$. It does not hold for all $$z,w,a$$ as printed.

### Exercise 11

The set-valued complex logarithm of $$i$$ is $$\operatorname{Log}(i)=i(\pi/2+2\pi\mathbb{Z})$$. Hence the set of values of $$i^i$$ is

$$
i^i
=\left\{e^{i\cdot i(\pi/2+2\pi k)}:k\in\mathbb{Z}\right\}
=\left\{e^{-\pi/2-2\pi k}:k\in\mathbb{Z}\right\}.
$$

Using the principal logarithm, the principal value is $$e^{-\pi/2}$$.

### Exercise 12

For every $$k=1,\ldots,n$$, the addition theorem gives

$$
|z_{n,k}-z_{n,k-1}|
=\left|e^{ixk/n}-e^{ix(k-1)/n}\right|
=\left|e^{ix/n}-1\right|
=2\left|\sin\frac{x}{2n}\right|.
$$

Summing the $$n$$ equal chord lengths yields

$$
L_n=2n\left|\sin\frac{x}{2n}\right|.
$$

Since $$\sin u/u\to1$$ as $$u\to0$$,

$$
\lim_{n\to\infty}L_n
=|x|\lim_{n\to\infty}
\left|\frac{\sin(x/(2n))}{x/(2n)}\right|
=|x|.
$$

For $$x=0$$, both sides are $$0$$ directly.

### Exercise 13

For $$z=x+iy$$,

$$
z^2=(x^2-y^2)+i\,2xy.
$$

Write $$w=u+iv=z^2$$. The hyperbola $$x^2-y^2=c$$ maps onto the vertical line $$u=c$$: every point $$c+iv$$ has a square root, whose real and imaginary parts satisfy $$x^2-y^2=c$$. Similarly, $$xy=c$$ maps onto the horizontal line $$v=2c$$, since every point $$u+2ci$$ has a square root with $$2xy=2c$$.

On the vertical line $$x=c$$, parameterized by $$y\in\mathbb{R}$$, the image is

$$
w=(c^2-y^2)+i\,2cy.
$$

If $$c\ne0$$, eliminating $$y$$ gives the left-opening parabola

$$
u=c^2-\frac{v^2}{4c^2}.
$$

For $$c=0$$ the image is the nonpositive real axis. On the horizontal line $$y=c$$, the image is

$$
w=(x^2-c^2)+i\,2cx.
$$

If $$c\ne0$$, this is the right-opening parabola

$$
u=\frac{v^2}{4c^2}-c^2.
$$

For $$c=0$$ the image is the nonnegative real axis.

### Exercise 14

**(a)** The right side has modulus $$1$$ and argument $$\pi/4$$. Its fourth roots are

$$
z_k=e^{i(\pi/16+k\pi/2)},\qquad k=0,1,2,3.
$$

**(b)** Since $$i=e^{i\pi/2}$$, the fifth roots are

$$
z_k=e^{i(\pi/10+2\pi k/5)},\qquad k=0,1,2,3,4.
$$

**(c)** Let $$\omega=e^{2\pi i/3}$$. The equation is depressed, and Cardano’s formula gives the three roots

$$
z_k=\omega^k\sqrt[3]{2}-\omega^{-k}\sqrt[3]{4},
\qquad k=0,1,2.
$$

Indeed, the two cube-root terms have product $$-2$$, and their cubes sum to $$-2$$, so their sum satisfies $$z^3+6z+2=0$$.

**(d)** Factoring gives

$$
z^3+(1-2i)z^2-(1+2i)z-1
=(z+1)(z-i)^2.
$$

Thus the solutions are $$z=-1$$ and $$z=i$$, with $$i$$ a double root.

### Exercise 15

For fixed $$n$$, the limit defining $$f_n(x)$$ equals $$1$$ if $$|\cos(n!\pi x)|=1$$ and equals $$0$$ otherwise. For real arguments, $$|\cos(m\pi)|=1$$ exactly when $$m\in\mathbb{Z}$$. Therefore

$$
f_n(x)=
\begin{cases}
1,&n!x\in\mathbb{Z},\\
0,&n!x\notin\mathbb{Z}.
\end{cases}
$$

If $$x$$ is irrational, $$n!x$$ is never an integer, so $$f_n(x)=0$$ for every $$n$$. If $$x=p/q$$ is rational in lowest terms, then $$q\mid n!$$ for every $$n\ge q$$, so $$f_n(x)=1$$ eventually. Consequently,

$$
\lim_{n\to\infty}f_n(x)=
\begin{cases}
1,&x\in\mathbb{Q},\\
0,&x\notin\mathbb{Q}.
\end{cases}
$$

### Exercise 16

Suppose, for contradiction, that $$\cosh 1=p/q$$ with integers $$p$$ and $$q>0$$. Choose $$n\ge1$$ large enough that $$q\mid(2n)!$$. Then both

$$
(2n)!\cosh 1
\quad\text{and}\quad
(2n)!\sum_{k=0}^{n}\frac1{(2k)!}
$$

are integers. Their difference is therefore an integer:

$$
T_n=(2n)!\sum_{k=n+1}^{\infty}\frac1{(2k)!}.
$$

But $$T_n>0$$, and its first term is $$1/((2n+1)(2n+2))$$; each subsequent term is smaller than the preceding one by a factor at most $$1/((2n+3)(2n+4))<1$$. Bounding the tail by the corresponding geometric series gives

$$
T_n<
\frac{1}{(2n+1)(2n+2)}
\cdot\frac{1}{1-\frac1{(2n+3)(2n+4)}}<1.
$$

This contradicts that $$T_n$$ is an integer. Hence $$\cosh 1$$ is irrational.
