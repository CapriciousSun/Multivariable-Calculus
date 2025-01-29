20250123103315

Tags:

## Maxima/Minima
The definition of the absolute (global) maximum is that it exists where $f(x, y) ≤ f(a, b)$ for all $x, y$ in the domain of $f$. The local maximum exists if $f(x, y) ≤ f(a, b)$ for all $(a, b)$ in some open disk centered at $(a, b)$. Said open disk is a projection that's parallel to the plane of discussion. 
![[Pasted image 20250123103837.png|300]]
The disk $D(P, r)$ for a unit vector $\vec{u}$ has slope $D_{\vec{u}}f(p) = 0$.  Hence, the gradient is $\nabla f(p) \cdot \vec{u} = 0$ for all $\vec{u}$. Therefore, $\nabla f(p) = \vec{0}$. 

## Several Variables
For a multivariable system, a point $P = (a, b)$ in the domain of $f(x, y)$ is a critical point of $f$ if either $f_{x}p = f_{y}(p) = 0$ or both points do not exist. 

## Fermat's Theorem
Fermat's Theorem stipulates that if $f(x, y)$ has a local maximum or local minimum at $P = (a, b)$, then $(a, b)$ is a critical point of $f(x, y)$. However, the inverse may not be true. Just because $(a, b)$ is a critical point doesn't mean that $f$ has a local maximum or minimum at $(a, b)$. Examples of this includes saddle points, where the graph curves downwards at the point $(a, b)$, since it's a local max in the x-direction and a local minimum in the y-direction, hence there's no overall local extermum. .
![[Pasted image 20250123110300.png|300]]
If $f_{x}(a, b) = 0 = f_{y}(a, b)$, then $\nabla f(a, b) = \vec{0}$ and the [[Tangents#Tangent Plane|tangent plane]] at $f$ at $(a, b)$ is $$z = f(a, b) + f_{x}(a, b)(x - a) + f_{y}(a, b)(y - b) \implies z = f(a, b)$$
```ad-example
#### Find all critical points of $f(x, y) = xe^{-x^{2} - y^{2}}$
$$f_{x} = e^{x^{2} - y^{2}} + xe^{-x^{2} - y^{2}}(-2x) = (1 - 2x^{2})e^{-x^{2} - y^{2}}$$
$$f_{y} = xe^{-x^{2} - y^{2}}(-2y) = -2xye^{-x^{2} - y^{2}}$$
Here $f_{x}$ and $f_{y}$ are defined for all $x$ and $y$. Hence, the only critical points will be when they are equal to 0. 
$$f_{x} = 0: (1 - 2x^{2})\underbrace{e^{-x^{2} - y^{2}}}_{\text{Never zero}} = 0 \implies 1 - 2x^{2} = 0 \implies x = \pm \frac{1}{\sqrt{2}}$$
$$f_{y} = 0: -2xy\underbrace{e^{-x^{2} - y^{2}}}_{\text{Never zero}} = 0 \implies -2xy = 0 \implies xy = 0 \implies y = 0$$
For $f_{y}$, $x$ could never be 0, so $x ≠ 0$ for $f_{y}$. 

Answer
#### So the only critical points that exist is $(\frac{1}{\sqrt{2}}, 0)$ and $(-\frac{1}{\sqrt{2}}, 0)$
```

## Second Derivative Test
The second derivative test is used to classify $f$ for each critical point $(a, b)$. It relies on the sign of the discriminant $D$ evaluated at the critical point $(a, b)$. If $f(x, y)$ is a twice-differentiable function, the discriminant is defined as 
```ad-formula
#### Second Derivative Test Formula
#### $$Det(x, y) = \begin{vmatrix} f_{xx} & f_{xy} \\ f_{yx} & f_{yy} \end{vmatrix} = f_{xx}f_{yy} - f_{xy}f_{yz} = f_{xx}f_{yy} - (f_{xy})^{2}$$
```

The second derivative test, in turn, assumes that $f_{xx}$, $f_{yy}$, and $f_{xy}$ are continuous near $P = (a, b)$. Then, several rules apply.
1) If $D(a, b) > 0$ and $f_{xx}(a, b) > 0$, then $f(a, b)$ is a local minimum
2) If $D(a, b) > 0$ and $f_{xx}(a, b) < 0$, then $f(a, b)$ is a local maximum
3) If $D(a, b) < 0$, then $f$ has a saddle point at $(a, b)$
4) If $D(a, b) = 0$, the test is inconclusive. 

