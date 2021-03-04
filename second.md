<script type="text/x-mathjax-config">
  MathJax.Hub.Config({tex2jax: {inlineMath: [['$','$'], ['\\(','\\)']]}});
</script>
<script type="text/javascript"
  src="http://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>
## Differentiation
**Neighborhood**: an open interval $I=(a,b)$ that contains $x_0$ is called the **neighborhood** of $x_0$    
**Slope**: for a point $x \in I$ and $x \neq x_0$, the slope of the line containing $(x_0, f(x_0))$ and $(x, f(x))$ is
$$\frac{f(x) - f(x_0)}{x-x_0}$$
**Differentiable**: Let $I$ be a neighborhood of $x_0$. $f \colon I \rightarrow \mathbb{R}$ is **differentiable** at $x_0$ if
$$f'(x_0) = \lim_{x \rightarrow x_0}{\frac{f(x) - f(x_0)}{x-x_0}} \quad \text{    exists}$$
If $f \colon I \rightarrow \mathbb{R}$ is differentiable at every pt in $I$, then $f$ is **differentiable** and $f' \rightarrow I \rightarrow \mathbb{R}$ is the **derivative** of $f$    
**Tangent line** to graph of $f$ at $x_0, f(x_0)$ is defined as
$$ y = f(x_0) + f'(x_0)(x - x_0)$$

<details><summary><b>Examples</b></summary>
<p>

$f(x) = x^2$ and $f'(x) = 2x$   
$$\lim_{x \rightarrow x_0}{\frac{f(x) - f(x_0)}{x - x_0}} = \lim{\frac{x^2 - x_0^2}{x - x_0}} = \lim[x + x_0] = 2x_0$$
$f(x) = |x|$
$$\lim_{x \rightarrow 0^+}{\frac{f(x) - f(0)}{x - 0} = 1} \neq \lim_{x \rightarrow 0^-}{\frac{f(x) - f(0)}{x - 0} = -1}$$
Since the limit does not exist at $0$, $f$ is not differentiable at $x = 0$
</p>
</details>

**Proposition 4.4**: For a natural number $n$ and function $f(x) = x^n$, $f \colon \mathbb{R} \rightarrow \mathbb{R}$ is differentiable and
$$f'(x) = nx^{n-1}$$
<details><summary><b>Proof</b></summary>
<p>

Using the difference of powers formula, for $x \neq x_0$
$$\frac{f(x) - f(x_0)}{x - x_0} = \frac{(x-x_0)(x^{n-1} + x^{n-2}x_0 + \ldots + x_0^{n-1})}{x-x_0} = x^{n-1} + x^{n-2}x_0 + \ldots + x_0^{n-1}$$
Observe that the righthand side has $n$ terms that each have a limit of $x_0^{n-1}$. Thus by sum property of limits
$$\lim_{x \rightarrow x_0}{\frac{f(x) - f(x_0)}{x-x_0}} = nx_0^{n-1}$$
</p>
</details>

**Proposition 4.5**: let $I$ be a neighborhood of $x_0$ and suppose $f \colon I \rightarrow \mathbb{R}$ is differentiable at $x_0$. Then $f$ is continuous at $x_0$
<details><summary><b>Proof</b></summary>
<p>

We know that 
$$\lim_{x \rightarrow x_0}{\frac{f(x) - f(x_0)}{x -x_0}} = f'(x_0) \quad \text{ and } \quad \lim_{x \rightarrow x_0}[x - x_0] = 0$$
Thus
$$\lim_{x \rightarrow x_0}[f(x) - f(x_0)] = \lim[\frac{f(x) - f(x_0)}{x-x_0} \cdot (x - x_0)] = f'(x_0) \cdot 0 = 0 \text{ using the product property of limits}$$
Thus $\lim_{x \rightarrow x_0} = f(x_0) \implies f$ is continuous at $x_0$

</p>
</details>

**Theorem 4.6**: Let $I$ be a neighborhood of $x_0$ and suppose that $f \colon I \rightarrow \mathbb{R}$ and $g \colon I \rightarrow \mathbb{R}$ are differentiable at $x_0$. Then
1. $f + g \colon I \rightarrow \mathbb{R}$ is differentiable at $x_0$ and $(f+g)'(x_0) = f('x_0) + g'(x_0)$
<details><summary><b>Proof</b></summary>
<p>

