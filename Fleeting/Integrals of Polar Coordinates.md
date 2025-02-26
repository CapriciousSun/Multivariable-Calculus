20250223131422

Tags:

Polar coordinates are expressed in terms of $r$, the magnitude of the circle, and $θ$, the angle of the circle. From this, they are expressed as either a system of $\sin$ and $\cos$ functions with the coefficient of $r$ or $\tan$ with the coefficient of $r$, where $r$ is $\sqrt{ x^{2} + y^2 }$. Arc lengths also play a role, where for an arc length $β$, it is defined $θr$. 

## Definition
Polar coordinates are defined by a function $f$ on a polar rectangle.
```ad-formula
#### Polar Coordinate Integration
The region for polar integration is defined with boundaries
#### $$R: \begin{cases}θ_{1} ≤ θ ≤ θ_{2} \\ r_{1} ≤ r ≤ r_{2}\end{cases}$$
Therefore, the integral is 
#### $$\int \int_{R} f(x, y)dA = \int_{θ_{1}}^{θ_{2}} \int_{r_{1}}^{r_{2}} f(r\cos(θ_{1}), r\sin(θ_{2}))r dr\ dθ$$
It should be noted the [[Integrals of Rectangles#Fubini's Theorem|Fubini's theorem]] applies here.
```

## Radially Simple Regions
Radially simple regions are domains where a line drawn from $r_{1}(θ)$ always ends up at $r_{2}(θ)$. 
```ad-formula
#### Integration of a Radially Simple Region
For a continuous function $f$ on the radially simple domain $D: \begin{cases} θ_{1} ≤ θ ≤ θ_{2} \\ r_{1}(θ) ≤ r ≤ r_{2}(θ) \end{cases}$
#### $$\int \int_{D} f(x, y)dA = \int_{θ_{1}}^{θ_{2}} \int_{r_{1}(θ_{1})}^{r_{2}(θ_{1})} f(r\cos(θ), rsin(θ))r dr\ dθ $$
![[Pasted image 20250223220118.png|400]]
```
___
# References
[[MATH2010_15.4_14.3.pdf]]
