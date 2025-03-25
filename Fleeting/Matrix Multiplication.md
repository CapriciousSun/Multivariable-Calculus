20250313103112

Tags:

Matrix multiplication is the multiplication of every single value inside of a matrix with another matrix.

## Formalism
```ad-formula
#### Summation of a Matrix
For a matrix $A$ with $(m\times n)$ size and $B$ with $(n \times p)$ size, their product $AB$ is of size $(m \times p)$. In other words, their inner products must match up, or the number of columns of the first matrix must match up to the number of rows of the second matrix. If $AB_{ij}$ denotes the $ij$th-entry in $AB$, then 
#### $$AB_{ij} = a_{i1}b_{1j} + a_{i2}b_{2j} + \dots + a_{in}b_{nj} = \sum_{k = 1}^{n}a_{ik}b_{kj}$$
```

```ad-formula
#### Matrix Multiplication of Two Matrices
#### $$AB = \begin{bmatrix} a_{11} & a_{12} & \dots & a_{1n} \\ \vdots & \vdots &  & \vdots \\ a_{i1} & a_{i2} & \dots & a_{in} \\ \vdots & \vdots &  & \vdots \\ a_{m1} & a_{m2} & \dots & a_{mn} \end{bmatrix}\begin{bmatrix} b_{11} & b_{12} & \dots & b_{1p} \\ b_{21} & b_{22} & \dots & b_{2p} \\ \vdots & \vdots &  & \vdots \\ b_{n1} & b_{n2} & \dots & b_{np} \end{bmatrix} = \begin{bmatrix} c_{11} & \dots & c_{1j} & \dots & c_{1p} \\ \vdots &  & \vdots &  & \vdots \\ c_{i1} & \dots & c_{ij} & \dots & c_{ip} \\ \vdots &  & \vdots & & \vdots \\ c_{m1} & \dots & c_{mj} & \dots & c_{mp} \end{bmatrix}$$
```

```ad-formula
#### Column Vector Matrix Multiplication
Matrices can also be multiplied to vectors, which can be viewed as single columned vectors. 
#### $$A\vec{v} = v_{1}\vec{A_{1}} + v_{2}\vec{A_{2}} + \dots + v_{n}\vec{A_{n}} = \begin{bmatrix} a_{11} & a_{12} & \dots & a_{1n} \\ a_{21} & a_{22} & \dots &  a_{2n} \\ \vdots & \vdots &  & \vdots \\ a_{m1} & a_{m2} & \dots & a_{mn} \end{bmatrix}\begin{bmatrix} v_{1} \\ v_{2} \\ \vdots \\ v_{n} \end{bmatrix} = \begin{bmatrix} a_{11}v_{1} + a_{12}v_{2} + \dots + a_{1n}v_{n} \\ a_{21}v_{1} + a_{22}v_{2} + \dots + a_{2n}v_{n} \\ \vdots \\ a_{m1}v_{1} + a_{m2}v_{2} + \dots + a_{mn}v_{n} \end{bmatrix}$$
```

#### Example
For matrices
#### $$A = \begin{bmatrix}
2 & 1 \\
0 & 1 \\
1 & 0
\end{bmatrix};\ B = \begin{bmatrix}
1 & 1 \\
4 & 2
\end{bmatrix};\ C = \begin{bmatrix}
4 & -2 & 1 \\
0 & 2 & 3
\end{bmatrix};\ \vec{v} = \begin{bmatrix}
-1 \\
3
\end{bmatrix}$$
The following operations are defined
- $AC$
- $CA$
- $BA^{T}$
- $A\vec{v}$
- $B\vec{v}$

