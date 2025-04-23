---
{"dg-publish":true,"permalink":"/MATH/测度论/Nodes/7 Integration/","dgPassFrontmatter":true}
---


> [!definition]
> Let $(X, \mathcal{A}, \mu)$ be a measure space.
> - Let $s=\sum_{i=1}^n a_i \chi_{E_i}$ be a nonnegative measurable simple function. The (Lebesgue) integral of $s$ over $X$ is the number
> 
> $$
> \int_X s d \mu=\sum_{i=1}^n a_i \mu\left(E_i\right)
> $$
> 
> - If $f \geq 0$ is a measurable function. The integral of f over $X$ is the number $\int_X f d u$ defined by
> 
> $$
> \int_X f d \mu:=\sup _{s \leq f} \int_X s d \mu
> $$
> 
> where the supremum is taken over all measurable simple functions $s: X \rightarrow \mathbb{R}$ satisfying $0 \leq s(x) \leq f(x)$ for all $x \in X$.
> 
> Let $f$ be measurable and let $f^{+}=\max \{f, 0\}$ and $f^{-}=\max \{-f, 0\}$. Provided $\int_X f^{+} d \mu$ and $\int_X f^{-} d \mu$ **are not both infinite**, define
> 
> $$
> \int_X f d \mu=\int_X f^{+} d \mu-\int_X f^{-} d \mu
> $$
> 
> 
> Finally, if $f=u+i v$ is complex-valued and $\int_X(|u|+|v|) d \mu$ is finite, define
> 
> $$
> \int_X f d \mu=\int_X u d \mu+i \int_X v d \mu .
> $$

> [!definition]
> If $f$ is measurable and $\int_X|f| d \mu<\infty$, we say $f$ is integrable.

