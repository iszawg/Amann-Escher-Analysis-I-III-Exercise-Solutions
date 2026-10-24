# Chapter VI — Integral Calculus in One Variable

## 2. Continuous extensions

Throughout, $$E$$, $$E_j$$, $$F$$, and $$F_j$$ are normed vector spaces over $$\mathbb K$$, as in the exercises. Product spaces below are given their usual maximum norm.

### Exercise 1

Assume first that $$A^{-1}\in L(F,E)$$. By boundedness of the inverse, there is a constant $$M\geq0$$ such that

$$
\|A^{-1}y\|\leq M\|y\|\qquad(y\in F).
$$

For $$x\in E$$, apply this estimate to $$y=Ax$$. Then

$$
\|x\|=\|A^{-1}(Ax)\|\leq M\|Ax\|\leq(M+1)\|Ax\|.
$$

Thus the required inequality holds with $$\alpha=1/(M+1)>0$$.

Conversely, suppose that some $$\alpha>0$$ satisfies $$\alpha\|x\|\leq\|Ax\|$$ for every $$x\in E$$. If $$Ax=0$$, this inequality forces $$x=0$$, so $$A$$ is injective. It is surjective by hypothesis, hence bijective. For $$y\in F$$, put $$x=A^{-1}y$$. The same inequality gives

$$
\|A^{-1}y\|=\|x\|\leq\frac1\alpha\|Ax\|=\frac1\alpha\|y\|.
$$

Therefore $$A^{-1}\in L(F,E)$$.

Now suppose also that $$A\in L(E,F)$$ and that $$E\neq\{0\}$$. Since $$A$$ is bijective, both $$A$$ and $$A^{-1}$$ are nonzero. Using $$I_E=A^{-1}A$$ and submultiplicativity of the operator norm,

$$
1=\|I_E\|\leq\|A^{-1}\|\,\|A\|.
$$

Consequently, $$\|A^{-1}\|\geq\|A\|^{-1}$$.

### Exercise 2

Define the operator on $$E$$

$$
C:=A^{-1}(B-A).
$$

The operator norm is submultiplicative, so

$$
\|C\|\leq\|A^{-1}\|\,\|B-A\|<1.
$$

Because $$E$$ is finite-dimensional, it is complete, and the operator space $$L(E)$$ is complete as well. Hence the geometric series

$$
S:=\sum_{k=0}^{\infty}(-C)^k
$$

converges in $$L(E)$$. Its partial sums satisfy

$$
(I_E+C)\sum_{k=0}^{N}(-C)^k
=\left(\sum_{k=0}^{N}(-C)^k\right)(I_E+C)
=I_E-(-C)^{N+1}.
$$

Since $$\|C\|<1$$, the last term tends to $$I_E$$ as $$N\to\infty$$. Thus $$S=(I_E+C)^{-1}$$. Finally,

$$
B=A(I_E+C),
$$

so $$B$$ is invertible, with inverse

$$
B^{-1}=(I_E+C)^{-1}A^{-1}.
$$

### Exercise 3

Write $$x=(x_k)_{k=1}^n$$ and let $$A=(a_{jk})_{j,k=1}^n$$. The operator norm in each part is computed using the stated norm on $$\mathbb K^n$$.

**(i)** Set $$M_1:=\max_{1\leq k\leq n}\sum_{j=1}^n|a_{jk}|$$, the largest column sum. For every $$x\in\mathbb K^n$$,

$$
|Ax|_1
=\sum_{j=1}^n\left|\sum_{k=1}^n a_{jk}x_k\right|
\leq\sum_{k=1}^n\left(\sum_{j=1}^n|a_{jk}|\right)|x_k|
\leq M_1|x|_1.
$$

Therefore $$\|A\|_{L(E_1)}\leq M_1$$. Choose a column $$k_0$$ whose sum is $$M_1$$ and take the standard basis vector $$e_{k_0}$$. Since $$|e_{k_0}|_1=1$$,

$$
|Ae_{k_0}|_1=\sum_{j=1}^n|a_{jk_0}|=M_1.
$$

Thus $$\|A\|_{L(E_1)}=M_1$$.

**(ii)** Applying the Cauchy–Schwarz inequality to each row gives

$$
\left|\sum_{k=1}^n a_{jk}x_k\right|^2
\leq\left(\sum_{k=1}^n|a_{jk}|^2\right)
\left(\sum_{k=1}^n|x_k|^2\right).
$$

Summing over $$j$$ yields

$$
|Ax|_2^2
\leq\left(\sum_{j=1}^n\sum_{k=1}^n|a_{jk}|^2\right)|x|_2^2.
$$

Taking square roots and then the supremum over $$|x|_2\leq1$$ proves

$$
\|A\|_{L(E_2)}
\leq\left(\sum_{j=1}^n\sum_{k=1}^n|a_{jk}|^2\right)^{1/2}.
$$

