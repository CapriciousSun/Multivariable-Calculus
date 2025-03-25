20250313113216

Tags:

A matrix has several characteristics relating to operations and its inherent properties.

## Equality
Two matrices are equal if and only if they have the same size and every single entry are equal. Mathematically, this means for a $(m \times n)$ matrix, every single $A = a_{ij}$ and $B = b_{ij}$ are equal for all $1 ≤ i ≤ m$ and $1 ≤ j ≤ n$. 

## Summation
If $A$ and $B$ are both $(m \times n)$ matrices, then their sum is $A + B$ is a matrix where every entry $a_{ij} + b_{ij}$ for all $1 ≤ i ≤ m$ and $1 ≤ j ≤ n$. Otherwise, the sum will be undefined. 

## Scalar Multiplicity
If $A$ is a $(m \times n)$ matrix and $c$ is a scalar, then the *scalar multiple* $cA$ is the a matrix where every entry is $ca_{ij}$ for all $1 ≤ i ≤ m$ and $1 ≤ j ≤ n$. 

## Transpose
If $A$ is an $(m \times n)$ matrix, then the transpose $A^{T}$ is an $(n \times m)$ matrix where every entry $a^{T}_{ij} = a_{ji}$ for all $1 ≤ i ≤ m$ and $1 ≤ j ≤ n$. 

```ad-example
Consider the following matrices $A$ and $B$
#### $$A = \begin{bmatrix} 4 & -1 \\ 0 & 3 \\ 5 & 2 \end{bmatrix},\ \ \ \ B = \begin{bmatrix} 1 & 1 & 1 \\ 3 & 5 & 7 \end{bmatrix}$$
Find the following operations if they are defined.
#### $$2B = 2\begin{bmatrix} 1 & 1 & 1 \\ 3 & 5 & 7 \end{bmatrix} = \begin{bmatrix} 2 & 2 & 2 \\ 6 & 10 & 14 \end{bmatrix}$$
#### $$A + 2B = \begin{bmatrix} 4 & -1 \\ 0 & 3 \\ 5 & 2 \end{bmatrix} + \begin{bmatrix} 2 & 2 & 2 \\ 6 & 10 & 14 \end{bmatrix} = undefined$$
#### $$A^{T} + 2B = \begin{bmatrix} 4 & 0 & 5 \\ -1 & 3 & 2 \end{bmatrix} + \begin{bmatrix} 2 & 2 & 2 \\ 6 & 10 & 14 \end{bmatrix} = \begin{bmatrix} 6 & 2 & 7 \\ 5 & 13 & 16 \end{bmatrix}$$
#### $$A - 2B^{T} = \begin{bmatrix} 4 & -1 \\ 0 & 3 \\ 5 & 2 \end{bmatrix} - \begin{bmatrix} 2 & 6 \\ 2 & 10 \\ 2 & 14 \end{bmatrix} = \begin{bmatrix} 2 & -7 \\ -2 & -7 \\ 3 & -12 \end{bmatrix}$$
```

## Symmetry
A matrix is symmetric if $A^{T} = A$. Hence, it must be a square $(m = n)$. Symmetry can be viewed as drawing a diagonal line across the matrix and "folding" it. 
#### Example
#### $$A = \begin{bmatrix}
1 & 2 & 1 \\
2 & 3 & 2
\end{bmatrix};\ B = \begin{bmatrix}
1 & 2 \\
2 & 3
\end{bmatrix};\ C = \begin{bmatrix}
1 & 1 & 2 \\
1 & 2 & 0 \\
2 & 0 & 3
\end{bmatrix};\ D = \begin{bmatrix}
1 & -1 & -1 \\
0 & 1 & 0 \\
2 & 2 & 1
\end{bmatrix}$$
$A$ and $D$ are not symmetrical, whereas $B$ and $C$ are symmetrical. 

