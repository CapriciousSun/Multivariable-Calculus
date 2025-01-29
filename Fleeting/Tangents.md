20250109111835

Tags: 

## Tangent Line
Tangents lines are lines normal to the slope of a [[Graphs|graph]]. 
```ad-example
#### Tangent Line Formula
For a graph $y = f(x)$ wit point $P(a, f(a))$, the tangent line is $y - f(a) = f'(a)(x - a)$ or $y = f(a) + f'(a)(x - a)$. The tangent line gives the [[Linear Approximation|"linear approximation"]] to $y = f(x)$ for $x \approx a$. 
![[Pasted image 20250126174044.png]]
$\therefore f(x) \approx f(a) + f'(a)(x - a)$ when $x$ is near $a$
```

## Tangent Plane
The tangent plane is a plane normal to a surface. It is determined by intersecting the tangent lines of the $x$ trace curve and the $y$ trace curve. The equation of the tangent plane needs two non-parallel vectors on the plane, noted by $\vec{v}$ and $\vec{w}$.
```ad-note
#### $\vec{v}$ is tangent to the surface and lies in the plane $y = b$
Move 1 unit in the positive x-direction, 0 in the y-direction, and $f_{x}(a, b)$ units in the z-direction. 
#### $\therefore \vec{v} = \langle 1, 0, f_{x}(a, b) \rangle$
```

```ad-note
#### $\vec{w}$ is tangent to the surface and lies in the plane $x = a$
Move 0 units in the x-direction, 1 unit in the positive y-direction, and $f_y(a, b)$ units in the z-direction.
#### $\therefore \vec{w} = \langle 0, 1, f_{y}(a, b) \rangle$
```

Then, from these two vectors, the cross product of the two lines is the plane. 
```ad-note
#### Tangent Plane Formula 
With the two tangent line vectors, the normal vector $\vec{n}$ can be obtained by taking their cross product.
$$\vec{n} = \vec{v} \times \vec{w} = \begin{vmatrix}\hat{i} & \hat{j} & \hat{k} \\ 0 & 1 & f_{y}(a, b) \\ 1 & 0 & f_{x}(a, b)\end{vmatrix} = \langle f_{x}(a, b), f_{y}(a, b), -1 \rangle$$
The formula for a plane that passes thorugh a point $P(x_{0}, y_{0}, z_{0})$ and has a normal vector $\vec{n} = \langle a, b, c \rangle$ is $$a(x - x_{0}) + b(y - y_{0}) + c(z - z_{0}) = 0$$
Hence, the formula for the tangent plane that passes through point $(a, b, f(a, b))$ with normal vector $\vec{n} = \langle f_{x}(a, b), f_{y}(a, b), -1 \rangle$ is $f_{x}(a, b)(x - a) + f_{y}(a, b)(y - b) - 1(z - f(a, b)) = 0$ or
#### $$Z = f(a, b) + f_{x}(a, b)(x - a) + f_{y}(a, b)(y - b)$$
```

```ad-example
#### Find the equation of the tangent plane to $f(x, y) = x^{2}y - 4xy^{3}$ at the point $(1, -1)$
$$f(1, -1) = 1^{2}(-1) - 4(1)(-1)^{3} = -1 + 4 = 3$$
$$f_{x}(x, y) = 2xy - 4y^{3} \implies f_{x}(1, -1) = 2(1)-1)4(-1)^{3} = 2$$
$$f_{y}(x, y) = x^2 - 12xy^{2} \implies f_{y}(1, -1) = 1^{2} - 12(1)(-1)^{2} = -11$$
Tangent plane at $(1, -1)$ is $Z = 3 + 2(x - 1) + -11(y + 1)$
#### Answer
#### $$3 + 2x - 2 - 11y - 11 = -10 + 2x - 11y$$
```

In order for the plane to be tangent to the surface $Z = f(x, y)$ at $P(a, b, f(a, b))$, $f(x, y)$ must be locally linear. In other words, $f(x, y)$ is differentiable at $(a, b)$ if it's locally linear at $(a, b, f(a, b))$. 
```ad-example
#### Find the point(s) on the graph of $Z = 3x^{2} - 4y^{2}$ at which $\vec{n} = <3, 2, 2>$ is normal to the tangent plane
Since $\vec{n} = <f_{x}(a, b), f_{y}(a, b), -1>$ is the normal vector, the scaled version $\vec{n} = \langle -\frac{3}{2}, -1, -1 \rangle$. So $f_{x}(a, b) = -\frac{3}{2}$ and $f_{y}(a, b) = -1$. 
$$f(x, y) = 3x^{2} - 4y^{2} \implies f_{x}(x, y) = 6x \text{ and } f_{y}(x, y) = -8y$$ 
$$6x = -\frac{3}{2} \implies x = -\frac{1}{4}$$
$$-8y = -1 \implies y = \frac{1}{8}$$
#### Answer
#### $$\left(-\frac{1}{4}, \frac{1}{8}, \frac{1}{8}\right)$$
```

___
# References
[[MATH2010_14.3_14.4.pdf]]
