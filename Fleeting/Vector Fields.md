20250210105357

Tags:

A vector field is a collection of vectors which change magnitude and direction based on position

## Definition
For a domain $D$, the vector field is a subset of the dimensions in the field.
```ad-formula
#### 2-Dimensional Vector Field
For a $D$ that is a subset of $\mathbb{R}^{2}$, a vector field in said $\mathbb{R}^{2}$ is a function $\vec{F}$ that assigns to each point $(x, y)$ in $D$. We can write said function as 
#### $$\vec{F}(x, y) = \langle F_{1}(x, y), F_{2}(x, y) \rangle = F_{1}(x, y)\hat{i} + F_{2}(x, y)\hat{j}$$
```

```ad-formula
#### 3-Dimensional Vector Field
Likewise, for a vector field $\mathbb{R}^{3}$
#### $$\vec{F}(x, y, z) = \langle F_{1}(x, y, z), F_{2}(x, y, z), F_{3}(x, y, z) \rangle = F_{1}(x, y, z)\hat{i} + F_{2}(x, y, z)\hat{j} + F_{3}(x, y, z)\hat{k} $$
```

In essence, every point in the domain is assigned a vector. 

```ad-example
#### Example
What is the graph of a vector field $\vec{F}(x, y) = \langle -y, x \rangle$
#### $$\vec{F}(1, 0) = \langle 0, 1 \rangle$$
#### $$\vec{F}(2, 2) = \langle -2, 2 \rangle$$
#### $$\vec{F}(0, 2) = \langle -2, 0 \rangle$$
```

## Conservation
A vector field $\vec{F}$ is called the conservative if it is equal to the [[Gradients|gradient]] of some scalar function $f$, which is called the potential function of $\vec{F}$. For a scalar function $f(x, y, z), \nabla f = \langle \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}, \frac{\partial f}{\partial z} \rangle$ is the gradient vector field. If a conservative vector field is the gradient of a potential function, then it is orthogonal to the potential function's level curves. 
For a curve $C$ that's closed, the line integral of any vector field $\vec{F}$ around $C$ is a circulation of $\vec{F}$ around $C$.
```ad-formula
#### Circulation Line Integral
For a circular integral of $F$ around $C$, it's notation is
#### $$\oint_{C} \vec{F} \cdot d\vec{r}$$
```

Furthermore, for a conservative vector field $\vec{F}$, $C$ can be parameterized by $\vec{r}(t)$. 
```ad-formula
#### Conservative Vector Field
With bounds $a ≤ t ≤ b$, where points $P = \vec{r}(a)$ and $Q = \vec{r}(b)$, the conservative vector field can be be defined by the gradient of some scalar function $f$
#### $$\int_{C} \vec{F} \cdot d\vec{r} = \int_{a}^{b} \vec{F}(\vec{r}(t)) \cdot \vec{r}'(t)dt = \int_{a}^{b} \nabla f(\vec{r}(t)) \cdot \vec{r}'(t)dt = \int_{a}^{b} \frac{d}{dt} [f(\vec{r}(t))]dt = \left. f(\vec{r}(t)) \right\vert_{t = a}^{t = b} = f(\vec{r}(b)) - f(\vec{r}(a)) = f(Q) - f(P) $$
The conclusion is that, for a conservative vector field, the line integral over said vector field depends only on the points $P$ and $Q$, not the actual path that the points take. 
```

Closed paths within a conservative vector field follow similar rules.
```ad-formula
#### Conservative Vector Loops
In a field where $C$ is a closed loop, or $P$ = $Q$, if the general rule for the line integral is followed, then
#### $$\oint_{C} \vec{F} \cdot d\vec{r} = \int_{C} \vec{F} \cdot d\vec{r} = 0$$
```

## Operations
In order to find out if a vector field is conservative or not, new operations on vector fields needs to be defined. They are all based on the gradient operator $\nabla = \langle \frac{\partial}{\partial x}, \frac{\partial}{\partial y}, \frac{\partial}{\partial z} \rangle$. 
```ad-formula
#### Divergence
Divergence describes the tendency for vectors to point towards or point away from a single point, creating sinks or sources. It is defined as 
#### $$div(\vec{F}) = \nabla \cdot \vec{F} = \left\langle \frac{\partial}{\partial x}, \frac{\partial}{\partial y}, \frac{\partial}{\partial z} \right\rangle \cdot \langle F_{1}, F_{2}, F_{3} \rangle = \frac{\partial F_{1}}{\partial x} + \frac{\partial F_{2}}{\partial y} + \frac{\partial F_{3}}{\partial z}$$
The divergence of a vector field at a particular point describes how much the vectors are sourcing or sinking at that point.
```

