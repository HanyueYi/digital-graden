---
{"dg-publish":true,"permalink":"/MATH/测度论/Nodes/12 the Maximal Theorem/","dgPassFrontmatter":true}
---


> [!lemma]
> Let $\mathcal{C}$ be a collection of open balls in $\mathbb{R}^n$ and let $U=\cup_{B \in \mathcal{C}} B$. If $m(U)>c$, then there exist disjoint $B_1, \cdots, B_k \in \mathcal{C}$, such that
> 
> $$\sum_{i=1}^k m\left(B_i\right)>\frac{c}{3^n}$$
>
{ #e42f5f}


**_Proof._**
Consider a compact $K\subseteq \mathcal C$ and a finite open cover of $K$. Take $B_i$ such that $B_i$ is a ball with maximal radical and not intersecting with others, and they are what we desire. The key point is, each ball has intersection with some chosen ball and has shorter radius.

See [[Measure  Theory    (Xia).pdf#page=84&selection=336,0,336,10|here]].
□


> [!definition]
> A measurable function $f: \mathbb{R}^n \rightarrow \mathbb{C}$ is called locally integrable (with respect to Lebesgue measure) if $\int_K|f| d m<\infty$ for every bounded measurable set $K \subset \mathbb{R}^n$. 
> 
> We denote the space of locally integrable functions by $L_{l o c}^1$. If $f \in L_{l o c}^1, x \in \mathbb{R}^n$, and $r>0$, we define $A_r f(x)$ to be the average value of $f$ on $B(x, r)$ :
> 
> $$
> A_r f(x)=\frac{1}{m(B(x, r))} \int_{B(x, r)} f d m
> $$

**Remark.** If $f\in L_{loc}^1(\mathbb{R}^n)$, then for any $r>0$ the function 

$$h(x)=\frac{1}{m(B(x,r))}\int_{B(x,r)}|f|dm$$

is continuous. 

> [!definition]
> With each $f \in L_{l o c}^1\left(\mathbb{R}^n, m\right)$, we associate its maximal function, $f^*$, which is defined as
> 
> $$f^*(x)=\sup _{r>0} A_r|f|(x):=\sup _{r>0} \frac{1}{m(B(x, r))} \int_{B(x, r)}|f| d m .$$

With the remark above, we know $f^*$ is measurable.

> [!theorem] Hardy-Littlewood
> There is a constant $C>0$ such that for all $f \in L^1\left(\mathbb{R}^n, m\right)$ and all $\alpha>0$,
> 
> $$m\left(\left\{x \in \mathbb{R}^n: f^*(x)>\alpha\right\}\right) \leqslant \frac{C}{\alpha} \int_{\mathbb{R}^n}|f| d m =\frac{C}{\alpha}||f||_1.$$
{ #vufshf}


**_Proof._**
Let $E_\alpha=\left\{x \in \mathbb{R}^n: f^*(x)>\alpha\right\}$. For each $x \in E_\alpha$, there exists $r_x>0$ such that $A_{r_x}|f|(x)>\alpha$ and so the balls $B\left(x, r_x\right)$ cover $E_\alpha$. By [[#^e42f5f]], for any $c<m(E_\alpha)$, there are finite disjoint balls $B_j=B\left(x_j, r_{x_j}\right)$ satisfying $\sum_{j=1}^k m\left(B_j\right)>3^{-n} c$. It deduces that

$$c<3^n \sum_{j=1}^k m\left(B_j\right) \leqslant \frac{3^n}{\alpha} \sum_{j=1}^k \int_{B_j}|f| d m \leqslant \frac{3^n}{\alpha} \int_{\mathbb{R}^n}|f| d m .$$


Let $c \rightarrow m\left(E_\alpha\right)$. Now we finish the proof.
□


> [!lemma]
> If $f \in L_{\text {loc }}^1$, then $\lim _{r \rightarrow 0} A_r f(x)=f(x)$ for a.e. $x \in \mathbb{R}^n$.
{ #34aaa4}


**_Proof._**
It suffices to show, $\lim_{r\to 0}A_rf(x)=f(x)$ for a.e. $x\in B(x,N)$ for all $N\in \mathbb{N}$. For any fixed $N$ and $r<1$, consider $f\chi_{B(0,N+1)}$ and continuous $g$ such that $||f-g||_1<\epsilon$ by this [[Measure  Theory    (Xia).pdf#page=74&selection=269,0,270,1|lemma]]. Then we have 

$$\limsup_{r\to 0}|A_rf(x)-f(x)|\leqslant \limsup_{r\to 0}|A_r(f-g)(x)|+\limsup_{r\to 0}|A_rg(x)-g(x)|+|f-g|(x)\leqslant (f-g)^*(x)+|f-g|(x).$$

For $\alpha>0$, define $E_\alpha=\{x\in \mathbb{R}^n:\limsup_{r\to 0}|A_rf(x)-f(x)|>\alpha\}$. Since 

$$E_\alpha\subseteq\{x:(f-g)^*(x)>\alpha/2\}\cup\{x:|f-g|(x)>\alpha/2\}=S\cup T,$$

and $m(S)\leqslant \dfrac{2C}{\alpha}\epsilon$, $m(T)\leqslant \dfrac{2}{\alpha}\epsilon$, it yields that $m(E_\alpha)=0$ for any $\alpha>0$. Now we finish the proof.

Also see [[Measure  Theory    (Xia).pdf#page=85&selection=642,0,642,6|here]]. 
□

**Remark.** 这里说 $f\in L_{\mathrm{loc}}^1$ 只是因为它只需要在每个半径为 $N$ 的球上可积，当然对 $f\in L^1$ 更对。我觉得为了这点宽松引入新概念没什么意思。


> [!theorem]
> Define 
> 
> $$L_f=\left\{x: \lim _{r \rightarrow 0} \frac{1}{m(B(x, r))} \int_{B(x, r)}|f(y)-f(x)| d y=0\right\}.$$
> 
> If $f \in L_{\text {loc }}^1$, then $m\left(\left(L_f\right)^c\right)=0$.

**_Proof._**
For each $c \in \mathbb{C}$, define $g_c(x)=|f(x)-c|$. By [[#^34aaa4]], there is

$$\lim _{r \rightarrow 0} \frac{1}{m(B(x, r))} \int_{B(x, r)}|f(y)-c| d y=|f(x)-c|, \forall x\in E_c^c\mbox{ with }m(E_c)=0.$$

Let $D=\mathbb{Q}+\mathbb{Q}\cdot i$, and let $E=\cup_{c \in D} E_c$. Then $m(E)=0$. If $x \notin E$, for any $\epsilon>0$ we can choose $c \in D$ such that $|f(x)-c|<\epsilon$ and $|f(y)-f(x)|<|f(y)-c|+\epsilon$. Thus

$$
\limsup _{r \rightarrow 0} \frac{1}{m(B(x, r))} \int_{B(x, r)}|f(y)-f(x)| d y \leq|f(x)-c|+\epsilon<2 \epsilon .
$$

By the arbitrary of $\epsilon$, we finish the proof.
□

**Remark.** 这证明和结果还挺有意思的，本来想定义 $g_{x_0}(x)=|f(x)-f(x_0)|$ with $x_0$ running over $\mathbb{R}^n$, 发现放不出来。这样的收敛有点像 Cesaro 求和啊。

> [!theorem]
> Let $1<p \leqslant \infty$ and $f \in L^p\left(\mathbb{R}^n\right)$. Then $f^* \in L^p\left(\mathbb{R}^n\right)$ and $\left\|f^*\right\|_p \leqslant c\|f\|_p$, where $c$ depends only on $n$ and $p$.
{ #4tmmbv}


**_Proof._**
When $p=\infty$, we have $||f^*||_\infty\leqslant ||f||_{\infty}$. Now we assume that $1<p<\infty$.

For any given $\alpha>0$, define 

$$g(x)=\begin{cases}
f(x),&|f(x)|\geqslant \alpha/2, \\
0,& \mbox{otherwise}.
\end{cases}$$

Note that

$$
\begin{aligned}
\|g\|_1 & =\int_{\left\{x \in \mathbb{R}^n:|f(x)| \geqslant \alpha / 2\right\}}|f(x)| d x \\
& \leqslant \int_{\mathbb{R}^n}|f(x)|\left(\frac{|f(x)|}{\alpha / 2}\right)^{p-1} d x=\left(\frac{2}{\alpha}\right)^{p-1}\|f\|_p^{p}<\infty,
\end{aligned}
$$

then $g \in L^1\left(\mathbb{R}^n\right)$. Also, we have $\|f-g\|_{\infty} \leqslant \alpha / 2$ and $f^*(x) \leqslant g^*(x)+{\alpha}/{2}$. It deduces that

$$\left\{x \in \mathbb{R}^n: f^*(x)>\alpha\right\} \subset\left\{x \in \mathbb{R}^n: g^*(x)>\alpha / 2\right\}.$$

For any $\alpha>0$, define $h(\alpha)=\left|\left\{x \in \mathbb{R}^n: f^*(x)>\alpha\right\}\right|$ as the distribution function of $f^*$. Then by [[#^vufshf]], there is

$$
\begin{aligned}
h(\alpha) & \leqslant\left|\left\{x \in \mathbb{R}^n: g^*(x)>\alpha / 2\right\}\right| \\
& \leqslant \frac{2 C}{\alpha}\|g\|_1=\frac{2 C}{\alpha} \int_{\left\{x \in \mathbb{R}^n:|f(x)| \geq \alpha / 2\right\}}|f(x)| d x
\end{aligned}
$$

By [[MATH/Cards/Nodes/Layer Cake Representation#^pa9wsk\|layer cake representation]], we have

$$\begin{aligned}
\int_{\mathbb{R}^n} (f^{*})^{p} d x&=p \int_0^{\infty} \alpha^{p-1} h(\alpha) d \alpha\\
&\leqslant p \int_0^{\infty} \alpha^{p-1}\left(\frac{2 C}{\alpha} \int_{\left\{x \in \mathbb{R}^n:|f(x)| \geqslant \alpha / 2\right\}}|f(x)| d x\right) d \alpha\\
&=2 C p \int_{\mathbb{R}^n}|f(x)|\left(\int_0^{2|f(x)|} \alpha^{p-2} d \alpha\right) d x \\
& =\frac{2^p C p}{p-1} \int_{\mathbb{R}^n}|f(x)|^p d x\\
&=\frac{2^p C p}{p-1}\|f\|_p^p.
\end{aligned}$$

Taking $p$ th roots, we see that $\left\|f^*\right\|_p \leq c\|f\|_p$.

Also see [[Measure  Theory    (Xia).pdf#page=87&selection=327,0,328,1|here]].
□

**Remark.** 最tricky的部分是定义了 $g$，因为它是 $L^1$ 的所以可以用小木头来控制。