20250210114530

Tags:

Line integrals are integrals with a vector parameterization to it. 

## Defintion
Let $\vec{r}(t)$ be some parameterization that traverses a curve $C$ for $a ≤ t ≤ b$, where $a$ and $b$ provide the bounds for integration.
```ad-formula
#### Line integral Definition
For a function $f(x, y, z)$ and parameterization $\vec{r}(t)$ that are both continuous, then the line integral is calculated as
#### $$\int{C} f(x, y, z)ds = \int_{a}^{b} f(\vec{r}(t))|\vec{r}'(t)|dt $$
$ds$ in the integral represents the arc length differential, or the rate of change of the curve. 
```


#### Example
Evaluate $\int_{e}(x^{2} + y^{2})ds$, where $C$ is the right half of the circle $x^{2} + y^{2} = 9$. Recall that the circle of radius $r$ centered at $(0, 0)$ is $\vec{r}(t) = \langle r\cos(t), r\sin(t) \rangle$ going from $0 ≤ t ≤ 2π$. 