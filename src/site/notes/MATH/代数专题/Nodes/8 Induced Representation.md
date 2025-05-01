---
{"dg-publish":true,"draft":false,"permalink":"/MATH/代数专题/Nodes/8 Induced Representation/","dgPassFrontmatter":true}
---


> [!definition]
> Assume that $G$ acts on $X$ with $X=\{x_1,\cdots,x_n\}$. Define $\mathbb{C}X=\mathbb{C}\left\langle x_1,\cdots,x_n\right\rangle$, then $\mathbb{C}X$ is a $G$-module, which is called permutation module associated with $X$.

**Example.** Let $G$ be a finite group and $H<G$, then we have a left coset decomposition

$$G=t_1H\sqcup \cdots\sqcup t_\ell H$$

and $G$ acts on $\mathcal H=\{t_1H,\cdots,t_\ell H\}$. Therefore, $\mathbb{C}\mathcal H$ is a $G$-module, which is called coset representation. 

# Restriction of Module

> [!definition]
> Let $G$ be a group and $H<G$ and $(V,\rho)$ is a representation of $G$, then $(V,\rho)$ is a representation of $H$, which is called restriction of $(V,\rho)$ to $H$, denoted by $V\downarrow_H$, $V\downarrow_H^G$ or $Res_H^G(V)$. 

**Remark.** Simple $G$-module $V$ is not necessarily simple $H$-module $V\downarrow_H^G$. 

# Induced Module

Now let $W$ be an $H$-module, then $\mathbb{C}G\otimes W$ is a $G$-module with respect to action $g(u\otimes w)=gu\otimes w$ with $g,u\in G$ and $w\in W$. Consider subspace $L$ in $\mathbb{C}G\otimes W$ spanned by 

$$\{uh\otimes w-u\otimes hw:h\in H,u\in G,w\in W\}.$$


Note that $L$ is a $G$-module, i.e., $L$ is $G$-invariant.

> [!definition]
> Let $H<G$, and let $W$ be an $H$ module. Define $L=\mathrm{span}\{uh\otimes w-u\otimes hw:h\in H,u\in G,w\in W\}$, then $\mathbb{C}G\otimes W/L$ is an $G$-module called induced module from an $H$-module $W$, denoted by $W\uparrow_H^G$, $W\uparrow^G$, or $Ind_H^G(W)$.

**Remark.** For details, look into file on tensor product of two modules over ring $R$.
- [[tensor-product.pdf]]
- [[tensorproduct2.pdf|tensor-product2.pdf]]

> [!proposition]
> For a finite group $G$, given a left coset decomposition $G=t_1H\sqcup\cdots\sqcup t_\ell H$, the vector space 
> 
> $$W\uparrow_H^G\simeq(t_1\otimes W)\oplus\cdots\oplus (t_\ell\otimes W)$$
> 
> and $\dim W\uparrow_H^G=\ell\cdot \dim W=\frac{|G|}{|H|}\dim W$. 
{ #hp5t8s}


**_Proof._**
Note that

$$\begin{aligned}
&\mathbb{C}G=\mathbb{C}(t_1H)\oplus\cdots\oplus \mathbb{C}(t_\ell H)=t_1\mathbb{C}H\oplus\cdots\oplus t_\ell \mathbb{C}H,\\
& \mathbb{C}G\otimes W=(t_1\mathbb{C}H\otimes W)\oplus\cdots\oplus (t_\ell \mathbb{C}H\otimes W).
\end{aligned}$$

On the other hand, for any $g\in G$ and $h\in H$, 

$$\begin{aligned}
gh\otimes w-g\otimes hw&=t_1kh\otimes w-t_1k\otimes hw\\
&=t_1(kh\otimes w-1\otimes khw+1\otimes khw-k\otimes hw).
\end{aligned}$$

Define $L_0=\mathrm{span}\{h\otimes w-1\otimes hw:h\in H,w\in W\}$, then $L=t_1L_0\oplus\cdots\oplus t_\ell L_0$. Note that $\mathbb{C}H\otimes W\simeq L_0\oplus(1\otimes W)$ as vector space. Then we have 

$$\mathbb{C}G\otimes W/L\simeq (t_1\mathbb{C}H\otimes W/L_0)\oplus\cdots\oplus (t_\ell \mathbb{C}H\otimes W/L_0)\simeq(t_1\otimes W)\oplus\cdots\oplus (t_{\ell}\otimes W),$$

and so $\dim (\mathbb{C}G\times W/L)=|G|/|H|\dim W$.
<p align="left">□</p>

**Example.** Let $G=S_3$ and $H=S_2$. Define $W=\mathbb{C}[1,2]$, then $W$ is a permutation $H$-module. A basis of $Ind_H^GW$ is 

$$1\otimes 1,1\otimes 2,(13)\otimes 1,(13)\otimes 2,(23)\otimes 1,(23)\otimes 2$$

as $S_3=S_2\sqcup (13)S_3\sqcup (23)S_2$. In the other word, the basis of $Ind_H^GW$ can be identified as $t_j\otimes w_i$ where $t_j\in\{t_1,\cdots,t_{\ell}\}$ and $w_i$ runs over a basis of $W$. 

**Example.** Let $H<G$. Consider the trivial module of $H$. A basis of $Ind_H^G\mathrm{tr}$ is 

$$t_1\otimes 1,\cdots,t_\ell\otimes 1$$

and $g(t_i\otimes 1)=t_jk\otimes 1=t_j\otimes 1$ for some $k\in H$. We say $\mathrm{tr}\uparrow^G=\mathbb{C}[t_1H_1,\cdots,t_\ell H]$ the coset representation of $G$. 


For a general $H$-module $W$, we want to compute character of $Ind_H^GW$. The corresponding matrix of $g$ is a permutation block matrix with each block being $Y(t_i^{-1}gt_j)$. Here $Y$ is defined as $H\to\mathrm{GL}(W)$. See [[Pasted image 20241028145247.png|here]].


> [!proposition]
> Let $W$ be a $H$-module with character $\psi$, then $\psi\uparrow_H^G(g)=\frac{1}{|H|}\sum_{x\in G}\psi(x^{-1}gx)$ with the convention that $\psi(g)=0$ if $g\not\in H$. 

**_Proof._**
By the argument above, $\psi\uparrow_H^G=\sum_{i=1}^\ell\mathrm{tr}Y(t_i^{-1}gt_i)$. Since $\psi$ is constant on conjugacy class, there is

$$\sum_{i=1}^\ell\mathrm{tr}Y(t_i^{-1}gt_i)=\frac{1}{|H|}\sum_{i=1}^\ell\sum_{h\in H}\psi(h^{-1}t_i^{-1}gt_ih)=\frac{1}{|H|}\sum_{x\in G}\psi(x^{-1}gx)$$

and now we finish the proof.
<p align="left">□</p>

> [!corollary]
> $\psi\uparrow_H^G(g)=\sum_{i=1}^\ell\psi(t_i^{-1}gt_i)$. 

