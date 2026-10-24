# Chapter VII — Multivariable Differential Calculus

## 1. Continuous linear maps

Throughout, $$\mathbb K$$ is $$\mathbb R$$ or $$\mathbb C$$. For a finite product of normed spaces, use the maximum norm; any other usual product norm is equivalent. Exercises follow the numbering in the textbook.

### Exercise 1

Let $$F=F_1\times\cdots\times F_m$$ with $$\|(y_1,\ldots,y_m)\|_F=\max_j\|y_j\|_{F_j}$$, and let $$A x=(A_1x,\ldots,A_mx)$$.

If $$A\in L(E,F)$$, then the coordinate projection $$\pi_j:F\to F_j$$ has norm at most $$1$$, and $$A_j=\pi_jA$$. Thus every $$A_j$$ is continuous.

Conversely, if every $$A_j\in L(E,F_j)$$, then

$$
\|Ax\|_F=\max_j\|A_jx\|_{F_j}
\leq\left(\max_j\|A_j\|\right)\|x\|_E.
$$

Hence $$A\in L(E,F)$$. The Banach assumptions ensure that these are Banach spaces, but the boundedness equivalence itself only uses the finite product norm.

### Exercise 2

For matrices $$A=[a^j_k]$$ and $$B=[b^j_k]$$, the trace is $$\operatorname{tr}(A)=\sum_j a^j_j$$.

**(i)** For scalars $$\alpha,\beta\in\mathbb K$$,

$$
\operatorname{tr}(\alpha A+\beta B)
=\sum_j(\alpha a^j_j+\beta b^j_j)
=\alpha\operatorname{tr}(A)+\beta\operatorname{tr}(B).
$$

Thus the trace map is linear.

**(ii)** The diagonal entries of a product give

$$
\operatorname{tr}(AB)
=\sum_j\sum_k a^j_k b^k_j
=\sum_k\sum_j b^k_j a^j_k
=\operatorname{tr}(BA),
$$

where the middle equality just renames the finite summation indices and uses commutativity of scalar multiplication.

### Exercise 3

If $$A=SBS^{-1}$$, apply Exercise 2(ii) to the two square matrices $$SB$$ and $$S^{-1}$$:

$$
\operatorname{tr}(A)
=\operatorname{tr}\bigl((SB)S^{-1}\bigr)
=\operatorname{tr}\bigl(S^{-1}(SB)\bigr)
=\operatorname{tr}(B).
$$

So trace is invariant under similarity.

### Exercise 4

Let $$\mathcal E$$ and $$\mathcal F$$ be two bases of the finite-dimensional space $$E$$. Let $$P$$ be the change-of-coordinate matrix defined by $$[x]_{\mathcal E}=P[x]_{\mathcal F}$$. The two representation matrices of the same operator satisfy

$$
[A]_{\mathcal F}=P^{-1}[A]_{\mathcal E}P.
$$

They are similar, so Exercise 3 yields $$\operatorname{tr}([A]_{\mathcal E})=\operatorname{tr}([A]_{\mathcal F})$$. This proves that $$\operatorname{tr}(A):=\operatorname{tr}([A]_{\mathcal E})$$ is independent of the chosen basis.

In any fixed basis, the assignment $$A\mapsto[A]_{\mathcal E}$$ is linear, and matrix trace is linear by Exercise 2(i). Hence $$\operatorname{tr}:L(E)\to\mathbb K$$ is linear. Since $$L(E)$$ is finite-dimensional, every linear map from it to $$\mathbb K$$ is continuous; therefore $$\operatorname{tr}\in L(L(E),\mathbb K)$$.

For $$A,B\in L(E)$$, choose a basis and apply Exercise 2(ii) to their representation matrices. This gives $$\operatorname{tr}(AB)=\operatorname{tr}(BA)$$.

### Exercise 5

We use the convention that inner products are linear in the first argument. For each fixed $$y\in F$$, the map $$x\mapsto(Ax\mid y)_F$$ is a linear functional on the finite-dimensional Hilbert space $$E$$. The Riesz representation theorem gives a unique vector, denoted $$A^*y$$, such that

