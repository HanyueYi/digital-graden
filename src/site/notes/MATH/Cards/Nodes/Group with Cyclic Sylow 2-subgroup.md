---
{"dg-publish":true,"permalink":"/MATH/Cards/Nodes/Group with Cyclic Sylow 2-subgroup/","dgPassFrontmatter":true}
---


> [!proposition]
> If a group of order $2^nm$ with odd $m$ has cyclic Sylow $2$-subgroup, then $G$ has the unique normal subgroup of order $m$ and so $G$ is solvable.

**_Proof._**
When $n=1$, there exists a $g\in G$ with $|g|=2$. Then $\check g\in\mathrm{Sym}(G)$, which is defined [[MATH/Cards/Nodes/Three Permutations on G Induced from G\|here]], is a product of $2$-cycles. Since $m$ is odd, we have that $\check g$ is a product of $m$'s $2$-cycles and so $\check g$ is an odd permutation. Define $\varphi:\check G\to \mathbb{Z}_2$ such that $\ker\varphi=\check G\cap A_{|G|}$. Then $\ker\varphi\lhd \check G$ is a group of order $m$ and so we get a normal subgroup $H$ of $G$ with order $m$. 

Furthermore, if there is another normal subgroup $K\lhd G$ of order $m$, then the product $KH$ is a subgroup as $K\lhd G$. Note that $|KH|=|K||H|/|K\cap H|>m$ is odd, which is a contradiction. Therefore, it has the unique normal subgroup of order $m$.

Now suppose that it holds for groups of order $2m,2^2m,\cdots,2^{n-1}m$, and suppose that $|G|=2^nm$. With the similar argument, there is a $L\lhd G$ such that $|L|=2^{n-1}m$. As each Sylow $2$-subgroup of $L$ is contained in a Sylow $2$-subgroup of $G$, each Sylow $2$-subgroup of $L$ is also cyclic. Then by induction hypothesis, group $L$ has the unique normal subgroup of order $m$, denoted by $L_0$. Since $L_0$ is a [[MATH/Cards/Nodes/Characteristic Subgroup\|characteristic subgroup]] of $L$, there is $L_0\lhd G$. Additionally, with the same argument in the previous paragraph, we can prove that $L_0$ is unique.

By [Feit-Thompson theorem](https://en.wikipedia.org/wiki/Feit–Thompson_theorem), a group $G$ with cyclic Sylow $2$-subgroup is solvable.
<p align="left">□</p>

