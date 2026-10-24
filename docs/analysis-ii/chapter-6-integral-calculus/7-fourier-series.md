# Chapter VI — Integral Calculus in One Variable

## 7. Fourier series

For $$f\in SC_{2\pi}$$, write

$$
\widehat f_k:=\frac{1}{2\pi}\int_0^{2\pi}f(t)e^{-ikt}\,dt,
\qquad
S_nf(t):=\sum_{k=-n}^{n}\widehat f_k e^{ikt}.
$$

Several printed exercise statements need correction. Exercise 1 is false for the stated class of normalized piecewise-continuous functions, even when the function is real-valued. In Exercise 2 the cosine argument must be $$2kt$$. In Exercise 3 the ordinary integral of the Dirichlet kernel is $$2\pi$$; its mean over one period is $$1$$. In Exercise 8(iii), with the normalized functions $$e_k(t)=(2\pi)^{-1/2}e^{ikt}$$ defined in the text, the right-hand side needs a factor $$1/\sqrt{2\pi}$$. Each issue is explained in its solution below.

### Exercise 1

As stated, the conclusion does not follow from $$\int_0^{2\pi}f=0$$. Define a real-valued function on one period by

$$
f(t)=
\begin{cases}
1,&0<t<\pi,\\[2pt]
-\dfrac{2(t-\pi)}{\pi},&\pi<t<2\pi.
\end{cases}
$$

Choose its values at the break points by the normalization convention (the average of the two one-sided limits). This gives

$$
f(\pi)=\frac12,
\qquad
f(0)=f(2\pi)=-\frac12.
$$

The resulting periodic function belongs to $$SC_{2\pi}$$ and never vanishes: it is positive on $$[0,\pi]$$ and negative on $$(\pi,2\pi)$$. Nevertheless,

$$
\int_0^{2\pi}f(t)\,dt
=\pi-\frac{2}{\pi}\int_\pi^{2\pi}(t-\pi)\,dt
=\pi-\frac{2}{\pi}\cdot\frac{\pi^2}{2}
=0.
$$

Thus the printed assertion is false even over $$\mathbb R$$. If the intended hypothesis was that $$f$$ is continuous and real-valued, then it is true: if $$f$$ never vanished, the intermediate value theorem would force it to have one strict sign on the connected interval, making its integral nonzero.

### Exercise 2

The formula in the book omits a factor $$2$$ in the cosine argument. The corrected Fourier expansion is

$$
Sf(t)=\frac{2}{\pi}
-\frac{4}{\pi}\sum_{k=1}^{\infty}\frac{\cos(2kt)}{4k^2-1}.
$$

Here $$f(t)=|\sin t|$$ is even and $$\pi$$-periodic. In the real trigonometric notation of the text, its constant coefficient is

$$
a_0=\frac{1}{\pi}\int_0^{2\pi}|\sin t|\,dt=\frac{4}{\pi}.
$$

Evenness gives $$b_k=0$$ for every $$k\ge1$$. Splitting the cosine coefficient integral into two periods of length $$\pi$$ gives

$$
a_k
=\frac{1+(-1)^k}{\pi}\int_0^\pi \sin t\cos(kt)\,dt.
$$

If $$k$$ is odd, then $$a_k=0$$. For $$k=2m$$ with $$m\ge1$$, the product-to-sum identity yields

$$
\begin{aligned}
\int_0^\pi\sin t\cos(2mt)\,dt
&=\frac12\int_0^\pi
\bigl(\sin((2m+1)t)+\sin((1-2m)t)\bigr)\,dt\\
&=\frac{1}{2m+1}-\frac{1}{2m-1}
=-\frac{2}{4m^2-1}.
\end{aligned}
$$

Therefore

$$
a_{2m}=-\frac{4}{\pi(4m^2-1)}.
$$

These coefficients give the displayed corrected series. Its nonconstant coefficients are absolutely summable because $$\sum_{m\ge1}(4m^2-1)^{-1}<\infty$$, so the Fourier series converges uniformly. By the completeness of the trigonometric system (equivalently, the quadratic-mean convergence result in this section), its limit agrees with $$f$$ almost everywhere. Both the limit and $$f$$ are continuous, so they agree everywhere.

### Exercise 3

By definition and the identity $$e_k(t)=(2\pi)^{-1/2}e^{ikt}$$,

$$
D_n(t)=\sum_{k=-n}^{n}e^{ikt}
=1+2\sum_{k=1}^{n}\cos(kt).
$$

