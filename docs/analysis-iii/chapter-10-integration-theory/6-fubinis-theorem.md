# Chapter X — Integration Theory

## 6. Fubini’s theorem

These solutions address Exercises 1–13. We write $$\lambda_n$$ for $$n$$-dimensional Lebesgue measure and use Tonelli's theorem for nonnegative functions, allowing the value $$+\infty$$. Fubini's theorem for signed or Banach-valued functions is invoked only after absolute integrability has been established. A centroid is defined when the total mass is positive and finite and the first moment is finite. Exercises 1, 4–6, and 13 have qualifications discussed below.

### Exercise 1

Write $$a=(a',h)$$, with $$a'\in\mathbb R^n$$ and $$h=a_{n+1}$$. If $$h\ne0$$, the horizontal section of the cylinder at height $$th$$ is $$B+ta'$$, and the section of the cone is $$(1-t)B+ta'$$, for $$0\le t<1$$. These sets are Lebesgue measurable: take a Borel set differing from $$B$$ by a null set and use the fact that the corresponding cylindrical or conical image of the null set is null on bounded pieces. The tip at $$t=1$$ is a singleton. Translation invariance and scaling give section measures $$\lambda_n(B)$$ and $$(1-t)^n\lambda_n(B)$$. Thus Tonelli and the substitution $$z=th$$ yield

$$
\lambda_{n+1}(Z_a(B))=|h|\lambda_n(B),\qquad
\lambda_{n+1}(K_a(B))=|h|\lambda_n(B)\int_0^1(1-t)^n\,dt
=\frac{|h|}{n+1}\lambda_n(B).
$$

The identities allow infinite volume when $$h\ne0$$. If $$h=0$$, both sets lie in the hyperplane $$x_{n+1}=0$$ and have measure zero, even when $$\lambda_n(B)=\infty$$; the displayed products then need the convention $$0\cdot\infty=0$$. The prose following the exercise in the printed text says “the total volume of $$n$$ cylinders”; the formula instead says the cone has **one $$(n+1)$$st** of the volume of a cylinder with the same base and height.

### Exercise 2

In cylindrical coordinates $$\rho=\sqrt{x^2+y^2}$$, the enclosed solid is

$$
V_{a,r}=\{(x,y,z):(\rho-a)^2+z^2\le r^2\}.
$$

Because $$a>r$$, its horizontal section at height $$z\in[-r,r]$$ is an annulus with radii $$a\pm\sqrt{r^2-z^2}$$. Its area equals

$$
\pi\left[(a+\sqrt{r^2-z^2})^2-(a-\sqrt{r^2-z^2})^2\right]
=4\pi a\sqrt{r^2-z^2}.
$$

Fubini and the area of a semicircle give

$$
\lambda_3(V_{a,r})=4\pi a\int_{-r}^r\sqrt{r^2-z^2}\,dz
=4\pi a\cdot\frac{\pi r^2}{2}=2\pi^2ar^2.
$$

### Exercise 3

Choose a finite nonnegative measurable representative of $$f$$, changing it on a null set if needed. The set $$R_f$$ is Lebesgue measurable, and its section at $$t\in J$$ is the closed $$n$$-ball of radius $$f(t)$$. Its measure is $$\omega_n f(t)^n$$, including zero radius. Tonelli gives

$$
\lambda_{n+1}(R_f)=\int_J\omega_n f(t)^n\,dt
=\omega_n\int_a^b f(t)^n\,dt.
$$

Both sides may be infinite, and the endpoints and unbounded intervals are handled by integration over $$J$$. For $$n=2$$, a slice perpendicular to the axis is a disk of area $$\pi f(t)^2$$; the solid's volume is the integral of these disk areas.

### Exercise 4

For a measurable set of finite positive measure with finite first moment, use the same centroid formula as for compact sets. Since a merely measurable $$f$$ need not give compact sets, this extension is needed for the stated hypotheses. Let $$M=\int_a^b f(x)\,dx$$.

**(a)** The vertical sections of $$A_f$$ have lengths $$f(x)$$, so $$\lambda_2(A_f)=M$$. If $$M>0$$, Tonelli gives

$$
\int_{A_f}x\,d(x,y)=\int_a^b xf(x)\,dx,\qquad
\int_{A_f}y\,d(x,y)=\frac12\int_a^b f(x)^2\,dx.
$$

The first integral is finite since $$[a,b]$$ is bounded, but the second need not be finite under $$f\in L^1$$ alone. If additionally $$f\in L^2$$, both first moments are finite and

$$
S(A_f)=\left(\frac{\int_a^b xf(x)\,dx}{\|f\|_1},
\frac{\int_a^b f(x)^2\,dx}{2\|f\|_1}\right).
$$

For a counterexample to existence under the printed assumption, take $$J=[0,1]$$ and $$f(x)=x^{-3/4}$$ for $$x>0$$, with $$f(0)=0$$. Then $$f\in L^1\setminus L^2$$, and the vertical first moment is infinite. If $$f=0$$ almost everywhere, the area is zero and the centroid is undefined.

**(b)** Let $$Q=\int_a^b f(t)^2\,dt>0$$. The section of $$R_f$$ at $$t$$ is a disk centered on the axis with area $$\pi f(t)^2$$. Its transverse first moments vanish by symmetry. The axial moment is finite because $$t$$ is bounded, and hence

$$
S(R_f)=\left(\frac{\pi\int_a^b t f(t)^2\,dt}{\pi Q},0,0\right)
=\left(\frac{\int_a^b t f(t)^2\,dt}{\|f\|_2^2},0,0\right).
$$

Again, $$Q=0$$ gives zero volume and no centroid.

**(c)** Whenever $$M>0$$ and $$f\in L^2$$, parts (a) and (b), or the disk-section formula directly, give

$$
\lambda_3(R_f)=\pi\int_a^b f(x)^2\,dx
=2\pi S_2(A_f)\lambda_2(A_f).
$$

For an arbitrary nonnegative $$L^1$$ function, the disk formula remains valid with value $$+\infty$$, but the centroid expression in the printed statement may be undefined, as the counterexample in (a) shows. Geometrically, the last product is the area of the generating region times the circumference traced by its centroid.

### Exercise 5

**(a)** Put $$c=\cos\alpha$$ and $$h=\sin\alpha$$. For $$0<\alpha<\pi/2$$, the cylinder section at height $$th$$ is a unit disk centered at $$(tc,0)$$, and the cone section is a disk of radius $$1-t$$ with the same center. Disk symmetry and the section areas show

$$
S(Z_a(B^2))=\left(c\frac{\int_0^1t\,dt}{\int_0^1dt},0,
 h\frac{\int_0^1t\,dt}{\int_0^1dt}\right)
=\left(\frac c2,0,\frac h2\right),
$$

$$
S(K_a(B^2))=\left(c\frac{\int_0^1t(1-t)^2\,dt}{\int_0^1(1-t)^2\,dt},0,
 h\frac{\int_0^1t(1-t)^2\,dt}{\int_0^1(1-t)^2\,dt}\right)
=\left(\frac c4,0,\frac h4\right).
$$

At $$\alpha=0$$ both solids have three-dimensional measure zero, so their centroids as defined in Exercise 4 do not exist. The displayed formulas give their limits as $$\alpha\downarrow0$$.

**(b)** Although $$A_\lambda$$ is unbounded, its area and first moments are finite. Direct integration gives

$$
\lambda_2(A_\lambda)=\frac1\lambda,\quad
\int_{A_\lambda}x\,d(x,y)=\frac1{\lambda^2},\quad
\int_{A_\lambda}y\,d(x,y)=\frac1{4\lambda}.
$$

Thus $$S(A_\lambda)=(1/\lambda,1/4)$$. It lies in $$A_\lambda$$ because $$1/4\le e^{-1}=e^{-\lambda/\lambda}$$.

**(c)** On $$[0,1]$$ let $$f=1$$ on $$[0,1/4]\cup[3/4,1]$$ and $$f=0$$ elsewhere. The region is the union of two unit-height rectangles, each of area $$1/4$$. Its centroid is $$(1/2,1/2)$$, while $$f(1/2)=0$$, so the centroid is outside the region.

### Exercise 6

Assume $$\rho_K=\int_K\rho\,dx>0$$, as required by the definition in Exercise 4. This condition is essential: if $$\rho=0$$ almost everywhere, the centroid is undefined. Normalize $$d\mu=\rho\,dx/\rho_K$$ to a probability measure. If $$s=\int_Kx\,d\mu(x)$$ were outside the nonempty compact convex set $$K$$, the separating hyperplane theorem would give a vector $$v$$ with

$$
v\cdot s>\sup_{x\in K}v\cdot x.
$$

But linearity and positivity of the integral give $$v\cdot s=\int_Kv\cdot x\,d\mu(x)\le\sup_Kv\cdot x$$, a contradiction. Hence $$S(K,\rho)\in K$$.

### Exercise 7

**(a)** Let $$V_n=\lambda_n(\Delta_n)$$ and $$V_0=1$$. At fixed last coordinate $$t\in[0,1]$$, the section is $$(1-t)\Delta_{n-1}$$. Tonelli therefore yields

$$
V_n=V_{n-1}\int_0^1(1-t)^{n-1}\,dt=\frac{V_{n-1}}n=\frac1{n!}.
$$

**(b)** Coordinate permutations preserve the simplex and measure, so all coordinate integrals are equal. For a fixed coordinate, its section gives

$$
\int_{\Delta_n}x_1\,dx
=\frac1{(n-1)!}\int_0^1t(1-t)^{n-1}\,dt
=\frac1{(n+1)!}.
$$

The last integral is $$1/[n(n+1)]$$, for instance by the substitution $$u=1-t$$. Division by $$V_n$$ gives $$S(\Delta_n)=(1/(n+1),\ldots,1/(n+1))$$.

### Exercise 8

Strong measurability of $$F(x,y)=f(x)g(y)$$ follows by approximating $$f$$ and $$g$$ almost everywhere by simple functions and taking their products. Tonelli then proves

$$
\int_{\mathbb R^{m+n}}\|F(x,y)\|\,d(x,y)
=\left(\int_{\mathbb R^m}|f(x)|\,dx\right)
 \left(\int_{\mathbb R^n}\|g(y)\|\,dy\right)<\infty.
$$

Thus $$F$$ is Bochner integrable. Fubini and linearity of the Bochner integral give

$$
\int_{\mathbb R^{m+n}}F
=\int_{\mathbb R^m}\left(f(x)\int_{\mathbb R^n}g(y)\,dy\right)dx
=\left(\int_{\mathbb R^m}f(x)\,dx\right)
 \left(\int_{\mathbb R^n}g(y)\,dy\right).
$$

### Exercise 9

On the triangle $$D$$, $$0\le x\le1$$ and $$0\le y\le1-x$$. Tonelli and the definition of the beta function give

$$
\begin{aligned}
\int_Dx^m y^n\,d(x,y)
&=\int_0^1x^m\left(\int_0^{1-x}y^n\,dy\right)dx\\
&=\frac1{n+1}\int_0^1x^m(1-x)^{n+1}\,dx
=\frac{B(m+1,n+2)}{n+1}.
\end{aligned}
$$

### Exercise 10

The integrand is $$y/\sqrt{x}$$ (assign any finite value on $$x=0$$, a null set). It is nonnegative, and Tonelli gives

$$
\int_{[0,1]^2}\frac{y}{\sqrt{x}}\,d(x,y)
=\left(\int_0^1x^{-1/2}\,dx\right)\left(\int_0^1y\,dy\right)
=2\cdot\frac12=1.
$$

The finite result also proves integrability.

### Exercise 11

The derivative $$\partial_j\varphi$$ is continuous with compact support, hence Bochner integrable. For each choice of the other coordinates, the one-variable function $$t\mapsto\varphi(x_1,\ldots,t,\ldots,x_n)$$ is continuously differentiable and compactly supported. The fundamental theorem of calculus gives its derivative integral over $$\mathbb R$$ as zero. Fubini, justified by the integrability just noted, now yields

$$
\int_{\mathbb R^n}\partial_j\varphi\,dx
=\int_{\mathbb R^{n-1}}\left(\int_{\mathbb R}\partial_j\varphi\,dx_j\right)dx_{\widehat j}=0.
$$

### Exercise 12

**(a)** For $$y>0$$, direct integration in $$x$$ gives

$$
\int_0^1\frac{x-y}{(x^2+y^2)^{3/2}}\,dx
=\frac1y-\frac{1+y}{y\sqrt{1+y^2}}.
$$

The apparent singularity at $$y=0$$ is removable in the outer integral. Using

$$
\int_0^1\frac{1-1/\sqrt{1+y^2}}y\,dy
=\log\frac{1+\sqrt2}{2},\qquad
\int_0^1\frac{dy}{\sqrt{1+y^2}}=\log(1+\sqrt2),
$$

we get $$\int_0^1\!\int_0^1 f(x,y)\,dx\,dy=-\log2$$. Swapping $$x$$ and $$y$$ changes the sign of $$f$$, so the other signed iterated integral is $$+\log2$$. Each inner integral and each resulting outer integral is finite; their disagreement does not contradict Fubini because $$f\notin L^1$$.

Indeed, in polar coordinates on any fixed angular sector contained in $$0<\theta<\pi/4$$ and bounded away from $$\pi/4$$, the integral of $$|f|$$ near the origin is bounded below by a positive constant times $$\int_0^\varepsilon dr/r=\infty$$. Tonelli consequently shows that **both** iterated integrals of $$|f|$$ are $$+\infty$$. The positive and negative parts also have infinite integrals, by the symmetry exchanging $$x$$ and $$y$$.

**(b)** Here $$f=|f|=(1-xy)^{-\alpha}\ge0$$, and the two orders agree by Tonelli, including when their common value is infinite. The binomial series and monotone convergence give the useful exact expression

$$
I_\alpha=\int_0^1\!\int_0^1(1-xy)^{-\alpha}\,dx\,dy
=\sum_{k=0}^\infty\frac{(\alpha)_k}{k!(k+1)^2},
$$

where $$(\alpha)_0=1$$ and $$(\alpha)_k=\alpha(\alpha+1)\cdots(\alpha+k-1)$$. Since $$(\alpha)_k/k!\sim k^{\alpha-1}/\Gamma(\alpha)$$, the series converges exactly for $$0<\alpha<2$$ and diverges to $$+\infty$$ for $$\alpha\ge2$$. Thus all four requested integrals equal $$I_\alpha$$ in the first case and $$+\infty$$ in the second. For $$\alpha=1$$ the series reduces to $$I_1=\sum_{k\ge0}(k+1)^{-2}=\pi^2/6$$. Equivalently, for $$0<\alpha<2$$ and $$\alpha\ne1$$,

$$
I_\alpha=\frac{\psi(2-\alpha)+\gamma}{1-\alpha},
$$

where $$\psi$$ is the digamma function and $$\gamma$$ Euler's constant; this follows by integrating first in $$y$$ and using $$\psi(z)+\gamma=\int_0^1(1-t^{z-1})/(1-t)\,dt$$ for $$z>0$$.

### Exercise 13

Assume $$n\ge1$$. The radial power criterion follows from polar coordinates: $$|x|^{-\beta}\mathbf1_{|x|<1}$$ is in $$L^s$$ exactly when $$\beta s<n$$, and $$|x|^{-\beta}\mathbf1_{|x|>1}$$ is in $$L^s$$ exactly when $$\beta s>n$$, for finite $$s$$.

**(a)** If $$1\le p<q<\infty$$, take $$f(x)=|x|^{-n/q}\mathbf1_{|x|<1}$$: it belongs to $$L^p$$ but not $$L^q$$. If $$p<q=\infty$$, use any $$0<\beta<n/p$$ in the same construction; the function is in $$L^p$$ but is not essentially bounded. If $$1\le q<p<\infty$$, take $$f(x)=|x|^{-n/q}\mathbf1_{|x|>1}$$, which lies in $$L^p$$ but not $$L^q$$. Finally, when $$p=\infty>q$$, the constant function 1 is bounded but not in $$L^q(\mathbb R^n)$$. These examples cover every distinct pair.

**(b)** If $$X$$ is bounded, $$\lambda_n(X)<\infty$$. For $$1\le q<p<\infty$$, Hölder's inequality yields

$$
\|f\|_{L^q(X)}\le\lambda_n(X)^{1/q-1/p}\|f\|_{L^p(X)}.
$$

For $$p=\infty$$ the same bound follows directly. Thus $$L^p(X)\subset L^q(X)$$. To see the inclusion is strict when $$X$$ is nonempty and open, choose a ball $$B(x_0,r)\subset X$$ and set $$g(x)=|x-x_0|^{-n/p}$$ on that ball and zero elsewhere when $$p<\infty$$. The power criterion gives $$g\in L^q(X)\setminus L^p(X)$$. For $$p=\infty$$ choose instead $$0<\beta<n/q$$: the analogous function belongs to $$L^q(X)$$ but is unbounded in the essential sense. If $$X=\varnothing$$, both spaces are zero, so the printed strict inclusion needs the implicit nonemptiness assumption.
