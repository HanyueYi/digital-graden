---
{"dg-publish":true,"permalink":"/MATH/测度论/Nodes/9 LP Spaces/","dgPassFrontmatter":true}
---


> [!lemma] Young
> If $a,b>0$, $p,q>1$ with $\frac{1}{p}+\frac{1}{q}=1$, then $ab\leqslant\frac{1}{p}a^p+\frac{1}{q}b^q$.
{ #bbb4ba}


**_Proof._**
Let $f=x^p/p-xb$ and consider its critical points. 
<p align="left">□</p>


> [!lemma] Holder and Minkowski
> Let $f, g: X \rightarrow[0, \infty]$ be measurable functions. Then $f$ and $g$ satisfy the Hölder inequality
> 
> $$
> \int_X f g d \mu \leqslant\left(\int_X f^p d \mu\right)^{1 / p}\left(\int_X g^q d \mu\right)^{1 / q}
> $$
> 
> and the Minkowski inequality
> 
> $$\left(\int_X(f+g)^p d \mu\right)^{1 / p} \leqslant\left(\int_X f^p d \mu\right)^{1 / p}+\left(\int_X g^p d \mu\right)^{1 / p}.$$
{ #cef2ff}


**_Proof._**
For Holder inequality, assume that $\|f\|_p=\|g\|_q=1$ and use [[MATH/测度论/Nodes/9 LP Spaces#^bbb4ba\|#^bbb4ba]].

For Minkowski inequality, we can suppose that $\|f\|_p<\infty$ and $\|g\|_q<\infty$. It deduces that $\|f+g\|_p<\infty$ by $f,g\leqslant(f^p+g^p)^{1/p}$ and $(f+g)^p\leqslant 2^p(f^p+g^p)$. Then by Holder inequality, there is

$$\begin{aligned} C^p & =\int_X f(f+g)^{p-1} d \mu+\int_X g(f+g)^{p-1} d \mu \\ & \leq\left(\int_X f^p d \mu\right)^{1 / p}\left(\int_X(f+g)^{(p-1) q} d \mu\right)^{1 / q}+\left(\int_X g^p d \mu\right)^{1 / p}\left(\int_X(f+g)^{(p-1) q} d \mu\right)^{1 / q} \\ & =(A+B)\left(\int_X(f+g)^p d \mu\right)^{1 / q}=(A+B) C^{p-1},\end{aligned}$$

where $C=\left(\int_X(f+g)^p d \mu\right)^{1 / p}$, $A=\left(\int_X f^p d \mu\right)^{1 / p}$ and $B=\left(\int_X g^p d \mu\right)^{1 / p}$. Now we finish the proof.

Also see [[Measure  Theory    (Xia).pdf#page=54&selection=140,0,141,1|here]].
<p align="left">□</p>


# Definition of $L^p$

> [!definition]
> Let $(X, \mathcal{A}, \mu)$ be a measure space and let $1 \leqslant p<\infty$. Let $f$ be a measurable function on $X$. The *$L^p$-norm* of $f$ is the number
> 
> $$
> \|f\|_p=\left(\int_X|f|^p d \mu\right)^{1 / p} .
> $$
> 
> 
> A function $f: X \rightarrow \mathbb{R}$ is called *$p$-integrable* or an *$L^p$-function* if it is measurable and $\|f\|_p<\infty$. The space of $L^p$-functions is denoted by
> 
> $$
> \mathfrak{L}^p(\mu):=\left\{f: X \rightarrow \mathbb{R} \mid f \text { is } \mathcal{A} \text {-measurable and }\|f\|_p<\infty\right\} .
> $$
> 
> We say $f\sim g$ if $f=g$ a.e. respect to $\mu$.

**Remark.** By Minkowski inequality, there is $\|f+g\|_p\leqslant\|f\|_p+\|g\|_p$. Hence $\|\cdot\|_p$ is indeed a norm.


> [!definition]
> Let $(X, \mathcal{A}, \mu)$ be a measure space and let $f: X \rightarrow[0, \infty]$ be a measurable function and set
> 
> $$
> G(f)=\{c: \mu(\{x:|f(x)|>c\})=0\},
> $$
> 
> and define the essential supremum of $f$, denoted by $\|f\|_{\infty}$, as
> 
> $$
> \|f\|_{\infty}=\operatorname{ess} \sup f=\left\{\begin{array}{cc}
> \inf G(f), & \text { if } G(f) \neq \emptyset \\
> \infty, & \text { if } G(f)=\emptyset
> \end{array}\right.
> $$
> The set of $L^{\infty}$-functions on $X$ will be denoted by
> 
> $$
> \mathfrak{L}^{\infty}(\mu):=\left\{f: X \rightarrow \mathbb{R} \mid f \text { is } \mathcal{A} \text { - measurable and }\|f\|_{\infty}<\infty\right\} .
> $$
> 


> [!lemma]
> Let $||f||_\infty<\infty$. Then:
> - if $\alpha\in G(f)$, then $[\alpha,\infty)\subseteq G(f)$;
> - $||f||_\infty\in G(f)$;
> - $\mu(\{x:|f(x)|>c\})=0$ iff that $c\geqslant||f||_\infty$ and $\mu(\{x:f(x)|>c\})>0$ iff that $c<||f||_{\infty}$.

**_Proof._**
i) is easy. 

ii) Let $\{t_n\}\subseteq G(f)$ with $t_n\downarrow ||f||_\infty$. Let $E_n=\{x:|f(x)|>t_n\}$, then $\mu(E_n)=0$. Since $\{x:|f(x)|>||f||_\infty\}=\cup_{n=1}^\infty E_n$, we have that $\mu(\{x:|f(x)|>||f||_\infty\})=0$ and so $||f||_\infty\in G(f)$.

iii) is also easy. 
<p align="left">□</p>


> [!lemma]
> For a measurable function $f$,
> - $||f||_\infty\leqslant M$ iff $|f|\leqslant M$ a.e.;
> - $f\in\mathfrak L^\infty$ iff there exists a bounded function $g$ such that $f=g$ almost everywhere.

**_Proof._**
Easy.
<p align="left">□</p>


Denote the equivalence class of a function $f\in \mathfrak L^\infty(\mu)$ under the equivalence relation $f\sim g\iff f=g$ almost everywhere. Then define $L^\infty(\mu)=\mathfrak L^\infty(\mu)/\sim$ and it is a norm space where $||\cdot ||_\infty$ is the norm.

# Completeness

Recall that a metric space $M$ is called complete (or a Cauchy space) if every Cauchy sequence of points in $M$ has a limit that is also in $M$.

> [!lemma]
> A normed vector space $V$ is complete iff every absolutely convergent series in $V$ converges.

**_Proof._**
If $V$ is complete and $\sum_{n=1}^{\infty}\left\|x_n\right\|<\infty$, let $S_N=\sum_{n=1}^N x_n$. Then for $N>M$, we have

$$\left\|S_N-S_M\right\| \leq \sum_{n=M+1}^N\left\|x_n\right\| \rightarrow 0 \text {, as } M, N \rightarrow \infty$$

so the sequence $\left\{S_N\right\}$ is Cauchy and hence convergent. 

Conversely, suppose that every absolutely convergent series converges, and let $\left\{x_n\right\}$ be a Cauchy sequence. We can choose $n_1<n_2<\cdots$ such that $\left\|x_n-x_m\right\|<2^{-j}$ for $m, n \geq n_j$. Let $y_1=x_{n_1}, y_j=x_{n_j}-x_{n_{j-1}}$ for $j>1$. Then $\sum_{j=1}^k y_j=x_{n_k}$, and

$$
\sum_{j=1}^{\infty}\left\|y_j\right\| \leq\left\|y_1\right\|+\sum_{j=1}^{\infty} \frac{1}{2^j}<\infty
$$

so $\lim _{k \rightarrow \infty} x_{n_k}=\sum_{j=1}^{\infty} y_j$ exists. But since $\left\{x_n\right\}$ is Cauchy, we know that $\left\{x_n\right\}$ converges to the same limit as $\left\{x_{n_k}\right\}$.
<p align="left">□</p>


> [!theorem]
> For $1\leqslant p\leqslant \infty$, $L^p(\mu)$ is complete. Hence, $L^p(\mu)$ is a Banach space.

**_Proof._**
i) When $p<\infty$, define $\{f_n\}\subseteq L^p$ and $\sum_{n=1}^\infty||f||_p<\infty$. We aim to show there exists $f\in L^p$ such that $||\sum_{n=1}^\infty f_n-f||\to 0$.

Consider $F_n=\sum_{k=1}^n |f_k|$, then $F_n\in L^p$ and $F_n\uparrow F$. By MCT, $\int_X|F|^p=\lim_{n\to\infty}\int_X|F_n|^p\leqslant M^p<\infty$ and so $F$ is a.e. finite. Therefore, $\sum|f_k|$ converges almost everywhere and so $\sum f_k$ converges almost everywhere. Let $f=\sum f_k$. Then $\int_X |f|^p\leqslant\int_XF^pd\mu<\infty$ and so $f\in L^p$. Therefore, $||F-\sum_{k=1}^n f_i||_p^p=\int|f-\sum_{i=1}^n f_i|^p\to 0$ and so $\sum f_n$ converges to $f$ in the $L^p$ norm.

ii) Suppose now that $p=\infty$ and that $\left\{f_k\right\}$ is a sequence of functions that belong to $L^{\infty}(\mu)$ and satisfy $\sum_{k=1}^{\infty}\left\|f_k\right\|_{\infty}<\infty$. For each positive integer $k$, let $E_k=\left\{x \in X:\left|f_k(x)\right|>\left\|f_k\right\|_{\infty}\right\}$, and $E=\cup_{k=1}^{\infty} E_k$.

We have $\mu\left(E_k\right)=0$ and so $\mu(E)=0$. Hence $\sum_{k=1}^{\infty}\left|f_k(x)\right| \leq \sum_{k=1}^{\infty}\left\|f_k\right\|_{\infty}<\infty$ for all $x \in E^c$, which implies that $\sum_{k=1}^{\infty} f_k(x)$ converges for all $x \in E^c$. Define

$$
f(x)= \begin{cases}\sum_{k=1}^{\infty} f_k(x), & \text { if } x \notin E, \\ 0, & \text { if } x \in E .\end{cases}
$$


Then

$$\left|f(x)-\sum_{k=1}^n f_k(x)\right|=\left|\sum_{k=n+1}^{\infty} f_k(x)\right| \leqslant \sum_{k=n+1}^{\infty}\left|f_k(x)\right| \leqslant \sum_{k=n+1}^{\infty}\left\|f_k\right\|_{\infty} \text { a.e. }$$

Thus $\left\|f-\sum_{k=1}^n f_k\right\|_{\infty} \leq \sum_{k=n+1}^{\infty}\left\|f_k\right\|_{\infty}$. Letting $n \rightarrow \infty$, we have $\sum_{k=n+1}^{\infty}\left\|f_k\right\|_{\infty} \rightarrow 0$, so $\left\|f-\sum_{k=1}^n f_k\right\|_{\infty} \rightarrow 0$, i.e., $\sum_{l^n}^n f_k \rightarrow f$ in $L^{\infty}$. Therefore, $L^{\infty}$ is complete.
<p align="left">□</p>


**Remark.** 虽然在 $L^p$ 意义下 Cauchy 不一定收敛，但在一般的求和下 Cauchy 一定收敛。所以用 $\sum|f_k|<\infty$ almost everywhere 就能说明 $\sum f_k$ 存在了。

# Dense Subspace of $L^p$

> [!proposition]
> The follows hold.
> - $f_n \rightarrow f$ in $L^{\infty} \Leftrightarrow f_n \rightarrow f$ uniformly a.e..
> - For any $1 \leqslant p \leqslant \infty$, simple measurable functions determine a dense subspace of $L^p$.

**_Proof._**
i) Assume that $f_n\to f$ in $L^\infty$. Let $E_n=\{x:|f_n(x)-f(x)|>||f_n-f||_\infty\}$ and let $E=\cup _{n=1}^\infty E_n$. Then $\mu(E)=0$ and $f_n\to f$ uniformly on $X\setminus E$. Conversely, if $f_n\to f$ uniformly almost everywhere, then for any $\epsilon>0$ there exists $N$ such that $|f_n(x)-f(x)|<\epsilon$ a.e. and so $f_n\to f$ in $L^\infty$.

ii) Assume that $p<\infty$. There exists simple functions $f_n$ such that $f_n\to f$ pointwise satisfying $|f_n|\uparrow |f|$. Note that $|f_n-f|\leqslant 2|f|$, and it follows that $f_n\in L^p$ and $\lim\|f_n-f\|_p\to 0$ as $n\to\infty$ by DCT.

