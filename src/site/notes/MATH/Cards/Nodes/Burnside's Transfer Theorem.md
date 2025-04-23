---
{"dg-publish":true,"aliases":["Burnside's transfer theorem"],"permalink":"/MATH/Cards/Nodes/Burnside's Transfer Theorem/","dgPassFrontmatter":true}
---


> [!definition] transfer
> Let $H<G$ be a subgroup and $\Omega=[G:H]=\{Hx_1,\cdots,Hx_n\}$. Define $\hat g:Hx\mapsto Hxg$ and $\tau_g\in\mathrm{Sym}(n)$ be the permutation induced from $\hat g$. Since $Hx_ig=Hx_{i^{\tau(g)}}$, we have that $x_igx_{i^{\tau(g)}}^{-1}\in H$. 
> 
> Define $h_i(g)=x_igx_{i^{\tau(g)}}^{-1}$, and define
> 
> $$\begin{aligned}
> V_{G\to H}:G&\to H/H',\\
> g&\mapsto \big(\Pi_{i=1}^nh_i(g)\big)H'
> \end{aligned}$$
> 
> as a *transfer* from $G$ to $H/H'$.

**Observation.** 
- $V_{G \rightarrow H}$ is a homomorphism from $G$ to $H / H^{\prime}$;
- $V_{G \rightarrow H}$ does not depend on the choices of $x_1, \cdots, x_n$;
- Writing $\hat{g}$ in cycle form $\left(H x_1, H x_1 g, \cdots, H x_1 g^{l_1-1}\right)\left(H x_2, H x_2 g, \cdots, H x_2 g^{l_1-2}\right) \cdots\left(H x_t, \cdots, H x_t g^{l_t-1}\right)$, then there is $V_{G \rightarrow H}(g)=\Pi_{i=1}^n\left(x_i g^{l_i} x_i^{-1}\right) H$. 

> [!definition] p-nilpotent
> A group $G$ is called *$p$-nilpotent* if $G=NP$, where $N\lhd G$ and $P$ is a Sylow $p$-subgroup, and $N\cap P=1$.

> [!theorem] Burnside's transfer theorem
> Let $G$ be a finite group, and let $P$ be a Sylow $p$-subgroup. If $N_G(P)=C_G(P)$, then $G$ is $p$-nilpotent.

**_Proof._**
Since $N_G(P)=C_G(P)\geqslant P$, then $P$ is abelian and $P'=1$. 

Since $V_{G\to P}(g)=\Pi_{i=1}^tx_ig^{l_i}x_i^{-1}=\Pi_{i=1}^tg^{l_1+\cdots+l_t}=g^{|G/P|}$, $V_{G\to P}$ is surjective. So $V_{G\to P}:G\to P$ has kernel $K$ and $G/K\cong P$. So $K\lhd G$ such that $G=KP$ and so $G$ is $p$-nilpotent.
<p align="left">□</p>
# Corollary

