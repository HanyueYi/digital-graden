---
{"dg-publish":true,"draft":false,"permalink":"/MATH/Representations and Characters of Groups/Nodes/2 Group Algebra/","dgPassFrontmatter":true}
---


> [!definition] group algebra
> If the vector space $V$ over $F$ has a basis $\{g|g\in G\}$ and $\mathrm {dim} V=|G|$, we have a special $FG$-module: *group algebra*, which corresponds the "regular representation". 
> 
> The group algebra is denoted by $FG$, and $\{g|g\in G\}$ is called the *natural basis* of $FG.$

# Maschke's theorem

This theorem shows that $FG$ is completely reducible if $F=\mathbb{C}$ or $\mathbb{R}$.

> [!theorem] Maschke's theorem
> Let $G$ be a finite group, let $F$ be $\mathbb{R}$ or $\mathbb{C}$, and let $V$ be an FG-module. If $U$ is an FG-submodule of $V$, then there is an FG-submodule $W$ of $V$ such that$$V=U\oplus W.$$

**Remark.** The Maschke's theorem may fail, if one of the following holds.
- $G$ is an infinite group.
- The characteristic of $F$ is not $0$. See [[MATH/Cards/Nodes/Maschke's Theorem\|Maschke's theorem]] for more details.

# Schur's lemma

