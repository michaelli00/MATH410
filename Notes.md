# MATH410
## Chapter 2 Convergent Sequences
**Sequence:** $f \colon \mathbb{N} \rightarrow \mathbb{R}$, denoted $\{a_n\}$. It **converges** to $a$ if for every $\epsilon > 0$, there is an index $N$  
such that $\forall n \geq N, |a_n - a| < \epsilon$.   

**Example**: $\frac{2}{n^2} + \frac{4}{n} + 3$ converges to $3$. For an arbitrary $\epsilon > 0$ and for all indexes $n \geq N$, we need to show
$$|\frac{2}{n^2} + \frac{4}{n} + 3 - 3| < \epsilon$$
Through algebra we have
$$|\frac{2}{n^2} + \frac{4}{n} + 3 - 3| \leq \frac{6}{n} \leq \frac{6}{N} < 6 * \frac{\epsilon}{6} = \epsilon$$
Using Archimedean Property    
**Comparison Lemma**: let $\{a_n\} \rightarrow a$. Then $\{b_n\} \rightarrow b$ if there is a $c \geq 0$ and $N_1$ such that for $n \geq N_1$:
$$|b_n - b| \leq c|a_n - a|$$
**Sum Property**:     
**Boundness**: $\{a_n\}$ is **bounded** if $\forall n, M \geq |a_n|$    
**Theorem 2.18**: Every convergent sequence is bounded:   
**Theorem 2.22**: if $\{c_n\}$ is in $[a, b]$ and converges to $c$, then $c \in [a,b]$. This gives the definition:    
$S \subseteq R$ is **closed** if $\{a_n\} \subseteq S$ and converges to $a \in S$   

**Monotone Convergence Theorem**: a **monotone** sequence **converges** **if and only if** it is **bounded**. It will converge to
* $\sup{\{a_n \mid n \in \mathbb{N}\}}$ if the sequence is monotonically increasing
* $\inf{\{a_n \mid n \in \mathbb{N}\}}$ if the sequence is monotonically decreasing   

**Proof**: Without loss of generality, assume the sequence is monotonically increasing and let $S = \{a_n\}$ that is bounded. By the Completeness Axiom, $S$ has a least upper bound $l = \sup{S}$. Thus $|a_n - l | < \epsilon$ and we have
$$l - \epsilon < a_n < l + \epsilon$$
For the right side, $a_n \leq l < l + \epsilon$ as desired.     
For the left side, $l- \epsilon$ is not an upper bound so $\exists N, l - \epsilon < a_N$ but $\{a_n\}$ is monotonically increasing, thus     
$\forall n \geq N, l - \epsilon < a_n \leq a_n$ as desired.   
**Example**: $s_n = \sum_{k = 1}^{n}\frac{1}{k} * \frac{1}{2^k}$    
Clearly $s_n$ is monotonically increasing. Using geometric sum, we have
$$s_n \leq \frac{1/2 - (1/2)^{n+1}}{1 - 1/2} \leq \frac{1/2}{1/2} = 1$$
Thus $s_n$ is bounded and by Monotone Convergence Theorem, the sequence converges.    
**Example**: Show $\lim_{n \rightarrow \infty}{c^n} = 0$    
If $c = 0$, trivial   
If $c \neq 0$, $|c^n| = |(-c)^n|$ so we can use positive $c$ without loss of generality.  
Let $0 < c < 1$. $c^n$ is decreasing and is bounded below by $0$ thus by Monotone Convergence Theorem, the sequence converges to $l = \inf{c^n}$    
$l$ must be $0$ otherwise we have $c^n = \frac{c^{n+1}}{c} \geq \frac{l}{c}$.     
$\frac{l}{c}$ must be a lower bound but since $0 < c < 1$, $\frac{l}{c} > l$ thus is not a lower bound    

