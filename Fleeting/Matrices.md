20250323145937

Tags:

A matrix is way of representing [[Linear Equations and Linear Systems#Linear System|systems of linear equations]]. 

## Formalism
A matrix is rectangular array of numbers. A matrix $A$ would have $m$ rows and $n$ columns. If $m = n$, then $A$ is a square matrix.
```ad-formula
#### General Form of a Matrix
A matrix $A$ always has $m$ rows and $n$ columns
#### $$A = \begin{bmatrix} a_{11} & a_{12} & \dots & a_{1n} \\ a_{21} & a_{22} & \dots & a_{2n} \\ \vdots & \vdots & & \vdots \\ a_{m1} & a_{m2} & \dots & a_{mn} \end{bmatrix} $$
The notation $A = (a_{ij})_{m \times n}$ is typically used to represent a matrix $A$. The number $a_{ij}$ is the $ij$-entry of the (m \times n) matrix $A$, or the entry of row $i$ and column $j$.
```

Furthermore, a matrix with one row is called a row vector and a matrix with one column is called a column vector. 

## Augmented Matrices
Augmented matrices are what's used for representing non-homogeneous linear systems. 
```ad-formula
#### General Form of an Augmented Matrix
For a general linear system with $m$ equations and $n$ variables, the augmented matrix would be split between variables represented by the matrix $A$ and constants represented by the column vector $\vec{b}$
#### $$ [A | \vec{b}] = \left[\begin{array}{c c c c | c} a_{11} & a_{12} & \dots & a_{1n} & b_{1} \\ a_{21} & a_{22} & \dots & a_{2n} & b_{2} \\ \vdots & \vdots & & \vdots & \vdots \\ a_{m1} & a_{m2} & \vdots & a_{mn} & b_{m} \end{array}\right] $$
Here, $A$ is called the coefficient matrix. The solution to this system is called the solution matrix $\vec{x}$ where $\vec{x} = \begin{bmatrix} x_{1} \\ x_{2} \\ \vdots \\ x_{n} \end{bmatrix}$. 
```

## Elementary Row Operations
The main idea of elimination is to eliminate variables in a systematic manner called elementary operations. This would result in a matrix that's equivalent to the one being solved. The following are some elementary row operations.
- Interchange any two rows ($R_{i} \longleftrightarrow R_{j}$)
- Multiply a row by a non-zero number ($kR_{i}, k \neq 0$)
- Add a multiple of one row to another row ($R_{i} + kR_{j}$)
The goal of these operations is to reduce an augmented matrix until the coefficient matrix is in echelon or row reduced echelon form. This process is also called Gauss-Jordan elimination. 

## Echelon Form
Echelon form works off of the concept of leading entries, or the leftmost non-zero entry in a non-zero row. So, a $(m \times n)$ matrix is in echelon form if it satisfies all three conditions
1. All non-zero rows are above any rows of all zeros
2. The leading entry of each non-zero row is a 1, and the leading 1 is in a column to the right of the leading 1 in the row above it
3. All entries in a column below a leading 1 must be zero
For a matrix to be in row-reduced echelon form, it requires one more condition.
4. Each leading 1 is the only non-zero entry in its column
```ad-example
#### Examples
Each of the following matrix is either not in echelon form, in echelon form, and in row-reduced echelon form.
#### $$A = \begin{bmatrix} 1 & 2 & 3 \\ 0 & 1 & 4 \\ 0 & 0 & 1 \end{bmatrix} \text{  II}$$
#### $$ B = \begin{bmatrix} 1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \end{bmatrix} \text{  I}$$
#### $$ C = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0 \end{bmatrix} \text{  III} $$
#### $$ D = \begin{bmatrix} 1 & 0 & 0 & 2 \\ 0 & 1 & 0 & 1 \\ 0 & 0 & 1 & 2 \end{bmatrix} \text{  III} $$
#### $$ E = \begin{bmatrix} 1 & 2 & 0 \\ 0 & 0 & 1 \\ 0 & 0 & 0 \end{bmatrix} \text{  III} $$
```

## Solving a Linear System
Solving a linear system using matrices involves using the above described techniques to arrive at a row-reduced echelon form.
```ad-example
Solve the following linear system
#### $$ \begin{cases} x_{1} - 3x_{2} = 7 \\ -3x_{1} + 4x_{2} = -1 \end{cases} $$
The augmented matrix of this system would look like
#### $$ \left[\begin{array}{c c | c} 1 & -3 & 7 \\ -3 & 4 & -1 \end{array}\right] $$
Add row 2 by -3 times of row 1 to eliminate the first coefficient in row 2
#### $$ \left[ \begin{array}{c c | c} 1 & -3 & 7 \\ 0 & -5 & 20 \end{array} \right] $$
Divide row 2 by -5 to make the second coefficient in row 2 a leading 1
#### $$ \left[ \begin{array}{c c | c} 1 & -3 & 7 \\ 0 & 1 & -4 \end{array} \right] $$
Add row 1 by 3 times of row 2 to eliminate the second coefficient of row 1
#### $$ \left[ \begin{array}{c c | c} 1 & 0 & -5 \\ 0 & 1 & -4 \end{array} \right] $$
This yields the unique solution $(-5, -4)$ or $\vec{x} = \begin{bmatrix} -5 \\ -4 \end{bmatrix}$
```

This process is commonly called a *row reduction algorithm*, going from an augmented matrix to echelon form, and from echelon form to row-reduced echelon form. 
```ad-example
Solve the following linear system using the row reduction algorithm
#### $$ \begin{array} x_{1} - 2x_{2} - x_{3} = 3 \\ 3x_{1} - 6x_{2} - 5x_{3} = 3 \\ 2x_{1} - x_{2} + x_{3} = 0 \end{array} $$
Turn this system to an augmented matrix
#### $$ \left[ \begin{array}{c c c | c} 1 & -2 & -1 & 3 \\ 3 & -6 & -5 & 3 \\ 2 & -1 & -1 & 0 \end{array} \right] $$
Start with the leftmost column, eliminating all the non-zero entries aside from the first row. Subtract row 2 with 3 times of row 1 and subtract row 3 with 2 times of row 1
#### $$ \left[ \begin{array}{c c c | c} 1 & -2 & -1 & 3 \\ 0 & 0 & -2 & -6 \\ 0 & 3 & 3 & -6 \end{array} \right] $$
Row 3 has a leading entry before row 2, so those two are switched. Then, divide row 2 by a factor of 3 and row 3 by a factor of -2
#### $$ \left[ \begin{array}{c c c | c} 1 & -2 & -1 & 3 \\ 0 & 1 & 1 & -2 \\ 0 & 0 & 1 & 3 \end{array} \right] $$
Now, the augmented matrix is in echelon form. The matrix should not have any non-zero solutions for a non-zero coefficient matrix, because that is a system without solutions. If the system has a solution, then the echelon form can be row-reduced. Here, row 1 is added by row 3 and row 2 is subtracted by row 2.
#### $$ \left[ \begin{array}{c c c | c} 1 & -2 & 0 & 6 \\ 0 & 1 & 0 & -5 \\ 0 & 0 & 1 & 3 \end{array} \right] $$
Then, row 1 is added by 2 times row 2
#### $$ \left[ \begin{array}{c c c | c} 1 & 0 & 0 & -4 \\ 0 & 1 & 0 & -5 \\ 0 & 0 & 1 & 3 \end{array} \right] $$
Since the augmented matrix is now in row-reduced echelon form, the algorithm is complete. The solution of this system is 
#### $$ \begin{array}{} x_{1} = -4 \\ x_{2} = -5 \\ x_{3} = 3 \end{array} $$
or 
#### $$\vec{x} = \begin{bmatrix} x_{1} \\ x_{2} \\ x_{3} \end{bmatrix} = \begin{bmatrix} -4 \\ -5 \\ 3 \end{bmatrix}$$
```

In a row-reduced matrix, the variables occupying the leading 1 positions are called *leading variables*. Zero terms are called *free variables*. 

## Systems with Constants
There are some linear systems with a value $a$, and the solutions are to be found in terms of $a$.
```ad-example
Find all the values of $a$ for which the given system is consistent.
#### $$ \begin{array}{} x_{1} - x_{2} + 7x_{3} = 1 \\ x_{1} - 2x_{2} + 9x_{3} = 0 \\ 2x_{1} - 3x_{2} + 16x_{3} = a \end{array} $$
Convert the system to an augmented matrix
#### $$ \left[ \begin{array}{c c c | c} 1 & -1 & 7 & 1 \\ 1 & -2 & 9 & 0 \\ 2 & -3 & 16 & a \end{array} \right] $$
Subtract row 2 by row 1 and negate it, and subtract row 3 by 2 times of row 1
#### $$ \left[ \begin{array}{c c c | c} 1 & -1 & 7 & 1 \\ 0 & 1 & -2 & 1 \\ 0 & -1 & 2 & a - 2 \end{array} \right] $$
Add row 1 by row 2 and add row 3 by row 2
#### $$ \left[ \begin{array}{c c c | c} 1 & 0 & 5 & 2 \\ 0 & 1 & -2 & 1 \\ 0 & 0 & 0 & a - 1 \end{array} \right] $$
The third row would only be consistent if the constant is 0, so $a - 1 = 0$ and $a = 1$. Therefore, the solutions to this system are
#### $$ \begin{array}{} x_{1} + 5x_{3} = 2 \\ x_{2} - 2x_{3} = 1 \end{array} \implies \begin{array}{} x_{1} = 2 - 5x_{3} \\ x_{2} = 1 + 2x_{3} \\ x_{3} = x_{3} \end{array} $$ 
This system has infinitely many solutions
```

___
# References
[[MATH2010_1.1_1.2.pdf]]
[[MATH2010_1.2_1.3.pdf]]
