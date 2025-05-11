---
{"dg-publish":true,"aliases":["radical","socle"],"draft":true,"permalink":"/Representation Theory 101/Nodes/Radical and Socle of Modules/","dgPassFrontmatter":true}
---


> [!definition]
> Suppose that $U$ is a $kG$-module. Then:
> - the radical $\mathrm{rad}U$ is the minimal submodule such that $U/\mathrm{rad}U$ is semisimple;
> - the socle $\mathrm{soc}U$ is the direct sum of all minimal submodules, that is, the maximal submodule which is semisimple.

> [!proposition] [[Alperin_1993_Local representation theory.pdf#page=50|Alperin_1993_Local representation theory, page 50]]
> If $U$ is any $kG$-module, then $\mathrm{soc}(U^*)\cong (U/\mathrm{rad}U)^*$.

> [!proposition]
> Let $U$ be a $kG$-module. Then $U/\mathrm{rad}U$ is irreducible iff $\mathrm{rad}U$ is the unique maximal $kG$-submodule.

**_Proof._**
One direction is easy. If $\mathrm{rad}U$ is maximal, then $U/\mathrm{rad}U$ is irreducible. Conversely, suppose that $U/\mathrm{rad}U$ is irreducible. It follows that $\mathrm{rad}U$ is a maximal $kG$-submodule. If there is another maximal $kG$-submodule $W\subseteq U$, then $U/W$ is irreducible and so is semisimple. Then $W\supseteq \mathrm{rad}U$ and so $W=U$ or $\mathrm{rad}U$, contradiction.
<p align="left">□</p>

**Remark.**
- Is there some connection with [[MATH/Lie Group and Lie Algebra/Nodes/3 The Killing form - describe solvable and semi-simple\|3 The Killing form - describe solvable and semi-simple]]?
	- [Semisimple module](https://en.wikipedia.org/wiki/Semisimple_module)
	- [Semisimple algebra](https://en.wikipedia.org/wiki/Semisimple_algebra)
- The definition of radical above is different to [wiki](https://en.wikipedia.org/wiki/Radical_of_a_module).

