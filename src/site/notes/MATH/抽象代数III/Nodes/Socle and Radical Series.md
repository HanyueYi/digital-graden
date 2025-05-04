---
{"dg-publish":true,"draft":false,"permalink":"/MATH/抽象代数III/Nodes/Socle and Radical Series/","dgPassFrontmatter":true}
---


> [!proposition]
> Let $A$ be an Artinian ring, and let $U$ be a finitely generated $A$-module. 
> - TFAE for an $A$-submodule of $U$:
> 	- $V=\mathrm{Rad}U$
> 	- $V$ is the smallest submodule of $U$ with semisimple quotient. 
> 	- $J(A)U=V$
> - TFAE for an $A$-submodule of $U$:
> 	- $V=\mathrm{soc} U$
> 	- $V$ is the largest semisimple submodule of $U$
> 	- $V=\{u\in U:J(A)u=0\}$.
{ #045478}


**_Proof._**
(1) iii)->ii) Let $V=J(A)U$, then $U/V$ is an $A/J(A)$-module by [[MATH/抽象代数III/Nodes/Module Constructions and Universal Properties#^xy300k\|Module Constructions and Universal Properties#^xy300k]]. Since $A$ is Artinian, we know $A/J(A)$ is semisimple by [[MATH/抽象代数III/Nodes/Socle and Radical of Module#^r8oe32\|Socle and Radical of Module#^r8oe32]]. Since $U/V$ is a finitely generated $A/J(A)$-module, $U/V$ is also semisimple because $(A/J(A))^n\twoheadrightarrow U$ for some $n$ and $U$ is a quotient module of semisimple $(A/J(A))^n$. To show $V$ is the smallest submodule, assume that there exists $V'$ with $V'\subseteq V$ and $U/V'$ semisimple. By [[MATH/抽象代数III/Nodes/Annihilator and Jacobson Radical#^p95eh4\|Annihilator and Jacobson Radical#^p95eh4]] i), we know $J(A)(U/V')=0$ and $V=J(A)U\subseteq V'$. It deduces that $V=V'$ and we finish the proof. 

ii)->i) By [[MATH/抽象代数III/Nodes/Socle and Radical of Module#^r8oe32\|Socle and Radical of Module#^r8oe32]].

i)->iii) It suffices to show $J(A)U=\mathrm{Rad}U$. Since $U/\mathrm{Rad}U$ is semisimple, $J(A)(U/\mathrm{Rad} U)=0$ and so $J(A)U\subseteq \mathrm{Rad}U$. On the other hand, since $U/J(A)U$ is a finitely generated $A/J(A)$-module and so is semisimple, we know $J(A)U\supseteq \mathrm{Rad}U$. Therefore, $J(A)U=\mathrm{Rad}U$. 

