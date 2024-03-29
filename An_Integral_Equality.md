### An Integral Equality
Denote the probability measure associated with $F$ by $\mu$ so that $\mu(a, b] = F(b) - F(a)$ for $a < b$. Then the probability measure $\nu$ associated with $F^n$ is given by $\nu(A) = \int_A dF^n(x)$ for $A \in \mathscr{R}^1$.  The goal is to prove for any $g$ is non-negative or integrable with respect to $\nu$ (this is a natural condition imposed on the integrand that you didn't clearly stated) under the assumption $F$ is strictly increasing and continuous, it holds that
```math
\int_\mathbb{R}g(x)\nu(dx) = n\int_\mathbb{R}g(x)F^{n - 1}(x)\mu(dx). \tag{1}
```

By Theorem 16.11 in *Probability and Measure* (3rd edition) by Patrick Billingsley, to show $(1)$, it suffices to show that $\nu$ has density $nF^{n - 1}(x)$ with respect to $\mu$, that is, to show that for any $A \in \mathscr{R}^1$, it holds that 
```math
\nu(A) = \int_AnF^{n - 1}(x)\mu(dx). \tag{2}
```

Because the linear Borel set $\mathscr{R}^1$ is generated by the class $\mathscr{I}$ consisting of intervals $(a, b]$, which is a $\pi$-system, if we can show that $\nu(a, b] = \int_a^bnF^{n - 1}(x)\mu(dx)$ holds for any $a < b$, then $(2)$ holds by Theorem 10.3 in *Probability and Measure*. Since $\nu(a, b] = \int_a^b dF^n(x) = F(b)^n - F(a)^n$, we eventually reduced the original problem to proving 
```math
F(b)^n - F(a)^n = \int_a^b nF^{n - 1}(x)\mu(dx) = \int_a^bnF^{n - 1}(x)dF(x). \tag{3}
```
$(3)$ is almost trivial under the condition that $F$ is continuous and strictly increasing, which allows us to make the variable substitution $u = F(x)$ in the right-hand side of $(3)$, which gives
```math
\int_a^b nF^{n - 1}(x)dF(x) = \int_{F(a)}^{F(b)}nu^{n - 1}du = F(b)^n - F(a)^n.  
```

This completes the proof.  

It should be pointed out this equality does not hold for general distribution function $F$.  For example, when $F$ is the distribution function of $X \sim B(1, 1/2)$. For this $F$ and $n = 2$, 
```math
\nu(\mathbb{R}^1) = 1 \neq 2\int_\mathbb{R}F(x)dF(x) = 2 \times (0.5 \times 0.5 +  1 \times 0.5) = \frac{3}{2}. 
```

```math
\begin{align}
E[X] =& \int_\Omega X dP \\
     =& \int_\mathbb{R} x\mu(dx). 
\end{align}
```
