20250223124713

Tags:

A triple integral is solved in pretty much the same way as a double integral, with many of the same rules applying

## Fubini's Theorem for Triple Integrals
The triple integral of a function $f(x, y, z)$ over a box $B = [a, b] \times [c, d] \times [p, q]$ calculated with an iterated integral.
```ad-formula
#### Iterated Integral of a Box
#### $$\int \int \int_{B} f(x, y, z)dV = \int_{x = a}^{b} \int_{y = c}^{d} \int_{z = p}^{q} f(x, y, z) dz\ dy\ dx $$
As with any iterated integral, it can be evaluated in any order. 
![[Pasted image 20250224125840.png|400]]
```

## Continuous Function
A triple integral can also be seen as the volume of an object stuck between two functions. This creates three definitions for a triple integral; x-simple, y-simple, and z-simple.
```ad-formula
#### X-Simple Triple Integral
The region $D$ is defined as the $yz$-plane and integrated over the $x$-axis.
#### $$\int \int \int_{W} f(x, y, z)dV = \int \int_{D} \left( \int_{x = x_{1}(y, z)}^{x = x_{2}(y, z)}f(x, y, z)dx \right)dA $$
![[Pasted image 20250224131254.png|400]]
```

```ad-formula
#### Y-Simple Triple Integral
The region $D$ is defined as the $xz$-plane integrated over the $y$-axis
#### $$\int \int \int_{W} f(x, y, z)dV = \int \int_{D} \left( \int_{y = y_{1}(x, z)}^{y = y_{2}(x, z)} f(x, y, z)dy \right)dA $$
```

```ad-formula
#### Z-Simple Triple Integral
The region $D$ is defined as the $xy$-plane integrated over the $z$-axis
#### $$\int \int \int_{W} f(x, y, z)dV = \int \int_{D} \left( \int_{z = z_{1}(x, y)}^{z = z_{2}(x, y)} f(x, y, z)dz \right)dA $$
![[Pasted image 20250224131628.png|400]]
```

___
# References
[[MATH2010_15.4_14.3.pdf]]
[[MATH2010_15.3_16.1_16.2.pdf]]