(2) By definition of [[MATH/抽象代数III/Nodes/Socle and Radical of Module#^4du342\|socle]], i) and ii) are equivalent. By [[MATH/抽象代数III/Nodes/Annihilator and Jacobson Radical#^p95eh4\|Annihilator and Jacobson Radical#^p95eh4]] i), $\mathrm{soc}U\subseteq \{u\in U:J(A)u=0\}$ is trivial. Conversely, notice that $W:=\{u\in U:J(A)u=0\}$ is the largest submodule of $U$ annihilated by $J(A)$. Thus $W$ is a $A/J(A)$-module and so it is semisimple $A$-module. Thus $W\subseteq\mathrm{soc} U$ by definition. Now we finish the proof. 
<p align="left">□</p>


> [!definition]
> Let $U$ be a finitely generated $A$-module with $A$ Artinian. Define inductively 
> - $\mathrm{Rad}^n(U)=\mathrm{Rad}(\mathrm{Rad}^{n-1}(U))$, and 
> - $\mathrm{soc}^n(U)/\mathrm{soc}^{n-1}(U)=\mathrm{soc}(U/\mathrm{soc}^{n-1}(U))$.
> 
> By [[MATH/抽象代数III/Nodes/Socle and Radical Series#^045478\|#^045478]], we have $\mathrm{Rad}^n(U)=J(A)^nU$ and $\mathrm{soc}^n(U)=\{u\in U:J(A)^nu=0\}$. Then define chains of submodules:
> - $\mathrm{Rad}^0(U)\supseteq \mathrm{Rad}(U)\supseteq\cdots$ is called radical series/Loewy series.
> - $0\subseteq \mathrm{soc}(U)\subseteq\mathrm{soc}^2(U)\subseteq\cdots$ is called socle series. 
>   
> Furthermore, we call $\mathrm{Rad}^{n-1}U/\mathrm{Rad}^{n}U$ radical layer/Loewy layer, and call $\mathrm{soc}^n(U)/\mathrm{soc}^{n-1}(U)$ socle layer.


> [!lemma]
> $\mathrm{Rad}^n(U\oplus V)=\mathrm{Rad}^n(U)\oplus \mathrm{Rad}^n(V)$.
> $\mathrm{soc}^n(U\oplus V)=\mathrm{soc}^n(U)\oplus \mathrm{soc}^n(V)$.


> [!theorem]
> Let $A$ be an Artinian ring, and let $U$ be a finitely generated $A$-module. The radical series of $U$ is the fastest descending series of submodules of $U$ with semisimple quotient, and the socle series of $U$ is the fastest ascending series with semisimple quotient. 
> 
> The two series terminate. If $m$ and $n$ are the minimal integer with $\mathrm{Rad}^mU=0$ and $\mathrm{soc}^nU=U$, then $m=n$.
{ #5ypk5s}


**_Proof._**
Suppose that $\cdots\subseteq U_2\subseteq U_1\subseteq U_0=U$ is a series of submodules of $U$ with semisimple quotient. We show by induction on $r$ such that $\mathrm{Rad}^r(U)\subseteq U_r$. We prove it by induction. When $r=0$, it is trivial. Now assume that $\mathrm{Rad}^{r-1}(U)\subseteq U_{r-1}$. Then we have 

$$\mathrm{Rad}^{r-1}(U)/(\mathrm{Rad}^{r-1}(U)\cap U_r)\simeq \mathrm{Rad}^{r-1}(U)+U_r/U_r\subseteq U_{r-1}/U_r$$

is semisimple and so $\mathrm{Rad}^{r-1}(U)\cap U_r\supseteq \mathrm{Rad}(\mathrm{Rad}^{r-1}(U))=\mathrm{Rad}^r(U)$. Similarly, we can prove the case of socle.

Since $A$ is an Artinian ring, its Jacobson radical $J(A)$ is nilpotent by [[MATH/抽象代数III/Nodes/Annihilator and Jacobson Radical#^a43f1d\|Annihilator and Jacobson Radical#^a43f1d]]. Let $k \geqslant 1$ be an integer such that $J(A)^k = 0$. Then $\mathrm{Rad}^k(U) = J(A)^k U = 0 \cdot U = 0$. And $\mathrm{soc}^k(U) = \{u \in U \mid J(A)^k u = 0\} = \{ u \in U \mid 0 \cdot u = 0 \} = U$. Thus, both series terminate in at most $k$ steps.

Let $m$ be the minimal integer such that $\mathrm{Rad}^m(U) = 0$, and let $n$ be the minimal integer such that $\mathrm{soc}^n(U) = U$. 
- Show $m \leqslant n$: Consider the socle series $0=V_0 \subset V_1 \subset \dots \subset V_n = U$, where $V_i = \mathrm{soc}^i(U)$. Define a descending series $U_i = V_{n-i}$ for $0 \leqslant i \leqslant n$. Then $U=U_0 \supset U_1 \supset \dots \supset U_n = 0$, and the quotients $U_{i-1}/U_i = V_{n-i+1}/V_{n-i}$ are semisimple. We have proved that $\mathrm{Rad}^r(U) \subseteq U_r$ for all $r \le n$. Setting $r=n$, we get $\mathrm{Rad}^n(U) \subseteq U_n = V_0 = 0$. Since $\mathrm{Rad}^n(U)=0$ and $m$ is the minimal such integer, we must have $m \leqslant n$. 
- Show $n \leqslant m$: Consider the radical series $U=W_0 \supset W_1 \supset \dots \supset W_m = 0$, where $W_i = \mathrm{Rad}^i(U)$. Define an ascending series $V_i = W_{m-i}$ for $0 \leqslant i \leqslant m$. Then $0=V_0 \subset V_1 \subset \dots \subset V_m = U$, and the quotients $V_i/V_{i-1} = W_{m-i}/W_{m-i+1}$ are semisimple. Recall that $V_r \subseteq \mathrm{soc}^r(U)$ for all $r \leqslant m$. Setting $r=m$, we get $V_m = W_0 = U \subseteq \mathrm{soc}^m(U)$. Since $\mathrm{soc}^m(U)=U$ and $n$ is the minimal such integer, we must have $n \le m$. 

Combining $m \leqslant n$ and $n \leqslant m$, we conclude $m=n$.
<p align="left">□</p>


> [!lemma]
> - Let $A$ be a semisimple ring, then $A$ is Artinian iff it is Noetherian. 
> - If $A$ is Artinian ring, then it is Noetherian. 
{ #u3of0p}


**_Proof._**
i) is easy.

ii) For the left $A$-module ${}_A A$, we have $J^{n+1}=J(J^n)=\mathrm{Rad}(J^n)$ and so $J^n/J^{n+1}$ is semisimple. To show $A$ is Noetherian, as $A/J$ is Noetherian, it suffices to show $J$ is Noetherian. As $J/J^2$ is Noetherian, it suffices to show $J^2$ is Noetherian. Repeat this procedure, and finitely it suffices to show $J^r=0$ is Noetherian. Now we finish the proof. 
<p align="left">□</p>

