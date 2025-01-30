20250129011825

Tags:

## 14.3 Partial Derivatives
#### The Basics
Partial derivatives are the basis of most calculations in the following sections. The only thing to remember is the notation $f_{x}$, where $x$ is the basis that the partial derivation is in. So for a function $f(x, y)$, $f_{x}(x, y)$ means ignoring all $y$ values and treating it as a constant.

## Visualization of a Partial Derivative
For a multivariable system, a partial derivative of the function can be interpreted as taking the slope of a slice of the function. 
![[Pasted image 20250129013316.png]]

#### Example
For a function $f(x, y) = x^{4}y + xy^{-2}$ 
#### $$\begin{cases}
f_{x}(x, y) = \frac{\partial}{\partial x}(x^{4}y + xy^{-2}) = 4x^{3}y + y^{-2} \\
f_{y}(x, y) = \frac{\partial}{\partial y}(x^{4}y + xy^{-2}) = x^{4} - 2xy^{-3}
\end{cases}$$

## Higher Order Partial Derivatives
Higher order partial derivatives are much like higher order normal derivatives. They are notated by more letters in the subscript. It should be noted that the order of the partial derivatives does not matter. 
#### $$f_{xy} = f_{yx}$$

#### Example
For a function $f(x, y) = x^{2}e^{xy}$, the 1st order partial derivatives
#### $$\begin{cases}
f_{x}(x, y) = (2x + x^{2}y)e^{xy} \\
f_{y}(x, y) = x^{3}e^{xy}
\end{cases}$$
From these 1st order partial derivatives, the second order partial derivatives are
#### $$\begin{cases}
f_{xx}(x, y) = \frac{\partial}{\partial x}[(2x + x^{2}y)e^{xy}] = (2 + 2xy)e^{xy} + (2x + x^{2}y)ye^{xy} =  \\
(2 + 4xy + x^{2}y^{2})e^{xy} \\
f_{xy}(x, y) = \frac{\partial}{\partial y}[(2x + x^{2}y)e^{xy}] = x^{2}e^{xy} + (2x + x^{2}y)xe^{xy} = (3x^{2} + x^{3}y)e^{xy} \\
f_{yx}(x, y) = \frac{\partial}{\partial x}(x^{3}e^{xy}) = 3x^{2}e^{xy} + x^{3}ye^{xy} = (3x^{2} + x^{3}y)e^{xy} \\
f_{yy}(x, y) = \frac{\partial}{\partial y}(x^{3}e^{xy}) = x^{3}(xe^{xy}) = x^{4}e^{xy}
\end{cases}$$

## 14.4 Tangents and Linear Approximations
#### Tangents
There are two kinds of tangents, tangent lines and tangent planes. Tangent lines are the derivative taken on a trace. Tangent planes are the result of two tangent lines intersecting at a single point. The tangent plane of a function $f(x, y)$ at a point $P(a, b)$ requires a normal vector $\vec{n}$. Said normal vector is calculated with the formula
#### $$\vec{n} = \langle f_{x}(a, b), f_{y}(a, b), -1 \rangle$$
And the tangent plane is calculated with the formula 
#### $$Z = f(a, b) + f_{x}(a, b)(x - a) + f_{y}(a, b)(y - b)$$

#### Visualization of a Tangent Plane
The tangent plane being the intersection of two tangent lines at a point means that it's the cross product of two tangents. 
![[Pasted image 20250129021248.png|400]]


#### Example
For a function $f(x, y) = x^{2}y - 4xy^{3}$, the tangent plane at point $P(a, b) = (1, -1)$ is 
#### $$\begin{cases}
f(a, b) = 3 \\
f_{x}(x, y) = 2xy - 4y^{3} \implies f_{x}(1, -1) = 2 \\
f_{y}(x, y) = x^{2} - 12xy^{2} \implies f_{y}(1, -1) = -11
\end{cases}$$
Here, the normal vector calculation is not needed, as the partial derivatives of the function can be calculated without it. The answer would be
#### $$Z = 3 + 2(x - 1) - 11(x + 1) = 2x - 11y - 10$$

