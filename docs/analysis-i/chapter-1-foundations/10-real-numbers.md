# Chapter I — Foundations

## 10. The Real Numbers

### Exercise 1

**(a)** The set

$$
A=\{(x,y)\in\mathbb R^2:|x-1|+|y+1|\le1\}
$$

is the closed diamond centered at $$(1,-1)$$ with vertices $$(0,-1)$$, $$(1,0)$$, $$(2,-1)$$, and $$(1,-2)$$.

**(b)** The condition $$|x|\le|y|$$ describes the two closed vertical cones $$y\ge|x|$$ and $$y\le-|x|$$. Thus $$B$$ consists of the points in those cones that lie strictly outside the ellipse

$$
2x^2+y^2=1.
$$

The ellipse itself is excluded because the inequality is strict.

**(c)** The two linear inequalities imply

$$
\frac{x-1}{2}<y<2x+1,
$$

so $$x>-1$$. Together with $$x^2-y^2>1$$, which implies $$|x|>1$$, this gives $$x>1$$. Now $$y^2<x^2-1$$, and the first linear inequality gives $$y>(x-1)/2>0$$. The other linear inequality is automatic: $$y<\sqrt{x^2-1}<x<2x+1$$. Therefore

$$
C=\left\{(x,y)\in\mathbb R^2:x>1,\ \frac{x-1}{2}<y<\sqrt{x^2-1}\right\}.
$$

### Exercise 2

**(a)** Write $$K=\mathbb Q(\sqrt2)=\{a+b\sqrt2:a,b\in\mathbb Q\}$$. It is closed under addition, subtraction, and multiplication. If $$a+b\sqrt2\ne0$$, then

$$
\frac{1}{a+b\sqrt2}=\frac{a-b\sqrt2}{a^2-2b^2}.
$$

The denominator is nonzero: otherwise either $$a=b=0$$ or $$\sqrt2$$ would be rational. Hence $$K$$ is a subfield of $$\mathbb R$$ containing $$\mathbb Q$$.

The number $$\sqrt3$$ is not in $$K$$. If $$\sqrt3=a+b\sqrt2$$, squaring gives $$3=a^2+2b^2+2ab\sqrt2$$, so $$ab=0$$. Then either $$a^2=3$$ or $$b^2=3/2$$, both impossible for rational $$a,b$$.

To see that $$K$$ is not order complete, consider

$$
S=\{q\in\mathbb Q:q>0,\ q^2<3\}\subset K.
$$

Suppose $$s\in K$$ were the supremum of $$S$$ in $$K$$. If $$s<\sqrt3$$, rational density gives a rational $$q$$ with $$\max(s,0)<q<\sqrt3$$, so $$q\in S$$ and $$s$$ is not an upper bound. If $$s>\sqrt3$$, choose rational $$q$$ with $$\sqrt3<q<s$$; then $$q$$ is an upper bound of $$S$$ in $$K$$ smaller than $$s$$. Thus $$s=\sqrt3$$, which is not in $$K$$.

**(b)** Every subfield $$F\subset\mathbb R$$ contains $$1$$, all integer multiples of $$1$$, their negatives, and the inverses of nonzero integers. Thus it contains every rational number, so $$\mathbb Q\subset F$$. Since $$\mathbb Q$$ is itself a subfield of $$\mathbb R$$, it is the smallest one.

### Exercise 3

Let $$r=p/q$$ and $$s=u/v$$, with $$p,u\in\mathbb Z$$ and $$q,v\in\mathbb N^\times$$. Positive rational powers are defined using the unique positive roots from Proposition 10.9.

**(a)** Put $$w=a^{1/(qv)}$$. Then $$a^r=w^{pv}$$ and $$a^s=w^{uq}$$, so

$$
a^r a^s=w^{pv+uq}=a^{r+s}.
$$

**(b)** With the same $$w$$, the positive $$v$$th root of $$(a^r)^u=w^{pvu}$$ is $$w^{pu}$$. Hence

$$
(a^r)^s=w^{pu}=a^{rs}.
$$

**(c)** Let $$A=a^{1/q}$$ and $$B=b^{1/q}$$. Since $$(AB)^q=ab$$, uniqueness of the positive $$q$$th root gives $$(ab)^{1/q}=AB$$. Raising both sides to the integer power $$p$$ yields

