# Chapter VIII — Line Integrals

## 6. Meromorphic functions

These solutions address Exercises 1–21. We write $$D(a,r)=\{z:|z-a|<r\}$$ and take circle boundaries counterclockwise. Meromorphic functions are understood up to removable extension. Exercises 12–15 require attention to their printed parameters or hypotheses, as explained below.

### Exercise 1

Let $$A=\operatorname{Res}(g,w_0)$$. Near $$w_0$$ write $$g(w)=A/(w-w_0)+h(w)$$ with $$A\ne0$$ and $$h$$ holomorphic. Since $$f(z)-w_0=(z-z_0)u(z)$$ with $$u(z_0)=f'(z_0)\ne0$$, shrink the neighborhood so that $$u$$ is nonzero there and $$f(z)\ne w_0$$ for $$z\ne z_0$$. Then

$$
g(f(z))=\frac{A}{(z-z_0)u(z)}+h(f(z)).
$$

The second term is holomorphic and the first has a simple pole. Its residue is $$A/u(z_0)=\operatorname{Res}(g,w_0)/f'(z_0)$$.

### Exercise 2

The implication is false. For $$f(z)=1/(z-1)$$ and $$1<|z|<2$$, the geometric series gives

$$
f(z)=\frac{1/z}{1-1/z}=\sum_{n=1}^{\infty}z^{-n}.
$$

Every negative coefficient is nonzero, yet $$f$$ is meromorphic on the plane, with a simple pole at $$1$$ and no essential singularity. The annulus does not approach its center: its negative powers encode the behavior of singularities inside the inner circle, not necessarily an isolated singularity at $$0$$.

### Exercise 3

The partial fraction decomposition is $$f(z)=1/(z-a)-1/(z-b)$$. Expanding each term in its appropriate geometric series gives the following Laurent expansions about zero:

$$
\begin{aligned}
|z|<|a|:\quad &\sum_{n=0}^{\infty}\left(\frac1{b^{n+1}}-\frac1{a^{n+1}}\right)z^n,\\
|a|<|z|<|b|:\quad &\sum_{n=0}^{\infty}a^n z^{-n-1}+\sum_{n=0}^{\infty}\frac{z^n}{b^{n+1}},\\
|z|>|b|:\quad &\sum_{n=0}^{\infty}(a^n-b^n)z^{-n-1}.
\end{aligned}
$$

For example, $$1/(z-a)=z^{-1}\sum_{n\ge0}(a/z)^n$$ when $$|z|>|a|$$, whereas $$1/(z-b)=-b^{-1}\sum_{n\ge0}(z/b)^n$$ when $$|z|<|b|$$. The displayed restrictions ensure convergence of both constituent series.

At $$a$$, put $$\zeta=z-a$$. Since the other pole is at distance $$|a-b|$$,

$$
f(z)=\frac1\zeta-\frac1{a-b+\zeta}
=\frac1\zeta-\sum_{n=0}^{\infty}\frac{(-1)^n\zeta^n}{(a-b)^{n+1}},\qquad 0<|\zeta|<|a-b|.
$$

### Exercise 4

The poles of $$4/(1+4z^2)$$ inside the unit circle are $$\pm i/2$$. Their residues are respectively $$1/i$$ and $$-1/i$$, so their sum and the first integral are zero.

For the second integral the only zero of $$1-e^z$$ inside the unit circle is $$0$$. As $$z\to0$$,

$$
\frac{e^z\sin z}{(1-e^z)^2}
=\frac{z+O(z^2)}{z^2(1+O(z))}=\frac1z+O(1).
$$

Its residue is $$1$$, and the integral is $$2\pi i$$.

### Exercise 5

Assume $$n\ge1$$. The Laurent definition of a pole of order $$n$$ is equivalent to $$f(z)=(z-z_0)^{-n}g(z)$$ with $$g$$ holomorphic near $$z_0$$ and $$g(z_0)\ne0$$. This proves (i) iff (ii).

For (ii) implies (iii), continuity and nonvanishing of $$g$$ give $$0<M_1\le|g(z)|\le M_2$$ on a sufficiently small disc; divide by $$|z-z_0|^n$$. Conversely, (iii) makes $$g=(z-z_0)^n f$$ bounded on a punctured disc, so it extends holomorphically across $$z_0$$. The lower bound gives $$|g(z_0)|\ge M_1>0$$ by continuity, proving (ii).

### Exercise 6