For $$t\notin2\pi\mathbb Z$$, sum the finite geometric series:

$$
\begin{aligned}
D_n(t)
&=e^{-int}\frac{1-e^{i(2n+1)t}}{1-e^{it}}\\
&=\frac{\sin((n+\tfrac12)t)}{\sin(t/2)}.
\end{aligned}
$$

At $$t\in2\pi\mathbb Z$$ the quotient has a removable singularity, and its continuous extension has value $$2n+1$$, which is also the value of the finite sum. Thus the formula holds for every real $$t$$ when the quotient is interpreted by continuity at those points.

Integrating the trigonometric-polynomial expression over one period, all nonconstant cosine terms have integral zero. Hence

$$
\int_0^{2\pi}D_n(t)\,dt=2\pi.
$$

Consequently the normalized mean is

$$
\frac{1}{2\pi}\int_0^{2\pi}D_n(t)\,dt=1.
$$

The printed value $$1$$ is correct for this normalized mean, but not for the ordinary integral shown in the exercise.

### Exercise 4

For the normalized sawtooth function

$$
f(t)=\frac{\pi-t}{2}\quad(0<t<2\pi),\qquad f(0)=0,
$$

the Fourier coefficients are $$a_0=0$$, $$a_k=0$$ for every $$k\ge1$$, and $$b_k=1/k$$. Indeed, reflection about $$\pi$$ makes the cosine integral vanish, while integration by parts gives

$$
\int_0^{2\pi}\frac{\pi-t}{2}\sin(kt)\,dt
=\frac{\pi}{k}.
$$

Thus the $$n$$th Fourier polynomial is

$$
S_nf(t)=\sum_{k=1}^{n}\frac{\sin(kt)}{k}.
$$

We prove that these partial sums converge to $$f$$. From Exercise 3,

$$
D_n(s)=\frac{\sin((n+\tfrac12)s)}{\sin(s/2)}.
$$

For fixed $$t\in(0,2\pi)$$, set

$$
I_n(t):=\int_\pi^tD_n(s)\,ds.
$$

Integration by parts, with $$u(s)=1/\sin(s/2)$$, gives

$$
I_n(t)
=-\frac{\cos((n+\tfrac12)t)}{(n+\tfrac12)\sin(t/2)}
-\frac{1}{n+\tfrac12}
\int_\pi^t
\frac{\cos((n+\tfrac12)s)\cos(s/2)}{2\sin^2(s/2)}\,ds.
$$

Since the absolute integral of $$\cos(s/2)/(2\sin^2(s/2))$$ from $$\pi$$ to $$t$$ is $$|1/\sin(t/2)-1|$$, this implies the estimate

$$
|I_n(t)|
\le \frac{1}{n+\tfrac12}
\left(
\frac{1}{\sin(t/2)}
+\left|\frac{1}{\sin(t/2)}-1\right|
\right)
\le \frac{2}{(n+\tfrac12)\sin(t/2)}.
$$

Therefore $$I_n(t)\to0$$ for each fixed $$t\in(0,2\pi)$$. Also

$$
\int_0^\pi D_n(s)\,ds
=\pi+2\sum_{k=1}^{n}\frac{\sin(k\pi)}{k}
=\pi.
$$

The convolution formula for the Fourier partial sum, followed by the evenness of $$D_n$$, gives

$$
S_nf(t)-f(t)
=\frac{1}{2\pi}\int_0^\pi
\bigl(f(t-s)+f(t+s)-2f(t)\bigr)D_n(s)\,ds,
$$

where $$f$$ is read periodically. Put $$\delta=\min\{t,2\pi-t\}$$. For $$0\le s\le\delta$$, the function is linear on both sides of $$t$$, so

$$
f(t-s)+f(t+s)-2f(t)=0.
$$

For $$s>\delta$$, exactly one of $$t-s$$ and $$t+s$$ crosses the jump of the periodic sawtooth. Direct substitution into its defining formula shows that the bracket is $$-\pi$$ if $$t<\pi$$ and $$+\pi$$ if $$t>\pi$$. It follows that

$$
|S_nf(t)-f(t)|
=\frac12\left|\int_\delta^\pi D_n(s)\,ds\right|
=\frac12|I_n(\delta)|
\longrightarrow0.
$$

At $$t=0$$ (and hence at every multiple of $$2\pi$$), every partial sum is zero, equal to the normalized value of $$f$$. Thus the Fourier series converges to $$f$$ at every point, as asserted.