### Identity
An identity matrix is a matrix of size $(n \times n)$, denoted by $I_{n}$. It is a matrix where the main diagonal are 1s and everything else is a 0. If $A$ is an $(n \times n)$ matrix, then $AI_{n} = I_{n}A$, in other words, $I_{n}$ is the multiplicative identity of $A$. If $B$ is an $(m\times n)$ matrix, then $I_{m}B = B$ and $BI_{m} = B$. 
#### Example
For a matrix $A$
#### $$A = \begin{bmatrix}
-1 & -3 \\
4 & 6
\end{bmatrix}$$
show that $AI_{2} = I_{2}A$
#### $$AI_{2} = \begin{bmatrix}
-1 & -3 \\
4 & 6
\end{bmatrix}\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix} = \begin{bmatrix}
((-1) * 1 + (-3) * 0) & ((-1) * 0 + (-3) * 1) \\
(4 * 1 + 6 * 0) & (4 * 0 + 6 * 1)
\end{bmatrix} = \begin{bmatrix}
-1 & -3 \\
4 & 6
\end{bmatrix}$$

## Independence
For a $(m \times n)$ system of linear equations where $A\vec{x} = \vec{b}$, it can be written in the form $\vec{A_{1}}x_{1} + \vec{A_{2}}x_{2} + \dots + \vec{A_{n}}x_{n} = \vec{b}$ and is only consistent if $\vec{b}$ can be written as a linear combination of the columns of $A$. This idea is going to help determine if vectors are linearly dependent or not. 
#### Formalism
A set of $m$-dimensional vectors written as $\{ \vec{v_{1}}, \vec{v_{2}}, \dots, \vec{v_{p}} \}$ is linearly independent if the only possible solution to the system is $a_{1} = a_{2} = \dots = a_{p} = 0$. The system will be linearly independent if there are non-trivial solutions to the system, or if there exists some $a_{i} ≠ 0$. When taking the determinant of a matrix, if it is equal to zero, the vectors represented by the matrix are linearly dependent. 
#### Example
For a set of vectors 
#### $$\{ \begin{bmatrix}
2 \\
0
\end{bmatrix}, \begin{bmatrix}
0 \\
3
\end{bmatrix}, \begin{bmatrix}
6 \\
6
\end{bmatrix} \}$$
If these three vectors are linearly dependent, they must be linear combinations of each other. So take the third vector for example
#### $$\begin{bmatrix}
6 \\
6
\end{bmatrix} = 3\begin{bmatrix}
2 \\
0
\end{bmatrix} + 2\begin{bmatrix}
0 \\
3
\end{bmatrix}$$
Since it is possible to write these vectors as some linear combination of each other, this system is linearly dependent.

#### Example
For a vector M with some vector x
#### $$M = \begin{bmatrix}
6 & 2 \\
9 & 3
\end{bmatrix}$$
Taking the determinant will result in 
#### $$\det[\begin{bmatrix}
6 & 2 \\
9 & 3
\end{bmatrix}] = 6 * 3 - 9 * 2 = 0$$

#### Example
#### $$\left\{ \begin{bmatrix}
1 \\
0 \\
1
\end{bmatrix}, \begin{bmatrix}
0 \\
1 \\
0
\end{bmatrix}, \begin{bmatrix}
1 \\
1 \\
1
\end{bmatrix} \right\}$$
You can represent the last vector as a linear combination of the first two vectors
#### $$\begin{bmatrix}
1 \\
1 \\
1
\end{bmatrix} = a\begin{bmatrix}
1 \\
0 \\
1
\end{bmatrix} + b\begin{bmatrix}
0 \\
1 \\
0
\end{bmatrix}$$
Solving for $a$ and $b$ can determine if they are linear combinations of each other
#### $$\begin{bmatrix}
1 \\
1 \\
1
\end{bmatrix} = 1\begin{bmatrix}
1 \\
0 \\
1
\end{bmatrix} + 1\begin{bmatrix}
0 \\
1 \\
0
\end{bmatrix}$$
Hence, this system is linearly dependent