**Nested Interval Theorem**: let $a_n < b_n$ and $I = [a_n, b_n]$. Assume $I_{n+1} \subseteq I_n$ and $\lim_{n \rightarrow \infty}[b_n - a_n] = 0$. There is a single point $x$ in $I_n$ that $\{a_n\}$ and $\{b_n\}$ converge to.    
**Proof**: We know that $a_n \leq a_{n+1} < b_{n+1} \leq b_n$. Since $\{a_n\}$ is monotonically increasing and is bounded by $b_n$, it must converge to $a$. Similarly, $\{b_n\}$ must converge to $b$.   
Since $\lim_{n \rightarrow \infty}[b_n-a_] = b - a = 0$, $x = b = a$

If $\{a_n\} \rightarrow a$, then every subsequence $\{a_{n_k}\} \rightarrow a$    
**Theorem 2.32**: Every sequence has a monotonic subsequence    
**Proof**: One of 2 cases can occur using **peak indices**: index $m$ such that for $n \geq m, a_n \leq a_m$
1. There are a finite number of peak indices. Start the subsequence after the last peak and this is a strictly increasing subsequence
2. There are an infinite number of peak indices so the sequence is monotonically decreasing and so is the subsequence

**Theorem 2.33**: Every bounded sequence has a convergent subsequence.    
**Proof**: Every sequence has a monotone subsequence. Since the sequence is bounded, so is the subsequence and by Monotone Convergence Theorem, that subsequence must converge.   
**Sequentially Compactness**: A set $S$ is **sequentially compact** if for every sequence in $S$ has a subsequence that converges to a point in $S$.    

**Sequential Compactness Theorem**: Any closed interval $[a, b]$ is sequentially compact.   
**Proof**: we need 2 conditions
1. Sequence in $[a, b]$ has a convergent subsequence (using Theorem 2.33)
2. The limit of any sequence in a bounded, closed interval is in that interval. This works for subsequences as well.

**Continuity**: $f \colon D \rightarrow \mathbb{R}$ is **continuous at $x_0 \in D$** if whenever $\{x_n\} \subseteq D \rightarrow x_0$, then $\{f(x)\} \rightarrow f(x_0)$. $f \colon D \rightarrow \mathbb{R}$ is **continuous** if it is continuous at every point in $D$.    
**Example**: $f(x) = x^2 - 2x + 4$ is continuous $\mathbb{R} \rightarrow \mathbb{R}$.   
Let $x_0$ be arbitrary and $\{x_n\} \rightarrow x_0$ Then
$$\lim_{n \rightarrow \infty}{f(x_n)} = \lim_{n \rightarrow \infty}{[x^2_n - 2_n + 4]} = x^2_0 - 2x_0 + 4 = f(x_0)$$    
**Example**: $f(x) = \begin{cases} 1 & x\geq 0 \\ 2 & x < 0 \end{cases}$    
Consider $\{-1/n\} \rightarrow 0$. $\lim_{n \rightarrow \infty}{f(-1/n)} = 2 \neq 1 = f(0)$. Thus $f$ is not continuous at $x = 0$.     
**Example**: $f(x) = \begin{cases} 1 & x\in \mathbb{Q} \\ 0 & x \in \mathbb{I} \end{cases}$   
No point in $f$ is continuous. Let $\{u_n\} \subseteq \mathbb{Q}$ converge to $x_0$ and $\{v_n\} \subseteq \mathbb{I}$ converge to $x_0$. Then    
$\lim_{n \rightarrow \infty}{f(u_n)} = 1 \neq 0 = $\lim_{n \rightarrow \infty}{f(v_n)}$. Thus $f$ is not continuos.     
    
