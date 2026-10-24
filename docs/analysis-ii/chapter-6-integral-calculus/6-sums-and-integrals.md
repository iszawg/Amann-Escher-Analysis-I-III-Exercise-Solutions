# Chapter VI — Integral Calculus in One Variable

## 6. Sums and integrals

### Exercise 1

For fixed $$x\in\mathbb C$$, write

$$
F_x(z):=\frac{ze^{xz}}{e^z-1}
=\sum_{n=0}^{\infty}B_n(x)\frac{z^n}{n!}
$$
for $$z$$ near zero. The generating function gives

$$
F_{x+1}(z)-F_x(z)
=\frac{ze^{xz}(e^z-1)}{e^z-1}
=ze^{xz}.
$$

Expanding the right-hand side as

$$
ze^{xz}=\sum_{n=1}^{\infty}n x^{n-1}\frac{z^n}{n!}
$$
and comparing coefficients proves

$$
B_n(x+1)-B_n(x)=n x^{n-1}\qquad(n\ge1).
$$

For $$n=0$$, both sides of the intended identity are zero (the formula is read separately, without interpreting $$x^{-1}$$).

Next,

$$
F_x(-z)
=\frac{-ze^{-xz}}{e^{-z}-1}
=\frac{ze^{(1-x)z}}{e^z-1}
=F_{1-x}(z).
$$

Comparing coefficients of $$z^n/n!$$ in $$F_{1-x}(z)=F_x(-z)$$ yields

$$
B_n(1-x)=(-1)^nB_n(x),
$$
which is (v).

### Exercise 2

Multiplying the generating series for the Bernoulli numbers by
$$
\frac{e^z-1}{z}=\sum_{j=0}^{\infty}\frac{z^j}{(j+1)!}
$$
gives 1. Comparing the coefficient of $$z^m$$, after multiplying by $$(m+1)!$$, gives the recurrence

$$
\sum_{k=0}^{m}\binom{m+1}{k}B_k=0\qquad(m\ge1).
$$

Also, $$z/(e^z-1)+z/2$$ is even, so $$B_{2j+1}=0$$ for $$j\ge1$$. Starting from $$B_0=1$$, $$B_1=-1/2$$, $$B_2=1/6$$, $$B_4=-1/30$$, and $$B_6=1/42$$, the recurrence gives

$$
\begin{aligned}
B_8&=-\frac19\left(1+9B_1+36B_2+126B_4+84B_6\right)=-\frac1{30},\\
B_{10}&=-\frac1{11}\left(1+11B_1+55B_2+330B_4+462B_6+165B_8\right)=\frac5{66},\\
B_{12}&=-\frac1{13}\left(1+13B_1+78B_2+715B_4+1716B_6+1287B_8+286B_{10}\right)\\
&\quad=-\frac{691}{2730}.
\end{aligned}
$$

Now apply Proposition 6.6(i),
$$
B_n(X)=\sum_{k=0}^{n}\binom nk B_kX^{n-k}.
$$
The requested polynomials are

$$
\begin{aligned}
B_4(X)&=X^4-2X^3+X^2-\frac1{30},\\
B_5(X)&=X^5-\frac52X^4+\frac53X^3-\frac16X,\\
B_6(X)&=X^6-3X^5+\frac52X^4-\frac12X^2+\frac1{42},\\
B_7(X)&=X^7-\frac72X^6+\frac72X^5-\frac76X^3+\frac16X.
\end{aligned}
$$

### Exercise 3

We first establish two identities that locate the zeros. Proposition 6.6(v) gives

$$
B_{2m}(1-x)=B_{2m}(x),\qquad
B_{2m+1}(1-x)=-B_{2m+1}(x).
$$

The generating function also gives the duplication identity

$$
B_n\left(\frac{x}{2}\right)+B_n\left(\frac{x+1}{2}\right)
=2^{1-n}B_n(x).
$$