A pole has the local form $$f(z)=(z-z_0)^{-m}h(z)$$ with $$m\ge1$$ and $$h(z_0)\ne0$$, hence $$|f(z)|\to\infty$$. Conversely, if this limit holds, then $$f$$ has no zeros sufficiently near $$z_0$$ and $$1/f$$ is bounded there and tends to zero. Its removable extension $$g$$ satisfies $$g(z_0)=0$$ and is not identically zero. Thus $$g(z)=(z-z_0)^m h(z)$$ for some $$m\ge1$$ and holomorphic $$h$$ with $$h(z_0)\ne0$$. Taking reciprocals shows that $$f$$ has a pole of order $$m$$.

### Exercise 7

Suppose the singularity is essential. If some $$w_0$$ is not a limit along any sequence approaching $$z_0$$, then there are $$r,s>0$$ such that $$|f(z)-w_0|\ge s$$ on $$0<|z-z_0|<r$$. Thus $$g=1/(f-w_0)$$ is bounded and extends holomorphically to $$z_0$$. If $$g(z_0)\ne0$$, then $$f=w_0+1/g$$ extends holomorphically; if $$g(z_0)=0$$, the zero of $$g$$ has finite positive order and $$f$$ has a pole. Both contradict essentiality. Therefore, for each $$n$$, one may choose $$z_n$$ with $$0<|z_n-z_0|<1/n$$ and $$|f(z_n)-w_0|<1/n$$.

Conversely, the stated approximation property excludes a pole, since then $$|f(z)|\to\infty$$, and excludes a removable singularity, since then all finite limits equal the value of the extension. The classification of isolated singularities leaves the essential case.

### Exercise 8

For $$F(z)=e^{1/(z-1)}/(e^z-1)$$, the denominator has simple zeros at $$2\pi ik$$, $$k\in\mathbb Z$$. The numerator is nonzero and holomorphic there, so all these points are simple poles, with residues $$e^{1/(2\pi ik-1)}$$. At $$1$$ the denominator is holomorphic and nonzero; multiplying or dividing by a holomorphic nonvanishing function cannot turn the essential singularity of $$e^{1/(z-1)}$$ into a removable singularity or a pole. Thus $$1$$ is essential. There are no other finite singularities.

For $$G(z)=(z+1)\sin(1/(z-1))$$, the only finite singularity is at $$1$$. The Laurent expansion of the sine has infinitely many nonzero negative terms, and $$z+1$$ is nonzero at $$1$$, so this singularity is essential.

### Exercise 9

Choose the square-root branch near $$-1$$ taking the value $$i$$ at $$-1$$. Let $$z_n^2=-1+1/n$$ and $$w_n^2=-1+1/(in)$$ on that branch. Both sequences approach $$i$$ and avoid it. Yet

$$
\sin\!\left(\frac{\pi}{z_n^2+1}\right)=\sin(\pi n)=0,
\qquad
\left|\sin\!\left(\frac{\pi}{w_n^2+1}\right)\right|=\sinh(\pi n)\to\infty.
$$

The first sequence excludes a pole and the second excludes a removable singularity. Hence $$i$$ is essential.

### Exercise 10

If a primitive exists, its integral around every closed curve in $$U\setminus\{a\}$$ vanishes; integrating around a small positively oriented circle about $$a$$ gives $$2\pi i\operatorname{Res}(f,a)=0$$.

Conversely, suppose the residue is zero. Every closed piecewise $$C^1$$ curve $$\Gamma$$ in $$U\setminus\{a\}$$ is null homologous in the simply connected set $$U$$ (Exercise 11). Choose a small positively oriented circle $$C$$ around $$a$$ whose closed disc lies in $$U$$ and avoids $$\Gamma$$. The cycle $$\Gamma-w(\Gamma,a)C$$ has winding number zero at $$a$$ and at every point outside $$U$$, hence is null homologous in $$U\setminus\{a\}$$. Cauchy's theorem there and the Laurent expansion on $$C$$ yield

$$
\int_\Gamma f(z)\,dz=2\pi i\,w(\Gamma,a)\operatorname{Res}(f,a)=0.
$$

This argument also covers an essential singularity. Vanishing of all closed-curve integrals makes the path integral from a fixed basepoint path independent, and defines a holomorphic primitive.

### Exercise 11

Let $$\Gamma$$ be a closed piecewise $$C^1$$ curve in simply connected $$U$$. It is homotopic in $$U$$ to a constant loop. For every $$a\notin U$$, this is a homotopy in $$\mathbb C\setminus\{a\}$$, so homotopy invariance of the winding number gives $$w(\Gamma,a)=0$$. This is precisely null homology in $$U$$. Equivalently, $$1/(z-a)$$ has a primitive on $$U$$, making its integral along $$\Gamma$$ zero.