$$\lim_{x \rightarrow x_0}\frac{(f+g)(x) - (f+g)(x_0)}{x - x_0} = \lim{\frac{f(x) - f(x_0)}{x-x_0} + \frac{g(x) - g(x_0)}{x - x_0}} = f'(x_0) + g'(x_0)$$
Using the sum property of limits and definition of derivatives

</p>
</details>

2. $fg \colon I \rightarrow \mathbb{R}$ is differentiable at $x_0$ and $(fg)'(x_0) = f'(x_0)g(x_0) + f(x_0)g'(x_0)$
<details><summary><b>Proof</b></summary>
<p>

$$\lim_{x \rightarrow x_0}\frac{(fg)(x) - (fg)(x_0)}{x - x_0} = \frac{f(x)g(x) - f(x_0)g(x_0)}{x - x_0} = \frac{f(x)g(x) - f(x)g(x_0) + f(x)g(x_0) - f(x_0)g(x_0)}{x - x_0}$$
$$ = \lim_{x \rightarrow x_0}f(x)[\frac{g(x) - g(x_0)}{x - x_0}] + g(x_0)[\frac{f(x) - f(x_0)}{x - x_0}] = f(x)g'(x_0) + f'(x)g(x_0)$$
If $f'(x)$ exists $\implies f$ is continuous at $x$, the above expression exists using the using sum and product properties of limits and the definition of derivatives.

</p>
</details>

3. if $g(x) \neq 0$ for all $x \in I$, $1/g \colon I \rightarrow \mathbb{R}$ is differentiable at $x_0$ and $(\frac{1}{g})'(x_0) = \frac{-g'(x_0)}{(g(x_0))^2}$
<details><summary><b>Proof</b></summary>
<p>

$$ \lim_{x \rightarrow x_0}\frac{(1/g)(x) - (1/g)(x_0)}{x - x_0} = \lim\frac{(1)(g(x)) - (1)(g(x_0))}{x - x_0} = \lim\frac{-1}{g(x)g(x_0)}[\frac{g(x) - g(x_0)}{x - x_0}] = \frac{-g'(x_0)}{(g(x_0))^2}$$

</p>
</details>

4. if $g(x) \neq 0$ for all $x \in I$, $f/g \colon I \rightarrow \mathbb{R}$ is differentiable at $x_0$ and $(\frac{f}{g})'(x_0) = \frac{g(x_0)f'(x_0) - f(x_0)g'(x_0)}{(g(x_0))^2}$
<details><summary><b>Proof</b></summary>
<p>

$$\frac{f(x)}{g(x)} = \frac{1}{g(x)} \cdot f(x)$$
So use the quotient and product properties above to prove differentiability

</p>
</details>

**Theorem 4.11**: Let $I$ be a neighborhood of $x_0$ and let $f \colon I \rightarrow \mathbb{R}$ be strictly monotone and continuous. Suppose $f$ is differentiable at $x_0$ and that $f'(x_0) \neq 0$. Define $J = f(I)$. Then the inverse $f^{-1} \colon J \rightarrow \mathbb{R}$ is differentiable at the point $y_0 = f(x_0)$ and
$$(f^{-1})'(y_0) = \frac{1}{f'(x_0)}$$
<details><summary><b>Proof</b></summary>
<p>

By the IVT, we know that $J$ is a neighborhood of $y_0 = f(x_0)$ so for a point $y \in J, y \neq y_0$ we can define $x = f^{-1}(y)$ such that
$$\frac{f^{-1}(y) - f^{-1}(y_0)}{y - y_0} = 1/\frac{f(x) - f(x_0)}{x - x_0}$$
Since $f^{-1}$ is continuous, we have
$$\lim_{y \rightarrow y_0}{f^{-1}(y)} = f^{-1}(y_0) = x_0$$
Thus by quotient property of limits and the definition of differentiability, we have
$$\lim_{y \rightarrow y_0} \frac{f^{-1}(y) - f^{-1}(y_0)}{y - y_0} = \lim 1/\frac{f(x) - f(x_0)}{x - x_0} = \frac{1}{f'(x_0)}$$

</p>
</details>

**Corollary 4.12**: Let $I$ be an open interval and suppose $f \colon I \rightarrow \mathbb{R}$ is strictly monotone and is differentiable with a nonzero derivative at each point in $I$. Define $J = f(I)$. Then the inverse function $f^{-1} \colon J \rightarrow \mathbb{R}$ is differentiable and for all $x \in J$
$$(f^{-1})'(x) = \frac{1}{f'(f^{-1}(x))}$$      
<details><summary><b>Proof</b></summary>
<p>