$$
(ab)^r=a^r b^r.
$$

These arguments also cover negative integer numerators because all bases are positive.

### Exercise 4

Let $$m<n$$. If $$a=1$$, both roots equal $$1$$. It remains to consider the two cases below.

**(a)** Suppose $$0<a<1$$ and set $$\alpha=a^{1/m}$$ and $$\beta=a^{1/n}$$. Then $$0<\beta<1$$, so $$\beta^m>\beta^n=a=\alpha^m$$. Since the map $$x\mapsto x^m$$ is strictly increasing on $$\mathbb R_+$$, it follows that $$\alpha<\beta$$.

**(b)** If $$a>1$$, then $$\beta=a^{1/n}>1$$, so $$\beta^m<\beta^n=a=\alpha^m$$. Strict increase of $$x\mapsto x^m$$ gives $$\beta<\alpha$$.

### Exercise 5

Set

$$
S=\{y\in\mathbb R:a\le y\le b,\ y\le f(y)\}.
$$

Since $$f(a)>a$$, we have $$a\in S$$. The set is bounded above by $$b$$, so let $$z=\sup S$$. For each $$y\in S$$, monotonicity gives $$y\le f(y)\le f(z)$$. Thus $$f(z)$$ is an upper bound of $$S$$, and $$z\le f(z)$$.

Also $$z\le b$$, so $$f(z)\le f(b)<b$$. Consequently $$f(z)\in[a,b]$$. From $$z\le f(z)$$ and monotonicity, $$f(z)\le f(f(z))$$; hence $$f(z)\in S$$. Since $$z$$ is an upper bound of $$S$$, $$f(z)\le z$$. Combining the two inequalities gives $$f(z)=z$$.

### Exercise 6

We use induction on $$n$$. For $$n=0$$, both sides equal $$1$$. Suppose

$$
(1+x)^n\ge1+nx.
$$

Since $$x>-1$$, we have $$1+x>0$$. Multiplying by this positive number and using $$nx^2\ge0$$ gives

$$
(1+x)^{n+1}\ge(1+nx)(1+x)
=1+(n+1)x+nx^2
\ge1+(n+1)x.
$$

This proves Bernoulli's inequality for every $$n\in\mathbb N$$.

### Exercise 7

Let $$\alpha=\inf(M)>0$$. For every $$x\in M$$, $$\alpha\le x$$, and therefore

$$
\frac1x\le\frac1\alpha.
$$

Thus $$1/\alpha$$ is an upper bound of $$M^{-1}:=\{1/x:x\in M\}$$. If $$c<1/\alpha$$ and $$c\le0$$, any element of $$M^{-1}$$ is greater than $$c$$. If $$0<c<1/\alpha$$, then $$\alpha<1/c$$. Since $$\alpha$$ is the greatest lower bound of $$M$$, some $$x\in M$$ satisfies $$x<1/c$$, so $$1/x>c$$. Therefore no number below $$1/\alpha$$ is an upper bound, and

$$
\sup(M^{-1})=\frac1{\inf(M)}.
$$

### Exercise 8

Write $$A+B=\{a+b:a\in A,\ b\in B\}$$, and interpret suprema and infima in the extended real line.

Suppose first that $$A$$ and $$B$$ are bounded above, and let $$\alpha=\sup(A)$$ and $$\beta=\sup(B)$$. Every sum is at most $$\alpha+\beta$$. Given $$\varepsilon>0$$, choose $$a\in A$$ and $$b\in B$$ with $$a>\alpha-\varepsilon/2$$ and $$b>\beta-\varepsilon/2$$. Then $$a+b>\alpha+\beta-\varepsilon$$, proving

$$
\sup(A+B)=\sup(A)+\sup(B).
$$

If either set is unbounded above, fixing one element of the other set shows that $$A+B$$ is unbounded above, so the same identity holds with value $$+\infty$$. Applying this argument to $$-A$$ and $$-B$$ proves

$$
\inf(A+B)=\inf(A)+\inf(B).
$$

### Exercise 9