#### Example
For a function $f(x, y) = 3x^{2} - 4y^{2}$ with a normal vector $\vec{n} = \langle 3, 2, 2 \rangle$, the first step would be to normalize the vector so that the last number would be -1.
#### $$\langle 3, 2, 2 \rangle \implies \langle -\frac{3}{2}, -1, -1 \rangle$$
With this, the the points can be obtained from using the partial derivatives of $f(x, y)$
#### $$\begin{cases}
f_{x}(x, y) = 6x \implies 6x = -\frac{3}{2} \implies x = -\frac{1}{4} \\
f_{y}(x, y) = -8y \implies -8y = -1 \implies y = \frac{1}{8}
\end{cases}$$
#### $$\therefore \left( -\frac{1}{4}, \frac{1}{8}, \frac{1}{8} \right)$$
is the only possible point. 

#### Linear Approximation
Linear approximation uses the same formula as the tangent plane, since that's what linearization is, a slope normal to a surface defined by $f(x, y)$. This is used for linear approximation of functions, where point $P(a, b)$ is plugged into $Z(x, y)$ to obtain the approximate value at that point.  

## 14.5 The Gradient and Directional Derivatives
#### Gradient
A gradient is a vector that indicates the direction of greatest rate of change. In other words, it points at a local extrema. It is noted by a nabla, and the formula for a gradient of a function $f(x, y)$ at a point $P(a, b)$
#### $$\nabla f_{P} = \nabla f(a, b) = \langle f_{x}(a, b), f_{y}(a, b) \rangle$$

#### Example
For a function $$f(x, y) = x^{2} + y^{2}$$
The gradient would be calculated as $$\nabla f = \left\langle \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y} \right\rangle = \langle 2x, 2y \rangle$$

#### Chain Rule for Paths
The chain rule for paths allows a function $f(x, y)$ comprised of $x = x(t)$ and $y = y(t)$ to be differentiated over the basis $t$. Essentially, it allows the function to be parametrized. The formula for differentiating such a function over that basis is
#### $$\frac{df}{dt} = \frac{\partial f}{\partial x} * \frac{dx}{dt} + \frac{\partial f}{\partial y} * \frac{dy}{dt}$$

However, using the previous formula for a gradient and substituting in a $\vec{r}(t) = \langle x(t), y(t) \rangle$ into the function $f(x, y) = f(\vec{r}(t))$, then the formula can be reformatted to
#### $$\frac{d}{dt}f(\vec{r}(t)) = \nabla f(\vec{r}(t)) \cdot \vec{r}'(t)$$

#### Example
For a function $f(x, y, z) = x^{2} + 4yz^{3}$ and $\vec{r}(t) = \langle \sin(t), \cos(t), 1 + 6t \rangle$, the derivative would be calculated like
#### $$\begin{cases}
\nabla f = \langle 2x, 4z^{3}, 12yz^{2} \rangle \\
\nabla f(\vec{r}(t)) = \langle 2\sin(t), 4(1 + 6t)^{3}, 12\cos(t)(1 + 6t)^{2} \rangle \\
\vec{r}'(t) = \langle \cos(t), -\sin(t), 6 \rangle
\end{cases}$$
Combined together
#### $$\frac{d}{dt}f(\vec{r}(t)) = \langle 2\sin(t), 4(1 + 6t)^{3}, 12\cos(t)(1 + 6t)^{2} \rangle \cdot \langle \cos(t), -\sin(t), 6 \rangle$$
#### $$2\sin(t)\cos(t) - 4(1 + 6t)^{3}\sin(t) + 72\cos(t)(1 + 6t)^{2}$$

#### Directional Derivative
The directional derivative, unlike the partial derivative, does not require a "basis". In other words, it's based on the direction of a vector, not the direction of an axis. The directional derivative uses the same steps as the chain rule for paths, but instead a directional vector is given. The formula of a directional derivative for a function $f(x, y)$ with the direction of a unit vector $\vec{u}$ is
#### $$D_{\vec{u}}f(P) = \nabla f_{P} \cdot \vec{u}$$
The vector may be given as some random vector $\vec{v}$, so it must be converted to a unit vector. Finding a unit vector in the direction of the maximum rate of increase when given a $\nabla f_{P}$ based on a point is done with the formula
#### $$\frac{\nabla f_{P}}{||\nabla f_{P}||} = \frac{\langle 1, -1, -3 \rangle}{\sqrt{ 11 }} = \left\langle \frac{1}{\sqrt{ 11 }}, -\frac{1}{\sqrt{ 11 }}, -\frac{3}{\sqrt{ 11 }} \right\rangle$$
$||\nabla f_{P}||$ is the maximum rate of increase of $f$ at $P$. 

