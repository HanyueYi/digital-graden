---
{"dg-publish":true,"permalink":"/MATH/测度论/Nodes/2 Measures/","dgPassFrontmatter":true}
---


> [!definition] measure space
> Let $(X, \mathcal{A})$ be a measurable space, where $X$ is a set and $\mathcal{A}$ is a $\sigma$-algebra on $X$. A *measure* on $(X, \mathcal{A})$ is a function $\mu: \mathcal{A} \rightarrow[0, \infty]$ such that
> - $\mu(\emptyset)=0$;
> - if $\{A_i\}_{i=1}^\infty\subseteq\mathcal A$ are pairwise disjoint, then
> 
> $$
> \mu\left(\cup_{i=1}^{\infty} A_i\right)=\sum_{i=1}^{\infty} \mu\left(A_i\right)
> $$
> 
> The triple $(X, \mathcal{A}, \mu)$ is called a *measure space*.

**Examples.**
- Let $X$ be any set, $\mathcal{A}$ the collection of all subsets of $X$ and let $\mu(A)=$ the number of elements in $A$ if $A$ is finite and $\mu(A)=\infty$ if $A$ is infinite. Then $\mu$ is called counting measure.
- Let $\delta_x(A)=1$ if $x \in A$ and $0$ otherwise. This measure is called Dirac measure at $x$.
- Let $X$ be an uncountable set and $\mathcal{C}$ the collection of those subsets that are either countable or the complement of a countable set. Define $\mu: \mathcal{C} \rightarrow\{0,1\}$ by $\mu(A)=0$ if $A$ is countable and $\mu(A)=1$ if $A$ is uncountable. Then $(X, \mathcal{C}, \mu)$ is a measure space.
- Let $\mathcal{L}$ be the collection of Lebesgue measurable sets of $\mathbb{R}^n$ and $m$ be the Lebesgue measure; the $(\mathbb{R}^n, \mathcal{L}, m)$ is a measure space. Also, $(\mathbb{R}^n, \mathcal{B}(\mathbb{R}^n), m)$ is a measure space.
- Let $X$ be a set that has at least two members, and let $\mathcal{A}=\mathcal{P}(X)$. Define a function $\mu: \mathcal{A} \rightarrow[0, \infty]$ by letting $\mu(A)$ be $1$ if $A \neq \emptyset$ and letting $\mu(A)$ be $0$ if $A=\emptyset$. Then $\mu$ is not a measure.

> [!lemma]
> Let $(X,\mathcal A,\mu)$ be a measure space.
> - (Monotonicity) If $A, B \in \mathcal{A}$ with $A \subset B$, then $\mu(A) \leqslant \mu(B)$;
> - (Subadditivity) If $A_i \in \mathcal{A}$ and $A=\cup_{i=1}^{\infty} A_i$, then $\mu(A) \leqslant \sum_{i=1}^{\infty} \mu\left(A_i\right)$;
> - (Continuity from below) If $A_i \in \mathcal{A}$ and $A_i \uparrow A$, then $\mu(A)=\lim _{i \rightarrow \infty} \mu\left(A_i\right)$;
> - (Continuity from above) Let $A_i \in \mathcal{A}$ and $A_i \downarrow A$. If $\mu\left(A_1\right)<\infty$, then
> 
> $$\mu(A)=\lim _{i \rightarrow \infty} \mu\left(A_i\right)$$

**_Proof._**
i) $B=A\cup(B-A)$. Then $\mu(B)=\mu(A)+\mu(B-A)\geqslant\mu(A)$.

ii) Let $B_1=A_1$, and let $B_i=A_i-\cup_{j=1}^{i-1}A_j$. Then $\{B_i\}_{i=1}^\infty$ are disjoint, and so $\mu(\cup_{i=1}^\infty A_i)=\mu(\cup_{i=1}^\infty B_i)=\sum_{i=1}^\infty\mu(B_i)\leqslant\sum_{i=1}^\infty \mu(A_i)$.

