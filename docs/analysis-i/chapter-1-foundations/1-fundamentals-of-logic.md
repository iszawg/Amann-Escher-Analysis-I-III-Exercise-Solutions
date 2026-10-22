# Chapter I — Foundations

## 1. Fundamentals of Logic

The first two exercises practice translating logical conditions into deductions and using a counting argument.

### Exercise 1

Let $H$ mean “Homer visits.” Define $M$, $B$, $L$, and $G$ analogously for Marge, Bart, Lisa, and Maggie. The conditions are

$$
H\Rightarrow M,\qquad G\lor L,\qquad M\oplus B,\qquad B\leftrightarrow L,\qquad G\Rightarrow(L\land H),
$$

where $\oplus$ means “exactly one of the two statements is true.”

Since $G\Rightarrow L$, the condition $G\lor L$ forces $L$: if Maggie visits then Lisa visits, and otherwise the disjunction itself gives Lisa. Thus Lisa visits. From $B\leftrightarrow L$, Bart visits as well.

Now $M\oplus B$, together with Bart’s visit, implies that Marge does not visit. Since $H\Rightarrow M$, Homer does not visit. Finally, $G\Rightarrow H$ implies that Maggie does not visit either.

Therefore **Bart and Lisa visit; Homer, Marge, and Maggie do not**.

### Exercise 2

Suppose the library has $n$ books, with distinct word counts $w_1,\ldots,w_n$, and let

$$
W=\sum_{i=1}^{n}w_i
$$

be the total number of words. The hypothesis says $W<n$.

If every book had at least one word, the $n$ distinct positive integer word counts would have sum at least

$$
1+2+\cdots+n=\frac{n(n+1)}{2}\ge n.
$$

That would give $W\ge n$, contradicting $W<n$. Hence at least one book has word count zero: **the library contains an empty book**.