Now assume that $p=\infty$. Define $E=\{x:|f(x)|>||f||_\infty\}$, then $\mu(E)=0$. On $E^c$, $|f(x)|\leqslant ||f||_\infty<\infty$ and so $f$ is bounded on $E^c$. Therefore, a series of simple functions $\{f_n\}$ converges to $f$ uniformly on $E^c$ and so $f_n\to f$ in $L^\infty$. 
<p align="left">□</p>

**Remark.** We will prove that the set of continuous functions with compact support is also a dense subspace of $L^p$ for $1\leqslant p< \infty$. See [[MATH/测度论/Nodes/10 Lebesgue Measure#^fe0685\|10 Lebesgue Measure#^fe0685]].


# Dual Space & Riesz Representation Theorem

> [!definition] dual
> Let $(X, \mathcal{A}, \mu)$ be a measure space and let $1 \leqslant p \leqslant \infty$. Let $q$ be the conjugate exponent of $p$, i.e., $1/p+1/q=1$. Let $g \in L^q(\mu)$ and define $T_g: L^p(\mu) \rightarrow \mathbb{R}$ by
>
> $$T_g(f)=\int_X f g d \mu, f \in L^p(\mu) .$$

Since $|T_g(f)|\leqslant ||f||_p||g||_q$ by [[MATH/测度论/Nodes/9 LP Spaces#^cef2ff\|#^cef2ff]], we have $||T_g||\leqslant ||g||_q$ and so $T_g\in L^p(\mu)^*$. 


> [!lemma]
> Let $(X, \mathcal{A}, \mu)$ be a $\sigma$-finite measure space. Let $1 \leqslant p<\infty$. If $g_1,g_2$ are in $L^q(\mu)$, where $q$ is the conjugate exponent of $p$, such that $T_{g_1}=T_{g_2}$, then $g_1=g_2$ a.e.

**_Proof._**
It is easy. See [[Measure  Theory    (Xia).pdf#page=59&selection=532,0,533,0|here]].
<p align="left">□</p>


> [!theorem]
> Let $(X, \mathcal{A}, \mu)$ be a finite measure space. Let $1 \leqslant p<\infty$. Let $T$ be a continuous linear functional on $L^p(\mu)$. Then, there exists a unique $g \in L^q(\mu)$ such that $T=T_g$ and $\|T\|=\|g\|_q$.
{ #051f47}


**_Proof._**
Let $\lambda:\mathcal{A}\to \mathbb{R},E\mapsto T(\chi_E)$ for all $\chi_E\in L^p$. 

Claim that it $\{E_i\}\subseteq \mathcal{A}$ and $E_i\cap E_j=\emptyset$, then $\lambda(\cup_{i=1}^\infty E_i)=\sum_{i=1}^\infty \lambda(E_i)$. In fact, let $F_n=\cup_{i=1}^nE_i$, then $||\chi_E-\chi_{F_n}||_p^p=\int_X|\chi_{E-F_n}|^p=\mu(E-F_n)\to 0$. Then $\chi_{F_n}\to \chi_E$ in $L^p$. It deduces that $T(\chi_{F_n})\to T(\chi_E)$. Therefore, $\lambda(E)=\lim_{n\to\infty}\sum_{i=1}^nT(\chi_E)=\sum_{i=1}^\infty\chi(E_i)$ and so $\lambda$ is a signed measure on $\mathcal{A}$. 

If $\mu(E)=0$, then $\lambda(E)=T(\chi_E)=0$ and so $\lambda\ll \mu$. By [[MATH/测度论/Nodes/8 Signed Measure#^bdb1bb\|8 Signed Measure#^bdb1bb]] there exists $g\in L^1(\mu)$ such that $\lambda(E)=\int_Egd\mu=\int_X g\chi_Ed\mu$ for all $E\in\mathcal{A}$. Now we proved that for all simple measurable $s$, $T(s)=\int_X gsd\mu$.

If $f\in L^\infty(\mu)$, $||f||_{\infty}\leqslant M<\infty$ yields that $f\in L^p$. Let $s_n$ be simple measurable functions with $|s_n|\leqslant|f|$ and $s_n\to f$ as $n\to\infty$. Since $|s_n-f|^p\leqslant (2|f|)^p\in L^1$ and $|s_n-f|^p\to\infty$, we have that $||s_n-f||_p\to 0$. As $T(s_n)=\int_X s_ngd\mu$, we have that $T(f)=\int_X fgd\mu$. 

When $p>1$, claim that $g\in L^q(\mu)$. Let $E_n=\{x:|g(x)|\leqslant n\}$ and let $h=\pm 1$ so that $hg=|g|$. Let $f_n=|g|^{q-1}h\chi_{E_n}$. Then we have $|f_n|^p=|g|^{(q-1)p}\chi_{E_n}=|g|^q\chi_{E_n}$. Since $f_n\in L^\infty$, there is $|T(f_n)|=|\int_X f_ng|=\int_{E_n}|g|^q$. It follows that 

$$\int_{E_n}|g|^q\leqslant ||T||||f_n||_p=|T||(\int_{E_n}|g|^qd\mu)^{1/p}$$

and so $(\int_{E_n}|g|^qd\mu)^{1/q}\leqslant ||T||$.

When $p=1$, $\lambda(E)=\int_E gd\mu=\int_X g\chi_Ed\mu=T(\chi_E)$. Then $|\int_Egd\mu|=|T(\chi_E)|\leqslant ||T||||\chi_E||_q=||T||\mu(E)$ and so $\frac{1}{\mu(E)}|\int_Egd\mu|\leqslant ||T||$. It yields that $\int_E(g-||T||)\leqslant 0$ and $\int_E(g+||T||)\geqslant 0$. Hence, $|g|\leqslant ||T||$ a.e. and so $||g||_{\infty}\leqslant ||T||$. Now we proved that $g\in L^q(\mu)$. 

Since $T_g,T\in L^p(\mu)^*$ and $T(s)=T_g(s)$ for any simple measurable function $s$, we have $T=T_g$ on a dense subspace of $L^p$ and $T=T_g$. Note that $||T||=||T_g||\leqslant ||g||_q\leqslant ||T||$ yields $||g||_q=||T||$, then we have done.
<p align="left">□</p>


> [!theorem] Riesz representation theorem
> Let $(X, \mathcal{A}, \mu)$ be a $\sigma$-finite measure space. Let $1 \leqslant p<\infty$. Let $T$ be a continuous linear functional on $L^p(\mu)$. Then, there exists a unique $g \in L^q(\mu)$ such that $T(f)=\int_Xfgd \mu$ for all $f \in L^p$, and $\|T\|=\|g\|_q$.
{ #on15z3}


**_Proof._**
Let $\{E_i\}\subseteq \mathcal{A}$ with $\mu(E_i)<\infty$ and $E_i\uparrow X$. We identity $L^p(E_n)$ as a subspace of $L^p(X)$. By [[MATH/测度论/Nodes/9 LP Spaces#^051f47\|#^051f47]], there exists $g_n\in L^q(E_n)\subseteq L^q(X)$ such that $T(f)=\int_{E_n}fg_n$ for all $f\in L^p(E_n)$. Note that $g_{n+1}=g_n$ almost everywhere on $E_n$. Define $g:X\to R$ such that $g(x)=g_n(x)$ for $x\in E_n$. Claim that $T(f)=\int_{X}fgd\mu$ for all $f\in L^p(X)$. 

Note that $f\chi_{E_n}\to f$ in $L^p$, $T(f\chi_{E_n})\to T(f)$ and so $T(f)=\int_Xfgd\mu$. 
<p align="left">□</p>

**Remark.** 复习烦的要死，忽然发现这个证明不考。

![Pasted image 20241228213914.png|100](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020241228213914.png)

# Reflexivity & Weakly Convergence

> [!definition]
> A sequence $\left\{f_n\right\}$ in a Banach space $X$ weakly converges to an element $f$, if $\ell\left(f_n\right) \rightarrow \ell(f)$ for all $\ell \in X^*$, where $X^*$ is the dual space of $X$.


> [!corollary]
> Let $(X, \mathcal{A}, \mu)$ be a $\sigma$-finite measure space with $1<p<\infty$; then $L^p(\mu)$ is reflexive. That is, $L^p(\mu)^{**}\simeq L^p(\mu)$.

Recall that a Banach space is reflexive if and only if every bounded sequence in the space has a weakly convergent subsequence. It deduces the following theorem. Furthermore, 如果一个函数列 $\{f_n\}$ 在 $L^p(\mu)$ 空间中有界（也就是说，这些函数的 p-范数都小于某个固定的常数），那么我们总能找到一个子列 $\{f_{n_k}\}$，使得它在几乎处处的意义下收敛（也就是除了在一个零测集上之外，$\{f_{n_k}(x)\}$ 会对每个 x 收敛）.

> [!theorem] The Riesz Weak Compactness Theorem
> Let $(X, \mathcal{A}, \mu)$ be a $\sigma$-finite measure space and $1<p<\infty$. Then every bounded sequence in $L^p(\mu)$ has a weakly convergent subsequence; that is, if $\left\{f_n\right\}$ is a bounded sequence $L^p(\mu)$, then there is a subsequence $\left\{f_{n_k}\right\}$ of $\left\{f_n\right\}$ and a function $f$ in $L^p(\mu)$ for which
> 
> $$\lim _{k \rightarrow \infty} \int_X f_{n_k} g d \mu=\int_X f g d \mu, \forall g \in L^q(\mu) \text {, where } \frac{1}{p}+\frac{1}{q}=1 .$$

# Interpolation

> [!lemma]
> If $1 \leqslant p<q<r \leqslant \infty$, then $L^q \subset L^p+L^r$; that is, each $f \in L^q$ is the sum of a function in $L^p$ and a function in $L^r$.
{ #a9aid4}


**_Proof._**
If $f \in L^q$, let $E=\{x:|f(x)|>1\}$ and set $g=f \chi_E$ and $h=f \chi_{E^c}$. Then $|g|^p=|f|^p \chi_E \leqslant|f|^q \chi_E$, so $g \in L^p$, and $|h|^r=|f|^r \chi_{E^c} \leqslant|f|^q \chi_{E^c}$, so $h \in L^r$. (For $r=\infty$, obviously $\|h\|_{\infty} \leqslant 1$.)
<p align="left">□</p>


> [!theorem]
> If $1 \leqslant p<q<r \leqslant \infty$, then $L^p \cap L^r \subset L^q$. For $f \in L^p \cap L^r$, we have $\|f\|_q \leqslant\|f\|_p^\lambda\|f\|_r^{1-\lambda}$, where $\lambda \in(0,1)$ is given by
>
> $$\frac{1}{q}=\frac{\lambda}{p}+\frac{1-\lambda}{r}$$
> 

**_Proof._**
If $r=\infty$, then $|f|^q \leqslant\|f\|_{\infty}^{q-p}|f|^p$ where $\lambda=p/q$ and so $\|f\|_q \leqslant\|f\|_p^\lambda\|f\|_r^{1-\lambda}$.

If $r<\infty$, we use Holder's inequality, taking the pair of conjugate exponents to be $\frac{p}{\lambda q}$ and $\frac{r}{(1-\lambda) q}$ 

$$
\int|f|^q=\int|f|^{\lambda q} \cdot|f|^{(1-\lambda) q} \leqslant\left\|\left|f\right|^{\lambda q}\right\|_{\frac{p}{\lambda q}} \cdot\left\||f|^{(1-\lambda) q}\right\|_{\frac{r}{(1-\lambda) q}}=\|f\|_p^{\lambda q} \cdot\|f\|_r^{(1-\lambda) q} .
$$

Also see [[Measure  Theory    (Xia).pdf#page=63&selection=299,0,301,1|here]].
<p align="left">□</p>

