# Chapter III — Continuous Functions

## 4. Connectivity

### Exercise 1

Give $$\{0,1\}$$ the discrete topology.

If $$X$$ is disconnected, write $$X=O_0\cup O_1$$ as a union of disjoint nonempty open sets. The characteristic map $$f:X\to\{0,1\}$$ defined by $$f(x)=j$$ for $$x\in O_j$$ is continuous and surjective, since $$f^{-1}(\{j\})=O_j$$ is open for each $$j\in\{0,1\}$$.

Conversely, if a continuous surjection $$f:X\to\{0,1\}$$ exists, then $$f^{-1}(\{0\})$$ and $$f^{-1}(\{1\})$$ are disjoint, nonempty open sets whose union is $$X$$. Thus $$X$$ is disconnected. This proves the equivalence.

### Exercise 2

Set $$C=\bigcup_{\alpha\in A}C_\alpha$$. Suppose, for a contradiction, that $$C$$ is disconnected. By Exercise 1 there is a continuous surjection $$f:C\to\{0,1\}$$. Each restriction $$f|_{C_\alpha}$$ is continuous. Since $$C_\alpha$$ is connected, its image is connected, so $$f(C_\alpha)$$ is a singleton. Thus $$f$$ is constant on each $$C_\alpha$$.

For every pair $$\alpha,\beta$$, choose a point of $$C_\alpha\cap C_\beta$$. The two constants must agree at that point, so they are equal. Hence $$f$$ is constant on all of $$C$$, contradicting surjectivity. Therefore $$C$$ is connected.

### Exercise 3

In $$\mathbb R^2$$, take the two unit circles

$$
A=\{(x,y):x^2+y^2=1\},\qquad B=\{(x,y):(x-1)^2+y^2=1\}.
$$

Each circle is path connected, hence connected. Their intersection consists of the two points $$\left(\frac12,\frac{\sqrt3}{2}\right)$$ and $$\left(\frac12,-\frac{\sqrt3}{2}\right)$$. A two-point space with its subspace metric is disconnected, so an intersection of connected sets need not be connected.

### Exercise 4

Assume first that $$X$$ and $$Y$$ are nonempty and connected. Fix $$x_0\in X$$. For each $$y\in Y$$, let

$$
C_y=(X\times\{y\})\cup(\{x_0\}\times Y).
$$

