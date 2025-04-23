---
{"dg-publish":true,"aliases":["Milnor lemma","Švarc-Milnor lemma"],"permalink":"/MATH/Cards/Nodes/Švarc-Milnor Lemma/","dgPassFrontmatter":true}
---



> [!definition] properly discontinuous
> The action is properly discontinuous if for every compact subset $K \subset X$ there are only finitely many $g \in G$ such that $g \cdot K \cap K \neq \varnothing$.


> [!definition] cocompact
> An action of a group $G$ on a locally compact space $X$ is called *cocompact* if there exists a compact subset $A \subset X$ such that $X=G \cdot A$. For a properly discontinuous action, cocompactness is equivalent to compactness of the quotient space $G \setminus X$.


> [!definition] word metric
> Let $G$ be a finitely-generated group $G$, and let $A$ be a finite set of generators for $G$. If $\gamma \in G$ is not the identity element, then the *length* of $\gamma$ is defined as the minimal number of elements of $A \cup A^{-1}$, counted with multiplicity, such that $\gamma$ can be written as a product of these elements. The length of the identity element is defined to be zero. 
> 
> The *word metric* $d_A$ on $G$ with respect to $A$ is then defined by the following formula: for all $\gamma$ and $\gamma^{\prime}$ in $G, d_A\left(\gamma, \gamma^{\prime}\right)$ is equal to the length of the product $\gamma^{\prime-1} \gamma$. The action of $G$ by left translations on the metric space $\left(G, d_A\right)$ is an action by isometries. If $A$ and $B$ are two finite generating sets for $G$, then the identity mapping between the metric spaces $\left(G, d_A\right)$ and $\left(G, d_B\right)$ is a *quasi-isometry*.


> [!theorem]
> Let $G$ be a group acting by isometries on a proper length space $X$ such that the action is properly discontinuous and cocompact. Then the group $G$ is finitely generated and for every finite generating set $S$ of $G$ and every point $p \in X$ the orbit map
> 
> $$
> f_p:\left(G, d_S\right) \rightarrow X, \quad g \mapsto g p
> $$
> 
> is a quasi-isometry. Here $d_S$ is the word metric on $G$ corresponding to $S$.


