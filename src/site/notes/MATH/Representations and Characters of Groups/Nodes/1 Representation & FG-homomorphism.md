---
{"dg-publish":true,"permalink":"/MATH/Representations and Characters of Groups/Nodes/1 Representation & FG-homomorphism/","dgPassFrontmatter":true}
---

# Basic Definitions

> [!definition]
> Consider a homomorphism from a group to a general linear group:
> 
> $$\rho:G\to \mathrm{GL}(n,F),$$
> 
> and we call $\rho$ is a *representation* of group $G$.

> [!definition]
> An *$FG$-module* is a vector space $V$ over field $F$, which satisfies the following properties:
> - $vg\in V$
> - associativity: $(vg)h=v(gh)$
> - identity axiom: $v1=v$
> - $(\lambda v)g=\lambda(vg)$
> - $(u+v)g=ug+vg$

**Remark.** For a $FG$-module and a fixed basis, we get a unique group representation. If the basis is changed, we get *similar matrices*. Conversely, from a group representation we can get *conjugate transformations*.

> [!definition]
> We say $\theta$ is a *$FG$-homomorphism*, if $\theta$ is a linear transformation and
> 
> $$\theta:V\to W,\quad (v\theta)g=(vg)\theta.$$
> 
> In the other word, if $\theta$ sends $v$ to $w$, then it sends $vg$ to $wg$. 
{ #d9ofk3}


**Remark.** Note that $FG$-module is a category, where object = vector, morphism = element of group, and they satisfy **associativity** and **identity axiom**. In addition, $FG$-homomorphism can be viewed as a functor between two $FG$-modules.  

> [!definition]
> A *submodule* is a subspace and invariant under any element $g$ of $G$. In the other word, $V\leqslant U$ is a submodule, if $vg\in V$ for all $v\in V$ and $g\in G$. A $FG$-module is *irreducible* if it has no non-trivial $FG$-submodule.
> 
> An $FG$-module $V$ is *faithful* if the identity element of $G$ is the only element $g$ for which $vg=v$ for all $v\in V$.


