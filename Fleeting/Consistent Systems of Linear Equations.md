20250310103231

Tags:

A system is consistent if it has one or more solutions to it. When it is consistent, then the reduced system should be looked at. 

## Formalism
```ad-formula
#### General Form of a Consistent Linear System
A system of linear equations is homogenous if $b_{1} = b_{2} = b_{m} = 0$. 
#### $$\begin{cases} a_{11}x_{1} + a_{12}x_{2} + \dots + a_{1n}x_{n} = 0 \\ a_{21}x_{1} + a_{22}x_{2} + \dots + a_{2n}x_{n} = 0 \\ \vdots \\ a_{m1}x_{1} + a_{m2}x_{2} + \dots + a_{mn}x_{n} = 0 \\ \end{cases} \implies \left[\begin{array}{c c c c | c} a_{11} & a_{12} & \dots & a_{1n} & 0 \\ a_{21} & a_{22} & \dots & a_{2n} & 0 \\ \vdots & \vdots & & \vdots & \vdots  \\ a_{m1} & a_{m2} & \dots & a_{mn} & 0 \end{array}\right] = [A|\vec{0}]$$
```

Every single homogenous system is consistent because $x_{1} = x_{2} = \dots = x_{n} = 0$ is always a solution. This is the *trivial solution*. Other solutions are called *non-trivial* solutions. If $m < n$, then the system will always have infinitely many solutions.
```ad-example
Find the solutions for the following system
#### $$ \begin{array}{} 2x_{1} + 3x_{2} - x_{3} = 0 \\ x_{1} - 5x_{2} - 2x_{3} = 0 \end{array} $$
In augmented matrix form
#### $$ \left[ \begin{array}{c c c | c} 2 & 3 & -1 & 0 \\ 1 & -5 & -2 & 0 \end{array} \right] $$
Swap row 1 and row 2, and subtract row 2 with 2 times of row 1
#### $$ \left[ \begin{array}{c c c | c} 1 & -5 & -2 & 0 \\ 0 & 13 & 3 & 0 \end{array} \right] $$
Factor row 2 by \frac{1}{13}
#### $$ \left[ \begin{array}{c c c | c} 1 & -5 & -2 & 0 \\ 0 & 1 & \frac{3}{13} & 0 \end{array} \right] $$
Add row 1 by 5 times of row 2
#### $$ \left[ \begin{array}{c c c | c} 1 & 0 & -\frac{11}{13} & 0 \\ 0 & 1 & \frac{3}{13} & 0 \end{array} \right] $$
The solutions of the system is
#### $$ \begin{array}{} x_{1} - \frac{11}{13}x_{3} = 0 \\ x_{2} + \frac{3}{13}x_{3} = 0 \end{array} \implies \begin{array}{} x_{1} = \frac{11}{13}x_{3} \\ x_{2} = -\frac{3}{13}x_{3} \\ x_{3} = x_{3} \end{array} $$
In vector form, the solution is
#### $$\vec{x} = \begin{bmatrix} x_{1} \\ x_{2} \\ x_{3} \end{bmatrix} = \begin{bmatrix} \frac{11}{13} \\ -\frac{3}{13} \\ 1 \end{bmatrix}$$
```

```ad-example
Find the solutions for the following system
#### $$ \begin{array}{} x_{1} + 2x_{2} + 3x_{3} = 0 \\ x_{2} + 2x_{3} = 0 \\ x_{1} + 3x_{3} = 0 \end{array} $$
Turn it into augmented matrix form
#### $$ \left[ \begin{array}{c c c | c} 1 & 2 & 3 & 0 \\ 0 & 1 & 2 & 0 \\ 1 & 0 & 3 & 0 \end{array} \right] $$
Subtract row 3 by row 1
#### $$ \left[ \begin{array}{c c c | c} 1 & 2 & 3 & 0 \\ 0 & 1 & 2 & 0 \\ 0 & -2 & 0 & 0 \end{array} \right] $$
Add row 3 by 2 times or row 2
#### $$ \left[ \begin{array}{c c c | c} 1 & 2 & 3 & 0 \\ 0 & 1 & 2 & 0 \\ 0 & 0 & 4 & 0 \end{array} \right] $$
Factor row 3 by $\frac{1}{4}$
#### $$ \left[ \begin{array}{c c c | c} 1 & 2 & 3 & 0 \\ 0 & 1 & 2 & 0 \\ 0 & 0 & 1 & 0 \end{array} \right] $$
This is now in row echelon form. There should be one unique, trivial solution to this system. Subtract row 1 by 3 times of row 3 and subtract row 2 by 2 times of row 3
#### $$ \left[ \begin{array}{c c c | c} 1 & 2 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \end{array} \right] $$
Subtract row 1 by 2 times of row 2
#### $$ \left[ \begin{array}{c c c | c} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \end{array} \right] $$
So the solution to this system is
#### $$ \begin{array}{} x_{1} = 0 \\ x_{2} = 0 \\ x_{3} = 0 \end{array} $$
In column vector form, it is
#### $$\vec{x} = \begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix}$$
```

