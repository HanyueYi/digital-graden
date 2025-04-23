---
{"dg-publish":true,"aliases":["Hall's theorem"],"permalink":"/MATH/Cards/Nodes/Hall's Theorems/","dgPassFrontmatter":true}
---


> [!definition]
> Let $G$ be a finite group of order $|G|=p_1^{f_1}\cdots p_t^{f_t}$, where $p_i$ are the prime divisors of $|G|$. Let $\pi(G)=\{p_1,\cdots,p_t\}$. For a subset $\pi\subseteq \pi(G)$, a subgroup $H\leqslant G$ is called a *Hall $\pi$-subgroup* of $G$ if $\pi(H)=\pi$ and $\gcd(|H|,|G/H|)=1$. 

**Remark.** Note that Hall subgroups do NOT always exist, and two Hall subgroups are NOT always conjugate.
- Let $G=A_5$. Suppose $H\leqslant G$ with $|H|=20$. Then $[G:H]$ is of size $3$. Since $G$ is simple, $G^{[G:H]}\cong G$ acting on $[G:H]$ is faithful. So we have $A_5=G\leqslant\mathrm{Sym}([G:H])\cong S_3$, which is impossible. Therefore, $\{2,5\}$-Hall subgroup does not exist.
- Let $G=\mathrm{PSL}_2(11)$. This group has two subgroups $H\cong A_4$ and $K\cong D_{12}$, which are Hall $\{2,3\}$-subgroups of $G$ but not conjugate.