### Exercise 12

The printed integrand uses $$r$$ while the hypothesis and answer use $$p$$. The intended exponent is $$p$$. More generally, the derivation below holds with any real exponent in $$(0,1)$$, and gives the corresponding sine in the denominator.

Set $$F(z)=e^{pz}/(1+e^z)$$ and $$I_R=\int_{-R}^R e^{px}/(1+e^x)\,dx$$. Integrate counterclockwise around the rectangle with vertices $$\pm R$$ and $$\pm R+2\pi i$$. Its only pole is at $$\pi i$$, with residue $$-e^{\pi ip}$$. The bottom contribution is $$I_R$$ and the reversed top contribution is $$-e^{2\pi ip}I_R$$. On the right vertical side $$|F|\le e^{pR}/(e^R-1)$$; on the left $$|F|\le e^{-pR}/(1-e^{-R})$$. Both side integrals tend to zero. The residue theorem therefore gives

$$
(1-e^{2\pi ip})\lim_{R\to\infty}I_R=-2\pi i e^{\pi ip},\qquad
\lim_{R\to\infty}I_R=\frac{\pi}{\sin(\pi p)}.
$$

The integral actually converges separately at both ends, because the integrand is $$O(e^{px})$$ at $$-\infty$$ and $$O(e^{-(1-p)x})$$ at $$+\infty$$; thus its principal value equals the ordinary improper integral.

### Exercise 13

Winding numbers require closed curves, so take the parametrizations to be closed, as the notation $$w(\Gamma_j,z)$$ presupposes. The inequality also implies that neither curve passes through $$z$$. Define

$$
q(t)=\frac{\gamma_1(t)-z}{\gamma_0(t)-z}.
$$

It is a closed piecewise $$C^1$$ curve in $$D(1,1)$$, which does not contain zero, because $$|q(t)-1|<1$$. The straight-line homotopy to the constant curve $$1$$ stays in that disc, so $$w([q],0)=0$$. Logarithmic differentiation and integration show

$$
w([q],0)=\frac1{2\pi i}\int\left(\frac{\gamma_1'}{\gamma_1-z}-\frac{\gamma_0'}{\gamma_0-z}\right)dt
=w(\Gamma_1,z)-w(\Gamma_0,z).
$$

Hence the winding numbers are equal.

### Exercise 14

The assertion needs $$f$$ to be nonzero on every connected component of $$U$$; in particular, it holds for nonzero $$f$$ when $$U$$ is connected. Without this, a function identically zero on one component is a counterexample to discreteness and has no meromorphic reciprocal there.

Under that hypothesis, near any non-pole the zeros are isolated by the identity theorem. Near a pole $$p$$ of order $$m$$, write $$f(z)=(z-p)^{-m}h(z)$$ with $$h(p)\ne0$$; after shrinking the disc, $$h$$ is nonzero, so there are no nearby zeros. Hence $$N(f)$$ has no accumulation point in $$U$$ and is relatively closed and discrete.

At a zero $$a$$ of order $$m$$, $$f(z)=(z-a)^m h(z)$$ with $$h(a)\ne0$$, so $$1/f$$ has a pole of order $$m$$. At a pole $$p$$ of order $$m$$, its reciprocal extends as $$(z-p)^m/h(z)$$, with a zero of order $$m$$. Elsewhere it is holomorphic and nonzero. Thus the meromorphic reciprocal has exactly the stated poles and zeros; values at former poles are supplied by removable extension.

### Exercise 15

For a nonempty connected open $$U$$, the meromorphic functions form a field, with operations followed by removable extension where needed. Locally at any point, $$f=(z-a)^{-m}u$$ and $$g=(z-a)^{-n}v$$ for nonnegative integers $$m,n$$ and holomorphic $$u,v$$. Thus $$f+g$$ and $$fg$$ are holomorphic after multiplication by a sufficiently high power of $$z-a$$; their apparent singularities are removable or poles. Their possible poles lie in the union of the two relatively closed discrete pole sets, so they are meromorphic. Associativity, distributivity and the other ring laws hold on the common holomorphic domain and hence after unique removable extension. The constant functions $$0$$ and $$1$$ are distinct.

