# Chapter I — Foundations

## 4. Relations and Operations

### Exercise 1

Define
$$
f_*:X/\sim\;\longrightarrow Y/\mathrel{\dot\sim},
\qquad [x]\longmapsto[f(x)].
$$
This is well defined: if $$[x]=[y]$$, then $$x\sim y$$, so the hypothesis gives $$f(x)\mathrel{\dot\sim}f(y)$$ and therefore $$[f(x)]=[f(y)]$$. By construction, $$f_*\circ p_X=p_Y\circ f$$, so the diagram commutes.

If $$g:X/\sim\to Y/\mathrel{\dot\sim}$$ is another function making the diagram commute, then for every $$x\in X$$,
$$
g([x])=g(p_X(x))=p_Y(f(x))=[f(x)].
$$
Since every element of $$X/\sim$$ has the form $$[x]$$, this forces $$g=f_*$$. Thus the required function exists and is unique.

### Exercise 2

Let $$X$$ contain at least two elements and let $$\mathcal X=\mathcal P(X)\setminus\{X\}$$, ordered by inclusion. The function in Example 4.7(b) is the identity on $$\mathcal X$$, so its image is all of $$\mathcal X$$. If this image had an upper bound $$U\in\mathcal X$$, then $$\{x\}\subseteq U$$ for every $$x\in X$$, since each singleton is a proper subset of $$X$$. Hence $$X\subseteq U$$, giving $$U=X$$, contrary to $$U\in\mathcal X$$. Thus the image is not bounded above, and the function is not bounded.

### Exercise 3

Take $$X=\{0,1\}$$. Define $$f,g:X\to X$$ by $$f(0)=f(1)=0$$, $$g(0)=1$$, and $$g(1)=0$$. Then $$g\circ f$$ is the constant function with value $$1$$, whereas $$f\circ g$$ is the constant function with value $$0$$. Therefore composition is not commutative in general.

### Exercise 4

Let $$r$$ be the right identity supplied by the definition. The defining equivalences imply
$$
x\diamond y=r\quad\Longleftrightarrow\quad x=y,
$$
and also that $$ (x\diamond y)\diamond(y\diamond x)=r$$ holds exactly when $$x=y$$.

Suppose first that $$\diamond$$ were commutative. Choose $$x\ne r$$, which is possible because $$X$$ has more than one element. Then $$r\diamond x=x$$ by commutativity and the right identity, while $$x\diamond r=x$$. Since $$x\diamond x=r$$, we get
$$
(r\diamond x)\diamond(x\diamond r)=x\diamond x=r.
$$
The defining condition would then imply $$r=x$$, a contradiction. Thus $$\diamond$$ is not commutative.

If $$e$$ were a two-sided identity, then $$e\diamond r=e$$ because $$r$$ is a right identity, but $$e\diamond r=r$$ because $$e$$ is an identity. Hence $$e=r$$. Choose $$x\ne r$$. Since $$r$$ would then be a two-sided identity, $$r\diamond x=x\diamond r=x$$, so
$$
(r\diamond x)\diamond(x\diamond r)=x\diamond x=r.
$$
The defining condition would force $$r=x$$, a contradiction. Therefore there is no identity element.

### Exercise 5

Write $$\diamond$$ for the operation on $$X$$ and $$\star$$ for the operation on $$Y$$. By operation preservation and the anticommutativity condition on $$Y$$,
$$
x\sim y
\quad\Longleftrightarrow\quad f(x\diamond y)=r_Y
\quad\Longleftrightarrow\quad f(x)\star f(y)=r_Y
\quad\Longleftrightarrow\quad f(x)=f(y).
$$

**(a)** Thus $$\sim$$ is the relation of having the same image under $$f$$. It is reflexive, symmetric, and transitive because equality in $$Y$$ has these properties.

**(b)** Define $$\widetilde f:X/\sim\to Y$$ by $$\widetilde f([x])=f(x)$$. If $$[x]=[y]$$, then $$x\sim y$$ and hence $$f(x)=f(y)$$, so the definition is well defined. If $$\widetilde f([x])=\widetilde f([y])$$, then $$f(x)=f(y)$$, which gives $$x\sim y$$ and $$[x]=[y]$$; thus $$\widetilde f$$ is injective. If $$f$$ is surjective, every $$y\in Y$$ equals $$f(x)=\widetilde f([x])$$ for some $$x\in X$$, so $$\widetilde f$$ is surjective as well and therefore bijective.

