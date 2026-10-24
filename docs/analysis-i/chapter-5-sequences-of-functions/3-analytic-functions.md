This section develops the local structure of analytic functions through power series, zero sets, and classical expansions. Each solution makes the relevant convergence and domain arguments explicit.

### Exercise 1

**(a)** Fix $$x_0\in D_{\mathbb R}$$. Since $$f$$ is analytic, on some disk centered at $$x_0$$ it has a convergent expansion

$$
f(z)=\sum_{k=0}^{\infty}a_k(z-x_0)^k.
$$

For real $$x$$ sufficiently close to $$x_0$$, the quantity $$x-x_0$$ is real. Taking real and imaginary parts term by term gives

$$
\operatorname{Re}f(x)=\sum_{k=0}^{\infty}\operatorname{Re}(a_k)(x-x_0)^k,
\qquad
\operatorname{Im}f(x)=\sum_{k=0}^{\infty}\operatorname{Im}(a_k)(x-x_0)^k.
$$

Both series converge on that real neighborhood. Thus the restrictions of $$\operatorname{Re}f$$ and $$\operatorname{Im}f$$ are real analytic at every point of $$D_{\mathbb R}$$.

**(b)** Suppose first that every coefficient $$a_k$$ is real. The displayed expansion then shows that $$f(x)$$ is real for every $$x\in\widetilde D$$. At any $$y\in\widetilde D$$, re-expand the power series about $$y$$. Its coefficients are real because they are sums of real multiples of $$a_k$$, and the re-expansion converges in a neighborhood of $$y$$. Hence $$f|_{\widetilde D}$$ is real analytic.

Conversely, suppose $$f|_{\widetilde D}$$ is real analytic as a real-valued function. In particular, it is real-valued near $$x_0$$. The imaginary part of the original expansion there is

$$
\operatorname{Im}f(x)=\sum_{k=0}^{\infty}\operatorname{Im}(a_k)(x-x_0)^k=0.
$$

Uniqueness of power-series coefficients (equivalently, differentiating at $$x_0$$) implies $$\operatorname{Im}(a_k)=0$$ for every $$k$$. Thus all $$a_k$$ are real, proving the equivalence.

### Exercise 2

Fix $$z_0\in D$$. Write the local power series of $$f$$ at $$z_0$$ as

$$
f(z)=a_0+\sum_{k=1}^{\infty}a_k(z-z_0)^k,
\qquad a_0=f(z_0)\ne0.
$$

By continuity, choose a smaller disk around $$z_0$$ on which

$$
\left|\frac{f(z)-a_0}{a_0}\right|<1.
$$

On that disk the geometric series converges locally uniformly, so

$$
\frac1{f(z)}
=\frac1{a_0}\frac1{1+(f(z)-a_0)/a_0}
=\frac1{a_0}\sum_{n=0}^{\infty}\left(-\frac{f(z)-a_0}{a_0}\right)^n.
$$

This is a convergent power-series composition near $$z_0$$, so $$1/f$$ is analytic there. Since $$z_0$$ was arbitrary and $$f$$ has no zeros on $$D$$, $$1/f$$ is analytic throughout $$D$$.

### Exercise 3

For $$z\ne0$$, the exponential series gives

$$
h(z)=\frac{e^z-1}{z}=\sum_{k=0}^{\infty}\frac{z^k}{(k+1)!}.
$$

The series converges for every complex $$z$$ and has value $$1$$ at $$z=0$$. It therefore agrees with the definition of $$h$$ everywhere and proves that $$h$$ is entire.

Now let $$r=|z|<1/(e-1)$$. Then $$r<1$$, and the reverse triangle inequality yields

$$
|h(z)|
\ge 1-\sum_{k=1}^{\infty}\frac{r^k}{(k+1)!}
\ge 1-r\sum_{k=1}^{\infty}\frac1{(k+1)!}
=1-r(e-2)
>1-\frac{e-2}{e-1}
>0.
$$

Thus $$h(z)\ne0$$ whenever $$|z|<1/(e-1)$$.

### Exercise 4

Set $$H(z):=h(z)=\sum_{k=0}^{\infty}z^k/(k+1)!$$. By Exercise 3, $$H$$ has no zeros near zero, so write the Taylor expansion

$$
\frac1{H(z)}=\sum_{k=0}^{\infty}\frac{B_k}{k!}z^k
$$

there. Multiplying by the series for $$H$$ and comparing coefficients with the constant series $$1$$ gives $$B_0=1$$ and, for every $$m\ge1$$,

$$
\sum_{j=0}^{m}\binom{m+1}{j}B_j=0,
\qquad
B_m=-\frac1{m+1}\sum_{j=0}^{m-1}\binom{m+1}{j}B_j.
$$

The recurrence computes the requested coefficients:

