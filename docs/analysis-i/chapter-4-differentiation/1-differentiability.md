# Chapter IV — Differentiation in One Variable

## 1. Differentiability

### Exercise 1

All functions are considered on their natural domains, with $$x>0$$ where the exercise specifies that interval.

**(a)** Since $$f(x)=(x^x)^x=x^{x^2}$$, logarithmic differentiation gives

$$
f'(x)=x^{x^2}(2x\log x+x).
$$

**(b)** Put $$u(x)=x^x$$, so $$f(x)=x^{u(x)}$$. Then $$u'(x)=x^x(\log x+1)$$ and

$$
f'(x)=x^{x^x}\left(x^x(\log x+1)\log x+\frac{x^x}{x}\right).
$$

**(c)** Writing $$f(x)=\exp((\log x)/x)$$ yields

$$
f'(x)=x^{1/x}\frac{1-\log x}{x^2}.
$$

**(d)** The chain rule gives

$$
f'(x)=\frac{1}{(1+x)\log(1+x)}.
$$

**(e)** Logarithmic differentiation of $$f(x)=x^{\sin x}$$ gives

$$
f'(x)=x^{\sin x}\left(\cos x\log x+\frac{\sin x}{x}\right).
$$

**(f)** Set

$$
A(x)=x^{3/5}+\sin^3(1/x)-\tan^2x.
$$

At each $$x>0$$ with $$\cos x\ne0$$ and $$A(x)\ne0$$,

$$
f'(x)=\frac{\frac35x^{-2/5}-\frac{3\sin^2(1/x)\cos(1/x)}{x^2}-2\tan x\sec^2x}{3\bigl(\sqrt[3]{A(x)}\bigr)^2}.
$$

At a zero $$x_0$$ of $$A$$, write $$A(x)=(x-x_0)^rB(x)$$ locally, where $$B(x_0)\ne0$$. Such a factorization exists because $$A$$ is analytic wherever $$\tan x$$ is defined. The cube root is differentiable at $$x_0$$ exactly when $$r\ge3$$: its derivative is $$\sqrt[3]{B(x_0)}$$ for $$r=3$$ and $$0$$ for $$r\ge4$$. For a simple or double zero it is not differentiable.

**(g)** Since $$2+\sin(\log x)\ge1$$, the quotient rule gives

$$
f'(x)=\frac{-\sin x\bigl(2+\sin(\log x)\bigr)-\frac{\cos x\cos(\log x)}{x}}{\bigl(2+\sin(\log x)\bigr)^2}.
$$

### Exercise 2

If $$m=0$$, then for $$x\ne0$$ we have $$f_{0,n}(x)=x^n\sin1$$. Thus it is smooth when $$n\ge1$$, while $$f_{0,0}$$ is discontinuous at $$0$$. If $$m\ge1$$ and $$n=0$$, the oscillation $$\sin(x^{-m})$$ also prevents continuity at $$0$$.

Now suppose $$m\ge1$$ and $$n\ge1$$. Repeated differentiation for $$x\ne0$$ gives a leading term

$$
(-m)^k x^{n-k(m+1)}\sin\left(x^{-m}+\frac{k\pi}{2}\right),
$$

with all remaining terms of higher order in $$x$$. For $$k(m+1)<n$$, this and the lower order terms tend to zero, matching the derivatives at $$0$$. At the first integer $$k$$ for which $$k(m+1)\ge n$$, the leading term either oscillates without a limit or is unbounded along sequences tending to zero. Consequently,

$$
f_{m,n}\in C^k(\mathbb R)\quad\Longleftrightarrow\quad k(m+1)<n
$$

for $$m\ge1,n\ge1$$. Equivalently, the largest such integer is $$\left\lfloor\frac{n-1}{m+1}\right\rfloor$$.

### Exercise 3

Because $$f$$ never vanishes, $$h:=g/f$$ is differentiable on $$\mathbb K$$, and

$$
h'=\frac{g'f-gf'}{f^2}=0.
$$