#### Example
#### $$\left\{ \begin{bmatrix}
0 \\
0 \\
1
\end{bmatrix}, \begin{bmatrix}
0 \\
1 \\
0
\end{bmatrix}, \begin{bmatrix}
0 \\
0 \\
1
\end{bmatrix} \right\}$$


## Solution
Solving for $a_{1}\vec{v_{1}} + a_{2}\vec{v_{2}} + \dots + a_{p}\vec{v_{p}} = \vec{0}$ is equivalent to solving the system $v\vec{x} = \vec{0}$ where $v = \{ \vec{v_{1}}, \vec{v_{2}}, \dots, \vec{v_{p}} \}$ is the $(m \times n)$ matrix with columns $\vec{v_{1}}, \vec{v_{2}}, \dots, \vec{v_{p}}$ and $\vec{x} = \begin{bmatrix}a_{1} \\ a_{2} \\ \vdots \\ a_{p}\end{bmatrix}$The unit vectors of a linearly independent set are 
#### $$\vec{e_{1}} = \begin{bmatrix}
1 \\
0 \\
0 \\
\vdots \\
0
\end{bmatrix},\ \ \vec{e_{2}} = \begin{bmatrix}
0 \\
1 \\
0 \\
\vdots \\
0
\end{bmatrix},\ \ \dots,\ \ \vec{e_{n}} = \begin{bmatrix}
0 \\
0 \\
0 \\
\vdots \\
1
\end{bmatrix}$$
where these column vectors are of domain $\mathbb{R}^{n}$. 
#### Example
For a linear combination of vectors 
#### $$\vec{v_{1}} = \begin{bmatrix}
0 \\
0 \\
2
\end{bmatrix},\ \ \vec{v_{2}} = \begin{bmatrix}
0 \\
5 \\
-8
\end{bmatrix},\ \ \vec{v_{3}} = \begin{bmatrix}
-6 \\
10 \\
2
\end{bmatrix}$$
the combined matrix of them should be 
#### $$a_{1}\vec{v_{1}} + a_{2}\vec{v_{2}} + a_{3}\vec{v_{3}} = \vec{0} \implies \begin{bmatrix}
0 & 0 & -6 \\
0 & 5 & 10 \\
2 & -8 & 2
\end{bmatrix}\begin{bmatrix}
a_{1} \\
a_{2} \\
a_{3}
\end{bmatrix} = \begin{bmatrix}
0 \\
0 \\
0
\end{bmatrix} \implies \left[\begin{array}{c c c | c}
0 & 0 & -6 & 0 \\
0 & 5 & 10 & 0 \\
2 & -8 & 2 & 0
\end{array}\right]$$
Exchange row 3 and row 1 so that there'll be a leading 0
#### $$\left[ \begin{array}{c c c | c}
2 & -8 & 2 & 0 \\
0 & 5 & 10 & 0 \\
0 & 0 & -6 & 0
\end{array} \right]$$
Divide row 1 by 2, divide row 2 by 5, divide row 3 by -6
#### $$\left[ \begin{array}{c c c | c}
1 & -4 & 1 & 0 \\
0 & 1 & 2 & 0 \\
0 & 0 & 1 & 0
\end{array} \right]$$
This will put the system into a reduced row echelon form. Row 1 will be subtracted by row 3 and row 2 will be subtracted by 2 times of row 3.
#### $$\left[ \begin{array}{c c c | c}
1 & -4 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0
\end{array} \right]$$
Row 1 will add 4 times of row 2
#### $$\left[ \begin{array}{c c c | c}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0
\end{array} \right]$$
This the solutions to this system are trivial. 
#### $$\begin{cases}
a_{1} = 0 \\
a_{2} = 0 \\
a_{3} = 0
\end{cases}\ \ \ \ \vec{x} = \begin{bmatrix}
0 \\
0 \\
0
\end{bmatrix}$$
Hence, this system is linear independent. 

