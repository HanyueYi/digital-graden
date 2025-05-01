---
{"dg-publish":true,"draft":false,"permalink":"/MATH/测度论/Nodes/6 Convergence of Measurable Functions/","dgPassFrontmatter":true}
---



> [!theorem] Egorov's Theorem 
> Suppose $(X, \mathcal{A}, \mu)$ is a measure space with $\mu(X)<\infty$. Suppose $f_1, f_2, \ldots$ is a sequence of measurable functions from $X$ to $\mathbb{R}$ that converges pointwise on $X$ to a measurable function $f: X \rightarrow \mathbb{R}$. Then for every $\epsilon>0$, there exists a set $E \in \mathcal{A}$ such that $\mu(X-E)<\epsilon$ and $f_n \rightarrow f$ uniformly on $E$.
{ #6ijlum}


**_Proof._**
For any $n\in \mathbb{N}_{+}$, we have that 

$$\cup_{m=1}^\infty\cap_{k=m}^\infty\{x:|f_k(x)-f(x)|<\frac{1}{n}\}=X.$$

Define $A_{m,n}=\cap_{k=m}^\infty\{x:|f_k(x)-f(x)|<\frac{1}{n}\}$, then $A_{m,n}\uparrow X$ as $m\to\infty$. For any $\epsilon>0$, there exists $m_n$ such that $\mu(A_{m_n,n})>\mu(X)-{\epsilon}/{2^n}$. Let $X_0=\cap_{n=1}^\infty A_{m_n,n}$. Note that

$$\mu(X-X_0)=\mu(X-\cap_{n=1}^\infty A_{m_n,n})=\mu(\cup_{n=1}^\infty(X-A_{m_n,n}))\leqslant\sum_{n=1}^\infty\frac{\epsilon}{2^n}=\epsilon.$$

For any $\epsilon'>0$, take $N$ such that $1/N<\epsilon'$. If $x\in X_0\subseteq A_{m_N,N}$, for any $k>m_N$, we have $|f_k(x)-f(x)|<\frac{1}{N}<\epsilon'$ for all $x\in X_0$. Therefore, $f_n\to f$ uniformly on $X_0$.
<p align="left">□</p>


**Remark.** $\mu(X)<\infty$ is necessary. Let $X=\mathbb{N}$, $\mathcal{A}=\mathcal{P}(X)$, and let $\mu$ be counting measure. Define $f_n=\chi_{1,\cdots,n}$, then $f_n\to f$ where $f\equiv 1$. Let $\epsilon =\frac{1}{2}$. For any $X_0\in \mathcal{P}(X)$ with $\mu(X-X_0)<1/2$, we aim to show $f_n$ does not converge uniformly on $X_0$. Since $\mu(X-X_0)\geqslant 1$ if $X\neq X_0$, then $X=X_0$. Claim that $f_n\to f$ does not converge uniformly on $X$, that is, there exists $\epsilon_0>0$, for any $N>0$, there exists $x\in X$ and $n\geqslant N$ such that $|f_n(x)-f(x)|\geqslant\epsilon_0$. Take $\epsilon_0=1/2$, then for any $N>0$ there is $|f_N(N+1)-f(N+1)|=1\geqslant\epsilon$. Hence, $f_n\to f$ is not uniformly convergent. 
{ #xi5yxj}


> [!definition] simple function
> Let $X$ be a set. A function $s: X \rightarrow \mathbb{R}$ is called a simple function if it takes on only finitely many values, i.e., the image $s(X)$ is a finite subset of $\mathbb{R}$.

> [!theorem] approximation by simple functions
> Suppose $(X, \mathcal{A})$ is a measurable space and $f: X \rightarrow[-\infty, \infty]$ is measurable. Then there exists a sequence $f_1, f_2, \ldots$ of functions from $X$ to $\mathbb{R}$ such that
> - each $f_k$ is a simple measurable function;
> - $\left|f_k(x)\right| \leq\left|f_{k+1}(x)\right| \leq|f(x)|$ for all $k \in \mathbb{N}$ and all $x \in X$;
> - $\lim _{k \rightarrow \infty} f_k(x)=f(x)$ for every $x \in X$;
> - $f_1, f_2, \ldots$ converges uniformly to $f$ on any set on which $f$ is bounded.
{ #n03bsd}


**_Proof._**
Define $f_k$ as the diagram below.![Pasted image 20241011144717.png|700](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020241011144717.png)

Then it is easy to prove the theorem. 
<p align="left">□</p>


> [!definition]
> Let $(X, \mathcal{A}, \mu)$ be a measure space and let $\left\{f_n\right\}_{n=1}^{\infty}$ be a sequence of real-valued measurable functions defined on $X$. Let $f$ be a real-valued measurable function defined on $X$. We say that $\left\{f_n\right\}$ *converges in measure* to $f$, with notation $f_n \xrightarrow{\mu} f$, if for every $\epsilon>0$, we have
> 
> $$
> \lim _{n \rightarrow \infty} \mu\left(\left\{x \in X:\left|f_n(x)-f(x)\right| \geq \epsilon\right\}\right)=0
> $$
> 
> We say that $\left\{f_n\right\}$ is *Cauchy in measure* if for every $\epsilon>0$ and for every $\delta>0$, there exists $N \in \mathbb{N}$ such that for all $n, m \geq N$, we have
> 
> $$
> \mu\left(\left\{x \in X:\left|f_n(x)-f_m(x)\right| \geq \epsilon\right\}\right)<\delta .
> $$


> [!theorem]
> Let $(X, \mathcal{A}, \mu)$ be a measure space and $\mu(X)<\infty$. Let $\left\{f_n\right\}_{n=1}^{\infty}$ be a sequence of real-valued measurable functions, defined on $X$, converging a.e. to a real-valued measurable function $f$. Then $f_n \xrightarrow{\mu} f$.

**_Proof._**
Let $D=\{x\in X:|f_n(x)-f(x)|\not\to 0\}$. Then $\mu(D)=0$. For any $\epsilon>0$, let $A_n=\{x:|f_n(x)-f(x)|\geqslant\epsilon\}$. Note that $\lim\sup_{n\to\infty}A_n\subseteq D$ and so $\mu(\lim\sup A_n)=0$. Define $B_n=\cup_{k=n}^\infty A_k$, then $B_n\downarrow 0$, which yields that $f_n\xrightarrow{\mu} f$.
<p align="left">□</p>


**Remark.** Let $X=\mathbb{R}$, and let $f_n=\chi_{(n,n+1)}$. Note that $f_n\to 0$ almost everywhere, and $\mu(\{x\in X:|f_{n}(x)-0|\geqslant 1/2\})=1\not\to 0$. Therefore, $f_n\not \xrightarrow{\mu} 0$. Furthermore, [[MATH/测度论/Nodes/6 Convergence of Measurable Functions#^xi5yxj\|this]] is also an example.


> [!proposition]
> Let $(X, \mathcal{A}, \mu)$ be a measure space, and let $f$ and $f_1, f_2, \ldots$ be real-valued measurable functions on $X$. If $f_n \xrightarrow{\mu} f$, then there is a subsequence of $\left\{f_n\right\}$ that converges a.e. to $f$.

**_Proof._**
Since $\lim_{n\to\infty}\mu(\{x:|f_n(x)-f(x)|\geqslant 1\})=0$, there exists $n_1$ such that $\mu(\{x:|f_{n_1}(x)-f(x)|\geqslant 1\})<\frac{1}{2}$. Repeat this procedure, 

$$\mu(\{x:|f_{n_k}(x)-f(x)|\geqslant\frac{1}{k}\})<\frac{1}{2^k}.$$

Now we get a subsequence $\{f_{n_k}\}$. Define $A_k=\{x:|f_{n_k}(x)-f(x)|\geqslant 1/k\}$, then $D=\cap_{j=1}^\infty\cup_{k=j}^\infty A_k$. It is easy to prove that $\mu(D)=0$. If $x\not\in D$, then there exists $j$ such that $x\not\in \cup_{k=j}^\infty A_j$ and so $|f_{n_k}(x)-f(x)|<1/k$ for all $k\geqslant j$. Hence $f_{n_k}\to f$ on $D^c$. 
<p align="left">□</p>