$$
(Ax\mid y)_F=(x\mid A^*y)_E\qquad(x\in E).
$$

Uniqueness in this identity implies that $$y\mapsto A^*y$$ is linear, so $$A^*\in L(F,E)$$. It also proves uniqueness of the adjoint.

The defining identity gives the operator rules. For scalars $$\alpha,\beta\in\mathbb K$$,

$$
(\alpha A+\beta B)^*=\overline\alpha A^*+\overline\beta B^*,
$$

so the adjoint map is conjugate linear. For composable operators,

$$
(ABx\mid y)=(Bx\mid A^*y)=(x\mid B^*A^*y),
$$

and uniqueness yields $$(AB)^*=B^*A^*$$. Applying the defining identity twice yields $$((A^*)^*)=A$$. If $$C$$ is invertible, then

$$
(C^{-1})^*C^*=(CC^{-1})^*=I
\quad\text{and}\quad
C^*(C^{-1})^*=(C^{-1}C)^*=I,
$$

so $$(C^{-1})^*=(C^*)^{-1}$$.

For the standard inner products on $$\mathbb K^n$$ and $$\mathbb K^m$$, direct substitution in the defining identity shows that the matrix of $$A^*$$ is the conjugate transpose $$[\overline{a^j_k}]$$.

If $$A=A^*$$, then

$$
(A^*A)^*=A^*A,\qquad (AA^*)^*=AA^*.
$$

Thus both $$A^*A\in L(E)$$ and $$AA^*\in L(F)$$ are self-adjoint.

### Exercise 6

Let $$\{\varphi_1,\ldots,\varphi_n\}$$ be an orthonormal basis. The trace is independent of basis by Exercise 4, so it can be computed in this basis:

$$
\operatorname{tr}(A)=\sum_{j=1}^n(A\varphi_j\mid\varphi_j).
$$

The diagonal entries of the matrix of $$A^*$$ are the conjugates of those of $$A$$. Therefore

$$
\operatorname{tr}(A^*)=\overline{\operatorname{tr}(A)}.
$$

This proves both claims.

### Exercise 7

Define $$A:B=\operatorname{tr}(B^*A)$$. Conjugate linearity of the adjoint and linearity of trace show that this form is linear in $$A$$ and conjugate linear in $$B$$. Also,

$$
\overline{A:B}
=\overline{\operatorname{tr}(B^*A)}
=\operatorname{tr}((B^*A)^*)
=\operatorname{tr}(A^*B)
=B:A.
$$

For an orthonormal basis $$\{\varphi_j\}$$ of $$E$$, Exercise 6 gives

$$
A:A=\operatorname{tr}(A^*A)
=\sum_j(A^*A\varphi_j\mid\varphi_j)
=\sum_j\|A\varphi_j\|^2.
$$

This is nonnegative and vanishes only when $$A$$ vanishes on a basis, hence only when $$A=0$$. Thus $$A:B$$ is an inner product, and finite dimensionality makes $$L(E,F)$$ complete.

For $$E=\mathbb K^n$$ and $$F=\mathbb K^m$$ with their Euclidean norms, write $$A=[a_{ij}]$$. Cauchy–Schwarz in each row gives

$$
\|Ax\|^2
=\sum_i\left|\sum_j a_{ij}x_j\right|^2
\leq\sum_i\left(\sum_j|a_{ij}|^2\right)\|x\|^2
=(A:A)\|x\|^2.
$$

Taking the supremum over unit vectors yields $$\|A\|_{L(E,F)}\leq\sqrt{A:A}$$. The latter is the Frobenius norm $$\|A\|$$ in the exercise.

### Exercise 8

The form is bilinear because it is a finite sum of products of coordinates. The symmetry $$g_{jk}=g_{kj}$$ gives

$$
(x\mid y)_g=\sum_{j,k}g_{jk}x^jy^k
=\sum_{j,k}g_{kj}y^kx^j
=(y\mid x)_g.
$$

