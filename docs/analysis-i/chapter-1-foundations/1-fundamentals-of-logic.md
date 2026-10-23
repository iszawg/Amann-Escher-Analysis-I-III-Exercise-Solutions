# Chapter I — Foundations

## 1. Fundamentals of Logic

The first two exercises practice translating logical conditions into deductions and using a counting argument.

### Exercise 1

Use these propositions:

$$
\begin{aligned}
H &:\text{ Homer visits},\\
M &:\text{ Marge visits},\\
B &:\text{ Bart visits},\\
L &:\text{ Lisa visits},\\
G &:\text{ Maggie visits}.
\end{aligned}
$$

The conditions translate to:

$$
\begin{aligned}
H &\Rightarrow M,\\
G &\lor L,\\
M &\oplus B,\\
B &\leftrightarrow L,\\
G &\Rightarrow (L\land H).
\end{aligned}
$$

The third condition says exactly one of Marge and Bart visits. The fourth says Bart and Lisa either both visit or both stay away.

The two conditions involving Maggie and Lisa imply $$L$$: if $$L$$ were false, then $$G\lor L$$ would force $$G$$, and $$G\Rightarrow(L\land H)$$ would force $$L$$, a contradiction. Since $$B\leftrightarrow L$$, Lisa's visit also forces Bart to visit.

Now $$M\oplus B$$ says exactly one of Marge and Bart visits. Since $$B$$ is true, $$M$$ is false. The implication $$H\Rightarrow M$$ then rules out $$H$$. Finally, $$G\Rightarrow(L\land H)$$ together with the fact that $$H$$ is false rules out $$G$$.

Therefore **Bart and Lisa visit; Homer, Marge, and Maggie do not**.

### Exercise 2

Let the library have a finite number of books, each with a distinct word count. Use this notation:

$$
\begin{aligned}
n&=\text{number of books},\\
w_i&=\text{word count of book }i,\\
W&=\sum_{i=1}^{n}w_i<n.
\end{aligned}
$$

By hypothesis, the total number of words is less than the number of books. The distinct word counts cannot all be positive: if they were, their sum would be at least

$$
1+2+\cdots+n=\frac{n(n+1)}{2}\ge n.
$$

This would mean at least as many words as books, contradicting the hypothesis. Hence one book has word count zero: **the library contains an empty book**.
