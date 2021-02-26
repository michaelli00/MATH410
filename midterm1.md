---
geometry: margin=2cm
---
**Theorem 2.18**: Every convergent sequence is bounded:   
**Proof**: let $\epsilon > 0$ be arbitrary. Then $\exists N$ such that $\forall n \geq N, |a_n - a| < \epsilon$   
Let $M = \max(|a_1|, |a_2|, \ldots, |a_N|, |a_N| + \epsilon)$, then $\forall n \geq 1, M \geq |a_n|$    
**Monotone Convergence Theorem**: a **monotone** sequence **converges** **if and only if** it is **bounded**. It will converge to
* $\sup{\{a_n \mid n \in \mathbb{N}\}}$ if the sequence is monotonically increasing
* $\inf{\{a_n \mid n \in \mathbb{N}\}}$ if the sequence is monotonically decreasing   

**Proof**: Without loss of generality, assume the sequence is monotonically increasing and let $S = \{a_n\}$ that is bounded. By the Completeness Axiom, $S$ has a least upper bound $l = \sup{S}$. Thus $|a_n - l | < \epsilon$ and we have
$$l - \epsilon < a_n < l + \epsilon$$
For the right side, $a_n \leq l < l + \epsilon$ as desired.     
For the left side, $l- \epsilon$ is not an upper bound so $\exists N, l - \epsilon < a_N$ but $\{a_n\}$ is monotonically increasing, thus     
$\forall n \geq N, l - \epsilon < a_n \leq a_n$ as desired.   
  
**Nested Interval Theorem**: let $a_n < b_n$ and $I = [a_n, b_n]$. Assume $I_{n+1} \subseteq I_n$ and $\lim_{n \rightarrow \infty}[b_n - a_n] = 0$. There is a single point $x$ in $I_n$ that $\{a_n\}$ and $\{b_n\}$ converge to.    
**Proof**: We know that $a_n \leq a_{n+1} < b_{n+1} \leq b_n$. Since $\{a_n\}$ is monotonically increasing and is bounded by $b_n$, it must converge to $a$. Similarly, $\{b_n\}$ must converge to $b$.   
Since $\lim_{n \rightarrow \infty}[b_n-a_] = b - a = 0$, $x = b = a$

**Note**: If $\{a_n\} \rightarrow a$, then every subsequence $\{a_{n_k}\} \rightarrow a$    

**Theorem 2.32**: Every sequence has a monotonic subsequence (peek index proof)   
**Theorem 2.33**: Every bounded sequence has a convergent subsequence.    
**Proof**: Every sequence has a monotone subsequence. Since the sequence is bounded, so is the subsequence and by Monotone Convergence Theorem, that subsequence must converge.   
  
**Sequentially Compactness**: A set $S$ is **sequentially compact** if every sequence in $S$ has a subsequence that converges to a point in $S$.    
**Sequential Compactness Theorem**: Any closed interval $[a, b]$ is sequentially compact.   
**Proof**: we need 2 conditions
1. Sequence in $[a, b]$ has a convergent subsequence (using Theorem 2.33)
2. The limit of any sequence in a bounded, closed interval is in that interval. This works for subsequences as well.

**Continuity**: $f \colon D \rightarrow \mathbb{R}$ is **continuous at $x_0 \in D$** if whenever $\{x_n\} \subseteq D \rightarrow x_0$, then $\{f(x)\} \rightarrow f(x_0)$.   
  
**Extreme Value Theorem**: a continuous function on a closed, bounded interval $f \colon [a, b] \rightarrow \mathbb{R}$ has a minimum and a maximum value.      
**Proof**:
1. Show $f \colon [a,b] \rightarrow \mathbb{R}$ is bounded above.   
Proof by contradiction: $\exists x \in [a,b], f(x) > n$. Define a sequence $\{x_n\}$ such that $\forall n \geq 1, f(x_n) > n$   
By the Sequential Compactness Theorem, there is a subsequence $\{x_{n_k}\} \rightarrow x_0 \in [a,b]$. Since $f$ is continuous, $\{f(x_{n_k})\} \rightarrow f(x_0)$.    
Since $\{f(x_{n_k})\}$ converges, it is bounded. Thus contradiction is reached since
$$\forall k, f(x_{n_k}) > n_k \geq k$$
2. $\sup{f(D)}$ is a functional value:   
Let $M = \sup\{f(x) \mid a \leq x \leq b\}$. This means that there is a sequence $\{f(x_n)\} \rightarrow M$    
There is also a subsequence $\{x_{n_k}\} \rightarrow x_0 \in [a,b]$. Since $f$ is continuous we have 
$$\{f(x_{n_k})\} \rightarrow f(x_0) = M$$     
   