> [!theorem]
> Let $G$ be a finite group of order $|G|=p_1^{f_1}\cdots p_t^{f_t}$ where $p_i$ are prime. Then $G$ is solvable if and only if $G$ has Hall $\pi$-subgroups for each subset $\pi\subseteq\pi(G)$.
{ #58494b}


**_Proof._**
If $|\pi|=1$, then $G$ is solvable as $p$-group has nontrivial center. If $|\pi|=2$, by [[MATH/Cards/Nodes/Burnside's Theorem\|Burnside's Theorem]] $G$ is solvable. Now we assume that $|\pi|\geqslant 3$ and assume inductively that this theorem holds for groups of which the order has at most $t-1$ prime divisors including multiplicity.

i) Firstly, assume that $G$ has Hall subgroups for all $\pi\subseteq \pi(G)$. We aim to show $G$ is a solvable group. Let $H_i$ be a Hall $\{p_i\}'$-subgroup of $G$ for $1\leqslant i\leqslant t$, where $\{p_i\}'=\pi(G)\setminus \{p_i\}$. By induction hypothesis, $H_i$ is solvable. There [[MATH/Cards/Nodes/Group Core#^a65a1w\|exists]] a prime divisor $p$ of $|H_1|$ such that $O_p(H_1)\neq 1$. Since $p$ divides $|H_2|$ or $|H_3|$, WLOG we may assume that $p$ divides $|H_2|$. Let $P$ be a Sylow $p$-subgroup of $H_2$. Then $P$ is a Sylow $p$-subgroup of $G$. Furthermore, by [[MATH/Cards/Nodes/Sylow Theorems\|Sylow theorem]] $O_p(H_1)\leqslant P^g\leqslant H_2^g$ for some $g\in G$. We have $G=H_1H_2^g$, because

$$|H_1H_2^g|=\frac{|H_1||H_2^g|}{|H_1\cap H_2^g|}\geqslant \frac{(p_2^{f_2}\cdots p_t^{f_t})(p_1^{f_1}p_3^{f_3}\cdots p_t^{f_t})}{p_3^{f_3}\cdots p_t^{f_t}}\geqslant |G|.$$

Let $N=\left\langle O_p(H_1)^x:x\in G\right\rangle$ be the normal closure of $O_p(H_1)$ in $N$. Then $N\lhd G$. For any $x\in G$, there exist $x_1\in H_1$ and $x_2\in H_2^g$ such that $x=x_1x_2$. Then we have $O_p(H_1)^x=O_p(H_1)^{x_1x_2}=O_p(H_1)^{x_2}\leqslant H_2^g$ and so $N\leqslant H_2^g$. Thus $N$ is the proper normal subgroup of $G$. 

For a Hall $\pi$-subgroup $H$ of $G$, we have that $N\cap H$ is a Hall $\pi$-subgroup of $N$ by computing $|HN|=|H||N|/|H\cap N|$, and $HN/N\cong H/(H\cap N)$ is a Hall subgroup of $G/N$. By induction hypothesis $N$ and $G/N$ are solvable, which yields that $G$ is solvable.

ii) Conversely, assume that $G$ is solvable. Take a subset $\pi\subseteq\pi(G)$ with $|\pi|=|\pi(G)|-1$, and it suffices to find a Hall $\pi$-subgroup of $G$. Let $M\lhd_{\min}G$. Then $M=\mathbb{Z}_p^d$ for some prime $p$ and $\overline G:=G/M$ is solvable. Let $\overline H$ be a Hall $\pi$-subgroup of $\overline G$. If $p\in\pi$, then the full preimage of $\overline H$ under $G\to\overline G$ is a Hall $\pi$-subgroup of $G$. Otherwise, if $p\notin \pi$, then $p\not\mid |\overline H|$. 

Define $X:=M{.}\overline H$ as the full preimage of $\overline H$ under $G\to\overline G$. If $X<G$, then by induction, $X$ has a Hall $\pi$-subgroup $Y$ which is isomorphic to $\overline H$, and $Y$ is a Hall $\pi$-subgroup of $G$. So now we suppose that $G=X=M{.}\overline H$. 

Since $\overline H$ is solvable, there [[MATH/Cards/Nodes/Group Core#^a65a1w\|exists]] a prime $q\in\pi(\overline H)$ such that $\overline Q=O_q(\overline H)\neq 1$. Let $M{.}\overline Q$ be the full preimage of $\overline Q$ under $G\to\overline G$, and let $Q$ be a Sylow $q$-subgroup of $M{.}\overline Q$. Remark that $Q\cong\overline Q$ and $M{.}\overline Q=M{:}Q\lhd G$, because $\overline Q\lhd\overline H$. For any $x\in N_M(Q)$ and $y\in Q$, we have $xyx^{-1}y^{-1}\in M\cap Q=1$ and so $N_M(Q)=C_M(Q)$.

Assume that $N_G(Q)\cap M=N_M(Q)=C_M(Q)=1$. With this assumption, we claim that $|N_G(Q)|\geqslant |N_{\overline H}(\overline Q)|$. Since $\overline Q\lhd\overline H$,  there is $\overline H=N_{\overline H}(\overline Q)$. Take an element $\overline g\in\overline H=N_{\overline H}(\overline Q)$ and a preimage $g$ under $G\to\overline G$. Then $M{:}Q=(M{:}Q)^g=M(g^{-1}Qg)$ and so $g^{-1}Qg\subseteq M{:}Q$. Since $g^{-1}Qg$ is a Sylow $q$-subgroup of $M{:}Q$, there exists $x\in M$ such that $x^{-1}(g^{-1}Qg)x=Q$ by [[MATH/Cards/Nodes/Sylow Theorems\|Sylow theorem]], that is, $gx\in N_G(Q)$. If there is another $x'$ such that $gx'\in N_G(Q)$ with $x'\in M$, then $x^{-1}x'=(gx)^{-1}(gx')\in N_G(Q)\cap M=1$ and it yields $x=x'$. Therefore, there is a unique $x\in M$ such that $gx\in N_G(Q)$. Define 

$$\varphi:N_{\overline H}(\overline Q)\to N_G(Q), \overline g\mapsto gx.$$

Suppose $g_1x_1=g_2x_2$. Then $\overline{g_2^{-1}g_1}=\overline{x_2x_1^{-1}}=\overline1$ yields that $\overline {g_1}=\overline {g_2}$ and so $\varphi$ is injective. Thus $|N_{\overline H}(\overline Q)|\leqslant|N_G(Q)|$ and we prove the claim.

If $|\overline H|=|N_{\overline H}(\overline Q)|=|N_G(Q)|$, then $N_G(Q)$ is a Hall $\pi$-subgroup of $G$. Otherwise, if $|N_{\overline H}(\overline Q)|<|N_G(Q)|$, then

$$N_G(Q)=N_G(Q)/(N_G(Q)\cap M)\cong N_G(Q)M/M\leqslant G/M=\overline H=N_{\overline H}(\overline Q),$$

which is impossible. 

Now we assume that $C_M(Q)=N_M(Q)=N_G(Q)\cap M\neq 1$. Let $P:=C_M(Q)\neq 1$. Note that $P\lhd_{\mathrm{char}} Z(M{:}Q)\lhd_{\mathrm{char}} M{:}Q\lhd G$ yields that $P\lhd G$. Since $P\leqslant M\lhd_{\min}G$ and $P\neq 1$, we have $P=M$ and so $M{:}Q=M\times Q\lhd G$. Thus $Q$ is a normal subgroup of $G$. Let $\overline K$ be a Hall $\pi$-subgroup of $G/Q$. Then the full preimage of $\overline K$ under $G\to G/Q$ is a Hall $\pi$-subgroup of $G$.
<p align="left">□</p>

**Remark.** The proof of ii) is similar as [[MATH/Cards/Nodes/a Lemma of Cohomology\|a Lemma of Cohomology]].

> [!theorem]
> Hall subgroups are conjugate if $G$ is solvable.

**_Proof._**
Let $G$ be a solvable group. Let $M\lhd G$ such that $|G/M|$ is a prime $p$. The existence of $M$ is guaranteed by the [[MATH/Cards/Nodes/Composition Series\|composition series]] of $G$. Let $H,K$ be Hall $\pi$-subgroups of $G$. If $p\notin\pi$, then $H,K\leqslant M$ and $H,K$ are conjugation by induction. If $p\in\pi$, then $H\cap M$, $K\cap M$ are Hall $\pi$-subgroups of $M$. By induction hypothesis, there is a $x\in M$ such that $(H\cap M)^x=K\cap M$. 

WLOG we may assume that Hall $\pi$-subgroups $H$ and $K$ satisfies $H\cap M=K\cap M$. It suffices to show $H$ and $K$ are conjugate. Let $L=\left\langle H,K\right\rangle$. If $L<G$, then by induction hypothesis, $H$ and $K$ are Hall $\pi$-subgroups of $L$ and so they conjugate in $L$. Then we suppose that $L=G$, that is, $G=\left\langle H,K\right\rangle$. 

Let $N:=H\cap M$. Note that $N$ is a normal subgroup of $G$. Since $H/N$ and $K/N$ are Hall subgroups of $G/N$, by induction hypothesis, we have a $\overline g\in G/N$ such that $(H/N)^{\overline g}=K/N$. As $H/N\cong \mathbb{Z}_p$, there is a $h\in H$ such that $H=\left\langle N,h\right\rangle$. Let $k=h^g$ for some preimage of $\overline g$ under $G\to G/N$. Then by $K/N\cong \mathbb{Z}_p$, we have $K=\left\langle N,k\right\rangle$ and so $H^g=K$. Therefore, $H$ and $K$ are conjugate.
<p align="left">□</p>

> [!theorem]
> Let $G$ be a finite solvable group and $\pi$ be any set of primes. Then any subgroup whose order is a product of primes in $\pi$ is contained in some Hall $\pi$-subgroup.

**_Proof._**
Suppose $H\leqslant G$ is a $\pi$-subgroup of $G$ and $K$ is a Hall $\pi$-subgroup of $G$. Note that 

$$|H|/|H\cap K|=|H|/(|H||K|/|HK|)=|HK|/|K|\mbox{ is a divisor of $|G|/|K|$},$$

we have that $\gcd(|H|/|H\cap K|,|H\cap K|)=1$. So if $H\cap K\neq 1$, then $H\cap K$ is a Hall $\pi$-subgroup of $H$. Since the Hall $\pi$-subgroup of $H$ is itself, there is $H\cap K=H$ and $K\geqslant H$. Therefore, if $H$ is not contained in any Hall $\pi$-subgroup, then $H\cap K=1$ for all Hall $\pi$-subgroup $K$. 

Take a prime $p\in\pi$. Let $P$ be a Sylow $p$-subgroup of $H$, and let $P_K$ be a Sylow $p$-subgroup of Hall $\pi$-subgroup $K$. As $P_K$ is a Sylow $p$-subgroup of $G$, then there exists a $g\in G$ such that $P\leqslant P_K^g$. Then $K^g$ is a Hall $\pi$-subgroup and $K^g\cap H\geqslant P$, contradiction. 
<p align="left">□</p>

