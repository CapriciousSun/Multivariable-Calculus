20250113113806

Tags:

A directional derivative is defined in the direction of the unit vector's limit. 

## Equation
```ad-formula
#### Formula for a Direction Vector
$$D_{\vec{u}}f(x, y) = \lim_{t \rightarrow 0} \frac{f(x + ht, y + kt) - f(x, y)}{t}$$
```

In practice, the [[Chain Rule for Paths|chain rule for paths]] could be used here. For a line through $(a, b)$ in the direction of a unit vector $\vec{u} = \langle h, k \rangle : \vec{r}(t) = \langle a, b \rangle + t\vec{u} = \langle a + ht, b + kt \rangle$. In interpretation, the directional derivative is the slope of $f$ in the direction of $\vec{u}$. Thus, if the directional derivative is less than 0, then it is going downhill in the direction of $\vec{u}$, whereas a positive directional derivative is going uphill. 
```ad-formula
#### Directional Derivative with Chain Rule for Paths
The directional derivative of $z = f(x, y)$ at $(a, b)$ in the direction of the unit vector $\vec{u}$ is 
#### $$D_{\vec{u}}f(a, b) = \frac{d}{dt}f(\vec{r}(t))|_{t = 0} = \nabla f(a, b) \cdot \vec{u}$$
where $\vec{r}(t) = \langle a, b \rangle + t\vec{u}$, assuming $f$ is differentiable.
```

```ad-example
#### Find the directional derivative of $f(x, y) = e^{xy - y^{2}}$ in the direction of $\vec{v} = \langle 12, -5 \rangle$ at the point $P(2, 2)$. 
The unit vector in the direction of $\vec{v}$ is 
$$\vec{u} = \vec{e}_{\vec{v}} = \frac{1}{||\vec{v}||}\vec{v} = \frac{1}{12^{2} + (-5)^{2}}\langle 12, -5 \rangle = \langle \frac{12}{13}, \frac{-5}{13} \rangle$$
$$\nabla f = \langle f_{x}(x, y), f_{y}(x, y) \rangle$$
$$f_{x}(x, y) = e^{xy - y^{2}}(y)$$
$$f_{y}(x, y) = e^{xy - y^{2}}(x - 2y)$$
$$\nabla f(2, 2) = \langle 2, -2 \rangle$$
Answer
#### $$D_{\vec{u}}f(2, 2) = \langle 2, -2 \rangle \cdot \langle \frac{12}{13}, \frac{-5}{13} \rangle = \frac{34}{13}$$
```

```ad-example
#### Find the directional derivative of $f(x, y, z) = x^{2} + 3y^{3}z$ in the direction $\vec{v} = \langle 1, -2, 2 \rangle$ at the point $P(2, 1, 3)$
$$\nabla f = \langle 2x, 9y^{2}z, 3y^{3} \rangle$$
$$\vec{u} = \vec{e}_{\vec{v}} = \frac{\vec{v}}{||\vec{v}||} = \frac{\langle 1, -2, 2 \rangle}{\sqrt{1^{2} + (-2)^{2} + 2^{2}}} = \left\langle \frac{1}{3}, \frac{-2}{3}, \frac{2}{3} \right\rangle$$
$$\nabla f_{p} = \nabla f(2, 1, 3) = \langle 2(2), 9(1)^{2}(3), 3(1)^{3} \rangle = \langle 4, 27, 3 \rangle$$
$$D_{\vec{u}}f(p) = \nabla f_{p} \cdot \vec{u} = \langle 4, 27, 3 \rangle \cdot \left\langle \frac{1}{3}, -\frac{2}{3}, \frac{2}{3} \right\rangle$$
```

## Directionality
If asked what direction the rate of change is the largest, the angle between two unit vectors are key to determining rate of change. 
```ad-formula
#### Directional Derivative Rate of Change
#### $$D_{\vec{u}}f(p) = \nabla f_{p} \cdot \vec{u} = ||\nabla f_{p}||\ ||\vec{u}||cos(θ) = ||\nabla f_{p}||cos(θ)$$
#### $$\therefore\ \ \ \underbrace{-||\nabla f_{p}||}_{θ = π,\ cos(π) = -1} ≤ D_{\vec{u}}f(p) ≤ \underbrace{||\nabla f_{p}||}_{θ = 0,\ cos(0) = 1}$$
```
In essence, $\nabla f_{p}$ points in the directional of the fastest rate of increase of $f$ at $P$, and is thd direction of the steepest ascent. $-\nabla f_{p}$ points in the direction of the fastest rate of decrease of $f$ at $P$, the direction of steepest descent. $\nabla f_{p}$ is normal to the level curve (level surface) of $f$ at $P$. 

```ad-example
#### Given $f(x, y, z) = x + \frac{y}{z}$ and point $P(4, 3, -1)$
###### Find the maximum rate of increase of $f$ and $P$
$$f(x, y, z) = x + y \times \frac{1}{z} = x + y \times z^{-1}$$
$$\nabla f = \left\langle 1, \frac{1}{2}, -yz^{-z} \right\rangle = \left\langle 1, \frac{1}{2}, -\frac{y}{z^{z}} \right\rangle$$
$$\nabla f_{p} = \nabla f(4, 3, -1) = \langle 1, -1, -3 \rangle$$
$$||\nabla f_{p}|| = \sqrt{1^{2} + (-1)^{2} + (-3)^{2}} = \sqrt{1 + 1+ 9} = \sqrt{11}$$
The maximum rate of increase of $f$ at $P$ is $\sqrt{11}$
###### Find a unit vecotr in the direction of the maximum rate of increase (steepest ascent) at $P$
$$\frac{\nabla f_{p}}{||\nabla f_{p}||} = \frac{\langle 1, -1, -3 \rangle}{\sqrt{11}} = \left\langle$$
```


___