iii) Let $A_0=\emptyset$. Then $\mu(A)=\sum_{i=1}^\infty\mu(A_i-A_{i-1})=\lim_{n\to\infty}\mu(A_n)-\mu(A_{0})=\lim_{n\to\infty}\mu(A_n)$.

iv) Let $B_n=A_1-A_n$. Since $B_n\uparrow A_1-A$, we have $\mu(A_1)-\mu(A)=\mu(A_1-A)=\lim_{n\to\infty}\mu(B_n)=\mu(A_1)-\lim_{n\to\infty}\mu(A_n)$. Therefore, $\mu(A)=\lim _{i \rightarrow \infty} \mu\left(A_i\right)$.
<p align="right">□</p>


**Remark.** In iv), $\mu(A_1)<\infty$ is necessary. Consider 
- $[1,\infty)\supset [2,\infty)\supset \cdots\supset [n,\infty)\cdots$ and
- $A_i=\{i,i+1,\cdots\}$.

> [!definition]
> A measure $\mu$ is a finite measure if $\mu(X)<\infty$. 
> 
> A measure $\mu$ is $\sigma$-finite if there exist sets $E_i \in \mathcal{A}$ for $i=1,2, \ldots$ such that $\mu\left(E_i\right)<\infty$ for each $i$ and $X=\cup_{i=1}^{\infty} E_i$. 
> 
> If $\mu$ is a finite measure, then $(X, \mathcal{A}, \mu)$ is called a finite measure space, and similarly, if $\mu$ is a $\sigma$-finite measure, then $(X, \mathcal{A}, \mu)$ is called a $\sigma$-finite measure space.

> [!definition] almost everywhere holds
> For a measure space $(X, \mathcal{A}, \mu)$ and a measurable subset $E$ of $X$, we say that a property holds almost everywhere on $E$, or it holds for almost all $x$ in $E$, provided it holds on $E-E_0$, where $E_0$ is a measurable subset of $E$ for which $\mu\left(E_0\right)=0$.
> 

> [!lemma] Borel-Cantelli 
> Let $(X, \mathcal{A}, \mu)$ be a measure space and $\left\{E_k\right\}_{k=1}^{\infty}$ a countable collection of measurable sets for which $\sum_{i=1}^{\infty} \mu\left(E_k\right)<\infty$. Then almost all $x$ in $X$ belong to at most a finite number of the $E_k$ 's.

**_Proof._**
Let $D=\{x:x\mbox{ belongs to at most finite number of the }E_k\mbox{'s}\}$. It suffices to show that $\mu(D^c)=0$. Note that $D^c=\{x:x\mbox{ belongs to infinitely many }E_k\mbox{'s}\}=\lim\sup_{n\to\infty} E_n$. So we have $\mu(D^c)=\mu(\cap_{n=1}^\infty\cup_{k=n}^\infty E_k)\leqslant\mu(\cap_{k=n}^\infty E_k)\leqslant\sum_{k=n}^\infty\mu(E_k)=0$.
<p align="right">□</p>

> [!definition] complete
> A measure space $(X, \mathcal{A}, \mu)$ is said to be *complete* if
> 
> $$N \in \mathcal{A}, \mu(N)=0, E \subset N \Rightarrow E \in \mathcal{A}.$$

**Example.** Let $X=\{a, b, c\}$. Then $\mathcal{A}=\{\emptyset,\{a\},\{b, c\}, X\}$ is a $\sigma$-algebra of subsets of $X$. Define function $\mu$ on $\mathcal{A}$ by $\mu(\emptyset)=0, \mu(\{a\})=$ $1, \mu(\{b, c\})=0$, and $\mu(X)=1$, then $\mu$ is a measure on $\mathcal{A}$. The set $\{b, c\}$ is a null set in the measure space $(X, \mathcal{A}, \mu)$, but its subset $\{b\}$ is not a member of $\mathcal{A}$. Therefore $(X, \mathcal{A}, \mu)$ is not a complete measure space.

