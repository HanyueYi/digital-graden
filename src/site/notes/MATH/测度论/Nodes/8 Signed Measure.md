---
{"dg-publish":true,"permalink":"/MATH/测度论/Nodes/8 Signed Measure/","dgPassFrontmatter":true}
---


> [!definition]
> Let $\mathcal{A}$ be a $\sigma$-algebra. A *signed measure* is a function $\mu: \mathcal{A} \rightarrow$ $(-\infty, \infty]$ such that
> - $\mu(\emptyset)=0$;
> - if $A_1, A_2, \ldots$ are pairwise disjoint and all the $A_i$ are in $\mathcal{A}$, then $\mu\left(\cup_{i=1}^{\infty} A_i\right)=$ $\sum_{i=1}^{\infty} \mu\left(A_i\right)$.

**Remark.** 
- For any $\{A_i\}_{i=1}^\infty$, either $\{\mu(A_i)\}$ is absolutely convergent, or $\sum\mu(A_i)=\infty$.
- For example, suppose $f$ is an integrable function, then $\mu(A):=\int_A f$ is a signed measure.


> [!proposition]
> The followings hold.
> - Let $\mu$ be a signed measure on a measurable space $(X, \mathcal{A})$. As in the case of measure, if $\left\{A_j\right\}_{j=1}^{\infty} \subset \mathcal{A}$ and $A_j \uparrow \cup_{j=1}^{\infty} A_j$, then $\mu\left(\cup_{j=1}^{\infty} A_j\right)=\lim _{j \rightarrow \infty} \mu\left(A_j\right)$. Similarly, if $\left\{A_j\right\}_{j=1}^{\infty} \subset \mathcal{A}$ and $A_j \downarrow \cap_{j=1}^{\infty} A_j, \mu\left(A_1\right)<\infty$, then $\mu\left(\cap_{j=1}^{\infty} A_j\right)=$ $\lim _{j \rightarrow \infty} \mu\left(A_j\right)$.
> - A signed measure $\mu$ on a measurable space $(X, \mathcal{A})$ is said to be finite if $\mu(X)<$ $\infty$ and it is said to be $\sigma$-finite if there exists a sequence of sets $\left\{A_j\right\}_{j=1}^{\infty} \subset \mathcal{A}$ such that $X=\cup_{j=1}^{\infty} A_j$ and $\mu\left(A_j\right)<\infty$ for every $j$.
> - Note that if $\mu$ is a signed measure, then $\mu\left(\cup_{i=1}^{\infty} A_i\right)=\lim _{n \rightarrow \infty} \mu\left(\cup_{i=1}^n A_i\right)$.

# Positive/Negative Set and Hahn Decomposition Theorem

> [!definition]
> Let $\mu$ be a signed measure. 
> - A set $A \in \mathcal{A}$ is called a *positive set* for $\mu$ if $\mu(B) \geqslant 0$ whenever $B \subset A$ and $B \in \mathcal{A}$. 
> - We say $A \in \mathcal{A}$ is a *negative set* if $\mu(B) \leqslant 0$ whenever $B \subset A$ and $B \in \mathcal{A}$. 
> - A *null set* $A$ is one where $\mu(B)=0$ whenever $B \subset A$ and $B \in \mathcal{A}$.