Thus $$h$$ is constant: for $$\mathbb K=\mathbb R$$ this follows from the mean value theorem; for $$\mathbb K=\mathbb C$$, restrict $$h$$ to each line segment joining two points. Hence $$g=cf$$ for some $$c\in\mathbb K$$. Since $$f'=f$$ and $$g'=g$$, induction shows that all their derivatives exist and equal the functions themselves. Therefore $$f,g\in C^\infty(\mathbb K,\mathbb K)$$.

### Exercise 4

For $$h\ne0$$, the difference quotient at any $$z\in\mathbb C$$ is

$$
\frac{\overline{z+h}-\overline z}{h}=\frac{\overline h}{h}.
$$

This is $$1$$ for real $$h$$ and $$-1$$ for purely imaginary $$h$$. The limit therefore does not exist at any $$z$$, so conjugation is nowhere complex differentiable.

### Exercise 5

For $$f(z)=z\overline z$$, the difference quotient at $$z$$ is

$$
\frac{f(z+h)-f(z)}{h}=\overline z+z\frac{\overline h}{h}+\overline h.
$$

If $$z=0$$, this tends to $$0$$. If $$z\ne0$$, the term $$\overline h/h$$ depends on the direction of $$h\to0$$, so there is no limit. Thus $$f$$ is complex differentiable exactly at $$0$$, with $$f'(0)=0$$.

### Exercise 6

**(a)** The bound at $$x=0$$ implies $$f(0)=0$$. For $$x\ne0$$,

$$
\left\|\frac{f(x)-f(0)}{x}\right\|\le K|x|^{\alpha-1}\longrightarrow0.
$$

Hence $$f$$ is differentiable at $$0$$ and $$f'(0)=0$$.

**(b)** If $$f$$ were differentiable at $$0$$, its difference quotients would be bounded near $$0$$. But for $$x\ne0$$,

$$
\left\|\frac{f(x)-f(0)}{x}\right\|\ge K|x|^{\alpha-1}\longrightarrow+\infty,
$$

because $$\alpha<1$$. This is impossible, so $$f$$ is not differentiable at $$0$$.

**(c)** The condition alone does not decide differentiability. If $$f$$ is differentiable at $$0$$, then taking norms of the difference quotients gives $$\|f'(0)\|=K$$. For example, on a real domain with a unit vector $$v\in E$$, the functions $$f(x)=Kxv$$ and $$f(x)=K|x|v$$ satisfy the condition; the first is differentiable at $$0$$ and the second is not when $$K>0$$. For $$K=0$$, the function is identically zero.

### Exercise 7

Write $$x=n+r$$ with $$n=\lfloor x\rfloor$$ and $$0\le r<1$$. If $$0<r<1$$, then $$f(x)=n+\sqrt r$$, hence

$$
\partial_-f(x)=\partial_+f(x)=\frac{1}{2\sqrt r}.
$$

At an integer $$n$$, from the left,

$$
\partial_-f(n)=\lim_{t\downarrow0}\frac{f(n-t)-f(n)}{-t}
=\lim_{t\downarrow0}\frac{\sqrt{1-t}-1}{-t}=\frac12.
$$

From the right,

$$
\frac{f(n+t)-f(n)}{t}=\frac{\sqrt t}{t}=\frac1{\sqrt t}\longrightarrow+\infty.
$$

So the right derivative is not finite at integers, and $$f$$ is differentiable precisely at the nonintegers.

### Exercise 8

The claims in **(a)** are false in general: on an interval containing $$0$$, take $$f(x)=x$$ and $$g(x)=-x$$. Then $$|f(x)|=f\vee g=|x|$$ and $$f\wedge g=-|x|$$, none of which is differentiable at $$0$$.

All three functions in **(b)** are one-sided differentiable. Indeed,

$$
|f|=|f|,\qquad f\vee g=\frac{f+g+|f-g|}{2},\qquad f\wedge g=\frac{f+g-|f-g|}{2}.
$$

If a differentiable function $$u$$ satisfies $$u(a)=0$$, then

$$
\lim_{t\downarrow0}\frac{|u(a+t)|}{t}=|u'(a)|,
\qquad
\lim_{t\uparrow0}\frac{|u(a+t)|}{t}=-|u'(a)|.
$$