**(a)** Let $$A,B\subset(0,\infty)$$ be nonempty. If either set is unbounded above, fixing a positive element of the other shows that $$A\cdot B=\{ab:a\in A,\ b\in B\}$$ is unbounded above. Otherwise set $$\alpha=\sup(A)>0$$ and $$\beta=\sup(B)>0$$. Every product is at most $$\alpha\beta$$, and elements of $$A$$ and $$B$$ can be chosen arbitrarily close to their suprema. Thus

$$
\sup(A\cdot B)=\sup(A)\sup(B).
$$

Now let $$\alpha=\inf(A)\ge0$$ and $$\beta=\inf(B)\ge0$$. Every product is at least $$\alpha\beta$$. If both infima are positive, choose elements arbitrarily close to them from above to see that products approach $$\alpha\beta$$. If, for example, $$\alpha=0$$, fix $$b\in B$$ and choose elements $$a\in A$$ arbitrarily close to zero; then $$ab$$ approaches zero. The case $$\beta=0$$ is the same. Hence

$$
\inf(A\cdot B)=\inf(A)\inf(B).
$$

**(b)** Take $$A=B=\{-2,-1\}$$. Then $$\sup(A)=\sup(B)=-1$$ and $$\inf(A)=\inf(B)=-2$$, while $$A\cdot B=\{1,2,4\}$$. Therefore

$$
\sup(A)\sup(B)=1<4=\sup(A\cdot B)
$$

and

$$
\inf(A)\inf(B)=4>1=\inf(A\cdot B).
$$

### Exercise 10

Let $$x_1,\ldots,x_n\ge0$$ and let $$a=(x_1+\cdots+x_n)/n$$. If $$a=0$$, all the $$x_j$$ vanish and the result is immediate. Otherwise, divide each number by $$a$$. It is enough to prove that

$$
\prod_{j=1}^n x_j\le1
\quad\text{whenever}\quad
x_1+\cdots+x_n=n.
$$

For $$n=1$$ this is equality. For $$n\ge2$$, repeatedly choose a smallest and a largest entry, say $$u$$ and $$v$$, and replace both by $$(u+v)/2$$. The sum stays equal to $$n$$, and the product does not decrease because

$$
\left(\frac{u+v}{2}\right)^2-uv=\frac{(u-v)^2}{4}\ge0.
$$

At each step the sum of the squares of all entries decreases by $$(u-v)^2/2$$. This sum is bounded below, so the difference between the largest and smallest entries tends to zero. Their fixed average is $$1$$, so every entry tends to $$1$$. The products therefore tend to $$1$$, and since they never decrease, the original product is at most $$1$$. Undoing the normalization gives

$$
\left(\prod_{j=1}^n x_j\right)^{1/n}
\le \frac1n\sum_{j=1}^n x_j.
$$

### Exercise 11

Assume $$|\alpha|=\alpha_1+\cdots+\alpha_n\ge1$$. Form a list of $$|\alpha|$$ numbers by repeating $$x_j$$ exactly $$\alpha_j$$ times. Its product is $$x^\alpha=\prod_{j=1}^n x_j^{\alpha_j}$$, and its arithmetic mean is

$$
\frac{\sum_{j=1}^n\alpha_jx_j}{|\alpha|}
=\frac{x\mathbin{\cdot}\alpha}{|\alpha|}.
$$

Applying Exercise 10 to this list gives

$$
\sqrt[|\alpha|]{x^\alpha}
\le\frac{x\mathbin{\cdot}\alpha}{|\alpha|}.
$$

### Exercise 12

The construction in this section makes $$\mathbb R$$ an ordered field containing $$\mathbb Q$$ with its usual order. Proposition 10.6 shows that $$\mathbb N$$ is unbounded above in $$\mathbb R$$: for every $$x\in\mathbb R$$, some $$n\in\mathbb N$$ satisfies $$n>x$$. Thus $$\mathbb R$$ is an Archimedean ordered field.

### Exercise 13

Let $$x\in K$$. If $$x\le0$$, then $$1>x$$. If $$x>0$$, apply the hypothesis to $$1/x$$ to find $$r\in\mathbb Q$$ with

$$
0<r<\frac1x.
$$

Thus $$1/r>x$$. Since $$\mathbb Q$$ is Archimedean, there is some $$n\in\mathbb N$$ with $$n>1/r$$. Hence $$n>x$$, proving that $$K$$ is Archimedean.

### Exercise 14