### Exercise 6

Throughout, the notation $$\sup\{s,t\}$$ and $$\inf\{s,t\}$$ means the supremum and infimum of the two-element set $$\{s,t\}$$.

**(a)** An element $$u$$ is an upper bound of $$A\cup B$$ exactly when it is an upper bound of both $$A$$ and $$B$$. Since the suprema exist, this is equivalent to $$\sup(A)\le u$$ and $$\sup(B)\le u$$. Thus the upper bounds of $$A\cup B$$ are exactly the upper bounds of $$\{\sup(A),\sup(B)\}$$, and their least elements agree:
$$
\sup(A\cup B)=\sup\{\sup(A),\sup(B)\}.
$$
The dual lower-bound argument gives
$$
\inf(C\cup D)=\inf\{\inf(C),\inf(D)\}.
$$

**(b)** If $$A\subseteq B$$, then $$\sup(B)$$ is an upper bound of $$A$$. The least-upper-bound property gives $$\sup(A)\le\sup(B)$$. If $$C\subseteq D$$, then $$\inf(D)$$ is a lower bound of $$C$$, so $$\inf(C)\ge\inf(D)$$.

**(c)** Every element of $$A\cap B$$ is bounded above by both $$\sup(A)$$ and $$\sup(B)$$. Consequently, $$\sup(A\cap B)$$ is a lower bound of $$\{\sup(A),\sup(B)\}$$, and therefore
$$
\sup(A\cap B)\le\inf\{\sup(A),\sup(B)\}.
$$
Likewise, $$\inf(C\cap D)$$ is an upper bound of $$\{\inf(C),\inf(D)\}$$, so
$$
\inf(C\cap D)\ge\sup\{\inf(C),\inf(D)\}.
$$

**(d)** Let the partially ordered set be $$\mathcal P(\{a,b\})$$ with inclusion, and take $$A=\{\{a\}\}$$ and $$B=\{\{b\}\}$$. Then $$\sup(A)=\{a\}$$ and $$\sup(B)=\{b\}$$. These two sets are incomparable, so they have no maximum, while
$$
\sup(A\cup B)=\{a,b\}
$$
exists. Thus the supremum in (a) cannot in general be replaced by a maximum.

### Exercise 7

Let $$R$$ and $$S$$ be equivalence relations. The relation on $$X\times Y$$ is given by
$$
(x,y)(R\times S)(u,v)\quad\Longleftrightarrow\quad xRu\ \text{and}\ ySv.
$$
It is reflexive because $$xRx$$ and $$ySy$$. If $$(x,y)(R\times S)(u,v)$$, symmetry of $$R$$ and $$S$$ gives $$uRx$$ and $$vSy$$, so $$(u,v)(R\times S)(x,y)$$. If $$(x,y)(R\times S)(u,v)$$ and $$(u,v)(R\times S)(w,z)$$, transitivity gives $$xRw$$ and $$ySz$$, so $$(x,y)(R\times S)(w,z)$$. Hence $$R\times S$$ is an equivalence relation.

### Exercise 8

Take $$X=\{a,b\}$$. In $$\mathcal P(X)$$, the sets $$\{a\}$$ and $$\{b\}$$ are incomparable: neither is a subset of the other. Therefore $$\bigl(\mathcal P(X),\subseteq\bigr)$$ is not totally ordered.

### Exercise 9

Let $$\mathcal A$$ be a nonempty subset of $$\mathcal P(X)$$. Each $$A\in\mathcal A$$ is contained in $$\bigcup_{A\in\mathcal A}A$$. If $$U\subseteq X$$ is any upper bound of $$\mathcal A$$, then every $$A\in\mathcal A$$ is contained in $$U$$, so their union is contained in $$U$$. Thus
$$
\sup(\mathcal A)=\bigcup_{A\in\mathcal A}A.
$$

The intersection $$\bigcap_{A\in\mathcal A}A$$ is contained in each member of $$\mathcal A$$, so it is a lower bound. Any other lower bound is contained in every $$A\in\mathcal A$$ and hence in their intersection. Therefore
$$
\inf(\mathcal A)=\bigcap_{A\in\mathcal A}A.
$$
