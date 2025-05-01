---
{"dg-publish":true,"draft":false,"permalink":"/MATH/代数专题/Nodes/5 Semi-Simple and Characters/","dgPassFrontmatter":true}
---


# Semi-Simple

**Example.** For any algebra $A$, $A^{op}$ is the opposite algebra of $A$, where $a\circ_{A^{op}}b=ba$. Let $A=\mathrm{Mat}_n(\mathbb{C})$, then $A^{op}=(\mathrm{Mat}_n(\mathbb{C}),A\circ_{A^{op}}B=BA)$. Define $\varphi:\mathrm{Mat}_n(\mathbb{C})\to \mathrm{Mat}_n^{op}(\mathbb{C}),M\mapsto M^T$. It follows that $A\simeq A^{op}$.  

> [!definition]
> An algebra $A$ is called *semi-simple* if $\mathrm{rad}A=0$.

> [!theorem]
> Let $A$ be a finite-dimensional associative algebra. Then the followings are equivalent:
> - $A$ is semi-simple.
> - $\sum_{i=1}^r\dim V_i^2=\dim A$, where $V_1,\cdots,V_r$ are all pairwise non-isomorphic irreducible $A$-modules.
> - $A=\oplus_{i=1}^r\mathrm{Mat}_{d_i}(\mathbb{C})$
> - Any finite dimensional representation of $A$ is completely reducible, that is, the representation is a direct sum of irreducible representation.
> - $A$ is completely reducible as a $A$-module.
{ #7b841b}


**_Proof._**

(i)<->(ii). Note that $A$ is semi-simple iff $A\simeq\oplus_{i=1}^r\mathrm{End}(V_i)$ by [[MATH/代数专题/Nodes/4 Division algebra, density theorem and radical#^b8akty\|4 Division algebra, density theorem and radical#^b8akty]] iff $\dim A=\sum_{i=1}^r\dim V_i^2$ by $\mathrm{End}(V_i)\simeq n_iV_i$.

(i)->(iii). Note that $A\simeq\oplus_{i=1}^r\mathrm{End}(V_i)=\oplus_{i=1}^rM_{d_i}(\mathbb{C})$. 

(iii)->(i). Any representation is a direct sum of copies of irreducible modules $V_i$, where $V_i$ is unique for $M_{d_i}(\mathbb{C})$. Thus $\mathrm{rad} A=0$ and so $A$ is semi-simple.

(iii)->(iv). By [[MATH/代数专题/Nodes/4 Division algebra, density theorem and radical#^i6fgf3\|4 Division algebra, density theorem and radical#^i6fgf3]], any module is direct sum of irreducible. Then we get (iv).

(iv)->(v) is trivial. 

(v)->(iii). Let $A=\oplus_{i=1}^r n_iV_i$, where $V_i$ are pairwise non-isomorphic. By Schur lemma, $\mathrm{End}_A(V_i)\simeq \mathbb{C}$. It follows that $\mathrm{End}_A(n_iV_i)=M_{n_i}(\mathbb{C})$ and $\mathrm{End}_A(A)=\oplus_{i=1}^rM_{n_i}(\mathbb{C})$. Take $f\in\mathrm{End}_A(A)$, then $f$ satisfies that $f(av)=af(v)$ for any $a,v\in A$. Since $f(a\cdot1_A)=af(1_A)$, then $f$ is a multiplication by $f(1_A)$ and so $\mathrm{End}_A(A)\simeq A^{op}$. Therefore, $A\simeq\oplus_{i=1}^r M_{n_i}(\mathbb{C})$ and we get (iii). 
<p align="left">□</p>


**Remark.** 
- $G$ and $\mathbb{C}G$ have the same representation. Let $G$ be a finite group. Then $\mathbb{C}G$ is semi-simple $\iff$ By [[MATH/代数专题/Nodes/5 Semi-Simple and Characters#^7b841b\|#^7b841b]], any representation for $\mathbb{C}G$, or for $G$, is completely reducible $\iff$ $|G|=\dim\mathbb{C}G=\sum(\dim V_i)^2$. 
- Completely reducible is composable, but not vice versa. See [[MATH/代数专题/Nodes/3 Quaternions and Associative Algebra#^ahq6o8\|here]].

# Characters

> [!definition]
> For any group representation $(V,\rho)$, its character is mapping $\chi_V:G\to \mathbb{C},g\mapsto\mathrm{tr}\rho(g)$. 

**Remarks**. 
- If $\dim V=1$, then $\chi_V(g)$ is just scalar $\rho(g)$.
- $\chi_V$ is in fact in $G^V$ (dual group)
- $\mathrm{Tr}(AB)\neq\mathrm{Tr}(A)\mathrm{Tr}(B)$, so $\chi_V$ is not a group homomorphism.
- $\chi_V(g)$ is the same on conjugacy class of $g$ in G.
- If $V\simeq W$ as $G$-modules, then $\chi_V=\chi_W$ as $\rho_W(g)=\varphi^{-1}(\rho_V(\varphi(g)))$. 

> [!definition]
> Define the vector space of class function on $G$ to be the set of functions from $G$ to $\mathbb{C}$ which are constant on conjugacy classes, denoted by $F_C(G,\mathbb{C})$. In particular, $\chi_V\in F_C(G,\mathbb{C})$.

> [!lemma]
> Let $V=V_1\oplus\cdots\oplus V_r$ be a $G$-module. Then $\chi_V=\chi_{V_1}+\cdots+\chi_{V_r}$. 

**Example.** Consider the permutation representation of $S_3$. Then $\chi_{\mathbb{C}^3}(g)=\{\mbox{number of fixed points by }g\}$. Note that $\chi_{\mathbb{C}^3}=\chi_{S}+\chi_W$ where $S=\{(x,y,z)\in \mathbb{C}^3:x+y+z=0\}$ and $W=\{(x,x,x):x\in \mathbb{C}\}$. Then $\chi_W= 1$ and $\chi_S=\chi_{\mathbb{C}^3}-\chi_W$. 

> [!definition]
> The irreducible characters are characters of irreducible $G$-modules.


> [!lemma]
> Suppose that $f:M_n(\mathbb{C})\to \mathbb{C}$ is a linear map with $f(AB)=f(BA)$ for all $A,B\in M_n(\mathbb{C})$. Then $f=c\cdot \mathrm{Tr},c\in \mathbb{C}$.
{ #230d2b}


**_Proof._**
For any $i\neq j$, we have that $f(E_{ij})=f(E_{ii}E_{ij})=f(E_{ij}E_{ii})=0$ and $f(E_{ii})=f(E_{ij}E_{ji})=f(E_{ji}E_{ij})=f(E_{jj})$. Therefore, $f=c\cdot\mathrm{Tr}$ for some $c\in\mathbb{C}$. 
<p align="left">□</p>


> [!theorem]
> Irreducible characters form a basis of $F_C(G,\mathbb{C})$.
{ #c62c01}


**_Proof._**
Note that $F_C(G,\mathbb{C})=\{f\in\mathrm{Hom}(\mathbb{C}G,\mathbb{C}):f(ab)=f(ba),\forall a,b\in \mathbb{C}G\}$. Since $\mathbb{C}G$ is semi-simple, by [[MATH/代数专题/Nodes/5 Semi-Simple and Characters#^7b841b\|#^7b841b]], $\mathbb{C}G=\mathrm{Mat}_{n_1}(\mathbb{C})\oplus\cdots\oplus\mathrm{Mat}_{n_r}(\mathbb{C})$. By [[MATH/代数专题/Nodes/5 Semi-Simple and Characters#^230d2b\|#^230d2b]], any $f\in F_C(G,\mathbb{C})$ can be written as 

$$f=c_1\mathrm{tr}_{n_1}+\cdots+c_r\mathrm{tr}_{n_r}=c_1\chi_{V_1}+\cdots+c_r\chi_{V_r}.$$

Thus $\chi_{V_1},\cdots,\chi_{V_r}$ is a set of generators of $F_C(G,\mathbb{C})$. 

Assume that $c_1\mathrm{tr}_{n_1}+\cdots+c_r\mathrm{tr}_{n_r}=0$, where $c_i\in \mathbb{C}$. Note that 

$$c_1=(c_1\mathrm{tr}_{n_1}+\cdots+c_r\mathrm{tr}_{n_r})(E_{11})=0$$

and similarly each $c_i=0$. Therefore, $\chi_{V_1},\cdots,\chi_{V_r}$ are linear independent, and so irreducible characters form a basis of $F_C(G,\mathbb{C})$.
<p align="left">□</p>


> [!corollary]
> The number of irreducible characters is equal to the number of conjugacy classes of $G$.

**_Proof._**
Since $\dim F_C(G,\mathbb{C})=\#\mbox{ conjugacy classes}$, then by [[MATH/代数专题/Nodes/5 Semi-Simple and Characters#^c62c01\|#^c62c01]] we have that 

$$\#\mbox{ conjugacy classes}=\#\mbox{ irreducible }G\mbox{-modules}.$$

Now we finish the proof.
<p align="left">□</p>


> [!proposition]
> $V\simeq W$ iff $\chi_V=\chi_W$.

**_Proof._**
Assume that $V=m_1V_1\oplus\cdots\oplus m_rV_r$ where $V_i$ are pairwise non-isomorphic irreducible modules and $W=n_1V_1\oplus\cdots\oplus n_r V_r$. Then $\chi_V=m_1\chi_{V_1}+\cdots+m_r\chi_{V_r}$ and $\chi_{W}=n_1\chi_{V_1}+\cdots+n_r\chi_{V_r}$. Therefore, $\chi_V=\chi_W$ iff $m_i=n_i$ iff $V\simeq W$. 
<p align="left">□</p>

