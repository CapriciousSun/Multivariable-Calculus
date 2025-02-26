20250220103419

Tags:

Green's Theorem refers to a domain $D$ whose boundary is $\partial D$, and is a positively oriented, simple closed curve in the plane. 

## Definition
A simple close curve is one that does not intersect itself at any point other than the endpoints. A positively oriented curve is one where the boundary curve $C = \partial D$ is traced counter-clockwise. 
```ad-formula
#### Green's Theorem Circular Integral
If $\vec{F} = \langle F_{1}, F_{2} \rangle$ where $F_{1}$ and $F_{2}$ have continuous partial derivatives, then the line integral for this field is defined as
#### $$\oint_{\partial D} \vec{F} \cdot d\vec{r} = \oint_{\partial D} F_{1}dx + F_{2}dy = \int \int_{\partial D} \left( \frac{\partial F_{2}}{\partial x} - \frac{\partial F_{1}}{\partial y} \right)dA$$
A note to make is that if $\frac{\partial F_{2}}{\partial x} - \frac{\partial F_{1}}{\partial y} = 1$, then $\oint_{\partial D} \vec{F} \cdot d\vec{r} = \int \int_{D} 1dA = \text{Area}(D)$. There are other formulas for calculating the area of $D$ enclosed by an area C is $C = \oint_{C} x dy = \oint_{C} -ydx = \frac{1}{2} \oint_{C} xdy - ydx$
```

A more general form of Green's theorem is for a domain whose boundary consists of more than one simple curve. Positively-oriented if the region $D$ lies to the left as the boundary curve $\partial D$ is traversed. 
```ad-example
Consider the following region where $D$ is a rectangle with $c_{1}$ and $c_{2}$ are both going counterclockwise, with $c_{1}$ being the perimeter of $D$ and $c_{2}$ being the perimeter of a smaller rectangle inside of $D$. If we get the line integral of $c_{1}$
#### $$\begin{cases} \oint_{c_{1}} \vec{F} \cdot d\vec{r} = 4 \\ \int \int_{D} \left( \frac{\partial F_{2}}{\partial x} - \frac{\partial F_{1}}{\partial y} \right)dA = 1 \end{cases}$$
calculating $\oint_{c_{2}} \vec{F} \cdot d\vec{r}$ requires the use of Green's theorem. 
#### $$\begin{gather*} \partial D = c_{1} - c_{2} \\ \oint_{\partial D} \vec{F} \cdot d\vec{r} = \oint_{c_{1}}F \cdot d\vec{r} - \oint_{c_{2}} \vec{F} \cdot d\vec{r} = 4 - \oint_{c_{2}} \vec{F} \cdot d\vec{r} \end{gather*}$$
By Green's theorem,
#### $$\oint_{\partial D} \vec{F} \cdot d\vec{r} = \int \int_{D} \left( \frac{\partial F_{2}}{\partial x} - \frac{\partial F_{1}}{\partial y} \right)dA = 1$$
So,
#### $$1 = 4 - \oint_{c_{2}} F \cdot d\vec{r} \implies \oint_{c_{2}} \vec{F} \cdot d\vec{r} = 3$$
```

## Curve That's not Closed
if $C$ is positively oriented, but not closed, add a segment $c_{1}$ to form a closed curve. Let $C$ and $c_{1}$ form the boundary of $D$, so that $\partial D = C + c_{1}$. Then
#### $$\int_{C} \vec{F} \cdot d\vec{r} + \int_{c_{1}} \vec{F} \cdot d\vec{r} = \oint_{\partial D} \vec{F} \cdot d\vec{r} = \int \int_{D} \left( \frac{\partial F_{2}}{\partial x} - \frac{\partial F_{1}}{\partial y} \right)dA \implies \int_{C} \vec{F} \cdot d\vec{r} = \int \int_{D} \left( \frac{\partial F_{2}}{\partial x} - \frac{\partial F_{1}}{\partial y} \right)dA - \int_{c_{1}} \vec{F} \cdot d\vec{r}$$

#### Example
Compute the line integral of $\vec{F} = \langle x^{3}, 4x \rangle$ along the path from $A = (-1, 0)$ to $B = (-1, -1)$ in the given figure. To save work, we can add a line segment $c_{1}$ from $B$ to $A$ to use Green's theorem ![[Pasted image 20250220110013.png|400]]
The boundary of $D$ is $C + c_{1}$. 
#### $$\oint_{\partial D} \vec{F} \cdot d\vec{r} = \int_{C} \vec{F} \cdot d\vec{r} + \int_{c_{1}} F \cdot d\vec{r} = \int \int_{D} \left( \frac{\partial F_{2}}{\partial x} - \frac{\partial F_{1}}{\partial y} \right)dA \implies \int_{C} \vec{F} \cdot d\vec{r} = \int \int_{D} \left( \frac{\partial F_{2}}{\partial x} - \frac{\partial F_{1}}{\partial y} \right)dA - \int_{c_{1}} \vec{F} \cdot d\vec{r}$$
So to solve this system, 
#### $$\int_{c_{1}} \vec{F} \cdot d\vec{r} : c_{1} : \vec{r}(t) = \langle -1, t \rangle, -1 ≤ t ≤ 0$$
#### $$\vec{r^{'}}(t) = \langle 0, 1 \rangle : \int_{c_{1}} \vec{F} \cdot d\vec{r} = \int_{-1}^{0} \langle -1, -4 \rangle \cdot \langle 0, 1 \rangle = \int_{-1}^{0} -4dt = -4t\vert_{-1}^{0} = -4(0) - (-4(-1)) = -4$$
To solve this integral
#### $$\begin{gather*}
\int \int_{D} \left( \frac{\partial F_{2}}{\partial x} - \frac{\partial F_{1}}{\partial y} \right)dA = \int \int_{D} \left( \frac{\partial}{\partial x}[4x] - \frac{\partial}{\partial y}[x^{3}] \right)dA = \int \int_{D} 4dA = 4 \text{Area}(D) = 4(3 * 1 + 1 * 1) = 16 \\
\therefore \int_{C}\vec{F} \cdot d\vec{r} = 16 - (-4) = 20
\end{gather*}$$