> [!lemma]
> Let $\mu$ be a signed measure which takes values in $(-\infty, \infty]$. Let $E$ be measurable with $\mu(E)<0$. Then there exists a measurable subset $F$ of $E$ that is a negative set with $\mu(F)<0$.
{ #6e1e47}


**_Proof._**
Assume that $E$ is not a negative set, then there exists $E_1\subseteq E$ such that $\mu(E_1)>0$ and $\mu(E_1)\geqslant\frac{1}{n_1}$ where $n_1$ is the smallest positive integer with this property. If $F_1=E-E_1$ is a negative set, then $F_1$ is the designed set. 

Otherwise, assume that $F_1$ is not a negative set, then there exists $E_2\subseteq F_1$ such that $\mu(E_2)\geqslant\frac{1}{n_2}$ where $n_2$ is the smallest positive integer with this property. Assume $F_k=E-\cup_{i=1}^k E_i$ is not negative, there exists $E_{k+1}\subseteq E$ such that $\mu(E_{k+1})\geqslant\frac{1}{n_{k+1}}$ where $n_{k+1}$ is the smallest positive integer with this property. 

Let $F=E-\cup_{k=1}^\infty E_k$. We claim that $F$ is a negative set with $\mu(F)<0$. Note that

$$-\infty<\mu(F)=\mu(E)-\sum_{k=1}^\infty\mu(E_k)\leqslant\mu(E)-\sum_{k=1}^\infty\frac{1}{n_k}<0$$

yields that $\sum_{k=1}^\infty\frac{1}{n_k}<\infty$. It follows that $\lim_{n\to\infty}n_k=\infty$. 

If $n_k>1$, then for any measurable set $G\subseteq F_{k-1}$, $\mu(G)<\frac{1}{n_k-1}$. Hence, for all $H\subseteq F$, we have that $H\subseteq F_{k-1}$ for all $k\in \mathbb{N}_+$ and so $\mu(H)<\frac{1}{n_k-1}$ for all big enough $k\in \mathbb{N}_+$. Take $k\to\infty$, there is $\mu(H)\leqslant 0$. Now we finish the proof.
<p align="right">□</p>


> [!theorem] Hahn decomposition theorem
> Let $\mu$ be a signed measure taking values in $(-\infty, \infty]$.
> - There exist disjoint measurable sets $E$ and $F$ in $\mathcal{A}$ whose union is $X$ and such that $E$ is a negative set and $F$ is a positive set.
> - If $E_0$ and $F_0$ are another such pair, then $E \Delta E_0=F \Delta F_0$ is a null set with respect to $\mu$.
> - If $\mu$ is not a positive measure, then $\mu(E)<0$. If $-\mu$ is not a positive measure, then $\mu(F)>0$.
> 
> Remark. We write $A\Delta B$ for $(A-B)\cup (B-A)$.

**_Proof._**
i) Assume that there exists measurable set with negative measure. Let $\mathcal F=\{A\in\mathcal{A}:A \mbox{ is a negative set}\}$. Let $L=\inf_{A\in\mathcal{A}}\mu(A)<0$. Let $\{A_i\}\subseteq\mathcal F$ with $\mu(A_i)\to L$. Let $B_n=A_n-\cup_{i=1}^{n-1}A_i$. Then $B_i$ is a negative set and $B_i\cap B_j=\emptyset$. Define $A=\cup_{i=1}^\infty A_i=\cup_{i=1}^\infty B_i$. For any $C\subseteq A$, $\mu(C)=\sum_{n=1}^\infty\mu(B_n\cap C)<0$ and so $A\in\mathcal F$. Note that 

$$L\leqslant\mu(A)=\mu(A\setminus A_n)+\mu(A_n)\leqslant\mu(A_n)\to L\mbox{ as }n\to\infty.$$

Therefore, $\mu(A)=L$. 

Let $E=A$ and $F=E^c$. Then $E,F$ is a partition of $X$. Now we claim that $F$ is a positive set. Otherwise, there is $G\in\mathcal{A}$ such that $\mu(G)<0$. By [[#^6e1e47]], we can assume $G$ is a negative set and then $\mu(E\cup G)<\mu(E)$, which is a contradiction. 

ii) If $E_0,F_0\in\mathcal{A}$ with $E_0,F_0$ another pair, then $E-E_0=F_0-F$ and $E_0-E=F-F_0$. Thus $E\Delta E_0=F\Delta F_0$. Let $A\subseteq E-E_0=F_0-F$. It follows that $\mu(A)\geqslant 0$, $\mu(A)\leqslant 0$ and so $\mu(A)=0$. Therefore, $E\cap E_0$ is null.

iii) If $\mu$ is not a positive measure and $\mu(E)=0$, for any $A\in\mathcal{A}$, $\mu(A)=\mu(A\cap E)+\mu(A\cap F)=\mu(A\cap F)\geqslant 0$, which contradicts with $\mu$ not positive.
<p align="right">□</p>


# Jordan Decomposition Theorem

> [!definition]
> We say two measures $\mu$ and $\nu$ are *mutually singular* if there exist two disjoint sets $E$ and $F$ in $\mathcal{A}$ whose union is $X$ with $\mu(E)=\nu(F)=0$. This is often written as $\mu \perp \nu$.


