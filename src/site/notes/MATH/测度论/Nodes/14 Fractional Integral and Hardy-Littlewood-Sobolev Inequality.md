---
{"dg-publish":true,"draft":false,"permalink":"/MATH/测度论/Nodes/14 Fractional Integral and Hardy-Littlewood-Sobolev Inequality/","dgPassFrontmatter":true}
---



> [!theorem] 
> If $T: \mathbb{R}^n \rightarrow \mathbb{R}^n$ is a Lipschitz map, that is, there exists $c$ such that $|T x-T y| \leqslant c|x-y|$, $\forall x, y \in \mathbb{R}^n$, then $T$ maps measurable sets into measurable sets. 
{ #179d20}


**_Proof._**
We can prove that:
- $T$ maps $F_\sigma$-set to $F_\sigma$-set, because continuous map preserves compact sets and $F_\sigma$-set can be covered by countable union of compact sets;
- $T$ maps sets of measure zero into sets of measure zero by considering the cover of sets with cubes.

[[MATH/测度论/Nodes/10 Lebesgue Measure#^7b1c20\|Recall]] that for any measurable set $E$, there exists $F_\sigma$-set $H$ and $Z$ of measure zero such that $E=H\cup Z$. Then we finish the proof.
<p align="left">□</p>


> [!lemma]
> If $f(x)$ is measurable in $\mathbb{R}^n$, then the function $F(x, t)=f(x-t)$ is measurable in $\mathbb{R}^n \times \mathbb{R}^n=\mathbb{R}^{2 n}$.

**_Proof._**
Define $g(x,t)=f(x)$, then $g$ is measurable because $g^{-1}((a,\infty))=\{x\in \mathbb{R}^n:f(x)>a\}\times \mathbb{R}^n$. Define $T(x,t)=(x-t,x+t)$, then $T$ is Lipschitz. Note that $F(x,t)=g\circ T(x,t)$ and $F^{-1}((a,\infty))=T^{-1}\circ g^{-1}((a,\infty))$ is measurable by [[MATH/测度论/Nodes/14 Fractional Integral and Hardy-Littlewood-Sobolev Inequality#^179d20\|#^179d20]]. Thus $F$ is measurable.
<p align="left">□</p>


**Remark.** If we take $T(x,t)=(x-t,x+t)$, the proof also works. ChatGPT tells me the choice of $T(x,t)=(x-t,x+t)$ might simply reflect a convention or aesthetic preference.


> [!lemma]
> Assume that $f,g\in L^1(\mathbb{R}^n)$. 
> - $f * g \in L^1\left(\mathbb{R}^n\right)$, $||f*g||_1\leqslant ||f||_1||g||_1$ and 
> 
> $$
> \int_{\mathbb{R}^n} f * g d x =\left(\int_{\mathbb{R}^n} f d x\right)\left(\int_{\mathbb{R}^n} g d x\right) .
> $$
> 
> - If $1<p \leqslant \infty, f \in L^1$, and $g \in L^p$, then $\|f * g\|_p \leqslant\|f\|_1\|g\|_p$.
{ #8b552d}


**_Proof._**
i) Note that if $f,g\geqslant 0$, then 

$$||f*g||_1=\int_{\mathbb{R}^n}f*gdx=||f||_1||g||_1.$$

Then for any $f,g\in L^1(\mathbb{R}^n)$, we have $||f*g||_1\leqslant ||f||_1||g||_1$ and so $f*g\in L^1(\mathbb{R}^n)$. Then by Fubini's theorem, there is $\int_{\mathbb{R}^n} f * g d x =\left(\int_{\mathbb{R}^n} f d x\right)\left(\int_{\mathbb{R}^n} g d x\right)$.

ii) Let $1\leqslant p<\infty$, and let $q$ be the conjugate exponent to $p$. By Holder's inequality,

$$
\begin{aligned}
& \left|\int_{\mathbb{R}^n} f(y) g(x-y) d y\right| \\
\leqslant & \int_{\mathbb{R}^n}|f(y)|^{\frac{1}{q}}|f(y)|^{1-\frac{1}{q}}|g(x-y)| d y \\
\leqslant & \left(\int_{\mathbb{R}^n}|f(y)| d y\right)^{1 / q}\left(\int_{\mathbb{R}^n}|f(y)|^{p\left(1-\frac{1}{4}\right)}|g(x-y)|^p d y\right)^{1 / p} .
\end{aligned}
$$


Then using the Fubini theorem, there is

$$
\begin{aligned}
\int_{\mathbb{R}^n}|f * g(x)|^p d x & \leqslant \int_{\mathbb{R}^n}\left(\int_{\mathbb{R}^n}|f(y)| d y\right)^{p / q} \int_{\mathbb{R}^n}|f(y) \| g(x-y)|^p d y d x \\
& =\|f\|_1^{p / q}\|g\|_p^p \int_{\mathbb{R}^n}|f(y)| d y \\
& =\|f\|_1^{1+p / q}\|g\|_p^p\\
& =\|f\|_1^p\|g\|_p^p
\end{aligned}
$$


and then taking $p^{t h}$ roots gives our desire result.

When $p=\infty$, for any given $x$, we have 

$$f*g(x)=\int_{\mathbb{R}^n}f(y)g(x-y)dy\leqslant \|g\|_\infty\int_{\mathbb{R}^n}|f(y)|dy=\|f\|_1\|g\|_\infty.$$

By the arbitrary of $x$, we finish the proof.
<p align="left">□</p>

The definition of $I_\alpha f$ is written in this [[MATH/测度论/Nodes/14 Fractional Integral and Hardy-Littlewood-Sobolev Inequality#^3qk3we\|remark]].

> [!theorem] Hardy-Littlewood-Sobolev
> Let $0<\alpha<n, 1 \leqslant p<\frac{n}{\alpha}, \frac{1}{q}=\frac{1}{p}-\frac{\alpha}{n}$. Then for every $f \in L^p\left(\mathbb{R}^n\right), I_\alpha f$ is measurable in $\mathbb{R}^n$. Moreover, 
> - if $1<p<\frac{n}{\alpha}$, then $\left\|I_\alpha f\right\|_q \leqslant c\|f\|_p$ for a constant $c$ that depends only on $\alpha, n$, and $p$;
> - if $p=1$, then
> 
> $$\|I_\alpha f\|_{q,w}=\sup _{\lambda>0} \lambda\left|\left\{x \in \mathbb{R}^n:\left|I_\alpha f(x)\right|>\lambda\right\}\right|^{1 / q} \leqslant c\|f\|_1.$$
>
{ #z20dwo}


**_Proof._**
See [[Measure  Theory    (Xia).pdf#page=101&selection=421,0,422,1|here]]. 

读了一遍，大概拿中文写个大纲：
- 先考虑nonnegative f的情况，估计 $I_\alpha f$ 的大小。
	- 把 $I_\alpha f$ 分成 $|x-y|<\delta$ 和 $|x-y|>\delta$ 两部分来算积分，后者用Holder估计，前者用 the HardyLittlewood maximal function 在一系列圆环来做（因为这样可以避开奇点）
	- 取一个 $\delta$ 把前面两部分得到的丑陋的两个常数操作一下，得到 $I_\alpha f(x) \leq c\|f\|_{p^{\frac{\alpha P}{N^n}}}^* f^*(x)^{1-\frac{\alpha p}{n}}$.
- 用[[MATH/测度论/Nodes/12 the Maximal Theorem#^4tmmbv\|12 the Maximal Theorem#^4tmmbv]]算 $||I_\alpha f||_q$. 现在我们完成了 i) 的对于 nonnegative 的证明。
- 当 $p=1$ 时，还是用 $I_\alpha f$ 的估计，用一下 [[MATH/测度论/Nodes/12 the Maximal Theorem#^vufshf\|Hardy-Littlewood]]. 现在我们完成了 ii) 的对于 nonnegative 的证明。
- 现在考虑一般的 $f$，注意到 $\left\|I_\alpha f\right\|_q \leq\left\|I_\alpha(|f|)\right\|_q$ 就可以了。
<p align="left">□</p>

**Remark.** Here is a motivation of [[MATH/测度论/Nodes/14 Fractional Integral and Hardy-Littlewood-Sobolev Inequality#^z20dwo\|#^z20dwo]]. Define 
{ #3qk3we}


$$I_\alpha f(x)=\int_{\mathbb{R}^n} f(y) \frac{1}{|x-y|^{n-\alpha}} d y, x \in \mathbb{R}^n,$$

and note that it is a convolution of $f$ and $|x|^{\alpha-n}$. By Fubini's theorem, we know $\int_{\mathbb{R}^n} f * g d x=\left(\int_{\mathbb{R}^n} f d x\right)\left(\int_{\mathbb{R}^n} g d x\right)$ and so $I_\alpha f$ exists but it is not necessary finite.

We aim to find $p$ and $q$ such that $I_\alpha$ is a bounded operator from $L^p$ to $L^q$. It will turn out that the values of $p$ and $q$ for which the norm inequality 

$$\left\|I_\alpha f\right\|_q \leqslant c\|f\|_p \text { for all } f \in L^p\left(\mathbb{R}^n\right)\tag{*}$$

is true, for some $c$ independent of $f$, are limited to

$$
1<p<\frac{n}{\alpha} \text { and } \frac{1}{q}=\frac{1}{p}-\frac{\alpha}{n} .
$$

To explain it, we need to verify the following observation:
- If $p \geqslant \frac{n}{\alpha}$, there exists $f \in L^p\left(\mathbb{R}^n\right)$ such that $I_\alpha f=\infty$ everywhere in $\mathbb{R}^n$. That is, $(*)$ cannot hold if $p \geqslant \frac{n}{\alpha}$.
- If $p=1$ and $\frac{1}{q}=1-\frac{\alpha}{n}$, there exists $f \in L^1\left(\mathbb{R}^n\right)$ such that $\left\|I_\alpha f\right\|_q=\infty$. Thus, $(*)$ fails when $p=1$ and $q=n /(n-\alpha)$.
- If $1 \leqslant p<\frac{n}{\alpha}$, the only value of $q$ for which $(*)$ can possibly hold for all $f \in L^p\left(\mathbb{R}^n\right)$ satisfies $\frac{1}{q}=\frac{1}{p}-\frac{\alpha}{n}$.

The computation is omitted. 

**Remark.** 这个证明不考。