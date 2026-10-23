# Chapter IV — Differentiation in One Variable

## 3. Taylor’s Theorem

### Exercise 1

Set $$g:=p^{-\beta}$$. Since $$p\ge\alpha>0$$, this is a well-defined twice continuously differentiable function, and

$$
g''(x)=\beta p(x)^{-\beta-2}\bigl((\beta+1)p'(x)^2-p(x)p''(x)\bigr)\le0.
$$

Thus the hypotheses imply that $$p^{-\beta}$$ is concave. They do not, however, imply the requested conclusion. For example, take $$p(x)=1$$ on $$[0,\infty)$$, with $$\alpha=1/2$$ and any $$\beta>0$$. Then $$p(x)\ge\alpha$$ and

$$
(\beta+1)p'(x)^2=0\le p''(x)p(x)=0,
$$

but the domain has no finite right endpoint and $$p$$ does not tend to infinity. Even if $$R$$ is required to be finite, the same function restricted to $$[0,1)$$ satisfies the hypotheses while $$p(x)\to1$$ as $$x\to1^-$$. Hence Exercise 1 is false as printed; an additional assumption is needed.

### Exercise 2

Assume first that $$\omega\ne0$$. In part (a), the equation is

$$
f''=-\frac{1}{\omega^2}f.
$$

The solution with the prescribed initial values is

$$
f(z)=a\cos\left(\frac z\omega\right)+\omega^2b\sin\left(\frac z\omega\right).
$$

Indeed, this function satisfies the differential equation, has value $$a$$ at zero, and its derivative at zero is $$\omega b$$. Any solution is uniquely determined by these two initial values: differentiating the equation repeatedly determines all derivatives at zero, or equivalently the difference of two solutions solves the same linear equation with zero initial data and is identically zero. The equation also gives derivatives of every order recursively, so $$f\in C^\infty(\mathbb C)$$.

For part (b), the equation is $$f''=f/\omega^2$$. The unique solution is

$$
f(z)=a\cosh\left(\frac z\omega\right)+\omega^2b\sinh\left(\frac z\omega\right).
$$

The same initial-value check and uniqueness argument apply. If $$\omega=0$$, either equation reduces to $$f=0$$. A solution exists exactly when $$a=0$$; in that case the unique solution is $$f\equiv0$$, and the derivative condition is automatically satisfied for every $$b$$.

### Exercise 3

**(a)** Put $$w=z-1$$, so $$z=1+w$$. Expanding the polynomial gives

$$
3(1+w)^3-7(1+w)^2+2(1+w)+4
=2-3w+2w^2+3w^3.
$$

Therefore the Taylor series at $$1$$ (which terminates) is

$$
2-3(z-1)+2(z-1)^2+3(z-1)^3.
$$

**(b)** Since $$e^z=e\,e^{z-1}$$, its Taylor series at $$1$$ is

$$
e^z=e\sum_{k=0}^{\infty}\frac{(z-1)^k}{k!},
$$

which converges for every $$z\in\mathbb C$$.

### Exercise 4

For $$|x|<1$$, subtract the Taylor series of $$\log(1-x)$$ from that of $$\log(1+x)$$:

$$
\log\left(\frac{1+x}{1-x}\right)
=\log(1+x)-\log(1-x)
=2\sum_{j=0}^{\infty}\frac{x^{2j+1}}{2j+1}.
$$

The even powers cancel. Hence, for $$n\ge1$$,

$$
T_n(x)=2\sum_{j=0}^{\lfloor(n-1)/2\rfloor}\frac{x^{2j+1}}{2j+1}.
$$

For $$n=0$$, the Taylor polynomial is $$T_0(x)=0$$.

### Exercise 5

**(a)** Let $$f(x)=x^3/(x-1)^2$$. Its domain is $$\mathbb R\setminus\{1\}$$, and

$$
f'(x)=\frac{x^2(x-3)}{(x-1)^3},
\qquad
f''(x)=\frac{6x}{(x-1)^4}.
$$

On $$(-\infty,1)$$ the function is increasing (the derivative vanishes at $$0$$ but does not change sign). On $$(1,3)$$ it decreases, and on $$(3,\infty)$$ it increases. Thus $$x=3$$ is a local minimum, with $$f(3)=27/4$$; it is the minimum on the component $$(1,\infty)$$, but there is no global extremum on the full domain. The sign of $$f''$$ changes from negative to positive at zero, so $$x=0$$ is an inflection point. The point $$x=1$$ is outside the domain.

**(b)** Let $$f(x)=e^{\sin x}$$. The domain is $$\mathbb R$$, and

$$
f'(x)=e^{\sin x}\cos x,
\qquad
f''(x)=e^{\sin x}\bigl(\cos^2x-\sin x\bigr).
$$

The global maximum $$e$$ occurs at $$x=\pi/2+2k\pi$$, and the global minimum $$e^{-1}$$ occurs at $$x=3\pi/2+2k\pi$$, where $$k\in\mathbb Z$$. To find inflection points, set $$s=\sin x$$. Then $$\cos^2x-\sin x=1-s^2-s$$, whose only root in $$[-1,1]$$ is

$$
\rho=\frac{\sqrt5-1}{2}.
$$

The sign changes at every solution of $$\sin x=\rho$$. Thus the inflection abscissae are

$$
x=\arcsin\rho+2k\pi
\quad\text{and}\quad
x=\pi-\arcsin\rho+2k\pi,
\qquad k\in\mathbb Z.
$$

**(c)** Let $$f(x)=x^n e^{-x^2}$$, where $$n\in\mathbb N$$. The domain is $$\mathbb R$$.

For $$n\ge1$$,

$$
f'(x)=e^{-x^2}x^{n-1}(n-2x^2).
$$

If $$n$$ is odd, the global minimum and maximum occur at

$$
x=-\sqrt{n/2}
\quad\text{and}\quad
x=\sqrt{n/2},
$$

respectively; their values are $$-\bigl(n/(2e)\bigr)^{n/2}$$ and $$\bigl(n/(2e)\bigr)^{n/2}$$. There is no extremum at zero (for odd $$n\ge3$$ it is stationary; for $$n=1$$ it is not). If $$n\ge2$$ is even, zero is the global minimum, with value zero, and both $$x=\pm\sqrt{n/2}$$ are global maxima, with value $$\bigl(n/(2e)\bigr)^{n/2}$$. For $$n=0$$, the function is $$e^{-x^2}$$: it has a global maximum $$1$$ at zero and no minimum; its infimum is zero and is not attained.

For $$n\ge2$$, direct differentiation gives

$$
f''(x)=e^{-x^2}x^{n-2}\left(4x^4-(4n+2)x^2+n(n-1)\right).
$$

Define

$$
r_\pm=\frac{2n+1\pm\sqrt{8n+1}}4.
$$

For even $$n\ge2$$ the inflection points are $$x=\pm\sqrt{r_-},\pm\sqrt{r_+}$$. For odd $$n\ge3$$ they are those four points and $$x=0$$. The small cases are obtained directly: for $$n=0$$ they are $$x=\pm1/\sqrt2$$, and for $$n=1$$ they are $$x=0,\pm\sqrt{3/2}$$.

**(d)** Let $$f(x)=x^2/\log x$$. Its domain is $$(0,1)\cup(1,\infty)$$, and

$$
f'(x)=\frac{x(2\log x-1)}{(\log x)^2},
\qquad
f''(x)=\frac{2(\log x)^2-3\log x+2}{(\log x)^3}.
$$

The numerator of $$f''$$ is positive because its discriminant is $$9-16<0$$. On $$(0,1)$$ the function decreases from the limiting value zero (from below) to $$-\infty$$. On $$(1,\infty)$$ it decreases until $$x=\sqrt e$$ and then increases. Thus $$x=\sqrt e$$ is a local minimum, with value $$2e$$; there is no global minimum on the full domain because the function is unbounded below on $$(0,1)$$, and there is no maximum. The second derivative is negative on $$(0,1)$$ and positive on $$(1,\infty)$$. Since $$1$$ is not in the domain, there is no inflection point.

**(e)** Let $$f(x)=\sqrt[3]{(x-1)^2(x+1)}$$. Its domain is $$\mathbb R$$. Put $$g(x)=(x-1)^2(x+1)$$. Away from $$x=\pm1$$,

$$
f'(x)=\frac{(x-1)(3x+1)}{3|g(x)|^{2/3}}.
$$

Its sign is positive for $$x<-1/3$$ and for $$x>1$$, and negative for $$-1/3<x<1$$. The function is continuous and increasing across $$x=-1$$ as well. Hence $$x=-1/3$$ is a local maximum with value $$\sqrt[3]{32/27}$$, and $$x=1$$ is a local minimum with value zero. Neither is a global extremum, since $$f(x)\to-\infty$$ as $$x\to-\infty$$ and $$f(x)\to+\infty$$ as $$x\to+\infty$$.

For $$x<-1$$, $$f''(x)>0$$, while for $$x>-1$$, away from $$x=1$$,

$$
f''(x)=-\frac{8(x-1)^2}{9|g(x)|^{5/3}}<0.
$$

Thus concavity changes at $$x=-1$$, making it an inflection point (although $$f'(-1)$$ does not exist). At $$x=1$$ the function is not differentiable, and the concavity is downward on both sides, so it is not an inflection point.

**(f)** Let $$f(x)=(\log(3x))^2/x$$. Its domain is $$(0,\infty)$$. Write $$t=\log(3x)$$. Then

$$
f'(x)=\frac{t(2-t)}{x^2},
\qquad
f''(x)=\frac{2(t^2-3t+1)}{x^3}.
$$

The function decreases for $$t<0$$, increases for $$0<t<2$$, and decreases for $$t>2$$. Therefore $$x=1/3$$ is a global minimum, with value zero, and $$x=e^2/3$$ is a local maximum, with value $$12/e^2$$. There is no global maximum because $$f(x)\to\infty$$ as $$x\to0^+$$. The second derivative changes sign when

$$
t=t_\pm:=\frac{3\pm\sqrt5}{2}.
$$

The two inflection points are

$$
\left(\frac{e^{t_\pm}}3,\;3t_\pm^2e^{-t_\pm}\right).
$$

### Exercise 6

For $$a>1$$ define

$$
h(x)=\frac1{1+x}-\frac1{1+ax}
=\frac{(a-1)x}{(1+x)(1+ax)}.
$$

Differentiation gives

$$
h'(x)=\frac{(a-1)(1-ax^2)}{(1+x)^2(1+ax)^2}\le0
\qquad(x\ge1).
$$

Thus $$h(x)\le h(1)=(a-1)/(2(a+1))$$. To compare this with the stated bound, put $$u=\sqrt a>1$$. Then

$$
\frac{a-1}{2(a+1)}\le\frac{\sqrt a-1}{\sqrt a+1}
\quad\Longleftrightarrow\quad
(u+1)^2\le2(u^2+1),
$$

which follows from $$(u-1)^2\ge0$$. This proves the inequality.

### Exercise 7

Let $$F(t)=(1+t)^s$$ on $$(-1,\infty)$$. Its derivatives are

$$
F^{(k)}(t)=s(s-1)\cdots(s-k+1)(1+t)^{s-k}.
$$

Taylor’s theorem with the Lagrange remainder, applied between $$0$$ and a fixed $$x>-1$$, gives a point $$\tau\in(0,1)$$ such that

$$
(1+x)^s
=\sum_{k=0}^n\binom{s}{k}x^k
+\binom{s}{n+1}\frac{x^{n+1}}{(1+\tau x)^{n+1-s}}.
$$

When $$x=0$$ the identity holds for any $$\tau\in(0,1)$$. The interval between $$0$$ and $$x$$ lies in $$(-1,\infty)$$, so the derivatives used by Taylor’s theorem are defined throughout it.

### Exercise 8

Since $$30=2^5(1-1/16)$$,

$$
\sqrt[5]{30}=2(1-1/16)^{1/5}.
$$

Use Exercise 7 with $$s=1/5$$, $$x=-1/16$$, and $$n=3$$. The first four terms give

$$
\sqrt[5]{30}\approx
2\left(1-\frac1{80}-\frac1{3200}-\frac3{256000}\right)
=1.9743515625.
$$

Here $$\binom{1/5}{4}=-21/625$$. The remainder formula, together with $$1-\tau/16\ge15/16$$, yields

$$
\left|\sqrt[5]{30}-1.9743515625\right|
\le
\frac{42}{625\cdot16^4}\left(\frac{16}{15}\right)^{19/5}
<1.33\cdot10^{-6}.
$$

### Exercise 9

Set $$c_k=\binom{s}{k}$$. Unless the series terminates, its successive coefficients satisfy

$$
\frac{c_{k+1}}{c_k}=\frac{s-k}{k+1},
\qquad
\lim_{k\to\infty}\left|\frac{c_{k+1}}{c_k}\right|=1.
$$

The ratio test therefore shows that $$S(x)=\sum_{k=0}^{\infty}c_kx^k$$ converges for $$|x|<1$$; the same is immediate if it terminates. It may be differentiated term by term there. The coefficient recurrence implies

$$
(1+x)S'(x)=sS(x),\qquad S(0)=1.
$$

The function $$F(x)=(1+x)^s$$ on $$(-1,1)$$ satisfies the same differential equation and initial value. In fact,

$$
\frac{d}{dx}\left((1+x)^{-s}S(x)\right)=0,
$$

so $$S(x)/(1+x)^s$$ is constant on $$(-1,1)$$. Its value at zero is one. Consequently

$$
(1+x)^s=\sum_{k=0}^{\infty}\binom{s}{k}x^k,\qquad -1<x<1.
$$

### Exercise 10

Suppose first that $$f$$ has a zero of multiplicity at least $$n$$ at $$x_0$$, so that $$f^{(j)}(x_0)=0$$ for $$0\le j<n$$. Taylor’s theorem gives

$$
f(x)=\frac{f^{(n)}(x_0)}{n!}(x-x_0)^n+o(|x-x_0|^n)
\qquad(x\to x_0).
$$

For $$x\ne x_0$$ define $$g(x)=f(x)/(x-x_0)^n$$, and set $$g(x_0)=f^{(n)}(x_0)/n!$$. The expansion shows that $$g$$ is continuous at $$x_0$$; away from $$x_0$$ it is a quotient of continuous functions with nonzero denominator. Thus $$g\in C(X,\mathbb K)$$ and $$f(x)=(x-x_0)^ng(x)$$.

Conversely, suppose $$f(x)=(x-x_0)^ng(x)$$ for a continuous $$g$$. Then $$f(x)=O(|x-x_0|^n)$$ near $$x_0$$. Taylor’s theorem for the given $$C^n$$ function writes

$$
f(x)=\sum_{j=0}^n\frac{f^{(j)}(x_0)}{j!}(x-x_0)^j+o(|x-x_0|^n).
$$

The bound $$f(x)=O(|x-x_0|^n)$$ forces each coefficient of degree below $$n$$ in this expansion to vanish: otherwise the lowest nonzero power would make $$f(x)/|x-x_0|^n$$ unbounded as $$x\to x_0$$. Hence $$f^{(j)}(x_0)=0$$ for $$j<n$$, which means that $$f$$ has a zero of multiplicity at least $$n$$.

### Exercise 11

The assertion is false for every even degree: take $$p(x)=x^n$$ with even $$n$$. Then $$p(x)+e^x=x^n+e^x>0$$ for all $$x\in\mathbb R$$, so there is no zero.

For comparison, if $$n$$ is odd, every monic polynomial satisfies $$p(x)\to-\infty$$ as $$x\to-\infty$$, while $$p(x)+e^x\to+\infty$$ as $$x\to+\infty$$. The intermediate value theorem gives a zero. At every point,

$$
(p+e^x)^{(n)}=n!+e^x>0,
$$

so no zero can have multiplicity greater than $$n$$. Thus the statement does hold for odd $$n$$, but it is not true for all monic polynomials.

### Exercise 12

**(a)** For $$x=\cos\alpha$$ with $$\alpha\in[0,\pi]$$, de Moivre’s formula gives

$$
\cos(n\alpha)+i\sin(n\alpha)
=(\cos\alpha+i\sin\alpha)^n
=(x+i\sqrt{1-x^2})^n.
$$

Taking real parts and expanding the right side yields

$$
T_n(x)=\sum_{j=0}^{\lfloor n/2\rfloor}
\binom n{2j}x^{n-2j}(x^2-1)^j.
$$

This is a polynomial of degree at most $$n$$. Its leading coefficient is $$\sum_j\binom n{2j}=2^{n-1}$$ for $$n\ge1$$, so its degree is exactly $$n$$. The formula agrees with $$\cos(n\arccos x)$$ on $$[-1,1]$$ and gives its polynomial extension to all real $$x$$.

**(b)** For $$x=\cos\alpha$$, the cosine addition identity gives

$$
T_{n+1}(x)+T_{n-1}(x)
=2\cos\alpha\cos(n\alpha)=2xT_n(x).
$$

Since both sides are polynomials and agree for every $$x\in[-1,1]$$, they agree identically:

$$
T_{n+1}=2XT_n-T_{n-1}.
$$

**(c)** The leading coefficient found in (a) is $$2^{n-1}$$. Subtracting this leading term leaves a polynomial of degree strictly below $$n$$, so

$$
T_n=2^{n-1}X^n+p_n,\qquad \deg p_n<n.
$$

**(d)** Put $$\alpha_k=(2k-1)\pi/(2n)$$. These are distinct points in $$(0,\pi)$$, and

$$
T_n(x_k)=\cos(n\alpha_k)=0,
\qquad
x_k=\cos\alpha_k.
$$

To see that each zero is simple, differentiate $$T_n(\cos\alpha)=\cos(n\alpha)$$ for $$0<\alpha<\pi$$:

$$
T_n'(\cos\alpha)=\frac{n\sin(n\alpha)}{\sin\alpha}.
$$

At $$\alpha=\alpha_k$$ the numerator is nonzero and $$\sin\alpha_k>0$$, so $$T_n'(x_k)\ne0$$.

**(e)** For $$x=\cos\alpha\in[-1,1]$$,

$$
|T_n(x)|=|\cos(n\alpha)|\le1.
$$

At $$y_k=\cos(k\pi/n)$$, the value is

$$
T_n(y_k)=\cos(k\pi)=(-1)^k.
$$

These alternating values attain both bounds $$1$$ and $$-1$$. Interior points $$y_k$$ are local extrema, and the endpoints $$y_0=1$$ and $$y_n=-1$$ are one-sided extrema on the interval.

### Exercise 13

For $$n\ge1$$, the leading coefficient of $$T_n$$ is $$2^{n-1}$$, so $$\widetilde T_n=2^{1-n}T_n$$ is monic. By Exercise 12(e), its maximum norm on $$[-1,1]$$ is $$2^{1-n}$$. For $$n=0$$, $$\widetilde T_0=1$$ and the same norm formula gives one.

**(a)** Let $$p\in\mathcal P_n$$. For $$n=0$$ the claim is immediate. For $$n\ge1$$, suppose for contradiction that

$$
\|p\|_\infty<2^{1-n}.
$$

Set $$q=p-\widetilde T_n$$. The leading terms cancel, so $$\deg q\le n-1$$. At the points $$y_k=\cos(k\pi/n)$$, Exercise 12(e) gives $$\widetilde T_n(y_k)=2^{1-n}(-1)^k$$. The strict norm bound forces $$q(y_k)$$ to have sign $$-(-1)^k$$. Thus the signs of $$q$$ alternate at the $$n+1$$ ordered points $$y_0,\ldots,y_n$$. The intermediate value theorem gives at least one zero in each of the $$n$$ intervals between consecutive points, contradicting $$\deg q\le n-1$$. Therefore

$$
\|\widetilde T_n\|_\infty\le\|p\|_\infty.
$$

**(b)** Let $$m=(a+b)/2$$ and $$L=(b-a)/2>0$$, and define

$$
q(t)=\frac{p(m+Lt)}{L^n}.
$$

Because $$p$$ is monic of degree $$n$$, $$q$$ is also monic of degree $$n$$. The change of variables maps $$[-1,1]$$ onto $$[a,b]$$, so Exercise 13(a) implies

$$
\max_{a\le x\le b}|p(x)|
=L^n\|q\|_\infty
\ge L^n2^{1-n}
=2^{1-2n}(b-a)^n.
$$

**(c)** Let

$$
\omega(x)=\prod_{j=0}^n(x-x_j).
$$

The zeros $$x_0,\ldots,x_n$$ are those of $$T_{n+1}$$, whose leading coefficient is $$2^n$$. Hence $$\omega=2^{-n}T_{n+1}$$ and $$\|\omega\|_\infty=2^{-n}$$ on $$[-1,1]$$. The interpolation remainder formula gives, for each $$x\in[-1,1]$$, a point $$\xi_x\in[-1,1]$$ such that

$$
r_n[f;x_0,\ldots,x_n](x)
=\frac{f^{(n+1)}(\xi_x)}{(n+1)!}\,\omega(x).
$$

Consequently

$$
\|r_n[f;x_0,\ldots,x_n]\|_\infty
\le\frac{\|f^{(n+1)}\|_\infty}{2^n(n+1)!}.
$$

This bound is attained for $$f(x)=x^{n+1}$$. Its interpolation error is a monic polynomial of degree $$n+1$$ that vanishes at every $$x_j$$, so it equals $$\omega(x)$$. Also $$\|f^{(n+1)}\|_\infty=(n+1)!$$. Thus both sides equal $$2^{-n}$$, proving optimality.
