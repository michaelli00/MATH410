# MATH410
### Sequence Definition of Continuity
If $\{u_n\}$ converges to $x_0$ then $\{f(u_n)\}$ converges to $f(x_0)$
### $\epsilon - \delta$ Definition of Continuity
$f$ is continuous at $x_0$ if for each $\epsilon > 0$, $\exists \delta > 0$ such that
$$|x- x_0| < \delta \implies |f(x) - f(x_0)| < \epsilon$$
**Example**: Let $f(x) = x^2$ and prove that $f(x)$ is continuous at $x = 3$. Let $\epsilon$ be arbitrary.  
$$|f(x) - f(3)| = |x^2 - 3^2| < \epsilon \implies |x-3||x+3| < \epsilon$$
Setting $\delta = \min{(1, \epsilon/7)}$ then
$$|x-3| < \delta \implies x < 4 \implies x + 3 < 7 \implies |x-3||x+3| < \frac{\epsilon}{7}*7 = \epsilon$$