The two sets in this union are connected and meet at $$(x_0,y)$$, so $$C_y$$ is connected. Also, any two sets $$C_y$$ and $$C_{y'}$$ meet along the nonempty set $$\{x_0\}\times Y$$. By Exercise 2, their union is connected. Since $$\bigcup_{y\in Y}C_y=X\times Y$$, the product is connected.

Induction gives the same result for any finite product of nonempty connected metric spaces. Conversely, if $$X_1\times\cdots\times X_n$$ is connected and every factor is nonempty, each coordinate projection is a continuous surjection onto $$X_j$$. Its image $$X_j$$ is therefore connected.

Thus the claimed equivalence holds when all factors are nonempty. If empty spaces are allowed, as in this book's convention that the empty space is connected, the reverse implication needs that qualification: a product with an empty factor is empty and connected even if another factor is disconnected.

### Exercise 5

Let $$A$$ be connected in $$X$$. Suppose that its closure $$\overline A$$ is disconnected, and write $$\overline A=U\cup V$$ as a disjoint union of nonempty sets open in $$\overline A$$. Since $$A$$ is dense in $$\overline A$$, each nonempty relatively open set in $$\overline A$$ meets $$A$$. Therefore $$A\cap U$$ and $$A\cap V$$ are nonempty, disjoint, relatively open subsets of $$A$$ whose union is $$A$$. This contradicts the connectedness of $$A$$. Hence $$\overline A$$ is connected.

### Exercise 6

For each $$x\in X$$, the singleton $$\{x\}$$ is connected, so it belongs to the family whose union defines $$K(x)$$. All the connected sets in that family contain $$x$$; by Exercise 2 their union $$K(x)$$ is connected. By definition, every connected subset of $$X$$ containing $$x$$ is contained in $$K(x)$$.

**(a)** Suppose $$K(x)\cap K(y)\ne\varnothing$$. Both components are connected, so Exercise 2 shows that $$K(x)\cup K(y)$$ is connected. It contains both $$x$$ and $$y$$. The maximality just proved implies that this union is contained in each of $$K(x)$$ and $$K(y)$$. Hence $$K(x)=K(y)$$. Every point belongs to its own component, so the components cover $$X$$; the equality property shows that distinct components are disjoint. Thus they form a partition.

**(b)** By Exercise 5, $$\overline{K(x)}$$ is connected. It contains $$x$$, so maximality gives $$\overline{K(x)}\subseteq K(x)$$. The reverse inclusion always holds, and consequently $$K(x)=\overline{K(x)}$$ is closed.

### Exercise 7

By Theorem 4.4, every connected subset of $$\mathbb R$$ is an interval. If an interval contained two distinct rational numbers, it would contain every real number between them, including irrational numbers. Thus every connected subset of $$\mathbb Q$$ is either empty or a singleton. Each singleton $$\{q\}$$ is connected, so the connected components of $$\mathbb Q$$ are exactly $$\{q\}$$ for $$q\in\mathbb Q$$.

### Exercise 8

First show that $$E\setminus\{0\}$$ is path connected. For nonzero $$x,y\in E$$, the segment from $$x$$ to $$y$$ avoids the origin unless $$y=-c x$$ for some $$c>0$$. In that exceptional case, choose $$z\notin\operatorname{span}\{x\}$$, which is possible because $$\dim E\ge2$$. Neither segment from $$x$$ to $$z$$ nor from $$z$$ to $$y$$ contains the origin, so the two segments give a path in $$E\setminus\{0\}$$ from $$x$$ to $$y$$. Therefore $$E\setminus\{0\}$$ is connected.

The map $$r:E\setminus\{0\}\to S$$ given by $$r(x)=x/\|x\|$$ is continuous and surjective. A continuous image of a connected space is connected, so the unit sphere $$S$$ is connected as well.

### Exercise 9

Homeomorphisms preserve connectedness after deleting corresponding points.

**(a)** Choose $$p\in S^1$$ whose image under a hypothetical homeomorphism $$h:S^1\to[0,1]$$ is $$1/2$$. The punctured circle $$S^1\setminus\{p\}$$ is connected (it is homeomorphic to $$\mathbb R$$), whereas $$[0,1]\setminus\{1/2\}$$ is disconnected. This is a contradiction.

**(b)** Removing any point disconnects $$\mathbb R$$. In contrast, $$\mathbb R^n\setminus\{p\}$$ is path connected for $$n\ge2$$: two points can be joined by a segment unless that segment passes through $$p$$, in which case an intermediate point off the line through them gives a two-segment path avoiding $$p$$. A homeomorphism would preserve the connectedness of these punctured spaces, which is impossible.

**(c)** Removing any point from $$X=(0,1)\cup(2,3)$$ leaves exactly three connected components: the interval containing the removed point splits into two intervals, and the other interval remains intact. But removing the endpoint $$3$$ from $$Y=(0,1)\cup(2,3]$$ leaves exactly two connected components, namely $$ (0,1)$$ and $$ (2,3)$$. If a homeomorphism $$h:X\to Y$$ existed, deleting $$h^{-1}(3)$$ from $$X$$ would have to give a space homeomorphic to $$Y\setminus\{3\}$$, contradicting the different numbers of connected components.

### Exercise 10

For $$n\ge1$$, the determinant is a continuous map $$\det:O(n)\to\{-1,1\}$$, since it is a polynomial in the matrix entries and every orthogonal matrix has determinant $$1$$ or $$-1$$. It is surjective: $$I_n$$ has determinant $$1$$, while $$\operatorname{diag}(-1,1,\ldots,1)$$ has determinant $$-1$$. The discrete two-point space $$\{-1,1\}$$ is disconnected. If $$O(n)$$ were connected, its continuous image would be connected, a contradiction. Hence $$O(n)$$ is not connected.

### Exercise 11

Set $$q(x)=B(x,x)$$. This is a continuous function and satisfies $$q(tx)=t^2q(x)$$ for every real $$t$$.

**(a)** If $$q(x)=0$$ for some nonzero $$x$$, then $$x/|x|\in S^{n-1}$$ and homogeneity gives $$q(x/|x|)=0$$. Otherwise, because $$B$$ is neither positive nor negative definite, there are nonzero vectors where $$q$$ has opposite signs. After normalizing, these give points on the unit sphere where $$q$$ has opposite signs. For $$n\ge2$$ the sphere is path connected, so the intermediate value theorem applied along a path between these points gives a point $$u\in S^{n-1}$$ with $$q(u)=0$$. If $$n=1$$, then $$q(x)=b x^2$$ for some $$b\in\mathbb R$$; being neither positive nor negative definite forces $$b=0$$, and either point of $$S^0$$ has value zero.

**(b)** The restriction of $$q$$ to the compact unit sphere $$S^{n-1}$$ attains a minimum $$\beta$$. Positive definiteness implies $$q(u)>0$$ at every point of that sphere, so $$\beta>0$$. For $$x\ne0$$, homogeneity yields

$$
B(x,x)=|x|^2q\!\left(\frac{x}{|x|}\right)\ge\beta|x|^2.
$$

The inequality also holds for $$x=0$$.

### Exercise 12

**(a)** Let $$\{C_\lambda\}_{\lambda\in\Lambda}$$ be a family of convex subsets of $$E$$. If $$x,y\in\bigcap_{\lambda\in\Lambda}C_\lambda$$ and $$t\in[0,1]$$, then $$(1-t)x+ty$$ belongs to every $$C_\lambda$$, hence to their intersection. The empty intersection is $$E$$, which is convex as well.

**(b)** If $$M$$ is convex, closure under convex combinations of two points extends to any finite number of points by induction. Indeed, for weights $$\alpha_j\ge0$$ summing to $$1$$, if $$\alpha_n<1$$, write

$$
\sum_{j=1}^n\alpha_jx_j=(1-\alpha_n)\left(\sum_{j=1}^{n-1}\frac{\alpha_j}{1-\alpha_n}x_j\right)+\alpha_nx_n.
$$

The expression in parentheses is a convex combination of the first $$n-1$$ points; if $$\alpha_n=1$$, the sum is just $$x_n$$. Conversely, closure under all finite convex combinations includes the two-point combinations $$(1-t)x+ty$$, which is precisely convexity.

**(c)** Suppose $$x,y\in\mathring M$$. Choose $$r>0$$ such that $$B(x,r)\subseteq M$$ and $$B(y,r)\subseteq M$$. For any $$t\in[0,1]$$ and $$h\in E$$ with $$\|h\|<r$$, both $$x+h$$ and $$y+h$$ belong to $$M$$. Convexity gives

$$
(1-t)x+ty+h=(1-t)(x+h)+t(y+h)\in M.
$$

Thus the ball of radius $$r$$ about $$(1-t)x+ty$$ lies in $$M$$, proving that $$\mathring M$$ is convex.

Now let $$x,y\in\overline M$$. Choose sequences $$x_k,y_k\in M$$ with $$x_k\to x$$ and $$y_k\to y$$. For each $$t\in[0,1]$$, convexity gives $$(1-t)x_k+ty_k\in M$$, and these points converge to $$(1-t)x+ty$$. Therefore $$(1-t)x+ty\in\overline M$$, so $$\overline M$$ is convex.
