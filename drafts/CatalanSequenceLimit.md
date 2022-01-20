Let $C_n$ be the Catalan sequence. Calculate the limit 
$$
\lim_{n \to \infty} \frac{C_{n+1}}{C_n}
$$

The $n$-th Catalan number can be calculated using the following formula.
$$
C_n=\frac{1}{n+1} {2n \choose n}
$$

It follows the $(n+1)$-th Catalan number.
$$
C_{n+1}=\frac{1}{n+2} {2(n+1) \choose n+1}
$$

Thus,
$$
\begin{aligned}
C_n&=\frac{(2n)!}{n! (n+1)!}\\\\
C_{n+1}&= \frac{(2n+1)!}{(n+1)!(n+2)!}
\end{aligned}
$$
Therefore,

$$
\begin{aligned}
\frac{C_{n+1}}{C_n}&=\frac{\frac{1}{n+2}{2(n+1) \choose n+1}}{\frac{1}{n+1}{2n \choose n}}
=
\frac{\frac{(2n+2)!}{(n+1)!(n+2)!}}{\frac{(2n)!}{n!(n+1)!}}
\\
\\
&=
\frac{(2n+1)!}{(n+1)!(n+2)!}\frac{n!(n+1)!}{(2n)!}
=
\frac{(2n+2)!n!}{(n+2)!(2n)!}
\\
\\
&=
\frac{(2n+2)!n!}{(n+1)(n+2)n!(2n)!}
=
\frac{(2n+2)!}{(n+1)(n+2)(2n)!}
\\
\\
&=
\frac{(2(n+1))!}{(n+1)(n+2)(2n)!}
=
\frac{(2n+2)(2n+1)(2n)!}{(n+1)(n+2)(2n)!}
\\
\\
&=
\frac{(2n+2)(2n+1)}{(n+1)(n+2)}
=
\frac{2(n+1)(2n+1)}{(n+1)(n+2)}
\\
\\
&=
\frac{2(2n+1)}{n+2}=\frac{4n+2}{n+2}
\\
\\
&=
\frac{4(n+2)-6}{n+2}=4-\frac{6}{n+2}
\end{aligned}
$$

And therefore,
$$
\lim_{n \to \infty} \frac{C_{n+1}}{C_n}=\lim_{n \to \infty} \biggl( 4-\frac{6}{n+2} \biggr)=4
$$