For $$x\neq0$$, the assumed positive-definiteness bound gives

$$
(x\mid x)_g=\sum_{j,k}g_{jk}x^jx^k\geq\gamma|x|^2>0.
$$

Thus this is a real scalar product.

### Exercise 9

Since $$AB=BA$$, the operator $$A$$ commutes with every power of $$B$$ and hence, by norm convergence of the exponential series, with $$e^B$$. This proves $$Ae^B=e^BA$$.

For the second identity, the binomial formula is valid for commuting operators. Absolute convergence in the Banach algebra permits rearrangement of the double series:

$$
e^Ae^B
=\sum_{p,q\geq0}\frac{A^pB^q}{p!\,q!}
=\sum_{n\geq0}\frac1{n!}\sum_{p=0}^n\binom np A^pB^{n-p}
=\sum_{n\geq0}\frac{(A+B)^n}{n!}
=e^{A+B}.
$$

### Exercise 10

Let

$$
A=\begin{pmatrix}0&1\\0&0\end{pmatrix},
\qquad
B=\begin{pmatrix}0&0\\1&0\end{pmatrix}.
$$

Then $$AB=\begin{pmatrix}1&0\\0&0\end{pmatrix}$$ and $$BA=\begin{pmatrix}0&0\\0&1\end{pmatrix}$$, so they do not commute. Since $$A^2=B^2=0$$, we have $$e^A=I+A$$ and $$e^B=I+B$$. Also $$S:=A+B$$ satisfies $$S^2=I$$, and therefore

$$
e^{A+B}=\cosh(1)I+\sinh(1)S,
\qquad
e^Ae^B=I+A+B+AB.
$$

Their diagonal entries already differ, proving (i).

For (ii), set

$$
S=\begin{pmatrix}1&0\\0&-1\end{pmatrix},
\qquad
T=\begin{pmatrix}-1/2&\sqrt3/2\\sqrt3/2&1/2\end{pmatrix},
\qquad
A=2\pi iS,\quad B=2\pi iT.
$$

Direct multiplication gives $$S^2=T^2=(S+T)^2=I$$. If $$R^2=I$$, its exponential series separates into even and odd powers:

$$
e^{2\pi iR}=\cos(2\pi)I+i\sin(2\pi)R=I.
$$

Consequently $$e^A=e^B=e^{A+B}=I$$. The off-diagonal entries of $$ST$$ and $$TS$$ have opposite signs, so $$AB\neq BA$$. This gives the requested example.

### Exercise 11

Induction gives $$(BAB^{-1})^n=BA^nB^{-1}$$ for every integer $$n\geq0$$. Summing the norm-convergent exponential series,

$$
e^{BAB^{-1}}
=\sum_{n=0}^\infty\frac{BA^nB^{-1}}{n!}
=B\left(\sum_{n=0}^\infty\frac{A^n}{n!}\right)B^{-1}
=Be^AB^{-1}.
$$

### Exercise 12

The adjoint is continuous in finite dimensions, so it can be applied term by term to the norm-convergent exponential series. Using Exercise 5,

$$
(e^A)^*
=\left(\sum_{n=0}^\infty\frac{A^n}{n!}\right)^*
=\sum_{n=0}^\infty\frac{(A^*)^n}{n!}
=e^{A^*}.
$$

If $$A=A^*$$, this says $$(e^A)^*=e^A$$, so $$e^A$$ is self-adjoint. If $$A^*=-A$$, then

$$
(e^A)^*e^A=e^{-A}e^A=I,
$$

where the last equality follows from Exercise 9 because $$-A$$ and $$A$$ commute.

### Exercise 13

For the first matrix, let $$J$$ be the $$4\times4$$ matrix whose entries are all $$1$$. Since $$J^2=4J$$, induction gives $$J^k=4^{k-1}J$$ for $$k\geq1$$. Hence

$$
e^J=I+\sum_{k=1}^\infty\frac{4^{k-1}J}{k!}
=I+\frac{e^4-1}{4}J.
$$

For each of the other three matrices, write $$A=2I+N$$. The respective nilpotent parts are:

