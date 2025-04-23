---
{"dg-publish":true,"permalink":"/MATH/代数专题/Nodes/1 Schur Lemma/","dgPassFrontmatter":true}
---


- Iryna Kashuba SICM room 218
- office hour: odd week 12:00-14:00, even week 14:00-16:00
- exercises 20% + midterm 35% (8th week Monday) + final exam 45% (17th week)

> [!definition]
> A *representation* of group $G$ is a mapping $\rho:G\to\mathrm{End}_kV$ which satisfies the following properties
> - for any $g_1$, $g_2\in G$, $\rho(g_1g_2)=\rho(g_1)\rho(g_2)$,
> - $\rho(e)=\mathrm{Id}$ where $\mathrm{Id}:V\to V,v\mapsto v$,
> 
> where $k$ is a field and $\mathrm{End}_kV$ is the set of linear transformation on $V$. 
> 
> In other words, representation of $G$ on $V$ is a homomorphism $\rho:G\to\mathrm{GL}(V)$. Also we call $V$ a $G$-module. 

> [!definition]
> Let $V$ and $W$ be two $G$-modules, and let $\rho$ and $\sigma$ be representations in $V$ and $W$, respectively. A *map* between two $G$-modules is a linear transformation $T:V\to W$ such that for any $g\in G$ the diagram 
> 
> $$\require{AMScd}\begin{CD}V @>T>> W\\    @V \rho(g) V V @VV \sigma(g) V\\    V @>>T> W \end{CD}$$
> 
> is commutative. That is, $\sigma(g)\circ T=T\circ \rho(g)$ for all $g\in G$. If $T$ is invertible, we say that $\rho$ and $\sigma$ are isomorphic or equivalent.
{ #7wc4nf}


> [!definition] dual representation
> Suppose $V$ is a $G$-module. Let $V^*=\mathrm{Hom}_k(V,k)$, and let $\rho^*$ is a representation of $G$ on $V^*$. For any $f\in\mathrm{Hom}_k(V,k)$, define $\rho^*(g)f=f\circ\rho(g^{-1})$. Then $\rho^*$ is a representation of $G$ in $V^*$.

**_Proof._**
See [[MATH/代数专题/Nodes/List 1#^rkzacd\|here]].
<p align="left">□</p>


> [!definition]
> We call a $G$-module $V$ irreducible, if $V$ and $\{0\}$ are only $G$-invariant subspaces.

For example, let $G=S_n$ and $\sigma:G\to\mathrm{GL}_n(k),\sum\alpha_ie_i\mapsto \sum\alpha_i e_{\sigma(i)}$. Then $D:=\{(\alpha,\cdots,\alpha):\alpha\in k\}$ and $W:=\{(\alpha_1,\cdots,\alpha_n):\sum\alpha_i=0\}$ are two $G$-invariant subspaces, and $V=D\oplus W$. 

> [!lemma] Schur lemma
> A morphism between irreducible representations of groups is either zero or isomorphism.
> 
> If $k$ is algebraically closed field, $\rho$ is a irreducible representation of $G$ in $V$, $\dim V<\infty$ and $S:V\to V$ morphism of $G$-modules, then there exists $\lambda\in k$ such that $S=\lambda\mathrm{Id}$. 

**_Proof._**
i) Let $T:V\to W$ be a morphism with $V,W$ irreducible. Since $\ker T$ and $\mathrm{Im}T$ are submodules of $V$ and $W$, respectively, then one of the following holds:
- $\ker T=V$, $\mathrm{Im}T=0$
- $\ker T=0$, $\mathrm{Im}T=W$

Thus either $T$ is zero or isomorphism.

ii) Let $\lambda$ be a root of the characteristic polynomial $p_S(\lambda)$. Then $\ker(S-\lambda I)\neq\{0\}$ and $S-\lambda I$ is also a morphism. By i) we have that $\ker(S-\lambda I)=V$. Therefore, $S=\lambda I$. 
<p align="left">□</p>

> [!lemma]
> Any irreducible representation of finite group is of finite dimension.

**_Proof._**
Let $V$ be a irreducible representation of $G$. For any nonzero $v\in V$, define $W:=\left\langle v\right\rangle=\{gv:g\in G\}$. Then $\dim W<\infty$ by $|G|<\infty$. Since $W$ is $G$-invariant, we have that $W=V$ and so $V$ is of finite dimension.
<p align="left">□</p>