> [!proposition]
> There are some easy propositions, see [[Measure  Theory    (Xia).pdf#page=33&selection=7,0,7,15|here]].

# MCT

> [!theorem] monotone convergence theorem
> Suppose $\left\{f_n\right\}$ is a sequence of non-negative measurable functions with $f_1(x) \leq f_2(x) \leq \cdots$ for all $x$ and with $\lim _{n \rightarrow \infty} f_n(x)=f(x)$ for all $x$. Then $\int_X f_n d \mu \rightarrow \int_X f d \mu$.

**_Proof._**
Let $s$ be a simple function with $0\leqslant s\leqslant f$. For any fixed $c\in(0,1)$, let $A_n=\{x:f_n(x)\geqslant cs(x)\}$. We have $A_1\subseteq A_2\subseteq\cdots$ and $\cup_{n=1}^\infty A_n=X$. Hence, $\lim_{n\to\infty}\mu(A_n)=\mu(X)$. Note that

$$\int_X f_n\geqslant\int_{A_n}f_n\geqslant\int_{A_n}csd\mu=c\sum a_j\mu(A_n\cap E_j)$$

where $s=\sum_{j=1}^\infty a_j\chi_{E_j}$. As $n\to\infty$, 

$$c\sum a_j\mu(A_n\cap E_j)\to c\sum a_j\chi(E_j)=c\int_X sd\mu.$$

Take $c\to 1$, then we have $\lim_{n\to\infty}\int_X f_n\geqslant\int_X s$ for all simple functions $s\leqslant f$ hold. Then we obtain $\lim_{n\to\infty}\int_X f_n\geqslant\int_X f$. On the other hand, as $f_1\uparrow f$, $\lim_{n\to\infty}\int_X f_n\leqslant\int_X f$. Now we finish the proof.
□

**Remark.** $f$ is non-negative is necessary. Let $X=[0, \infty)$ and $f_n(x)=-1 / n$ for all $x$. Then $\int f_n=-\infty$, but $f_n \uparrow f$ where $f=0$ and $\int f=0$. 

# Additivity

> [!proposition]
> If $s,t\geqslant 0$ are simple functions, then $\int_X(s+t)d\mu=\int_X sd\mu+\int_X td\mu$.
{ #33d8fd}


**_Proof._**
Assume that $s=\sum_{j=1}^n a_j\chi_{E_j}$ and $t=\sum_{i=1}^m b_i\chi_{E_i}$. Then 

$$\int_X(s+t)d\mu=\sum_{i=1}^m\sum_{j=1}^n(a_i+b_j)\chi_{A_i\cap B_j}=\int_Xsd\mu+\int_Xtd\mu.$$

We have done.
□


> [!theorem]
> If $f$ and $g$ are non-negative and measurable, then
> 
> $$
\int_X(f+g) d \mu=\int_X f d \mu+\int_X g d \mu.
$$

**_Proof._**
By [[MATH/测度论/Nodes/6 Convergence of Measurable Functions#^n03bsd\|6 Convergence of Measurable Functions#^n03bsd]], there exist $0\leqslant s_1\leqslant s_2\leqslant\cdots$ and $0\leqslant t_1\leqslant t_2\leqslant\cdots$ such that $s_i(x)\to f(x)$ and $t_i(x)\to g(x)$. Then by [[MATH/测度论/Nodes/7 Integration#^33d8fd\|#^33d8fd]], $\int_X s_i+t_i=\int_X s_i+\int_X t_i$. It follows that 

$$\int_X(f+g)=\lim_{n\to\infty}\int_X(s_n+t_n)=\lim_{n\to\infty}(\int_Xs_n+\int_X t_n)=\int_Xf+\int_Xg.$$

Therefore, we have that $\int_X(f+g) d \mu=\int_X f d \mu+\int_X g d \mu$.
□


> [!theorem]
> If $f$ and $g$ are integrable, then
> 
> $$
\int_X(f+g) d \mu=\int_X f d \mu+\int_X g d \mu.
$$

**_Proof._**
Since $\int|f+g|\leqslant\int|f|+\int|g|<\infty$, then $f+g$ is integrable. Write

$$
(f+g)^{+}-(f+g)^{-}=f+g=f^{+}-f^{-}+g^{+}-g^{-}
$$

so that

$$
(f+g)^{+}+f^{-}+g^{-}=f^{+}+g^{+}+(f+g)^{-}
$$


Using the result for non-negative functions,

$$
\int(f+g)^{+}+\int f^{-}+\int g^{-}=\int f^{+}+\int g^{+}+\int(f+g)^{-}
$$


Rearranging,

$$
\begin{aligned}
\int(f+g) & =\int(f+g)^{+}-\int(f+g)^{-} \\
& =\int f^{+}-\int f^{-}+\int g^{+}-\int g^{-}=\int f+\int g
\end{aligned}
$$


If $f$ and $g$ are complex-valued, apply the above to the real and imaginary parts.
□


> [!proposition]
> Let $s\geqslant 0$ be a simple function. Assume that $\{E_i\}\subseteq\mathcal{A}$ with $E_i\cap E_j=\emptyset$ if $i\neq j$. Then $\int_{\cup_{i=1}^\infty E_i}sd\mu=\sum_{i=1}^\infty\int_{E_i}sd\mu$.

**_Proof._**
Let $E=\cup_{i=1}^\infty E_i$ and $F_n=\cup_{i=1}^n E_i$. Then $F_n\uparrow E$ and 

$$\int_E s=\int_Xs\chi_E=\lim_{n\to\infty}\int_Xs\chi_{F_n}=\lim_{n\to\infty}\int_{F_n}s.$$

Since $\int_{F_n}s=\sum_{i=1}^n\int_{E_i}s$, we have that $\int_{\cup_{i=1}^\infty E_i}s=\sum_{i=1}^\infty\int_{E_i}s$.
□


> [!proposition]
> If $f: X \rightarrow[0, \infty]$ is measurable and $E_1, E_2, E_3, \ldots$ is a sequence of pairwise disjoint measurable sets. Then
> 
> $$
> \int_{\cup_{i=1}^{\infty} E_i} f d \mu=\sum_{i=1}^{\infty} \int_{E_i} f d \mu
> $$
> 

**_Proof._**
Let $E=\cup_{i=1}^{\infty} E_i, f_n=\sum_{k=1}^n f \chi_{E_k}$, then $f_n \uparrow f \chi_E$ and

$$
\int_X f_n d \mu=\sum_{k=1}^n \int_{E_k} f d \mu.
$$

Taking $n \rightarrow \infty$ and using the monotone convergence theorem, one gets $\int_{\cup_{i=1}^{\infty} E_i} f d \mu=\sum_{i=1}^{\infty} \int_{E_i} f d \mu$. 
□



> [!proposition]
> Let $f_n:X\to[0,\infty]$ be a sequence of measurable functions. Then
>
> $$\int_{E}\sum_{n=1}^\infty f_n=\sum_{n=1}^\infty\int_E f_n$$
> 
> for all $E\in\mathcal{A}$.

**_Proof._**
Let $F_n=\sum_{i=1}^n f_i$. For any $a \in \mathbb{R}$, since $F_n \uparrow \sum_{n=1}^\infty f_n$, we have

$$
\{x \in X: F(x)>a\}=\cup_{n=1}^{\infty}\left\{x \in X: F_n(x)>a\right\}
$$


Thus $\sum_{n=1}^\infty f_n$ is measurable and

$$
\begin{aligned}
\int_E \sum_{i=1}^{\infty} f_i d \mu & =\int_E \lim _{n \rightarrow \infty} \sum_{i=1}^n f_i d \mu=\int_E \lim _{n \rightarrow \infty} F_n d \mu \\
& =\lim _{n \rightarrow \infty} \int_E F_n d \mu=\sum_{i=1}^{\infty} \int_E f_n d \mu.
\end{aligned}
$$

Now we finish the proof.
□

**Example.** For a non-negative double sequence of reals, the order of summation can be reversed. See [[Measure  Theory    (Xia).pdf#page=36&selection=532,0,532,7|here]].

# Fatou Lemma and DCT

> [!theorem] Fatou Lemma
> Suppose the $f_n$ are non-negative and measurable. Then
> 
> $$
> \int \liminf _{n \rightarrow \infty} f_n \leqslant \liminf _{n \rightarrow \infty} \int f_n
> $$

**_Proof._**
Note that 

$$\int_X\liminf_{n\to\infty} f_n=\int_X\lim_{n\to\infty}\inf_{k\geqslant n}f_k=\lim_{n\to\infty}\int_X\inf_{k\geqslant n}f_k=\liminf_{n\to\infty}\int_X\inf_{k\geqslant n}f_k\leqslant\liminf_{n\to\infty}\int_X f_n.$$

We have done.
□

**Remark.** The inequality can be strict, see [[Measure  Theory    (Xia).pdf#page=37&selection=302,0,303,0|here]].


> [!theorem] Dominated convergence theorem
> Suppose that $f_n, f$ are measurable extended real-valued functions and $f_n(x) \rightarrow f(x)$ for each $x$. Suppose there exists a non-negative integrable function $g$ such that $\left|f_n(x)\right| \leq g(x)$ for all $x$. Then
> 
> $$
> \lim _{n \rightarrow \infty} \int f_n d \mu=\int f d \mu
> $$


**_Proof._**
Since $f_n+g \geq 0$, by Fatou lemma,

$$
\int f+\int g=\int(f+g) \leq \liminf _{n \rightarrow \infty} \int\left(f_n+g\right)=\liminf _{n \rightarrow \infty} \int f_n+\int g
$$

Since $g$ is integrable, $\int f \leq \liminf _{n \rightarrow \infty} \int f_n(*)$. Similarly, $g-f_n \geq 0$, so

$$
\int g-\int f=\int(g-f) \leq \liminf _{n \rightarrow \infty} \int\left(g-f_n\right)=\int g+\liminf _{n \rightarrow \infty} \int\left(-f_n\right),
$$

and so $-\int f \leq \liminf _{n \rightarrow \infty} \int\left(-f_n\right)=-\limsup _{n \rightarrow \infty} \int f_n$, which with $(*)$ proves the theorem.
□


> [!theorem] GDCT/An Extension of the Dominated Convergence 
> Given a measure space $(X, \mathcal{A}, \mu)$. Let $\left\{f_n\right\}$ and $f$ be extended real-valued measurable functions and let $\left\{g_n\right\}$ and $g$ be nonnegative extended real-valued measurable functions on X. Suppose
> - $f_n \rightarrow f$ and $g_n \rightarrow g$ a.e. on $X$.
> - $g_n$ and $g$ are all integrable and $\int_X g_n d \mu \rightarrow \int_X g d \mu$.
> - $\left|f_n\right| \leq g_n$ on $X$ for any $n \in \mathbb{N}$.
> 
> Then $f$ is integrable and $\int_X f_n d \mu \rightarrow \int_X f d \mu$.

**_Proof._**
Firstly, we show that $f$ is integrable. Note that

$$\begin{aligned} \int_X|f| d \mu & =\int_X \lim _{n \rightarrow \infty}\left|f_n\right| d \mu \\ & \leq \liminf _{n \rightarrow \infty} \int_X\left|f_n\right| d \mu \\ & \leq \liminf _{n \rightarrow \infty} \int_X g_n d \mu \\ & =\int_X g d \mu<\infty,\end{aligned}$$

then $f$ is integrable. 

Since $f_n+g_n\geqslant 0$, then 

$$\int(g+f) \leq \liminf _{n \rightarrow \infty} \int\left(g_n+f_n\right)=\int g+\liminf _{n \rightarrow \infty} \int f_n$$

and so $\int f\leqslant\liminf\int f_n$. Similarly, since $g_n-f_n\geqslant 0$ we can show that $\limsup\int f_n\leqslant\int f$. Now we have that $\lim\int f_n=\int f$.
□

# Chebyshev's Inequality

> [!theorem] Chebyshev's Inequality 
> Let $(X, \mathcal{A}, \mu)$ be a measure space $f$ and $\lambda$ a positive real number.
> - If $f$ a nonnegative measurable function on $X$, then
> 
> $$
> \mu(\{x \in X, f(x)>\lambda\}) \leq \frac{1}{\lambda} \int_X f d \mu.
> $$
> 
> - If $g$ is an integrable function on $X$, then
> 
> $$
> \mu(\{x \in X,|g(x)|>\lambda\}) \leq \frac{1}{\lambda} \int_{\{x \in X,|g(x)|>\lambda\}}|g| d \mu.
> $$
>
{ #ceec71}


**_Proof._**
Easy.
□


> [!proposition]
> Let $(X, \mathcal{A}, \mu)$ be a measure space and $f$ a nonnegative measurable function on $X$ for which $\int_X f d \mu<\infty$. Then $f$ is finite a.e. on $X$ and $\{x \in X: f(x)>0\}$ is $\sigma$-finite.

**_Proof._**
By [[MATH/测度论/Nodes/7 Integration#^ceec71\|#^ceec71]]. 
□

> [!proposition]
> Suppose $f$ is measurable and non-negative and $\int_X f d \mu=0$. Then $f=0$ almost everywhere.
{ #ra34bw}


**_Proof._**
Since $\{x:f(x)>0\}=\cup_{n=1}^\infty \{x:f(x)>1/n\}$, we have $0=\int_X f\geqslant 1/n\cdot\mu(\{x:f(x)>1/n\})$ and so $\mu(\{x:f(x)>0\})=0$.
□


> [!proposition]
> Suppose $f$ is real-valued and integrable and for every measurable set $A$ we have $\int_A f d \mu=0$. Then $f=0$ almost everywhere.

**_Proof._**
Let $A=\{x:f(x)>0\}$, and let $B=\{x:f(x)<0\}$. By [[MATH/测度论/Nodes/7 Integration#^ra34bw\|#^ra34bw]], $f=0$ almost everywhere on both $A$ and $B$. Now we finish the proof.
□

# VCT

> [!definition]
> Let $(X, \mathcal{A}, \mu)$ be a measure space and $\left\{f_n\right\}$ a sequence of functions on $X$, each of which is integrable over $X$. The sequence $\left\{f_n\right\}$ is said to be *uniformly integrable* over $X$ provided for each $\epsilon>0$, there is a $\delta>0$ such that for any natural number $n$ and measurable subset $E$ of $X$, if $\mu(E)<\delta$, then
> 
> $$\int_E\left|f_n\right| d \mu<\epsilon$$
> 
> The sequence $\left\{f_n\right\}$ is said to be *tight* over $X$ provided for each $\epsilon>0$, there is a subset $X_0 \subset X$ that has finite measure and, for any natural number $n$,
> 
> $$
> \int_{X-X_0}\left|f_n\right| d \mu<\epsilon
> $$
> 


> [!lemma]
> Let $(X, \mathcal{A}, \mu)$ be a measure space and the function $f$ be integrable over $X$. Then for each $\epsilon>0$, there is a $\delta>0$ such that for any measurable subset $E$ of $X$,
> 
> $$
> \mu(E)<\delta \Rightarrow \int_E|f| d \mu<\epsilon
> $$
> 
> 
> Furthermore, for each $\epsilon>0$, there is a subset $X_0 \subset X$ that has finite measure and
> 
> $$
> \int_{X-X_0}|f| d \mu<\epsilon
> $$

**_Proof._**
Assume that $f\geqslant 0$ and $\int _Xf<\infty$. 

i) For any $\epsilon>0$, let $s$ be a non-negative simple measurable function with $s\leqslant f$, and $\int_X f\leqslant \int_X s+\epsilon/2$. Note that $s$ is a bounded function, then

$$\int_Af\leqslant\int_A(f-s)+\int_A s\leqslant \epsilon/2+M\mu(A).$$

Take $\delta=\mu(A)/2M$, then $\int _Af<\epsilon$.

ii) Let $X_0=\{x:s(x)\geqslant 0\}$, and let $s$ be the same function defined in i). Then $\mu(X_0)<\infty$, and 

$$\int_{X-X_0}f=\int_{X-X_0}(f-s)+\int_{X-X_0}s\leqslant\int_X(f-s)<\epsilon.$$

Now we finish the proof.
□


> [!theorem] Vitali Convergence Theorem 
> Let $(X, \mathcal{A}, \mu)$ be a measure space and $\left\{f_n\right\}$ a sequence of functions on $X$ that is both uniformly integrable and tight over $X$. Assume $f_n \rightarrow f$ pointwise a.e. on $X$ and the function $f$ is integrable over $X$. Then
>
>$$
\lim _{n \rightarrow \infty} \int_X f_n=\int_X f.
$$

**_Proof._**
For any $\epsilon>0$, take $X_0\in A$ with $\mu(X_0)<\infty$, then $\int_{X-X_0}(|f_n|+|f|)<\epsilon/6$ for all $n\in \mathbb{N}_+$. Further, there exists $\delta>0$ such that if $\mu(A)<\delta$, then $\int_A(|f_n|+|f|)<\epsilon/6$ for all $n\in \mathbb{N}_+$. 

Since $f_n\to f$ pointwise on $X_0$ and $\mu(X_0)<\epsilon$, by [[MATH/测度论/Nodes/6 Convergence of Measurable Functions#^6ijlum\|Egorov's theorem]], there exists $X_1\subseteq X_0$ with $\mu(X_0-X_1)<\delta$ such that $f_n\to f$ uniformly on $X_1$. It follows that 

$$\begin{aligned}
\int_X|f_n-f|&\leqslant\int_{X-X_0}(|f_n|+|f|)+\int _{X_0}|f_n-f|\\
&<\frac{\epsilon}{6}+\int_{X_0-X_1}|f_n-f|+\int_{X_1}|f_n-f|\\
&<\frac{\epsilon}{3}+\int_{X_1}|f_n-f|.
\end{aligned}$$

As $f_n\to f$ uniformly on $X_1$, there exists $N$ such that $|f_n(x)-f(x)|<\epsilon/6\mu(X_1)$ for any $n>N$. Hence, when $n>N$, $\int_X|f_n-f|<\epsilon/2$, i.e., $\lim_{n\to\infty}\int_Xf_n=\int_X f$.
□


> [!theorem]
> A bounded real-valued function $f$ on $[a, b]$ is Riemann integrable if and only if the set of points at which $f$ is discontinuous has Lebesgue measure 0, and in that case, $f$ is Lebesgue measurable and the Riemann integral of $f$ is equal in value to the Lebesgue integral of $f$.