Since differentiability $\implies$ continuity, $f \colon I \rightarrow \mathbb{R}$ is continuous and by applying Theorem 4.11  at $x \in J$, where $x = f(f^{-1}(x))$ and $f^{-1}(x)$ plays the role of $x_0$.    

</p>
</details>

**Theorem 4.14 The Chain Rule**: Let $I$ by a neighborhood of $x_0$ and let $f \colon I \rightarrow \mathbb{R}$ be differentiable at $x_0$. Let $J$ be an open interval such that $f(I) \subseteq J$ and let $g \colon J \rightarrow \mathbb{R}$ be differentiable at $f(x_0)$. Then $g \circ f \colon I \rightarrow \mathbb{R}$ is differentiable at $x_0$ and
<details><summary><b>Proof</b></summary>
<p>

$$(g \circ f)'(x_0) = g'(f(x_0))f'(x_0)$$   
Let $y_0 = f(x_0)$ and $y = f(x)$. Then we have
$$\frac{f(x) - f(x_0)}{y - y_0} = 1$$
Using this we have
$$\frac{g \circ f)(x) - (g \circ f)(x_0)}{x - x_0} = \frac{g(y) - g(y_0)}{x - x_0} = \frac{g(y) - g(y_0)}{y - y_0} * \frac{f(x) - f(x_0)}{x - x_0}$$
Provided that $y - y_0 = f(x) - f(x_0) \neq 0$. If there is no open interval containing $x_0$ such that $f(x) - f(x_0)$ we can define an auxiliary function $h \colon J \rightarrow \mathbb{R}$ such that
$$h(y) = \begin{cases}{} [g(y) - g(y_0)]/[y-y_0] & y \in J, y \neq y_0\\ g'(y_0) & y=y_0\end{cases}$$
This gives us
$$\lim_{x \rightarrow x_0} \frac{(g \circ f)(x) - (g \circ f)(x_0)}{x - x_0} = \lim h(f(x))[\frac{f(x) - f(x_0)}{x - x_0}]$$ 
$$= h(f(x_0))f'(x_0) = g'(f(x_0))f'(x_0)$$

</p>
</details>

 **Lemma 4.16**: Let $I$ be a neighborhood of $x_0$ and suppose $f \colon I \rightarrow \mathbb{R}$ is differentiable at $x_0$. If $x_0$ is a maximizer or a minimizer of $f$, then $f'(x_0) = 0$

<details><summary><b>Proof</b></summary>
<p>

Suppose $x_0$ is a maximizer. Then for $x < x_0, x \in I$
$$f'(x_0) = \lim_{x \rightarrow x_0^-}\frac{f(x) - f(x_0)}{x - x_0} \geq 0$$
For $x > x_0, x \in I$, we have
$$f'(x_0) = \lim_{x \rightarrow x_0^+}\frac{f(x) - f(x_0)}{x - x_0} \leq 0$$
Thus $f'(x_0) = 0$

</p>
</details>

**Theorem 4.17 Rolle's Theorem**: Suppor $f \colon [a,b] \rightarrow \mathbb{R}$ is continuous and that $f$ restricted to the open interval $(a,b)$ is differentiable. Also assume that
$$f(a) = f(b)$$
Then there is a point $x_0$ in the open interval $(a, b)$ such that
$$f'(x_0) = 0$$

<details><summary><b>Proof</b></summary>
<p>

By the Extreme Value Theorem, $f$ attains both a maximum and a minimum value on $[a,b]$.    
Case 1: $f(a) = f(b)$ is the maximum or minimum so $f$ is a constant function and $f'(x) = 0$   
Case 2: $f$ has some other maximum or minimum point where the derivative is 0, based on Lemma 4.16.

</p>
</details>

**Theorem 4.18: Mean value Theorem**: Suppose that $f \colon [a, b] \rightarrow \mathbb{R}$ is continuous and that the restriction of $f$ to the open interval $(a,b)$ is differentiable. Then there is a point $x_0$ in $(a,b)$ such that
$$f'(x_0) = \frac{f(b) - f(a)}{b - a}$$
<details><summary><b>Proof</b></summary>
<p>