**Intermediate Value Theorem**: Let $f \colon [a,b] \rightarrow \mathbb{R}$ is continuous. If there is a $c$ strictly between $f(a)$ and $f(b)$ then there is a point $x_0$ in $(a,b)$ such that $f(x_0) = c$   


**Uniform Continuity**: for arbitrary sequences $\{u_n\}$ and $\{v_n\}$,
$$\lim_{n \rightarrow \infty}{[u_n - v_n]} = 0 \implies \lim_{n \rightarrow \infty}{[f(u_n) - f(v_n)]} = 0$$
**Note**: neither sequence needs to convergent      
  
**Theorem 3.17**: A continuous function on a closed bounded interval $f \colon [a,b] \rightarrow \mathbb{R}$ is uniform continuous    
**Proof**: Proof by contradiction so for an arbitrary $\epsilon > 0$ and arbitrary sequences $\{u_n\}$ and $\{v_n\}$
$$\lim_{n \rightarrow \infty}[f(u_n) - f(v_n)] \geq \epsilon$$
By the Sequential Compactness Theorem, $\{u_{n_k}\} \rightarrow x_0 \in [a,b]$. Since $\lim{u_n} = \lim{v_n}$, we can conclude that $\{v_{n_k}\} \rightarrow x_0$. However, since $f$ is continuous, we have
$$|f(u_{n_k}) - f(v_{v_k})| \leq |f(u_{n_k}) - f(x_0)| + |f(v_{n_k}) - f(x_0)| = 0$$
Thus a contradiction is reached   
  
$\epsilon - \delta$ **criterion at a point**: $f \colon D \rightarrow \mathbb{R}$ satisifies $\epsilon - \delta$ criterion at $x_0 \in D$ if for each $\epsilon > 0, \exists \delta > 0$ such that
$$|x-x_0| < \delta \implies |f(x) - f(x_0)| < \epsilon$$    
Following are equivalent:
* $f \colon D \rightarrow \mathbb{R}$ is uniform continuous if $\lim[u_n - v_n] = 0 \implies \lim[f(u_n) - f(v_n)] = 0$
* $f$ satisfies $\epsilon - \delta$ on domain $D$ if $|u - v| < \delta \implies |f(u) - f(v) < \epsilon$    
  
**Theorem 3.23**: if $f \colon D \rightarrow \mathbb{R}$ is monotone and $f(D)$ is an interval, then $f$ is continuous    
**Corollary 3.25**: Let $f \colon I \rightarrow \mathbb{R}$ be monotone. Then $f$ is continuous iff $f(I)$ is an interval.      
  
$f \colon D \rightarrow \mathbb{R}$ is **1-1** if each point $y \in f(D)$ has exactly one $x \in D$ such that $f(x) = y$    
    
Inverse properties
* $f^{-1}(f(x)) = x$
* f(f^{-1}(y)) = y$
* Inverse of strictly monotone function is strictly monotone


**Theorem 3.29**: if $f \colon I \rightarrow \mathbb{R}$ is strictly monotone then $f^{-1} \colon f(I) \rightarrow \mathbb{R}$ is continuous      
      
**Completeness Axiom**: if a non empty set $S$ of real number is bounded above, then $S$ has a least upper bound        
**Archimedean Property**: for any positive number $c$, there is a natural number $n$ such that $n > c$. Also for any positive $\epsilon$, there is a natural $n$ such that $1/n < \epsilon$   
  
**Difference of Powers Formula**:
$$a^n - b^n = (a-b)(a^{n-1} + a^{n-2}b + \ldots + ab^{n-2} + b^{n-1})$$   
  
**Geometric Sum Formula**:
$$1 + r + r^2 + \ldots + r^n = \frac{1 - r^{n+1}}{1-r}$$    
    
**Binomial Formula**:
$$(a+b)^n = {n \choose 0}a^n + {n \choose 1}a^{n-1}b + \ldots + {n \choose n-1}ab^{n-1} + {n \choose n}b^n$$