### Exercise 5

Let $$\widetilde B_m$$ be the 1-periodic extension of $$B_m|_{[0,1)}$$. We compute its Fourier coefficients on $$[0,1]$$. For $$k\in\mathbb Z\setminus\{0\}$$, put

$$
\gamma_{m,k}:=\int_0^1B_m(x)e^{-2\pi ikx}\,dx.
$$

The first Bernoulli polynomial is $$B_1(x)=x-\tfrac12$$, and direct integration by parts gives

$$
\gamma_{1,k}=\frac{i}{2\pi k}.
$$

For $$m\ge1$$, use $$B_{m+1}'=(m+1)B_m$$. Since $$B_{m+1}(1)=B_{m+1}(0)$$ for $$m+1\ge2$$, integration by parts has no boundary term and gives

$$
\gamma_{m,k}
=\frac{i\,2\pi k}{m+1}\gamma_{m+1,k},
\qquad
\gamma_{m+1,k}
=\frac{m+1}{i\,2\pi k}\gamma_{m,k}.
$$

Induction therefore yields

$$
\gamma_{m,k}=-\frac{m!}{(i\,2\pi k)^m}
\qquad(m\ge1,\ k\ne0).
$$

The zeroth coefficient is $$\int_0^1B_m(x)\,dx=0$$ for every $$m\ge1$$. Pairing the coefficients for $$k$$ and $$-k$$ now gives two cases. For $$m=2n$$,

$$
\gamma_{2n,k}e^{2\pi ikx}+\gamma_{2n,-k}e^{-2\pi ikx}
=2(-1)^{n-1}\frac{(2n)!}{(2\pi)^{2n}}
\frac{\cos(2\pi kx)}{k^{2n}}.
$$

For $$m=2n+1$$,

$$
\gamma_{2n+1,k}e^{2\pi ikx}
+\gamma_{2n+1,-k}e^{-2\pi ikx}
=2(-1)^{n-1}\frac{(2n+1)!}{(2\pi)^{2n+1}}
\frac{\sin(2\pi kx)}{k^{2n+1}}.
$$

The coefficients are absolutely summable for every $$m\ge2$$, so these Fourier series converge uniformly. Their limits have the computed Fourier coefficients; completeness of the trigonometric system identifies the limits with the continuous periodic extensions $$\widetilde B_m$$. For $$m=1$$, Exercise 4 gives the sine series directly, including the normalized values at the integers. We obtain

$$
\widetilde B_{2n}(x)
=2\frac{(-1)^{n-1}(2n)!}{(2\pi)^{2n}}
\sum_{k=1}^{\infty}\frac{\cos(2\pi kx)}{k^{2n}}
\qquad(n\ge1),
$$

and

$$
\widetilde B_{2n+1}(x)
=2\frac{(-1)^{n-1}(2n+1)!}{(2\pi)^{2n+1}}
\sum_{k=1}^{\infty}\frac{\sin(2\pi kx)}{k^{2n+1}}
\qquad(n\ge0),
$$

which are the stated expansions.

### Exercise 6

Set

$$
\zeta(2n):=\sum_{k=1}^{\infty}\frac1{k^{2n}}.
$$

Evaluating the even Bernoulli Fourier expansion from Exercise 5 at $$x=0$$ gives

$$
|B_{2n}|
=2\frac{(2n)!}{(2\pi)^{2n}}\zeta(2n).
$$

Since $$x\mapsto x^{-2n}$$ is decreasing,

$$
0\le \zeta(2n)-1
=\sum_{k=2}^{\infty}k^{-2n}
\le\int_1^\infty x^{-2n}\,dx
=\frac{1}{2n-1}.
$$

Thus $$\zeta(2n)\to1$$, proving the first asymptotic equivalence:

$$
|B_{2n}|\sim 2\frac{(2n)!}{(2\pi)^{2n}}.
$$

Finally, Stirling's formula gives

$$
(2n)!\sim\sqrt{4\pi n}\left(\frac{2n}{e}\right)^{2n}
=2\sqrt{\pi n}\left(\frac{2n}{e}\right)^{2n}.
$$

Consequently,

$$
2\frac{(2n)!}{(2\pi)^{2n}}
\sim4\sqrt{\pi n}\left(\frac{n}{\pi e}\right)^{2n},
$$

which proves the second equivalence.

### Exercise 7

First reduce to the interval $$[0,\pi]$$ by setting

$$
u(t):=f\left(a+\frac{b-a}{\pi}t\right).
$$

