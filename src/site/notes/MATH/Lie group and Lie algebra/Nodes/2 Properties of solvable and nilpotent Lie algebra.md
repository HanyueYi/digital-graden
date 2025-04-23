---
{"dg-publish":true,"permalink":"/MATH/Lie group and Lie algebra/Nodes/2 Properties of solvable and nilpotent Lie algebra/","dgPassFrontmatter":true}
---

# Solvable Lie Algebra

## Existence of Weight Space

We show that every finite dimensional complex representation of a solvable Lie algebra has a weight space:


<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



> [!proposition]
>  For a finite dimensional complex solvable Lie algebra $g$ and its finite dimensional complex representation $(\rho,g)$, this representation has a weight.

</div></div>


Then we have the following corollary:

> [!corollary]
> Every irreducible representation of finite dimensional solvable Lie algebra is $1$-dimensional.
{ #115533}


> [!question] 
> Conversely, for a Lie algebra $g$, if every finite dimensional complex representation of $g$ has a weight, would it must be solvable? 

> [!note] Answer
> The answer is yes. Consider the adjoint representation. Since $\mathrm{ad}:g\to\mathrm{End}(g)$ is an representation, using the same argument in [[MATH/Lie group and Lie algebra/Nodes/2 Properties of solvable and nilpotent Lie algebra#^e008cf\|Lie's theorem]], there exists a set of basis such that $\mathrm{ad}g$ are upper triangular matrices. Then $\mathrm{ad}([g,g])$ are nilpotent. By [[MATH/Lie group and Lie algebra/Nodes/2.2 Engel's theorem#^e1bcc4\|Engel's theorem]], $[g,g]$ is nilpotent and so $g$ is solvable by [[MATH/Lie group and Lie algebra/Nodes/2 Properties of solvable and nilpotent Lie algebra#^2be7fe\|#^2be7fe]].

> [!proposition] Lie's theorem
> Let $g$ be a finite dimensional solvable Lie algebra over $\mathbb C$ and $(\rho,V)$ a finite dimensional representation. Then one can choose a basis $\{v_1,\cdots,v_n\}$ of $V$ and $\rho(g)\subseteq\{\text{ upper triangular matrices }\}$ w.r.t. the identification $\mathrm{End}(V)\cong M_{n\times n}(\mathbb C)$.
{ #e008cf}


**_Proof._**Since $g$ is solvable, there is a weight $U\subseteq V$ and $\rho|_U$ is diagonalizable. Let $U=\mathrm{span}\{v_1,\cdots,v_t\}$. Then consider $\tilde\rho:g\to V/U$, still $\tilde \rho$ has a weight $\widetilde{U_1}$.  Let $U_1$ be the preimage of $\widetilde{U_1}$ and $U_1=\mathrm{span}\{v_1,\cdots,v_t,v_{t+1},\cdots,v_m\}$. Then repeat the procedure, that is consider ${\tilde\rho}':g\to V/U_1$ and its weight until we get a set of basis of $V$. It is easy to verify under this basis $\rho(g)\subseteq\{\text{ upper triangular matrices }\}$. 
<p align="left">□</p>

## Finest Ideal Sequence

> [!proposition]
> A finite dimensional Lie algebra is solvable iff it admits a sequence of ideals 
> 
> $$0=I_0\subsetneq I_1\subsetneq\cdots\subsetneq I_{n-1}\subsetneq I_n=g\tag{*}$$
> 
> with $\dim I_k=k$.

**_Proof._**i) If $g$ is solvable, then $g\supseteq g^{(1)}\supseteq\cdots\supseteq g^{(n)}=0$. Note that any subspace contains $[g,g]=g^{(1)}$ is an ideal, so there is a sequence of ideals

$$g^{(1)}\subsetneq g^{(1)}\oplus\mathbb CY_1\subsetneq\cdots\subsetneq g^{(1)}\oplus (\mathbb CY_1\oplus\cdots\oplus\mathbb CY_k)\subsetneq g$$

where $Y_i\in g\backslash g^{(1)}$. Similarly, use $Z_i\in g^{(1)}\backslash Y^{(2)}$ to construct subsequence of $(*)$ between $g^{(2)}$ and $g^{(1)}$. Repeat this process and get the sequence we want.

ii) Conversely, suppose $g$ admits a sequence $(*)$. Take a set of basis $\{e_1,\cdots,e_n\}$ such that $I_k=\mathrm{span}\{e_1,\cdots,e_k\}$. Then under this basis $\mathrm{ad}X$ is an upper triangular matrix for any $X\in g$, and so $\mathrm{ad}([g,g])$ are nilpotent. By [[MATH/Lie group and Lie algebra/Nodes/2.2 Engel's theorem#^e1bcc4\|Engel's theorem]], $[g,g]$ is nilpotent and so $g$ is solvable by [[MATH/Lie group and Lie algebra/Nodes/2 Properties of solvable and nilpotent Lie algebra#^2be7fe\|#^2be7fe]].
<p align="left">□</p>
## Unique Maximal Nilpotent Ideal of Solvable Lie Algebra

> [!corollary]
> Let $g$ be a finite dimensional complex Lie algebra. Then
> - $g$ is solvable $\iff$ $[g,g]$ is nilpotent;
> - when $g$ is solvable, $g$ has a unique maximal nilpotent ideal 
> 
> $$n=\{x\in g:\mathrm{ad}X\text{ is nilpotent }\}.$$
> 
>
{ #2be7fe}


**_Proof._**i) $[g,g]$ nilpotent $\Rightarrow$ $g$ solvable is trivial. Now assume $g$ is solvable. Then $\mathrm{ad}g$ can be represented by upper triangular matrices. So elements of $\mathrm{ad}[g,g]$ can be represented by strictly upper triangular matrices. By [[MATH/Lie group and Lie algebra/Nodes/2.2 Engel's theorem#^e1bcc4\|Engel's theorem]], $[g,g]$ is nilpotent.

ii) Since $g$ is solvable, we have the following diagram.

![Pasted image 20231010164310.png](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020231010164310.png)

Thus $n$ is a nilpotent ideal. Let $n'$ be a nilpotent ideal. Since $n'$ is nilpotent, for each $Y\in n'$, $\mathrm{ad}(Y)$ is nilpotent. Then $Y\in n$ yields $n'\subseteq n$ and $n$ is the unique maximal nilpotent ideal. <p align="left">□</p>


> [!Warning] Open Question
> Could we "classify" all complex representation of a finite dimensional solvable Lie algebra?

# Nilpotent Lie algebra

## Decomposed as Direct Sum of Generalized Weight Space

Every representation of a nilpotent Lie algebra can be decomposed as a direct sum of generalized weight space. See [[MATH/Lie group and Lie algebra/Nodes/2.1 Existence of (generalized) weight space#Nilpotent Lie algebra\|here]].

> [!question]
> If its each finite dimensional complex representation can be decomposed as a direct product sum of generalized weight spaces, would it must be nilpotent? 

> [!note] Answer
> The answer is yes, and we prove it [[MATH/Lie group and Lie algebra/Nodes/0.0 Exercise#^167cef\|here]].

## Engel's Theorem


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/math/lie-group-and-lie-algebra/nodes/2-2-engel-s-theorem/#e1bcc4" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



> [!theorem] Engel's theorem
> Let $g$ be a finite dimensional complex Lie algebra. Then $g$ is nilpotent $\iff$ $\mathrm{ad}X$ is nilpotent for each $X\in g$. 

</div></div>


This theorem is proved [[MATH/Lie group and Lie algebra/Nodes/2.2 Engel's theorem\|here]], and we get the following corollary.

> [!corollary]
> Let $g$ be a finite dimensional complex Lie algebra. Then $g$ is nilpotent iff it has a basis w.r.t. which the adjoint representation sends $g$ into the space spanned by strictly upper triangular matrices.

**_Proof._**i) Suppose any $\mathrm{ad}X$ is upper triangular matrix. By Cayley-Hamilton $\mathrm{ad}X$ is nilpotent. Then $g$ is nilpotent by [[MATH/Lie group and Lie algebra/Nodes/2.2 Engel's theorem#^e1bcc4\|Engel's theorem]]. 

ii) Suppose $g$ is nilpotent. Then $g$ is solvable and there is a basis s.t. $\mathrm{ad}X$ is upper triangular for all $X\in g$. By [[MATH/Lie group and Lie algebra/Nodes/2.2 Engel's theorem#^e1bcc4\|Engel's theorem]], $\mathrm{ad}X$ is nilpotent. By Cayley-Hamilton $\mathrm{ad}X$ is strictly upper triangular matrix. 
<p align="left">□</p>

