# Chapter IV — Differentiation in One Variable

## 1. Differentiability

### Exercise 1

All derivatives below are taken on the natural domains of the displayed functions. In particular, in (f) we require $$x>0$$ and $$\cos x\ne0$$.

**(a)** We first simplify the nested power:
$$
f(x)=(x^x)^x=x^{x^2}.
$$
Since $$x>0$$, logarithmic differentiation is valid. Taking logarithms and differentiating gives
$$
\log f(x)=x^2\log x,
\qquad
\frac{f'(x)}{f(x)}=2x\log x+x.
$$
Therefore
$$
f'(x)=x^{x^2}(2x\log x+x).
$$

**(b)** Write $$u(x)=x^x$$, so that $$f(x)=x^{u(x)}$$. First,
$$
\log u(x)=x\log x,
\qquad
u'(x)=x^x(\log x+1).
$$
Now take logarithms of $$f$$:
$$
\log f(x)=u(x)\log x.
$$
The product rule gives
$$
\frac{f'(x)}{f(x)}
=u'(x)\log x+\frac{u(x)}{x}
=x^x(\log x+1)\log x+\frac{x^x}{x}.
$$
Thus
$$
f'(x)=x^{x^x}\left(x^x(\log x+1)\log x+\frac{x^x}{x}\right).
$$

**(c)** Rewrite the power using the exponential:
$$
f(x)=x^{1/x}=\exp\left(\frac{\log x}{x}\right).
$$
The quotient rule yields
$$
\left(\frac{\log x}{x}\right)'=\frac{1-\log x}{x^2}.
$$
Applying the chain rule,
$$
f'(x)=x^{1/x}\frac{1-\log x}{x^2}.
$$

**(d)** Apply the chain rule twice to $$f(x)=\log(\log(1+x))$$:
$$
f'(x)=\frac{1}{\log(1+x)}\cdot\frac{1}{1+x}
=\frac{1}{(1+x)\log(1+x)}.
$$

**(e)** Take logarithms of $$f(x)=x^{\sin x}$$:
$$
\log f(x)=\sin x\log x.
$$
Differentiate the product on the right and then multiply by $$f(x)$$:
$$
\frac{f'(x)}{f(x)}
=\cos x\log x+\frac{\sin x}{x},
\qquad
f'(x)=x^{\sin x}\left(\cos x\log x+\frac{\sin x}{x}\right).
$$

**(f)** Let
$$
A(x)=x^{3/5}+\sin^3(1/x)-\tan^2x,
\qquad
f(x)=\sqrt[3]{A(x)}.
$$
Differentiate each term of $$A$$. For the middle term, use the chain rule with inner function $$1/x$$:
$$
A'(x)=\frac35x^{-2/5}
-\frac{3\sin^2(1/x)\cos(1/x)}{x^2}
-2\tan x\sec^2x.
$$
When $$A(x)\ne0$$, the derivative of the cube-root function gives
$$
f'(x)=\frac{A'(x)}{3\bigl(\sqrt[3]{A(x)}\bigr)^2}.
$$
Equivalently,
$$
f'(x)=
\frac{\frac35x^{-2/5}-\frac{3\sin^2(1/x)\cos(1/x)}{x^2}-2\tan x\sec^2x}
{3\bigl(\sqrt[3]{A(x)}\bigr)^2}.
$$

At a zero $$x_0$$ of $$A$$, the preceding formula cannot be used because its denominator is zero. On the domain $$x>0$$, $$\cos x\ne0$$, the function $$A$$ is analytic. If the zero has order $$r$$, write locally
$$
A(x)=(x-x_0)^rB(x),
\qquad
B(x_0)\ne0.
$$
Then $$f(x_0)=0$$ and
$$
\frac{|f(x)-f(x_0)|}{|x-x_0|}
\sim |\sqrt[3]{B(x_0)}|\,|x-x_0|^{r/3-1}.
$$
This tends to zero when $$r\ge4$$. When $$r=3$$, we can write $$f(x)=(x-x_0)\sqrt[3]{B(x)}$$, so
$$
f'(x_0)=\sqrt[3]{B(x_0)}.
$$
For $$r=1$$ or $$r=2$$, the difference quotient is unbounded in magnitude, so the derivative does not exist. Hence the cube root is differentiable at $$x_0$$ exactly when the zero of $$A$$ has order at least three.

**(g)** Let $$u(x)=\cos x$$ and $$v(x)=2+\sin(\log x)$$. The denominator never vanishes, since $$v(x)\ge1$$. Their derivatives are
$$
u'(x)=-\sin x,
\qquad
v'(x)=\frac{\cos(\log x)}{x}.
$$
The quotient rule now gives
$$
f'(x)=
\frac{-\sin x\bigl(2+\sin(\log x)\bigr)-\frac{\cos x\cos(\log x)}{x}}
{\bigl(2+\sin(\log x)\bigr)^2}.
$$

### Exercise 2

We separate the cases in which the oscillatory factor is absent or the function is already discontinuous at the origin.

If $$m=0$$, then for $$x\ne0$$,
$$
f_{0,n}(x)=x^n\sin1.
$$
For $$n\ge1$$ this is the polynomial $$x^n\sin1$$, including at $$x=0$$, so it is smooth. For $$n=0$$, the function equals $$\sin1$$ off zero and equals zero at zero, so it is discontinuous. If $$m\ge1$$ and $$n=0$$, the oscillation $$\sin(x^{-m})$$ has no limit at zero, and again the function is not continuous.

It remains to consider $$m\ge1$$ and $$n\ge1$$. For $$x\ne0$$, differentiating the oscillatory factor contributes the most singular power of $$x$$:
$$
\frac{d}{dx}\sin(x^{-m})
=-m x^{-(m+1)}\cos(x^{-m}).
$$
After $$k$$ derivatives, the term obtained by differentiating the trigonometric factor every time is
$$
(-m)^k x^{n-k(m+1)}
\sin\left(x^{-m}+\frac{k\pi}{2}\right).
$$
Every other term has at least one derivative falling on a power of $$x$$, and is of higher order by a factor of at least $$|x|^m$$. Thus, for each fixed $$k\ge1$$,
$$
f_{m,n}^{(k)}(x)
=(-m)^k x^{n-k(m+1)}
\sin\left(x^{-m}+\frac{k\pi}{2}\right)
+O\left(|x|^{n-k(m+1)+m}\right)
\quad (x\to0,\ x\ne0).
$$

Suppose first that $$k(m+1)<n$$. For every $$j\le k$$, the exponent $$n-j(m+1)$$ is positive, so the formula above shows that $$f_{m,n}^{(j)}(x)\to0$$ as $$x\to0$$. These values agree with derivatives at zero: inductively, if $$f_{m,n}^{(j-1)}(0)=0$$, then
$$
\frac{f_{m,n}^{(j-1)}(x)-f_{m,n}^{(j-1)}(0)}{x}
=O\left(|x|^{n-(j-1)(m+1)-1}\right)\longrightarrow0,
$$
because
$$
n-(j-1)(m+1)-1=n-j(m+1)+m>0.
$$
Consequently all derivatives through order $$k$$ exist at zero, equal zero there, and are continuous. Hence $$f_{m,n}\in C^k(\mathbb R)$$ whenever $$k(m+1)<n$$.

Now let $$k_0$$ be the smallest integer such that $$k_0(m+1)\ge n$$, and put $$\beta=n-k_0(m+1)\le0$$. In the derivative formula of order $$k_0$$, take
$$
x_j=\left(2\pi j+\frac{\pi}{2}-\frac{k_0\pi}{2}\right)^{-1/m}
$$
for sufficiently large $$j$$. Then $$x_j\to0$$ and the sine factor equals one. If $$\beta<0$$, the derivative along this sequence is unbounded. If $$\beta=0$$, also take
$$
y_j=\left(2\pi j+\frac{3\pi}{2}-\frac{k_0\pi}{2}\right)^{-1/m}.
$$
Along this second sequence the sine factor is minus one, so the derivative has two different limits. In both cases the error term is smaller than the leading term by a factor of order $$|x|^m$$. Thus the derivative of order $$k_0$$ on the punctured line does not extend continuously to zero, and $$f_{m,n}\notin C^{k_0}(\mathbb R)$$. It cannot belong to any higher class either.

Combining these cases, for $$m\ge1,n\ge1$$,
$$
f_{m,n}\in C^k(\mathbb R)
\quad\Longleftrightarrow\quad
k(m+1)<n.
$$
The largest such integer is
$$
\left\lfloor\frac{n-1}{m+1}\right\rfloor.
$$
For completeness, if $$m=0,n\ge1$$, the function is in $$C^\infty(\mathbb R)$$; for $$m=0,n=0$$ or $$m\ge1,n=0$$, it is not even continuous.

### Exercise 3

Because $$f(x)\ne0$$ for every $$x\in\mathbb K$$, the quotient
$$
h(x)=\frac{g(x)}{f(x)}
$$
is defined and differentiable everywhere. The quotient rule and the equations $$f'=f$$ and $$g'=g$$ imply
$$
h'(x)=\frac{g'(x)f(x)-g(x)f'(x)}{f(x)^2}
=\frac{g(x)f(x)-g(x)f(x)}{f(x)^2}=0.
$$
If $$\mathbb K=\mathbb R$$, the mean value theorem says that a differentiable function with zero derivative on an interval is constant. If $$\mathbb K=\mathbb C$$, take any two points $$z_0,z_1$$ and restrict $$h$$ to the line segment between them:
$$
H(t)=h\bigl(z_0+t(z_1-z_0)\bigr),\qquad 0\le t\le1.
$$
The chain rule gives $$H'(t)=h'(z_0+t(z_1-z_0))(z_1-z_0)=0$$, so the real and imaginary parts of $$H$$ are constant by the real mean value theorem. Thus $$h$$ has one constant value $$c\in\mathbb K$$, and
$$
g=cf.
$$

Finally, the differential equations themselves give all higher derivatives. Since $$f'=f$$, induction yields $$f^{(j)}=f$$ for every $$j\ge1$$; likewise $$g^{(j)}=g$$. In particular, both functions belong to $$C^\infty(\mathbb K,\mathbb K)$$.

### Exercise 4

At any $$z\in\mathbb C$$ and for any nonzero increment $$h$$, the difference quotient is
$$
\frac{\overline{z+h}-\overline z}{h}
=\frac{\overline h}{h}.
$$
Along real increments $$h=t$$ this quotient equals $$1$$. Along purely imaginary increments $$h=it$$ it equals $$-1$$. Since these two limits disagree as $$t\to0$$, the complex derivative does not exist at any $$z$$. Thus conjugation is nowhere complex differentiable.

### Exercise 5

Expand the numerator before taking the quotient:
$$
\frac{(z+h)\overline{(z+h)}-z\overline z}{h}
=\overline z+z\frac{\overline h}{h}+\overline h.
$$
At $$z=0$$ this becomes $$\overline h$$, which tends to zero. Therefore $$f$$ is complex differentiable at zero and $$f'(0)=0$$.

Now let $$z\ne0$$. If $$h$$ tends to zero through real values, then $$\overline h/h=1$$, and the quotient tends to
$$
\overline z+z.
$$
If $$h$$ tends to zero through purely imaginary values, then $$\overline h/h=-1$$, and it tends to
$$
\overline z-z.
$$
These limits differ by $$2z\ne0$$. Hence the complex derivative does not exist at any nonzero point.

### Exercise 6

**(a)** Substituting $$x=0$$ into the bound shows that $$f(0)=0$$. For any nonzero increment $$h\to0$$,
$$
\left\|\frac{f(h)-f(0)}{h}\right\|
\le K|h|^{\alpha-1}\longrightarrow0,
$$
because $$\alpha>1$$. The difference quotient therefore converges, so $$f$$ is differentiable at zero and
$$
f'(0)=0.
$$

**(b)** Here $$f(0)=0$$ is assumed. If $$f$$ were differentiable at zero, its difference quotients would converge to a vector and would therefore remain bounded near zero. But the lower bound gives
$$
\left\|\frac{f(h)-f(0)}{h}\right\|
\ge K|h|^{\alpha-1}\longrightarrow+\infty,
$$
because $$\alpha<1$$. This contradiction proves that $$f$$ is not differentiable at zero.

**(c)** The equality at $$x=0$$ forces $$f(0)=0$$. If $$f$$ is differentiable at zero, then for every nonzero $$h$$,
$$
\left\|\frac{f(h)-f(0)}{h}\right\|
=\frac{\|f(h)\|}{|h|}=K.
$$
Taking the limit and using continuity of the norm gives
$$
\|f'(0)\|=K.
$$
This condition alone does not guarantee differentiability when $$K>0$$. For example, if $$v\in E$$ is a unit vector, the maps
$$
f_1(h)=Khv,
\qquad
f_2(h)=K|h|v
$$
both satisfy $$\|f_j(h)\|=K|h|$$. The first is differentiable at zero. For real increments, the difference quotient of the second is $$Kv$$ from the right and $$-Kv$$ from the left, so it is not differentiable there. If $$K=0$$, the condition forces $$f=0$$, which is differentiable.

### Exercise 7

Write
$$
x=n+r,
\qquad
n=\lfloor x\rfloor,
\qquad
0\le r<1.
$$
When $$x$$ is not an integer, the integer part is constant in a neighborhood of $$x$$. Thus
$$
f(x)=n+\sqrt r
\quad\Longrightarrow\quad
\partial_-f(x)=\partial_+f(x)=\frac{1}{2\sqrt r}.
$$

At an integer $$n$$, consider the left and right difference quotients separately. For $$t>0$$,
$$
\frac{f(n-t)-f(n)}{-t}
=\frac{\sqrt{1-t}-1}{-t}
=\frac{1}{1+\sqrt{1-t}}
\longrightarrow\frac12.
$$
Thus
$$
\partial_-f(n)=\frac12.
$$
On the right,
$$
\frac{f(n+t)-f(n)}{t}
=\frac{\sqrt t}{t}
=\frac{1}{\sqrt t}\longrightarrow+\infty.
$$
There is no finite right derivative at an integer. Therefore $$f$$ is differentiable exactly at the nonintegers.

### Exercise 8

**(a)** The assertion that the three functions must be differentiable is false. On any interval containing zero, let
$$
f(x)=x,
\qquad
g(x)=-x.
$$
Both are differentiable, but
$$
|f(x)|=|x|,
\qquad
(f\vee g)(x)=|x|,
\qquad
(f\wedge g)(x)=-|x|.
$$
Each of these functions has unequal left and right derivatives at zero.

**(b)** All three functions are one-sided differentiable. To see the point that matters, let $$u$$ be differentiable at $$a$$. If $$u(a)\ne0$$, its sign is constant near $$a$$, so $$|u|$$ is locally either $$u$$ or $$-u$$. If $$u(a)=0$$, differentiability gives
$$
u(a+t)=u'(a)t+o(|t|).
$$
For positive $$t$$ this implies
$$
\lim_{t\downarrow0}
\frac{|u(a+t)|-|u(a)|}{t}
=|u'(a)|,
$$
while for negative $$t$$ it implies
$$
\lim_{t\uparrow0}
\frac{|u(a+t)|-|u(a)|}{t}
=-|u'(a)|.
$$
Thus $$|u|$$ has both one-sided derivatives at every point.

Finally, the maximum and minimum can be written as
$$
f\vee g=\frac{f+g+|f-g|}{2},
\qquad
f\wedge g=\frac{f+g-|f-g|}{2}.
$$
Apply the preceding result to $$u=f$$ and $$u=f-g$$. Sums and scalar multiples of one-sided differentiable functions are one-sided differentiable, which proves the claim.

### Exercise 9

**(a)** Differentiability at $$a$$ means that there is a remainder $$r(h)=o(|h|)$$ such that
$$
f(a+h)=f(a)+f'(a)h+r(h).
$$
Applying the same expansion to the increment $$-h$$ gives
$$
f(a-h)=f(a)-f'(a)h+r(-h),
\qquad
r(-h)=o(|h|).
$$
Subtracting these equalities and dividing by $$2h$$ yields
$$
\frac{f(a+h)-f(a-h)}{2h}
=f'(a)+\frac{r(h)-r(-h)}{2h}.
$$
The norm of the remainder term is at most
$$
\frac{\|r(h)\|+\|r(-h)\|}{2|h|},
$$
which tends to zero. Therefore
$$
\lim_{h\to0}\frac{f(a+h)-f(a-h)}{2h}=f'(a).
$$

**(b)** The converse is false. Let $$f(x)=|x|$$ and $$a=0$$. Then for every nonzero real $$h$$,
$$
\frac{f(h)-f(-h)}{2h}=0,
$$
so the symmetric quotient has a limit. However, the ordinary right and left derivatives are $$1$$ and $$-1$$, respectively. Hence $$f$$ is not differentiable at zero.

### Exercise 10

We use induction on $$n$$. For $$n=1$$, the product rule gives
$$
\partial(xf(x))=x\partial f(x)+f(x),
$$
which is the stated identity.

Suppose the identity holds for some $$n\ge1$$:
$$
\partial^n(xf(x))=x\partial^n f(x)+n\partial^{n-1}f(x).
$$
Differentiate both sides. The product rule on the first term gives
$$
\begin{aligned}
\partial^{n+1}(xf(x))
&=\partial\left(x\partial^n f(x)+n\partial^{n-1}f(x)\right)\\
&=\partial^n f(x)+x\partial^{n+1}f(x)+n\partial^n f(x)\\
&=x\partial^{n+1}f(x)+(n+1)\partial^n f(x).
\end{aligned}
$$
This is the formula with $$n+1$$ in place of $$n$$, completing the induction.

### Exercise 11

We prove the identity by induction on $$n$$. For $$n=1$$,
$$
\partial\left(x^0e^{1/x}\right)
=-\frac{e^{1/x}}{x^2},
$$
as required.

For the induction step, set
$$
u_n(x)=x^{n-1}e^{1/x}
$$
and assume
$$
\partial^n u_n(x)=(-1)^n\frac{e^{1/x}}{x^{n+1}}.
$$
Since $$xu_n(x)=x^ne^{1/x}$$, Exercise 10 at order $$n+1$$ gives
$$
\begin{aligned}
\partial^{n+1}\left(x^ne^{1/x}\right)
&=x\partial^{n+1}u_n(x)+(n+1)\partial^nu_n(x)\\
&=(-1)^n\left[
x\partial\left(\frac{e^{1/x}}{x^{n+1}}\right)
+(n+1)\frac{e^{1/x}}{x^{n+1}}
\right].
\end{aligned}
$$
For $$x>0$$,
$$
\partial\left(\frac{e^{1/x}}{x^{n+1}}\right)
=-\frac{e^{1/x}}{x^{n+3}}
-(n+1)\frac{e^{1/x}}{x^{n+2}}.
$$
After multiplying by $$x$$, the second term cancels with the added term in brackets. Hence
$$
\partial^{n+1}\left(x^ne^{1/x}\right)
=(-1)^n\left(-\frac{e^{1/x}}{x^{n+2}}\right)
=(-1)^{n+1}\frac{e^{1/x}}{x^{n+2}}.
$$
This proves the formula for every $$n\in\mathbb N^\times$$.

### Exercise 12

Rodrigues’ formula is
$$
P_n(x)=\frac{1}{2^n n!}\frac{d^n}{dx^n}(x^2-1)^n.
$$

**(a)** Expand the powers and take the indicated derivatives. For the first two cases,
$$
P_0(x)=1,
\qquad
P_1(x)=\frac12\frac{d}{dx}(x^2-1)=x.
$$
For the next cases,
$$
\begin{aligned}
P_2(x)
&=\frac18\frac{d^2}{dx^2}(x^4-2x^2+1)
=\frac12(3x^2-1),\\
P_3(x)
&=\frac1{48}\frac{d^3}{dx^3}(x^6-3x^4+3x^2-1)
=\frac12(5x^3-3x),\\
P_4(x)
&=\frac1{384}\frac{d^4}{dx^4}(x^8-4x^6+6x^4-4x^2+1)
=\frac18(35x^4-30x^2+3),\\
P_5(x)
&=\frac1{3840}\frac{d^5}{dx^5}(x^{10}-5x^8+10x^6-10x^4+5x^2-1)
=\frac18(63x^5-70x^3+15x).
\end{aligned}
$$

**(b)** The leading monomial of $$(x^2-1)^n$$ is $$x^{2n}$$. After differentiating $$n$$ times and dividing by $$2^n n!$$, its contribution is
$$
\frac{(2n)!}{2^n(n!)^2}x^n.
$$
All other monomials contribute terms of degree less than $$n$$. Thus $$P_n$$ has degree exactly $$n$$.

We next show that $$P_n$$ is orthogonal on $$[-1,1]$$ to every polynomial $$q$$ of degree less than $$n$$. Rodrigues’ formula and integration by parts $$n$$ times yield
$$
\int_{-1}^1P_n(x)q(x)\,dx
=\frac{(-1)^n}{2^n n!}
\int_{-1}^1(x^2-1)^nq^{(n)}(x)\,dx.
$$
There are no boundary terms: the polynomial $$(x^2-1)^n$$ has a zero of order $$n$$ at both endpoints, so it and its first $$n-1$$ derivatives vanish at $$-1$$ and $$1$$. Since $$\deg q<n$$, we also have $$q^{(n)}=0$$. Therefore
$$
\int_{-1}^1P_n(x)q(x)\,dx=0.
$$

Suppose, toward a contradiction, that $$P_n$$ has fewer than $$n$$ sign-changing zeros in $$(-1,1)$$. Let $$r_1,\ldots,r_s$$ be all those zeros and define
$$
q(x)=\prod_{j=1}^s(x-r_j).
$$
Then $$\deg q=s<n$$. At each sign-changing zero, both $$P_n$$ and $$q$$ change sign, so their product does not. At any other zero of $$P_n$$ in the interval, $$P_n$$ does not change sign. Consequently $$P_nq$$ has one constant sign throughout $$(-1,1)$$, apart from its zeros, and is not identically zero. Its integral is therefore nonzero. This contradicts the orthogonality just proved, because $$\deg q<n$$.

Thus $$P_n$$ has at least $$n$$ distinct sign-changing zeros in $$(-1,1)$$. Since its degree is $$n$$, it has exactly $$n$$ zeros there, and each zero is simple.
