---
{"dg-publish":true,"aliases":"layer cake representation","permalink":"/MATH/Cards/Nodes/Layer Cake Representation/","dgPassFrontmatter":true}
---


> [!definition]
> Let $f$ be a non-negative, real-valued measurable function $f$ defined on a measure space $(\Omega,\mathcal{A},\mu)$. Define 
> 
> $$L(f, t)=\{y \in \Omega \mid f(y) \geqslant t\},$$
> 
> then we have 
> 
> $$f(x)=\int_0^\infty\chi_{L(f,t)}(x)dt,$$
> 
> which is called the *layer cake representation* of $f$.


By applying the [[MATH/测度论/Nodes/11 Product measures, Tonelli, Fubini theorems#^67db20\|Fubini-Tonelli theorem]] (see [[Measure  Theory    (Xia).pdf#page=81&selection=361,0,362,0|here]]), there is

$$
\int_{\Omega} f(x) \mathrm{d} \mu(x)=\int_0^{\infty} \mu(\{x \in \Omega \mid f(x)>t\}) \mathrm{d} t.\tag{*}
$$

For any $f\in L^p$ for $1 \leqslant p<\infty$, by $(*)$ with the change of variables $t=s^p$ and $f:=|f|^p$, we have

$$\int_{\Omega}|f(x)|^p \mathrm{~d} \mu(x)=p \int_0^{\infty} s^{p-1} \mu(\{x \in \Omega: | f(x) |>s\}) \mathrm{d} s.$$
{ #pa9wsk}



