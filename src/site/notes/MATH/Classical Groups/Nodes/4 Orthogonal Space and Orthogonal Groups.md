---
{"dg-publish":true,"draft":false,"permalink":"/MATH/Classical Groups/Nodes/4 Orthogonal Space and Orthogonal Groups/","dgPassFrontmatter":true}
---


# Orthogonal Space

## Classification of Symmetric Forms

Assume $(V,B)$ is an [[MATH/Classical Groups/Nodes/1 Sesquilinear Form#^6hwkgu\|orthogonal space]] and $\mathrm{char}F\neq 2$. There are two ways to classify symmetric forms.

> [!theorem]
> Suppose $(V,Q)$ is a non-degenerated orthogonal space and $B$ is the corresponding symmetric form. Then there exist $e_1,\cdots,e_n$ such that $(B(e_i,e_j))$ is $I_n$ or $\mathrm{diag}(1,\cdots,1,\alpha)$, where $\alpha\in F$ is a non-square element.

**Remark.** If there are $e_1,e_2$ satisfying $B(e_1,e_1)=B(e_2,e_2)=\alpha$ where $\alpha$ is non-square. By [[MATH/Classical Groups/Nodes/4 Orthogonal Space and Orthogonal Groups#^b21b58\|#^b21b58]], there exist $b,c\in F$ such that $\alpha^{-1}=b^2+c^2$. Let $e_1'=be_1+ce_2$ and $e_2'=ce_1-be_2$. Then $B(e_1',e_1')=B(e_2',e_2')=1$. 

> [!lemma]
> If $\mathrm{char}F\neq 2$, then for any $a\in F^\times$, there are $b,c\in F$ satisfying $b^2+c^2=a$.
{ #b21b58}


**_Proof._**
Let $S=\{b^2:b\in F\}$ and $T=\{a-c^2:c\in F\}$. Then $|S|=|T|=(q+1)/2$. Then $S\cap T\neq \emptyset$ and it yields the existence of $b,c$. 
<p align="left">□</p>

> [!theorem]
> If $\dim V\geq 3$, there is a isotropic vector $v$ and a hyperbolic plane $H$ containing $v$. Furthermore, suppose $(V,Q)$ is a non-degenerated orthogonal space and $\mathrm{char}F\neq 2$. Then $V$ can be written as
> 
> $$V=H_1\bot \cdots \bot H_m\bot V',$$
> 
> where $H_i$ is hyperplane, $V'$ does not contain isotropic vector and $\dim V'\leq 2$.
{ #171a94}


**Remark.** If $\dim V'=0$, $V$ is of plus type; if $\dim V'=2$, $V$ is of minus type. The definitions of plus type and minus type are as follows.

> [!definition]
> A form in $2m$ dimensions is defined to be of plus type if there is a totally isotropic subspace of dimension $m$, and of minus type otherwise. 

Note that:
- A straightforward calculation shows that the form which has an orthonormal basis is of minus type just if $q\equiv 3$ mod $4$ and $m$ is odd. 
- The maximal dimension of a totally isotropic subspace is often called the **Witt index** of the form. Thus the forms of plus type have Witt index $m$ while those of minus type have Witt index $m-1$.

## Universal Quadratic Form

> [!definition]
> A quadratic form $Q$ and its corresponding symmetric form $B$ are called *universal* if for any $a\in F^\times$ there is $v\in V$ such that $Q(v)=B(v,v)/2=a$.

> [!proposition]
> Suppose $(V,Q)$ is a non-degenerated orthogonal space. 
> - If $V$ contains an isotropic vector, then $Q$ is universal. 
> - If $V$ is a vector space over finite field and $\dim V\geq 2$, then $Q$ is universal.

# Orthogonal Groups

The general orthogonal group $\mathrm{GO}(V,f)$ is defined as the group of isometries of non-singular symmetric bilinear form $f$. Let $\alpha$ be a non-square element.

When $\dim V=2m+1$ is odd, by [[MATH/Classical Groups/Nodes/4 Orthogonal Space and Orthogonal Groups#^171a94\|#^171a94]], $V$ can be decomposed as $V=H_1\oplus\cdots\oplus H_m\oplus V'$, where $V'$ is congruent to $[1]$ or $[\alpha]$. Note that if $f$ is congruent to $I_n$, then $\alpha f$ is congruent to $\mathrm{diag}(1,\cdots,1,a)$ and vice versa. Moreover, we have $\mathrm{GO}(V,f)=\mathrm{GO}(V,\alpha f)$. So there is only one orthogonal group.

When $\dim V=2m$ is even, then $f$ is either of plus type or minus type. So there are two orthogonal groups. If $f$ is of plus type we write $\mathrm{GO}_{2m}^+(q)$ for $\mathrm{GO}(V,f)$, while if $f$ is of minus type we write $\mathrm{GO}_{2m}^-(q)$. 


有两个地方没说清楚：

- when dimension is even, $(1,0;0,\alpha)$ has no isotropic element. ——不一定对吧？
- 很有问题啊！这些都是特征奇的啊！
