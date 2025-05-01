---
{"dg-publish":true,"draft":false,"permalink":"/MATH/代数专题/Nodes/7 Character Table, Frobenius-Schur Indicator & Complexification/","dgPassFrontmatter":true}
---


> [!proposition]
> For a character table,
> - the rows as "weighted" orthogonal by [[MATH/代数专题/Nodes/6 Inner product & Schur's orthogonality relations#^rld430\|Schur's orthogonality relations]];
> - for columns $j$ and $j'$, 
> $$\sum_{i=1}^r\chi_i(C_j)\overline{\chi_i(C_j')}=\frac{|G|}{|C_j|}\delta_{jj'};$$
> 
> - the matrix $U=\left[\sqrt\frac{|C_j|}{|G|}\right]\chi_i(C_j)$ satisfies $UU^*=\mathrm{I}$, where $U^*=\overline U^T$;
> - the complex conjugate of a row is a row of the character table by $\overline\chi_s=\chi_{s^*}$ (possible the same);
> - the complex conjugate of a column is also a column by $\overline{\chi_s(g)}=\chi_s(g^{-1})$ (possible the same);
> - (twisting) the pointwise product of a row starting with $1$ with any other row is again a row;
> - the pointwise product of any two rows is a linear combination of rows of the character table with non-negative integer coefficients.

**Example.** Different groups with the same character table: $D_8$ and $Q_8$. 

# Frobenius-Schur Indicator

> [!definition]
> Frobenius-Schur indicator is defined as $FS(\chi)=\frac{1}{|G|}\sum_{g\in G}\chi(g^2)$, where $\chi$ is an irreducible character. 

**Remark.** For compact group and its irreducible character $\chi$, define $FS(\chi)=\int_{g\in G}\chi(g^2)d\mu$ where $\mu$ is Haar measure with $\mu(G)=1$ in Gordon Liebeck, real representation.

> [!theorem]
> Let $\chi$ be an irreducible character. Then 
> 
> $$FS(\chi)= \begin{cases} 1 & \mbox{if }\chi\mbox{ is real-valued and }S_i\mbox{ is of symmetric type} \\ 0 & \mbox{if }\chi\mbox{ is not real-valued}\\ -1 & \mbox{if }\chi\mbox{ is real-valued and }S_i\mbox{ is of skew symmetric type} \end{cases}$$
> 
> where $S_i$ is called of symmetric (rep. skew-symmetric) type if it has a non-zero symmetric (rep. skew-symmetric) $G$-invariant form.
{ #df16b3}



> [!definition]
> We say that $S_i$ is symmetric (rep. skew-symmetric) type if $S_i$ admits non-zero symmetric (rep. skew-symmetric) $G$-invariant bilinear form. A bilinear map $B:V\times V\to \mathbb{C}$ is called a bilinear form, and is called
> - $G$-invariant if $B(gv_1,gv_2)=B(v_1,v_2)$;
> - symmetric if $B(v_1,v_2)=B(v_2,v_1)$;
> - skew-symmetric if $B(v_1,v_2)=-B(v_2,v_1)$.

**Remark.** If $S_i$ has character $\chi_i$, then $\overline \chi_i$ is a character of $S_i^*$. Then:
- if $S_i$ is irreducible, then $S_i^*$ is irreducible as well;
- $\chi_i$ is real-valued iff $\chi_i=\overline\chi_i$ iff $S_i$ is self-dual.


# Tensor Square

If $V$ is a vector space, then $V\otimes V=\mathrm S^2V\otimes\Lambda^2 V$. If $v_1,\cdots,v_n$ is basis of $V$, then $v_i\otimes v_j$ is basis of $V\otimes V$ and

$$\begin{aligned}
\mathrm S^2V&=\left\langle v_i\otimes v_j+v_j\otimes v_i:1\leqslant i\leqslant j\leqslant n\right\rangle,\\
\Lambda^2V&=\left\langle v_i\otimes v_j-v_j\otimes v_i:1\leqslant i<j\leqslant n\right\rangle. 
\end{aligned}$$

Define $P:V\otimes V\to V\otimes V,v_i\otimes v_j\to v_j\otimes v_i$, then $P$ preserves $\mathrm S^2V$ and $\Lambda^2V$. Note that $\mathrm S^2V$ (rep. $\Lambda^2V$) is the eigenspace of $P$ corresponding to eigenvalue $1$ (rep. $-1$). It yields that $\mathrm S^2V=\ker(P-I)$ and $\Lambda^2V=\ker(P+I)$. Since $P^2=\mathrm{id}$, we can check that $\dim \mathrm S^2V=n(n+1)/2$, $\dim \Lambda^2V=n(n-1)/2$ and $V\otimes V=\mathrm S^2V\oplus \Lambda^2V$. 

If $V=S_i$, then

$$(S_i\otimes S_i)^G\simeq \left(\mathrm{Hom}(S_i^*,S_i)\right)^G\simeq\mathrm{Hom}_G(S_i^*,S_i)$$

and so 

$$\dim\mathrm{Hom}_G(S_i^*,S_i)=\begin{cases}
1,\mbox{ if }S_i\mbox{ is self-dual,} \\
0,\mbox{ if }S_i\mbox{ is not self-dual.}
\end{cases}$$

Note that $(S_i\otimes S_i)^G=(\mathrm S^2 S_i)^G\oplus(\Lambda^2S_i)^G$. Hence, if $S_i$ is self-dual, then $\dim(S_i\otimes S_i)^G=1$ and one of the following holds:
{ #efck4j}

- $\dim (\mathrm S^2S_i)^G=1$ and $\dim(\Lambda^2S_i)^G=0$, which will correspond to symmetric type of $S_i$;
- $\dim (\mathrm S^2S_i)^G=0$ and $\dim(\Lambda^2S_i)^G=1$, which will correspond to skew-symmetric type of $S_i$.

> [!lemma]
> Let $V$ be $G$-module, then
> - $\chi_{\mathrm S^2V}(g)=\frac{1}{2}(\chi_V(g)^2+\chi_V(g^2))$;
> - $\chi_{\Lambda^2V}(g)=\frac{1}{2}(\chi_V(g)^2-\chi_V(g^2))$;
>- $\chi_{V\otimes V}(g)=\chi_V(g)^2=\chi_{\mathrm S^2V}(g)+\chi_{\Lambda^2V}(g)$.

**_Proof._**
Since $G$ is finite, $\rho(g)$ has finite order and so $\rho(g)$ is diagonalizable for all $g\in G$. For a fixed $G$ and vector space $V$, we have basis of eigenvectors $v_1,\cdots,v_n$ of $\rho(g)$ such that $\lambda_1,\cdots,\lambda_n$ are corresponding eigenvalues. It follows that

$$\chi_{\mathrm{S}^2V}(g)=\sum_{1\leqslant i\leqslant j\leqslant n}\lambda_i\lambda_j=\frac{1}{2}\left(\sum_{i=1}^n\lambda_i^2+(\sum_{i=1}^n\lambda_i)^2\right)=\frac{1}{2}(\chi(g)^2+\chi_V(g^2)).$$

Similarly, there is

$$\chi_{\Lambda^2V}(g)=\frac{1}{2}(\chi_V(g)^2-\chi_V(g^2))$$

and now we finish the proof.
<p align="left">□</p>


Now we are ready to prove [[MATH/代数专题/Nodes/7 Character Table, Frobenius-Schur Indicator & Complexification#^df16b3\|#^df16b3]].

**_Proof._**
Note that 

$$\begin{aligned}
FS(\chi_i)&=\frac{1}{|G|}\sum_{g\in G}\chi_i(g^2)=\frac{1}{|G|}\sum_{g\in G}(\chi_{\mathrm{S}^2S_i}(g)-\chi_{\Lambda^2S_i}(g))\\
&=\left\langle\chi_{\mathrm{S}^2S_i},1\right\rangle-\left\langle\chi_{\Lambda^2S_i},1\right\rangle=\dim (\mathrm{S}^2S_i)^G-\dim(\Lambda^2S_i)^G\\
&=\begin{cases} 1 & \mbox{if }\chi\mbox{ is real-valued and }S_i\mbox{ is of symmetric type} \\ 0 & \mbox{if }\chi\mbox{ is not real-valued}\\ -1 & \mbox{if }\chi\mbox{ is real-valued and }S_i\mbox{ is of skew symmetric type} \end{cases}
\end{aligned}$$
     
by [[MATH/代数专题/Nodes/7 Character Table, Frobenius-Schur Indicator & Complexification#^efck4j\|here]]. 
<p align="left">□</p>


**Exercise.** Let $V$ be vector space, then $Bil(V)$ is a vector space of bilinear forms on $V$ Show that $V^*\otimes V^*\simeq Bil(V)$. (I think it is easy, with $f\otimes f'\mapsto B(v,u):=f(v)f'(u)$.)

Now consider $P:V^*\otimes V^*\to V^*\otimes V^*,v^*\otimes u^*\to u^*\otimes v^*$. Since $Bil(V)\simeq V^*\otimes V^*$, we have that $\mathrm{S}^2V$ is the space of symmetric bilinear forms on $V$ and $\Lambda^2V$ is the space of skew-symmetric bilinear forms on $V$. If $V$ is $G$-module, then $V^*\otimes V^*$ is also $G$-module as well, by $g(f\otimes h)(u\otimes v)=f(g^{-1}u)\otimes h(g^{-1}v)$. 

If $B\in Bil(V)$ is $G$-invariant, then $(gB)(u,v)=B(g^{-1}u,g^{-1}v)=B(u,v)$ and so the space of $G$-invariant bilinear form is $(V^*\otimes V^*)^G$. Recall that

$$(V^*\otimes V^*)^G=(\mathrm S^2V^*)^G\oplus(\Lambda^2 V^*)^G,$$

and it yields that the space of $G$-invariant bilinear form can be decomposed as the space of symmetric $G$-invariant bilinear forms and the space of skew $G$-invariant bilinear forms. In fact, for each $f(u,v)\in Bil(V)$, it can be written as $f=f_1+f_2$ where $f_1(u,v)=f(u,v)+f(v,u)$ and $f_2(v,u)=f(u,v)-f(v,u)$. The decomposition above coincides with [[MATH/代数专题/Nodes/7 Character Table, Frobenius-Schur Indicator & Complexification#^efck4j\|it]] and we also have names *real*, *complex* and *quaternionic* type for symmetric, complex and skew-symmetric.

**Remark.** From linear algebra, odd dimensional space cannot have a non-degenerate skew symmetric bilinear form. Hence, if $S_i$ is self-dual and of odd dimension, then $S_i$ is of symmetric type.

**Example.** Check $FS$ for characters of $D_8$ and $Q_8$. 
- Note that these two groups have the same character table.
- When $G=D_8$, $\{g^2:g\in G\}=\{1,1,1,1,1,1,a^2,a^2\}$ and $FS(\chi_5)=\frac{1}{8}(2\times 6+(-2)\times 2)=1$ and $FS(\chi_i)=1$ for $i=1,2,3,4$.
- When $G=Q_8$, $\{g^2:g\in G\}=\{1,1,-1,-1,-1,-1,-1,-1\}$ and $FS(\chi_5)=\frac{1}{8}(2\times 2+(-2)\times 6)=-1$ and $FS(\chi_i)=1$ for $i=1,2,3,4$, where $\chi_i$ is defined [[MATH/代数专题/Nodes/List 2#^tsqbbt\|here]].

# Complexification

Note that $2$-dimensional $D_4$ complex representation is just a complexification of $2$-dimensional real representation. 

If $U$ is a $\mathbb{R}G$-module, then $\mathbb{C}\otimes_{\mathbb{R}}U$ is a $\mathbb{C}G$-module. That is, if $\{u_1,\cdots,u_n\}$ is an $\mathbb{R}$-basis of $U$, then $\{1\otimes u_1,\cdots,1\otimes u_n\}$ is a $\mathbb{C}$-basis of $\mathbb{C}\otimes_{\mathbb{R}}U$ and usually we write that $\alpha_1 u_1+\cdots+\alpha_nu_n$ with $\alpha_i\in \mathbb{C}$. 

**Observation.** if $U$ is an irreducible $\mathbb{R}$-module, $U_{\mathbb{C}}$ is not always irreducible. For example, $C_3=\left\langle \begin{bmatrix}0 &-1\\1& -1\end{bmatrix}\right\rangle$ is irreducible over $\mathbb{R}$ but reducible over $\mathbb{C}$.


> [!proposition]
> If $U_\mathbb{C}$ is simple, then it is of symmetric type.

