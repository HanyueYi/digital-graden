---
{"dg-publish":true,"permalink":"/MATH/代数几何/Nodes/dimension of affine variety/","dgPassFrontmatter":true}
---


> [!definition]
> If $X$ is a topological space, we define the dimension of $X$ (denoted $\operatorname{dim} X$ ) to be the supremum of all integers $n$ such that there exists a chain $Z_0 \subset Z_1 \subset \ldots \subset Z_n$ of distinct irreducible closed subsets of $X$. 
> 
> We define the dimension of an affine or quasi-affine variety to be its dimension as a topological space.

**Example.** The dimension of $\mathbf{A}^1$ is $1$. Indeed, the only irreducible closed subsets of $\mathbf{A}^1$ are the whole space and single points.

> [!definition]
> In a ring $A$, the height of a prime ideal $\mathfrak{p}$ is the supremum of all integers $n$ such that there exists a chain $\mathfrak{p}_0 \subset \mathfrak{p}_1 \subset \ldots \subset \mathfrak{p}_n=\mathfrak{p}$ of distinct prime ideals. We define the dimension (or Krull dimension) of $A$ to be the supremum of the heights of all prime ideals.


> [!proposition]
> If $Y$ is an affine algebraic set, then the dimension of $Y$ is equal to the dimension of its affine coordinate ring $A(Y)$.

**_Proof._**
If $Y$ is an affine algebraic set in $\mathbf{A}^n$, then the closed irreducible subsets of $Y$ correspond to prime ideals of $A=k\left[x_1, \ldots, x_n\right]$ containing $I(Y)$. These in turn correspond to prime ideals of $A(Y)$. Hence $\operatorname{dim} Y$ is the length of the longest chain of prime ideals in $A(Y)$, which is its dimension.