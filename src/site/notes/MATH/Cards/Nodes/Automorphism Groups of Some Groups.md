---
{"dg-publish":true,"permalink":"/MATH/Cards/Nodes/Automorphism Groups of Some Groups/","dgPassFrontmatter":true}
---


> [!proposition]
> If $p$ is an odd prime, then $\operatorname{Aut}\left(Z_{p^n}\right) \cong Z_{\varphi\left(p^n\right)}$ with $n\geqslant 1$. If $p=2$, then $\operatorname{Aut}\left(Z_{2^n}\right) \cong Z_2 \times Z_{2^{n-2}}$ with $n \geq 2$.  

**_Proof._**
The case of odd prime is easy, using the existence of primitive root. 

For the case of $2^n$, we can prove that $a^{2^{k-2}} \equiv 1 \pmod{2^k}$ and $3^{2^{k-3}}\not\equiv 1\bmod{ 2^k}$ with $k\geqslant 3$ by induction. Then we finish the proof by [here](https://en.wikipedia.org/wiki/Multiplicative_group_of_integers_modulo_n#Powers_of_2). 
<p align="right">□</p>


> [!proposition]
> Let $D_{2n}$ be a dihedral group. Then:
> - $\mathrm{Aut}(D_4)\cong S_3$;
> - $\mathrm{Aut}(D_{2n})\cong \mathbb{Z}_n{:}\mathrm{Aut}(\mathbb{Z}_n)$ when $n\geq 3$.

**_Proof._**
When $n=2$, the group $D_4\cong \mathbb{Z}_2\times \mathbb{Z}_2$. Suppose $D_4=\{1,a,b,ab\}$ where $|a|=|b|=|ab|=2$. For any $\varphi\in\mathrm{Aut}(D_4)$, there is $\varphi(1)=1$. Thus $|\mathrm{Aut}(D_4)|\leq 3!=6$. Furthermore, since any element of $\mathrm{Sym}\{a,b,ab\}$ is an automorphism, we have $\mathrm{Aut}(D_4)\cong S_3$.

When $n\geq 3$, define $D_{2n}$ as 

$$D_{2n}=\left\langle x,y:|x|=n,|y|=2,x^y=x^{-1}\right\rangle.$$

Then for any $\varphi\in\mathrm{Aut}(D_{2n})$, it satisfies $|\varphi(x)|=n$ and $|\varphi(y)|=2$. Hence 

$$\begin{aligned}
&\varphi(x)\in\{x^l:(l,n)=1\},\\
&\varphi(y)\in\{x^my:0\leq m\leq n-1\}.
\end{aligned}$$

Let $A:=\left\langle\varphi_m:0\leq m\leq n-1\right\rangle$ and $B:=\left\langle\varphi^l:(l,n)=1\right\rangle$, where $\varphi_m(x)=x,\varphi_m(y)=x^my$ and $\varphi^l(x)=x^l,\varphi^l(y)=y$. Then $\mathrm{Aut}(D_{2n})=\left\langle A,B\right\rangle$ and $A\cap B=1$. It is easy to verify that $B\lhd\mathrm{Aut}(D_{2n})$. Therefore, we have 

$$\mathrm{Aut}(D_{2n})=A{:}B\cong \mathbb{Z}_n{:}\mathrm{Aut}(\mathbb{Z}_n)$$

and so the proof is completed.
<p align="right">□</p>
> [!proposition]
> $\mathrm{Aut}(Q_8)=S_4$.
{ #5s4s0f}


**_Proof._**
Note that $Q_8$ has three cyclic subgroups of order $4$: $\langle i\rangle,\langle j\rangle,\langle k\rangle$, and $\operatorname{Aut}\left(Q_8\right)$ acts on these three subgroups; inducing a homomorphism $\Phi: \operatorname{Aut}\left(Q_8\right) \rightarrow S_3$. We can see that, the homomorphism is surjective, since the two automorphisms $f: i \mapsto j, j \mapsto i$, and $g: j \mapsto k, k \mapsto j$ give two transpositions in $S_3$. Thus $\Phi(\mathrm{Aut}(Q_8))\cong S_3$. 

The kernel contains those $\varphi \in \operatorname{Aut}(G)$ such that $\varphi(\langle i\rangle)=\langle i\rangle$, $\varphi(\langle j\rangle)=\langle j\rangle$ and $\varphi(\langle k\rangle)=\langle k\rangle$. Notice that $\varphi(\langle i\rangle)=\langle i\rangle$ means $\varphi(i) \in\{i,-i\}$, and similarly, $\varphi(j) \in\{j,-j\}$. One can check that these four choices are automorphisms of order $2$ (or $1$) (since they are switching elements in a pair), and hence the kernel is [Klein-4](https://en.wikipedia.org/wiki/Klein_four-group) group $V_4$.

Consider the following automorphisms: $S: i \mapsto j, j \mapsto i$ and $T: j \mapsto k, k \mapsto j$. Since $S$ and $T$ fix subgroup $\left\langle k\right\rangle$ and $\left\langle i\right\rangle$ respectively, they are not inner. Therefore, we have $\langle S, T\rangle=K \leqslant \operatorname{Aut}\left(Q_8\right)$, such that $K \cong S_3$ and $\Phi(K)=S_3$. Also,

$$
\operatorname{ker}(\Phi) \cap K=1
$$


Therefore, $\operatorname{Aut}\left(Q_8\right)=\operatorname{ker}(\Phi) \rtimes K \cong V_4 \rtimes S_3$.

Consider an element $f: i \mapsto-i, j \mapsto j$ of $\operatorname{ker}(\Phi)$, and two elements of $K \cong \operatorname{Im}$: $g: i \mapsto j, j \mapsto i$ (like a transposition), and $h: i \mapsto j, j \mapsto k$ (like a 3-cycle). One can check that $f$ doesn't commute with $g$ as well as $h$.
In fact, this shows that no element of $V_4 \backslash\{1\}$ commutes with any element of $K \backslash\{1\}$. This means, the action of $K$ on $V_4$ (by conjugation) is faithful; and up to equivalence, there is only one such action. Therefore, $\operatorname{Aut}\left(Q_8\right)=V_4 \rtimes K \cong S_4$. 
<p align="right">□</p>


> [!proposition]
> The following holds:
> - $\mathrm{Aut}(p_{-}^{1+2})\cong p_{-}^{1+2}{:}\mathbb{Z}_{p-1}$;
> - $\mathrm{Aut}(p_{+}^{1+2})\cong \mathrm{GL}_2(p)$.

**_Proof._**
i) #todo Assume that $G:=p_{-}^{1+2}=\left\langle a\right\rangle{:}\left\langle b\right\rangle$ with $|a|=p^2$ and $|b|=p$. Then $G/\Phi(G)\cong \mathbb{Z}_p^2$ and $\Phi(G)=Z(G)=G'=\{1,a^p,\cdots,a^{p(p-1)}\}$. For any nontrivial $\varphi\in\mathrm{Aut}(G)$, $\varphi$ is a nontrivial automorphism of $G/\Phi(G)$. Thus, $\mathrm{Aut}(G)\lesssim\mathrm{GL}_2(p)$. Note that $[a,b]=a^{-1}a^b=a^{kp}$ for some $k\in \mathbb{Z}$, we may suppose that $a^b=a^{kp+1}$. 

(to be continued)

ii) Since $G=\langle a,b|a^p=b^p=c^p=1,[a,b]=c\rangle$ by the argument of [[MATH/Cards/Nodes/Structure of p-groups#^oymbgb\|Structure of p-groups#^oymbgb]], it is easy to prove. 


<p align="right">□</p>