Indeed, the sum of the two generating functions on the left is
$$
\frac{ze^{xz/2}(1+e^{z/2})}{e^z-1}
=\frac{ze^{xz/2}}{e^{z/2}-1}
=2F_x\left(\frac z2\right).
$$
Setting $$x=0$$ in the coefficient identity gives

$$
B_n\left(\frac12\right)=\left(2^{1-n}-1\right)B_n,
\qquad B_n:=B_n(0).
$$

For odd indices greater than 1, $$B_{2m+1}=0$$, as follows from the evenness of $$z/(e^z-1)+z/2$$. Hence $$B_{2m+1}(0)=B_{2m+1}(1/2)=0$$ for every $$m\ge1$$.

For the base case,

$$
B_2(x)=x^2-x+\frac16
$$
has exactly one zero in $$(0,1/2)$$: it is strictly decreasing there and changes sign between 0 and $$1/2$$. Further,
$$
B_3(x)=x\left(x-\frac12\right)(x-1)>0\qquad(0<x<1/2).
$$

Suppose now that $$B_{2m-1}$$ has one strict sign throughout $$(0,1/2)$$. Since
$$
B_{2m}'(x)=2mB_{2m-1}(x),
$$
the polynomial $$B_{2m}$$ is strictly monotone on $$[0,1/2]$$. Its endpoint values satisfy
$$
B_{2m}(1/2)=\left(2^{1-2m}-1\right)B_{2m}(0).
$$
The factor is negative. Moreover, $$B_{2m}(0)\ne0$$: if it were zero, both endpoint values would be zero, contradicting strict monotonicity. Thus the endpoint values have opposite signs, and strict monotonicity proves that $$B_{2m}$$ has exactly one zero in $$(0,1/2)$$.

The derivative of $$B_{2m+1}$$ changes sign exactly once there, because $$B_{2m+1}'=(2m+1)B_{2m}$$ and $$B_{2m}$$ has exactly one zero. Thus $$B_{2m+1}$$ is strictly monotone on each side of that zero, with one interior maximum or minimum. Since $$B_{2m+1}(0)=B_{2m+1}(1/2)=0$$, it has one strict sign on $$(0,1/2)$$. This completes the induction.

For (i), the preceding argument shows that $$B_{2n+1}$$ has no zero in $$(0,1/2)$$. The reflection identity shows that it has no zero in $$(1/2,1)$$ either; its zeros in $$[0,1]$$ are precisely $$0,1/2,1$$.

For (ii), $$B_{2n}$$ has exactly one zero $$x_{2n}$$ in $$(0,1/2)$$. The reflection identity supplies exactly one more, $$x'_{2n}=1-x_{2n}$$, in $$(1/2,1)$$. There are no endpoint zeros, and these two zeros satisfy

$$
x_{2n}+x'_{2n}=1.
$$

### Exercise 4

Let $$\widetilde B_n$$ be the 1-periodic continuation of $$B_n|_{[0,1)}$$.

**(i)** On each interval $$(k,k+1)$$, where $$k\in\mathbb Z$$, we have
$$
\widetilde B_n(x)=B_n(x-k).
$$
For $$0\le j\le n-2$$, its derivative there is
$$
\widetilde B_n^{(j)}(x)
=\frac{n!}{(n-j)!}B_{n-j}(x-k).
$$
At an integer endpoint, the one-sided limits of this derivative agree: the relevant polynomial has degree $$n-j\ge2$$, and Proposition 6.6(iv) at 0 gives
$$
B_{n-j}(1)-B_{n-j}(0)=(n-j)0^{n-j-1}=0.
$$
Thus the derivatives through order $$n-2$$ join continuously at every integer, proving
$$
\widetilde B_n\in C^{n-2}(\mathbb R)\qquad(n\ge2).
$$

**(ii)** As printed, the exercise states this for $$n\in\mathbb N$$. With the book's convention that $$0\in\mathbb N$$, the case $$n=0$$ is false: $$\widetilde B_0\equiv1$$, so its integral over a unit interval is 1. The correct assertion is for $$n\ge1$$. For such $$n$$, periodicity and the derivative identity give, for every $$k\in\mathbb Z$$,

