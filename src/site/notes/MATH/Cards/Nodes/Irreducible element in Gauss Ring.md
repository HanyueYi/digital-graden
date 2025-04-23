---
{"dg-publish":true,"permalink":"/MATH/Cards/Nodes/Irreducible element in Gauss Ring/","dgPassFrontmatter":true}
---


# Units and Prime Norm

Since $\mathbb{Z}[i]$ is a Euclidean domain with norm $N(a+bi)=a^2+b^2$, $\alpha$ is a unit in $\mathbb{Z}[i]$ iff $N(\alpha)=\pm 1$. Therefore, the units in $\mathbb{Z}[i]$ are $\{ \pm 1, \pm i\}$. 

If $\beta=x+yi$ and $x^2+y^2$ is a prime, then $\beta$ is irreducible. Otherwise $\beta=(a+bi)(c+di)$ with non-unit elements $a+bi$, $c+di$, it follows $(a^2+b^2)(c^2+d^2)$ is a prime, which is impossible. 

# Irreducible Integers

If $p$ is a prime in $\mathbb{Z}$ and it is reducible in $\mathbb{Z}[i]$, then $p=(a+bi)(c+di)$ and so $p^2=(a^2+b^2)(c^2+d^2)$. It follows that $a^2+b^2=c^2+d^2=p$ as they are non-units. Therefore, $p$ is a sum of two squares of integers. Conversely, if $p=a^2+b^2$, then $p=(a+bi)(a-bi)$ and so $p$ is reducible. 

Recall that when $p\equiv 1\pmod 4$, $p$ can be written as $p=a^2+b^2$ and $2=1^2+1^2$. Hence, $p\equiv 1\pmod 4$ and $p=2$ are reducible. On the other hand, if $p=a^2+b^2$, then $p\equiv 0,1,\mbox{or }2\pmod 4$. Thus $p\equiv 3\pmod 4$ is irreducible. 

# Irreducible $a+bi$

Assume that irreducible $a+bi$ has norm $p_1\cdots p_k$ where $p_j$ are primes, then $a+bi$ must divide one of $p_j$ because $a+bi$ is irreducible and is prime. Hence $p_j\equiv 1\pmod 4$ and the factorization of $p_j$ is $(m+ni)(m-ni)$, that is, $a+bi=m\pm ni$. 

Up to associates, all the irreducible elements in $\mathbb{Z}[i]$ are as follows:
- The element $1+i$ (of norm 2).
- The primes $p \in \mathbb{Z}$ congruent to 3 modulo 4 (of norm $p^2$ ).
- The distinct irreducible factors $a+b i$ and $a-b i$ (each of norm p) of $p=a^2+b^2$ where $p \in \mathbb{Z}$ is congruent to 1 modulo 4 .