#### Example
For a linear combination of vectors
#### $$\vec{u_{1}} = \begin{bmatrix}
1 \\
2 \\
3
\end{bmatrix},\ \ \vec{u_{2}} = \begin{bmatrix}
4 \\
5 \\
6
\end{bmatrix},\ \ \vec{u_{3}} = \begin{bmatrix}
2 \\
1 \\
0
\end{bmatrix}$$
Turn this into a system of liner equations
#### $$x_{1}\vec{u_{1}} + x_{2}\vec{u_{2}} + x_{3}\vec{u_{3}} = \vec{0} \implies \begin{bmatrix}
1 & 4 & 2 \\
2 & 5 & 1 \\
3 & 6 & 0
\end{bmatrix}\begin{bmatrix}
x_{1} \\
x_{2} \\
x_{3}
\end{bmatrix} = \begin{bmatrix}
0 \\
0 \\
0
\end{bmatrix}$$
Solving for this system results in 
#### $$\left[ \begin{array}{c c c | c}
1 & 4 & 2 & 0 \\
2 & 5 & 1 & 0 \\
3 & 6 & 0 & 0
\end{array} \right] \longrightarrow \text{EROs} \longrightarrow \left[ \begin{array}{c c c | c}
1 & 0 & -2 & 0 \\
0 & 1 & 1 & 0 \\
0 & 0 & 0 & 0
\end{array} \right]$$
Writing this as a reduced system allows for the solution
#### $$\begin{array}{}
x_{1} - 2x_{3} = 0 \\
x_{2} + x_{3} = 0
\end{array} \implies \begin{array}{}
x_{1} = 2x_{3} \\
x_{2} = -x_{3} \\
x_{3} = x_{3}
\end{array} \implies \vec{x} = \begin{bmatrix}
x_{1} \\
x_{2} \\
x_{3}
\end{bmatrix} = \begin{bmatrix}
2x_{3} \\
-x_{3} \\
x_{3}
\end{bmatrix} = x_{3}\begin{bmatrix}
2 \\
-1 \\
1
\end{bmatrix}$$
So the easiest choice is to let $x_{3} = 1$. $x_{3} = 0$  would be the trivial solution. 
#### $$\begin{array}{}
x_{1} = 2 \\
x_{2} = -1 \\
x_{3} = 1
\end{array} \implies 2\vec{u_{1}} + (-1)\vec{u_{2}} + 1\vec{u_{3}} = 0$$
Therefore, $\vec{u_{3}} = \vec{u_{2}} - 2\vec{u_{1}}$ would be the proper, non-trivial solution. 
#### Shortcuts
There are some rules that can help determine the linear independence faster.
- $\{ \vec{v} \}$ is linearly independent if and only if $\vec{v} ≠ \vec{0}$
- $\{ \vec{v_{1}}, \vec{v_{2}} \}$ is linearly independent if and only if $\vec{v_{1}} ≠ c\vec{v_{2}}$ for some scalar $c$
	- In other words, they are linearly dependent if they are scalar multiples of each other
- If $\{ \vec{v_{1}}, \vec{v_{2}}, \dots, \vec{v_{p}} \}$ contain $\vec{0}$, then the set is linearly dependent
- The set $\{ \vec{v_{1}}, \vec{v_{2}}, \dots, \vec{v_{n}} \}$ in $\mathbb{R}^{m}$ is linearly dependent if $n > m$
#### Example
#### $$\left\{ \begin{bmatrix}
2 \\
1
\end{bmatrix}, \begin{bmatrix}
4 \\
-1
\end{bmatrix}, \begin{bmatrix}
-2 \\
2
\end{bmatrix} \right\}$$
is linearly dependent, since $m(3) > n(2)$.
#### $$\left\{ \begin{bmatrix}
1 \\
1 \\
2
\end{bmatrix}, \begin{bmatrix}
-3 \\
-3 \\
-6
\end{bmatrix} \right\}$$
is linearly dependent, since $-3\vec{v_{1}} = \vec{v_{2}}$
#### $$\left\{ \begin{bmatrix}
2 \\
3 \\
5
\end{bmatrix}, \begin{bmatrix}
0 \\
0 \\
0
\end{bmatrix}, \begin{bmatrix}
1 \\
1 \\
8
\end{bmatrix} \right\}$$
is linearly dependent, since it contains $\vec{0}$
#### $$\left\{ \begin{bmatrix}
-2 \\
4 \\
6 \\
10
\end{bmatrix}, \begin{bmatrix}
3 \\
-6 \\
-9 \\
15
\end{bmatrix} \right\}$$
is linearly independent, since it does not fulfill any of the prerequisites for linear dependence.