#### $$AC = \begin{bmatrix}
2 & 1 \\
0 & 1 \\
1 & 0
\end{bmatrix}\begin{bmatrix}
4 & -2 & 1 \\
0 & 2 & 3
\end{bmatrix} = \begin{bmatrix}
(4 * 2 + 1 * 0) & ((-2) * 2 + 2 * 1) & (2 * 1 + 3 * 1) \\
(0 * 4 + 1 * 0) & ()
\end{bmatrix} = \begin{bmatrix}
8 & -2 & 5 \\
0 & 2 & 3 \\
4 & -2 & 1
\end{bmatrix}$$
#### $$CA = \begin{bmatrix}
4 & -2 & 1 \\
0 & 2 & 3
\end{bmatrix}\begin{bmatrix}
2 & 1 \\
0 & 1 \\
1 & 0
\end{bmatrix} = \begin{bmatrix}
(4 * 2 + (-2) * 0 + 1 * 1) & (4 * 1 + (-2) * 1 + 1 * 0) \\
(0 * 2 + (2) * 0 + 3 * 1) & (0 * 1 + 2 * 1 + 3 * 0)
\end{bmatrix} = \begin{bmatrix}
9 & 2 \\
3 & 2
\end{bmatrix}$$
#### $$BA^{T} = \begin{bmatrix}
1 & 1 \\
4 & 2
\end{bmatrix}\begin{bmatrix}
2 & 0 & 1 \\
1 & 1 & 0
\end{bmatrix} = \begin{bmatrix}
(1 * 2 + 1 * 1) & (1 * 0 + 1 * 1) & (1 * 1 + 1 * 0) \\
(4 * 2 + 2 * 1) &  (4 * 0 + 2 * 1) & (4 * 1 + 2 * 0)
\end{bmatrix} = \begin{bmatrix}
3 & 1 & 1 \\
10 & 2 & 4
\end{bmatrix}$$
#### $$A\vec{v} = \begin{bmatrix}
2 & 1 \\
0 & 1 \\
1 & 0
\end{bmatrix}\begin{bmatrix}
-1 \\
3
\end{bmatrix} = -1\begin{bmatrix}
2 \\
0 \\
1
\end{bmatrix} + 3\begin{bmatrix}
1 \\
1 \\
0
\end{bmatrix} = \begin{bmatrix}
(2 * (-1) + 1 * 3) \\
(0 * (-1) + 1 * 3) \\
(1 * (-1) + 0 * 3)
\end{bmatrix} = \begin{bmatrix}
1 \\
3 \\
-1
\end{bmatrix}$$
#### $$B\vec{v} = \begin{bmatrix}
1 & 1 \\
4 & 2
\end{bmatrix}\begin{bmatrix}
-1 \\
3
\end{bmatrix} = \begin{bmatrix}
(1 * (-1) + 1 * 3) \\
(4 * (-1) + 2 * 3)
\end{bmatrix} = \begin{bmatrix}
2 \\
2
\end{bmatrix}$$

Matrix multiplication is not commutative, even when both options are defined. 

## Matrix Equation
A system of linear equations can be expressed as a matrix equation.
#### $$\begin{array}{}
a_{11}x_{1} + a_{12}x_{2} + \dots + a_{1n}x_{n} = b_{1} \\
a_{21}x_{1} + a_{22}x_{2} + \dots + a_{2n}x_{n} = b_{2} \\
\vdots \\
a_{m1}x_{1} + a_{m2}x_{2} + \dots + a_{mn}x_{n} = b_{n}
\end{array} \longleftrightarrow \begin{bmatrix}
a_{11} & a_{12} & \dots & a_{1n} \\
a_{21} & a_{22} & \dots & a_{2n} \\
\vdots & \vdots &  & \vdots \\
a_{m1} & a_{m2} & \dots & a_{mn}
\end{bmatrix}\begin{bmatrix}
x_{1} \\
x_{2} \\
\vdots \\
x_{n}
\end{bmatrix} = \begin{bmatrix}
b_{1} \\
b_{2} \\
\vdots \\
b_{n}
\end{bmatrix}$$
The system must be solved as $A\vec{x} = \vec{b}$. 

## Physical Interpretation
The physical interpretation of matrices and vectors can be viewed as graphs. The solution to $\vec{x}$ to some $A$ is the linear combination of the column vectors $\vec{A_{1}}, \vec{A_{2}}, \dots \vec{A_{n}}$. 
#### Example
#### $$\begin{array}{}
3x_{1} + x_{2} = 7 \\
x_{1} + 2x_{2} = 4
\end{array}$$
For the linear equation as seen above, the following augmented matrix can be made
#### $$\left[\begin{array}{c c | c}
3 & 1 & 7 \\
1 & 2 & 4
\end{array}\right] \longrightarrow \text{EROs} \longrightarrow \left[\begin{array}{c c | c}
1 & 0 & 2 \\
0 & 1 & 1
\end{array}\right]$$
We interpret the solution of this system as the intersection between the two lines in the planes $x_{1}$ and $x_{2}$. 
```tikz
\begin{document}
  \begin{tikzpicture}[scale=1]
    \draw[thin] (-0.1,-4.1) grid (16,3);
    \draw[->, very thick] (0,0) -- (16,0) node[right] {\Large $x_{1}$};
    \draw[->, very thick] (0,-4) -- (0,3) node[above] {\Large $x_{2}$};
    \draw[color=green, domain=0:13, very thick] plot (\x,{0.5*\x - 3.5}) node[right] {\Large $2x - 4y = 14$};
    \draw[color=cyan, domain=0:16, very thick] plot (\x,{(1/3)*\x - 3}) node[right] {\Large $-2x + 6y = -17$};
    \filldraw[yellow] (3, -2) circle (4pt) node[right] {\Large $(x, y) = (3, -2)$};
  \end{tikzpicture}
\end{document}
```

Another way of interpretation is to see the system as a linear combination of columns. 
#### $$\begin{bmatrix}
3 & 1 \\
1 & 2
\end{bmatrix}\begin{bmatrix}
x_{1} \\
x_{2}
\end{bmatrix} = \begin{bmatrix}
7 \\
4
\end{bmatrix} \implies A\vec{x} = x_{1}\begin{bmatrix}
3 \\
1
\end{bmatrix} + x_{2}\begin{bmatrix}
1 & 2
\end{bmatrix} = \begin{bmatrix}
7 \\
4
\end{bmatrix}$$