If $$K$$ is Archimedean, then for every $$x\in K$$ there is some $$n\in\mathbb N$$ with $$n\cdot1>x$$. Thus the set $$\{n\cdot1:n\in\mathbb N\}$$ is not bounded above.

Conversely, if that set is not bounded above, then for each $$x\in K$$ there is an $$n\in\mathbb N$$ such that $$n\cdot1>x$$. This is exactly the Archimedean property.

### Exercise 15

For a nonzero rational function, use its reduced representation $$f=p/q$$ with $$q$$ monic. Define $$P$$ to contain zero and all such $$f$$ for which the leading coefficient of $$p$$ is positive. This is the stated condition $$p_n\ge0$$, with zero included.

If either of two elements of $$P$$ is zero, their sum and product remain in $$P$$. Otherwise write them as $$f=p/q$$ and $$g=r/s$$, where the numerators have positive leading coefficients and $$q,s$$ are monic. The numerator of their sum over denominator $$qs$$ is $$ps+rq$$. The term of higher degree determines its leading coefficient; if the two degrees agree, the positive leading coefficients add. The numerator of $$fg$$ is $$pr$$ and also has positive leading coefficient. When reducing either fraction, divide numerator and denominator by a common monic factor; this preserves the numerator's leading coefficient. Therefore $$P$$ is closed under addition and multiplication.

Every nonzero $$f$$ has numerator with either positive or negative leading coefficient, so exactly one of $$f$$ and $$-f$$ lies in $$P$$. Therefore

$$
P\cap(-P)=\{0\},\qquad P\cup(-P)=K.
$$

Also $$1\in P$$. Define the order by

$$
f\preceq g\quad\Longleftrightarrow\quad g-f\in P
$$

This relation is a total order. Reflexivity follows from $$0\in P$$; antisymmetry follows from $$P\cap(-P)=\{0\}$$; and transitivity follows from closure of $$P$$ under addition. Totality follows from $$P\cup(-P)=K$$. Adding the same element to both sides preserves the order, and multiplying two nonnegative elements gives a nonnegative element by closure of $$P$$ under multiplication.

If $$f\succ0$$, totality implies that either $$f^{-1}\in P$$ or $$-f^{-1}\in P$$. The second possibility would give $$-1=f(-f^{-1})\in P$$, contradicting the fact that $$-1$$ has a negative leading coefficient. Thus positive elements have positive inverses, and $$K$$ is an ordered field. Finally, for every $$n\in\mathbb N$$, the polynomial $$X-n$$ has positive leading coefficient, so $$n\prec X$$. The natural numbers are bounded above by $$X$$, and this ordered field is not Archimedean.

### Exercise 16

**(a)** Write $$I_n=[a_n,b_n]$$. The nesting implies that $$a_n$$ is increasing and $$b_n$$ is decreasing. Set

$$
a=\sup_{n\in\mathbb N}a_n,\qquad b=\inf_{n\in\mathbb N}b_n.
$$

For any $$m,n$$, a sufficiently late interval is contained in both $$I_m$$ and $$I_n$$ and is nonempty, so $$a_m\le b_n$$. Hence $$a\le b$$. Also,

$$
0\le b-a\le b_n-a_n=|I_n|
$$

for every $$n$$. The lengths tend to zero, so $$a=b=:x$$. Then $$a_n\le x\le b_n$$ for every $$n$$, and therefore $$x\in\bigcap_n I_n$$. If $$x,y$$ both belong to every interval, then $$|x-y|\le|I_n|$$ for every $$n$$, which forces $$x=y$$.

**(b)** By density of $$\mathbb Q$$ in $$\mathbb R$$, for each $$n\ge1$$ choose rationals $$p_n,q_n$$ such that

$$
p_n<x<q_n,\qquad q_n-p_n<\frac1n.
$$

Set $$a_n=\max(p_1,\ldots,p_n)$$ and $$b_n=\min(q_1,\ldots,q_n)$$. These are rational numbers, $$a_n\le x\le b_n$$, and the intervals $$I_n=[a_n,b_n]$$ are nonempty, closed, and nested. Moreover, $$|I_n|\le q_n-p_n<1/n$$. Their intersection contains $$x$$, and any point in it must be at distance at most $$|I_n|$$ from $$x$$ for every $$n$$. Thus $$\bigcap_n I_n=\{x\}$$.
