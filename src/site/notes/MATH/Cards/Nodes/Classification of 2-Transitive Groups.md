---
{"dg-publish":true,"permalink":"/MATH/Cards/Nodes/Classification of 2-Transitive Groups/","dgPassFrontmatter":true}
---

 #RESOURCE/cards #TERMS/quasiprimitive #TERMS/2-transitive #todo 

Here we want to prove the following well-known theorem. 

In fact, it is proved [[MATH/Cards/Nodes/Burnside 2-Transitive\|here]]. This notes come from GroupTheory2024Spring, but I don't know understand the idea of our professor ( )

> [!theorem] Burnside
> A $2$-transitive permutation group $G$ has a unique minimal normal subgroup which is either:
> - non-abelian simple group, where $G$ is called almost simple;
> - elementary abelian, where $G$ is called affine.

Recall that for a quasiprimitive permutation group $G$, we have $\mathrm{soc}(G)=T^n$ where $T$ is a simple group and $n\geq 1$. The proof is as follows.


<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



Let $X$ be a quasiprimitive permutation group on a finite set $\Omega$ of size $n$, and $\alpha\in\Omega$. Let $B$ be the socle of $X$. Then $B=K_1\times K_2\cong T^k$ with $k\geq 1$ where $T$ is a simple group by [[MATH/Cards/Nodes/Minimal Normal Subgroups of Permutation Groups#^7p85qz\|Minimal Normal Subgroups of Permutation Groups#^7p85qz]]. 

</div></div>


Let $G$ be a $2$-transitive group. Then $G$ is primitive and quasiprimitive, and so $\mathrm{soc}(G)=T^n$ with simple $T$. Then we have the following lemma.

> [!lemma] 
> Let $G\leq\mathrm{Sym}(\Omega)$ be a $2$-transitive group. Let $N$ be a normal subgroup of $G$ such that $N=T^k$ with $k\geq 2$ and $T$ non-abelian simple. Then:
> - $N$ does not have a proper normal subgroup which is regular on $\Omega$. Furthermore, the group $G$ is not HS, HC, SD, CD.
> - $N$ is not regular on $\Omega$. Furthermore, $G$ is not TW.
{ #ou5ao7}


**_Proof._**
Assume that there is a regular $M\lhd N$. Note that $N_{\omega}\neq 1$ is half-transitive on $\Omega\setminus\{\omega\}$ as $N_\omega\lhd G_\omega$, and define $m$ as the size of an orbits of $N_\omega$ on $\Omega\setminus\{1\}$. Then both $|\Omega|-1$ and $|N_\omega|$ are divisible by $m$. Furthermore, because $N=M{:}N_\omega$, we have $|\Omega|=|M|=|T|^l$ and $|N_\omega|=|T|^{k-l}$ with $1\leq l<k$. So $m$ divides $\gcd(|\Omega|-1,|N_\omega|)=(|T|^l-1,|T^{k-l}|)=1$ and it yields $m=1$, which is impossible.

Suppose that $N$ is regular on $\Omega$. Then we have $G=N{:}G_{\omega}$ and so $G_\omega$ acting on $\Omega$ can be identified by $G_\omega$ acting $N$ by conjugation. By [[MATH/Cards/Nodes/Burnside's Theorem\|Burnside's Theorem]] $|N|$ has at least $3$ prime divisors $r,s,t$. Let $x,y,z$ be elements of $N$ such that $|x|=r$, $|y|=s$ and $|z|=t$. Then $x^{G_\omega}$, $y^{G_\omega}$ and $z^{G_\omega}$ are three orbits and so $\mathrm{rank}(G)\geq 4$. Contradiction.
□

> [!corollary]
> Let $G$ be a quasiprimitive permutation group on $\Omega$, and let $N=\mathrm{soc}(G)$. If $N$ is regular on $\Omega$, then $\mathrm{rank}(G)\geq 4$.

**_Proof._**
By the proof of (ii) of [[#^ou5ao7]].
□

> [!theorem]
> Let $G\leq\mathrm{Sym}(\Omega)$ be a $2$-transitive group. Then $G$ acts on $\Omega$ in product action, that is, $\Omega=\Delta^k$ and $G\leq\mathrm{Sym}({\Delta})\wr S_k$ acting on $\Omega$ by 
> 
> $$(\delta_1,\cdots,\delta_k)^{(\tau_1,\cdots,\tau_k)\pi}=(\delta_1^{\tau_1},\cdots,\delta_k^{\tau_k})^\pi=(\delta_{1^{\pi^{-1}}}^{\tau_{1^{\pi^{-1}}}},\cdots,\delta_{k^{\pi^{-1}}}^{\tau_{k^{\pi^{-1}}}})$$
> 
> where $\delta_i\in\Delta$ and $\pi\in S_k$. Furthermore, in this case $G$ is PA.

**_Proof._**
Let $N\lhd_{\min}G$ such that $N=T^k$ with $k\geq 2$ and $T$ nonabelian simple. Note that $N$ is transitive as $G$ is $2$-transitive and quasiprimitive. So $N_\omega\neq 1$ and $N$ does not have a normal subgroup which is regular on $\Omega$ by [[#^ou5ao7]]. Additionally, by the proof of [[MATH/Cards/Nodes/Minimal Normal Subgroups of Permutation Groups\|Minimal Normal Subgroups of Permutation Groups]], $N$ is the unique minimal normal subgroup. We write $N$ as $N=T_1\times\cdots\times T_k$ where $T_1\cong\cdots\cong T_k$. 

Let $H_i$ be the projection of $N_\omega$ into $T_i$. Then $H_i\cong N_\omega/(N_\omega\cap M_i)\cong N_\omega M_i/M_i$, where $M_i=\Pi_{j\neq i}T_j$ and $N/M_i\cong T_i$. 

- [ ] Then $H_i\lesssim T_i$ and $H_1\cong\cdots\cong H_k$.

Since $G=NG_\omega$ is transitive on $\{T_1,\cdots,T_k\}$ and $N$ acts on $\mathscr T:=\{T_1,\cdots,T_k\}$ trivially by conjugation, we have $G_\omega$ is transitive on $\mathscr T$. Also, $G_\omega$ is transitive on $\{H_1,\cdots,H_k\}$ by $N_\omega\lhd G_\omega$.

Then $N_\omega\leq K:=H_1\times\cdots\times H_k<N$ and $K$ is normalized by $G_\omega$. Thus $G_{\omega}\leq KG_\omega<G$. Since $G$ is $2$-transitive and primitive, $G_\omega$ is maximal and so $G_\omega=KG_\omega$. Note that $K\leq G_\omega$ and $K<N$ yield $K\leq N_\omega$. Therefore, we have $K=N_\omega$. 

As $N=T_1\times\cdots\times T_k$ acting on $\Omega$ transitively, $\Omega$ can be identified with

$$[N{:}N_\omega]=[(T_1\times\cdots\times T_k):(H_1\times\cdots\times H_k)]=[T_1:H_1]\times\cdots\times[T_k:H_k]:=\Delta_1\times\cdots\times\Delta_k,$$

and $N$ acts on $\Omega$ by 

$$\omega^{(t_1,\cdots,t_k)}=(H_1x_1,\cdots,H_kx_k)^{(t_1,\cdots,t_k)}=(H_1x_1t_1,\cdots,H_kx_kt_k).$$

- [ ] Then we have $G_\omega\leq(L_1\times\cdots\times L_k){:}S_k$ where $H_i\leq L_i\leq\mathrm{Aut}(T_i)$ and $G\leq(\mathrm{Aut}(T_1)\times\cdots\times\mathrm{Aut}(T_k)){:}S_k$.


It yields that $G$ acts on $\Omega$ in product action and we complete the proof.
□

> [!corollary]
> By [[MATH/Cards/Nodes/Classification of Quasiprimitive Groups\|Classification of Quasiprimitive Groups]], a $2$-transitive permutation group is one of the three types: HA, AS and PA.

- [ ] to be continued