$$
\begin{array}{c|rrrrrrrrrrr}
m&0&1&2&3&4&5&6&7&8&9&10\\
\hline
B_m&1&-\frac12&\frac16&0&-\frac1{30}&0&\frac1{42}&0&-\frac1{30}&0&\frac5{66}
\end{array}
$$

Every binomial coefficient in the recurrence is an integer. Starting from $$B_0=1$$, induction therefore shows that each $$B_m$$ is rational.

### Exercise 5

For a holomorphic function, its complex derivative can be computed using increments along either coordinate direction.

**(i)** If $$\operatorname{Re}f$$ is constant, then for real $$t\ne0$$ the quotient $$[f(z+t)-f(z)]/t$$ is purely imaginary. Letting $$t\to0$$ shows that $$f'(z)\in i\mathbb R$$. For real $$t\ne0$$, the quotient $$[f(z+it)-f(z)]/(it)$$ is real, so also $$f'(z)\in\mathbb R$$. Hence $$f'(z)=0$$.

**(ii)** If $$\operatorname{Im}f$$ is constant, then the real-direction difference quotient is real and the imaginary-direction difference quotient is purely imaginary. Again, $$f'(z)\in\mathbb R\cap i\mathbb R=\{0\}$$.

In either case, $$f'$$ vanishes on $$D$$. The local power series of $$f$$ is then constant near each point; since $$D$$ is connected, these local constants agree throughout $$D$$. Thus $$f$$ is constant.

**(iii)** If $$\overline f$$ is analytic, then $$g:=f+\overline f=2\operatorname{Re}f$$ is analytic and real-valued. Its imaginary part is constantly zero, so (ii) makes $$g$$ constant. Therefore $$\operatorname{Re}f$$ is constant, and (i) makes $$f$$ constant.

**(iv)** Let $$|f|=c$$ on $$D$$. If $$c=0$$, then $$f=0$$. If $$c>0$$, then $$f$$ has no zeros. By Exercise 2, $$1/f$$ is analytic, and

$$
\overline f=\frac{|f|^2}{f}=\frac{c^2}{f}
$$

is analytic as well. Part (iii) now implies that $$f$$ is constant.

### Exercise 6

If $$f$$ is even, then $$f(x_n)=f(-x_n)$$ for every $$n$$. If all odd coefficients vanish, its power series contains only even powers, so $$f(-z)=f(z)$$ throughout $$\rho B$$. This proves (i) and (iii) each imply the other direction needed for evenness.

Now assume $$f(x_n)=f(-x_n)$$ for every $$n$$ and define

$$
g(z):=f(z)-f(-z)=2\sum_{m=0}^{\infty}a_{2m+1}z^{2m+1}.
$$

The analytic function $$g$$ vanishes at all the $$x_n$$. Since $$x_n\ne0$$ and $$x_n\to0$$, its zeros have the limit point $$0\in\rho B$$. The identity theorem gives $$g\equiv0$$. Uniqueness of Taylor coefficients then yields $$a_{2m+1}=0$$ for every $$m$$. This proves the three conditions equivalent.

For odd functions the analogous conditions are: (i) $$f(-z)=-f(z)$$; (ii) $$f(-x_n)=-f(x_n)$$ for every $$n$$; (iii) $$a_{2m}=0$$ for every $$m\in\mathbb N$$. The same argument applies to $$f(z)+f(-z)=2\sum_{m\ge0}a_{2m}z^{2m}$$.

### Exercise 7

For $$n\ge1$$, factor the common product in the two terms on the right to obtain

$$
\begin{aligned}
\binom{\alpha-1}{n}+\binom{\alpha-1}{n-1}
&=\frac{(\alpha-1)\cdots(\alpha-n)}{n!}
+\frac{n(\alpha-1)\cdots(\alpha-n+1)}{n!}\\
&=\frac{(\alpha-1)\cdots(\alpha-n+1)((\alpha-n)+n)}{n!}\\
&=\binom{\alpha}{n}.
\end{aligned}
$$

For $$n\ge0$$, the second identity follows directly from the product definition:

$$
(n+1)\binom{\alpha}{n+1}
=\frac{\alpha(\alpha-1)\cdots(\alpha-n)}{n!}
=\alpha\binom{\alpha-1}{n}.
$$

These are the two formulas in (3.4).

### Exercise 8

For $$|z|<1$$, apply the binomial-series expansion to both factors and use $$ (1+z)^\alpha(1+z)^\beta=(1+z)^{\alpha+\beta}$$. The Cauchy product on the left is valid because both power series converge absolutely there. Its coefficient of $$z^k$$ is

$$
\sum_{\ell=0}^{k}\binom{\alpha}{\ell}\binom{\beta}{k-\ell},
$$