> [!theorem] Jordan Decomposition Theorem
> If $\mu$ is a signed measure on a measurable space $(X, \mathcal{A})$, there exist positive measures $\mu^{+}$and $\mu^{-}$such that $\mu=\mu^{+}-\mu^{-}$and $\mu^{+}$and $\mu^{-}$are mutually singular. This decomposition is unique.

**_Proof._**
i) Let $E,F\in\mathcal{A}$ be a partition of $X$ where $E$ is negative of $\mu$ and $F$ is positive of $\mu$. Define $\mu^+,\mu^-$ by $\mu^+(A)=\mu(A\cap F)$ and $\mu^-(A)=\mu(A\cap E)$. Then $\mu^+\bot\mu^-$. 

ii) Assume that $\mu=\mu^+-\mu^-=\nu^+-\nu^-$ with $\mu^+\bot\mu^-$ and $\nu^+\bot\nu^-$, and assume that $E_0,F_0$ with $\nu^+(E_0)=\nu^-(F_0)=0$. For any $A\in\mathcal{A}$ with $A\subseteq E_0$, note that 

$$\mu(A)=\nu^+(A)-\nu^-(A)=0-\nu^-(A)\leqslant 0.$$

If $A\in\mathcal{A}$ with $A\subseteq F_0$, then $\mu(A)\geqslant 0$. Hence $E_0, F_0$ give another Hahn-decomposition of $\mu$ and so $E\Delta E_0=F\Delta F_0$ is null. For any $A\in\mathcal{A}$, $\nu^+(A)=\nu^+(A\cap F_0)+\nu^+(A\cap E_0)=\nu ^+(A\cap F_0)$ and so $\mu(A\cap F_0)=\nu^+(A)$. Further, $\mu^+(A)=\mu(A\cap F_0)$ and it follows that $\nu^+=\mu^+$ for any $A\in\mathcal{A}$. 
<p align="right">□</p>


**Remark.** Since $\mu$ takes values in $(-\infty, \infty]$, from the construction of $\mu^{ \pm}$in the proof of Theorem 9.7, we know that $\mu^{-}$ is a finite measure. Thus if $\mu$ is a finite (respectively, $\sigma$-finite), then the same is true for $\mu^{ \pm}$.

# Absolutely Continuous

> [!definition]
> A measure $\nu$ is said to be *absolutely continuous* with respect to a measure $\mu$ if $\mu(A)=0 \Rightarrow \nu(A)=0$. In this case, we write $\nu\ll \mu$. 


> [!lemma]
> Let $\nu$ be a finite measure. Then $\nu$ is absolutely continuous with respect to $\mu$ if and only if for all $\epsilon>0$ there exists $\delta>0$ such that $\mu(A)<\delta$ implies $\nu(A)<\epsilon$.

**_Proof._**
One direction is easy. Otherwise, assume that there exists $\epsilon_0>0$ such that for and $\delta>0$, there is $A$ with $\mu(A)<\delta$ and $\nu(A)\geqslant\epsilon_0$. By taking $\delta=1/2^k$, there is $A_k$ such that $\mu(A_k)<1/2^k$ and $\nu(A_k)\geqslant\epsilon$. It follows that $E=\cap_{n=1}^\infty\cup_{k=n}^\infty A_k$ satisfies $\mu(E)=0$ and $\nu(E)\geqslant\epsilon_0$, which is a contradiction.
<p align="right">□</p>


# Radon-Nikodym Theorem

