---
{"dg-publish":true,"permalink":"/MATH/Classical Groups/Nodes/2 Symplectic Space and Symplectic Group/","dgPassFrontmatter":true}
---


# Symplectic Space

Let $(V,B)$ be a [[MATH/Classical Groups/Nodes/1 Sesquilinear Form#^6hwkgu\|symplectic space]] of dimension $n$ over field $F$. Suppose $e_1,\cdots,e_n$ is a set of basis, then $M'=-M$. We call $M$ an *alternate matrix*.

For any $u,v\in V$, $B(x,y)=-B(y,x)$. Thus $0=B(x+y,x+y)=B(x,y)+B(y,x)$. If $\mathrm{char}F\neq 2$, $B$ is anti-symmetric. Otherwise, $\mathrm{char}F=2$ yields $B$ is symmetric.

In this section, we want to find "standard form" of an alternate matrix.

If $B\neq 0$, there is $u,v\in V$ such that $B(u,v)\neq 0$. Let $u_1=u$ and $v_1=B(u,v)^{-1}v$. Then $B(u_1,v_1)=1$, and we call $(u_1,v_1)$ a *hyperbolic pair* and $\big<u_1,v_1\big>$ a *hyperbolic plane*. Repeat the procedure, $V$ can be written as

$$V=H_1\bot H_2\bot \cdots\bot H_r\bot V^\bot,$$

where $H_i=\big<u_i,v_i\big>$ is hyperbolic plane. Suppose $w_1,\cdots,w_{n-2r}$ is a set of basis of $V^\bot$, then under the basis $u_1,v_1,\cdots,u_r,v_r,w_1,\cdots,w_{n-2r}$ the corresponding matrix of $B$ is

$$M= \left[ \begin{matrix} S &  & & \\  & \ddots & & \\  &  & S & \\ & & & 0_{n-2r} \end{matrix} \right] $$

where $S =\begin{pmatrix} 0&1\\-1&0 \end{pmatrix}$. Matrix $M$ is the standard form of an alternate matrix, and $\det M=1$.

# Symplectic Group

> [!definition]
> Suppose $(V,B)$ a non-degenerated symplectic space of dimension $2m$. Define *symplectic group* as 
> 
> $$\mathrm{Sp}_{2m}(V)=\{\tau:\tau \;\rm is\;a\;isometery\}.$$

We only list some properties here and omit proofs.

> [!proposition]
> - $|\mathrm{Sp}_{2m}(q)|=q^{m^2}\prod_{i=1}^m(q^{2i}-1)$.
> - $\mathrm{Sp}_2(V)=\mathrm{SL}_2(V)$
> - $\mathrm{GL}_m(F)\hookrightarrow \mathrm{Sp}_{2m}(F)$

The only scalars in $\mathrm{Sp}_{2m}(q)$ is $\pm 1$. The group $\mathrm{PSp}_{2m}(q)$ is defined to be the quotient of $\mathrm{Sp}_{2m}(q)$ by the subgroup (of order $1$ or $2$) of scalar matrices. The most important theorem in this section is about the simplicity of $\mathrm{PSp}(V)$.

> [!theorem]
> Let $V$ be a non-degenerated symplectic space of dimension $n$. Then $\mathrm{PSp}(V)$ is simple except for $(n,|F|)=(2,2),(2,3),(4,2)$. 

