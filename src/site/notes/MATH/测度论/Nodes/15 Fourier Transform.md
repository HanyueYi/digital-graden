---
{"dg-publish":true,"draft":false,"permalink":"/MATH/测度论/Nodes/15 Fourier Transform/","dgPassFrontmatter":true}
---


> [!definition]
> The Fourier transform $\hat{f}(x)$ of a function $f$ on $\mathbb{R}^n, n \geq 1$, defined formally as
> 
> $$\hat{f}(x)=\frac{1}{(2 \pi)^n} \int_{\mathbb{R}^n} f(y) e^{-i x \cdot y} d y.$$

We first list some properties of $\hat f(x)$ in $L^1(\mathbb{R})$.

- Note that $|\hat{f}(x)|=\left|\frac{1}{(2 \pi)^n} \int_{\mathbb{R}^n} f(y) e^{-i x \cdot y} d y\right| \leqslant \frac{1}{(2 \pi)^n} \int_{\mathbb{R}^n}|f(y)| d y, x \in \mathbb{R}^n$, then we have $\sup _{x \in \mathbb{R}^n}|\hat{f}(x)| \leqslant(2 \pi)^{-n}\|f\|_1$.
- $f\to \hat f$ is linear on $L^1(\mathbb{R}^n)$.
- $\hat{f}(x)$ is a uniformly continuous function of $x$ on $\mathbb{R}^n$ if $f \in L^1\left(\mathbb{R}^n\right)$. (By considering $(2 \pi)^n|\hat{f}(x+h)-\hat{f}(x)|  =\left|\int_{\mathbb{R}^n} f(y) e^{-i x \cdot y}\left\{e^{-i y \cdot h}-1\right\} d y\right|$.)
- Riemann Lebesgue theorem. See [[Measure  Theory    (Xia).pdf#page=104&selection=357,1,357,8|here]]. 
- (Translation) $\hat f(x+h)=e^{ixh}\hat f(x)$.
- (Dilation) Define $\delta_\lambda f(x)=f(\lambda x)$, then $\widehat {\delta_\lambda f}(x)=1/|\lambda|^n\hat f(x/\lambda)$. 
- (Rotation) Let $\mathcal O$ be an orthogonal linear transformation of $\mathbb{R}^n$, then $\widehat{\mathcal Of}(x)=\hat f(\mathcal O(x))$.
- The Fourier transform of an integrable radial function is a radial function.
- Let $f(x)=e^{-|x|^2}, x \in \mathbb{R}^n$, then $\hat{f}(x)=\frac{1}{(2 \sqrt{\pi})^n} e^{-|x|^2 / 4}$.
- Gauss-Weierstrass kernel
{ #pszdqo}

- (Shifting hats) $\int_{\mathbb{R}^n} \hat{f}(x) g(x) d x=\int_{\mathbb{R}^n} \hat{g}(x) f(x) d x$.


> [!theorem]
> Suppose $1 \leq p \leq \infty$ and $f \in L^p\left(\mathbb{R}^n\right)$.
> - (1) For each $\epsilon>0, f * \phi_\epsilon$ is infinitely differentiable. For each $\alpha_1, \alpha_2, \ldots, \alpha_n$ non-negative integers
> 
> $$\frac{\partial^{\alpha_1+\cdots \alpha_n}\left(f * \phi_\epsilon\right)}{\partial_{x_1}^{\alpha_1} \cdots \partial_{x_n}^{\alpha_n}}=f * \frac{\partial^{\alpha_1+\cdots \alpha_n}\left(\phi_\epsilon\right)}{\partial_{x_1}^{\alpha_1} \cdots \partial_{x_n}^{\alpha_n}}$$
> 
> We use the convention that the $0^{\text {th }}$ order derivative of a function is just the function itself.
> - (2) $f * \phi_\epsilon \rightarrow f$ a.e. as $\epsilon \rightarrow 0$.
> - (3) If $f$ is continuous, then $f * \phi_\epsilon \rightarrow f$ uniformly on compact sets as $\epsilon \rightarrow 0$.
> - (4) If $1 \leq p<\infty$ and $f \in L^p\left(\mathbb{R}^n\right)$, then $f * \phi_\epsilon \rightarrow f$ in $L^p$.

**_Proof._**
See [[Measure  Theory    (Xia).pdf#page=107&selection=486,0,487,0|here]].
<p align="left">□</p>


> [!proposition]
> Suppose $\phi \in L^1\left(\mathbb{R}^n\right)$ and $\int_{\mathbb{R}^n} \phi(x) d x=1$. Let $\phi_\delta(x)=$ $\delta^{-n} \phi(x / \delta)$.
> - If $g$ is continuous with compact support, then $g * \phi_\delta$ converges to $g$ pointwise as $\delta \rightarrow 0$.
> - If $g$ is continuous with compact support, then $g * \phi_\delta$ converges to $g$ in $L^1$ as $\delta \rightarrow 0$.
> - If $f \in L^1$, then $\left\|f * \phi_\delta-f\right\|_1 \rightarrow 0$ as $\delta \rightarrow 0$.

**_Proof._**
See [[Measure  Theory    (Xia).pdf#page=109&selection=41,0,41,5|here]].  （我并没有看。
<p align="left">□</p>


> [!theorem] Inversion of the Fourier transform on $L^1$
> If $f$ and $\hat{f}$ are in $L^1\left(\mathbb{R}^n\right)$, then
> 
> $$f(x)=\int_{\mathbb{R}^n} \hat{f}(y) e^{i x \cdot y} d y \text {, a.e. }$$

**_Proof._**
See [[Measure  Theory    (Xia).pdf#page=110&selection=4,0,5,1|here]]. 


> [!corollary] Uniqueness
> If $f, g \in L^1\left(\mathbb{R}^n\right)$ and $\hat{f}(x)=\hat{g}(x)$ for all $x \in \mathbb{R}^n$, then $f=g$ a.e. in $\mathbb{R}^n$.


> [!proposition] The Convolution Property
> The convolution of any two integrable functions is also integrable and therefore has a well-defined Fourier transform.


> [!theorem]
> If $f, g \in L^1\left(\mathbb{R}^n\right)$, then
> 
> $$\widehat{f* g}(x)=(2 \pi)^n \hat{f}(x) \hat{g}(x) \text { for all } x \in \mathbb{R}^n.$$


This follows easily from Fubini's theorem and is left as an exercise.


*****

> [!theorem]
> - Let $x_k, k=1, \ldots, n$, denote the $k$ th coordinate of $x \in \mathbb{R}^n$. If $f$ and $x_k f(x)$ belong to $L^1\left(\mathbb{R}^n\right)$, then $\hat{f}$ has a partial derivative with respect to $x_k$ everywhere in $\mathbb{R}^n$, and
> 
> $$\frac{\partial \hat{f}}{\partial x_k}=\left(\widehat{-i{x}_k f}\right)=\frac{1}{(2 \pi)^n} \int_{\mathbb{R}^n}\left(-i y_k f(y)\right) e^{-i x \cdot y} d y.$$
> 
> - Fix $k=1, \ldots, n$ and let $h=\left(0, \ldots, 0, h_k, 0, \ldots, 0\right) \neq 0$ lie on the $k$ th coordinate axis. Suppose that $f \in L^1\left(\mathbb{R}^n\right)$ and that there is a function $g$ such that
> 
> $$\lim _{h_k \rightarrow 0} \int_{\mathbb{R}^{\mathrm{n}}}\left|\frac{f(x+h)-f(x)}{h_k}-g(x)\right| d x=0.$$
> 
> Then $g \in L^1\left(\mathbb{R}^n\right)$ and
> 
> $$\hat{g}(x)=i x_k \hat{f}(x) \text { for all } x \in \mathbb{R}^n.$$

**_Proof._**
See [[Measure  Theory    (Xia).pdf#page=111&selection=206,0,207,0|here]]. 
<p align="left">□</p>


# Fourier Transform on $L^2$

> [!lemma]
> Let $f, g \in L^2\left(\mathbb{R}^n\right)$. Then $f * g$ is uniformly continuous and bounded on $\mathbb{R}^n$, and $\|f * g\|_{\infty} \leq\|f\|_2\|g\|_2$.

**_Proof._**
By Cauchy inequality. See [[Measure  Theory    (Xia).pdf#page=112&selection=4,0,4,5|here]]. 
<p align="left">□</p>


> [!theorem] Plancherel
> If $f$ is continuous with compact support, then $\hat{f} \in L^2\left(\mathbb{R}^n\right)$ and
> 
> $$\|\hat{f}\|_2=(2 \pi)^{-n / 2}\|f\|_2.$$

**_Proof._**
By [[MATH/测度论/Nodes/15 Fourier Transform#^pszdqo\|Gauss-Weierstrass kernel]], we have 

$$\int_{\mathbb{R}^n}e^{-iuy}\hat f(u) H_a(u)du=(f* \hat{H_a})(y).$$

Take $f=f*\overline{f(-x)}$ and take $y=0$, then 

$$(2\pi)^n\int|\hat f(u)|^2H_a(u)du=(f*g)*\hat{H_a}(0).$$

Take $a\to \infty$ and we finish the proof.

Also see [[Measure  Theory    (Xia).pdf#page=112&selection=332,0,332,5|here]].
<p align="left">□</p>


**Remark.** If $\{f_k\}$ satisfying $||f_k-f||_2\to 0$, then $\{\hat{f_k}\}$ is Cauchy in $L^2$ and converges to a function $\hat f$ in $L^2$. We can check that $\hat f$ is not depending on the choice of $f_k$, and so it is well-defined. (That is the way how we define $\hat f$?)

