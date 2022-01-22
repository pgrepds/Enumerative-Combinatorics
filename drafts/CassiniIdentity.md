**Theorem:** Denote the Fibonacci sequence by $f_n$. Then
$$
f_{n-1}f_{n+1}-f_n^2=(-1)^n
$$

**Proof:** we proceed by induction on $n$. The base case is trivial. Suppose that the claim holds for $n$. Then,

$$
\begin{aligned}
f_nf_{n+1}-f_{n+1}^2&=f_n(f_n+f_{n+1})-f_{n+1}^2 \\
&=
f_n^2+f_nf_{n+1}-f_{n+1}(f_n+f_{n-1})\\
&=
f_n^2+f_nf_{n+1}-f_{n+1}f_n-f_{n+1}f_{n-1}\\
&=
f_n^2-f_{n+1}f_{n-1} \\
&=
-(f_{n+1}f_{n-1}-f_n^2)\\
&=
-(-1)^n \qquad \qquad \qquad \text{Induction Hypothesis} \\
&=
(-1)^{n+1}
\end{aligned}
$$

This completes the proof.
