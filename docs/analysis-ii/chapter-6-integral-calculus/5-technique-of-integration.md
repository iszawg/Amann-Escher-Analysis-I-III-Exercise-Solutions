# Chapter VI — Integral Calculus in One Variable

## 5. The Technique of Integration

All functions and integrals in this section are real-valued. Unless limits are displayed, an integral is indefinite and its formula holds on any interval where the integrand is defined; $$C$$ denotes an arbitrary constant of integration.

### Exercise 1

**(i)** Consider

$$
q(x)=a^2x^2+bx+c,
\qquad \Delta=4a^2c-b^2.
$$

Suppose first that $$a\ne0$$, and put $$t=2a^2x+b$$. Then $$t^2+\Delta=4a^2q(x)$$. If $$\Delta>0$$, differentiating the arctangent below gives

$$
\frac{d}{dx}\left[\frac{2}{\sqrt\Delta}\arctan\left(\frac{t}{\sqrt\Delta}\right)\right]
=\frac{4a^2}{t^2+\Delta}
=\frac1{q(x)}.
$$

If $$\Delta<0$$, set $$d=\sqrt{-\Delta}=\sqrt{b^2-4a^2c}$$. Since $$t^2-d^2=4a^2q(x)$$,

$$
\frac{d}{dx}\left[\frac1d\log\left|\frac{t-d}{t+d}\right|\right]
=\frac{4a^2}{t^2-d^2}
=\frac1{q(x)}.
$$

When $$\Delta=0$$, we have $$q(x)=t^2/(4a^2)$$, so the primitive is $$-2/t$$. Thus, for $$a\ne0$$,

$$
\int\frac{dx}{a^2x^2+bx+c}
=\begin{cases}
\displaystyle \frac{2}{\sqrt\Delta}\arctan\left(\frac{2a^2x+b}{\sqrt\Delta}\right)+C,&\Delta>0,\\[1.2ex]
\displaystyle \frac{1}{\sqrt{-\Delta}}\log\left|\frac{2a^2x+b-\sqrt{-\Delta}}{2a^2x+b+\sqrt{-\Delta}}\right|+C,&\Delta<0,\\[1.2ex]
\displaystyle -\frac{2}{2a^2x+b}+C,&\Delta=0.
\end{cases}
$$

The cases where the quadratic term vanishes must be handled separately: if $$a=0$$ and $$b\ne0$$, the answer is $$b^{-1}\log|bx+c|+C$$; if $$a=b=0$$ and $$c\ne0$$, it is $$x/c+C$$. If $$a=b=c=0$$, the integrand is nowhere defined.

**(ii)** Complete the square and split the numerator into a multiple of the derivative of the denominator plus a constant:

$$
x=\frac12(2x-2)+1,
\qquad x^2-2x+3=(x-1)^2+2.
$$

Therefore

$$
\int\frac{x\,dx}{x^2-2x+3}
=\frac12\log(x^2-2x+3)
+\frac1{\sqrt2}\arctan\left(\frac{x-1}{\sqrt2}\right)+C.
$$

**(iii)** Polynomial division gives

$$
x^5=(x^2+x+1)(x^3-x^2+1)-(x+1).
$$

Also $$x+1=\tfrac12(2x+1)+\tfrac12$$ and $$x^2+x+1=(x+\tfrac12)^2+\tfrac34$$. Integrating each term yields

$$
\int\frac{x^5\,dx}{x^2+x+1}
=\frac{x^4}{4}-\frac{x^3}{3}+x
-\frac12\log(x^2+x+1)
-\frac1{\sqrt3}\arctan\left(\frac{2x+1}{\sqrt3}\right)+C.
$$

**(iv)** Factor the denominator over $$\mathbb R$$ by setting

$$
q_+(x)=x^2+\sqrt2x+1,
\qquad q_-(x)=x^2-\sqrt2x+1.
$$

Then $$x^4+1=q_+q_-$$, and direct combination over a common denominator gives