By Exercise 14 every nonzero meromorphic function has a meromorphic reciprocal, giving the multiplicative inverse. If $$U$$ is disconnected, the printed field claim fails: take the characteristic functions of two disjoint nonempty unions of components. They are nonzero holomorphic functions with zero product. Thus connectedness (and nonemptiness) is needed.

### Exercise 16

Integrate $$F(z)=z^2/(1+z^4)$$ over the upper semicircle of radius $$R>1$$. The upper poles are $$\alpha=e^{i\pi/4}$$ and $$\beta=e^{3i\pi/4}$$, and each is simple with residue $$1/(4z)$$. Hence

$$
\operatorname{Res}(F,\alpha)+\operatorname{Res}(F,\beta)
=\frac14(e^{-i\pi/4}+e^{-3i\pi/4})=-\frac{i\sqrt2}{4}.
$$

On the arc, $$|F(z)|\le R^2/(R^4-1)$$ and its length is $$\pi R$$, so the arc contribution vanishes. Passing to the limit in the residue theorem gives $$\int_{-\infty}^{\infty}x^2/(1+x^4)\,dx=\pi/\sqrt2$$.

### Exercise 17

For $$a>0$$ integrate $$F(z)=e^{iz}/(z^2+a^2)$$ over the upper semicircle of radius $$R>a$$. Its only enclosed pole is $$ia$$, with residue $$e^{-a}/(2ia)$$. Since $$|e^{iz}|=e^{-\operatorname{Im}z}\le1$$ on the arc, the arc integral is bounded by $$\pi R/(R^2-a^2)\to0$$. Therefore

$$
\int_{-\infty}^{\infty}\frac{e^{ix}}{x^2+a^2}\,dx=\frac{\pi e^{-a}}a.
$$

The sine term is odd and the cosine term is even; absolute convergence permits taking real parts and splitting the integral. The requested integral is $$\pi e^{-a}/(2a)$$.

### Exercise 18

Assume, as in Exercise 14, that $$f$$ is not identically zero on any component. Locally at a zero or pole $$a$$ write

$$
f(z)=(z-a)^k h(z),\qquad h(a)\ne0,
$$

where $$k=m>0$$ for a zero of order $$m$$ and $$k=-m<0$$ for a pole of order $$m$$. Logarithmic differentiation yields

$$
\frac{f'(z)}{f(z)}=\frac{k}{z-a}+\frac{h'(z)}{h(z)}.
$$

The second term is holomorphic near $$a$$, so the logarithmic derivative has a simple pole there with residue $$m$$ at a zero and $$-m$$ at a pole. At points where $$f$$ is holomorphic and nonzero it is holomorphic. These local formulas prove all three claims. On a component where $$f\equiv0$$ the quotient is undefined, so the additional hypothesis is necessary when $$U$$ is disconnected.

### Exercise 19

With the componentwise nonvanishing assumption of Exercise 18, $$f'/f$$ is meromorphic and avoids poles on $$\Gamma$$. Apply the residue theorem to this function and use Exercise 18. Its poles are exactly the zeros and poles of $$f$$, with residues equal to their signed multiplicities. Therefore

$$
\frac1{2\pi i}\int_\Gamma\frac{f'(z)}{f(z)}\,dz
=\sum_{n\in N(f)}w(\Gamma,n)\nu(n)-\sum_{p\in P(f)}w(\Gamma,p)\nu(p).
$$

Only finitely many summands are nonzero: the winding number vanishes outside a bounded set and, by null homology, outside $$U$$; the relevant zeros and poles form a relatively closed discrete set in $$U$$. Equivalently, the residue theorem supplies this finiteness directly.

### Exercise 20

The denominator factors as $$(z-a)(z-b)$$, and its derivative is the numerator. Thus the integrand is $$1/(z-a)+1/(z-b)$$. Both simple poles lie inside the unit circle, each with residue $$1$$, so the normalized integral is $$2$$. This also follows from the argument principle in Exercise 19.

### Exercise 21

Factor and use partial fractions:

$$
\frac1{x^4+4x^2+3}=\frac1{(x^2+1)(x^2+3)}
=\frac12\left(\frac1{x^2+1}-\frac1{x^2+3}\right).
$$

Using $$\int_{-\infty}^{\infty}dx/(x^2+c^2)=\pi/c$$ for $$c>0$$, obtained for example by the substitution $$x=c\tan t$$, gives

$$
\int_{-\infty}^{\infty}\frac{dx}{x^4+4x^2+3}
=\frac\pi2\left(1-\frac1{\sqrt3}\right).
$$