Let $h \colon [a,b] \rightarrow \mathbb{R}$ be defined by $h(x) = f(x) - mx$ for $x \in [a,b]$. To apply Rolle's Theorem, we need $h(a) = h(b)$, which happens when
$$m = \frac{f(b) - f(a)}{b - a}$$
Thus by this choice of $m$ and Rolle's Theorem, then there is a point $x_0$ in $(a,b)$ such that $h'(x_0) = 0$. Since $h'(x_0)  = f'(x_0) - m$, we have
$$f'(x_0) = m = \frac{f(b) - f(a)}{b - a}$$
as desired.

</p>
</details>

**Proposition 4.20: Identity Criterion**: Let $I$ by an open interval and let $g \colon I \rightarrow \mathbb{R}$ and $h \colon I \rightarrow \mathbb{R}$ by differentiable. These functions differ by a constant if and only if for all $x \in I$
$$g'(x) = h'(x)$$
<details><summary><b>Proof</b></summary>
<p>

Define $f = g - h \colon I \rightarrow \mathbb{R}$. We then have
$$f'(x) = g'(x) - h'(x)$$
Observe that $f$ is constant if and only if $g$ and $h$ differ by a constant. The derivative of any constant is 0. Thus $g'(x) = h'(x)$

</p>
</details>

**Corollary 4.21 Strict Monotonicity Criterion**: Let $I$ be an open interval and $f \colon I \rightarrow \mathbb{R}$ be differentiable. Suppose $f'(x) > 0$ for all $x \in I$. Then $f$ is strictly increasing.
<details><summary><b>Proof</b></summary>
<p>

Let $u, v \in I$ and $u < v$. Using the Mean Value Theorem, we can restrict $f$ to closed bounded interval $[u,v]$ and choose a point $x_0 \in (a,b)$ such that
$$f'(x_0) = \frac{f(v) - f(u)}{v - u}$$
Since $f'(x_0) > 0$ and $v - u > 0$, we have $f(u) < f(v)$. Thus $f$ is strictly increasing.    
Similar proof can be done to prove that $f'(x) < 0$ for all $x \in I \implies$ $f$ is strictly decreasing.

</p>
</details>

**Local Maximizer**: A point $x_0$ in the domain of $f \colon D \rightarrow \mathbb{R}$ is a **local maximizer** if there is some $\delta > 0$ such that for all $x \in D$ such that $|x - x_0| < \delta$, we have
$$f(x) \leq f(x_0)$$    
**Local Minimizer**: if $|x - x_0| < \delta$ implies
$$f(x) \geq f(x_0)$$

By Lemma 4.16, if $I$ is a neighborhood of $x_0$ and $f \colon I \rightarrow \mathbb{R}$ is differentiable at $x_0$, then for $x_0$ to either be a local minimizer or local maximizer, we need
$$f'(x_0) = 0$$
However, $f'(x_0) = 0$ does NOT imply that it is a local minimizer or local maximizer (e.g. $f(x) = x^3$ and $f'(0) = 0$)

**Theorem 4.22**: Let $I$ be an open interval containing $x_0$ and suppose that $f \colon I \rightarrow \mathbb{R}$ has a second derivative. Suppose $f'(x_0) = 0$ then
* If $f''(x_0) > 0$ then $x_0$ is a local minimizer
* If $f''(x_0) < 0$ then $x_0$ is a local maximizer

<details><summary><b>Proof</b></summary>
<p>

Suppose $f''(x_0) > 0$. This implies
$$f''(x_0) = \lim_{x \rightarrow x_0}\frac{f'(x) - f'(x_0)}{x - x_0} > 0$$
There is an open interval such that for $\delta > 0$, $(x_0 - \delta, x_0 + \delta)$ that is contained in $I$, we have
* $f'(x) > 0$ if $x_0 < x < x_0 + \delta$
* $f'(x) < 0$ if $x_0 - \delta < x < x_0$

Using the Mean Value Theorem, we have if $0 < |x - x_0| < \delta$
$$f(x) > f(x_0)$$
Similar proof for $''(x_0) < 0$

</p>
</details>
