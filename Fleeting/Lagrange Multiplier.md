20250127105137

Tags:

The Lagrange multiplier is a strategy of finding the local extrema of a function subject to a constraint. 

## Formalism
Assuming that $f(x, y)$ and $g(x, y)$ are differentiable functions. If $f(x, y)$ has a local minimum or local maximum on the constraint curve $g(x, y) = 0$ at $P(a, b)$ and if $\nabla g_{p} ≠ 0$, then there is a scalar $λ$ such that the Lagrange condition $\nabla f_{p} = λ\nabla g_{p}$ written in terms of its components 
$$\begin{cases}
f_{x}(a, b) = λg_{x}(a, b) \\
f_{y}(a, b) = λg_{y}(a, b)
\end{cases}$$
A point $P(a, b)$ that satisfies the Lagrange condition is called a critical point for the constraint and $f(a, b)$, 

#### Example
Find the minimum and maximum values of $f(x, y) = x^{2} + y^{2}$ on the circle $\underbrace{x^{2} + y^{2} = 1}_{\text{Constraint}}$. 
$$\begin{cases}
\nabla f = λ\nabla g \\
g(x, y) = 0
\end{cases} \implies \begin{cases}
f_{x} = λg_{x} \\
f_{y} = λg_{y}
\end{cases}$$
$$2x = λ(2χ) \implies 2x - λ(2x) = 0 \implies 2x(1 - λ) = 0 \implies x = 0\text{ or }λ = 1$$
$$-2y = λ(2y) \implies -2y - λ(2y) = 0 \implies -2y(1 + λ) = 0 \implies y = 0\text{ or }λ = -1$$
$$x^{2} + y^{2} - 1 = 0$$
Then, the critical point must satisfy all 3 equations 
$$x = 0, y = 0: x^{2} + y^{2} = 1 : 0 ^{2} + 0^{2} = 0 ≠ 1$$
$\therefore (0, 0)$ is not a critical point
$$x = 0, λ = -1 : x^{2} + y^{2} = 1 \implies 0^{2} + y^{2} = 1 \implies y^{2} \implies y = ±1$$
$\therefore (0, 1)$ and $(0, -1)$ are critical points
$$λ = 1, y = 0 : x^{2} + y^{2} = 1 \implies x^{2} = 1 \implies x = ±1$$
$\therefore (1, 0)$ and $(-1, 0)$ are critical points
$$λ = 1, λ. = -1$$

Finally, $f$ is to be evaluated at all 4 critical points. At $(0, 1)$, $f(0, 1) = -1$. At $(0, -1)$, $f(0, -1) = -1$. At $(1, 0)$, $f(1, 0) = 1$. At $f(-1, 0)$, $f(-1, 0) = 1$. 

## More than 2 variables
The Lagrange multiplier can be extended to beyond 2 variables. 
#### Example
Find the minimum and maximum values of $f(x, y, z) = xy + 2z$ subject to the constraint $z^{2} = 36 - x^{2} - y^{2}$.
$$\begin{cases}
\nabla f = λ\nabla g \\
g(x, y, z) = 0
\end{cases} \implies \begin{cases}
f_{x} = λg_{x} \\
f_{y} = λg_{y} \\
f_{z} = λg_{z}
\end{cases}$$
$$y = λ(2x)$$
$$x = λ(2y)$$
$$2 = λ(2z) \implies 1 = λ(z)$$
$$x^{2} + y^{2} + z^{2} = 36$$
$$y^{2} = 2λxy$$
$$x^{2} = 2λxy$$
$$x^{2} = y^{2}$$
If $x = y : y = λ(2y) \implies y - 2λy = 0 \implies y(1 - 2λ) = 0 \implies y = 0, λ = \frac{1}{2}$ 
$$x^{2} + y^{2} + z^{2} = 36 \implies z^{2} = 36 \implies z = ±6$$
$\therefore (0, 0, 6)$ and $(0, 0, -6)$ are the critical points.
$$x = y, λ = \frac{1}{2} : 1 = \left( \frac{1}{2} \right)z \implies z = 2$$
$$x^{2} + y^{2} + z^{2} = 36 \implies 2x^{2} + z^{2} = 36 \implies 2x^{2} = 32 \implies x^{2} = 16 \implies x = ±4$$
$\therefore (4, 4, 2)$ and $(-4, -4, 2)$ are critical points. 
If $x = -y : y = 2λx \implies y = -2λy \implies y(1 + 2λ) = 0$, so $y = 0$ and $λ = - \frac{1}{2}$