- $$N_1$$ has $$1$$ on the three entries immediately above the diagonal and zero elsewhere, so $$N_1^4=0$$.
- $$N_2$$ has $$1$$ in positions $$(1,2)$$ and $$(2,3)$$, so $$N_2^3=0$$.
- $$N_3$$ has $$1$$ only in position $$(1,2)$$, so $$N_3^2=0$$.

Because scalar multiples of the identity commute with every matrix, $$e^{2I+N}=e^2e^N$$. Thus the remaining answers, in the order printed, are

$$
e^{A_1}
=e^2\begin{pmatrix}
1&1&1/2&1/6\\
0&1&1&1/2\\
0&0&1&1\\
0&0&0&1
\end{pmatrix},
\qquad
e^{A_2}
=e^2\begin{pmatrix}
1&1&1/2&0\\
0&1&1&0\\
0&0&1&0\\
0&0&0&1
\end{pmatrix},
$$

$$
e^{A_3}
=e^2\begin{pmatrix}
1&1&0&0\\
0&1&0&0\\
0&0&1&0\\
0&0&0&1
\end{pmatrix}.
$$

The finite sums follow because the indicated powers of each $$N_j$$ vanish.

### Exercise 14

Differentiate the given identity at $$t=0$$. Since $$\frac{d}{dt}e^{tA}|_{t=0}=A$$, differentiating its right-hand side gives

$$
A=\begin{pmatrix}0&-1&0\\1&0&0\\0&0&0\end{pmatrix}.
$$

Conversely, the square of the upper-left $$2\times2$$ block is $$-I$$. Its exponential series therefore gives the cosine-sine rotation block in the question, while the last coordinate stays fixed. So this $$A$$ indeed has the required property.

### Exercise 15

Write $$u=(x,y)^{\mathsf T}$$ and

$$
M=\begin{pmatrix}3&-2\\4&-1\end{pmatrix}.
$$

The system is $$u'=Mu+(t,t^2)^{\mathsf T}$$. Since $$M^2-2M+5I=0$$, we have $$(M-I)^2=-4I$$ and

$$
e^{tM}=e^t\left(I\cos(2t)+\frac{M-I}{2}\sin(2t)\right).
$$

A polynomial particular solution can be found by setting $$p(t)=a_2t^2+a_1t+a_0$$ and equating powers of $$t$$ in $$p'=Mp+(t,t^2)^{\mathsf T}$$. The coefficient equations are

$$
Ma_2+(0,1)^{\mathsf T}=0,\qquad
Ma_1+(1,0)^{\mathsf T}=2a_2,\qquad
Ma_0+(0,1)^{\mathsf T}=a_1.
$$

Solving gives

$$
p(t)=
\begin{pmatrix}
-\frac25t^2-\frac3{25}t-\frac{11}{125}\\[2pt]
-\frac35t^2+\frac{18}{25}t-\frac9{125}
\end{pmatrix}.
$$

Therefore the general solution is

$$
\begin{pmatrix}x(t)\\y(t)\end{pmatrix}
=e^t\left(I\cos(2t)+\frac{M-I}{2}\sin(2t)\right)c+p(t),
\qquad c\in\mathbb R^2.
$$

The arbitrary vector $$c$$ supplies the two constants of the homogeneous system.

### Exercise 16

Eliminate $$x$$ and $$y$$ in favor of $$z$$. From $$z'=z-x$$ we obtain $$x=z-z'$$. The equation $$x'=z-y$$ then gives $$y=z-z'+z''$$. Substituting this into $$y'=z+e^t$$ yields