$f(D)$ attains a **maximum value** at $x_0$ if $\forall x \in D, f(x) \leq f(x_0)$. $x_0$ in this case is called the **maximizer**.   
$f(D)$ attains a **minimum value** at $x_0$ if $\forall x \in D, f(x) \geq f(x_0)$. $x_0$ in this case is called the **minimizer**.   
**Extreme Value Theorem**: a continuous function on a closed, bounded interval $f \colon [a, b] \rightarrow \mathbb{R}$ has a minimum and a maximum value.    
**Proof**: 
1. Show that $f(D)$ is bounded above so $f(x) \leq M$ for all $x \in [a, b]$.     
**Proof by contradiction**: $f(x_n) > n$ for some $x_n \in [a,b]$ and $n \in \mathbb{N}$ which means that $\{x_n\}$ has $f(x_n) > n$ for all $n$.    
However, by the Sequential Compactness Theorem, there is a subsequence $\{n_{n_k}\} \rightarrow x_0 \in [a,b]$. Furthermore, since $f$ is continuous at $x_0$, $\{f(x_{n_k})\}$ must converge to $f(x_0)$   
Since a convergent sequence is bounded, $f(\{x_{n_k})\}$ is bounded and a contradiction is reached since we said that 
$$ \forall k, f(x_{n_k}) > n_k \geq k$$

**Intermediate Value Theorem**: Let $f \colon [a,b] \rightarrow \mathbb{R}$ is continuous. If there is a $c$ strictly between $f(a)$ and $f(b)$ then there is a point $x_0$ in $(a,b)$ such that $f(x_0) = c$   
**Example**: There is a $c > 0$ and $x> 0$ such that $x^2 = c$    
Let $f \colon [0, c+1]$ and $f(x) = x^2$. Then we have $f(0) = 0 < c$ and $f(c+1) = c^2 + 2c + 1 > c$. Thus by IVT, there is an $x \in (0, c+1)$ such that $f(x) = c$     
  
  **Uniform Continuity**: for arbitrary sequences $\{u_n\}$ and $\{v_n\}$, if 
  $$\lim_{n \rightarrow \infty}{[u_n - v_n]} = 0$$
  then
  $$\lim_{n \rightarrow \infty}{[f(u_n) - f(v_n)]} = 0$$
  **Note**: neither sequence needs to convergent    
**Example** continuity does not imply uniform continuity    
$f(x) = x^2$ and let $\{u_n\} = n$ and $\{v_n\} = n - 1/n$    
$$\lim_{n \rightarrow \infty}{[u_n - v_n]} = \lim_{n \rightarrow \infty}{[1/n]} = 0$$   
**Theorem 3.17**: A continuous function on a closed bounded interval $f \colon [a,b] \rightarrow \mathbb{R}$ is uniform continuous    
**Proof**: Proof by contradiction so for an arbitrary $\epsilon > 0$ and arbitrary sequences $\{u_n\}$ and $\{v_n\}$
$$\lim_{n \rightarrow \infty}[f(u_n) - f(v_n)] \geq \epsilon$$
By the Sequential Compactness Theorem, $\{u_{n_k}\} \rightarrow x_0 \in [a,b]$. Since $\lim{u_n} = \lim{v_n}$, we can conclude that $\{v_{n_k}\} \rightarrow x_0$   
However, since $f$ is continuous,     
    
$\epsilon - \delta$ **criterion at a point**: $f \colon D \rightarrow \mathbb{R}$ satisifies $\epsilon - \delta$ criterion at $x_0 \in D$ if for each $\epsilon > 0, \exists \delta > 0$ such that
$$|x-x_0| < \delta \implies |f(x) - f(x_0)| < \epsilon$$    
**Example**: $f(x) = \begin{cases} -x & x\leq 0 \\ x-1 & x > 0 \end{cases}$    
Doesn't satisfy $\epsilon - \delta$ at $x_0 = 0$. Let $\epsilon = 1/2$ the there is no $\delta$ such that
$$-\delta < x < \delta \implies -1/2 < |f(x) - 0| < 1/2$$
Since any positive $x \in (-\delta, \delta)$ has $f(x) < -1/2$    
Following are equivalent
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