## Singularity
#### Formalism
A $(n \times n)$ matrix is nonsingular if the only solution to $A\vec{x} = \vec{0}$ is $\vec{x} = \vec{0}$. Otherwise, $A$ is called a singular. Operation wise, this means
#### $$[A | \vec{0}] \longrightarrow \text{EROs} \longrightarrow [I_{n} | \vec{0}]$$
The $(n \times n)$ matrix $A = [\vec{A_{1}}, \vec{A_{2}}, \dots, \vec{A_{n}}]$ where some $\vec{A_{i}} \in \mathbb{R}^{n}$ are the columns of $A$, is nonsingular if and only if $\{ \vec{A_{1}}, \vec{A_{2}}, \dots, \vec{A_{n}} \}$ is a linearly independent set. If $A$ is a nonsingular $(n \times n)$ matrix, then for each $\vec{b} \in \mathbb{R}^{n}$, the equation $A\vec{x} = \vec{b}$ has a unique solution. 
#### Example
For a square matrix 
#### $$A = \begin{bmatrix}
1 & 3 \\
4 & 4
\end{bmatrix}$$
it can be broken down to columns 
#### $$\vec{A_{1}} = \begin{bmatrix}
1 \\
4
\end{bmatrix},\ \ \vec{A_{2}} = \begin{bmatrix}
3 \\
4
\end{bmatrix}$$
which are linearly indepdendent, hence, this system is nonsingular.

#### Example
For a square matrix
#### $$B = \begin{bmatrix}
1 & 2 \\
3 & 6
\end{bmatrix}$$
can be broken down to columns
#### $$\vec{B_{1}} = \begin{bmatrix}
1 \\
3
\end{bmatrix},\ \ \vec{b_{2}} = \begin{bmatrix}
2 \\
6
\end{bmatrix}$$
which are linearly dependent due to $2\vec{B_{1}} = B_{2}$. Hence, the system is singular