$$
z'''-z''+z'-z=e^t.
$$

The characteristic polynomial is $$(r-1)(r^2+1)$$. Since the forcing $$e^t$$ resonates with the root $$1$$, a particular solution is $$\frac12te^t$$. Thus

$$
z(t)=c_1e^t+c_2\cos t+c_3\sin t+\frac12te^t.
$$

The initial data imply $$z(0)=1$$, $$z'(0)=z(0)-x(0)=1$$, and $$z''(0)=y(0)-z(0)+z'(0)=\frac32$$. Solving for the constants gives $$c_1=\frac34$$, $$c_2=\frac14$$, and $$c_3=-\frac14$$. Recovering $$x=z-z'$$ and $$y=z-z'+z''$$ gives

$$
x(t)=\frac12(\cos t-e^t),\qquad
y(t)=e^t\left(\frac54+\frac t2\right)+\frac14(\cos t+\sin t),
$$

$$
z(t)=e^t\left(\frac34+\frac t2\right)+\frac14(\cos t-\sin t).
$$

At $$t=0$$ these formulas give the three stated initial values.

### Exercise 17

**The statement is false as printed.** The printed assumptions allow $$A=I_n$$: its off-diagonal entries are nonnegative and every row sum is $$1$$. But $$e^{tA}x=e^t x$$, so for any nonzero $$x\in H_c$$ with $$c\neq0$$, the coordinate sum of $$e^{tA}x$$ is $$e^tc$$, not $$c$$.

For preservation of the hyperplanes $$H_c$$, the required condition on the matrix is that each column sum vanish. In the convention $$(Ax)^j=\sum_k a^j_kx^k$$, this is

$$
\sum_{j=1}^n a^j_k=0\qquad(k=1,\ldots,n).
$$

Under this correction, if $$x(t)$$ solves $$x'=Ax$$, then

$$
\frac{d}{dt}\sum_jx^j(t)
=\sum_k\left(\sum_j a^j_k\right)x^k(t)=0.
$$

The coordinate sum is constant, so every solution starting in $$H_c$$ remains there. The additional off-diagonal nonnegativity is the usual generator condition that also ensures positivity preservation; it is not needed just for conservation of the sum.

### Exercise 18

Write $$z=u+iv$$ with real-valued $$u,v$$. Since $$b,c\in\mathbb R$$,

$$
z''+bz'+cz
=(u''+bu'+cu)+i(v''+bv'+cv).
$$

The left side is zero, so its real and imaginary parts vanish separately. Hence both $$u=\operatorname{Re}z$$ and $$v=\operatorname{Im}z$$ solve the real equation.

### Exercise 19

**(i)** The equation can be written as

$$
u''=g-bu'-cu.
$$

For $$k=0$$, the assumed solution is already twice continuously differentiable. If $$g\in C^k$$, this identity upgrades the regularity one derivative at a time: whenever $$u\in C^r$$ with $$r\geq2$$ and $$r-1\leq k$$, the right-hand side belongs to $$C^{r-1}$$, so $$u''\in C^{r-1}$$ and therefore $$u\in C^{r+1}$$. Starting from $$u\in C^2$$ and iterating gives $$u\in C^{k+2}$$ for finite $$k$$. If $$g$$ is smooth, the same induction applies for every finite order, so $$u\in C^\infty$$.

**(ii)** Set $$U=(u,u')^{\mathsf T}$$. Then the second-order equation is the first-order system

$$
U'=
\begin{pmatrix}0&1\\-c&-b\end{pmatrix}U
+\begin{pmatrix}0\\g(t)\end{pmatrix}.
$$

Fix any $$t_0\in\mathbb R$$. Variation of constants expresses the solution near $$t_0$$ as

$$
U(t)=e^{(t-t_0)M}U(t_0)
+\int_{t_0}^t e^{(t-s)M}\begin{pmatrix}0\\g(s)\end{pmatrix}\,ds,
\qquad
M=\begin{pmatrix}0&1\\-c&-b\end{pmatrix}.
$$

The matrix exponential is analytic, and $$g$$ is real analytic by assumption. Products and local antiderivatives of real-analytic functions are real analytic, so this formula shows $$U$$, and hence $$u$$, is real analytic near every $$t_0$$. Therefore $$u\in C^\omega(\mathbb R)$$.

### Exercise 20

The homogeneous characteristic equation is

$$
r^2+2\alpha r+\omega_0^2=0.
$$

Accordingly, its general solution is

$$
u_h(t)=
\begin{cases}
C_1e^{(-\alpha+\sqrt{\alpha^2-\omega_0^2})t}
+C_2e^{(-\alpha-\sqrt{\alpha^2-\omega_0^2})t},
&\alpha>\omega_0,\\[2pt]
(C_1+C_2t)e^{-\alpha t},&\alpha=\omega_0,\\[2pt]
e^{-\alpha t}\bigl(C_1\cos(\beta t)+C_2\sin(\beta t)\bigr),
&0<\alpha<\omega_0,\quad \beta=\sqrt{\omega_0^2-\alpha^2}.
\end{cases}
$$

For a particular solution, try $$u_p=P\sin(\omega t)+Q\cos(\omega t)$$. Put $$D=\omega_0^2-\omega^2$$ and $$d=2\alpha\omega$$. Matching sine and cosine coefficients gives

$$
DP-dQ=c,\qquad dP+DQ=0.
$$

Since $$D^2+d^2>0$$, the solution is $$P=cD/(D^2+d^2)$$ and $$Q=-cd/(D^2+d^2)$$. Thus

$$
u_p(t)=\frac{c\bigl(D\sin(\omega t)-d\cos(\omega t)\bigr)}{D^2+d^2},
\qquad
u(t)=u_h(t)+u_p(t).
$$

The positive damping $$\alpha>0$$ makes the denominator nonzero even when $$\omega=\omega_0$$.

### Exercise 21

**(i)** The homogeneous solutions of $$u''+u=0$$ are $$\cos t$$ and $$\sin t$$. For

$$
u_p(t)=\cos t\log(\cos t)+t\sin t,
$$

direct differentiation gives $$u_p''+u_p=1/\cos t$$. The logarithm is well-defined on the whole stated interval because $$\cos t>0$$ there. Hence

$$
u(t)=C_1\cos t+C_2\sin t+\cos t\log(\cos t)+t\sin t.
$$

**(ii)** The homogeneous solutions of $$u''+4u=0$$ are $$\cos(2t)$$ and $$\sin(2t)$$. Variation of parameters gives

$$
u_p(t)
=-\cos(2t)\int \sin(2t)\tan t\,dt
+\sin(2t)\int \cos(2t)\tan t\,dt.
$$

On this interval,

$$
\int \sin(2t)\tan t\,dt=t-\frac12\sin(2t),
\qquad
\int \cos(2t)\tan t\,dt=\log(\cos t)-\cos^2t.
$$

Substitution yields a particular solution, so the general solution is

$$
u(t)=C_1\cos(2t)+C_2\sin(2t)
-\cos(2t)\left(t-\frac12\sin(2t)\right)
+\sin(2t)\left(\log(\cos t)-\cos^2t\right).
$$

### Exercise 22

Every solution with initial value $$x_0$$ is $$u(t)=e^{tA}x_0$$.

Suppose first that all these solutions tend to zero. In finite dimensions, this implies $$e^{tA}x\to0$$ for every vector, and hence $$e^{tA}\to0$$ as an operator. If $$\lambda\in\sigma(A)$$, pass to the complexification if necessary and choose an eigenvector $$v\neq0$$. Then $$e^{tA}v=e^{t\lambda}v$$. This tends to zero only if $$\operatorname{Re}\lambda<0$$.

Conversely, suppose every eigenvalue has negative real part. In a complex Jordan basis, each block has the form $$J=\lambda I+N$$ with $$N$$ nilpotent, and

$$
e^{tJ}=e^{t\lambda}\left(I+tN+\frac{t^2N^2}{2!}+\cdots\right),
$$

where the sum is finite. Each entry is a polynomial in $$t$$ times $$e^{t\lambda}$$, which tends to zero when $$\operatorname{Re}\lambda<0$$. Thus $$e^{tA}\to0$$ and every solution tends to zero. The argument applies to real spaces by complexifying their matrices.

### Exercise 23

Because $$\operatorname{Re}\lambda>\|A\|$$,

$$
\|e^{-t(\lambda I-A)}\|
\leq e^{-t\operatorname{Re}\lambda}e^{t\|A\|}
=e^{-t(\operatorname{Re}\lambda-\|A\|)}.
$$

The right side is integrable, so the operator-valued integral

$$
R(\lambda)=\int_0^\infty e^{-t(\lambda I-A)}\,dt
$$

converges in norm. Differentiate the integrand:

$$
\frac{d}{dt}e^{-t(\lambda I-A)}
=-(\lambda I-A)e^{-t(\lambda I-A)}.
$$

Integrating this identity from $$0$$ to $$T$$ and letting $$T\to\infty$$ gives

$$
(\lambda I-A)R(\lambda)=I.
$$

Since $$R(\lambda)$$ is a norm limit of functions of $$A$$, it commutes with $$A$$, so also $$R(\lambda)(\lambda I-A)=I$$. Therefore

$$
(\lambda I-A)^{-1}=\int_0^\infty e^{-t(\lambda I-A)}\,dt.
$$

### Exercise 24

For all sufficiently large $$n$$, $$\|(t/n)A\|<1$$, so $$I-(t/n)A$$ is invertible by the Neumann series. Its logarithm is defined by the norm-convergent power series

$$
\log\left(I-\frac tnA\right)
=-\frac tnA+O(n^{-2})
$$

in operator norm, with $$t$$ and $$A$$ fixed. Consequently,

$$
-n\log\left(I-\frac tnA\right)=tA+O(n^{-1})\longrightarrow tA.
$$

Exponentiation is norm-continuous in a Banach algebra. Since $$\exp(\log(I-(t/n)A))=I-(t/n)A$$, it follows that

$$
\left(I-\frac tnA\right)^{-n}
=\exp\left(-n\log\left(I-\frac tnA\right)\right)
\longrightarrow e^{tA}.
$$

### Exercise 25

**The equivalence is false as printed.** There are two separate issues.

First, (i) need not imply the stated (ii), even over $$\mathbb R$$. Take $$E=\mathbb R$$, $$A=0$$, and $$C=\{1\}$$. Then $$e^{tA}C=C$$ for every real $$t$$, but for any $$\lambda>0$$,

$$
(\lambda I-A)^{-1}C=\{1/\lambda\}\not\subseteq\{1\}
$$

unless $$\lambda=1$$.

Second, (ii) need not imply invariance for all positive and negative times. Let $$E=\mathbb R^2$$, $$C=\mathbb R_+^2$$, and

$$
A=\begin{pmatrix}0&1\\0&0\end{pmatrix}.
$$

Here $$\|A\|=1$$ and, for every real $$\lambda>1$$,

$$
(\lambda I-A)^{-1}
=\begin{pmatrix}\lambda^{-1}&\lambda^{-2}\\0&\lambda^{-1}\end{pmatrix},
$$

which maps $$C$$ into itself. But $$e^{tA}=I+tA$$, and for $$t=-1$$ it sends $$(0,1)$$ to $$(-1,1)\notin C$$.

A standard corrected forward-time criterion uses the **normalized resolvent** $$J_\lambda(A):=\lambda(\lambda I-A)^{-1}$$ for real $$\lambda>\|A\|$$. For a closed convex set, $$e^{tA}C\subseteq C$$ for all $$t\geq0$$ is equivalent to $$J_\lambda(A)C\subseteq C$$ for all such $$\lambda$$. In one direction, Exercise 23 gives

$$
J_\lambda(A)x
=\int_0^\infty \lambda e^{-\lambda s}e^{sA}x\,ds,
$$

which is a convex average of points of $$C$$. In the other direction, for fixed $$t>0$$,

$$
e^{tA}=\lim_{n\to\infty}J_{n/t}(A)^n,
$$

by Exercise 24; every approximating operator preserves $$C$$, and closedness passes this property to the limit. To obtain invariance for **all** real $$t$$, the same normalized-resolvent condition must also hold for $$-A$$. If $$\mathbb K=\mathbb C$$, the averaging parameter here is real and positive; arbitrary complex $$\lambda$$ do not preserve real convex combinations.
