---
{"dg-publish":true,"permalink":"/MATH/测度论/Nodes/4 Outer Measure and Premeasure/","dgPassFrontmatter":true}
---


> [!definition] outer measure
> Let $X$ be a set. An outer measure is a function $\mu^*: \mathcal{P}(X) \rightarrow$ $[0, \infty]$ satisfying
> - $\mu^*(\emptyset)=0$;
> - if $A \subset B$, then $\mu^*(A) \leqslant \mu^*(B)$;
> - $\mu^*\left(\cup_{i=1}^{\infty} A_i\right) \leqslant \sum_{i=1}^{\infty} \mu^*\left(A_i\right)$ whenever $A_1, A_2, \ldots$ are subsets of $X$.


> [!proposition]
> Suppose $\mathcal{C}$ is a collection of subsets of $X$ such that $\emptyset \in \mathcal{C}$ and there exist $D_1, D_2, \ldots$ in $\mathcal{C}$ such that $X=\cup_{i=1}^{\infty} D_i$. Suppose $l: \mathcal{C} \rightarrow[0, \infty]$ with $l(\emptyset)=0$. Define
> 
> $$
> \mu^*(E)=\inf \left\{\sum_{i=1}^{\infty} l\left(A_i\right): A_i \in \mathcal{C} \text { for each } i \text { and } E \subset \bigcup_{i=1}^{\infty} A_i\right\}
> $$
> 
> Then $\mu^*$ is an outer measure.
{ #5cf938}


**_Proof._**
Note that (i), (ii) is easy. So we only need to check (iii). Let $\{A_i\}\subseteq\mathcal{P}(X)$. If $\mu^{*}(A_{i})=\infty$, it is OK. Assume that $\mu^*(A_i)<\infty$ for all $i\in\mathbb{N}$. For any each $i$, any $\epsilon>0$, there exists $\{C_{ij}\}_{j=1}^\infty\subseteq\mathcal C$ such that $\sum_{i=1}^\infty l(c_{ij})\leqslant \mu^{*}(A_i)+\dfrac{\epsilon}{2^i}$. Then $\cup_{i=1}^\infty A_i\subseteq\cup_{i,j}C_{ij}$ and $\mu^{*}(\cup_{i=1}^\infty A_i)\leqslant\sum_{i,j}l(C_{ij})\leqslant\sum_{i=1}^\infty\mu^*(A_i)+\epsilon$. Take $\epsilon\to 0$, then we finish the proof.
<p align="right">□</p>


> [!definition]
> Let $\mu^*$ be an outer measure. A set $A \subset X$ is $\mu^*$-measurable if
> 
> $$
> \mu^*(E)=\mu^*(E \cap A)+\mu^*\left(E \cap A^c\right)
> $$
> 
> for all $E \subset X$.

**Note.** Since $\mu^*(E)\leqslant\mu^*(E\cap A)+\mu^*(E\cap A^c)$ by definition, to verify $A$ is $\mu^*$-measurable, it suffices to show $\mu^*(E)\geqslant\mu^*(E\cap A)+\mu^*(E\cap A^c)$ with $\mu^*(E)$ finite.


> [!theorem]
> If $\mu^*$ is an outer measure on $X$, then:
> - The collection $\mathcal{A}$ of $\mu^*$-measurable sets is a $\sigma$-algebra. 
> - If $\mu$ is the restriction of $\mu^*$ to $\mathcal{A}$, then $\mu$ is a complete measure.
{ #036d19}


**_Proof._**
i) Note that $X,\emptyset\in\mathcal A$, and $A\in\mathcal{A}$ iff $A^c\in\mathcal{A}$.  Let $A,B\in\mathcal{A}$. Aim to show $A\cap B\in\mathcal{A}$. That is, $\mu^*(E)\geqslant\mu^*(E\cap A\cap B)+\mu^*(E\cap(A\cap B)^c)$. Since 

$$\begin{aligned}
\mu^*(E)&\geqslant\mu^*(E\cap A)+\mu^*(E\cap A^c)\\
&\geqslant \mu^*(E\cap A\cap B)+\mu^*(E\cap A\cap B^c)+\mu^*(E\cap A^c)\\
&\geqslant \mu^*(E\cap A\cap B)+\mu^*(E\cap (A^c\cup B^c))\\
&\geqslant \mu^*(E\cap A\cap B)+\mu^*(E\cap(A\cap B)^c),
\end{aligned}$$

then $A\cap B\in\mathcal{A}$. It remains to show that if $\{A_i\}\subseteq\mathcal{A}$ with $A_i\cap A_j=\emptyset$, then $\cup A_i\in\mathcal{A}$. Let $B_n=\cup_{i=1}^nA_i$. Then $\cup_{n=1}^\infty B_n=\cup_{i=1}^\infty A_i=A$. We want to show $\mu^*(E)\geqslant\mu^*(E\cap A)+\mu^*(E\cap A^c)$. Since 

$$\begin{aligned}
\mu^*(E\cap B_n)&\geqslant\mu^*(E\cap B_n\cap A_n)+\mu^*(E\cap B_n\cap A_n^c)\\
&=\mu^*(E\cap A_n)+\mu^*(E\cap B_{n-1})\\
&=\sum_{i=1}^n\mu^*(E\cap A_i).
\end{aligned}$$

Then there is 

$$\mu^*(E)\geqslant\mu^*(E\cap B_n)+\mu^*(E\cap B_n^c)\geqslant\sum_{i=1}^n\mu^*(E\cap A_i)+\mu^*(E\cap A^c).$$

Let $n\to\infty$. Then  

$$\mu^*(E)\geqslant\sum_{i=1}^\infty \mu^*(E\cap A_i)+\mu^*(E\cap A^c)\geqslant\mu^*(E\cap A)+\mu^*(E\cap A^c)\geqslant\mu^*(E).$$

So $\cup_{i=1}^\infty A_i\in\mathcal{A}$. In addition, since $\sum_{i=1}^\infty\mu^*(E\cap A_i)=\mu^*(E\cap A)$ for all $E\subseteq X$. Then if $E=A=\cup A_i$, we have that $\sum_{i=1}^\infty\mu^*(A_i)=\mu^*(A)$. Thus, $\mu^*$ is a measure on $\mathcal{A}$. 

Note that if $A\subseteq X$ with $\mu^*(A)=0$, then for any $E\subseteq X$ there is $\mu^*(A\cap E)=0$ and so $\mu^*(E)\geqslant\mu^*(A^c\cap E)+\mu^*(A\cap E)$ and so $A\in\mathcal{A}$. Thus $\mathcal{A}$ is a complete measure.
<p align="right">□</p>


**Example.** Let $X=\mathbb{R}$ and let $\mathcal{C}$ be the collection of intervals of the form $(a, b]$. Let $l(I)=b-a$ if $I=(a, b]$. Let $\mathcal L$ be the set of $\mu^*$-measurable set, then it is a $\sigma$-algebra, called the Lebesgue $\sigma$-algebra. However, there are subsets in $\mathbb{R}$ which are non-measurable with respect to $\mu^*$ and so $\mu^*$ is not a measure on $\mathcal{P}(\mathbb{R})$. See [[Pasted image 20241003182321.png|here]].

> [!definition] premeasure
> Let $\mathcal{A}_0$ be an algebra. Saying $\mu: \mathcal{A}_0 \rightarrow[0, \infty]$ is a measure on $\mathcal{A}_0$ means the following: $\mu(\emptyset)=0$ and if $A_1, A_2, \ldots$ are pairwise disjoint elements of $\mathcal{A}_0$ and also $\cup_{i=1}^{\infty} A_i \in \mathcal{A}_0$, then $\mu\left(\cup_{i=1}^{\infty} A_i\right)=\sum_{i=1}^{\infty} \mu\left(A_i\right)$. Sometimes one calls a measure on an algebra a premeasure .

> [!theorem] Caratheodory-Hahn
> Suppose $\mathcal{A}_0$ is an algebra on $X$ and $l$ : $\mathcal{A}_0 \rightarrow[0, \infty]$ is a measure. For $E \in \mathcal{P}(X)$, define
> 
> $$
> \mu^*(E)=\inf \left\{\sum_{i=1}^{\infty} l\left(A_i\right): A_i \in \mathcal{A}_0 \text { for each } i \text { and } E \subset \bigcup_{i=1}^{\infty} A_i\right\}
> $$
> 
> Then
> - $\mu^*$ is an outer measure;
> - $\mu^*(A)=l(A)$ if $A \in \mathcal{A}_0$;
> - every set in $\mathcal{A}_0$ is $\mu^*$-measurable;
> - if $l$ is $\sigma$-finite, then $\mu^*$ is a measure on $\sigma\left(\mathcal{A}_0\right)$ which is the unique extension of l to $\sigma\left(\mathcal{A}_0\right)$.

**_Proof._**
i)-iii) are easy. See [[Measure  Theory    (Xia).pdf#page=19&selection=290,0,291,0|here]].

iv) We firstly consider the case of finite measure and then consider the case of $\sigma$-finite.

**Case 1.** Assume that $l$ is finite. Let $\nu$ is a measure on $\sigma(\mathcal{A}_0)$. For any $A\in\sigma(\mathcal{A}_0)$, there is

$$l(X)=\nu(X)=\nu(A)+\nu(A^c)\leqslant\mu^*(A)+\mu^*(A^c)=\mu^*(X)=l(X)$$

and so $\nu(A)=\mu^*(A)$. 

**Case 2.** Assume that $l$ is $\sigma$-finite. Let $\{C_i\}\subseteq\mathcal{A}_0$ such that $C_i\uparrow X$ and $l(C_i)<\infty$. Consider $l_i:\mathcal{A}_0\to[0,\infty),l_i(A)=l(A\cap C_i)$. Let $\nu,\mu$ be measures on $\sigma(\mathcal{A}_0)$ with $\nu=\mu$ on $\mathcal{A}_0$. Define $\mu_i,\nu_i$ as $\nu_i(A)=\nu(A\cap C_i)$ and $\mu_i(A)=\mu(A\cap C_i)$. By Case 1 we have $\nu_i=\mu_i$ for all $A\in\sigma(\mathcal{A}_0)$. Thus $\nu(A)=\lim\nu(A\cap C_i)=\lim\mu(A\cap C_i)=\mu(A)$.  
<p align="right">□</p>

**Remark.** Note that $\mathcal{A}$ defined in [[#^036d19]] is a $\sigma$-algebra and $\mathcal{A}\supseteq\mathcal{A}_0$. Thus $\sigma(\mathcal{A}_0)\subseteq\mathcal{A}$. 