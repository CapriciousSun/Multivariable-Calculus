 20250113103505

A linear approximation stipulates, if a function $f(x, y)$ is differentiable at $(a, b)$, then the [[Tangents#Tangent Plane|tangent plane]] may be used to approximate the value of $f$ for values $(x, y)$ at $(a, b)$. 

## Linearization Equation
The linearization of $f$ at $(a, b)$ is as below.
```ad-formula
#### Linearization Formula
#### $$L(x, y) = f(a, b) + f_{x}(a, b)(x - a) + f_{y}(a, b)(y - b)$$
#### $$f(x, y) \approx L(x, y)\text{ for } (x, y)\text{ near }(a, b)$$
```

We can also write $x = a + Δx$ and $y = b + Δy$ so the linear approximation here is 
#### $$f(\underbrace{a + Δx}_{\text{"x"}}, \underbrace{b + Δy}_{\text{"y"}}) \approx f_{x}(a, b)Δx + f_{y}(a, b)Δy$$
#### $$Δf = f(x, y) - f(a, b) \approx f_{x}(a, b)Δx + f_{y}(a, b)Δy$$
Therefore, the differential of the function $f$, $df$, is defined as
```ad-formula
#### Differential of function $f$
#### $$df = f_{x}(x, y)dx + f_{y}(x, y)dy$$
where $Δx = dx$ and $Δy = dy$
```

The actual change of the function is approximate $df$, or $Δf \approx df$. It is almost the exact same equation as the tangent plane. 

```ad-example
#### Use linearization to approximate $\frac{3.03}{1.99}$
Whole numbers should be used here for approximation, so
$$f(3, 2) = \frac{3}{2}$$
$$f(x, y) = \frac{x}{y} = \frac{1}{y} \times x \implies f_{x}(x, y) = \frac{1}{y} \implies f_{x}(3, 2) = \frac{1}{2}$$
$$f(x, y) = x \times y^{-1} \implies f_{y}(x, y) = -x \times y^{-2} = \frac{-x}{y^{2}} \implies f_{y}(3, 2) = \frac{-3}{4}$$
$$L(x, y) = \frac{3}{2} + \frac{1}{2}(x - 3) - \frac{3}{4}(y - 2)$$
Answer
#### $$f(\underbrace{3.03}_{\text{"x"}}, \underbrace{1.99}_{\text{"y"}}) \approx L(3.03, 1.99) = \frac{3}{2} + \frac{1}{2}(3.03 - 3) - \frac{3}{4}(1.99 - 2) = 1.5225$$
```

```ad-example
#### Differential of $\frac{3.03}{1.99}$
#### $$Δf = f(3.03, 1.99) - f(3, 2)$$
#### $$Δf \approx df = f_{x}(3, 2)dx + f_{y}(a, b)dy = \frac{1}{2}(0.03) - \frac{3}{4}(-0.01) = 0.0225$$
```

## More than 3 Variables
The linearization formula extends to more than 3 variables.
```ad-formula
#### More than 3 Variable Linearization
#### $$f(x, y, z) \approx f(a, b, c) + f_{x}(a, b, c)(x - a) + f_{y}(a, b, c)(y - b) + f_{z}(a, b, c)(z - c)$$
and
#### $$Δf \approx f(a, b, c)Δx + f_{y}(a, b, c)Δy + f_{z}(a, b, c)Δz$$
```

___
# References
[[MATH2010_1316_0101325.pdf]]