> [!theorem]
> Let $(X, \mathcal{A}, \mu)$ be a measure space and define
> 
> $$
> \mathcal{A}^*=\{E \subseteq X: \exists A, B \in \mathcal{A} \text { such that } A \subseteq E \subseteq B \text { and } \mu(B-A)=0\}.
> $$
> 
> Then the following holds.
> - $\mathcal{A}^*$ is a $\sigma$-algebra and $\mathcal{A} \subset \mathcal{A}^*$.
> - There exists a unique measure $\mu^*$ on $\mathcal{A}^*$ such that $\left.\mu^*\right|_{\mathcal{A}}=\mu$.
> - The triple $\left(X, \mathcal{A}^*, \mu^*\right)$ is a complete measure space. It is called the completion of $(X, \mathcal{A}, \mu)$.

**_Proof._**
i) Note that $\emptyset,X\in\mathcal A^*$. Let $E\in\mathcal A^*$. Then there exists $A\subseteq E\subseteq B$ such that $\mu(B-A)=0$. Then $A^c\supseteq E^c\supseteq B^c$ and 
$\mu(A^c-B^c)=\mu(A^c\cap B)=\mu(B-A)=0$. So $E^c\in\mathcal A^*$. Let $\{E_n\}\subseteq\mathcal A^*$, and let $A_n\subseteq E_n\subseteq B_n$ with $\mu(B_n-A_n)=0$. Let $A=\cup_{n=1}^\infty A_n$ and $B=\cup_{n=1}^\infty B_n$. Then $\mu(B-A)\leqslant\sum_{i=1}^\infty\mu(B_n-A_n)=0$ and $A\subseteq E=\cup_{n=1}^\infty E_n\subseteq B$. Therefore, $E\in \mathcal A^*$. 

ii) For any $E\in\mathcal A^*$, we have $A\subset E\subset B$ and $\mu(B-A)=0$. If $\mu^*$ is defined, then $\mu^*(E)=\mu(A)$. Define $\mu^*(E)=\mu(A)$ if $A\subset E\subset B$. Claim that $\mu^*$ is well defined. Otherwise, assume that $A_1\subset E\subset B_1$ and $A_2\subset E\subset B_2$ with $\mu(B_i-A_i)=0$. Then $\mu(A_1)\leqslant\mu(B_2)=\mu(A_2)\leqslant\mu(B_1)=\mu(A_1)$, i.e., $\mu(A_1)=\mu(A_2)$. If $\{E_i\}\subseteq\mathcal{A}^*$ with $E_i\cap E_j=\emptyset$, then there exist $A_i\subseteq E_i\subseteq B_i$ such that $\mu(B_i-A_i)=\emptyset$. Let $A=\cup_{i=1}^\infty A_i$, and let $B=\cup_{i=1}^\infty B_i$. Then $B-A\subseteq\cup_{i=1}^\infty(B_i-A_i)$ and so $\mu(B-A)=0$. It follows that $\mu^*(\cup_{i=1}^\infty E_i)=\mu^*(A)=\mu(A)=\sum_{i=1}^\infty\mu^*(E_i)$. Therefore, $\mu^*$ is a measure.

iii) If $N\in\mathcal{A}^*$ and $\mu^*(N)=0$, then there exists $A,B$ such that $A\subseteq N\subseteq B$ such that $\mu(B-A)=0$. Since $\mu(A)=0$, we have $\mu(B)=0$. For any $M\subseteq N$, there is $\emptyset\subseteq M\subseteq B$ and $\mu(B-\emptyset)=0$. Therefore, $M\in\mathcal{A}^*$ and we finish the proof.
<p align="right">□</p>


> [!definition]
> A probability or *probability measure* is a measure $\mu$ such that $\mu(X)=1$.