> [!theorem]
> Let $V$ and $W$ be irreducible $\mathbb CG$-modules. 
> - If $\theta: V\to W$ is a $\mathbb CG$-homomorphism, then either $\theta$ is a CG-isomorphism, or $v\theta=0$ for all $v\in V$.
> - If $\theta:V\to V$ is a $\mathbb CG$-isomorphism, then $\theta$ is a scalar multiple of the identity endomorphism $1_V$.
{ #po1qjp}


**_Proof._**
Since $V$ is irreducible and $\ker\theta\leqslant V$ is an submodule, we have that $\ker\theta=0\mbox{ or }V$. If $\ker\theta=V$, then $v\theta=0$ for all $v\in V$. Otherwise, when $\ker\theta=0$, $\theta$ is an isomorphism.

Now suppose that $V=W$. As $\theta$ is a linear transformation, it has at least one eigenvalue $\lambda$. Then $\theta-\lambda I$ is also a $\mathbb{C}G$-homomorphism and $\ker(\theta-\lambda I)=V$. It follows that $v\theta= \lambda v$.
<p align="left">□</p>

**Remark.** Note that $V$ should be a finite-dimensional vector space, otherwise the eigenvalue of $\theta$ may not exist.
 
## Applications of Schur's lemma

> [!proposition]
> Let $V$ be a FG-module. If every $FG$-homomorphism $\theta:V\to V$ is $\theta = \lambda I$, then $V$ is irreducible.

> [!corollary]
> Let $\rho:G\to \mathrm{GL}(n,\mathbb{C})$ be a representation of G. Then $\rho$ is irreducible if and only if every matrix A which satisfies $A(g\rho)=(g\rho)A$ for all $g\in G$ has the form $A=\lambda I_n$ with $\lambda\in \mathbb{C}$.

# Structure of Group Algebra $FG$

> [!warning]
> These conclusions hold only for $\mathbb CG$-module, as all of them need Maschke's theorem and Schur's lemma.
 
By Maschke's theorem, we know that $FG=U_1\oplus...\oplus U_r$ when $F=\mathbb{R}$ or $\mathbb C$, where $U_i$ are irreducible FG-submodules.

## Abelian Group

Let $G$ be an abelian group and $V$ be the group algebra $FG$. Note that for any $x\in G$, $\theta_x:v\mapsto vx$ is an $FG$-homomorphism, as $vxg=vgx$ for all $v\in V$ and $g\in G$. 

For any irreducible submodule $W\subseteq V$, there exists a $\lambda_W$ such that $\theta_x|_{W}:v\mapsto\lambda_Wv$ by [[MATH/Cards/Nodes/Schur's Lemma\|Schur's lemma]]. It follows that $W=\left\langle v\right\rangle$ is a submodule of $V$. Therefore, each irreducible submodule of $FG$ is of dimension $1$. In the other word, suppose $\rho$ is the regular representation, then there exists a basis such that $\rho(x)$ is a diagonal matrix, as the following proposition shows.

> [!proposition]
> Let $G$ be a finite group, and let $V$ be a $\mathbb CG$-module. Then there is a basis $\mathcal B$ such that $[g]_{\mathcal B}$ is diagonal and the entries on the diagonal of $[g]_{\mathcal B}$ are nth roots of unity, where n is the order of $g$.

**Remark.** This proposition shows that every representation of a element of a finite group is diagonalizable. We can use it to prove that "$A$ is diagonalizable if $A^n=I$ for some $n$".

By the fundamental theorem of abelian group, the abelian group $G$ can be written as $G=C_{n_1}\times...\times C_{n_r}$. Then there are $n$ irreducible $\mathbb{C}G$-modules, whose corresponding representation $\rho_{\lambda_1\cdots\lambda_r}$ is defined as $g_i\rho=(\lambda_i)$ for any generator $g_i$ of $C_{n_i}$, where

$$n=|\{\lambda=\Pi_{i=1}^r\lambda_i:\lambda_i^{n_i}=1\}|=|G|.$$

So we get the following theorem.

> [!theorem]
> Let $G$ be the abelian group $C_{n_1}\times\cdots\times C_{n_r}$. The representations $\rho_{\lambda_1\cdots\lambda_r}$ of $G$ constructed above are irreducible and have degree $1$. There are $|G|$ of these representations, and every irreducible representation of $G$ over $\mathbb{C}$ is equivalent to precisely one of them.

Furthermore, the converse argument is also true.

> [!proposition]
> Suppose that $G$ is a finite group such that every irreducible $\mathbb CG$-module has dimension 1. Then $G$ is abelian.

## Non-abelian Group

By [[MATH/Cards/Nodes/Maschke's Theorem\|Maschke's theorem]], We know that $FG=U_1\oplus...\oplus U_s$ where $U_i$ are irreducible $FG$-submodule.

Now consider the number of $j$ such that $U_i\cong U_j$ for a fixed $U_i$, and denote the number as $d_i$. By [[MATH/Cards/Nodes/Schur's Lemma\|Schur's lemma]], there is $d_i=\mathrm{dim}(\mathrm{Hom}_{\mathbb{C}G}(U_i,\mathbb CG))$, because
- $\dim(\mathrm{Hom}_{\mathbb{C}G}(U_i,U_j))=1$ if $U_i\cong U_j$, and
- $\dim(\mathrm{Hom}_{\mathbb{C}G}(U_i,U_j))=0$ if $U_i\not\cong U_j$.

Furthermore, there is

$$\begin{aligned}
\mathrm{dim}(\mathrm{Hom}_{\mathbb{C}G}(U_i,\mathbb CG))&=\sum_{j=1}^s\dim(\mathrm{Hom}_{\mathbb{C}G}(U_i,U_j))\\
&=\sum_{j=1}^s\dim(\mathrm{Hom}_{\mathbb{C}G}(U_j,U_i))\\
&=\mathrm{dim}(\mathrm{Hom}_{\mathbb{C}G}(\mathbb CG,U_i))
\end{aligned}$$

and so we have that $d_i=\mathrm{dim}(\mathrm{Hom}_{\mathbb{C}G}(\mathbb CG,U_i))$.

Suppose that $u_1,\cdots,u_d$ is a set of basis of $U_i$. Define $\varphi_i:\mathbb{C}G\to U_i$ by $r\mapsto u_ir$. For any $\varphi\in\mathrm{Hom}_{\mathbb{C}G}(\mathbb{C}G,U_i)$, $1\varphi=\lambda_1u_1+\cdots+\lambda_du_d$, then $r\varphi=(1\varphi)r=r(\lambda_1u_1+\cdots+\lambda_du_d)$ and so $\varphi=\lambda_1\varphi_1+\cdots+\lambda_d\varphi_d$. Then we have

$$\mathrm{dim}(\mathrm{Hom}_{\mathbb{C}G}(\mathbb CG,U_i))=\mathrm{span}(\varphi_1,...,\varphi_s)=\mathrm{dim}U_i,$$

and get the following theorem.

> [!theorem]
> Suppose that $\mathbb{C}G=U_1\oplus\cdots\oplus U_r$ a direct sum of irreducible $\mathbb{C}G$-submodule. If $U$ is any irreducible $\mathbb{C}G$-module, then the number of $\mathbb{C}G$-module $U_i$ with $U_i\cong U$ is equal to $\dim U$.
> 
> In particular, let $V_1,\cdots,V_k$ form a complete set of non-isomorphic irreducible $\mathbb{C}G$-modules. Then $\sum_{i=1}^k(\dim V_i)^2=|G|$.

## Center of $FG$

Define the center of $\mathbb CG$ as

$$Z(\mathbb CG)=\{z\in\mathbb CG :zr=rz,\forall r\in \mathbb CG\}.$$

Each element of $Z(\mathbb CG)$ is a sum of elements of some conjugate classes. Notice that $Z(\mathbb CG)$ is a subspace of $\mathbb CG$, so $\mathrm{dim}Z(\mathbb CG)=\#$conjugate classes of $G$.

For any $r\in Z(\mathbb CG)$, $vrg=vgr$ and $\theta:v\to vr$ is a $\mathbb CG$-homomorphism. If $\theta:V\to V$ for an irreducible $\mathbb CG$-submodule, then $vr=\lambda v$. Similarly, for an element $z\in Z(G)$, $\theta:v\to vz$ is also a $\mathbb CG$-homomorphism. Then we get a proposition as follows.

> [!proposition]
> If there exists a faithful irreducible $\mathbb CG$-module $V$, then $Z(G)$ is cyclic.

**_Proof._**
For any $z\in Z(G)$,

$$\theta:V\to V,\;
v\mapsto vz$$

is a $\mathbb CG$-homomorphism and $vz=\lambda_zv$ by [[MATH/Cards/Nodes/Schur's Lemma\|Schur's lemma]]. Since $V$ is faithful, we have that $\lambda_x\neq\lambda_y$ if $x\neq y$. Otherwise, there exists $1\neq xy^{-1}\in Z(G)$ such that $v(xy^{-1})=\lambda_x\lambda_y^{-1}v=v$ for all $v\in V$. Thus, $Z(G)$ is a subgroup of $\mathbb C^{*}$ and so it is cyclic.
<p align="left">□</p>

