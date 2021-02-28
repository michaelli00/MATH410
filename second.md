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
$$ = \lim_{x \rightarrow x_0}f(x)[\frac{g(x) - g(x_0)}{x - x_0}] + g(x_0)[\frac{f(x) - f(x_0)}{x - x_0}] = f(x)g'(x) + f'(x)g(x)$$
Using sum and product properties of limits and the definition of derivatives

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
