20250113111937

Tags:

For a differentiable function $f(x, y)$ where $x = x(t)$ and $y = y(t)$ are both differentiable functions of $t$, then $f$ is a differentiable function of t and $$\frac{df}{dt} =  \frac{δf}{δx} \frac{dx}{dt} + \frac{δf}{δy} \frac{dy}{dt}$$
If we let $\vec{r}(t) = \langle x(t), y(t) \rangle$ and $f(x, y) = f(\vec{r}(t))$, then $$\frac{df}{dt} = \frac{d}{dt}f(\vec{r}(t)) = \langle \frac{δf}{δx}, \frac{δf}{δy} \rangle \cdot \langle x'(t), y'(t) \rangle = \nabla f(\vec{r}(t)) \cdot \vec{r}'(t)$$
## Equation
Using the fact that $\vec{r}(t)$ can be described a s vector-valued function or path describing the movement of a particle, then the chain rule for paths has the equation
```ad-formula
#### Equation of Chain Rule for Paths
#### $$\frac{d}{dt}f(\vec{r}(t)) = \nabla f(\vec{r}(t)) \cdot \vec{r}'(t)$$
```

```ad-example
#### Suppose $f(x, y, z) = x^{2} + 4yz^{3}$ and $\vec{r}(t) = \langle sin(t), cos(t), 1 + 6t \rangle$, find $\frac{d}{dt}f(\vec{r}(t))$
$$\frac{d}{dt}f(\vec{r}(t)) = \nabla f(\vec{r}(t)) \cdot \vec{r}'(t)$$
$$\nabla f = \langle 2x, 4z^{3}, 12yz^{2} \rangle$$
$$\nabla f(\vec{r}(t)) = \langle 2sin(t), 4(1 + 6t)^{3}, 12cos(t)(1 + 6t)^{2} \rangle$$
$$\vec{r}'(t) = \langle cos(t), -sin(t), 6 \rangle$$
$$\frac{d}{dt}f(\vec{r}(t)) = \langle 2sin(t), 4(1 + 6t)^{3}, 12cos(t)(1 + 6t)^{2} \rangle \cdot \langle cos(t), -sin(t), 6 \rangle$$
$$\underbrace{2sin(t)cos(t) - 4sin(t)(1 + 6t)^{3} + 72cos(t)(1 + 6t)^{2}}_{\text{function of t only!}}$$
```

## General Composite Functions
For a differentiable function $f(x, y)$ of $x$ and $y$ where $x = x(s, t)$ and $y = y(s, t)$, then the following applies
```ad-formula
#### Differentiable Functions
#### $$\frac{δf}{δs} = \frac{δf}{δx}\frac{δx}{δs} + \frac{δf}{δy}\frac{δy}{δs}$$
and
#### $$\frac{δf}{δt} = \frac{δf}{δx}\frac{δx}{δt} + \frac{δf}{δy}\frac{δy}{δt}$$
```

If we let $\vec{R}(s, t) = \langle x(s, t) + y(s,t ) \rangle$, then the dot product can be used.
```ad-formula
#### $$\frac{δf}{δs} = \nabla f(\vec{R}(s, t)) \cdot \left\langle \frac{δx}{δs}, \frac{δy}{δs} \right\rangle$$
and
#### $$\frac{δf}{δt} = \nabla f(\vec{R}(s, t)) \cdot \left\langle \frac{δx}{δt}, \frac{δy}{δt} \right\rangle$$
```

## General Version
Let $f(x_{1}, \dots, x_{n})$ be a differentiable function of $n$ variables. If each of those variables are a differentiable function of $m$ variables $t_{1}, \dots, t_{m}$, then for $K = 1, \dots, m$, the below applies.
$$\frac{δf}{δt_{k}} = \frac{δf}{δx_{1}}\frac{δx_{1}}{δt_{k}} + \dots + \frac{δf}{δx_{n}} \frac{δx_{n}}{δt_{k}}$$
```ad-example
#### Given $f(x, y) = e^{x}sin(y)$ where $x(s, t) = st^{2}$ and $y(s, t) = s^{2}t$, find $\frac{δf}{δs}$ and $\frac{δf}{δt}$
$$\frac{δf}{δs} = \frac{δf}{δx} \times \frac{δx}{δs} + \frac{δf}{δy} \times \frac{δy}{δs} = (e^{x}sin(y))(t^{2}) + (e^{x}cos(y))(2st) =$$
$$e^{st^{2}}sin(s^{2}t)(t^{2}) + e^{st^{2}}cos(s^{2}t)(2st)$$
$$\frac{δf}{δt} = \frac{δf}{δx} \times \frac{δx}{δt} + \frac{δf}{δy} \times \frac{δy}{δt} = e^{st^{2}}sin(s^{2}t)(2st) + e^{st^{2}}cos(s^{2}t)(s^{2})$$
```

```ad-example
#### Given $f(x, y, z) = xy + yz + xz$ where $x(s, t) = st, y(s, t) = e^{st}$ and $z(s, t) = t^{2}$. Find $\frac{δf}{δs}$ at $(s, t) = (0, 1)$
$$f_{s} = \frac{δf}{δs} = \frac{δf}{δx} \times \frac{δx}{δs} + \frac{δf}{δy} \times \frac{δy}{δs} + \frac{δf}{δz} \times \frac{δz}{δs}$$
$$(y + z)(t) + (x + z)(te^{st}) + (y + x)(0)$$
Evaluate
$$x(0, 1), y(0, 1), z(0, 1)$$
When $(s, t) = (0, 1)$: $x(0, 1) = (0)1 = 0$, $y(0, 1) = e^{0} = 1$, $z(0, 1) =. 1$
Answer
#### $$\frac{δf}{δs}|_{(s, t) = (0, 1)} = (1 + 1)(1) + (0 + 1)(1 \times e^{0}) = 2 + 1(1) = 3$$
```


___
# References
