---
{"dg-publish":true,"permalink":"/MATH/Cards/Nodes/Affine Quasiprimitive is Primitive/","dgPassFrontmatter":true}
---


> [!proposition]
> Let $G\leqslant\mathrm{AGL}(V)$ be an affine group. If $G$ is quasiprimitive on $V$, then $G$ is primitive.

**_Proof._**
Suppose that $G=V{:}G_0\leqslant V{:}\mathrm{GL}(V)$. For any $v\in V$ and $g\in G_0\leqslant\mathrm{GL}(V)$, define $vg:w\mapsto (v+w)^g$. 

If $G_0$ is irreducible, then $G$ is primitive. Therefore, $G$ imprimitive yields $G_0$ reducible. Then there is a subspace $W\subseteq V$ stabilized by $G_0$. However, $W\lhd G$ is not transitive on $V$ and so $G$ is not quasiprimitive, contradiction.
<p align="right">□</p>

**Another proof comes from [[MATH/Group Theory - 2024spring\|Group Theory - 2024spring]].**

**_Proof._**
Suppose $G$ is imprimitive on $V$. Then by [[MATH/Cards/Nodes/Equivalent Condition of Primitivity\|Equivalent Condition of Primitivity]], $G_0$ is not a maximal subgroup and there is a $M$ satisfying $G_0<M<G$. Let $N:=M\cap V$. Note that $N$ is a normal subgroup of $V$ by $V$ abelian. Also we have $N=M\cap V\lhd M$ by $V\lhd G$. It yields that $N\lhd\left\langle M,V\right\rangle=G$. Then $N\lhd G$ is not transitive on $V$, which contradicts to $G$ quasiprimitive.
<p align="right">□</p>

**Remark.** In fact, the group $G$ is of type HA in the [[MATH/Cards/Nodes/Classification of Quasiprimitive Groups\|Classification of Quasiprimitive Groups]]. 