## Inversion
#### Formalism
For an $(n \times n)$ matrix $A$, it is invertible if there exists an $(n \times n)$ matrix denoted by $A^{-1}$ such that $AA^{-1} = I_{n} = A^{-1}A$. $A$ is only invertible if and only if it is nonsingular, so $A$ is row equivalent to $I_{n}$. If $A$ is an invertible $(n \times n)$ matrix, then for each $\vec{b} \in \mathbb{R}^{n}$ te equation $A\vec{x} = \vec{b}$ has the unique solution $\vec{x} = A^{-1}\vec{b}$. 
#### Finding the Inverse
Given a $(n \times n)$ matrix $A$, finding $A^{-1}$ involves row reducing the augmented matrix $[A | I_{n}]$. If $A$ is a row equivalent to $I_{n}$, then $[A | I_{n}]$ is row equivalent to $[I_{n} | A^{-1}]$. Otherwise, $A$ does not have an inverse. 
#### Example
Find the inverse of the matrix $A$
#### $$\begin{gather}
A = \begin{bmatrix}
1 & 1 & 1 \\
2 & 3 & 2 \\
3 & 8 & 2
\end{bmatrix} \\ \\
[A | I_{3}] = \left[\begin{array}{c c c | c c c}
1 & 1 & 1 & 1 & 0 & 0 \\
2 & 3 & 2 & 0 & 1 & 0 \\
3 & 8 & 2 & 0 & 0 & 1
\end{array}\right]
\end{gather}$$
Row 2 should be subtracted by 2 times row 1 and row 3 should be subtracted by 3 times row 1
#### $$[A | I_{3}] = \left[\begin{array}{c c c | c c c}
1 & 1 & 1 & 1 & 0 & 0 \\
0 & 1 & 0 & -2 & 1 & 0 \\
0 & 0 & -1 & -3 & 0 & 1
\end{array}\right]$$
Row 1 should be subtracted by row 2 and row 3 should be subtracted by 5 times row 2
#### $$[A | I_{3}] = \left[ \begin{array}{c c c | c c c}
1 & 0 & 1 & 3 & -1 & 0 \\
0 & 1 & 0 & -2 & 1 & 0 \\
0 & 0 & -1 & 7 & -5 & 1
\end{array} \right]$$
Row 3 should be the negation of row 3 and then row 1 should be subtracted by row 3
#### $$[A | I_{3}] = \left[ \begin{array}{c c c | c c c}
1 & 0 & 0 & 10 & -6 & 1 \\
0 & 1 & 0 & -2 & 1 & 0 \\
0 & 0 & 1 & -7 & 5 & -1
\end{array} \right]$$
Hence, $A^{-1}$ is acquired through this process
#### $$A^{-1} = \begin{bmatrix}
10 & -6 & 1 \\
-2 & 1 & 0 \\
-7 & 5 & 1
\end{bmatrix}$$
#### Shortcuts
There are a few shortcuts to find $A^{-1}$ for a $(2 \times 2)$ matrix. Let there be some $A$ matrix
#### $$A = \begin{bmatrix}
a & b \\
c & d
\end{bmatrix}$$
If $\det(A) = ad - bc ≠ 0$, then $A$ is invertible and the inversion is the following
#### $$A^{-1} = \frac{1}{ad - bc} \begin{bmatrix}
d & -b \\
-c & a
\end{bmatrix}$$
Otherwise, $A$ is not invertible. 
#### Example
Consider the system of equations
#### $$\begin{array}{}
3x_{1} + 4x_{2} = 3 \\
5x_{1} + 6x_{2} = 7
\end{array}$$
Find $A^{-1}$ and use it to calculate the solution of the system
#### $$\begin{bmatrix}
3 & 4 \\
5 & 6
\end{bmatrix}\begin{bmatrix}
x_{1} \\
x_{2}
\end{bmatrix} = \begin{bmatrix}
3 \\
7
\end{bmatrix}$$
Use the formula for a $(2 \times 2)$ matrix
#### $$A^{-1} = \frac{1}{3 * 6 - 4 * 5} \begin{bmatrix}
6 & -4 \\
-5 & 3
\end{bmatrix} = -\frac{1}{2} \begin{bmatrix}
6 & -4 \\
-5 & 3
\end{bmatrix} = \begin{bmatrix}
-3 & 2 \\
\frac{5}{2} & -\frac{3}{2}
\end{bmatrix} \implies \begin{array}{}
-3x_{1} + 2x_{2} = 3 \\
\frac{5}{2}x_{1} - \frac{3}{2}x_{2} = 7
\end{array}$$
Then, all there is left is to multiply the answer column vector by the inverse of $A$
#### $$\vec{x} = A^{-1}\vec{b} = \begin{bmatrix}
-3 & 2 \\
\frac{5}{2} & -\frac{3}{2}
\end{bmatrix}\begin{bmatrix}
3 \\
7
\end{bmatrix} = \begin{bmatrix}
5 \\
-3
\end{bmatrix} = 3\begin{bmatrix}
3 \\
\frac{5}{2}
\end{bmatrix} + 7\begin{bmatrix}
2 \\
-\frac{3}{2}
\end{bmatrix}$$
Hence, the answer is $\vec{x}$
#### $$\vec{x} = \begin{bmatrix}
5 \\
-3
\end{bmatrix}$$
___
# References
[[MATH2010_1.3_1.5_1.6.pdf]]
