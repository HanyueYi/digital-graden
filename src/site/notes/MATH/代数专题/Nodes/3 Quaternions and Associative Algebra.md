---
{"dg-publish":true,"permalink":"/MATH/代数专题/Nodes/3 Quaternions and Associative Algebra/","dgPassFrontmatter":true}
---


# Representation of Quaternion Group

$\mathbb H=\mathbb{C}+\mathbb{C} j=\{\alpha+\beta i+\gamma j+\delta k:\alpha,\beta,\gamma,\delta\in\mathbb{R}\}$ is a space $2$-dimensional over $\mathbb{C}$ and $4$-dimensional over $\mathbb{R}$. 

Quaternion group is $Q=\{\pm1,\pm i,\pm j,\pm k\}$ where $ijk=i^2=j^2=k^2=-1$ and $i^2=-1$. Equivalently, $Q=\left\langle x,y:x^4=1,x^2=y^2,x^y=x^{-1}\right\rangle$. 

Consider the representation $\rho:H\to\mathbb{C}^*$. Note that $iji^{-1}j^{-1}=-1$, we have that $\rho(-1)=\rho(i)\rho(j)(\rho(i))^{-1}(\rho(j))^{-1}=1$. Since $\rho(i)^2=\rho(i^2)=1=\rho(j)^2=\rho(k)^2$, we have that $\{\rho(i),\rho(j)\}\in\{\pm1\}$ and $\rho(k)=\rho(i)\rho(j)$. So there are $4$ one-dimensional representations and $|Q|=1^2\cdot 4+2^2\cdot 1$.  

Note that $Z(Q)=\{1,-1\}$, then $Q/Z(Q)=C_2\times C_2$. Define $q:Q\to Q/Z(Q)$ and $\rho:C_2\times C_2\to\mathbb{C}^*$. Then $q\circ \rho:Q\to \mathbb{C}^*$ is one-dimensional representation of $Q$. 

To get two dimensional representation of $H$, consider space of quaternions $\mathbb H=\mathbb{C}+\mathbb{C}j=\{(a+bi)+(c+di)j:a,b,c,d\in \mathbb{R}\}$. Since $\mathbb H$ is a $Q$-module where $\mathbb H$ is a $2$-dimensional vector space over $\mathbb{C}$, the we have the following matrices (also see [Pauli matrices](https://en.wikipedia.org/wiki/Pauli_matrices))
{ #jfs683}


$$1\mapsto\left[ \begin{matrix} 1 & 0 \\ 0 & 1  \end{matrix} \right],i\mapsto\left[ \begin{matrix} i &  \\  & -i  \end{matrix} \right],j\mapsto \left[ \begin{matrix} & 1 \\ -1 &   \end{matrix} \right],k\mapsto \left[ \begin{matrix}  & i \\ i &   \end{matrix} \right].$$

# Representation of Associative Algebra

> [!definition]
> Associative algebra is vector space over $k$ with binary bilinear operation $A\times A\to A,(a,b)\mapsto ab$. Representation of $A$ is a homomorphism $\rho:A\to\mathrm{End}_k(V)$ satisfying $\rho(ab)=\rho(a)\rho(b)$. 

**Examples.** 
- $V=0$, then any $A\to\mathrm{End}_k(V)$ is a trivial representation.
- For an associative algebra $A$ and $V=A$, $\rho:A\to\mathrm{End}_k(A),\rho(a)b:=ab$ is a regular representation of $A$.
- For a group $G$, we get a group algebra $kG$ which can be seen as a vector space. Then $\rho:G\to \mathrm{End}_k(kG)$ is a representation.
- Direct sum of two representation or two $A$-modules: Let $V$ and $W$ be two $A$-module. Define $a(v\oplus w)=av\oplus aw$. Note that this representation is composable.

> [!definition]
> Non-zero representation $V$ is called *indecomposable* if it is not isomorphic to a direct sum of two non-zero representations.
{ #ahq6o8}


**Remark.** There exists $A$-module which is indecomposable but not irreducible. For example, let $A=\{\left[ \begin{matrix} a & b \\  & c  \end{matrix} \right]:a,b,c\in k\}$. Then ${(x,0):x\in k}$ is a submodule, but $V$ is indecomposable.

> [!definition]
> Let $V$ and $W$ be two $A$-modules, and let $T:V\to W$ be a linear transformation. If the following diagram 
> 
> $$\require{AMScd}\begin{CD}  V @>T>> W\\ @V \rho(a) V V @VV \sigma(a) V\\ V @>>T> W \end{CD}$$
> 
> for all $a\in A$, then $T$ is a homomorphism of $A$-modules $V$ and $W$.

**Example.** $k=\mathbb{R}$, $A=V=\mathbb{C}$. Then $\varphi:\mathbb{C}\to\mathbb{C},a+ib\mapsto a-ib$ is a field automorphism but not homomorphism of modules.

> [!lemma] Schur lemma
> Let $V,W$ be two irreducible $A$-modules. If $\varphi:V\to W$ is a homomorphism, then either $\varphi =0$ or $\varphi$ is an isomorphism. If $k$ is algebraically closed and $V$ is finite-dimensional irreducible, then for any $\varphi:V\to V$ there is $\lambda\in k$ such that $\varphi=\lambda\mathrm{Id}$. 

**Examples.**
- If $A$ is a commutative algebra and $\rho:A\to V$ is a representation, then $\rho(a):V\to V$ is a homomorphism by $\rho(a)\rho(b)=\rho(b)\rho(a)$ for any $b\in A$. Then by Schur lemma, $\rho(a)=\lambda\mathrm{id}$ and each irreducible module has dimension $1$. Therefore, if $A=\mathbb{C}$, then the only irreducible module is $V=\mathbb{C}$ and the only indecomposable module is $V=\mathbb{C}$. 
- Let $A=\mathbb{C}[x]$. Define $\rho:A\to \mathbb{C},x\mapsto\alpha$. Then for any polynomial $p(x)$, we have $\rho(p(x))=\rho(\alpha)$. It is a one-dimensional representation of $A$. 
- If $\rho:A\to \mathrm M_n(\mathbb{C})$ is indecomposable, then in dimension $n$ and $x\in A$ we have $x\mapsto\left[ \begin{matrix} \lambda &  1 &\\  & \ddots &  1 \\ &  &\lambda\end{matrix} \right]$. 
