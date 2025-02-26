20250223123030

Tags:

There have to be considerations for $\int \int_{D} f(x, y)dA$ where $D$ is not a rectangle. These are called general regions, where between bounds are placed in context of regions. 
## Simple Regions
There are two kinds of simple regions, vertically simple and horizontally simple. 
```ad-formula
#### Vertically Simple Region
$D$ is a vertically simple region if $a ≤ x ≤ b,\ g_{1}(x) ≤ y ≤ g_{2}(x)$. If that's the case,
#### $$\int \int_{D}f(x, y)dA = \int_{a}^{b}\int_{g_{1}(x)}^{g_{2}(x)}f(x, y)dy\ dx$$
```

```ad-formula
#### Horizontally Simple Region
$D$ is a horizontally simple region if $c ≤ y ≤ d,\ h_{1}(y) ≤ x ≤ h_{2}(y)$. If that's the case
#### $$\int \int_{D}f(x, y)dA = \int_{c}^{d}\int_{h_{1}(y)}^{h_{2}(y)}f(x, y)dx\ dy$$
```

#### Finding the Bounds
The bounds of $D$ can be found by evaluating the graph. If the graph is both vertically simple and horizontally simple, it should be evaluated as a vertically simple region. The way the function is bounded is always provided, so all that is left is to equate the bounds and find the roots.

#### Example
For a function $\int \int_{D}(x^{2} + y)dA$ where $D$ is the region bounded by $y = x^{2}$ and $y = 2x$. It is vertically simple and horizontally simple. The points of intersection are found with $$x^{2} = 2x \implies x^{2} - 2x = 0 \implies x = 0\text{ and } x = 2$$
The bounds for a vertically simple region is $$\begin{cases}
0 ≤ x ≤ 2 \\
x^{2} ≤ y ≤ 2x
\end{cases}$$The integral for solving for the vertically simple region looks like $$\begin{gather*}
\int \int_{D}(x^{2} + y)dA = \int_{0}^{2}\int_{x^{2}}^{2x}(x^{2} + y)dy\ dx = \int_{0}^{2}\left.\left( x^{2}y + \frac{y^{2}}{2}\right\vert_{y = x^{2}}^{y = 2x} \right)dx = \\
\int_{0}^{2}\left[ \left( x^{2}(2x) + \frac{(2x)^{2}}{2} \right) - \left( x^{2}\left( x^{2} + \frac{(x^{2})^{2}}{2} \right) \right)\right]dx = \int_{0}^{2}\left( 2x^{3} + 2x^{2} - \frac{3}{2}x^{4} \right)dx = \frac{56}{15}
\end{gather*}$$
For a horizontally simple region $$\begin{cases}
0 ≤ y ≤ 4 \implies\\
\frac{y}{2} ≤ x ≤ \sqrt{ y }
\end{cases}$$
So the integral for solving for this region is $$\begin{gather*}
\int_{0}^{4}\int_{\frac{y}{2}}^{\sqrt{ y }}(x^{2} + y)dx\ dy
\end{gather*}$$

#### Example
For a function $\int \int_{D}xydA$ where $D$ is the region bounded by $y = x - 1$ and $y^{2} = 2x + 6$. When sketched, it's revealed that this function is not vertically simple, but it is horizontally simple. The horizontal system for this is $$\begin{cases}
y = x - 1 \implies x = y + 1 \\
y^{2} = 2x + 6 \implies x = \frac{y^{2} - 6}{2}
\end{cases}$$
The points of intersection to find are $$\begin{gather*}
\frac{y^{2} - 6}{2} = y + 1 \implies y^{2} - 6 = 2y + 2 \implies y^{2} - 2y - 8 = 0 \implies (y - 4)(y + 2) = 0 \\
\Downarrow \\
y = 4\text{ and }y = -2
\end{gather*}$$
$$\begin{gather*}
\int \int_{D}xydA = \int_{-2}^{4}\int_{\frac{y^{2} - 6}{2}}^{y + 1}xydx\ dy = \int_{-2}^{4} \left.\frac{1}{2}x^{2}y\right|_{x =\frac{ y^{2} - 6}{2}}^{x = y + 1}dy = \int_{-2}^{4}\left[ \frac{1}{2}(y + 1)^{2}y - \frac{1}{2}\left( \frac{y^{2} - 6}{2} \right)^{2}y \right]dy = 36
\end{gather*}$$

