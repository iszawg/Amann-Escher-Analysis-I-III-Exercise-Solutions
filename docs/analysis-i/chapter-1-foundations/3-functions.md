# Chapter I — Foundations

## 3. Functions

### Exercise 1

Let $$f : X \to Y$$ and $$g : Y \to V$$ be bijective. Their composition $$g \circ f$$ is bijective, and its inverse is
$$
h:=f^{-1}\circ g^{-1}:V\to X.
$$
Indeed,
$$
\begin{aligned}
h\circ(g\circ f)
&=f^{-1}\circ g^{-1}\circ g\circ f\\
&=f^{-1}\circ\operatorname{id}_Y\circ f\\
&=\operatorname{id}_X,
\end{aligned}
$$
and
$$
\begin{aligned}
(g\circ f)\circ h
&=g\circ f\circ f^{-1}\circ g^{-1}\\
&=g\circ\operatorname{id}_Y\circ g^{-1}\\
&=\operatorname{id}_V.
\end{aligned}
$$
Thus $$h$$ is the inverse of $$g \circ f$$, proving
$$
(g\circ f)^{-1}=f^{-1}\circ g^{-1}.
$$

### Exercise 2

Let $$f : X \to Y$$. In the statements about complements, $$A^{\mathrm c}$$ is relative to $$X$$ and $$(A')^{\mathrm c}$$ is relative to $$Y$$. We use the set-valued map notation for images and preimages.

**(i)** If $$y \in f(A)$$, then $$y=f(x)$$ for some $$x\in A$$. Since $$A\subseteq B$$, the same $$x$$ belongs to $$B$$, so $$y\in f(B)$$. Hence $$f(A)\subseteq f(B)$$.

**(ii)** For $$y\in Y$$, membership in either side means that $$y=f(x)$$ for some $$x$$ belonging to at least one $$A_\alpha$$. Therefore
$$
f\left(\bigcup_{\alpha\in I}A_\alpha\right)
=\bigcup_{\alpha\in I}f(A_\alpha).
$$

**(iii)** If $$y\in f(\bigcap_{\alpha\in I}A_\alpha)$$, then $$y=f(x)$$ for some $$x$$ in every $$A_\alpha$$. Thus $$y$$ belongs to every $$f(A_\alpha)$$, and
$$
f\left(\bigcap_{\alpha\in I}A_\alpha\right)
\subseteq\bigcap_{\alpha\in I}f(A_\alpha).
$$

**(iv)** Take $$y\in f(X)\setminus f(A)$$. There is an $$x\in X$$ with $$f(x)=y$$. This $$x$$ cannot be in $$A$$, since that would put $$y$$ in $$f(A)$$. Hence $$x\in A^{\mathrm c}$$ and $$y\in f(A^{\mathrm c})$$. Therefore
$$
f(A^{\mathrm c})\supseteq f(X)\setminus f(A).
$$

For the preimage statements, let $$A',B'\subseteq Y$$.

**(i′)** If $$x\in f^{-1}(A')$$, then $$f(x)\in A'\subseteq B'$$, so $$x\in f^{-1}(B')$$. Thus $$f^{-1}(A')\subseteq f^{-1}(B')$$.

**(ii′)** For $$x\in X$$, $$f(x)$$ belongs to $$\bigcup_{\alpha\in I}A'_\alpha$$ exactly when it belongs to at least one $$A'_\alpha$$. Consequently
$$
f^{-1}\left(\bigcup_{\alpha\in I}A'_\alpha\right)
=\bigcup_{\alpha\in I}f^{-1}(A'_\alpha).
$$

**(iii′)** For $$x\in X$$, $$f(x)$$ belongs to $$\bigcap_{\alpha\in I}A'_\alpha$$ exactly when it belongs to every $$A'_\alpha$$. Hence
$$
f^{-1}\left(\bigcap_{\alpha\in I}A'_\alpha\right)
=\bigcap_{\alpha\in I}f^{-1}(A'_\alpha).
$$

**(iv′)** An element $$x\in X$$ belongs to $$f^{-1}((A')^{\mathrm c})$$ exactly when $$f(x)\notin A'$$, which is exactly when $$x\notin f^{-1}(A')$$. Complements on the right are relative to $$X$$, so
$$
f^{-1}((A')^{\mathrm c})=\bigl(f^{-1}(A')\bigr)^{\mathrm c}.
$$

Finally, for $$C\subseteq V$$,
$$
\begin{aligned}
x\in(g\circ f)^{-1}(C)
&\iff g(f(x))\in C\\
&\iff f(x)\in g^{-1}(C)\\
&\iff x\in f^{-1}\bigl(g^{-1}(C)\bigr).
\end{aligned}
$$
Thus, as set-valued preimage maps, $$(g \circ f)^{-1}=f^{-1}\circ g^{-1}$$.

The one-way inclusions above can all be strict. For a single example, let $$X=\{0,1\}$$, $$Y=\{a\}$$, and let $$f:X\to Y$$ be the constant function. For (i), take $$A=\varnothing$$ and $$B=\{0\}$$; then $$f(A)=\varnothing\subsetneq\{a\}=f(B)$$. For (iii), take $$A_1=\{0\}$$ and $$A_2=\{1\}$$; then
$$
f(A_1\cap A_2)=\varnothing\subsetneq\{a\}=f(A_1)\cap f(A_2).
$$
For (iv), take $$A=\{0\}$$; then
$$
f(X)\setminus f(A)=\varnothing\subsetneq\{a\}=f(A^{\mathrm c}).
$$
For (i′), take $$A'=\varnothing$$ and $$B'=\{a\}$$; then $$f^{-1}(A')=\varnothing\subsetneq X=f^{-1}(B')$$.

### Exercise 3

Let $$f:X\to Y$$ and $$g:Y\to V$$.

**(a)** If $$f$$ and $$g$$ are injective and $$g(f(x))=g(f(x'))$$, injectivity of $$g$$ gives $$f(x)=f(x')$$, and injectivity of $$f$$ then gives $$x=x'$$. Thus $$g\circ f$$ is injective.

If $$f$$ and $$g$$ are surjective, take any $$v\in V$$. Choose $$y\in Y$$ with $$g(y)=v$$, and then choose $$x\in X$$ with $$f(x)=y$$. It follows that $$(g\circ f)(x)=v$$, so $$g\circ f$$ is surjective.

**(b)** If $$h:Y\to X$$ satisfies $$h\circ f=\operatorname{id}_X$$, then $$f(x)=f(x')$$ implies
$$
x=h(f(x))=h(f(x'))=x',
$$
so $$f$$ is injective.

Conversely, suppose $$f$$ is injective and $$X$$ is nonempty. Fix $$x_0\in X$$ and define $$h:Y\to X$$ by sending each $$y$$ in $$f(X)$$ to its unique preimage under $$f$$, and each $$y$$ outside $$f(X)$$ to $$x_0$$. This is well defined by injectivity and gives $$h(f(x))=x$$ for every $$x\in X$$. Therefore $$h\circ f=\operatorname{id}_X$$.

There is a boundary exception in the statement as printed: if $$X=\varnothing$$ and $$Y\ne\varnothing$$, the empty function $$f:\varnothing\to Y$$ is injective, but no function $$h:Y\to\varnothing$$ exists. Thus the claimed equivalence holds when $$X$$ is nonempty; for $$X=\varnothing$$ it holds only when $$Y=\varnothing$$.

**(c)** If $$f\circ h=\operatorname{id}_Y$$ for some $$h:Y\to X$$, then for every $$y\in Y$$ we have $$y=f(h(y))$$, so $$f$$ is surjective.

Conversely, if $$f$$ is surjective, choose for each $$y\in Y$$ an element $$h(y)\in X$$ such that $$f(h(y))=y$$. Then $$h:Y\to X$$ is a function and $$f\circ h=\operatorname{id}_Y$$. This choice of one preimage for each $$y$$ uses the usual axiom-of-choice convention for arbitrary sets.

### Exercise 4

We prove the three conditions equivalent.

**(a) implies (b).** For every $$A\subseteq X$$, $$A\subseteq f^{-1}(f(A))$$ by definition. If $$f$$ is injective and $$x\in f^{-1}(f(A))$$, then $$f(x)=f(a)$$ for some $$a\in A$$. Injectivity gives $$x=a\in A$$. Thus
$$
f^{-1}(f(A))=A.
$$

**(b) implies (a).** Assume the equality holds for every $$A\subseteq X$$. If $$f(x)=f(y)$$, take $$A=\{x\}$$. Then $$y\in f^{-1}(f(\{x\}))=\{x\}$$, so $$y=x$$. Hence $$f$$ is injective.

**(a) implies (c).** The inclusion $$f(A\cap B)\subseteq f(A)\cap f(B)$$ always holds. If $$y\in f(A)\cap f(B)$$, then $$y=f(a)=f(b)$$ for some $$a\in A$$ and $$b\in B$$. Injectivity implies $$a=b$$, so $$y\in f(A\cap B)$$. Therefore
$$
f(A\cap B)=f(A)\cap f(B).
$$

**(c) implies (a).** Suppose $$f(A\cap B)=f(A)\cap f(B)$$ for all $$A,B\subseteq X$$. If distinct $$x,y\in X$$ had $$f(x)=f(y)$$, choose $$A=\{x\}$$ and $$B=\{y\}$$. Then $$f(A\cap B)=\varnothing$$, whereas $$f(A)\cap f(B)=\{f(x)\}$$, a contradiction. Thus $$f$$ is injective.

### Exercise 5

For the projection $$\operatorname{pr}_k:X_1\times\cdots\times X_n\to X_k$$ and $$y\in X_k$$, its fiber is the set of tuples whose coordinate with index $$k$$ is $$y$$:
$$
\operatorname{pr}_k^{-1}(y)
=X_1\times\cdots\times X_{k-1}\times\{y\}\times X_{k+1}\times\cdots\times X_n.
$$
Indeed, a tuple $$(x_1,\ldots,x_n)$$ lies in this preimage exactly when $$\operatorname{pr}_k(x_1,\ldots,x_n)=x_k=y$$; all its other coordinates may be chosen freely from their respective factors. Thus the fiber is also $$\{x\in X_1\times\cdots\times X_n:x_k=y\}$$. If $$y\notin X_k$$, no tuple has kth coordinate $$y$$, so the fiber is empty.

### Exercise 6

Define $$\Phi:\mathcal P(X)\to\{0,1\}^X$$ by sending each $$A$$ to its characteristic function:
$$\Phi(A)=\chi_A$$.

To prove injectivity, suppose $$\Phi(A)=\Phi(B)$$. Then the characteristic functions of $$A$$ and $$B$$ agree at every $$x\in X$$. Since a characteristic function equals 1 exactly on its set, $$x\in A$$ iff $$x\in B$$ for every $$x$$; hence $$A=B$$.

To prove surjectivity, let $$\varphi:X\to\{0,1\}$$ be any function and set
$$
A:=\{x\in X:\varphi(x)=1\}.
$$
For every $$x\in X$$, $$\varphi(x)=1$$ exactly when $$x\in A$$, and otherwise $$\varphi(x)=0$$. Therefore $$\varphi$$ is the characteristic function of $$A$$, so $$\varphi=\Phi(A)$$. Thus $$\Phi$$ is surjective, and hence bijective.

### Exercise 7

Let $$i:A\to X$$ be the inclusion, so $$i(a)=a$$.

**(a)** For every $$a\in A$$,
$$
(f\circ i)(a)=f(i(a))=f(a)=(f|_A)(a).
$$
The two functions have the same domain and codomain and agree at every input, so $$f|_A=f\circ i$$.

**(b)** By the definition of preimage under the restriction,
$$
\begin{aligned}
(f|_A)^{-1}(B)
&=\{a\in A:f(a)\in B\}\\
&=A\cap\{x\in X:f(x)\in B\}\\
&=A\cap f^{-1}(B).
\end{aligned}
$$
