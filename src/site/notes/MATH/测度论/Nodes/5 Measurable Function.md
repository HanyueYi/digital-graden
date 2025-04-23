---
{"dg-publish":true,"permalink":"/MATH/测度论/Nodes/5 Measurable Function/","dgPassFrontmatter":true}
---


> [!definition] measurable function
> - $\operatorname{Let}(X, \mathcal{A})$ and $(Y, \mathcal{B})$ be measurable spaces. A map $f: X \rightarrow Y$ is called measurable if
> 
> $$
> B \in \mathcal{B} \Rightarrow f^{-1}(B) \in \mathcal{A}
> $$
> 
> - Let $(X, \mathcal{A})$ be a measurable space. A function $f: X \rightarrow \overline{\mathbb{R}}$ is measurable if it is measurable with respect to the Borel $\sigma$-algebra on $\overline{\mathbb{R}}$ associated to the standard topology as defined above.
> - Let $X$ and $Y$ be topological spaces. A map $f: X \rightarrow Y$ is called Borel measurable if the pre-image of every Borel measurable subset of $Y$ under $f$ is a Borel measurable subset of $X$.

**Remark.** $\overline {\mathbb{R}}$ is defined as $\mathbb{R}\cup\{\infty\}\cup\{-\infty\}$. A subset of $\overline{\mathbb{R}}$ is open, if it is a countable union of the set of the form: $[-\infty,a),(a,\infty],(a,b)$. 

**Example.** Define $\chi_A:X\to\mathbb{R}$ as $\chi_A(x)=1$ if $x\in A$; $\chi_A(x)=0$ if $x\not\in A$. Then $\chi_A$ is measurable iff $A$ is a measurable set.


> [!proposition]
> Let $(X, \mathcal{A}),(Y, \mathcal{B}),(Z, \mathcal{C})$ be measurable spaces.
> - The identity map $\operatorname{id}_X: X \rightarrow X$ is measurable.
> - If $f: X \rightarrow Y$ and $g: Y \rightarrow Z$ are measurable maps, then so is the composition $g \circ f: X \rightarrow Z$.
> - Let $f: X \rightarrow Y$ be any map. Then the set
> 
> $$
> f_* \mathcal{A}:=\left\{B \subset Y \mid f^{-1}(B) \in \mathcal{A}\right\}
> $$
> 
> is a $\sigma$-algebra on $Y$, called the pushforward of $\mathcal{A}$ under $f$.
> - A map $f: X \rightarrow Y$ is measurable if and only if $\mathcal{B} \subset f_* \mathcal{A}$.

**_Proof._**
Easy. 
□

> [!proposition] measurable and continuous maps
> Let $(X, \mathcal{A})$ and $(Y, \mathcal{B})$ be measurable spaces. Assume that $\mathcal{B}$ is the Borel $\sigma$-algebra of a topology on $Y$.
> - A map $f: X \rightarrow Y$ is measurable if and only if for every open subset $U \subset Y$, $f^{-1}(U) \in \mathcal{A}$.
> - Assume that $\mathcal{A}=\mathcal{B}(X)$ is the Borel $\sigma$-algebra of a topology on $X$. Then every continuous map $f: X \rightarrow Y$ is (Borel) measurable.

**_Proof._**
Easy.
□


> [!proposition] characterization of measurable functions
> Let $(X, \mathcal{A})$ be $a$ measurable space and let $f: X \rightarrow \overline{\mathbb{R}}$ be any function. Then the following are equivalent: 
> - $f$ is measurable;
> - $f^{-1}((a, \infty])$ is a measurable subset of $X$ for every $a \in \mathbb{R}$;
> - $f^{-1}([a, \infty])$ is a measurable subset of $X$ for every $a \in \mathbb{R}$;
> - $f^{-1}([-\infty, b))$ is a measurable subset of $X$ for every $b \in \mathbb{R}$;
> - $f^{-1}([-\infty, b])$ is a measurable subset of $X$ for every $b \in \mathbb{R}$.

**_Proof._**
Easy.
□