## Consistency of Systems
Let $C$ be a $(m \times n)$ matrix in row reduced echolon from and let $r$ be the number of nonzero rows of $C$. Then, for the system represented by $[C | \vec{d}]$ there are three possibilities. 
1. The system is inconsistent
2. The system is consistent and $r < n$ and there are infinitely many solutions
3. The system is consistent and $r = n$ and there is a unique solution

A corollary for this theorem is that an $(m \times n )$ system of linear equations where $m < n$ means the system is inconsistent or has infinitely many solutions. 

```ad-example
Solve the following augmented matrix
#### $$[A | \vec{b}] \rightarrow\text{EROs} \rightarrow [C | \vec{d}] = \left[\begin{array}{c c c c | c}1 & 0 & 0 & 3 & 1 \\ 0 & 0 & 1 & -2 & 4 \\ 0 & 0 & 0 & 0 & a \\ 0 & 0 & 0 & 0 & 0\end{array}\right]$$
When $a ≠ 0$, the system would be inconsistent, so $a$ has to be 0. When $a = 0$, the matrix can be written as
#### $$ \begin{array}{} x_{1} + 3x_{4} = 1 \\ x_{3} - 2x_{4} = 4 \end{array} \implies \begin{array}{} x_{1} = 1 - 3x_{4} \\ x_{2} = x_{2} \\ x_{3} = 4 + 2x_{4} \\ x_{4} = x_{4} \end{array} $$
Both $x_{2}$ and $x_{4}$ are free variables, so the solution of the system in vector form would be
#### $$\vec{x} = \begin{bmatrix} x_{1} \\ x_{2} \\ x_{3} \\ x_{4} \end{bmatrix} = \begin{bmatrix} 1 \\ 0 \\ 4 \\ 0 \end{bmatrix} + x_{2}\begin{bmatrix} 0 \\ 1 \\ 0 \\ 0 \end{bmatrix} + x_{4}\begin{bmatrix} -3 \\ 0 \\ 2 \\ 1 \end{bmatrix}$$
```

```ad-example
Solve the following augmented matrix
#### $$[A | \vec{b}] \rightarrow \text{EROs} \rightarrow [C | \vec{d}] = \left[\begin{array}{c c | c} 1 & 0 & 2 \\ 0 & 1 & 0 \\ \hdashline 0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{array}\right]$$
Here $r = n$, so there should be one single unique solution. 
#### $$ \begin{array}{} x_{1} = 2 \\ x_{2} = 0 \end{array}  $$
The column vector form should be 
#### $$\vec{x} = \begin{bmatrix} 2 \\ 0 \end{bmatrix}$$
```

```ad-example
Determine conditions on $b_{1}$, $b_{2}$, $b3$ for the system to be consistent. 
#### $$\begin{array}{} x_{1} - 2x_{2} + 3x_{3} = b_{1} \\ 2x_{1} - 3x_{2} + 2x_{3} = b_{2} \\ -x_{1} + 5x_{3} = b_{3} \end{array}$$
First convert it to an augmented matrix, and then perform EROs on it
#### $$\left[ \begin{array}{c c c | c} 1 & -2 & 3 & b_{1} \\ 2 & -3 & 2 & b_{2} \\ -1 & 0 & 5 & b_{3} \end{array} \right] \rightarrow \text{EROs} \rightarrow \left[\begin{array}{c c c | c} 1 & 0 & -5 & -3b_{1} + 2b_{2} \\ 0 & 1 & -4 & -2b_{1} + b_{2} \\ 0 & 0 & 0 & -3b_{1} + 2b_{2} + b_{3} \end{array}\right]$$
This means that if the bottom row's constant is non-zero, there is no solution to this system. Otherwise, there are infinitely many solutions, since $r < n$. In order to make it a consistent system, $-3b_{1} + 2b_{2} + b_{3} = 0$ must mean $b_{1} = b_{2} = b_{3} = 1$. So the column vector of the solution must be 
#### $$\vec{b} = \begin{bmatrix} 1 \\ 1 \\ 1 \end{bmatrix}$$
```

___
# References
[[MATH2010_1.2_1.3.pdf]]
[[MATH2010_1.3_1.5_1.6.pdf]]
