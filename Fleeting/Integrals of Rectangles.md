20250120103415

Tags

For a [[Functions|function]] of two variables, an integral for two variables is a double integral.

## Notation
A double integral typically looks like
```ad-formula
#### Double Integral
#### $$\int \int_{D} f(x, y)dA$$
```
where represents the signed volume of a solid region between the [[Graphs|graph]] of $Z = f(x, y)$ and the region $D$ in the xy-plane. 
## Definition
The volume of a solid could be approximated using the Reimann's Sum, calculated by the area of the base and the height to reach the graph surface.
```ad-formula
#### Riemann's Sum for Volume
#### $$S_{N, M} = \sum _{i = 1}^{N}\sum_{j = 1}^{M}f(P_{ij})ΔA_{ij}$$
```

For any given partition $P$ and sampling, this sum gives an approximation of the integral. Hence, the definition of the double integral of $f(x, y)$ over a rectangle $R$ is
```ad-formula
#### Double Integral of a Rectangle
#### $$\int \int_{R}f(x, y)dA = \lim_{ ||P|| \to 0 }\sum_{i = 1}^{N}\sum_{j = 1}^{M}f(P_{ij})ΔA_{ij}$$
```

If this limit exists, one can say that $f$ is integrable over $R$. The theorem goes, that if a function $f$ comprised of two variables is continuous on a rectangle $R$, then $f(x, y)$ is integrable over $R$. 
```ad-formula
#### Linearity of the Double Integrals
Assuming that $f(x, y)$ and $g(x, y)$ are integrable, then 
#### $$\int \int_{R}(f(x, y) + g(x, y))dA = \int \int_{R}f(x, y)dA + \int \int_{R}g(x, y)dA$$
```

So for any constant $C$, then that can be factored out from like 
```ad-formula
#### Constants
#### $$\int \int_{R}Cf(x, y)dA = C\int \int_{R}f(x, y)dA$$
```

## Iterated Integrals
The first kind of integral to remember are iterated integrals. Iterated integrals have a function $f$ comprised of 2 variables that is integrable on $R = [a, b] \times [c, d]$, where $a$, $b$, $c$, and $d$ are the bounds of the function. 
```ad-formula
#### Iterated Integrals Formula
To compute $\int_{c}^{d}f(x, y)dy$, fix $x$ and integrate with respect to $y$ on $[c, d]$. This is called a partial anti-differentiation with respect to $y$. This gives a function of $x$ $S(x) = \int_{c}^{d}f(x, y)dy,$ which can then be plugged into the double integral.
#### $$\int_{a}^{b}S(x)dx = \int_{a}^{b}\left( \int_{c}^{d}f(x, y)dy \right)dx$$
Alternatively, for an $S(X) = \int_{a}^{b}f(x, y)dx$
#### $$\int_{c}^{d} S(x)dy = \int_{c}^{d}\left( \int_{a}^{b}f(x, y)dx \right)dy$$
```

## Fubini's Theorem
Fubini's theorem, on the other hand, states that the double integral of a continuous function $f(x, y)$ over a rectangle $R = [a, b] \times [c, d]$ is equal to the iterated integral in any order, similar to what was demonstrated earlier. 
```ad-formula
#### Fubini's Theorem
#### $$\int \int_{R} f(x, y)dA = \int_{x = a}^{b} \int_{y = c}^{d} f(x, y)dy\ dx = \int_{y = c}^{d} \int_{x = a}^{b} f(x, y)dx\ dy$$
```

#### Example
Evaluate the following function $$\int_{0}^{3}\int_{1}^{2}x^{2}y\ dy\ dx$$
The $R$ here is $$\begin{cases}
0 ≤ x ≤ 3 \\
1 ≤ y ≤ 2
\end{cases}$$
So $R = [0, 3] \times [1, 2]$. $$\int_{1}^{2}\int_{0}^{3}x^{2}y\ dx\ dy = \int_{0}^{3} \left.\frac{1}{2}x^{2}y^{2}\right\vert_{y = 1}^{y = 2}dx = \int_{0}^{3}\left( \frac{1}{2}x^{2}2^{2} - \frac{1}{2}x^{2}1^{2}\right)dx = \int_{0}^{3} \frac{3}{2}x^{2}dx = \frac{1}{2}\left. \frac{3}{2}x^{3}\right\vert_{x = 0}^{x = 3}$$
$$\frac{27}{2} - 0 = \frac{27}{2}$$
Checking that reversing the order of integration will give the same result $$\int_{1}^{2}\int_{0}^{3}x^{2}y\ dx\ dy = \int_{1}^{2}\left. \frac{1}{3}x^{3}y\right\vert_{x = 0}^{x = 3}dy = \int_{1}^{2}9y\ dy = \left. \frac{9}{2}y^{2}\right\vert_{y = 1}^{y = 2} = \left( \frac{9}{2}2^{2} - \frac{9}{2}1^{2} \right) = \frac{9}{2}(4 - 1) = \frac{27}{2}$$