#### Example
Evaluate $\int \int_{D} xydA$ where $D$ is the region bounded by the curves $y = x$ and $y = \sqrt{ x }$. This is vertically simple system 
#### $$D: \begin{cases}
0 ≤ x ≤ 1 \\
x ≤ y ≤ \sqrt{ x }
\end{cases}$$
The bounds for $x$ is found with $$\begin{gather}
x = \sqrt{ x } \\
x^{2} = x \\
x^{2} - x = 0 \\
x(x - 1) = 0 \\
x = 0, x = 1
\end{gather}$$
#### $$\int \int_{D} xydA = \int_{0}^{1} \int_{x}^{\sqrt{ x }} xydy\ dx = \int_{0}^{1} \left.\frac{1}{2}xy^{2}\right\vert_{x}^{\sqrt{ x }}dx = \frac{1}{24}$$

#### Example
Compute the integral $\int \int_{D} (x^{2} + y^{2})dA$ using polar coordinates, where $D$ is the region bounded between the circles $x^{2} + y^{2} = 4$, $x^{2} + y^{2} = 9$, and $x ≥ 0$, $y ≥ 0$.
#### $$\text{In polar D:} \begin{cases}
2 ≤ r ≤ 3 \\
0 ≤ θ ≤ \frac{π}{2}
\end{cases}$$
#### $$\int \int_{D} (x^{2} + y^{2})dA = \int_{0}^{π/2} \int_{2}^{3} r^{2} \cdot rdr\ dθ = \frac{65π}{8}$$
This can also be split into two separate integrals
#### $$\left( \int_{0}^{π/2} 1dθ \right)\left( \int_{2}^{3} r^{3}dr \right)$$
This can only be done on rectangles, regular and polar, and boxes. 

#### Example
Calculate the integral of $f(x, y) = (x^{2} + y^{2})^{-3/2}$ over the region $D$ given by $x^{2} + y^{2} ≤ 16, x + y ≥ 4$ by changing to polar coordinates. 
#### $$D: \begin{cases}
\frac{4}{\cos(θ) + \sin(θ)} ≤ r ≤ 4 \\
0 ≤ θ ≤ \frac{π}{2}
\end{cases}$$
The derivation for $r_{1}$ is 
$$x + y = 4 \implies r_{1}\cos(θ) + r_{1}\sin(θ) = 4 \implies r_{1}(\cos(θ) + \sin(θ)) = 4 \implies r_{1} = \frac{4}{\cos(θ) + \sin(θ)}$$
#### $$\int \int_{D} (x^{2} + y^{2})^{3/2}dA = \int_{0}^{π/2} \int_{\frac{4}{\cos(θ) + \sin(θ)}}^{4} (r^{2})^{-3/2}r dr\ dθ = \int_{0}^{π/2} \int_{\frac{4}{\cos(θ) + \sin(θ)}}^{4} r^{-2} dr\ dθ = \frac{1}{2} - \frac{π}{8}$$

#### Example
Evaluate $\int \int \int_{B} (xz + yz^{2})dV$, where $B = [0, 1] \times [2, 4] \times [0, 2]$
#### $$\int \int \int_{B} (xz + yz^{2})dV = \int_{0}^{1} \int_{0}^{2} \int_{2}^{4} (xz + yz^{2})dy\ dz\ dx = 18$$

#### Example
Evaluate $\int \int \int_{W} 66zdV$ where $w: x^{2} ≤ y ≤ 1, 0 ≤ x ≤ 1, x - y ≤ z ≤ x + y$.  
#### $$\int \int \int_{W} 66zdV = \int_{0}^{1} \int_{x^{2}}^{1} \int_{x - y}^{x + y} 66z dz\ dy\ dx = 22$$

#### Example
Find $(a) div (\vec{F})$ and $(b) curl (\vec{F})$ for $\vec{F} = \langle xy, e^{2y + 3z}, x^{2} + z^{2}$
#### $$div(\vec{F}) = \nabla \cdot \vec{F} = \frac{\partial}{\partial x}$$
#### $$curl(\vec{F})$$
$$a) div(\vec{F}) = y + 2e^{2y + 3z} + 2z$$
$$b) curl(\vec{F}) = \langle -3e^{2y + 3z}, -2x, -x \rangle$$