## Non-Simple Regions
If $D$ is not a simple region, then it can be split into the sum of multiple simple regions.
```ad-formula
#### Splitting a Non-Simple Region
For a function $\int \int_{D}f(x, y)dA$ that is not a simple region, it can be split.
#### $$\int_{a}^{c}\int _{g_{1}(x)}^{g_{2}(x)}f(x, y)dy\ dx + \int_{c}^{b}\int_{g_{2}(x)}^{g_{1}(x)}f(x, y)dy\ dx$$
![[Pasted image 20250223125042.png]]
```

This introduces theorem 3
```ad-formula
#### Theorem 3 of Multivariable Caluclus
For functions $f(x, y)$ and $g(x, y)$ that are integrable functions on $D$, if $f(x, y) ≤ g(x, y)$ for all $(x, y) \in D$, then
#### $$\int \int_{D}f(x, y) dA ≤ \int \int_{D}g(x, y)dA$$
If $m ≤ f(x, t) ≤ M$ for all $(x, y) \in t D$, then
#### $$m \cdot \text{Area}(D) ≤ \int \int_{D}f(x, y)dA ≤ M \cdot \text{Area}(D)$$
```

What this leads to is the fact that double integrals over more general regions $D$ satisfy the same linearity that [[Integrals of Rectangles|integrals over rectangles]] have. 

#### Example
Evaluate $\int \int_{D}xydA$ where $D$ is a region between $y = x^{3}$ and $y = x$. The points of intersection would be $$\begin{gather*}
x^{3} = x \implies x^{3} - x = 0 \implies x(x^{2} - 1) = 0 \implies x(x + 1))x - 1) = 0 \\
\Downarrow \\
x = 0,\ x = -1,\ x = 1
\end{gather*}$$
The integral would then be $$\begin{gather*}
\int \int_{D}xydA = \int \int_{D_{1}}xydA + \int \int_{D_{2}}xydA = \int_{-1}^{0}\int_{x}^{x^{3}}xydy\ dx + \int_{0}^{1}\int_{x^{3}}^{x}xydy\ dx = \frac{1}{8}
\end{gather*}$$

#### Example
Evaluate $\int_{0}^{1}\int_{x}^{1}\sin(y^{2})dy\ dx$. To solve this, the order of integration needs to be changed. Looking at $D$, the system is $$\begin{cases}
0 ≤ x ≤ 1 \\
x ≤ y ≤ 1
\end{cases}$$
The integral has to be setup so that it switches from a vertically simple region to a horizontally simple region. The horizontally simple region transforms the system to $$\begin{cases}
0 ≤ y ≤ 1 \\
0 ≤ x ≤ y
\end{cases}$$
The new integral would look like $$\begin{gather*}
\int_{0}^{1}\int_{x}^{1}\sin(y^{2})dy\ dx = \int_{0}^{1}\int_{0}^{y}\sin(y^{2})dx\ dy = \int_{0}^{1} \left.\sin(y^{2})x\right\vert_{x = 0}^{x = y}dy = \int_{0}^{1}[\sin(y^{2})y - \sin(y^{2})(0)]dy \\
= \int_{0}^{1}y\sin(y^{2})dy = \frac{1}{2}\int_{0}^{1}\sin(u)du = -\frac{1}{2}\left.\cos(u)\right\vert_{0}^{1} = -\frac{1}{2}(\cos(1) - \cos(0)) = -\frac{1}{2}(\cos(1) - \cos(0))
\end{gather*}$$

#### Example
Evaluate $\int_{1}^{e}\int_{0}{\ln(x)}f(x, y)dy\ dx$. This also requires a change of the order of integration. The system for $D$ is $$\begin{cases}
0 ≤ y ≤ \ln(x) \\
1 ≤ x ≤ e
\end{cases}$$
This region is vertically simple, so it needs to be switched to a horizontally simple one. The system is $$\begin{cases}
e^{y} ≤ x ≤ e \\
0 ≤ y ≤ 1
\end{cases}$$
The setup for the integral is $$\begin{gather*}
\int_{1}^{e}\int_{0}^{\ln(x)}f(x, y)dy\ dx = \int_{0}^{1}\int_{e^{y}}^{e}f(x, y)dx\ dy
\end{gather*}$$

## Integrals of Domains
Domains can be the union of many other domains. 
```ad-formula
#### Integrals of Union of Domains
If $D$ is the union of domains $D_{1}, D_{2}, \dots, D_{N}$ and they do not overlap, then their volume is the sum of all the domains' integrals.
#### $$\int \int_{D} f(x, y)dA = \int \int_{D_{1}} f(x, y)dA + \dots + \int \int_{D_{N}} f(x, y)dA$$
```

___
# References
[[MATH2010_15.1_15.2.pdf]]
