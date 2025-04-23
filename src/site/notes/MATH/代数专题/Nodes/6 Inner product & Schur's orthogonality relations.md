---
{"dg-publish":true,"permalink":"/MATH/代数专题/Nodes/6 Inner product & Schur's orthogonality relations/","dgPassFrontmatter":true}
---


> [!definition]
> Define the following inner product on $F_C(G,\mathbb{C})$ as 
> 
> $$\left\langle f_1,f_2\right\rangle =\frac{1}{|G|}\sum_{g\in G}f_1(g)\overline {f_2(g)}.$$

**Remark.** Since it is on $F_C(G,\mathbb{C})$, we can also write 

$$\left\langle f_1,f_2\right\rangle =\frac{1}{|G|}\sum_{C}|C|f_1(C)\overline{f_2(C)},$$

where $C$ runs over all conjugacy classes of $G$.

> [!theorem] Schur's orthogonality relations
> The irreducible characters of $G$ form an orthonormal basis with respect to inner product introduced above.
{ #rld430}


To prove theorem first we talk about dual representation and tensor product of representation. The proof is written [[MATH/代数专题/Nodes/6 Inner product & Schur's orthogonality relations#^wl1f85\|here]].

# Dual Representation

Let $V$ be a vector space of dimension $n$, then the dual space $V^*=\mathrm{Hom}(V,\mathbb{C})$ is also vector space of dimension $n$. Let $v_1,\cdots,v_n$ be a basis of $V$, it is easy to prove that $v_1^*,\cdots,v_n^*\in V^*$ defined as $v_i^*(v_j)=\delta_{ij}$ is a basis of $V^*$.  If $V$ is a $G$-module, then $V^*$ also has a structure of $G$-module defined as 

$$(gf)(v)=f(g^{-1}(v)),\mbox{ for } v\in V,f\in\mathrm{Hom}(V,\mathbb{C}),g\in G.$$

The relations between matrices of $V$ and $V^*$ is the following: Suppose $g\in G$ has matrices as $M(g)=[a_{ij}(g)]$ and $M^*(g)=[a^*_{kl}(g)]$ relative to these two bases. Then we have

$$a_{kl}^*(g)=(gv_l^*)(v_k)=v_l^*(g^{-1}v_k)=a_{lk}(g^{-1}),$$

and so $M^*(g)=M(g^{-1})^T=(M(g)^{-1})^T$. In particular, 

$$\chi_{V^*}(g)=\mathrm{tr}(M^*(g))=\mathrm{tr}(M(g)^{-1})=\chi_V(g^{-1}).$$


> [!lemma]
> $\chi_V(g^{-1})=\overline {\chi_V(g)}$.

**_Proof._**
Let $M(g)$ be matrix of $g$, and let $\lambda_1,\cdots,\lambda_n$ be eigenvalues . Since $G$ is finite, then all $\lambda$ has to be root of unity. Therefore, matrix $M(g^{-1})$ has eigenvalues $\lambda_1^{-1},\cdots,\lambda_n^{-1}$ where $\lambda_i^{-1}=\overline{\lambda_i}$. Hence, $\chi_V(g^{-1})=\overline{\chi_V(g)}$.
<p align="left">□</p>


> [!corollary]
> On the characters, inner product is symmetric.

**_Proof._**
Note that 

$$\left\langle \chi_V,\chi_W\right\rangle=\frac{1}{|G|}\sum_{g\in G}\chi_V(g)\chi_W(g^{-1})=\frac{1}{|G|}\sum_{h\in G}\chi_V(h^{-1})\chi_W(h)=\left\langle\chi_W,\chi_V\right\rangle .$$

Therefore, the inner product is symmetric.
<p align="left">□</p>

# Tensor Product

> [!definition] 
> Given two vector spaces $V$ and $W$, we define their tensor product 
> a vector space $V\otimes W$ which consists of linear combinations $\sum c_{ij}v_i\otimes w_j$ subject to 
> - $(c_1v_1+c_2v_2)\otimes w=c_1(v_1\otimes w)+c_2(v_2\otimes w)$, and 
> - $v\otimes (b_1w_1+b_2w_2)=b_1(v\otimes w_1)+b_2(v\otimes w_2)$.

**Remarks.** 
- If $A$ and $B$ are two algebras, then $A\otimes B$ is also an algebra, where $(a\otimes b)(a'\otimes b')=aa'\otimes bb'$. 
- $\mathrm{End}(V)\otimes\mathrm{End}(W)=\mathrm{End}(V\otimes W)$,
- $\mathrm{Hom}(V,W)=W\otimes V^*$.
- $\chi_{\mathrm{Hom}(V,W)}=\overline{\chi_V}\chi_W$. 

If $v_1,\cdots,v_n$ is a basis of $V$ and $w_1,\cdots,w_m$ is a basis of $W$, we claim that $v_i\otimes w_j$ is a basis of $V\otimes W$. Since $\mathrm{Hom}(V\otimes W,\mathbb{C})=(V\otimes W)^*$. Define $\varphi_{ij}$ by $\varphi_{ij}(v_k\otimes w_\ell)=\delta_{ik}\cdot\delta_{j\ell}$, then $\varphi_{ij}$ is a basis of $(V\otimes W)^*$ and so $\dim(V\otimes W)=nm$. Therefore, $v_i\otimes w_j$ is a basis.

> [!definition] tensor product of algebras
> Let $A$, $B$ be algebras. Define the algebra $A\otimes B$ as $(a\otimes b)(a'\otimes b')=aa'\otimes bb'$. Then $\mathrm{End} V\otimes\mathrm{End}W\simeq\mathrm{End}(V\otimes W)$, where $(\varphi\otimes\psi)(v\otimes w)=\varphi(v)\otimes\psi(w)$. Furthermore, $\mathrm{End}(V\otimes W)$ is also an algebra, defined by $(\varphi\otimes\psi)(\varphi'\otimes\psi')=\varphi\varphi'\otimes\psi\psi'$. 

If $A,B$ are square matrices of $n\times n$ and $m\times m$, respectively. Then tensor product $A\otimes B$ is a block matrix 

$$\begin{bmatrix}a_{11}B &\cdots & a_{1b}B\\ \\
\vdots & &\vdots\\ \\
a_{n1}B &\cdots & a_{nn }B \end{bmatrix}\tag{*}.$$

> [!proposition]
> Let $\varphi\in\mathrm{End} V$ with matrix $A$ with respect to basis $v_1,\cdots,v_n$ and $\psi\in\mathrm{End} W$ with matrix $B$ with respect to basis $w_1,\cdots w_m$, then $\varphi\otimes\psi\in\mathrm{End}(V\otimes W)$ will have matrix $A\otimes B$ with respect to basis $v_i\otimes w$ written in lexicographical order $v_1\otimes w_1,v_1\otimes w_2,\cdots,v_n\otimes w_m$.

> [!definition]
> Let $V$ be a $G$-module and $W$ be a $H$-module, and let $(\rho,V)$ and $(\pi,W)$ be representations of $G, H$, respectively. Then the (outer) tensor product of $V$ and $W$, will be $G\times H$-module $V\otimes W$, where $(g,h)(v\otimes w)=(gv)\otimes (hw)$. 
> 
> If $G=H$, then the (inner) tensor product of $V$ and $W$ is $g(v\otimes w)=(g,g)(v\otimes w)=gv\otimes gw$.

> [!proposition]
> Let $(\rho, V)$ and $(\pi,W)$ be representations of $G$ and $H$, respectively. Then $\chi_{\rho\otimes\pi}(g,h)=\chi_{\rho}(g)\chi_\pi(h)$. 

**_Proof._**
Easy by $(*)$.
<p align="left">□</p>


Now consider the representation of $\mathrm{Hom}(V,W)$. 

> [!proposition]
> Let $V$ and $W$ be $G$-modules, then $\mathrm{Hom}(V,W)$ has a structure of $G$-module defined as $(g\varphi)(v):=g\varphi(g^{-1}v)$. Furthermore, $\mathrm{Hom}(V,W)\simeq V^*\otimes W$.
{ #65b04d}


**_Proof._**
To check this, first we show that $\mathrm{Hom}(V,W)\simeq V^*\otimes W$ as vector space. Let $v_1,\cdots,v_n$ be a basis of $V$, and let $w_1,\cdots,w_m$ be a basis of $W$. Define $v_i^*(v_j)=\delta_{ij}$, and define 

$$\Phi:V^*\otimes W\to\mathrm{Hom}(V,W),v_i^*\otimes w_j\to\varphi_{ij}$$

where $\varphi_{ij}(v_k)=\delta_{ik}w_i$. It is easy to check that $\Phi$ is an isomorphism. Therefore, $\mathrm{Hom}(V,W)\simeq V^*\otimes W$.

Now we claim that $V^*\otimes W$ has structure of $G$-module. Define $g(f\otimes w)=(gf)\otimes (gw)$ where $gf:v\mapsto f(g^{-1}v)$. Using our isomorphism $\Phi$, define $\varphi=\Phi(f\otimes w)$. If $\mathrm{Hom}(V,W)\simeq V^*\otimes W$ as modules, then we have $g\Phi(f\otimes w)=\Phi(g(f\otimes w))$ and so 

$$g\varphi(v)=g\Phi(f\otimes w)(v)=\Phi(gf\otimes gw)(v)=(gf)(v)(gw)=f(g^{-1}v)(gw)=g(f(g^{-1}v)w)=g\varphi(g^{-1}v)$$

by $\varphi(v)=f(v)w$. 
<p align="left">□</p>


For characters, [[MATH/代数专题/Nodes/6 Inner product & Schur's orthogonality relations#^65b04d\|#^65b04d]] gives 

$$\chi_{\mathrm{Hom}(V,W)}(g)=\chi_{V^*\otimes W}(g)=\chi_{V^*}(g)\chi_{W}(g)=\overline{\chi_V(g)}\chi_W(g).$$



> [!definition]
> For any $G$-module $V$, define $V^G=\{v\in V:gv=v\mbox{ for all }g\}$. 

By Maschke's theorem, for $V=V_1\oplus\cdots\oplus V_r$ with irreducible $V_i$'s, $V^G=V_1^G\oplus\cdots\oplus V_{r}^G$ is a submodule. Since each $V_i$ is irreducible, $V_i^G$ is either $0$ or $\mathbb{C}$. Note that $V_i^G\simeq \mathbb{C}$ iff $V_i\cong \mathbb{C}$ iff $V_i$ is trivial representation. It follows that $V^G$ says how many isotypical component isomorphic to trivial representation are in $V$. Define $\psi_1(g)(v)=\frac{1}{|G|}\sum_{g\in G}gv$ for all $g\in G$. Note that $\psi_1(g)$ is a projection of $V$ onto $V^G$, which is zero on any non-trivial irreducible submodule and identity on $V^G$. Hence, $\dim V^G=\mathrm{tr}\psi_1(g)=\frac{1}{|G|}\sum_{g\in G}\chi_V(g)=\left\langle \psi_1,\mathrm{id}\right\rangle$. 

**Remark.** Note that $\chi_V(g)=\mathrm{tr}(\rho(g))$ where $\rho:G\to\mathrm{GL}(V)$ satisfies $gv:=\rho(g)v$.

Now we are ready to prove [[MATH/代数专题/Nodes/6 Inner product & Schur's orthogonality relations#^rld430\|#^rld430]].

**_Proof._**
For any $g\in G$ and $\varphi\in\mathrm{Hom}(V,W)$ with $g\varphi=\varphi$, there is $\varphi(v)=(g\varphi)(v)=g\varphi(g^{-1}v)$ and so $\varphi(g^{-1}v)=g^{-1}\varphi(v)$. It follows that $\varphi\in\mathrm{Hom}_{\mathbb{C}G}(V,W)$. Note that 

$$\dim\mathrm{Hom}_{\mathbb{C}G}(V,W)=\dim\mathrm{Hom}(V,W)^G=\frac{1}{|G|}\sum_{g\in G}\chi_{\mathrm{Hom}(V,W)}(g)=\frac{1}{|G|}\sum_{g\in G}\overline{\chi_V(g)}\chi_W(g)=\left\langle\chi_W,\chi_V\right\rangle.$$

By [[MATH/Cards/Nodes/Schur's Lemma\|Schur's lemma]], $\dim\mathrm{Hom}_{\mathbb{C}G}(s_i,s_j)=\delta_{ij}$ for irreducible representations $s_i$ and $s_j$. Now we finish the proof. 
<p align="left">□</p> 
{ #wl1f85}



> [!corollary]
> A $G$-module $V$ is simple iff $\left\langle \chi_V,\chi_V\right\rangle=1$.

**_Proof._**
By [[MATH/Cards/Nodes/Maschke's Theorem\|Maschke's theorem]], if $V=\alpha_1 S_1\oplus\cdots\oplus \alpha_r S_r$, then $\left\langle\chi_V,\chi_V\right\rangle=\alpha_1^2+\cdots+\alpha_r^2$. Hence $V$ is simple iff $\alpha_1^2+\cdots+\alpha_r^2=1$ iff $\left\langle \chi_V,\chi_V\right\rangle=1$ iff there is the unique $\alpha_i=1$ and all others equal $0$.
<p align="left">□</p>