$$
\int_k^{k+1}\widetilde B_n(x)\,dx
=\int_0^1B_n(t)\,dt
=\frac{B_{n+1}(1)-B_{n+1}(0)}{n+1}
=0,
$$
because $$n+1\ge2$$ and Proposition 6.6(iv) makes the endpoint values equal.

**(iii)** The periodic function $$\widetilde B_{2n+1}$$ is bounded; let
$$
M_n:=\sup_{x\in\mathbb R}|\widetilde B_{2n+1}(x)|<\infty.
$$
Let $$K$$ be a compact subset of the half-plane $$\operatorname{Re}s>-2n$$, and put
$$
\sigma:=\min_{s\in K}\operatorname{Re}s>-2n.
$$
For $$s\in K$$ and $$x\ge1$$,

$$
\left|\widetilde B_{2n+1}(x)x^{-(s+2n+1)}\right|
\le M_nx^{-(\sigma+2n+1)}.
$$

The right-hand side is integrable on $$[1,\infty)$$ because $$\sigma+2n+1>1$$. Thus the defining improper integrals converge locally uniformly in $$s$$. The same argument applies after differentiating the integrand in $$s$$, since the extra factor $$\log x$$ still gives an integrable majorant on every such compact set. Therefore differentiation under the integral sign is valid, and

$$
F_n'(s)
=-\int_1^\infty \widetilde B_{2n+1}(x)\log x\,x^{-(s+2n+1)}\,dx.
$$

Hence $$F_n$$ is analytic on $$\{\operatorname{Re}s>-2n\}$$.

### Exercise 5

Let $$(a_k),(b_k)\in(\mathbb C^\times)^{\mathbb N}$$ and define asymptotic equivalence by $$a_k/b_k\to1$$.

- **Reflexivity:** $$a_k/a_k=1$$ for every $$k$$, so $$(a_k)\sim(a_k)$$.
- **Symmetry:** If $$a_k/b_k\to1$$, then $$b_k/a_k=(a_k/b_k)^{-1}\to1$$, so $$(b_k)\sim(a_k)$$.
- **Transitivity:** If $$a_k/b_k\to1$$ and $$b_k/c_k\to1$$, then
  $$
  \frac{a_k}{c_k}=\frac{a_k}{b_k}\frac{b_k}{c_k}\longrightarrow1.
  $$
  Thus $$(a_k)\sim(c_k)$$.

These are the three defining properties of an equivalence relation.

### Exercise 6

For integers $$n\ge2$$, the Dirichlet series for the Riemann zeta function gives
$$
\zeta(n)-1=\sum_{k=2}^{\infty}\frac1{k^n}.
$$
Since $$x\mapsto x^{-n}$$ is decreasing, for each $$k\ge3$$,
$$
\frac1{k^n}\le\int_{k-1}^{k}\frac{dx}{x^n}.
$$
Consequently,

$$
0\le\zeta(n)-1
\le\frac1{2^n}+\int_2^\infty\frac{dx}{x^n}
=\frac1{2^n}+\frac{2^{1-n}}{n-1}.
$$

The upper bound tends to zero as $$n\to\infty$$. Therefore
$$
\lim_{n\to\infty}\zeta(n)=1.
$$

### Exercise 7

Define the Simpson error functional on $$C^4[-h,h]$$ by
$$
L(f):=\int_{-h}^{h}f(x)\,dx-\frac h3\bigl(f(-h)+4f(0)+f(h)\bigr).
$$
This functional vanishes on every polynomial of degree at most three. Indeed, for the basis $$1,x,x^2,x^3$$, the integral and the displayed Simpson expression agree (both are $$2h$$ for 1, both are 0 for $$x$$ and $$x^3$$, and both are $$2h^3/3$$ for $$x^2$$).

Taylor's formula with integral remainder, expanded from $$-h$$, writes

