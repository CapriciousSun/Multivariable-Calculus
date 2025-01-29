20250116113937

Tags:

Assume that $F(x, y, z(x, y)) = 0$ implicitly defines $z$ as a differentiable function of $x$ and $y$. We use the chain rule to find $\frac{δz}{δx}$ and $\frac{δx}{dy}$.
```ad-formula
$$\frac{δ}{δx}[F(x, y, z(x, y))] = \frac{δ}{δx}[0]$$
$$\frac{δF}{δx}\frac{δx}{δx} + \frac{δF}{δy}\frac{δy}{δx} + \frac{δF}{δz}\frac{δz}{δx} = 0 \implies F_{x} + F_{z}\frac{δz}{δx} = 0 \implies $$
$$\begin{cases}\frac{δz}{δx} = -\frac{F_{x}}{F_{z}}, \text{ if } F_t ≠ 0 \\ \frac{δz}{δy} = -\frac{F_{y}}{F_{z}}, \text{ if } F_{t} ≠ 0\end{cases}$$
```

```ad-example
#### Find $\frac{δz}{δx}$ and $\frac{δz}{δy}$ if $x^{3} + y^{3} + z^{3} + 6xyz = 1$
$$F(x, y, z) = x^{3} + y^{3} + z^{3} + 6xyz - 1 = 0$$
$$F_{x} = 3x^{2} + 6yz$$
$$F_{y} = 3y^{2} + 6xz$$
$$F_{z} = 3z^{2} + 6xy$$
$$Z_{x} = \frac{δz}{δx} = -\frac{F_{x}}{F_{z}} = -\frac{3x^{2}} + 6yz$$
```
