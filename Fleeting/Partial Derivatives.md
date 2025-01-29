20250106113314

Tags:

A partial derivative is a rate of change with respect to individual variables separately. 
```ad-example
#### Partial Derivatives
Given a [[Functions|function]] $z = f(x, y)$
$$\frac{\partial f}{\partial x} = \lim_{ h \to 0 }\frac{f(x + h, y) - f(x, y)}{h}$$
has a fixed y and $$\frac{\partial f}{\partial y} = \lim_{ k \to 0 }\frac{f(x, y + k) - f(x, y)}{k}$$
has a fixed x.
```

## Geometric Interpretation
Partial derivatives are essentially [[Graphs#Analysis|traces]], where the vertical curve is intersected and the derivative of the curve is taken. Another way of interpreting it geometrically is the slope of surface in the direction that the partial derivative is taken in. 

```ad-example
#### $f(x, y) = x^{3}y + \ln(x + y)$
$$f_{x} = 3x^2y + \frac{1}{x + y}$$
$$f_{y} = x^{3} + \frac{1}{x + y}$$
```

```ad-example
#### $f(x, y) = x^{3}y + ln(x^2 + 4y^{3})$
$$f_{x} = 3x^{2}y + \frac{2x}{x^{2} + 4y^{3}}$$
$$f_{y} = x^{3} + \frac{12y^{2}}{x^2 + 4y^{3}}$$
```

```ad-example
#### $f(x, y) = x^{2}e^{xy}$
$$f_{x} = \frac{\partial}{\partial y}(x^{2}e^{xy}) = \frac{\partial}{\partial x}(x^{2})e^{xy} + x^{2}\frac{\partial}{\partial x}(e^{xy} = 2xe^{xy} + x^{2}e^{xy}y = (2x + x^{2}y)e^{xy}$$
$$f_{y} = \frac{\partial}{\partial y}(x^{2}e^{xy}) = x^{2}\frac{\partial}{\partial x}(e^{xy}) = x^{2}(xe^{xy}) = x^{3}e^{xy}$$
#### Answer
#### $$f_{x} = (2x + x^{2}y)e^{xy}$$
#### $$f_{y} = x^{3}e^{xy}$$
```

## Higher Order Partial Derivatives
The notation for every layer of partial derivatives is done so with subscript. For example, 2nd order partial derivatives are noted as $f_{xx}$ and $f_{xy}$, each subscript meaning a derivative in terms of. The order of mixed partials does not matter, with $f_{xy}$ and $f_{yx}$ meaning the same things. This is true for higher order partial derivatives as well. This is refer to as Clairaut's Theorem. 

All of the following examples are done with $f_{x} = x^{2}e^{xy}$ 
```ad-example
#### $f_{xx} = \frac{δ}{δx}(f_{x})$
$$\frac{δ}{δx}\left[(dx + x^{2}y)e^{xy}\right] = (2 + 2xy)e^{xy} + (2x + x^{2}y)ye^{xy}$$
Answer
#### $$(2 + 4xy + x^{2}y^{2})e^{xy}$$
```

```ad-example
#### $f_{xy} = \frac{δ}{δy}(f_{x})$
$$\frac{δ}{δy}\left[(2x + x^{2}y)e^{xy}\right] = (x^{2})e^{xy} + (2x + x^{2}y)xe^{xy}$$
Answer
#### $$(3x^{2} + x^{3}y)e^{xy}$$
```

```ad-example
#### $f_{yx} = \frac{δ}{δx}(f_{y})$
$$\frac{δ}{δx}\left[x^{3}e^{xy}\right] = 3x^{2}e^{xy} + x^{3}ye^{xy}$$
Answer
#### $$(3x^{2} + x^{3}y)e^{xy}$$
```

```ad-example
#### $f_{yy} = \frac{δ}{δy}(f_{y})$
$$\frac{δ}{δy}\left[x^{3}e^{xy}\right] = x^{3}xe^{xy}$$
Answer
#### $$x^{4}e^{xy}$$
```

## Variable Function
For a function $f(x, y, z) = yz\ln(xy)$, these are the following examples.
```ad-example
#### $f_{x}(x, y, z)$
$$yz \times \frac{1}{xy}y = \frac{yz}{x}$$
Answer
#### $$\frac{yz}{x}$$
```

```ad-example
#### $f_{y}(x, y, z)$
$$\frac{δ}{δx}\left[(yz)ln(xy)\right] = zln(xy) + yz \times \frac{1}{xy}x = zln(xy) + z$$
Answer
#### $$zln(xy) + z$$
```

```ad-example
#### $f_{z}(x, y, z)$
Answer
#### $$yln(xy)$$
```

```ad-example
#### $f_{yzx}$
$$f_{yz}(x, y, z) = \frac{δ}{δz}\left[zln(xy) + z\right] = ln(xy) + 1$$
$$f_{yzx}(x, y, z) = \frac{δ}{δx}\left[ln(xy) + 1\right] = \frac{1}{xy}y = \frac{1}{x}$$
Answer
#### $$\frac{1}{x}$$
```

```ad-example
#### $f_{zxy}$
$$f_{zx}(x, y, z) = \frac{δ}{δx}\left[yln(xy)\right] = y \times \frac{1}{xy}y = \frac{y}{x}$$
$$f_{zxy} = \frac{δ}{δx}\left[\frac{y}{x}\right] = \frac{1}{x}$$
Answer
#### $$\frac{1}{x}$$
```

___
# References
