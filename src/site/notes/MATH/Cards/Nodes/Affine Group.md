---
{"dg-publish":true,"aliases":["AGL"],"draft":false,"permalink":"/MATH/Cards/Nodes/Affine Group/","dgPassFrontmatter":true}
---


> [!definition]
> Let $V=\mathbb{F}_q^n$ be a vector space. It can be viewed as an elementary abelian group $(V,+)$. Then the action of $\mathrm{GL}(V)$ on $V$ induces a group extension:
> 
> $$
> \operatorname{AGL}_n(q):=\mathbb{Z}_p^{f n}{:} \mathrm{GL}_n(q),
> $$
> 
> which is called an *affine group*. 

**Remark.** When $n=1$, $\mathrm{GL}_1(q)$ is cyclic and it is isomorphic to $\mathbb{F}_{q}^\times$. Assume that $q=p^f$. Recall that a field $F=\mathbb{F}_{p^f}$ can be viewed as a vector space $F^{+}=\mathbb{F}_p^f=V$, of dimension $f$ over $\mathbb{F}_p$. Then $\mathrm{AGL}_1(q)\cong \mathbb{F}_q^{+}{:}\mathbb{F}_q^{\times}$ acts on $V$ as linear transformations:

$$(a,b):x\mapsto a+xb,\forall x\in \mathbb{F}_p^f.$$

> [!theorem]
> Let $G=N{:}H\leqslant\mathrm{AGL}_1(p^n)$ with $N\cong \mathbb{Z}_p^n$, and let $H\leqslant \mathbb{Z}_{p^n-1}$ with $|H|\not\mid p^f-1$ for any $f\mid n,f<n$. Then $\mathrm{Aut}(G)\cong\mathrm{A}\mathrm{\Gamma L}_1(p^n)=\mathrm{AGL}_1(p^n){:}\left\langle\phi\right\rangle$, where $\phi$ is the Frobenius automorphism of order $n$.

**_Proof._**
For any $\sigma\in\mathrm{Aut}(G)$, there is $N^\sigma/(N^\sigma\cap N)\lhd H$ as $N^\sigma\lhd G$. It yields that $N^\sigma=N$ by $(|N|,|H|)=1$. Therefore, $N$ is a [[MATH/Cards/Nodes/Characteristic Subgroup\|characteristic subgroup]] of $G$. In addition, since $Z(G)$ is trivial, $G\cong\mathrm{Inn}(G)\lhd\mathrm{Aut}(G)$. Therefore, we have that $N\lhd \mathrm{Aut}(G)$. 

Let $S=\{H^\sigma:\sigma\in\mathrm{Aut}(G)\}$. Since all complements of $N$ are conjugate in $G$ by [[MATH/Cards/Nodes/Hall's Theorems\|Hall's theorem]], $N$ is transitive on $S$. As $\mathrm{Aut}(G)$ is transitive on $S$, by [[MATH/Cards/Nodes/Frattini's Argument\|Frattini's argument]] we have that $\mathrm{Aut}(G)=NG_{(S)}$, where $G_{(S)}$ is the kernel of $\mathrm{Aut}(G)$ acting on $S$. If there exists a nontrivial $n\in N$ such that $H^n=H$, then for any $b\in H$, there is $b^n\in H$. Note that $b^n\in\mathrm{AGL}_1(p^n)$ maps $x$ to $bx+(nb-b)$, so $nb=b$ for all $b\in H$. Thus $n=0$, contradiction. Therefore, the action of $N$ on $S$ is regular. So $G_{(S)}\cap N$ is trivial and $\mathrm{Aut}(G)=N{:}L$ where $L=G_{(S)}$. Since $G\lhd\mathrm{Aut}(G)$, $H$ is a normal subgroup of $L$. 

Let $K=\{\alpha\in L:h^\alpha=h,\forall h\in H\}$. Then $H\leqslant K\lhd L$ and $L$ can be written as $L=K{.}L_0$. For any $\alpha\in K$, there is $v^{\alpha h}=v^{h\alpha}$ for all $v\in N$. Since $N$ can be seen as $\mathbb{F}_pH$-module, $\alpha$ is a module isomorphism of $N$. Note that $N$ is irreducible. Thus by [[MATH/Cards/Nodes/Schur's Lemma\|Schur's lemma]], $K$ is a multiplicative group of a field. Since $K\leqslant \mathrm{Aut}(N)\cong \mathbb{Z}_{p^n-1}$ and $|H|\not\mid p^f-1$ for all $f\mid n$ with $f<n$, we obtain that $K\cong \mathbb{Z}_{p^n-1}$ by [[MATH/Cards/Nodes/Properties of Finite Field\|this]]. Hence, $\mathrm{Aut}(G)\cong(\mathbb{Z}_p^n{:}\mathbb{Z}_{p^n-1}){.}\widetilde{L_0}$ with $\widetilde{L_0}\cong L_0$ and so $\mathrm{Aut}(G)\leqslant\mathrm{Aut}(\mathrm{AGL}_1(p^n))$. 

We claim that $\mathrm{Aut}(\mathrm{AGL}_1(p^n))=\mathrm{A}\mathrm{\Gamma L}_1(p^n)$. Let $A:=\mathrm{Aut}(\mathrm{AGL}_1(p^n))$, and let $\mathrm{AGL}_1(p^n)=F^+{:}F^{\times}$ where $F=\mathbb{F}_{p^n}$. Similarly, by [[MATH/Cards/Nodes/Hall's Theorems\|Hall's theorem]] each complement of $F^+\cong \mathbb{Z}_p^n$ in $\mathrm{AGL}_1(p^n)$ is in the same conjugacy class, and so there exists $a \in F^+$ such that $(F^\times)^{\delta a}=F^\times$. Then we may assume that $(F^\times)^\delta=F^\times$ and $\delta(1)=1$ as $a\in\mathrm{Inn}(\mathrm{AGL}_1(p^n))$.

For $0 \neq a \in F^+$, use $\bar{a}$ to denote the corresponding element of $F^\times$. So the semidirect product action is $\bar{a} b \bar{a}^{-1}=a b$. Now, for $0 \neq a \in F^\times$, using $\delta(1)=1$, we have

$$\delta(a)=\delta\left(\bar{a} 1 \bar{a}^{-1}\right)=\delta(\bar{a}) 1 \delta(\bar{a})^{-1},$$

so $\overline{\delta(a)}=\delta(\bar{a})$. In other words $\delta$ is acting in the same ways on $F^+\setminus\{0\}$ and on $F^{\times}$. Then, for $a, b \in F^+ \backslash\{0\}$

$$\delta(a) \delta(b)=\overline{\delta(a)} \delta(b) \overline{\delta(a)}^{-1}=\delta(\bar{a}) \delta(b) \delta(\bar{a})^{-1}=\delta\left(\bar{a} b \bar{a}^{-1}\right)=\delta(a b)$$

and hence $\delta$ is acting as a field automorphism of $F$. Therefore, $\mathrm{Aut}(\mathrm{AGL}_1(p^n))=\mathrm{A}\mathrm{\Gamma L}_1(p^n)$.

Furthermore, since $\mathrm{A}\mathrm{\Gamma L}_1(p^n)$ acts on $G=N{:}H$ faithfully, we obtain that $\mathrm{Aut}(G)=\mathrm{A}\mathrm{\Gamma L}_1(p^n)$. 
<p align="left">□</p>