$$
f(x)=p_3(x)+\int_{-h}^{h}\frac{(x-t)_+^3}{6}f^{(4)}(t)\,dt,
\qquad
(x-t)_+:=\max\{x-t,0\},
$$
where $$p_3$$ is a polynomial of degree at most three. Applying $$L$$ and using $$L(p_3)=0$$ gives

$$
L(f)=\int_{-h}^{h}K(t)f^{(4)}(t)\,dt,
\qquad
K(t):=L_x\left(\frac{(x-t)_+^3}{6}\right).
$$

For $$0\le t\le h$$, direct evaluation gives

$$
\begin{aligned}
K(t)
&=\frac{(h-t)^4}{24}-\frac h{18}(h-t)^3\\
&=-\frac{(h-t)^3(h+3t)}{72}.
\end{aligned}
$$

The kernel is even: reflecting $$x$$ to $$-x$$ leaves $$L$$ unchanged, and the reflected truncated cubic differs from the one defining $$K(t)$$ by a cubic polynomial, which $$L$$ annihilates. Hence, on the whole interval,

$$
K(t)=-\frac{(h-|t|)^3(h+3|t|)}{72}\le0.
$$

It follows that

$$
\begin{aligned}
\int_{-h}^{h}|K(t)|\,dt
&=\frac2{72}\int_0^h(h-t)^3(h+3t)\,dt\\
&=\frac2{72}\left(\frac{h^5}{4}+\frac{3h^5}{20}\right)
=\frac{h^5}{90}.
\end{aligned}
$$

Therefore

$$
\left|L(f)\right|
\le\|f^{(4)}\|_\infty\int_{-h}^{h}|K(t)|\,dt
=\frac{h^5}{90}\|f^{(4)}\|_\infty,
$$
which is the required estimate.

### Exercise 8

Partition $$[\alpha,\beta]$$ into the $$n$$ two-step panels
$$
[\alpha_{2j},\alpha_{2j+2}],\qquad 0\le j\le n-1,
$$
each of width $$2h$$. On each panel, Exercise 7 applies after translating its midpoint to 0: the local Simpson rule uses half-width $$h$$, so its error is at most
$$
\frac{h^5}{90}\|f^{(4)}\|_\infty.
$$
Adding the local rules gives exactly the sum $$S(f,[\alpha,\beta],h)$$ in the question: endpoints have weight 1, interior even-indexed nodes have weight 2, and odd-indexed nodes have weight 4, all multiplied by $$h/3$$. The triangle inequality therefore yields

$$
\left|\int_\alpha^\beta f(x)\,dx-S(f,[\alpha,\beta],h)\right|
\le\frac{nh^5}{90}\|f^{(4)}\|_\infty.
$$

Since $$\beta-\alpha=2nh$$, the right-hand side is

$$
\frac{\beta-\alpha}{180}h^4\|f^{(4)}\|_\infty,
$$
as claimed.

### Exercise 9

Write $$E=I-Q$$ for the signed error (exact integral minus numerical approximation), and $$T_n$$ and $$S_n$$ for the composite trapezoid and Simpson approximations. Put $$h_T=(b-a)/n$$ for the trapezoid step and $$h_S=(b-a)/(2n)$$ for the Simpson step:

$$
T_n=h_T\left(\frac{f(a)+f(b)}2+\sum_{j=1}^{n-1}f(a+jh_T)\right),
$$

$$
S_n=\frac{h_S}{3}\left(f(a)+f(b)+4\sum_{j=1}^{n}f(a+(2j-1)h_S)
+2\sum_{j=1}^{n-1}f(a+2jh_S)\right).
$$

For $$f(x)=1/(1+x^2)$$ on $$[0,1]$$, the exact value is $$I=\pi/4$$. Substitution of the grid values gives