whereas the coefficient of $$z^k$$ in the right-hand expansion is $$\binom{\alpha+\beta}{k}$$. Equality of the analytic functions implies equality of their Taylor coefficients, proving the identity for all $$\alpha,\beta\in\mathbb C$$ and $$k\in\mathbb N$$.

### Exercise 9

The exponential function is entire, so

$$
\sinh z=\frac{e^z-e^{-z}}2,
\qquad
\cosh z=\frac{e^z+e^{-z}}2,
\qquad
\sin z=\frac{e^{iz}-e^{-iz}}{2i},
\qquad
\cos z=\frac{e^{iz}+e^{-iz}}2
$$

are entire. Solving the exponential equations shows

$$
\cosh z=0\iff z\in i\pi(\mathbb Z+\tfrac12),
\quad
\sinh z=0\iff z\in i\pi\mathbb Z,
$$

and

$$
\cos z=0\iff z\in\pi(\mathbb Z+\tfrac12),
\quad
\sin z=0\iff z\in\pi\mathbb Z.
$$

Thus each denominator in $$\tanh=\sinh/\cosh$$, $$\tan=\sin/\cos$$, and $$\cot=\cos/\sin$$ is nonzero on the stated domain. Its reciprocal is analytic there by Exercise 2, and multiplying by the analytic numerator proves that all three quotients are analytic on their stated domains.

### Exercise 10

Since $$\cos0=\cosh0=1$$, both functions take values near $$1$$ for $$z$$ near zero. Composing them with the analytic logarithm near $$1$$ proves that $$\log(\cos z)$$ and $$\log(\cosh z)$$ are analytic near zero. Their derivatives are $$-\tan z$$ and $$\tanh z$$. Dividing the Taylor series for sine and cosine, or for hyperbolic sine and cosine, gives

$$
\tan z=z+\frac{z^3}{3}+\frac{2z^5}{15}+\frac{17z^7}{315}+\frac{62z^9}{2835}+\cdots,
$$

$$
\tanh z=z-\frac{z^3}{3}+\frac{2z^5}{15}-\frac{17z^7}{315}+\frac{62z^9}{2835}+\cdots.
$$

Integrating term by term and using $$\log(\cos0)=\log(\cosh0)=0$$ yields

$$
\log(\cos z)
=-\frac{z^2}{2}-\frac{z^4}{12}-\frac{z^6}{45}-\frac{17z^8}{2520}-\frac{31z^{10}}{14175}-\cdots,
$$

$$
\log(\cosh z)
=\frac{z^2}{2}-\frac{z^4}{12}+\frac{z^6}{45}-\frac{17z^8}{2520}+\frac{31z^{10}}{14175}-\cdots.
$$

For the third function, the logarithm series converges for $$|z|<1$$. Squaring it and collecting the coefficient of $$z^n$$ gives

$$
(\log(1+z))^2
=\sum_{n=2}^{\infty}(-1)^n\left(\sum_{k=1}^{n-1}\frac1{k(n-k)}\right)z^n
=\sum_{n=2}^{\infty}(-1)^n\frac{2H_{n-1}}{n}z^n,
$$

where $$H_m:=\sum_{j=1}^{m}1/j$$. In particular,

$$
(\log(1+z))^2=z^2-z^3+\frac{11}{12}z^4-\frac56z^5+\frac{137}{180}z^6-\cdots.
$$

Restricting these series to real $$x$$ gives the requested real-analytic expansions. The first two series converge at least for $$|z|<\pi/2$$, and the last for $$|z|<1$$.

### Exercise 11

For $$|x|<1$$, the geometric series gives

$$
\frac1{1+x^2}=\sum_{k=0}^{\infty}(-1)^k x^{2k}.
$$

It converges uniformly on every compact subinterval of $$(-1,1)$$. Integrating from $$0$$ to $$x$$ term by term, and using $$\arctan(0)=0$$ and $$ (\arctan x)'=1/(1+x^2)$$, gives

$$
\arctan x=\sum_{k=0}^{\infty}(-1)^k\frac{x^{2k+1}}{2k+1}
=x-\frac{x^3}{3}+\frac{x^5}{5}-\frac{x^7}{7}+\cdots
$$

for $$|x|<1$$. At $$x=1$$ and $$x=-1$$, the series converges by the alternating-series criterion. Moreover, on $$[0,1]$$ its remainder after degree $$2N+1$$ is bounded by $$1/(2N+3)$$, uniformly in $$x$$. Hence its sum is continuous up to the endpoints; taking limits from the interior extends the identity to $$[-1,1]$$. Evaluating at $$x=1$$, where $$\arctan1=\pi/4$$, gives Leibniz’s formula:

$$
\frac\pi4=\sum_{k=0}^{\infty}\frac{(-1)^k}{2k+1}
=1-\frac13+\frac15-\frac17+\cdots.
$$
