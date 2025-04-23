---
{"dg-publish":true,"permalink":"/MATH/测度论/Nodes/10 Lebesgue Measure/","dgPassFrontmatter":true}
---


> [!theorem] Carathéodory criterion
> Let $(X, d)$ be a metric space. Consider an outer measure $\mu^*: \mathcal{P}(X) \rightarrow[0, \infty]$. Let $\mathcal{A}\left(\mu^*\right)$ be the $\sigma$-algebra consisting of $\mu^*$-measurable subsets of $X$ and $\mathcal{B}(X) \subset \mathcal{P}(X)$ be the Borel $\sigma$-algebra of $(X, d)$. Then the following statements are equivalent:
> - $\mathcal{B}(X) \subset \mathcal{A}\left(\mu^*\right)$;
> - if $A, B \subset X$ satisfy $d(A, B):=\inf _{a \in A, b \in B} d(a, b)>0$; then $\mu^*(A \cup B)=$ $\mu^*(A)+\mu^*(B)$.

**_Proof._**
"->": Let $A,B\subseteq X$ with $d(A,B)>0$. Take open $U$ of $X$ such that $A\subseteq U$ and $U\cap B=\emptyset$. Since $U\in\mathcal A(\mu^*)$, we have 

$$\mu^*(A\cup B)=\mu^*(A\cup B\cap U)+\mu^*(A\cup B\cap U^c)=\mu^*(A)+\mu^*(B).$$

"<-": Fix a closed set $A\subseteq X$, then we aim to show for any $D\subseteq X$ there is 

$$\mu^*(D)\geqslant\mu^*(D\cap A)+\mu^*(D\cap A^c).$$

WLOG we may assume $\mu^*(D)<\infty$. Define $U_k=\cup_{a\in A}B(a,\frac{1}{k})$, then $d(D\cap A,D-U_k)\geqslant\frac{1}{k}>0$ and so 

$$\mu^*(D)\geqslant\mu^*((D\cap A)\cup( D-U_k))=\mu^*(D\cap A)+\mu^*(D-U_k).$$

Claim that $\lim_{k\to\infty}\mu^*(D-U_k)=\mu^*(D\setminus A)$. Since $A=\cap_{k=1}^\infty U_k$, we have that $D-A=(D-U_k)\cup ((U_k-A)\cap D)$. It follows that $\mu^*(D-A)\leqslant \mu^*(D-U_k)+\mu^*((U_k-A)\cap D)$. Note that $U_k-A=U_k-\cap_{j=1}^\infty U_k=\cup_{j=k}^\infty(U_{j}-U_{j+1})$ and $D\cap(U_k-A)=\cup_{j=k}^\infty(D\cap U_j-U_{j+1})=\cup_{j=k}^\infty E_j$ where $E_j=D\cap U_j-U_{j+1}$. 

Sub-claim that $\sum_{j=1}^\infty \mu^*(E_j)<\infty$. If $d(E_i,E_j)>0$ for any $j\geqslant i+2$, then we have $\mu^*(D)\geqslant\mu^*(\cup_{i=1}^\ell E_{2i})=\sum\mu^*(E_{2i})$, $\mu^*(D)\geqslant\mu^*(\cup_{i=1}^\ell E_{2i-1})=\sum \mu^*(E_{2i-1})$ and so $\sum_{k=1}^\infty \mu^*(E_i)\leqslant 2\mu^*(D)<\infty$. Thus, we only need to show $d(E_i,E_j)>0$ if $j\geqslant i+2$. If $x\in E_i$, $y\in X$ and $d(x,y)<\frac{1}{(i+1)(i+2)}$, then $y\not\in E_j$ by the definition of $U_j$. Now we finish the proof.
<p align="right">□</p>

**Remark.** 学实变的时候我好像管这个证明叫瑞士卷来着。


