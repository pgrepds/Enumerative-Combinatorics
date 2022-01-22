We proof a needed Lemma first.

**Lemma 1:** Let $m,n,r \in \mathbb{Z}^+$ and $r \leq \min{(m,n)}$. Then 
$$
{{m+n} \choose r} = \sum_{k=0}^r {m \choose {r-k}} {n \choose k}
$$

**Proof:** Let $A$ and $B$ be sets. Suppose $A \cap B =\emptyset$ and let $|A|=n$ and $|B|=m$, then clearly $|A \cup B|=|A|+|B|=m+n$. The number of ways to choose $r$ elements from $A \cup B$ is equal to ${m+n} \choose r$.

Suppose that we choose $r \leq k$ elements from $A$, then we get $n \choose k$ possible choices. If we pick the remaining elements from $B$, then we get $m \choose {r-k}$ possible choices.

The number $k$ is choosen from the set $\{1, 2, \cdots, r\}$, thus the total number of possible choices is given by

$$
\sum_{k=0}^r {m \choose {r-k}} {n \choose k}
$$

This completes the proof.

The following two corallaries follow directly from the above Lemma.

**Corollary 1:** 

$$
\sum_{k=0}^r {m \choose {r-k}} {n \choose k}=\sum_{k=0}^r {m \choose {m-r+k}} {n \choose k}
$$

**Proof:** By the symmetry property of the binomial coefficient (compare with lecture $1$) 

$$
{n \choose k}={n \choose {n-k}}
$$

the above equality follows directly.

**Corollary 2:** If $m=n$ and $r=n+1$, then 

$$
\sum_{k=1}^n {n \choose {k-1}} {n \choose k}={2n \choose {n+1}}
$$

**Proof:** Replacing $m$ with $n$ and $r$ with $n+1$ in the formula given in Corollary $1$, the claim follows.

Notice, that we have proven in Lecture $1$, that for $1 \leq k \leq n$, we have ${{n-1} \choose {k-1}} + {{n-1} \choose k}= {n \choose k}$ or equivalently ${n \choose {k-1}} + {n \choose k}={{n+1} \choose k}$.

**Theorem:** 
$$
\sum_{k=0}^n {n \choose k}^2 = {2n \choose n}
$$

**Proof:** We proceed with induction on $n$. The base case is trivial. Assume that the claim holds for $n$. Then,

$$
\begin{aligned}
\sum_{k=0}^{n+1} {n+1 \choose k}^2 &= {{n+1} \choose 0}^2 + \sum_{k=1}^{n+1} {{n+1} \choose k}^2\\
&=
1 + \sum_{k=1}^n {n+1 \choose k}^2 + {n +1 \choose n+1}^2 \\
&=
1 + \sum_{k=1}^n \biggl [ {n \choose k-1} + {n \choose k} \biggr]^2 + 1 \\
&=
2 + \sum_{k=1}^n \biggl [ {n \choose k-1}^2 + 2{n \choose k-1}{n \choose k} + {n \choose k}^2 \biggr] \\
&=
2 + \sum_{k=1}^n \biggl [ {n \choose k-1}^2 + {n \choose k}^2 \biggr] + 2 \sum_{k+1}^n {n \choose {k-1}}{n \choose k}\\
&=
1 + \sum_{k=1}^n {n \choose k}^2 + 1 + \sum_{k=1}^n {n \choose k}^2 + 2\sum_{k=1}^n {n \choose k-1} {n \choose k} \\
&=
{n \choose 0} + \sum_{k=1}^n {n \choose k}^2 + {n \choose 0} + \sum_{k=1}^n {n \choose k}^2 + 2\sum_{k=1}^n {n \choose k-1} {n \choose k} \\
&=
{2n \choose n} + {2n \choose n} + 2\sum_{k=1}^n {n \choose k-1} {n \choose k} \\
&=
2 {2n \choose n} + 2\sum_{k=1}^n {n \choose k-1} {n \choose k}  \\
&=
2 {2n \choose n} + 2 {2n \choose n+1} \qquad \qquad \qquad \qquad \text{(Corollary 2)}\\
&=
2 \biggl ( {2n \choose n} + {2n \choose n+1} \biggr) \\
&=
2 {2n +1 \choose n+1} \\
&=
{2(n + 1) \choose n +1}
\end{aligned}
$$

This completes the proof.