---
{"dg-publish":true,"aliases":["generalized polygon","generalized polygons"],"permalink":"/MATH/Cards/Nodes/Generalized Polygons/","dgPassFrontmatter":true}
---

#RESOURCE/cards #TERMS/combinatorics 

# Definitions

> [!definition] [[Talks/Some progress on locally-primitive generalized polygons\|Some progress on locally-primitive generalized polygons]]
> Let $\mathcal{S}=(\mathcal{P},\mathcal{L},\mathbf{I})$ be a finite geometry. The incidence graph $\Gamma$ of $\mathcal{S}$ is the graph with the vertex set $\mathcal{P}\cup\mathcal{L}$ and flags of $S$ as edges.
>
>$\mathcal{S}$ is a *finite generalized $n$-gon* if $\Gamma$ is a connected graph of [diameter](https://en.wikipedia.org/wiki/Distance_(graph_theory)#Related_concepts) $n$ and [girth](https://en.wikipedia.org/wiki/Girth_%28graph_theory%29) $2n$.
>
> A finite generalized $n$-gon $\mathcal{S}$ is called *thick* (*firm*) if every vertex of $\Gamma$ has degree at least $3$ ($2$). 
{ #nvfunb}


There are five equivalent definitions of [[MATH/Cards/Nodes/Generalized Polygons\|generalized polygon]], which is mentioned [here](https://cage.ugent.be/~hvm/artikels/107.pdf). For example, the type (IV) is as follows. 

> [!definition] [from here](https://cage.ugent.be/~hvm/artikels/107.pdf)
> $\mathcal{S}$ is a *finite generalized $n$-gon* if the following two axioms are satisfied:
> - $\mathcal{S}$ contains no ordinary $k$-gon as a sub-geometry, for $2\leqslant k<n$.
> - Any two elements $x,y\in\mathcal{P}\cup\mathcal{L}$ are contained in some ordinary $n$-gon as a sub-geometry in $\mathcal{S}$.

> [!definition]
> An automorphism of $\mathcal{S}$ is a permutation $\theta$ preserving $\mathcal{P}$, $\mathcal{L}$ and incidence relation $\mathrm{I}$. The *full automorphism group* $\mathrm{Aut}(\mathcal{S})$ is the group of all automorphisms of $\mathcal{S}$.

# Restriction of $n$

> [!lemma] Feit-Higman, 1964
> Finite thick generalized $n$-gons exist only for $n\in\{3,4,6,8\}$.

When $n=3$, $\mathcal{S}$ is a projective plane.

When $n=4$, $\mathcal{S}$ is a [[MATH/Cards/Nodes/Generalized Quadrangle\|generalized quadrangle]].

When $n=6$, $\mathcal{S}$ is a [[MATH/Cards/Nodes/Generalized Hexagons\|generalized hexagon]].

When $n=8$, $\mathcal{S}$ is a [[MATH/Cards/Nodes/Generalized Octagons\|generalized octagon]].

# Order $(s,t)$

> [!definition] [[Talks/Some progress on locally-primitive generalized polygons\|Some progress on locally-primitive generalized polygons]]
> Let $\mathcal{S}$ be a finite generalized $n$-gon. Then $\mathcal{S}$ has order $(s,t)$ if $\Gamma$ is bi-regular of degree $(s+1,t+1)$. Remark that $s$ and $t$ are also defined [[MATH/Cards/Nodes/Generalized Quadrangle#^6mhxqi\|here]].
> 

> [!Lemma] V Maldeghem, Generalized Polygons
> Every thick generalized $n$-gon has an order $(s,t)$ with $s,t\geqslant 2$; if $n=3$, then $s=t$, and if $n=8$ then $s\neq t$.

# Examples

## Easy Examples

The following slide comes from [[Talks/Some progress on locally-primitive generalized polygons\|here]]. 

![Pasted image 20240605161810.png](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020240605161810.png)

## Well-known Examples

Furthermore, more well-known examples are displayed as follows: 
- Thick GQs: [[Talks/Some progress on locally-primitive generalized polygons#Examples of Thick GQs\|Some progress on locally-primitive generalized polygons#Examples of Thick GQs]]
- Thick GHs and GOs: [[Talks/Some progress on locally-primitive generalized polygons#Examples of Thick GHs and GOs\|Some progress on locally-primitive generalized polygons#Examples of Thick GHs and GOs]]

# Certain Symmetry

## Integral Conditions

> [!definition]
> $\mathcal{S}$ is *flag-transitive* (*antiflag-transitive*), if it has an automorphism group $G\leqslant\mathrm{Aut}(\mathcal{S})$ such that $G$ acts transitively on all flags (antiflags) of $\mathcal{S}$.
> 
> $\mathcal{S}$ is *point-primitive* (*line-primitive*), if it has an automorphism group $G\leqslant\mathrm{Aut}(\mathcal{S})$ acting primitively on $\mathcal{P}$ ($\mathcal{L}$).

**Remark.** All known GHs and GOs are flag-transitive, point-primitive, and line-primitive; all known classical GQs are flag-transitive, point-primitive, and line primitive. All of them are mentioned [[MATH/Cards/Nodes/Generalized Polygons#Well-known Examples\|here]]. 

There are two open problems:
- Classify all flag-transitive finite [[MATH/Cards/Nodes/Generalized Polygons\|generalized polygons]]? With conjecture:
	- $n=4$, Kantor 1991, classical or finite exceptions.
	- $n=6,8$, are the known examples.
- Classify all point-primitive (line-primitive) finite [[MATH/Cards/Nodes/Generalized Polygons\|generalized polygons]]?

## Local Conditions

> [!definition]
> Let $\mathcal{S}=(\mathcal{P},\mathcal{L},\mathrm{I})$ be a generalized $n$-gon and $G\leqslant\mathrm{Aut}(\mathcal{S})$. $\mathcal{S}$ is called $G$-locally $\mathrm{P}$, if for each vertex $u$ in $\Gamma$, the stabilizer $G_u$ has the property $\mathrm P$ in $\Gamma(u)$, where $\Gamma(u)$ is the neighbor of $u$ in $\Gamma$.

**Remark.** [[Talks/Some progress on locally-primitive generalized polygons\|dwd]] gives some relations between local and integral conditions, see [[Pasted image 20240605163848.png|here]]. 

# Parameter Conditions

See [[Talks/Some progress on locally-primitive generalized polygons#Parameter conditions\|here]].

# Some Useful Tools

See [[Talks/Some progress on locally-primitive generalized polygons#Main tools\|here]]:
- Benson type argument
- Fixed element structure
- Normal quotient graphs