> [!theorem]
> Let $\mu^*$ be the Lebesgue outer measure on $\mathcal{P}(\mathbb{R}^n)$. Then:
> - $\mu^*(A+x)=\mu^*(A)$ for any $x\in \mathbb{R}^n$;
> - if $\forall A,B\subseteq \mathbb{R}^n$ with $d(A,B)>0$, then $\mu^*(A\cup B)=\mu^*(A)+\mu^*(B)$;
> - for any $Q$, $\mu^*(Q)=|Q|=\mu^*(Q^0)$.

**_Proof._**
i) & ii) are easy, but iii) is tricky. Note that $|Q|=\lim_{N\to\infty}\frac1{N^n}\#(Q\cap \frac1N \mathbb{Z}^n)$. We use it to show for any $\cup_{i=1}^\infty Q_i\supseteq Q$, there is $|Q|\leqslant \sum |Q_i|$. To make sure RHS converges, take open $U_i\supseteq Q_i$ and consider its open cover of $Q$.

Also see [[Measure  Theory    (Xia).pdf#page=69&selection=495,0,496,0|here]].
<p align="right">□</p>

**Remark.** 把算体积变成算格点数. As a corollary of ii), elements in $\mathcal{B}(\mathbb{R}^n)$ are Lebesgue measurable.


> [!theorem] regularity of the Lebesgue outer measure
> The followings hold.
> - Let $A\subseteq \mathbb{R}^n$. Then $\mu^*(A)=\inf\{\mu^*(U):U\mbox{ is open, }A\subseteq U\}$.
> - If $A\in \mathcal L(\mathbb{R}^n)$, then $\mu^*(A)=\sup\{\mu^*(K):K\subseteq A,K\mbox{ is compact}\}$.
> - If $\{A_i\}\subseteq \mathcal{P}(\mathbb{R}^n)$ and $A_i\uparrow A$, then $\mu^*(A)=\lim_{i\to\infty}\mu^*(A_i)$.
{ #7b1c20}


**_Proof._**
i) and ii) are Easy. See [[Measure  Theory    (Xia).pdf#page=72&selection=207,0,208,0|here]]. 

iii) If $\mu^*(A)=\infty$, done. Let $\mu^*(A)<\infty$. For any $\epsilon>0$, there is open $U_i\supseteq A_i$ and $\mu^*(U_i)\leqslant \mu^*(A_i)+\epsilon$. Let $V_i=\cap_{j=i}^\infty U_j$. Then

$$\mu^*(A)\leqslant\mu^*(\cup_{i=1}^\infty V_i)=\lim_{i\to\infty}\mu^*(V_i)\leqslant \lim_{i\to\infty}\mu^*(U_i)\leqslant \lim_{i\to\infty}\mu^*(A_i)+\epsilon$$

and so we finish the proof.
<p align="right">□</p>


> [!theorem] the Lebesgue measure as a completion
> Let $\mu^*: \mathcal{P}\left(\mathbb{R}^n\right) \rightarrow$ $[0, \infty]$ be the Lebesgue outer measure, let $m=\left.\mu^*\right|_{\mathcal{L}\left(\mathbb{R}^n\right)}: \mathcal{L}\left(\mathbb{R}^n\right) \rightarrow[0, \infty]$ be the Lebesgue measure, let $\mathcal{B} \subset \mathcal{L}\left(\mathbb{R}^n\right)$ be the Borel $\sigma$-algebra of $\mathbb{R}^n$, and define
> 
> $$\nu=\left.\mu^*\right|_{\mathcal{B}}: \mathcal{B} \rightarrow[0, \infty]$$
> 
> Then $\left(\mathbb{R}^n, \mathcal{L}\left(\mathbb{R}^n\right), m\right)$ is the completion of $\left(\mathbb{R}^n, \mathcal{B}, \nu\right)$.

**_Proof._**
Use [[#^7b1c20]] to construct union of compact sets $B_0$ and intersection of open sets $B_1$ such that $B_0\subseteq A\subseteq B_1$ with $\mu^*(B_1-B_0)=0$. Also see [[Measure  Theory    (Xia).pdf#page=73&selection=358,0,359,1|here]]. 
<p align="right">□</p>


> [!theorem]
> Let $C_0(\mathbb{R}^n)$ be the set of continuous functions with compact support. Then $C_0(\mathbb{R}^n)$ is dense in $L^1(\mathbb{R}^n)$.
{ #110128}


**_Proof._**
It suffices to show, for any $f\in L^1(\mathbb{R}^n)$, there exists $g\in C_0(\mathbb{R}^n)$ with $||g-f||_1<\epsilon$. On the other word, there exists $\{f_k\}\subseteq C_0(\mathbb{R}^n)$ with $||f_k-f||_1\to 0$.

Let $\mathcal J=\{f\in L^1(\mathbb{R}):\exists \{f_k\}\subseteq C_0(\mathbb{R}^n),||f_k-f||_1\to 0\}$. We can show that 
- $\mathcal J$ is closed w.r.t. finite linear combinations.
- If $\{f_i\}\subseteq \mathcal J$ and $||f_k-f||_1\to 0$, then $f\in\mathcal J$.

Then we approximate $f$ with simple functions, and it is enough to show $\chi_E\in \mathcal J$ with $\mu^*(E)<\infty$ and so for $\chi_I$ with half open cube $I$. The last one is easy to prove. 

Also see [[Measure  Theory    (Xia).pdf#page=75&selection=253,0,254,0|here]]. 
<p align="right">□</p>


> [!theorem]
> The set of continuous functions with compact support is dense in $L^p\left(\mathbb{R}^n\right)$ for $1 \leqslant p<\infty$.
{ #fe0685}


**_Proof._**
Suppose $f \in L^p$. We have $\int_{\mathbb{R}^n}\left|f-f \chi_{B(0, n)}\right|^p \rightarrow 0$ as $n \rightarrow \infty$ by DCT. Hence it suffices to approximate functions in $L^p$ that have compact support. By writing $f=f^{+}-f^{-}$ we may suppose $f \geqslant 0$. 

Similarly as [[#^110128]], it suffices to approximate characteristic functions of any partly open cube. For any given partly open cube $I$, there exists $g$ continuous with compact support and with values in $[0,1]$ such that $\int_{\mathbb{R}^n}\left|g-\chi_I\right|<\epsilon$. Since $\left|g-\chi_I\right| \leqslant 1$, then $\int_{\mathbb{R}^n}\left|g-\chi_I\right|^p \leqslant \int_{\mathbb{R}^n}\left|g-\chi_I\right|<\epsilon$. This completes the proof.
<p align="right">□</p>


> [!theorem] Continuity in $L^p$
> Let $f \in L^p\left(\mathbb{R}^n\right), 1 \leq p<\infty$. Then
> 
> $$\lim _{|h| \rightarrow 0}\|f(\cdot+h)-f(\cdot)\|_p=0$$

**_Proof._**
Define the set $C_p$ as the class of $f\in L^p$ such that $||f(\cdot+h)-f(\cdot)||_p\to 0$ as $|h|\to 0$. Then $f$ is closed under finite linear combination and the convergence with norm $L^p$. Since the characteristic function of a cube is contained in $C_p$, by [[#^110128]] and [[#^fe0685]] we finish the proof. 

Also see [[Measure  Theory    (Xia).pdf#page=75&selection=521,0,522,1|here]].
<p align="right">□</p>


> [!theorem] transformation formula
> Suppose $\phi: U \rightarrow V$ is a $C^1$ diffeomorphism between open subsets of $\mathbb{R}^n$.
> - If $f: V \rightarrow[0, \infty]$ is Lebesgue measurable, then $f \circ \phi: U \rightarrow[0, \infty]$ is Lebesgue measurable and
> 
> $$\int_U(f \circ \phi)|\operatorname{det}(d \phi)| d m=\int_V f d m .$$
>
> - If $E \in \mathcal{L}_U$ and $f \in L^1\left(m_V\right)$, then $\phi(E) \in \mathcal{L}_V,(f \circ \phi)|\operatorname{det}(d \phi)| \in L^1\left(m_U\right)$ and
> 
> $$\int_E(f \circ \phi)|\operatorname{det}(d \phi)| d m=\int_{\phi(E)} f d m .$$

**Remark.** The proof is omitted. 