> [!proposition]
> Let $\mu$ and $\nu$ be finite positive measures on a measurable space $(X, \mathcal{A})$. Then either $\mu \perp \nu$ or else there exist $\epsilon>0$ and $G \in \mathcal{A}$ such that $\mu(G)>0$ and $G$ is a positive set for $\nu-\epsilon \mu$.
{ #37ff4c}


**_Proof._**
Consider $\nu-\frac{1}{n}\mu$. Let $E_n,F_n\in \mathcal{A}$ such that $E_n\cap F_n=\emptyset$, $E_n\cup F_n=X$, where  $E_n$ is negative for $\nu-\frac{1}{n}\mu$ and $F_n$ is positive for $\nu-\frac{1}{n}\mu$. Let $E=\cap _{n=1}^\infty E_n$, and let $F=\cup_{n=1}^\infty F_n$. Then $E^c=F$ and $(\nu-\frac{1}{n}\mu)(E_n)\leqslant 0$ for all $n$. It follows that $\nu(E_n)\leqslant\frac{1}{n}\mu(E_n)\leqslant\frac{1}{n}\mu(X)$ and so $\nu(E)\leqslant\nu(E_n)\to 0$ as $n\to\infty$. Therefore, $\nu(E)=0$. 
- if $\mu(E^c)=\mu(F)=0$, then $\nu\bot\mu$.
- if $\mu(F)>0$, then there exists $n$ with $\mu(F_n)>0$. Let $\epsilon=\frac{1}{n}$, and let $G=F_n$. Then $\mu(G)>0$ and so $G$ is positive of $\nu-\epsilon\mu$.

Now we finish the proof.
<p align="right">□</p>


> [!theorem] Radon-Nikodym theorem
> Suppose $\mu$ and $\nu$ are $\sigma$-finite positive measures on a measurable space $(X, \mathcal{A})$ such that $\nu$ is absolutely continuous with respect to $\mu$. Then there exists a $\mu$-measurable non-negative function $f$ such that
> 
> $$
> \nu(A)=\int_A f d \mu
> $$
> 
> for all $A \in \mathcal{A}$. Moreover, if $g$ is another such function, then $f=g$ almost everywhere with respect to $\mu$.
{ #bdb1bb}


**_Proof._**
i) Uniqueness. If $g,f\geqslant 0$ satisfy the same condition, then $\int_A(f-g)d\mu=0$ for all $A\in\mathcal{A}$. Thus, $f=g$ almost everywhere with respect to $\mu$.

ii) Let $\mu,\nu$ be finite. Let $\mathcal J=\{f:f\geqslant 0\mbox{ measurable},\nu(A)\geqslant\int_A fd\mu,\forall A\in\mathcal{A} \}$. Since $0\in\mathcal J$, $\mathcal J\neq \emptyset$. Let $L=\sup_{g\in\mathcal J}\int_Xgd\mu$. Let $\{g_n\}\subseteq\mathcal J$. We need only to consider $h_2$. Since $h_2=\max{g_1,g_2}$, for any $A\in\mathcal{A}$, consider $A_1=\{x\in A:g_1(x)\geqslant g_2(x)\}$ and $A_2=\{x\in A:g_1(x)<g_2(x)\}$. Since 

$$\int_A h_2 d\mu=\int_{A_1} g_1 d\mu+\int_{A_2} g_2d\mu\leqslant \nu(A_1)+\nu(A_2)=\nu(A),$$

we have that $h_2\in\mathcal J$. Note that $h_n\uparrow h$, so we have that $\int_X g_nd\mu\leqslant \int_X h_nd\mu\leqslant\int_X hd\mu$. Take $n\to\infty$, then $L\leqslant\int_X hd\mu\leqslant L$. Therefore, $\int_X hd\mu=L$, i.e. there exists $f\in\mathcal J$ such that $\int_X fd\mu=L=\sup_{g\in \mathcal J}\int_x gd\mu$. 

Consider $\lambda(A)=\nu(A)-\int_X fd\mu$, then $\lambda$ is a positive measure on $(X,\mathcal{A})$. By [[#^37ff4c]], one of the following holds:
- $\lambda\bot\mu$ 
- there exists $G\in \mathcal{A}$, $\epsilon>0$ such that $\mu(G)>0$ and $G$ is a positive set of $\lambda-\epsilon \mu$. 

If the second case is true, then for any $A\in\mathcal{A}$, there is

$$\nu(A)-\int_A fd\mu=\lambda(A)\geqslant\lambda(A\cap G)\geqslant\epsilon\mu(G\cap A)=\int_A\epsilon \chi_Gd\mu$$

and $\nu(A)\geqslant \int_A(f+\epsilon \chi_G)d\mu$. Therefore, $f+\epsilon \chi_G\in\mathcal J$. However, $\int_X(f+\epsilon \chi_G)d\mu=L+\epsilon\mu(G)>L$, which is a contradiction.

It deduces that $\lambda\bot\mu$. Therefore, there exists $H,H^c\in\mathcal{A}$ such that $\lambda(H)=\mu(H^c)=0$ and $\lambda(H^c)=\nu(H^c)-\int_{H^c} fd\mu=0-0=0$. Therefore, $\nu(A)=\int_Afd\mu$ for all $A\in\mathcal{A}$. 

iii) Let $\mu,\nu$ be $\sigma$-finite. There exists measurable $X_n$ with $X_n\uparrow X$ such that $\mu(X_n)<\infty$ and $\nu(X_n)<\infty$. By ii), there exists $f_n$ such that $\nu(A)=\int_A f_nd\mu$ for any $A\subseteq X_n$ and $A\in\mathcal{A}$. Note that $f_{n+1}=f_n$ on $X_n$ almost everywhere. Define $f: X\to[0,\infty]$ by $f|_{X_n}=f_n$. It is easy to show that $f$ is measurable. Furthermore, note that