It is enough to show

$$
\int_0^\pi|u(t)|^2\,dt\le\int_0^\pi|u'(t)|^2\,dt.
$$

Extend $$u$$ oddly to $$g:[-\pi,\pi]\to\mathbb K$$ by

$$
g(x)=
\begin{cases}
u(x),&0\le x\le\pi,\\
-u(-x),&-\pi\le x<0.
\end{cases}
$$

Because $$u(0)=u(\pi)=0$$, the extension is continuously differentiable, and its endpoint derivatives match, so it extends to a $$2\pi$$-periodic $$C^1$$ function. It is odd, hence $$\widehat g_0=0$$. Integration by parts shows that the Fourier coefficient of $$g'$$ at index $$k$$ is $$ik\widehat g_k$$. Parseval's theorem applied to $$g$$ and $$g'$$ therefore gives

$$
\frac1{2\pi}\int_{-\pi}^{\pi}|g'|^2
=\sum_{k\in\mathbb Z}k^2|\widehat g_k|^2
\ge\sum_{k\ne0}|\widehat g_k|^2
=\frac1{2\pi}\int_{-\pi}^{\pi}|g|^2.
$$

The integrals on $$[-\pi,\pi]$$ are twice the corresponding integrals of $$u$$ and $$u'$$ on $$[0,\pi]$$, proving the reduced inequality. Changing variables back to $$[a,b]$$ yields

$$
\int_a^b|f(x)|^2\,dx
\le\left(\frac{b-a}{\pi}\right)^2
\int_a^b|f'(x)|^2\,dx.
$$

The constant is sharp: for the nonzero function

$$
f(x)=\sin\left(\frac{\pi(x-a)}{b-a}\right),
$$

we have $$f(a)=f(b)=0$$ and $$|f'(x)|^2=(\pi/(b-a))^2\cos^2(\pi(x-a)/(b-a))$$. The integrals of the squared sine and cosine over $$[a,b]$$ are both $$(b-a)/2$$, so equality holds. A smaller constant cannot work.

### Exercise 8

**(i)** By the substitution $$z=x-y$$ and periodicity, an integral over any interval of length $$2\pi$$ can be shifted to $$[0,2\pi]$$. Therefore

$$
\begin{aligned}
(f*g)(x)
&=\frac1{2\pi}\int_0^{2\pi}f(x-y)g(y)\,dy\\
&=\frac1{2\pi}\int_0^{2\pi}f(z)g(x-z)\,dz\\
&=(g*f)(x).
\end{aligned}
$$

**(ii)** The convolution is $$2\pi$$-periodic by periodicity of $$f$$. To prove continuity, for any $$x,x'\in\mathbb R$$,