| Sign of $Det(a, b)$ | Sign of $f_{xx}(a, b)$ | Type of critical point |
| :-----------------: | :--------------------: | :--------------------: |
|          +          |           +            |    Local min $\cup$    |
|          +          |           -            |    Local max $\cap$    |
|          -          |         (Any)          |         Saddle         |
|          0          |         (Any)          |      Inconclusive      |
If $D(a, b) > 0$, then $f_{xx}(a,b)$ and $f_{yy}(a, b)$ must have the same sign. Hence the sign of $f_{yy}(a, b)$ determines whether if $f(a, b)$ is a local minimum or a local maximum when $D(a, b) > 0$. $$D(a, b) > 0: f_{xx}(a, b)f_{yy}(a, b) - [f_{xy}(a, b)]^{2} > 0\ \&\ f_{xx}(a, b)f_{yy}(a, b) > [f_{xy}(a, b)]^{2}$$
```ad-example
#### Apply the second derivative test to classify the criticalpoints of $f(x, y) = xe^{-x^{2} - y^{2}}$
Calculate $D(x, y)$, need to find $f_{xx}$, $f_{yy}$, and $f_{xy}$
$$f_{xx} = -4xe^{-x^{2} - y^{2}} + (1 - 2x^{2})(-2x)e^{-x^{2} - y^{2}} = (4x^{3} - 6x)e^{-x^{2} - y^{2}}$$
$$f_{xy} = (1 - 2x^{2})(-2y)e^{-x^{2} - y^{2}}$$
$$f_{yy} = -2xe^{-x^{2} - y^{2}} - 2xy(-2y)e^{-x^{2} - y^{2}} = -2x(1 - 2y^{2})e^{-x^{2} - y^{2}}$$
$$f_{xx}(P_{1}) = -\frac{4}{\sqrt{2}}e^{-\frac{1}{2}},\ f_{xy}(P_{1}) = 0,\ f_{yy}(P_{1}) = -\frac{2}{\sqrt{2}}e^{-\frac{1}{2}}$$
$$f_{xx}(P_{2}) = \frac{4}{\sqrt{2}}e^{-\frac{1}{2}},\ f_{xy}(P_{2}) = 0,\ f_{yy}(P_{2}) = \frac{2}{\sqrt{2}}e^{-\frac{1}{2}}$$
Applying the second derivatives test shows that
$$D(P_{1}) = \underbrace{f_{xx}(P_{1})}_{(-)}\underbrace{f_{yy}(P_{1})}_{(-)} - \underbrace{[f_{xy}(P_{1})]^{2}}_{0} > 0$$
$$- \cdot - = +$$
$\therefore$ there is a local max at $P_{1}$, the local max of $f(P_{1})$
$$D(P_{2}) = \underbrace{f_{xx}(P_{2})}_{(+)}\underbrace{f_{yy}(P_{2})}_{(+)} - \underbrace{[f_{xy}(P_{2})]}_{0} > 0$$
$$+ \cdot + = +$$
$\therefore$ there is a local min at $P_{2} = (-\frac{1}{\sqrt{2}}, 0) = 0$, the local minimum is $f(P_{2})$
```

```ad-example
#### Find and classify all critical points of $f(x, y) = 2x^{2} - 4xy + y^{3} + 2$
$$\begin{cases}
f_{x} = 4x - 4y  = 0\ \ (1)\\
f_{y} = -4x + 3y^{2} = 0\ \ (2)
\end{cases}$$
From (1): $4x - 4y = 0 \implies 4x = 4y \implies x = y$
By substituting this into (2): $-4y + 3y^{2} = 0 \implies y(-4 + 3y) = 0$
$\therefore\ \ y = 0,\ y = \frac{4}{3}$
Critical points: $(0, 0)$, $(\frac{4}{3}, \frac{4}{3})$
To classify, find $D(x, y)$: 
$$D(x, y) = f_{xx}f_{yy} - [f_{xy}]^{2} = \begin{vmatrix}
f_{xx} & f_{xy} \\
f_{yx} & f_{yy}
\end{vmatrix} = \begin{vmatrix}
4 & -4
-4 & 6y
\end{vmatrix} = 24y - 16$$
Applying the second derivative test gets 
$$D(0, 0) = 24(0) - 16 = -16 < 0$$
$$D(\frac{4}{3}, \frac{4}{3}) = 24(\frac{4}{3}) - 16 = 16 > 0$$

Answer
#### There is a saddle point at $(0, 0)$ and a local minimum at $(\frac{4}{3}, \frac{4}{3})$
```

## Existence and Location of the Global Extrema
Let there be a continuous function on a closed, bounded domain $D$ in $\mathbb{R}^{2}$. Then $f(x, y)$ takes on both a global maximum and a global minimum value on $D$ and the extrema occur at either the critical points in the interior of $D$ or at points on the boundary of $D$. In order to find the global extrema, 
```ad-example
#### Find the absolute max & min values of $f(x, y) = 3 + xy - x - 2y$ on the domain $D$ which is the closed region with vertices $(1, 0)$, $(5, 0)$, and $(1, 4)$
$$f_{x} = y - 1 = 0 \implies y = 1$$
$$f_{y} = x - 2 = 0 \implies x = 2$$
The critical point of this system is $(2, 1)$. 
$$f(2, 1) = 3 + 2 - 2 - 2 = 1$$
![[Pasted image 20250123114903.png|300]]
$$A: y = 0,\ 1 ≤ x ≤ 5 : f(x, 0) = 3 - x$$
is a decreasing function. Hence, the max is $f(1, 0) = 3 - 1 = 2$ and the min is $f(5, 0) = 3 - 5 = -2$
$$B: x = 1, 0 ≤ y ≤ 4 : f(1, y) = 3 + y - 1 - 2y = 2 - y$$
is a decreasing function. Hence, the max is $f(1, 0) = 2$ and the min is $f(1, 4) = 2 - 4 = -2$
$$y = 5 - x, 1 ≤ x ≤ 5 : f(x, 5 - x) = 3 + x(5 - x) - x - 2(5 - x) = -x^{2} + 6x - 7$$
Let $g(x) = -x^{2} + 6x - 7$, and the max and min values need to be found using it. $$g'(x) = -2x + 6 = 0 \implies x = 3$$
So $g(1) = -(1)^{2} + 6(1) - 7 = -2$, $g(3) = -(3)^{2} + 6(3) - 7 = 2$, $g(5) = -(5)^{2} + 6(5) - 7 = -2$
#### Answer
#### The max value of $f$ is $2$ and the min value is $-2$. 
```

___
# Reference
[[MATH2010_14.7_14.8.pdf]]