$$
\frac1{x^4+1}
=\frac1{4\sqrt2}\frac{q_+'}{q_+}+\frac1{4q_+}
-\frac1{4\sqrt2}\frac{q_-'}{q_-}+\frac1{4q_-}.
$$

Completing squares, $$q_+=(x+1/\sqrt2)^2+1/2$$ and $$q_-=(x-1/\sqrt2)^2+1/2$$. Thus

$$
\int\frac{dx}{x^4+1}
=\frac1{4\sqrt2}\log\left(\frac{x^2+\sqrt2x+1}{x^2-\sqrt2x+1}\right)
+\frac1{2\sqrt2}\left[\arctan(\sqrt2x+1)+\arctan(\sqrt2x-1)\right]+C.
$$

**(v)** The corresponding decomposition for the even numerator is

$$
\frac{x^2}{x^4+1}
=-\frac1{4\sqrt2}\frac{q_+'}{q_+}+\frac1{4q_+}
+\frac1{4\sqrt2}\frac{q_-'}{q_-}+\frac1{4q_-}.
$$

The same completed-square integrals as in (iv) now give

$$
\int\frac{x^2\,dx}{x^4+1}
=\frac1{4\sqrt2}\log\left(\frac{x^2-\sqrt2x+1}{x^2+\sqrt2x+1}\right)
+\frac1{2\sqrt2}\left[\arctan(\sqrt2x+1)+\arctan(\sqrt2x-1)\right]+C.
$$

**(vi)** Put $$q(x)=ax^2+bx+c$$ and $$\Delta=4ac-b^2$$. For $$a\ne0$$ and $$\Delta\ne0$$, differentiation gives

$$
\left(\frac{2ax+b}{q(x)}\right)'
=\frac{\Delta}{q(x)^2}-\frac{2a}{q(x)}.
$$

Consequently, if $$J(x)$$ is any primitive of $$1/q(x)$$, then

$$
\int\frac{dx}{q(x)^2}
=\frac{2ax+b}{\Delta q(x)}+\frac{2a}{\Delta}J(x)+C.
$$

The primitive $$J$$ is obtained by the same discriminant calculation as in (i), with $$a^2$$ there replaced by $$a$$. Explicitly, it is $$\frac{2}{\sqrt\Delta}\arctan\frac{2ax+b}{\sqrt\Delta}$$ if $$\Delta>0$$, and $$\frac1{\sqrt{-\Delta}}\log\left|\frac{2ax+b-\sqrt{-\Delta}}{2ax+b+\sqrt{-\Delta}}\right|$$ if $$\Delta<0$$. If $$a\ne0$$ and $$\Delta=0$$, then $$q=(2ax+b)^2/(4a)$$ and

$$
\int\frac{dx}{q(x)^2}=-\frac{8a}{3(2ax+b)^3}+C.
$$

Finally, if $$a=0$$ and $$b\ne0$$, the integral is $$-1/[b(bx+c)]+C$$; if $$a=b=0$$ and $$c\ne0$$, it is $$x/c^2+C$$. The zero polynomial again gives no defined integrand.

### Exercise 2

Each substitution below turns the integrand into a rational function of the new variable.

**(i)** Let $$t=e^x$$, so $$dx=dt/t$$. Then

$$
\frac{e^x-1}{e^x+1}\,dx
=\frac{t-1}{t(t+1)}\,dt
=\left(-\frac1t+\frac2{t+1}\right)dt.
$$

Hence

$$
\int\frac{e^x-1}{e^x+1}\,dx
=-\log t+2\log(t+1)+C
=2\log(1+e^x)-x+C.
$$

**(ii)** Set $$t=\sqrt{1+x}$$, with $$t\ge0$$. Since $$x=t^2-1$$ and $$dx=2t\,dt$$,

$$
\int\frac{dx}{1+\sqrt{1+x}}
=\int\frac{2t}{1+t}\,dt
=\int\left(2-\frac2{1+t}\right)dt.
$$

Therefore

$$
\int\frac{dx}{1+\sqrt{1+x}}
=2\sqrt{1+x}-2\log\left(1+\sqrt{1+x}\right)+C.
$$

**(iii)** For $$x>0$$, set $$t=x^{1/6}$$. Then $$x=t^6$$ and $$dx=6t^5dt$$, so

$$
\frac{dx}{\sqrt{x}(1+\sqrt[3]{x})}
=\frac{6t^5}{t^3(1+t^2)}dt
=6\left(1-\frac1{1+t^2}\right)dt.
$$

It follows that

$$
\int\frac{dx}{\sqrt{x}(1+\sqrt[3]{x})}
=6\left(x^{1/6}-\arctan(x^{1/6})\right)+C.
$$

### Exercise 3

Let $$I=[\alpha,\beta]$$. Integration by parts, using $$d(-\cos(\lambda x)/\lambda)=\sin(\lambda x)\,dx$$, gives

$$
\int_\alpha^\beta f(x)\sin(\lambda x)\,dx
=\left[-\frac{f(x)\cos(\lambda x)}{\lambda}\right]_\alpha^\beta
+\frac1\lambda\int_\alpha^\beta f'(x)\cos(\lambda x)\,dx.
$$

Since $$|\cos(\lambda x)|\le1$$,

$$
\left|\int_\alpha^\beta f(x)\sin(\lambda x)\,dx\right|
\le\frac{|f(\alpha)|+|f(\beta)|+\int_\alpha^\beta|f'(x)|\,dx}{\lambda}.
$$

The numerator is finite and independent of $$\lambda$$. Letting $$\lambda\to\infty$$ proves the limit is zero.

### Exercise 4

**(i)** Write $$A=\int_0^\pi x f(\sin x)\,dx$$. Substituting $$t=\pi-x$$ and using $$\sin(\pi-t)=\sin t$$ gives

$$
A=\int_0^\pi(\pi-t)f(\sin t)\,dt.
$$

Adding this to the original expression for $$A$$ yields $$2A=\pi\int_0^\pi f(\sin x)\,dx$$, which is the required identity.

**(ii)** Let $$A=\int_0^{\pi/2}f(\sin 2x)\cos x\,dx$$. Split at $$\pi/4$$. In the second part use $$t=\pi/2-x$$; then $$\sin(2x)=\sin(2t)$$ and $$\cos x\,dx=-\sin t\,dt$$. Thus

$$
A=\int_0^{\pi/4}f(\sin2x)(\cos x+\sin x)\,dx.
$$

On this interval put $$u=\cos x-\sin x$$. Then $$du=-(\cos x+\sin x)dx$$, and $$\sin2x=1-u^2$$; the endpoints $$x=0,\pi/4$$ correspond to $$u=1,0$$. Therefore

$$
A=\int_0^1 f(1-u^2)\,du.
$$

For the right-hand side, the substitution $$u=\sin x$$ gives

$$
\int_0^{\pi/2}f(\cos^2x)\cos x\,dx
=\int_0^1 f(1-u^2)\,du.
$$

The two sides are equal.

### Exercise 5

By Rodrigues' formula,

$$
P_n(x)=\frac1{2^n n!}\frac{d^n}{dx^n}(x^2-1)^n.
$$

The polynomial $$(x^2-1)^n$$ and its derivatives of orders $$0,\ldots,n-1$$ vanish at both endpoints $$-1$$ and $$1$$, because it has a zero of order $$n$$ at each endpoint. We can therefore integrate by parts $$n$$ times without boundary terms.

If $$n>m$$, this gives

$$
\int_{-1}^1P_n(x)P_m(x)\,dx
=\frac{(-1)^n}{2^n n!}\int_{-1}^1(x^2-1)^nP_m^{(n)}(x)\,dx=0,
$$

since $$P_m$$ has degree $$m<n$$. Interchanging $$m$$ and $$n$$ covers the case $$m>n$$.

For the diagonal case, the leading coefficient of $$P_n$$ is $$\frac{(2n)!}{2^n(n!)^2}$$, so $$P_n^{(n)}=\frac{(2n)!}{2^n n!}$$. The same integrations by parts now yield

$$
\int_{-1}^1P_n(x)^2\,dx
=\frac{(2n)!}{2^{2n}(n!)^2}J_n,
\qquad J_n:=\int_{-1}^1(1-x^2)^n\,dx.
$$

For $$n\ge1$$, integrate the derivative of $$x(1-x^2)^n$$ over $$[-1,1]$$. Its boundary values are zero, and simplification gives

$$
(2n+1)J_n=2nJ_{n-1}.
$$

Since $$J_0=2$$, induction gives $$J_n=\frac{2^{2n+1}(n!)^2}{(2n+1)!}$$. Substitution into the norm formula proves

$$
\int_{-1}^1P_n(x)P_m(x)\,dx
=\begin{cases}
0,&n\ne m,\\[2pt]
\displaystyle\frac2{2n+1},&n=m.
\end{cases}
$$

### Exercise 6

Use $$x=\tan t$$, so $$dx/(1+x^2)=dt$$ and the endpoints $$x=0,1$$ become $$t=0,\pi/4$$. The integral becomes

$$
\int_0^{\pi/4}\log(1+\tan t)\,dt.
$$

For $$0\le t\le\pi/4$$, the given identity implies

$$
\log(1+\tan t)
=\frac12\log2+\log\sin\left(t+\frac\pi4\right)-\log\cos t.
$$

The two nonconstant terms have equal integrals: in the first, let $$u=t+\pi/4$$; in the second, let $$u=\pi/2-t$$. Each becomes $$\int_{\pi/4}^{\pi/2}\log\sin u\,du$$, so they cancel in the difference. The constant term contributes $$\frac12\log2\cdot\frac\pi4$$. Hence the original integral equals $$\frac\pi8\log2$$.

### Exercise 7

Set $$x=y/\sqrt2$$, so $$0\le y\le1$$ and $$dx=dy/\sqrt2$$. After simplifying the numerator and denominator, the integral becomes

$$
16\int_0^1\frac{y^5+y^4+2y^3-4}{y^8-16}\,dy.
$$

The supplied factorization implies

$$
\frac{y^5+y^4+2y^3-4}{y^8-16}
=\frac{y-1}{(y^2-2)(y^2-2y+2)}.
$$

Put $$t=y-1$$. Since $$y^2-2=t^2+2t-1$$ and $$y^2-2y+2=t^2+1$$, direct partial fractions give

$$
\frac{16(y-1)}{(y^2-2)(y^2-2y+2)}
=\frac{4(t+1)}{t^2+2t-1}+\frac{-4t+4}{t^2+1}.
$$

An antiderivative with respect to $$t$$ is

$$
2\log|t^2+2t-1|-2\log(t^2+1)+4\arctan t.
$$

The bounds $$y=0,1$$ correspond to $$t=-1,0$$. The antiderivative has values $$-\pi$$ at $$t=-1$$ and $$0$$ at $$t=0$$. Their difference is $$\pi$$, as required.

### Exercise 8

For $$0\le x\le c<1$$, the geometric expansion

$$
\frac1{1-x^m}=\sum_{n=0}^\infty x^{nm}
$$

converges uniformly: the tail after the $$N$$th term is bounded by $$c^{m(N+1)}/(1-c^m)$$. Multiplication by the bounded function $$x^{k-1}$$ preserves uniform convergence, so we may integrate the series term by term:

$$
\int_0^c\frac{x^{k-1}}{1-x^m}\,dx
=\sum_{n=0}^\infty\int_0^c x^{nm+k-1}\,dx
=\sum_{n=0}^\infty\frac{c^{nm+k}}{nm+k}.
$$

### Exercise 9

With $$c=1/\sqrt2$$ and $$m=8$$, Exercise 8 gives, for $$k=1,4,5,6$$,

$$
J_k:=\int_0^{1/\sqrt2}\frac{x^{k-1}}{1-x^8}\,dx
=2^{-k/2}\sum_{n=0}^\infty\frac{16^{-n}}{8n+k}.
$$

The integral in Exercise 7 is $$4\sqrt2J_1-8J_4-4\sqrt2J_5-8J_6$$. Substituting the four series and simplifying their coefficients gives

$$
\pi=\sum_{n=0}^\infty\frac1{16^n}\left(\frac4{8n+1}-\frac2{8n+4}-\frac1{8n+5}-\frac1{8n+6}\right),
$$

which is the stated series.

### Exercise 10

Each formula below follows from integration by parts; the additive constants are absorbed into the chosen primitives $$I_n$$.

**(i)** For $$n\ge1$$, take $$u=x^n$$ and $$dv=e^x dx$$. Then $$du=nx^{n-1}dx$$ and $$v=e^x$$, so

$$
I_n=x^ne^x-nI_{n-1},
\qquad I_0=e^x.
$$

**(ii)** On $$x>0$$, take $$u=(\log x)^n$$ and $$dv=x\,dx$$. This gives

$$
I_n=\frac{x^2}{2}(\log x)^n-\frac n2 I_{n-1},
\qquad I_0=\frac{x^2}{2}.
$$

**(iii)** For $$n\ge2$$, take $$u=\cos^{n-1}x$$ and $$dv=\cos x\,dx$$. After using $$\sin^2x=1-\cos^2x$$ and moving the resulting $$I_n$$ term to the left, we obtain

$$
I_n=\frac{\sin x\cos^{n-1}x}{n}+\frac{n-1}{n}I_{n-2},
\qquad I_0=x,\quad I_1=\sin x.
$$

**(iv)** For $$n\ge2$$, differentiate $$x/(1+x^2)^{n-1}$$:

$$
\left(\frac{x}{(1+x^2)^{n-1}}\right)'
=\frac{2(n-1)}{(1+x^2)^n}-\frac{2n-3}{(1+x^2)^{n-1}}.
$$

Solving for the first term gives

$$
I_n=\frac{x}{2(n-1)(1+x^2)^{n-1}}+\frac{2n-3}{2(n-1)}I_{n-1},
\qquad I_1=\arctan x.
$$