**(iii)** Set $$M_\infty:=\max_{1\leq j\leq n}\sum_{k=1}^n|a_{jk}|$$, the largest row sum. For every $$x\in\mathbb K^n$$,

$$
|Ax|_\infty
=\max_j\left|\sum_{k=1}^n a_{jk}x_k\right|
\leq\max_j\sum_{k=1}^n|a_{jk}|\,|x_k|
\leq M_\infty|x|_\infty.
$$

Hence $$\|A\|_{L(E_\infty)}\leq M_\infty$$. Choose a row $$j_0$$ whose sum is $$M_\infty$$. If $$a_{j_0k}\neq0$$, set $$x_k=\overline{a_{j_0k}}/|a_{j_0k}|$$; if $$a_{j_0k}=0$$, set $$x_k=1$$. Then $$|x|_\infty=1$$ and

$$
\left|\sum_{k=1}^n a_{j_0k}x_k\right|
=\sum_{k=1}^n|a_{j_0k}|=M_\infty.
$$

For real scalars, the same choice is $$x_k=\operatorname{sgn}(a_{j_0k})$$ when the entry is nonzero. Therefore $$\|A\|_{L(E_\infty)}=M_\infty$$.

### Exercise 4

Give $$B(\mathbb R^n)$$ the supremum norm $$\|f\|_\infty=\sup_{x\in\mathbb R^n}|f(x)|$$. The evaluation map $$\delta(f)=f(0)$$ is linear. For every bounded function $$f$$,

$$
|\delta(f)|=|f(0)|\leq\sup_{x\in\mathbb R^n}|f(x)|=\|f\|_\infty.
$$

Thus $$\delta\in L(B(\mathbb R^n),\mathbb R)$$ and $$\|\delta\|\leq1$$. The constant function $$\mathbf 1(x)=1$$ has $$\|\mathbf 1\|_\infty=1$$ and $$|\delta(\mathbf 1)|=1$$, so the upper bound is attained:

$$
\|\delta\|=1.
$$

### Exercise 5

Let $$T:=A_0\otimes A_1$$ denote the given coordinatewise map. With the maximum product norms, define

$$
\iota_0(e_0)=(e_0,0),\quad \iota_1(e_1)=(0,e_1),
\qquad
\pi_0(f_0,f_1)=f_0,\quad \pi_1(f_0,f_1)=f_1.
$$

Each inclusion $$\iota_j$$ and projection $$\pi_j$$ is bounded. If $$T$$ is bounded, then

$$
A_j=\pi_j\circ T\circ\iota_j\qquad(j=0,1)
$$

is a composition of bounded linear maps. Hence both $$A_0$$ and $$A_1$$ belong to $$L(E_j,F_j)$$.

Conversely, suppose $$A_0$$ and $$A_1$$ are bounded. For every $$(e_0,e_1)\in E_0\times E_1$$,

$$
\begin{aligned}
\|T(e_0,e_1)\|_{\max}
&=\max\{\|A_0e_0\|,\|A_1e_1\|\}\\
&\leq\max\{\|A_0\|,\|A_1\|\}
       \max\{\|e_0\|,\|e_1\|\}\\
&=\max\{\|A_0\|,\|A_1\|\}\,\|(e_0,e_1)\|_{\max}.
\end{aligned}
$$

Thus $$T\in L(E_0\times E_1,F_0\times F_1)$$, proving the equivalence.

### Exercise 6

Convergence $$A_n\to A$$ in $$L(E,F)$$ means convergence in operator norm. In particular, the sequence of norms $$\|A_n\|$$ is bounded: for all sufficiently large $$n$$,

$$
\|A_n\|\leq\|A\|+\|A_n-A\|\leq\|A\|+1,
$$

and the finitely many earlier terms are bounded as well. Let $$M:=\sup_n\|A_n\|<\infty$$. For each $$n$$, add and subtract $$A_nx$$ to obtain

$$
\begin{aligned}
\|A_nx_n-Ax\|
&\leq\|A_n(x_n-x)\|+\|(A_n-A)x\|\\
&\leq M\|x_n-x\|+\|A_n-A\|\,\|x\|.
\end{aligned}
$$

The first term tends to zero because $$x_n\to x$$, and the second tends to zero because $$A_n\to A$$ in operator norm. Therefore $$A_nx_n\to Ax$$ in $$F$$.

### Exercise 7

Linearity of $$A$$ implies that

$$
\ker(A)=\{x\in E:Ax=0\}
$$

is a vector subspace of $$E$$. To prove it is closed, let $$(x_n)$$ be any sequence in $$\ker(A)$$ converging to some $$x\in E$$. Since $$Ax_n=0$$ and $$A$$ is bounded,

$$
\|Ax\|=\|A(x-x_n)\|\leq\|A\|\,\|x-x_n\|\longrightarrow0.
$$

Thus $$Ax=0$$, so $$x\in\ker(A)$$. Every convergent sequence in the kernel therefore has its limit in the kernel; in the metric space $$E$$, this proves that $$\ker(A)$$ is closed.