$$\nu(A)=\lim_{n\to\infty}\nu(A\cap X_n)=\lim_{n\to\infty}\int_{A\cap X_n}f_n=\lim_{n\to\infty}\int_Af\chi_{X_n}d\mu=\int_Afd\mu.$$

Now we finish the proof.
<p align="right">□</p>


**Remark.** The hypothesis that $(X,\mathcal{A},\mu)$ is $\sigma$-finite cannot be removed, see [[Measure  Theory    (Xia).pdf#page=51&selection=430,0,430,12|here]].


> [!definition]
> Let $(X, \mathcal{A})$ be a measurable space and $\mu$ and $\nu$ be signed measures on $X$. We say that $\nu$ is absolutely continuous with respect to $\mu$ if $|\mu|(A)=$ $0 \Rightarrow \nu(A)=0$. In this case, we also write $\nu \ll \mu$.


> [!theorem] Radon-Nikodym
> Let $(X, \mathcal{A}, \mu)$ be a $\sigma$-finite measure space and $\nu$ be a $\sigma$-finite signed measure defined on $\mathcal{A}$ such that $\nu \ll \mu$. Then, there exists a measurable function $f$ defined on $X$ such that
> 
> $$
> \nu(A)=\int_A f d \mu
> $$
> 
> for every $A \in \mathcal{A}$. The function $f$ is unique in the sense that if $g$ is any real-valued measurable function on $X$ with $\nu(A)=\int_A g d \mu$ for all $A \in \mathcal{A}$, then $f=g$ a.e. respect to $\mu$.

**_Proof._**
Let $\nu=\nu^+-\nu^-$ be the Jordan decomposition of $\nu$, i.e. there exists $E,F\in\mathcal{A}$ such that $\nu^+(E)=\nu^-(F)=0$, $E\cap F=\emptyset$ and $E\cup F=X$. Note that $\nu^-$ is finite and $\nu^+$ is $\sigma$-finite. If $|\mu|(A)=0$, then $|\mu|(A\cap F)=0$, $|\mu|(A\cap E)=0$ and $\nu(A\cap F)=\nu(A\cap E)=0$. It follows that $\nu^+\ll\mu$ and $\nu^-\ll \mu$. By [[#^bdb1bb]], there exists $f_1,f_2$ such that $\nu^+(A)=\int_A f_1d\mu$ and $\nu^-(A)=\int_A f_2d\mu$ for all $A\in\mathcal{A}$. Let $f=f_1-f_2$. 

Consider the decomposition $f=f^+-f^-$, and we claim that $f^+\leqslant f_1$ and $f^-\leqslant f_2$. If $f(x)> 0$, then $f^+(x)=f(x)\leqslant f_1(x)$. If $f(x)\leqslant 0$, then $0=f^+(x)\leqslant f_1(x)$. Thus $f^+(x)\leqslant f_1(x)$. If $f(x)\leqslant 0$, then $f^-(x)=-f(x)=f_2(x)-f_1(x)\leqslant f_2(x)$. Thus $f^-(x)\leqslant f_2(x)$ for all $x\in X$. Now we prove the claim. With this claim and $\nu^-(X)<\infty$, we deduce that$\int_X f^-d\mu\leqslant\int_X f_2d\mu<\infty$ and so $\int_Xfd\mu$ is well-defined.

Note that $\int_A f^++f_2=\int_A f_1+f^-$, it follows that 

$$\int_A fd\mu=\int_A f_1d\mu-\int_A f_2d\mu=\nu^+(A)-\nu^-(A)=\nu(A)$$

and so $f$ is the function we desire.
<p align="right">□</p>