> [!lemma]
> Any open subset in $\mathbb{R}^n$ is a countable union of the sets in the form of $(a_1,b_1)\times\cdots\times(a_n,b_n)$.
{ #2bca2c}


**_Proof._**
Let $O$ be the open subset in $\mathbb{R}^n$. Define $X:=\{x\in O:x=(x_1,\cdots,x_n),x_i\in \mathbb{Q} \}$. Then $X$ is a countable set. For each $x\in X$, define $R_x=(a_1,b_1)\times\cdots\times (a_n,b_n)$ be the maximal cube such that $R_x\subseteq O$. Then $\cup_{x\in X} R_x=O$. 
□

> [!proposition] vector valued measurable functions
> Let $(X, \mathcal{A})$ be a measurable space and let $f=\left(f_1, \cdots, f_n\right): X \rightarrow \mathbb{R}^n$ be a function. Then $f$ is measurable if and only if $f_i: X \rightarrow \mathbb{R}$ is measurable for each $i$.

**_Proof._**
Note that $f_i=\pi_i\circ f$ and $\pi_i$ is continuous, then $f_i$ is measurable. Now assume that $f_i$ is measurable for each $i$. Let $Q(a,b)=(a_1,b_1)\times\cdots\times(a_n,b_n)$. Then 

$$f^{-1}(Q(a,b))=\cap\{x\in X:f_i(x)\in(a_i,b_i)\}=\cap f_i^{-1}((a_i,b_i))\in\mathcal{A} .$$

Since any open subset in $\mathbb{R}^n$ is a countable union of the set $Q(a,b)$ by [[MATH/测度论/Nodes/5 Measurable Function#^2bca2c\|#^2bca2c]], then $f$ is measurable.
□

> [!proposition]
> Let $(X, \mathcal{A})$ be a measurable space and let $u, v: X \rightarrow \mathbb{R}$ be measurable functions. If $\phi: \mathbb{R}^2 \rightarrow \mathbb{R}$ is continuous, then the function $h: X \rightarrow \mathbb{R}$ defined by
> 
> $$
> h(x)=\phi(u(x), v(x)), x \in X
> $$
> 
> is measurable.
{ #12414f}


**_Proof._**
Since $f:=(u,v)$ and $\phi$ are measurable, then $h$ is measurable.
□


> [!proposition] properties of measurable functions
> Let $(X, \mathcal{A})$ be a measurable space.
> - If $f, g: X \rightarrow \mathbb{R}$ are measurable functions, then so are the functions
> 
> $$
> f+g; \,  f g ; \, \max \{f, g\} ; \, \min \{f, g\} ; \, |f| .
> $$
> 
> - Let $f_k: X \rightarrow \overline{\mathbb{R}}, k=1,2, \ldots$ be a sequence of measurable functions. Then the following functions from $X$ to $\overline{\mathbb{R}}$ are measurable:
> 
> $$\inf f_k,\,\sup f_k,\,\lim\sup f_k,\, \lim\inf f_k. $$
>
{ #e11178}


**_Proof._**
i) By [[MATH/测度论/Nodes/5 Measurable Function#^12414f\|#^12414f]].

ii) Define $g:=\sup _k f_k: X \rightarrow \overline{\mathbb{R}}$ and let $a \in \mathbb{R}$. Then the set

$$
\begin{aligned}
g^{-1}((a, \infty]) & =\left\{x \in X: \sup _i f_i(x)>a\right\}=\left\{x \in X: \exists i \text { such that } f_i(x)>a\right\} \\
& =\bigcup_{i=1}^{\infty}\left\{x \in X \mid f_i(x)>a\right\}=\bigcup_{i=1}^{\infty} f_i^{-1}((a, \infty]) .
\end{aligned}
$$

is measurable. Hence it follows that $g$ is measurable. It also follows that $-f_k$ is measurable, and hence the function $\inf f_k=-\sup \left(-f_k\right)$ is measurable. Also we conclude that the functions

$$
\limsup _k f_k=\inf _{l \in \mathbb{N}} \sup _{k \geq l} f_k ; \liminf _k f_k=\sup _{l \in \mathbb{N}} \inf _{k \geq l} f_k
$$

are also measurable.
□

> [!corollary]
> If $f_n:X\to \overline {\mathbb{R}}$ is measurable and $f_n(x)\to f(x)$ for all $x$, then $f:X\to \mathbb{R}$ is measurable.

**_Proof._**
By [[MATH/测度论/Nodes/5 Measurable Function#^e11178\|#^e11178]], ii).
□

> [!proposition]
> If $f:\mathbb{R}\to \mathbb{R}$ is monotone, then $f$ is Borel measurable.

**_Proof._**
Suppose that $f$ is increasing, for otherwise let $g=-f$. For any $a\in \mathbb{R}$, define $x_0=\sup\{x:f(x)\leqslant a\}$. 
- If $f(x_0)>a$, then $f^{-1}((a,\infty))=[x_0,\infty)$.
- If $f(x_0)\leqslant a$, then $f^{-1}((a,\infty))=(x_0,\infty)$. 

Therefore, $f^{-1}((a,\infty))$ is measurable and so $f$ is Borel measurable.
□