#### Example
$$\int \int_{R}y\sin(xy)dA,\ \ R = [1, 2] \times \left[ 0, \frac{π}{2} \right]$$
$$\int_{0}^{\frac{p}{2}}\int_{1}^{2}y\sin(xy)dx\ dy = \int_{0}^{\frac{π}{2}}\left.y * -\frac{1}{y}\cos(xy)\right\vert_{x = 1}^{x = 2}dy = \int_{0}^{\frac{π}{2}}(-\cos(2y) + \cos(y))dy $$
$$\left. \left( -\frac{1}{2}\sin(2y) + \sin(y) \right)\right\vert_{y = 0}^{y = \frac{π}{2}} = \left( -\frac{1}{2}\sin(π) + \sin\left( \frac{π}{2} \right) \right) - \left( -\frac{1}{2}\sin(0) + \sin(0) \right) = 1$$


#### Example
Evaluate $\int \int_{R}-5dA$ where $R = [2, 5] \times [4, 7]$. The integral for this would look like $$\begin{gather*}
-5 \int_{2}^{5}\int_{4}^{7}dx\ dy = -5 \cdot \text{Area}(R) = -5 * 3 * 3 = -45
\end{gather*}$$

#### Example
Evaluate $\int_{0}^{2}\int_{1}^{3}x^{3}ydx\ dy$  $$\begin{gather*}
\int_{0}^{2} \left. \frac{x^{4}}{4}\right\vert_{1}^{3}dy = \int_{0}^{2}20dy = 40
\end{gather*}$$

#### Example
Evaluate $\int_{0}^{\frac{π}{4}}\int_{\frac{π}{4}}^{\frac{π}{2}}\cos(2x + y)dy\ dx$ $$\begin{gather*}
\int_{0}^{\frac{π}{4}}\left.\sin(2x + y)\right\vert_{\frac{π}{4}}^{\frac{π}{2}}dx = \int_{0}^{\frac{π}{4}}\sin\left( 2x + \frac{π}{2} \right) - \sin\left( 2x + \frac{π}{4} \right)dx = \\
\frac{1}{2}\left.\left[ -\cos\left( 2x + \frac{π}{2}\right) + \cos\left( 2x + \frac{π}{4} \right) \right]\right\vert_{0}^{\frac{π}{4}} = \frac{1 - \sqrt{ 2 }}{2}
\end{gather*}$$

#### Example
Evaluate $\int_{1}^{2}\int_{2}^{4}e^{3x - y}dy\ dx$ $$\begin{gather*}
\int_{1}^{2}e^{3x}dx \int_{2}^{4}e^{-y}dy = \left.\left( \frac{e^{3x}}{3}\right\vert_{1}^{2} \right)(\left.-e^{-y}\right\vert_{2}^{4}) = \frac{1}{3}(e^{6} - e^{3})(e^{-2} - e^{-4})
\end{gather*}$$

#### Example
Integrate $f(x, y) = x$ over the region bounded by $y = x^{2}$ and $y = x + 2$ $$\begin{cases}
-1 ≤ x ≤ 2 \\
x^{2} ≤ y ≤ x + 2
\end{cases}$$
$$\int_{-1}^{2}\int_{x^{2}}^{x + 2}xdy\ dx = \int_{-1}^{2}\left.xy\right\vert_{x^{2}}^{x + 2}dx = \int_{-1}^{2}$$



#### Example
$$\int_{0}^{2}\int_{1}^{2} \frac{x}{\sqrt{ x^{2} + y }}dx\ dy$$
Using substitution, we swap out $x^{2} + y$ $$\begin{equation}
u = x^{2} + y \implies du = 2xdx \implies \frac{1}{2}du = xdx
\end{equation}$$
$$\frac{1}{2} \int_{0}^{2} \frac{du}{\sqrt{ u }} dy = \int_{0}^{8}\left. (x^{2} + y)^{\frac{1}{2}}\right\vert_{x = 1}^{x = 2}dy = \int_{0}^{8}\left[ (4 + y)^{\frac{1}{2}} - (1 + y)^{\frac{1}{2}} \right]dy = \left. \left[ \frac{2}{3}(4 + y)^{\frac{3}{2}} - \frac{2}{3}(1 + y)^{\frac{3}{2}} \right]\right\vert_{y = 0}^{y = 8}$$
$$\left( \frac{2}{3}(12)^{\frac{3}{2}} - \frac{2}{3}(9)^{3\frac{3}{2}} \right) - \left( \frac{2}{3}(4)^{\frac{3}{2}} - \frac{2}{3}(1)^{\frac{3}{2}} \right) = \frac{2}{3}[(2\sqrt{ 3 })^{3} - 27 - 8 + 1] = 16\sqrt{ 3 } - \frac{68}{3}$$
___
# References
[[MATH2010_15.1_15.2.pdf]]
