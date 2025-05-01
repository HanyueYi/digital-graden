---
{"dg-publish":true,"draft":false,"permalink":"/MATH/Cards/Nodes/Separable Extension is Transitive/","dgPassFrontmatter":true}
---


> [!proposition]
> If $K / E, E / F$ are separable field extensions, then $K / F$ is separable.

**_Proof._** This proof comes from [here](https://math.stackexchange.com/questions/154765/k-e-e-f-are-separable-field-extensions-implies-k-f-is-separable). 

When the characteristic is $0$, $K/F$ is algebraic and so is separable. Now we assume that all fields are of characteristic $p$. 

Let $S$ be the set of all elements of $K$ that are separable over $F$. Then $E \subseteq S$ as $E / F$ is separable. Note that $S$ is a subfield of $K$ by [[MATH/Cards/Nodes/Separable Extension is Transitive#^1104cb\|#^1104cb]].

We claim that $K$ is purely inseparable over $S$. To show it, it suffices to show for any $u\in K$, there exists $n$ such that $u^{p^n}\in S$. For any $u\in K$, if $u\in S$, then $u^{p^0}\in S$ is trivial. Otherwise, $u\in K\setminus S$. If $u^p\in S$, we have done. If $u^p\notin S$, then $g=\mathrm{Irr}(u^p,S)$ and $f(x):=g(x^p)$ has a root $u$. Therefore, the degree of $\mathrm{Irr}(u^p,K)$ is less than $\mathrm{Irr}(u,K)$. Repeat this procedure, there exists $n$ such that $u^{p^{n-1}}$ is inseparable and $u^{p^{n}}$ is separable. Therefore, $u^{p^n}\in S$ and the minimal polynomial of $u$ over $S$ is a divisor of $x^{p^n}-u^{p^n}=(x-u)^{p^n}$, so $K$ is purely inseparable over $S$.

But since $E \subseteq S \subseteq K$ and $K$ is separable over $E$, then it is separable over $S$. So $K$ is both purely inseparable and separable over $S$. This can only occur if $S=K$, hence every element of $K$ is separable over $F$.
<p align="left">□</p>


> [!lemma]
> Let $K$ be an extension of $F$, and $X$ a subset of $F$ such that $K=F(X)$. If every element of $X$ is separable over $F$, then $K$ is a separable extension of $F$.
{ #1104cb}


**_Proof._**
Let $v \in K$. Then there exist $u_1, \ldots, u_n \in X$ such that $v \in F\left(u_1, \ldots, u_n\right)$. Let $f_i(x) \in F[x]$ be the irreducible polynomial of $u_i$ over $F$; by assumption, $f_i(x)$ is separable. Let $E$ be a splitting field over $F\left(u_1, \ldots, u_n\right)$ of $f_1(x), \ldots, f_n(x)$. Then $E$ is also a splitting field of $f_1, \ldots, f_n$ over $F$, and since the $f_i$ are separable, $E$ is separable over $F$. Therefore, since $v \in F\left(u_1, \ldots, u_n\right) \subseteq E$, it follows that $v$ is separable over $F$.
<p align="left">□</p>