```ad-formula
#### Curl
Curl describes the magnitude and the axis of rotation for vectors. It is defined as 
#### $$\begin{gather} curl(\vec{F}) = \nabla \times \vec{F} = \begin{vmatrix} \hat{i} & \hat{j} & \hat{k} \\ \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\ F_{1} & F_{2} & F_{3} \end{vmatrix} = \left( \frac{\partial F_{3}}{\partial y} - \frac{\partial F_{2}}{\partial z} \right)\hat{i} - \left( \frac{\partial F_{3}}{\partial x} - \frac{\partial F_{1}}{\partial z} \right)\hat{j} + \left( \frac{\partial F_{2}}{\partial x} - \frac{\partial F_{1}}{\partial y} \right)\hat{k} = \\ \left\langle \frac{\partial F_{3}}{\partial y} - \frac{\partial F_{2}}{\partial z}, \frac{\partial F_{1}}{\partial z} - \frac{\partial F_{3}}{\partial x}, \frac{\partial F_{2}}{\partial x} - \frac{\partial F_{1}}{\partial y} \right\rangle \end{gather}$$
The curl of a vector field at a particular point describes the immediate rotation that the point would have, with a positive curl corresponding to a clockwise rotation and a negative curl corresponding to a counter-clockwise rotation. 
```

The inputs and outputs of each operation should be noted as well.

|                   | Operation  | Input                  | Output          |
| ----------------- | ---------- | ---------------------- | --------------- |
| $\nabla f$        | Gradient   | Scalar function $f$    | Vector field    |
| $\nabla \cdot f$  | Divergence | Vector field $\vec{F}$ | Scalar function |
| $\nabla \times f$ | Curl       | Vector field $\vec{F}$ | Vector field    |
Curl is used to find the conservation of a vector field.
```ad-formula
#### Curl of a Conservative Vector Field
In $\mathbb{R}^{2}$, if the vector field $\vec{F} = \langle F_{1}, F_{2} \rangle$ is conservative, then 
#### $$\frac{\partial F_{1}}{\partial y} = \frac{\partial F_{2}}{\partial x} $$
In $\mathbb{R}^{3}$, if the vector field $\vec{F} = \langle F_{1}, F_{2}, F_{3} \rangle$ is conservative, then 
#### $$\text{curl}(\vec{F}) = 0 = \frac{\partial F_{1}}{\partial y} = \frac{\partial F_{2}}{\partial z}, \frac{\partial F_{2}}{\partial z} = \frac{\partial F_{3}}{\partial y}, \frac{\partial F_{3}}{\partial x} = \frac{\partial F_{1}}{\partial z}$$
```

```ad-example
#### Example
Let $\vec{F} = \langle xz, xyz, -y^{2} \rangle$, calculate $\text{div}(\vec{F})$ and $\text{curl}(\vec{F})$.
Divergence is calculated as 
#### $$\text{div}(\vec{F}) = \nabla \cdot \vec{F} = \frac{\partial}{\partial x}(xz) + \frac{\partial}{\partial y}(xyz) + \frac{\partial}{\partial z}(-y^{2}) = z + xz + 0 = z + xz$$
Curl is calculated as 
#### $$\begin{gather}\text{curl}(\vec{F}) = \nabla \times \vec{F} = \begin{vmatrix} \hat{i} & \hat{j} & \hat{k} \\ \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\ xz & xyz & -y^{2} \end{vmatrix} = \left( \frac{\partial}{\partial y}(-y^{2}) - \frac{\partial}{\partial z}(xyz) \right)\hat{i} - \left( \frac{\partial}{\partial x}(-y^{2}) - \frac{\partial}{\partial z}(xz) \right)\hat{j} + \left( \frac{\partial}{\partial x}(xyz) - \frac{\partial}{\partial y}(xz) \right)\hat{k} \\ = (-2y - xy)\hat{i} - (0 - x)\hat{j} + (yz - 0)\hat{k} = \langle -2y - xy, x, yz \rangle \end{gather}$$
```

```ad-example
#### Example
Show that $\vec{F} = \langle y, z, x \rangle$ is not conservative
#### $$\begin{gather}curl(\vec{F}) = \nabla \times \vec{F} = \begin{vmatrix} \hat{i} & \hat{j} & \hat{k} \\ \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\ y & z & x \end{vmatrix} = (0 - 1)\hat{i} - (1 - 0)\hat{j} + (0 - 1)\hat{k} \\ = \langle -1, -1, -1 \rangle ≠ 0 \end{gather}$$
```

___
# References
[[MATH2010_15.3_16.1_16.2.pdf]]
[[MATH2010_16.3_17.1.pdf]]
