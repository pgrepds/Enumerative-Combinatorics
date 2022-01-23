**Definition:** Let $(a_n)_{n \geq 0}$ be a sequence of integers. The generating function associated to this sequence is
$$
A(q)=\sum_{n \geq 0} a_nq^n.
$$

The generating function $A(q)$ is a formal power series.

We can interpret the above generating function as the number of objects of size $n$ in a given class $\mathcal{A}$ of objects that we want to enumerate. Notice that the variable $q$ is a *formal* letter, meaning it does not stand for any actual value. Loosely speaking, the variable $q$ is used for keeping track of the coefficients of $q^n$.

**Definition:** A *closed-form* is a mathematical expression with a finite number of standard operations. By *standard operations* we refer to the usual operations like addition, multiplication, etc. We usually exclude operations like limes,...

**Exmp.:** Given the formal power series 

$$
A(q)=\sum_{n \geq 0} q^n=1+q^2+q^3+\cdots
$$

What is its closed-form? The solution is rather simple. Multiply both sides of the above equality by $q$ yields to

$$
q \cdot A(q)=q \cdot(\sum_{n \geq 0} q^n=1+q^2+q^3+\cdots)=q+q^2+q^3+q^4+\cdots
$$
Thus,
$$
\begin{aligned}
&A(q)-A(q)\cdot q =(1+q^2+q^3+q^4 + \cdots)-q+q^2+q^3+q^4+\cdots\\
&\iff
A(q)(1-q)=1\\
&\iff 
A(q)=\frac{1}{1-q}
\end{aligned}
$$

Let us use the same trick for finding the closed form of the following formal power series.

Let 
$$A(q)=\sum_{n\geq 0} 2^nq^n=1+2q+4q^2+8q^3+16q^4+\cdots$$

Then,

$$
A(q)\cdot q=q \cdot \sum_{n\geq 0} 2^nq^n=q+2q^2+4q^3+8q^4+16q^5+\cdots\\
$$

By noticing that $A(q)-2q \cdot A(q)=1$, we proceed similarly to the above solution,

$$
\begin{aligned}
A(q)-2 \cdot A(q)\cdot q&=(1+2q+4q^2+8q^3+16q^4+\cdots)-2(q+2q^2+4q^3+8q^4+16q^5+\cdots)\\
A(q)-2 \cdot A(q) \cdot q &= 1\\
A(q) (1 - 2q)&=1\\
A(q) &= \frac{1}{1-2q}
\end{aligned}
$$

Let us consider the formal power series

$$
A(q)=\sum_{n \geq 0} 3^nq^n=1+3q+9q^2+27q^3+\cdots
$$

and calculate its closed form.

We have,
$$
A(q) \cdot q= q \cdot \sum_{n \geq 0} 3^nq^n=q+3q^2+9q^3+27q^4+\cdots
$$

Thus,

$$
\begin{aligned}
A(q)-3 \cdot A(q) \cdot q&=(1+3q+9q^2+27q^3+\cdots)-3(q+3q^2+9q^3+27q^4+\cdots)\\
A(q)-3 \cdot A(q) \cdot q&=1\\
A(q)(1-3q) &=1\\
A(q) &= \frac{1}{1-3q}
\end{aligned}
$$

The above results encourage the following theorem.

**Theorem:** Given the formal power series 

$$
A(q)=\sum_{n \geq 0} k^n q^n
$$

for $k \in \mathbb{Z}^+$. Then $A(q)$ has the closed form
$$
A(q)=\frac{1}{1-kq}
$$

**Proof:** We proceed with induction on $k$ ...

Notice that using the basic algebraic rules for formal power series, we can quickly calculate the closed form for the following formal power series.

Let 

$$
\begin{aligned}
A(q)&=\sum_{n \geq 0} (2^n+3^n)q^n=\sum_{n \geq 0} 2^nq^n + 3^n q^n=\sum_{n \geq 0} 2^nq^n + \sum_{n \geq 0} 3^nq^n\\
&= \frac{1}{1-2q} + \frac{1}{1-3q}\\
&= \frac{2-5q}{(1-3q)(1-2q)}
\end{aligned}
$$