> [!theorem]
> Let $G$ be finite of which Sylow subgroups are all cyclic. Let $p$ be the smallest prime divisor of $G$ and let $P$ be a Sylow $p$-subgroup of $G$. Then:
> - $G$ is $p$-nilpotent.
> - $G$ is solvable.
{ #sezt3q}


**_Proof._**
Since $P$ is cyclic and $p$ is the smallest prime divisor, we have that $N_G(P)/C_G(P)\lesssim \mathrm{Aut}(P)$ and $N_G(P)/C_G(P)=1$. So $G$ has a normal subgroup $K$ with $|G/K|=|P|$. Then $K$ is $q$-nilpotent where $q>p$ is the smallest prime divisor of $K$. Repeat this procedure and we get $G\rhd K\rhd K_1\cdots\rhd K_m$. Note that $K_m$ is a Sylow subgroup and $K_i/K_{i+1}$ is solvable. So $G$ is solvable.
<p align="left">□</p>

> [!corollary]
> If a Sylow $2$-group of $G$ is cyclic, then $G$ is solvable.

**_Proof._**
By [[MATH/Cards/Nodes/Burnside's Transfer Theorem#^sezt3q\|#^sezt3q]], $G$ is $2$-nilpotent and so there exists $N\lhd G$ such that $G=NP$ and $|N|$ is odd. By [Feit–Thompson theorem](https://en.wikipedia.org/wiki/Feit–Thompson_theorem), $G$ is solvable.
<p align="left">□</p>

> [!proposition]
> Let $G$ be a finite nonabelian simple group, and let $p$ be the smallest prime divisor of $|G|$. Then $|G|$ is divisible by $p^3$ or $12$.

**_Proof._**
Suppose $|G|$ is not divisible by $p^3$, then $p^2||G|$. Otherwise, a Sylow $p$-subgroup $P=C_p$ and $G$ is $P$-nilpotent, contradiction by $G$ simple. Thus $P$ is cyclic or $P\cong C_p\times C_p$. The first case is impossible. Hence $P\cong C_p\times C_p$ and $N_G(P)\neq C_G(P)$. Further $N_G(P)/C_G(P)\lesssim\mathrm{Aut}(P)=\mathrm{GL}_2(p)$ and $|\mathrm{GL}_2(p)|=p(p-1)^2(p+1)$. Since $p$ is the smallest prime divisor and $G$ is nonsolvable, then $p=2$ and $p+1=3$. It yields that $12\big||G|$.  
<p align="left">□</p>
# Application

> [!proposition]
> Let $|G|=p^2q^n$ with $p<q$ primes. Then $G$ is solvable.

**_Proof._**
Note that $n_q\equiv 1\pmod q$ and $n_q\mid p^2$, we have $n_q=p^2$. Let $P$ be a Sylow $p$-subgroup of $G$. If $N_G(P)/C_G(P)=1$, then $G$ is $p$-nilpotent and so $G$ is solvable. Otherwise $N_G(P)/C_G(P)\leqslant \mathrm{GL}(2,p)$ where $|\mathrm{GL}(2,p)|=(p-1)^2p(p+1)$. Since $p^2\mid |C_G(P)|$, there is $|N_G(P)/C_G(P)|=p+1$ and so $p=2$, $q=3$. Hence $n_3=4$ and so for a Sylow $3$-group $Q$, $G/Q_G\lesssim S_4$. As $Q_G$ is a $q$-group and is solvable, $G$ is solvable.
<p align="left">□</p>


> [!proposition]
> Group of order $2^3\cdot 3^3\cdot 5=1080$ is not simple.

**_Proof._**
Assume that $G$ is simple. Since $6!<1080$, $G$ does not have subgroup of index $\leqslant 6$. Hence $n_5\in\{36,216\}$. If $n_5=216$, $[G:N_G(P)]=216$ and so $N_G(P)=C_G(P)=P$. It deduces that $G$ is $5$-nilpotent, contradiction. Thus $n_5=36$ and $|N_G(P)|=30$. Since $N_G(P)\neq C_G(P)$ and $N_G(P)/C_G(P)\lesssim C_4$, we have $|C_G(P)|=15$ and $C_G(P)$ is cyclic. 

Let $H\leqslant C_G(P)$ be the group of order $3$. We claim that $N_G(P)<N_G(H)$.
- Since $H\,\mathrm{char}\, C_G(P)$ and $C_G(P)\lhd N_G(P)$, there is $H\lhd N_G(P)$. 
- Consider $N_G(H)$. There exists a Sylow $3$-subgroup $Q\geqslant H$. If $H\leqslant Z(Q)$, then $N_G(H)\geqslant Q\geqslant 27$. Otherwise $H\cap Z(Q)=\{1\}$ and $N_G(H)\geqslant\left\langle H,Z(Q)\right\rangle\geqslant 3^2$. Thus $3^2\mid N_G(H)$. 
- As $3^2\not\mid N_G(P)$, $N_G(P)<N_G(H)$.

Since $[N_G(H):N_{N_G(H)}(P)]=[N_G(H):N_G(P)]>1$, the number of Sylow $5$-subgroups of $N_G(H)$ is not equal to $1$. Since $n_5\neq 216$, the number of Sylow $5$-subgroups of $N_G(H)$ is $6$ or $36$. 
- If it equals to $6$, then $|N_G(H)|=6*30=180$ and $[G:N_G(H)]=6$, which is impossible.
- If it equals to $36$, then $N_G(H)=G$ and $H\lhd G$, contradicting with $G$ simple.

Now we finish the proof.
<p align="left">□</p>


> [!proposition]
> Group of order $180$ is not simple.

**_Proof._**
Since $180=2^2*5*9$, we have $n_5\in\{6,36\}$. If $n_5=36$, then $|G:N_G(P)|=36$ and $N_G(P)=5$, where $P$ is a Sylow $5$-subgroup. It deduces that $N_G(P)=C_G(P)=P$ and so $G$ is $5$-nilpotent. Hence $n_5=6$ and $|N_G(P)|=30$. Since $N_G(P)/C_G(P)\lesssim C_4$, we have $|C_G(P)|=15$ and $C_G(P)$ is cyclic. It yields that $G$ has an element of order $15$.

Since $n_5=[G:N_G(P)]=6$, $G\lesssim S_6$ does not have an element of order $15$. Contradiction.
<p align="left">□</p>


> [!proposition]
> Group of order $2^2*3*5*7=420$ is not simple.

**_Proof._**
Assume $G$ is simple. By Sylow's theorem, $n_7=15$. Then $N_G(P)/C_G(P)\lesssim C_6$ and $|N_G(P)|=420/15=28$ yield that $|C_G(P)|=14$. Since $Z(C_G(P))\geqslant P\simeq Z_7$ and $C_G(P)/Z(C_G(P))$ is cyclic, by [[MATH/Cards/Nodes/GZ-Theorem\|GZ-Theorem]] $C_G(P)$ is abelian. It deduces that $C_G(P)$ is cyclic. Assume that $x\in G$ is an element of order $14$. Since $[G:N_G(P)]=15$, there is an injective map $\varphi:G\to S_{15}$. Note that $\varphi(x)$ is a cycle of length $14$, then $\varphi^{-1}(\varphi(G)\cap A_{15})\lhd G$ and so $G$ is not simple.
<p align="left">□</p>


> [!proposition]
> Group of order $264=2^3\cdot 3\cdot 11$ is not simple.

**_Proof._**
Assume $G$ is simple, then $n_{11}=12$. Then $|N_G(P)|=22$ and $N_G(P)/C_G(P)\lesssim C_{10}$ yield that $|C_G(P)|=11$. Thus $C_G(P)=P$. Note that $P$ acting on $\Omega:=\{N_G(P)g:g\in G\}$ has two orbits, as $|\Omega|=12$, $P$ is a $11$-subgroup and $P$ has only one fixed point. Take $x\in N_G(P)\setminus C_G(P)$, then $x$ acts on $\{N_G(P)g:g\in G\}$ has at most $2$ fixed points by [[MATH/Cards/Nodes/Sylow Theorems#^x4xxhg\|Sylow Theorems#^x4xxhg]]. 

Since $o(x)=2$, $\varphi(x)\in \mathrm{Sym}(\Omega)$ is a product of $2$-cycles. Notice that $x\in N_G(P)$ fixes $N_G(P)\in\Omega$ and so $x$ is a product of five $2$-cycles. Therefore, $\varphi(G)\cap A_{12}\neq \varphi(G)$ amd so $G$ has a normal subgroup of index $2$. 
<p align="left">□</p>