$$
|(f*g)(x)-(f*g)(x')|
\le \|g\|_\infty
\sup_{z\in\mathbb R}|f(z+x-x')-f(z)|.
$$

The continuous periodic function $$f$$ is uniformly continuous on $$\mathbb R$$. The right-hand side tends to zero as $$x'\to x$$, so $$f*g$$ is continuous and belongs to $$C_{2\pi}$$.

**(iii)** With the normalization in the text,

$$
e_n(x-y)=e_n(x)e^{-iny},
\qquad
e_m(y)=\frac{1}{\sqrt{2\pi}}e^{imy}.
$$

Consequently,

$$
\begin{aligned}
(e_n*e_m)(x)
&=\frac{e_n(x)}{2\pi\sqrt{2\pi}}
\int_0^{2\pi}e^{i(m-n)y}\,dy\\
&=\frac{\delta_{nm}}{\sqrt{2\pi}}e_n(x).
\end{aligned}
$$

Thus the printed identity $$e_n*e_m=\delta_{nm}e_n$$ is missing the factor $$1/\sqrt{2\pi}$$ when $$e_k(t)=(2\pi)^{-1/2}e^{ikt}$$. The printed identity would hold for the unnormalized exponentials $$e^{ikt}$$ instead.

### Exercise 9

Using $$D_n(t)=\sum_{k=-n}^{n}e^{ikt}$$ and the definition of convolution,

$$
\begin{aligned}
(D_n*f)(x)
&=\frac1{2\pi}\int_0^{2\pi}
\left(\sum_{k=-n}^{n}e^{ik(x-y)}\right)f(y)\,dy\\
&=\sum_{k=-n}^{n}e^{ikx}
\left(\frac1{2\pi}\int_0^{2\pi}f(y)e^{-iky}\,dy\right)\\
&=\sum_{k=-n}^{n}\widehat f_k e^{ikx}\\
&=S_nf(x).
\end{aligned}
$$

The interchange of the sum and integral is valid because the sum is finite.

### Exercise 10

**(i)** Define the inner product on $$\ell_2(\mathbb Z)$$ by

$$
(x\mid y):=\sum_{k\in\mathbb Z}x_k\overline{y_k},
\qquad
\|x\|_2^2:=\sum_{k\in\mathbb Z}|x_k|^2.
$$

The Cauchy–Schwarz inequality makes the inner product well-defined, and its induced norm is the stated $$\ell_2$$ norm. To prove completeness, let $$(x^{(j)})$$ be Cauchy in this norm. For each fixed $$k$$, the coordinate sequence $$(x_k^{(j)})$$ is Cauchy in $$\mathbb K$$, because

$$
|x_k^{(j)}-x_k^{(\ell)}|
\le\|x^{(j)}-x^{(\ell)}\|_2.
$$

Let $$x_k:=\lim_{j\to\infty}x_k^{(j)}$$. The norms $$\|x^{(j)}\|_2$$ are bounded. For each finite set $$F\subset\mathbb Z$$, coordinatewise convergence gives

$$
\sum_{k\in F}|x_k|^2
=\lim_{j\to\infty}\sum_{k\in F}|x_k^{(j)}|^2
\le\sup_j\|x^{(j)}\|_2^2.
$$

Taking the supremum over finite $$F$$ shows that $$x\in\ell_2(\mathbb Z)$$. Given $$\varepsilon>0$$, choose $$J$$ such that $$\|x^{(j)}-x^{(\ell)}\|_2<\varepsilon$$ whenever $$j,\ell\ge J$$. Fix $$j\ge J$$ and let $$\ell\to\infty$$ in each finite coordinate sum:

$$
\sum_{k\in F}|x_k^{(j)}-x_k|^2\le\varepsilon^2
\qquad(F\subset\mathbb Z\text{ finite}).
$$

Taking the supremum over finite $$F$$ gives $$\|x^{(j)}-x\|_2\le\varepsilon$$. Thus every Cauchy sequence converges in $$\ell_2(\mathbb Z)$$, so it is a Hilbert space.

**(ii)** The Fourier coefficient map is linear. By Parseval's theorem for the complete orthonormal system $$(e_k)_{k\in\mathbb Z}$$,

$$
\|f\|_2^2
=\sum_{k\in\mathbb Z}|(f\mid e_k)_2|^2
=\sum_{k\in\mathbb Z}|\,\sqrt{2\pi}\widehat f_k\,|^2.
$$

Hence the sequence $$(\sqrt{2\pi}\widehat f_k)_{k\in\mathbb Z}$$ belongs to $$\ell_2(\mathbb Z)$$, and the map

$$
f\longmapsto(\sqrt{2\pi}\widehat f_k)_{k\in\mathbb Z}
$$

preserves norms. It is therefore a linear isometry.

### Exercise 11

For complex numbers $$z,w$$, use the polarization identity

$$
z\overline w
=\frac14\left(
|z+w|^2-|z-w|^2
+i|z+iw|^2-i|z-iw|^2
\right).
$$

Apply this identity pointwise to $$z=f(t)$$ and $$w=g(t)$$, then integrate and divide by $$2\pi$$. Apply it again to $$z=\widehat f_k$$ and $$w=\widehat g_k$$ and sum over $$k\in\mathbb Z$$. Parseval's theorem gives, for each of the four norm terms,

$$
\frac1{2\pi}\int_0^{2\pi}|f\pm g|^2\,dt
=\sum_{k\in\mathbb Z}|\widehat f_k\pm\widehat g_k|^2,
$$

and likewise with $$f\pm ig$$. These sums converge, and the mixed series converges absolutely by Cauchy–Schwarz:

$$
\sum_{k\in\mathbb Z}|\widehat f_k\overline{\widehat g_k}|
\le
\left(\sum_k|\widehat f_k|^2\right)^{1/2}
\left(\sum_k|\widehat g_k|^2\right)^{1/2}
<\infty.
$$

The polarization identity therefore yields

$$
\frac1{2\pi}\int_0^{2\pi}f(t)\overline{g(t)}\,dt
=\sum_{k=-\infty}^{\infty}
\widehat f_k\,\overline{\widehat g_k},
$$

which is the generalized Parseval theorem.