Thus $$|u|$$ has both one-sided derivatives at each point. Apply this to $$u=f$$ and $$u=f-g$$ in the displayed formulas; sums and scalar multiples preserve one-sided differentiability.

### Exercise 9

**(a)** Differentiability at $$a$$ gives

$$
f(a+h)=f(a)+f'(a)h+o(|h|),\qquad
f(a-h)=f(a)-f'(a)h+o(|h|).
$$

Subtracting and dividing by $$2h$$ proves

$$
\lim_{h\to0}\frac{f(a+h)-f(a-h)}{2h}=f'(a).
$$

**(b)** This implication is false. For $$f(x)=|x|$$ at $$a=0$$, the symmetric quotient is identically zero, but $$f$$ is not differentiable at $$0$$.

### Exercise 10

We prove the identity by induction. For $$n=1$$ it is the product rule. If it holds for $$n$$, differentiate once more:

$$
\begin{aligned}
\partial^{n+1}(xf(x))
&=\partial\bigl(x\partial^n f(x)+n\partial^{n-1}f(x)\bigr)\\
&=x\partial^{n+1}f(x)+(n+1)\partial^n f(x).
\end{aligned}
$$

This is the desired formula at order $$n+1$$.

### Exercise 11

For $$n=1$$, direct differentiation gives

$$
\partial(x^0e^{1/x})=-\frac{e^{1/x}}{x^2}.
$$

Assume the formula holds at order $$n$$. By Exercise 10, applied at order $$n+1$$ to $$x\cdot(x^{n-1}e^{1/x})$$,

$$
\begin{aligned}
\partial^{n+1}(x^ne^{1/x})
&=x\partial^{n+1}(x^{n-1}e^{1/x})+(n+1)\partial^n(x^{n-1}e^{1/x})\\
&=(-1)^n\left[x\partial\left(\frac{e^{1/x}}{x^{n+1}}\right)+(n+1)\frac{e^{1/x}}{x^{n+1}}\right]\\
&=(-1)^{n+1}\frac{e^{1/x}}{x^{n+2}}.
\end{aligned}
$$

This proves the identity for every $$n\in\mathbb N^\times$$ and $$x>0$$.

### Exercise 12

Rodrigues’ formula gives

$$
P_n(x)=\frac{1}{2^n n!}\frac{d^n}{dx^n}(x^2-1)^n.
$$

Differentiating for $$n=0,1,\ldots,5$$ yields

$$
\begin{aligned}
P_0(x)&=1,\\
P_1(x)&=x,\\
P_2(x)&=\frac12(3x^2-1),\\
P_3(x)&=\frac12(5x^3-3x),\\
P_4(x)&=\frac18(35x^4-30x^2+3),\\
P_5(x)&=\frac18(63x^5-70x^3+15x).
\end{aligned}
$$

The leading term of $$P_n$$ is

$$
\frac{(2n)!}{2^n(n!)^2}x^n,
$$

so $$P_n$$ has degree $$n$$. For every polynomial $$q$$ of degree less than $$n$$, integration by parts $$n$$ times gives

$$
\int_{-1}^1P_n(x)q(x)\,dx
=\frac{(-1)^n}{2^nn!}\int_{-1}^1(x^2-1)^nq^{(n)}(x)\,dx=0.
$$

All boundary terms vanish because $$(x^2-1)^n$$ and its first $$n-1$$ derivatives vanish at $$\pm1$$, while $$q^{(n)}=0$$. Now suppose $$P_n$$ had fewer than $$n$$ sign-changing zeros in $$(-1,1)$$, and let $$q$$ be the product of the corresponding distinct linear factors. Then $$\deg q<n$$, and $$P_nq$$ has a constant sign on $$(-1,1)$$ and is not identically zero. Its integral cannot be zero, contradicting the orthogonality just proved. Therefore $$P_n$$ has at least $$n$$ distinct zeros in $$(-1,1)$$. Since its degree is $$n$$, it has exactly $$n$$ such zeros, all simple.
