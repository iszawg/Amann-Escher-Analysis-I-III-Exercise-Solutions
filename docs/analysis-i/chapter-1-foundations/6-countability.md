# Chapter I — Foundations

## 6. Countability

### Exercise 1

We use induction on $$n$$. For $$n=1$$, every injective map from $$\{1\}$$ to itself is the identity, hence bijective.

Suppose the claim holds for $$n$$, and let $$f:\{1,\ldots,n+1\}\to\{1,\ldots,n+1\}$$ be injective. Put $$k=f(n+1)$$ and define $$g$$ by swapping $$k$$ and $$n+1$$ while fixing every other element. Then $$g$$ is bijective and $$h:=g\circ f$$ is injective, with $$h(n+1)=n+1$$. For each $$j\le n$$, injectivity gives $$h(j)\ne n+1$$, so the restriction of $$h$$ to $$\{1,\ldots,n\}$$ is an injective map into that same set. By the induction hypothesis, this restriction is bijective. Together with $$h(n+1)=n+1$$, this shows that $$h$$ is bijective. Since $$g$$ is bijective, $$f=g^{-1}\circ h$$ is bijective as well.

### Exercise 2

**(a)** Write $$[r]=\{1,\ldots,r\}$$ for $$r>0$$ and $$[0]=\varnothing$$. We prove the claim for nonnegative $$m,n$$ by induction on $$m+n$$. It is true when $$m+n=0$$. If exactly one of $$m,n$$ is zero, no bijection exists. Otherwise, let $$f:[m]\to[n]$$ be a bijection. Removing $$1$$ from $$[m]$$ and $$f(1)$$ from $$[n]$$ leaves a bijection between sets canonically in bijection with $$[m-1]$$ and $$[n-1]$$. The induction hypothesis gives $$m-1=n-1$$, hence $$m=n$$. Conversely, if $$m=n$$, the identity map is a bijection.

**(b)** An infinite system $$M$$ admits an injective map $$u:M\to M$$ that is not surjective. If $$M$$ were finite, there would be a bijection $$\varphi:[n]\to M$$ for some $$n$$. Then $$\varphi^{-1}\circ u\circ\varphi$$ would be an injective, non-surjective map from $$[n]$$ to itself, contradicting Exercise 1. Thus $$M$$ is infinite, and the definition gives $$\operatorname{Num}(M)=\infty$$.

### Exercise 3

Let $$N$$ be an $$n$$-element set and assume first that $$m\le n$$. Every bijection $$\sigma:[n]\to N$$ determines the $$m$$-element subset $$\sigma([m])$$. For a fixed $$m$$-element subset $$A\subseteq N$$, exactly $$m!(n-m)!$$ bijections determine $$A$$: choose independently a bijection from $$[m]$$ to $$A$$ and one from $$\{m+1,\ldots,n\}$$ to $$N\setminus A$$. Since there are $$n!$$ bijections in total, the number of such subsets is

$$
\frac{n!}{m!(n-m)!}=\binom{n}{m}.
$$

If $$m>n$$, there are no $$m$$-element subsets, and the defined value of $$\binom{n}{m}$$ is $$0$$.

### Exercise 4

Let $$m=\operatorname{Num}(M)$$ and $$n=\operatorname{Num}(N)$$. If $$m>n$$, an injective map would give an $$m$$-element subset of the $$n$$-element set $$N$$, which is impossible. If $$m\le n$$, label the elements of $$M$$ and $$N$$. The images of the $$m$$ elements of $$M$$ can be chosen successively in $$n,n-1,\ldots,n-m+1$$ ways. Hence the number of injective functions is

$$
n(n-1)\cdots(n-m+1)=\frac{n!}{(n-m)!}.
$$

For $$m=0$$ this product is empty and equals $$1$$, corresponding to the unique function from the empty set.

### Exercise 5

Form the tagged union

$$
D=\{(j,x):0\le j\le m,\ x\in X_j\}.
$$

Its number of elements is $$\sum_{j=0}^{m}\operatorname{Num}(X_j)$$. The map $$q:D\to X$$ given by $$q(j,x)=x$$ is surjective, so its image has no more elements than its finite domain. Therefore

$$
\operatorname{Num}(X)\le\sum_{j=0}^{m}\operatorname{Num}(X_j).
$$

If two distinct tagged pairs have the same image, $$q(D)=X$$ has at most one fewer elements than $$D$$. Thus equality holds exactly when $$q$$ is injective, which happens precisely when the sets $$X_0,\ldots,X_m$$ are pairwise disjoint.

### Exercise 6

For the disjoint union $$X=\bigsqcup_{j=0}^{m}X_j$$, the tagged union $$D$$ from Exercise 5 maps bijectively to $$X$$ by $$(j,x)\mapsto x$$. Counting the tagged copies gives

$$
\operatorname{Num}(X)=\sum_{j=0}^{m}\operatorname{Num}(X_j).
$$

### Exercise 7

If $$X$$ is countably infinite, a bijection from $$\mathbb N$$ to $$X$$ is already a surjection. If $$X$$ is finite and nonempty, list its elements and map all sufficiently large natural numbers to one fixed element; this also gives a surjection from $$\mathbb N$$ to $$X$$.

Conversely, suppose $$f:\mathbb N\to X$$ is surjective. Let

$$
A=\{n\in\mathbb N:f(n)\ne f(k)\text{ for every }k<n\}
$$

be the set of first occurrence indices. Distinct elements of $$A$$ have distinct images, and every element of $$X$$ occurs as $$f(n)$$ for some $$n\in A$$. If $$A$$ is finite, then $$X=f(A)$$ is finite. If $$A$$ is infinite, enumerate it increasingly as $$a_0<a_1<\cdots$$. Then $$j\mapsto f(a_j)$$ is a bijection from $$\mathbb N$$ to $$X$$. In either case, $$X$$ is countable.

### Exercise 8

If $$X$$ is finite, then its power set is finite, so its set of finite subsets is countable. Now suppose $$X$$ is countably infinite. For each $$n\in\mathbb N$$, let $$E_n(X)$$ be the set of subsets of $$X$$ with at most $$n$$ elements. The set $$X^n$$ is countable: after identifying $$X$$ with $$\mathbb N$$, finite powers of $$\mathbb N$$ can be enumerated by repeatedly listing pairs along diagonals. For $$n>0$$, the map

$$
X^n\to E_n(X),\qquad (x_1,\ldots,x_n)\mapsto\{x_1,\ldots,x_n\}
$$

is surjective, since a shorter list can be padded with repeated entries. Also $$E_0(X)=\{\varnothing\}$$. Thus each $$E_n(X)$$ is countable. The set of all finite subsets is $$\bigcup_{n\in\mathbb N}E_n(X)$$. Enumerating each $$E_n(X)$$ and then listing the pairs of indices $$(n,k)$$ along diagonals gives a surjection from $$\mathbb N$$ onto this union. By Exercise 7, the set of finite subsets of $$X$$ is countable.

### Exercise 9

Let $$F$$ be finite and choose a bijection $$\varphi:[n]\to F$$ (with the empty case immediate). For any subset $$A\subseteq F$$, its preimage $$\varphi^{-1}(A)$$ is a subset of the finite ordered set $$[n]$$, hence is finite. The restriction of $$\varphi$$ is a bijection from $$\varphi^{-1}(A)$$ to $$A$$, so $$A$$ is finite.
