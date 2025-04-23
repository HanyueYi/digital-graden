---
{"dg-publish":true,"permalink":"/MATH/测度论/Nodes/13 Riese-Thorin and Marcinkiewicz Interpolation Theorems/","dgPassFrontmatter":true}
---


> [!lemma] the three lines lemma
> Let $h$ be a bounded continuous function on the strip $0 \leqslant\mathrm{Re} z\leqslant 1$ that is holomorphic on the interior of the strip. If $|h| \leq M_0$ for $\mathrm {Re}z=0$ and $|h(z)| \leq M_1$ for $\mathrm{Re}z=1$, then $|h| \leq M_0^{1-t} M_1^t$ for Re $z=t, 0<t<1$.

**_Proof._**
WLOG assume that $M_0M_1\neq 0$. For $\epsilon>0$, define 

$$h_\epsilon(z)=h(z)M_0^{z-1}M_1^{-z}e^{\epsilon z(z-1)}$$

and it is holomorphic inside the strip. Note that $|h_\epsilon(iy)|\leqslant e^{-\epsilon y^2}\leqslant 1$ and $|h_\epsilon(1+iy)|\leqslant 1$. 

For any $x\in(0,1)$, there is

$$|h_\epsilon(x+iy)|=|h((x+iy)M_0^{x-1}M_1^{-x}e^{\epsilon x(x-1)}e^{-\epsilon y^2}|\leqslant Ce^{-\epsilon y^2}$$

because $h$ and $e^{\epsilon x(x-1)}$ are bounded. Since $e^{-\epsilon y^2}\to 0$ as $y\to\infty$, there exists $A>0$ such that $|h_{\epsilon}(x+iy)|\leqslant 1$ for any $x\in(0,1)$ and $y\in (-A,A)$ by the maximum modulus principle. It holds for any arbitrarily large $A$ and so $|h_\epsilon(z)|\leqslant 1$ inside the entire strip. Take $\epsilon\to 0$ and then we finish the proof.
<p align="right">□</p>


> [!definition]
> A measure $\mu$ on a measurable space $(X, \mathcal{A})$ is *semifinite* if for any measurable $A$ with $\mu(A)>0$, there exists a measurable $B \subset A$ such that $0<\mu(B)<\infty$.


> [!theorem]
> Let $(X, \mathcal{A}, \mu)$ be a measure space and let $1 \leq p, q \leq \infty$ be conjugate exponents. Suppose that $g$ is a measurable function on $X$ such that $f g \in$ $L^1$ for all $f$ in the space $\mathcal{S}$ of simple measurable functions that vanish outside a set of finite measure, and the quantity
> 
> $$\mathcal{M}_q(g)=\sup \left\{\left|\int f g\right|, f \in \mathcal{S} \text { and }\|f\|_p=1\right\}$$
> 
> is finite. Also, suppose that $S_g=\{x: g(x) \neq 0\}$ is $\sigma$-finite if $q<\infty$ and that $\mu$ is semifinite if $q=\infty$. Then $g \in L_q$ and $\mathcal{M}_q(g)=\|g\|_q$.

**_Proof._**
Take a bounded measurable $f$ with finite measure support $E$ and $\|f\|_p=1$, then there is a sequence $\left\{f_n\right\}$ of simple measurable functions such that $\left|f_n\right| \leqslant|f|$. Since $\left|f_n g\right| \leqslant\|f\|_{\infty} \chi_E|g|$ and $\chi_E|g| \in L^1$, by the dominated convergence theorem we have

$$
\begin{aligned}
\left|\int f g\right| & =\lim _{n \rightarrow \infty}\left|\int f_n g\right| \\
& \leqslant \lim _{n \rightarrow \infty}\left\|f_n\right\|_p \mathcal{M}_q(g)=\|f\|_p \mathcal{M}_q(g)=\mathcal{M}_q(g)
\end{aligned}
$$


Suppose that $q<\infty$. Let $\left\{E_n\right\}$ with finite measure such that $E_n\uparrow S_g$. Let $\left\{s_n\right\}$ be a sequence of simple measurable functions such that $s_n \rightarrow g$ pointwise and $|s_n| \leqslant|g|$ and let $g_n=s_n \chi_{E_n}$. Then $g_n \rightarrow g$ pointwise, $\left|g_n\right| \leqslant|g|$, and $g_n$ vanishes outside $E_n$. Let

$$
f_n=\frac{\left|g_n\right|^{q-1} \overline{\operatorname{sng} g}}{\left\|g_n\right\|_q^{q-1}},\mbox{ where} \operatorname{sng}(g)=\left\{\begin{array}{l}
\frac{g}{|g|}, \text { if } g \neq 0 \\
0, \text { if } g=0
\end{array}\right..
$$

Note that $g \overline{\text { sng }(g)}=|g|$. There exists some $f_n$ with $\left\|f_n\right\|_p=1$ satisfying $||g_n||_q=\int|f_ng_n|$ by [[MATH/测度论/Nodes/9 LP Spaces#^on15z3\|Riesz representation theorem]]. Then by Fatou's lemma

$$
\begin{aligned}
\|g\|_q & \leqslant \liminf _{n \rightarrow \infty}\left\|g_n\right\|_q=\liminf _{n \rightarrow \infty} \int\left|f_n g_n\right| \\
& \leqslant \liminf _{n \rightarrow \infty} \int\left|f_n g\right|=\liminf _{n \rightarrow \infty} \int f_n g \leqslant \mathcal{M}_q(g) .
\end{aligned}
$$

On the other hand, Holder's inequality gives $\mathcal{M}_q(g) \leq\|g\|_q$, so the proof is complete for the case $q<\infty$.

Now suppose $q=\infty$. Given $\epsilon>0$, let $A=\left\{x:|g(x)|>\mathcal{M}_{\infty}(g)+\epsilon\right\}$. If $\mu(A)$ were positive, we could choose $B \subset A$ with $0<\mu(B)<\infty$ since $\mu$ is semifinite. Setting $f=\mu(B)^{-1} \chi_B \overline{\text { sng } g}$, we would then have $\|f\|_1=1$, and $\int f g=\mu(B)^{-1} \int_B|g| \geq \mathcal{M}_{\infty}(g)+\epsilon$. But this is impossible by the argument at the beginning of the proof. Hence $\|g\|_{\infty} \leq \mathcal{M}_{\infty}(g)$, and the reverse inequality is obvious.
<p align="right">□</p>

**Remark.** Note that $\mathcal{M}_q(g)<\infty$ is the most crucial condition. It essentially measures how "large" $g$ is in terms of its interaction with all $f \in \mathcal S_{\text {normalized in }} L^p$, and finite $\mathcal{M}_q(g)$ implies that $g$ is "not too wild" and suggests that $g$ should belong to $L^q$. Furthermore, with some condition on the measurable space, we get $\mathcal M_q(g)=||g||_q$. 

**Remark**. 这个证明不考。

> [!theorem] the Riesz-Thorin interpolation theorem
> Suppose that $(X, \mathcal{A}, \mu)$ and $(Y, \mathcal{B}, \nu)$ are measure spaces and $p_0, p_1, q_0, q_1 \in[1, \infty], p_0 \leq p_1, q_0 \leq q_1$. If $q_0=q_1=\infty$, suppose also that $\nu$ is semifinite. For $0<t<1$, define $p_t$ and $q_t$ by
> 
> $$
> \frac{1}{p_t}=\frac{1-t}{p_0}+\frac{t}{p_1}, \frac{1}{q_t}=\frac{1-t}{q_0}+\frac{t}{q_1} .
> $$
> 
> 
> If $T$ is a linear map from $L^{p_0}(\mu)+L^{p_1}(\mu)$ into $L^{q_0}(\nu)+L^{q_1}(\nu)$ such that $\|T f\|_{q_0} \leqslant M_0\|f\|_{p_0}$ for $f \in L^{p_0}(\mu)$ and $\|T f\|_{q_1} \leqslant M_1\|f\|_{p_1}$ for $f \in L^{p_1}(\mu)$, then $\|T f\|_{q_t} \leqslant M_0^{1-t} M_1^t\|f\|_{p_t}$ for $f \in L^{p_t}(\mu)$.

**_Proof._**
See [[Measure  Theory    (Xia).pdf#page=90&selection=590,0,591,1|here]]. 
<p align="right">□</p>

**Remark.** 这个证明不考。

Recall that $f(x)=1/x$ is not integrable over $\mathbb{R}$, and to include such functions we slightly weaken the $L^p$ norms. Let $(X, \mathcal{A}, \mu)$ be a measure space and $f: X \rightarrow \mathbb{C}$ be a measurable function. We consider the distribution function $\mu_f(t)=\mu(\{x \in X:|f(x)|>t\})$ with $t \geqslant 0$. Recall that there is

$$\|f\|_p^p=p \int_0^{\infty} t^{p-1} \mu_f(t) d t, 1 \leqslant p<\infty$$

by [[MATH/Cards/Nodes/Layer Cake Representation\|layer cake representation]]. Notice that 

$$\begin{aligned}
\|f\|_p^p & =\int_X|f|^p d \mu \geqslant \int_{\{x \in X:|f(x)|>t\}}|f|^p d \mu \\
& \geqslant \int_{\{x \in X:|f(x)|>t\}} t^p d \mu=t^p \mu_f(t)
\end{aligned}$$

and so $\|f\|_p \geqslant t\left(\mu_f(t)\right)^{1 / p}$, for all $t>0$. This leads the following definition.

> [!definition]
> Let $(X, \mathcal{A}, \mu)$ be a measure space and $f: X \rightarrow \mathbb{C}$ be a measurable function. Define the distribution function as $\mu_f(t)=\mu(\{x \in X:|f(x)|>t\})$, and define
> 
> $$\|f\|_{p, w}=\begin{cases}\sup _{t>0} t\left(\mu_f(t)\right)^{1 / p}&1\leqslant p<\infty,\\ \|f\|_{\infty}& p=\infty.\end{cases}$$
> 
> which is called the *weak $p$-norm* of $f$. Furthermore, let us denote
> 
> $$L^{p, w}(X, \mu)=\left\{f: X \rightarrow \mathbb{C}:\|f\|_{p, w}<\infty\right\}.$$
>  
>  As in the $L^p$-space, we also regard functions in $L^{p, w}(X, \mu)$ which are equal a.e. as one function.

By construction we have $\|f\|_{p, w} \leq\|f\|_p$ when $1\leqslant p<\infty$. We have seen that $L^p(X, \mu) \subseteq L^{p, w}(X, \mu)$. Note that $f(x)=1/x\not\in L^1(\mathbb{R})$ with $t\mu_f(t)=2$, we have $\|f\|_{1,w}=2$ and it deduces that this inclusion is in general strict, that is $L^p(X, \mu) \subset L^{p, w}(X, \mu)$. 

> [!definition]
> Let $T$ be a map from some vector space $\mathcal{D}$ of measurable functions on $(X, \mathcal{A}, \mu)$ to the space of all measurable functions on $(Y, \mathcal{B}, \nu)$. $T$ is called *subadditive* if $|T(f+g)| \leqslant|T(f)|+|T(g)|$ and $|T(c f)|=c|T(f)|$ for all $f, g \in \mathcal{D}$ and $c>0$.
> 
> A subadditive operator $T$ is *strong type* $(p, q)$ with $1 \leqslant p, q \leqslant \infty$, if $L^p(\mu) \subset \mathcal{D}, T$ maps $L^p(\mu)$ into $L^q(\nu)$, and there exists $C>0$ such that
> 
> $$\|T(f)\|_q \leqslant C_{p, q}\|f\|_p, \forall f \in L^p(\mu) .$$
> 
> A subadditive operator $T$ is *weak type* $(p, q)$ with $1 \leqslant p, q<\infty$, if $L^p(\mu) \subset \mathcal{D}, T$ maps $L^p(\mu)$ into $L^{q, w}(\nu)$, and there exists $C_{p, q, w}>0$ such that
> 
> $$\|T(f)\|_{q, w} \leqslant C_{p, q, w}\|f\|_p, \forall f \in L^p(\mu) .$$
> 
> Also, we shall say that $T$ is weak type $(p, \infty)$ iff $T$ is strong type $(p, \infty)$.


> [!theorem] Marcinkiewicz
> Let $(X, \mathcal{A}, \mu)$ and $(Y, \mathcal{B}, \nu)$ be measure spaces and $1 \leqslant p_0<p_1 \leqslant \infty$. Let $T$ be a subadditive operator defined on $L^p(\mu), p \in\left[p_0, p_1\right]$. If $T$ is of weak type $\left(p_0, p_0\right)$ and $\left(p_1, p_1\right)$ then it is also of strong type $(p, p)$ for every $p_0<p<p_1$.

**_Proof._**
Firstly, assume that $p_1<\infty$. Fix $f \in L^p(\mu)$. By [[MATH/测度论/Nodes/9 LP Spaces#^a9aid4\|9 LP Spaces#^a9aid4]], we can take some number $r>0$ and decompose $f=f_0+f_1$ where $f_0=f \chi_{\{x:|f(x)|>r\}}$ and $f_1=f \chi_{\{x:|f(x)| \leq r\}}$. Then $f_0\in L^{p_0}\cap L^p$ and $f_1\in L^{p}\cap L^{p_1}$. We have

$$
\begin{aligned}
\|T(f)\|_p^p & =p \int_0^{\infty} r^{p-1} \nu_{T(f)}(r) d r \\
& =p \int_0^{\infty} r^{p-1} \nu(\{y \in Y:|T(f)(y)|>r\}) d r \\
& =p 2^p \int_0^{\infty} r^{p-1} \nu_{T(f)}(2 r) d r .
\end{aligned}
$$

Since $T$ is subadditive, there is $|T(f)|=\left|T\left(f_0+f_1\right)\right| \leqslant\left|T\left(f_0\right)\right|+\left|T\left(f_1\right)\right|$ and so $\nu_{T(f)}(2 r) \leqslant \nu_{T\left(f_0\right)}(r)+\nu_{T\left(f_1\right)}(r)$. Since $T$ is of weak type $\left(p_0, p_0\right)$ and of weak type $(p_1,p_1)$, we have

$$\nu_{T\left(f_0\right)}(r) \leqslant\left(\frac{C_0}{r}\right)^{p_0} \cdot\left\|f_0\right\|_{p_0}^{p_0}\mbox{ and }\nu_{T\left(f_1\right)}(r) \leqslant\left(\frac{C_1}{r}\right)^{p_1} \cdot\left\|f_1\right\|_{p_1}^{p_1}, \forall r>0.$$

Thus we have

$$\begin{aligned}
\|T(f)\|_p^p & \leqslant p 2^p\left(\int_0^{\infty} r^{p-1} \nu_{T\left(f_0\right)}(r) d r+\int_0^{\infty} r^{p-1} \nu_{T\left(f_1\right)}(r) d r\right) \\
& \leqslant p 2^p\left(\int_0^{\infty} r^{p-1}\left(\frac{C_0}{r}\right)^{p_0} \cdot\left\|f_0\right\|_{p_0}^{p_0}+\int_0^{\infty} r^{p-1}\left(\frac{C_1}{r}\right)^{p_1} \cdot\left\|f_1\right\|_{p_1}^{p_1}\right) d r
\end{aligned}$$

Observe that $\left\|f_0\right\|_{p_0}^{p_0} =\int_{\{x \in X:|f(x)|>r\}}|f|^{p_0} d \mu$ and $\left\|f_1\right\|_{p_1}^{p_1}=\int_{\{x \in X:|f(x)| \leq r\}}|f|^{p_1} d \mu$, then $\|T(f)\|_p^p \leq p 2^p\left(C_0^{p_0} I_0+C_1^{p_1} I_1\right)$, where

$$
\begin{aligned}
I_0 & =\int_0^{\infty}\left[\int_{\{x \in X:|f(x)|>r\}} r^{p-p_0-1}|f|^{p_0} d \mu\right] d r \\
& =\int_0^{\infty}\left[\int_X r^{p-p_0-1}|f|^{p_0} \chi_{\left\{(x, r) \in X \times \mathbb{R}^{+}:|f(x)|>r\right\}} d \mu\right] d r \\
& =\int_X\left[\int_0^{\infty} r^{p-p_0-1}|f|^{p_0} \chi_{\left\{(x, r) \in X \times \mathbb{R}^{+}:|f(x)|>r\right\}} d r\right] d \mu \\
& =\int_X\left[\int_0^{|f|} r^{p-p_0-1}|f|^{p_0} d r\right] d \mu=\frac{1}{p-p_0} \|\left. f\right\|_p
{ #p}
,
\end{aligned}
$$

and

$$
\begin{aligned}
I_1 & =\int_0^{\infty}\left[\int_{\{x \in X:|f(x)| \leq r\}} r^{p-p_1-1}|f|^{p_1} d \mu\right] d r \\
& =\int_X\left[\int_{|f|}^{\infty} r^{p-p_1-1}|f|^{p_1} d r\right] d \mu=\frac{1}{p_1-p}\|f\|_p^p
\end{aligned}
$$


Hence, $\|T(f)\|_p \leqslant C\|f\|_p$ and so $T$ is of strong type $(p,p)$. 

Now assume that $p_1=\infty$. In this case, we have $\|T(g)\|_{\infty} \leqslant C_1\|g\|_{\infty}$ for all $g \in L^{\infty}(\mu)$, and $\|T(h)\|_{p_0, w} \leqslant C_0\|h\|_{p_0}$ for all $h \in L^{p_0}(\mu)$. The case $C_1=0$ can be settled easily, and then we assume that $C_1>0$. Let $f \in L^p(\mu)$ and set

$$f_0=f \chi_{\left\{x \in X:|f(x)|> \frac{r}{C_1}\right\}} \in L^{p_0} \cap L^p \mbox{ and } f_1=f \chi_{\left\{x \in X:|f(x)| \leq \frac{r}{C_1}\right\}} \in L^p \cap L^{\infty} .$$

Since $\left\|f_1\right\|_{\infty} \leqslant r / C_1$, we have $\left\|T\left(f_1\right)\right\|_{\infty} \leqslant r$, which implies that $\nu_{T\left(f_1\right)}(r)=\nu\left(\left\{y \in Y:\left|T\left(f_1\right)(y)\right|>r\right\}\right)=0$. Hence

$$\begin{aligned}
\nu_{T(f)}(2 r) & \leqslant \nu_{T\left(f_0\right)}(r)+\nu_{T\left(f_1\right)}(r)=\nu_{T\left(f_0\right)}(r) \\
& \leqslant \frac{C_0^{p_0}}{r^{p_0}}\left\|f_0\right\|_{p_0}^{p_0}=\frac{C_0^{p_0}}{r^{p_0}} \int_{\left\{x \in X:|f(x)|>\frac{r}{C_1}\right\}}|f|^{p_0} d \mu.
\end{aligned}$$

It then follows from the same calculations as in the case 1 that

$$
\begin{aligned}
\|T(f)\|_p^p & =p 2^p \int_0^{\infty} r^{p-1} \nu_{T(f)}(2 r) d r \\
& \leqslant p 2^p C_0^{p_0} \int_0^{\infty}\left[\int_{\left\{x \in X:|f(x)|>\frac{r}{C_1}\right\}} r^{p-p_0-1}|f|^{p_0} d \mu\right] d r \\
& =p 2^p C_0^{p_0} \int_X|f(x)|^{p_0}\left[\int_0^{C_1|f(x)|} r^{p-p_0-1} d r\right] d \mu \\
& =\frac{p 2^p C_0^{p_0} C_1^{p-p_0}}{p-p_0} \int_X|f|^p d \mu .
\end{aligned}
$$

Therefore, $\|T(f)\|_p \leqslant 2\left(\frac{p}{p-p_0}\right)^{1 / p} C_0^{p_0 / p} C_1^{1-p_0 / p}\|f\|_p$ and so $T$ is of strong type $(p,p)$. 
<p align="right">□</p>



