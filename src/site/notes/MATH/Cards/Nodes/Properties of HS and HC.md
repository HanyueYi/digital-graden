---
{"dg-publish":true,"draft":false,"permalink":"/MATH/Cards/Nodes/Properties of HS and HC/","dgPassFrontmatter":true}
---


> [!proposition]
> Let $G$ be a quasiprimitive permutation group acting on $\Omega$. If $G$ has two different minimal normal subgroups $M$ and $N$, then there is 
> 
> $$M{:}\mathrm{Inn}(M)\leqslant G\leqslant M{:}\mathrm{Aut}(M).$$
> 
> Furthermore, $M\cong N\cong T^l$ is isomorphic to a direct product of isomorphic nonabelian simple groups $T$, and $\mathrm{Aut}(M)=\mathrm{Aut}(T)\wr S_l$.
{ #04lqgl}


**_Proof._**
Since $G$ is quasiprimitive, groups $M$ and $N$ are transitive. By [[MATH/Cards/Nodes/Minimal Normal Subgroups of Permutation Groups\|Minimal Normal Subgroups of Permutation Groups]], we have $M=C_G(N)$, $\mathrm{soc}(G)=M\times N$ and $M\cong N$. Note that $M\times N$ can be identified by 

$$M\times N=\hat M\times \check M=\hat M{:}\tilde M=M{:}\mathrm{Inn}(M),$$

where the notations come from [[MATH/Cards/Nodes/Three Permutations on G Induced from G\|Three Permutations on G Induced from G]]. By NC lemma, there is $N_G(N)/C_G(N)=G/M\leqslant\mathrm{Aut}(M)$ and so $G\leqslant M{:}\mathrm{Aut}(M)$. Moreover, $\mathrm{Aut}(M)=\mathrm{Aut}(T)\wr S_l$ is proved [[MATH/Cards/Nodes/Automorphism Groups of Direct Product of Isomorphic Simple Groups\|here]]. 
<p align="left">□</p>

**Remark.** If $l=1$, the type is named HS; while when $l>1$ the type is named HC. We have the following lemma. 

> [!lemma]
> A quasiprimitive permutation group of type HS, HC or HA is primitive.
{ #0e6r68}


**_Proof._**
i) Let $G=T{:}H$ be of type HS with simple $T$. By [[MATH/Cards/Nodes/Properties of HS and HC#^04lqgl\|#^04lqgl]], we have $\mathrm{Inn}(T)\leqslant H\leqslant\mathrm{Aut}(T)$. Then $H=G_\omega$ where $\omega=1\in T$. It remains to show $H$ is a maximal subgroup by [[MATH/Cards/Nodes/Equivalent Condition of Primitivity\|Equivalent Condition of Primitivity]]. Otherwise, there is a $K$ such that $H<K<G$, and there exists an element $g\in K\backslash H$ with the form $g=(t,h)\in G$. Then $(t,1)=(t,h)(1,h^{-1})\in K$. 

For any element $x\in H$, we have $(1,x^{-1})\in K$ and $(1,x^{-1})(t,1)=(t^x,x^{-1})\in K$. Hence $(t^x,1)=(t^x,x^{-1})(1,x)\in K$ and so $M$ is a subgroup of $K$, where 

$$M=\langle (t^x,1):x\in H\rangle\leqslant T\times\{1\}.$$

Since $H\geqslant\mathrm{Inn}(T)$, the action of $T$ on $M$ by conjugation fixes $M$. So $M\lhd T$ and $M=T$. Thus $K\geqslant\langle M,H\rangle=G$, contradiction. Therefore, $G$ is primitive.

ii) The proof is similar to i). Let $G=M{:}H$ be of type HC with $M\cong T^l$ a direct product of isomorphic simple groups. By [[MATH/Cards/Nodes/Properties of HS and HC#^04lqgl\|#^04lqgl]], we have $\mathrm{Inn}(M)\leqslant H\leqslant\mathrm{Aut}(M)$. If $H=G_\omega$ with $\omega=1\in T$ is not a maximal subgroup of $G$, then there is a $L$ such that $H<L<G$ and $L$ has a subgroup $N:=m^H$ where $(m,h)\in L\setminus H$. Note that $N\lhd M$ and $M$ is a minimal normal subgroup of $G$. Thus $N=M$ and so $L=G$, which is impossible. So $G$ is primitive.

iii) When $G$ is of type HA, the primitivity of $G$ is proved [[MATH/Cards/Nodes/Affine Quasiprimitive is Primitive\|here]].
<p align="left">□</p>
