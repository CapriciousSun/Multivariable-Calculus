20250113110729

Tags:

The gradient of a function is a measure of its rate of change and the function at which it is changing.

## Formula
```ad-formula
#### Gradient of a formula
The gradient of a point on a function is
$$\nabla f_{p} = \nabla f(a, b) = \langle f_{x}(a, b), f_{y}(a, b)\rangle$$
```

The point $P$ may be omitted and the gradient of $f$ is the vector of the partial derivatives of $f$. The gradient $\nabla f$ assigns a vector $\nabla f_{p}$ to each point $P$ in the domain of the function $f$. 

## Dependency of Number of Variables
In $\mathbb{R}^{2}$, the gradient is $\nabla = \langle \frac{δ}{δx}, \frac{δ}{δy} \rangle$, and in $\mathbb{R}^{3}$, the gradient is $\nabla = \langle \frac{δ}{δx}, \frac{δ}{δy}, \frac{δ}{δz} \rangle$, and so on.

```ad-example
#### $f(x, y) = x^{2} + y^{2}$
Answer
#### $$\nabla f = \langle \frac{δf}{δx}, \frac{δf}{δy} \rangle = \langle 2x, 2y \rangle$$
```

```ad-example
#### $f(x, y, z) = x^{2} + 3y^{3}z$
$$f_{x}(x, y, z) = 2x$$
$$f_{y}(x, y, z) = 9y^{2}z$$
$$f_{z}(x, y, z) = 3y^{3}$$
Answer
#### $$\nabla f = \langle 2x, 9y^{2}z, 3y^{3} \rangle$$
```

## Gradient as a Normal Vector
If there were a point $P(a, b, c)$ on a surface fiven by $F(x, y, z) = K$ for a constant $K$ and assuming $\nabla F_{p} = \vec{o}$, then $\nabla F_{p}$ is normal to the [[Tangents#Tangent Plane|tangent plane]] to the surface at $P$. The equation of the tangent plane can be written as 
```ad-formula
#### $$F_{x}(a, b, c)(x - a) + F_{y}(a, b, c)(y - b) + F_{z}(z, b, c)(z - c) = 0$$
or 
#### $$\nabla F_{p} \cdot \langle x - a, y - b, z - c \rangle = 0$$
```

If $z = f(x, y)$, 
```ad-example
#### Find an equation of the tangent plane to $\underbrace{x^{2} + 2y^{2} + 5z^{2}}_{F(x, y, z) = K} = 8$ at $(1, 1, -1)$
$$\nabla F = \langle 2x, 4y, 10z \rangle$$
$$\nabla F_{p} = \nabla F(1, 1, -1) = \langle 2, 4, -10 \rangle$$
Answer
#### $$2(x - 1) + 4(y - 1) -10(z + 1) = 0$$
```


___
# References