$$
\begin{aligned}
T_2&=\frac12\left(\frac34+\frac45\right)=\frac{31}{40},\\
T_3&=\frac13\left(\frac34+\frac9{10}+\frac9{13}\right)=\frac{203}{260},\\
T_4&=\frac14\left(\frac34+\frac{16}{17}+\frac45+\frac{16}{25}\right)=\frac{5323}{6800},\\
S_1&=\frac16\left(1+4\cdot\frac45+\frac12\right)=\frac{47}{60},\\
S_2&=\frac1{12}\left(1+\frac12+2\cdot\frac45+4\left(\frac{16}{17}+\frac{16}{25}\right)\right)
=\frac{8011}{10200}.
\end{aligned}
$$

Thus the errors are

| Rule | Approximation $$Q$$ | Signed error $$E=\pi/4-Q$$ | Absolute error |
| --- | ---: | ---: | ---: |
| Trapezoid, $$n=2$$ | $$31/40$$ | $$\pi/4-31/40$$ | $$\approx 0.0103982$$ |
| Trapezoid, $$n=3$$ | $$203/260$$ | $$\pi/4-203/260$$ | $$\approx 0.00462893$$ |
| Trapezoid, $$n=4$$ | $$5323/6800$$ | $$\pi/4-5323/6800$$ | $$\approx 0.00260405$$ |
| Simpson, $$n=1$$ | $$47/60$$ | $$\pi/4-47/60$$ | $$\approx 0.00206483$$ |
| Simpson, $$n=2$$ | $$8011/10200$$ | $$\pi/4-8011/10200$$ | $$\approx 0.00000600653$$ |

For $$f(x)=1/x$$ on $$[1,2]$$, the exact value is $$I=\log2$$. The same rules give

$$
\begin{aligned}
T_2&=\frac12\left(\frac34+\frac23\right)=\frac{17}{24},\\
T_3&=\frac13\left(\frac34+\frac34+\frac35\right)=\frac7{10},\\
T_4&=\frac14\left(\frac34+\frac45+\frac23+\frac47\right)=\frac{1171}{1680},\\
S_1&=\frac16\left(1+4\cdot\frac23+\frac12\right)=\frac{25}{36},\\
S_2&=\frac1{12}\left(\frac32+\frac43+\frac{16}{5}+\frac{16}{7}\right)
=\frac{1747}{2520}.
\end{aligned}
$$

Here the signed errors are negative, so the rules overestimate this integral:

| Rule | Approximation $$Q$$ | Signed error $$E=\log2-Q$$ | Absolute error |
| --- | ---: | ---: | ---: |
| Trapezoid, $$n=2$$ | $$17/24$$ | $$\log2-17/24$$ | $$\approx 0.0151862$$ |
| Trapezoid, $$n=3$$ | $$7/10$$ | $$\log2-7/10$$ | $$\approx 0.00685282$$ |
| Trapezoid, $$n=4$$ | $$1171/1680$$ | $$\log2-1171/1680$$ | $$\approx 0.00387663$$ |
| Simpson, $$n=1$$ | $$25/36$$ | $$\log2-25/36$$ | $$\approx 0.00129726$$ |
| Simpson, $$n=2$$ | $$1747/2520$$ | $$\log2-1747/2520$$ | $$\approx 0.000106788$$ |

### Exercise 10

Let $$m=(\alpha+\beta)/2$$ and $$h=(\beta-\alpha)/2$$, and set $$g(t)=p(m+ht)$$ for $$-1\le t\le1$$. Since $$p$$ has degree at most three, so does $$g$$. Under the change of variables $$x=m+ht$$,

$$
\int_\alpha^\beta p(x)\,dx
=h\int_{-1}^{1}g(t)\,dt.
$$

It is enough to check that the one-panel Simpson rule is exact for a basis of the polynomials of degree at most three. For $$1,t,t^2,t^3$$, respectively, the exact integrals on $$[-1,1]$$ are

$$
2,\qquad 0,\qquad \frac23,\qquad 0.
$$

The Simpson values $$\frac13[g(-1)+4g(0)+g(1)]$$ are the same: they are $$2$$, $$0$$, $$2/3$$, and $$0$$. By linearity, the rule is exact for every polynomial $$g$$ of degree at most three, and hence for $$p$$ on $$[\alpha,\beta]$$.