#### Interpretation of the Directional Derivative
When $D_{\vec{u}}(f) < 0$, this means the slope is "downhill" in the direction of $\vec{u}$. When $D_{\vec{u}}(f) > 0$, the slope is "uphill" in the direction of $\vec{u}$. 

#### Example
For a function $f(x, y) = e^{xy - y^{2}}$ with a vector $\vec{v} = \langle 12, -5 \rangle$ at the point $P(2, 2)$, the directional derivative is calculated like
#### $$\begin{cases}
\vec{u} = \vec{e}_{\vec{v}} = \frac{1}{||\vec{v}||}\vec{v} = \frac{1}{\sqrt{ 12^{2} + (-5)^{2} }} \langle 12, -5 \rangle = \langle \frac{12}{13}, -\frac{5}{13} \rangle \\
\nabla f = \langle f_{x}(x, y), f_{y}(x, y) \rangle = \langle e^{xy - y^{2}}y, e^{xy - y^{2}}(x - 2y) \rangle \\
\nabla f(2, 2) = \langle e^{4 - 4}(2), e^{4 - 4}(2 - 4) \rangle = \langle 2, -2 \rangle
\end{cases}$$
#### $$D_{\vec{u}}f(2, 2) = \langle 2, -2 \rangle \cdot \left\langle  \frac{12}{13}, -\frac{5}{13}  \right\rangle = \frac{24}{13} + \frac{10}{13} = \frac{34}{13}$$

## 14.6 Multivariable Calculus Chain Rules
#### General Composite Functions
Composite functions are functions that are composed of differentiable functions, who themselves could also be multivariable systems. So for a function $f(x, y)$, $x = x(s, t)$ and $y = y(s, t)$ would require the use of the chain rule for paths as mentioned earlier. The basic formula looks like 
#### $$\begin{cases}
\frac{\partial f}{\partial s} = \frac{\partial f}{\partial x} \frac{\partial x}{\partial s} + \frac{\partial f}{\partial y} \frac{\partial y}{\partial s} \\
\frac{\partial f}{\partial t} = \frac{\partial f}{\partial x} \frac{\partial x}{\partial t} + \frac{\partial f}{\partial y} \frac{\partial y}{\partial t}
\end{cases}$$
If we let $\vec{r}(s, t) = \langle x(s, t), y(s, t) \rangle$, then the derivation method used for directional derivatives would work. 

#### Implicit Differentiation
Implicit differentiation involves creating a function of n + 1 variables, where n is the number of original variables. So the function would be $F(x, y, z(x, y)) = 0$ where $z$ is implicitly defined as a differentiable function of $x$ and $y$. 

#### Example
For a function $f(x, y, z(x, y)) = x^{3} + y^{3} + z^{3} + 6xyz = 1$, find $\frac{\partial z}{\partial x}$ and $\frac{\partial z}{\partial y}$. 
#### $$\begin{cases}
f_{x} = 3x^{2} + 6yz \\
f_{y} = 3y^{2} + 6xz \\
f_{z} = 3z^{2} + 6xy
\end{cases}$$
With these partial derivatives, the implicit derivatives are
#### $$\begin{cases}
Z_{x} = \frac{\partial z}{\partial x} = -\frac{F_{x}}{F_{z}} = - \frac{3x^{2} + 6y^{2}}{3z^{2} + 6xy} \\
Z_{y} = \frac{\partial z}{\partial y} = - \frac{F_{y}}{F_{z}} = - \frac{3y^{2} + 6xz}{3z^{2} + 6xy}
\end{cases}$$

## 14.7 Optimization in Several Variables
#### Critical Points
A critical point is where a function could have a local extrema, thought it is not guaranteed. That's where the second derivative test and the discriminant comes into play. 