20250320110445

Vector space refers to the dimensions of the vectors. 

## Formalism
```ad-formula
#### General Form of an $n$-dimensional Vector
$\mathbb{R}^{n}$ is the set of all $n$-dimensional vectors with real components. The following is the matrix representation of the vector
#### $$R^{n} = \left\{ \vec{x} = \begin{bmatrix} x_{1} \\ x_{2} \\ \vdots \\ x_{n} \end{bmatrix} : x_{1}, x_{2}, \dots, x_{n} \in \mathbb{R} \right\}$$
where $x_{1}, x_{2}, \dots, x_{n}$ are all real. 
```

## Column Vectors

```ad-formula
#### Vector Form of the General Solution
An $n$-dimensional vector in $\mathbb{R}^{n}$ can be written as an $(n \times 1)$ matrix called a column vector
#### $$\vec{x} = \langle x_{1}, x_{2}, \dots, x_{n} \rangle \iff \vec{x} = \begin{bmatrix} x_{1} \\ x_{2} \\ \vdots \\ x_{n} \end{bmatrix}$$
This is a possible for the solution to a linear system.
```

```ad-example
Given the matrix $B$ is the augmented matrix for the homogenous system of linear equations. Give the vector form of the general solution.
#### $$B = \left[\begin{array}{c c c c | c}1 & 0 & -1 & -2 & 0 \\ 0 & 1 & 2 & 3 & 0\end{array}\right]$$
The matrix is already in row-reduced echelon form, so all there is left is to turn it to a linear system and solve for the variables
#### $$\begin{array}{} x_{1} - x_{3} - 2x_{4} = 0 \\ x_{2} + 2x_{3} + 3x_{4} = 0 \end{array} \implies \begin{array}{} x_{1} = x_{3} + 2x_{4} \\ x_{2} = -2x_{3} -3x_{4} \\ x_{3} = x_{3} \\ x_{4} = x_{4} \end{array}$$
In column vector form, this is represented by $x_{3}$ and $x_{4}$ followed by their vectors
#### $$\vec{x} = \begin{bmatrix} x_{1} \\ x_{2} \\ x_{3} \\ x_{4} \end{bmatrix} = \begin{bmatrix} x_{3} + 2x_{4} \\ -2x_{3} - 3x_{4} \\ x_{3} \\ x_{4} \end{bmatrix} = x_{3}\begin{bmatrix} 1 \\ -2 \\ 1 \\ 0 \end{bmatrix} + x_{4}\begin{bmatrix} 2 \\ -3 \\ 0 \\ 1 \end{bmatrix}$$
```


## Matrix Multiplication
If $A$ is an $(m \times n)$ matrix and $B$ is an $(n \times p)$ matrix, then their product $AB$ is defined and is an $(m \times p)$ matrix. The entry in row $i$ and column $j$ of $AB$ is the sum of the products corresponding entries from row $i$ of $A$ and column $j$ of $B$. If $(AB)_{ij}$ denotes the $ij$th-entry in $AB$, then 
#### $$(AB)_{ij} = a_{i1}b_{1j}$$
## Subspace
A subspace is a subset $w$ of the domain $\mathbb{R}^{n}$ if it satisfies certain properties. These properties includes
1. $\vec{0} \in w$ 
2. If $\vec{x}, \vec{y} \in w$, then $\vec{x} + \vec{y} \in w$
3. If $\vec{x} \in w$, then $a\vec{x} \in w$ for all scalar $a \in \mathbb{R}$

Intuitively, the subspace refers to all objects that could exist within a vector space domain. Namely, for a domain $\mathbb{R}^{2}$, the subspaces are
1. all of $\mathbb{R}^{2}$ 
2. any line through the origin $\begin{bmatrix}0 \\ 0\end{bmatrix}$
3. the zero vector $\vec{0}$ alone, $\left\{\begin{bmatrix}0 \\ 0\end{bmatrix}\right\}$

For a domain $\mathbb{R}^{3}$, the subspaces are
1. all of $\mathbb{R}^{3}$
2. any plane through the origin: $ax_{1} + bx_{2} + cx_{3} = 0$
3. any line through the origin $\begin{bmatrix}0 \\ 0 \\ 0\end{bmatrix}$
4. the zero vector $\vec{0}$ alone, $\left\{ \begin{bmatrix}0 \\ 0 \\ 0\end{bmatrix} \right\}$

#### Example
Determine whether $w$ is a subspace of $\mathbb{R}^{2}$
#### $$w = \left\{ \vec{x} = \begin{bmatrix}
3t \\
2 + 5t
\end{bmatrix} : t \in \mathbb{R} \right\}$$
For this, it is not a subspace, since $\vec{0}$ does not exist. 
#### $$\begin{bmatrix}
3t \\
2 + 5t
\end{bmatrix} = \begin{bmatrix}
0 \\
0
\end{bmatrix}$$
Geometrically, $w$ represents all points on some line that goes through $\begin{bmatrix}0 \\ 2\end{bmatrix}$ with direction vector $\begin{bmatrix}3 \\ 5\end{bmatrix}$. In this form, it shows that the line does not go through the origin, which is what $\vec{0}$ represents. In another way, the vector can be parameterized
#### $$\begin{array}{}
x = 3t \\
y = 2 + 5t
\end{array} \implies t = \frac{x}{3} \implies y = 2 + \frac{5}{3}x$$

#### Example
Determine whether $w$ is a subspace of $\mathbb{R}^{2}$
#### $$w = \left\{ \vec{x} \in \mathbb{R}^{2} : \vec{x} = \begin{bmatrix}
x_{1} \\
0
\end{bmatrix}, x_{1} \in \mathbb{R} \right\}$$
$\vec{0}$ is in $w$, since $x_{1} = 0$ would result in $\vec{x} = \begin{bmatrix}0 \\ 0\end{bmatrix}$. Checking for $\vec{x} + \vec{y} \in w$ is done by replacing variables.
#### $$\vec{x} + \vec{y} = \begin{bmatrix}
x_{1} \\
0
\end{bmatrix} + \begin{bmatrix}
y_{1} \\
0
\end{bmatrix} = \begin{bmatrix}
x_{1} + y_{1} \\
0
\end{bmatrix}$$
Since $x_{1} + y_{1} \in w$, the second property is satisfied. For the third condition, let $\vec{x} + w$ and $a \in \mathbb{R}$, then 
#### $$a\vec{x} = \vec{a} \begin{bmatrix}
x_{1} \\
0
\end{bmatrix} = \begin{bmatrix}
ax_{1} \\
0
\end{bmatrix} \in w$$
since $x_{1} \in \mathbb{R}$ and $a \in \mathbb{R}$. Since $w$ satisfies all 3 conditions, $w$ is a subspace of $\mathbb{R}^{2}$. Here, $w$ represents the x-axis, or in otherwords, the line through the origin with direction vector $\begin{bmatrix}1 \\ 0\end{bmatrix}$ since $\vec{x} = x_{1}\begin{bmatrix}1 \\ 0\end{bmatrix}$. 

#### Example
Determine whether $w$ is a subspace of $\mathbb{R}^{3}$
#### $$w = \left\{ \vec{x} \in \mathbb{R}^{3} : x_{1} = 2x_{2}, x_{3} = x_{1} \right\}$$
Constructing an $x$ vector is the first step
#### $$\vec{x} = \begin{bmatrix}
x_{1} \\
x_{2} \\
x_{3}
\end{bmatrix} = \begin{bmatrix}
2x_{2} \\
x_{2} \\
2x_{2}
\end{bmatrix} = x_{2}\begin{bmatrix}
2 \\
1 \\
2
\end{bmatrix}, x_{2} \in \mathbb{R}$$
$x_{2} = 0$ means that $\vec{x} = \begin{bmatrix}0 \\ 0 \\ 0\end{bmatrix}$, which is $\vec{0} \in w$. Checking closure under vector addition is next
#### $$\vec{x} + \vec{y} = \begin{bmatrix}
x_{1} \\
x_{2} \\
x_{2}
\end{bmatrix} + \begin{bmatrix}
y_{1} \\
y_{2} \\
y_{3}
\end{bmatrix} = \begin{bmatrix}
2x_{1} + 2y_{1} \\
x_{2} + y_{2} \\
2x_{3} + 2y_{3}
\end{bmatrix}$$
Since they are all in $\mathbb{R}$, $\vec{x} + \vec{y} \in w$. Testing closure under vector multiplication is last. For some $a \in \mathbb{R}$,
#### $$a\vec{x} = \vec{a}\begin{bmatrix}
2x_{2} \\
x_{2} \\
2x_{2}
\end{bmatrix} = \begin{bmatrix}
2ax_{2} \\
ax_{2} \\
2ax_{2}
\end{bmatrix} \in w$$
since $x_{2} \in \mathbb{R}$ and $a \in \mathbb{R}$, so $a\vec{x} \in \mathbb{R}$. In conclusion, $w$ is a subspace of $\mathbb{R}^{3}$. Geometrically, $w$ is a line through the origin with direction vector $\begin{bmatrix}2 \\ 1 \\ 2\end{bmatrix}$. 

#### Example
Determine whether $w$ is a subspace of $\mathbb{R}^{3}$
#### $$w = \left\{ \vec{x} \in \mathbb{R}^{3} : \vec{x} = \begin{bmatrix}
x_{1} \\
0 \\
x_{3}
\end{bmatrix} : x_{1} = x_{3} \text{  or  } x_{1} = -x_{3} \right\}$$
#### Example
Let $a \in \mathbb{R}^{3}$, $W \in \mathbb{R}^{3}$ means $W = \{ x : a^{T}x = 0 \}$
#### $$a = \begin{bmatrix}
α \\
β \\
γ
\end{bmatrix}$$
#### $$x = \begin{bmatrix}
0 \\
0 \\
0
\end{bmatrix}$$
#### $$ax = α * 0 + β * 0 + γ * 0 = 0$$
Hence, the zero vector is in $W$. 
#### $$\begin{bmatrix}
a \\
b \\
c
\end{bmatrix} = \begin{bmatrix}
a & b & c
\end{bmatrix}$$
Create two more column vectors
#### $$x = \begin{bmatrix}
t \\
w \\
v
\end{bmatrix},\ \ \ \ y = \begin{bmatrix}
i \\
j \\
k
\end{bmatrix}$$
Suppose that for these two vectors, $x, y \in W$. That means $a^{T}x = a^{T}y = 0$. The transpose are also 0, $a^{T}(x + y) = 0$.  Hence, $x + y \in W$. 
So multiplication of them are
#### $$\begin{bmatrix}
a & b & c
\end{bmatrix}\begin{bmatrix}
a \\
b \\
c
\end{bmatrix} = a^{2} + b^{2} + c^{2}$$


## Span
If some collection of vectors $S = \{ \vec{v_{1}}, \vec{v_{2}}, \dots, \vec{v_{r}} \}$ is a subset of $\mathbb{R}^{n}$, then the *span* of $S$ is the the set of all linear combinations of $\vec{v_{1}}, \vec{v_{2}}, \dots, \vec{v_{r}}$. In other words, 
#### $$Sp(s) = \{ \vec{x} \in \mathbb{R}^{n} : \vec{x} = a_{1}\vec{v_{1}} + a_{2}\vec{v_{2}} + \dots + a_{r}\vec{v_{r}}, a_{1}, a_{2}, \dots, a_{{r}} \in \mathbb{R} \}$$
If all vectors are in the vector space, then that means the span is also a subspace of $\mathbb{R}^{n}$. For s single vector $\vec{v} \in \mathbb{R}^{n}$, the span is the subset $Sp(\vec{v}) = \{ t\vec{v} : t \in \mathbb{R} \}$. If $\vec{v}$ is in $\mathbb{R}^{2}$ or $\mathbb{R}^{3}$, then the span is the line through the origin as determined by $\vec{v}$. 
#### Example
Show that $w$ is a subspace of $\mathbb{R}^{3}$
#### $$w = \{ \vec{x} \in \mathbb{R}^{3} : x_{1} = x_{2} = x_{3} \}$$
$\vec{x}$ must be in $w$, and it is equivalent to the column vector comprising of all 3 variables. And since all three variables are equivalent to each other
#### $$\vec{x} \in w \implies \vec{x} = \begin{bmatrix}
x_{1} \\
x_{1} \\
x_{2}
\end{bmatrix} = x_{1}\begin{bmatrix}
1 \\
1 \\
1
\end{bmatrix}$$
w must be some span of $\vec{x}$
#### $$w = Sp\left\{ \begin{bmatrix}
1 \\
1 \\
1
\end{bmatrix} \right\}$$
Hence, $w$ is a subspace of $\mathbb{R}^{3}$. 

#### Example
Is $\begin{bmatrix}-2 \\ 3\end{bmatrix}$ in $Sp\{ \vec{v_{1}}, \vec{v_{2}} \}$ for the given $\vec{v_{1}}$ and $\vec{v_{2}}$?
#### $$\vec{v_{1}} = \begin{bmatrix}
1 \\
-1
\end{bmatrix},\ \ \vec{v_{2}} = \begin{bmatrix}
-2 \\
2
\end{bmatrix}$$
The way to solve this is to rewrite the system as a coefficient matrix and constants
#### $$s \begin{bmatrix}
1 \\
-1
\end{bmatrix} + t \begin{bmatrix}
-2 \\
2
\end{bmatrix} = \begin{bmatrix}
-2 \\
3
\end{bmatrix} \implies \begin{bmatrix}
1 & -2 \\
-1 & 2
\end{bmatrix}\begin{bmatrix}
s \\
t
\end{bmatrix} = \begin{bmatrix}
-2 \\
3
\end{bmatrix}$$
This is the same as solving an augmented matrix
#### $$ \left[ \begin{array}{c c | c}
1 & -2 & -2 \\
-1 & 2 & 3
\end{array} \right] \longrightarrow \text{EROs} \longrightarrow \left[ \begin{array}{c c | c}
1 & -2 & -2 \\
0 & 0 & 1
\end{array} \right] $$
Since the augmented matrix shows that this is an inconsistent system, there's no solution $s$ and $t$ that would have $\begin{bmatrix}-2 \\ 3\end{bmatrix}$ be the span of the set of vectors. One thing to notice is that the two vectors are scalar multiples of each other, so only movement along the line drawn by the two vectors is possible.

#### Example
Is $\begin{bmatrix}-2 \\ 3\end{bmatrix}$ in $Sp\{ \vec{v_{1}}, \vec{v_{2}} \}$ for the given $\vec{v_{1}}$ and $\vec{v_{2}}$?
#### $$\vec{v_{1}} = \begin{bmatrix}
1 \\
1
\end{bmatrix},\ \ \vec{v_{2}} = \begin{bmatrix}
2 \\
0
\end{bmatrix}$$
Same thing, separate between coefficient matrix and constants to create an augmented matrix
#### $$s\begin{bmatrix}
1 \\
1
\end{bmatrix} + t\begin{bmatrix}
2 \\
0
\end{bmatrix} = \begin{bmatrix}
-2 \\
3
\end{bmatrix} \implies \left[ \begin{array}{c c | c}
1 & 2  & -2 \\
1 & 0 & 3
\end{array} \right] $$

EROs would transform this into a row reduced form
#### $$ \left[ \begin{array}{c c | c}
1 & 2 & -2 \\
1 & 0 & 3
\end{array} \right] \longrightarrow \text{EROs} \longrightarrow \left[ \begin{array}{c c | c}
1 & 0 & 3 \\
0 & 1 & -\frac{5}{2}
\end{array} \right] $$
Which results in the unique solution
#### $$\begin{array}{}
s = 3 \\
t = -\frac{5}{2}
\end{array}$$
Or in vector form
#### $$\vec{x} = \begin{bmatrix}
s \\
t
\end{bmatrix} = \begin{bmatrix}
3 \\
-\frac{5}{2}
\end{bmatrix}$$
The resulting span would be
#### $$3\begin{bmatrix}
1 \\
1
\end{bmatrix} - \frac{5}{2}\begin{bmatrix}
2 \\
0
\end{bmatrix} = \begin{bmatrix}
-2 \\
3
\end{bmatrix} \implies \begin{bmatrix}
-2 \\
3
\end{bmatrix} \in Sp\{ \vec{v_{1}}, \vec{v_{2}} \}$$
$\vec{v_{1}}$ and $\vec{v_{2}}$ are linearly independent, so the matrix is nonsingular. 

## Nullspace
Nullspace, or kernel, of a matrix $A$ is the set of vectors in $\mathbb{R}^{n}$ denoted as $N(A)$. The definition is 
#### $$N(A) = \{ \vec{x} \in \mathbb{R}^{n} : A\vec{x} = \vec{0} \}$$
The central idea is that if $A$ is an $(m \times n)$ matrix, then $N(A)$ is a subspace of $R^{n}$. To check if a single vector is a nullspace of $A$, check if $A\vec{x} = \vec{0}$. 
#### Example
Describe $N(A)$ for the matrix $A$
#### $$A = \begin{bmatrix}
1 & 1 & 3 & 1 & 6 \\
2 & -1 & 0 & 1 & -1 \\
-3 & 2 & 1 & -2 & 1 \\
4 & 1 & 6 & 1 & 4
\end{bmatrix}$$
Solve $A\vec{x} = [A | \vec{0}] \longrightarrow \text{EROs} \longrightarrow [R | \vec{0}]$
#### $$[A | \vec{0}] = \begin{bmatrix}
1 & 1 & 3 & 1 & 6 \\
2 & -1 & 0 & 1 & -1 \\
-3 & 2 & 1 & -2 & 1 \\
4 & 1 & 6 & 1 & 4
\end{bmatrix} \longrightarrow \text{EROs} \longrightarrow \left[ \begin{array}{c c c c c | c}
1 & 0 & 1 & 0 & -1 & 0 \\
0 & 1 & 2 & 0 & 3 & 0 \\
0 & 0 & 0 & 1 & 4 & 0 \\
0 & 0 & 0 & 0 & 0 & 0
\end{array} \right]$$
This can be converted to the system
#### $$\begin{array}{}
x_{1} + x_{3} - x_{5} = 0 \\
x_{2} + 2x_{3} + 3x_{5} = 0 \\
x_{4} + 4x_{5} = 0
\end{array} \implies \begin{array}{}
x_{1} = -x_{3} + x_{5} \\
x_{2} = -2x_{3} - 3x_{5} \\
x_{3} = x_{3} \\
x_{4} = -4x_{5} \\
x_{5} = x_{5}
\end{array} \implies \vec{x} = x_{2}\begin{bmatrix}
-1 \\
-2 \\
1 \\
0 \\
0
\end{bmatrix} + x_{5}\begin{bmatrix}
1 \\
-3 \\
0 \\
-4 \\
1
\end{bmatrix}$$
This must mean that the nullspace of $A$ is the span of the two vectors, hence it is a subspace. 
#### $$N(A) = Sp\left\{ \begin{bmatrix}
-1 \\
-2 \\
1 \\
0 \\
0
\end{bmatrix}, \begin{bmatrix}
1 \\
-3 \\
0 \\
-4 \\
1
\end{bmatrix} \right\}$$
The algebraic specification for this description would be 
#### $$N(A) = \left\{ \vec{x} \in \mathbb{R}^{5} : \vec{x} = x_{2}\begin{bmatrix}
-1 \\
-2 \\
1 \\
0 \\
0
\end{bmatrix} + x_{5}\begin{bmatrix}
1 \\
-3 \\
0 \\
-4 \\
1
\end{bmatrix}, x_{3}, x_{5}, \in \mathbb{R} \right\}$$

## Range
The range of a matrix $A$ is the set of vectors in $\mathbb{R}^{m}$, denoted as $R(A)$. It is defined as
#### $$R(A) = \{ \vec{b} \in \mathbb{R}^{m} : A\vec{x} = \vec{b}, \vec{x} \in \mathbb{R}^{n} \}$$
The range of is also called the column space of $A$, denoted as $col(A)$. Knowing that $A\vec{x} = \vec{b}$, if $A$ is a $(m \times n)$ matrix, then the range is a subspace of $\mathbb{R}^{m}$. 
#### Example
Describe $R(A)$ for the matrix $A$
#### $$A = \begin{bmatrix}
1 & 3 & -1 \\
1 & 2 & 0 \\
3 & 7 & -1
\end{bmatrix}$$
The span of a set of vectors would be 
#### $$R(A) = Sp\left\{ \begin{bmatrix}
1 \\
1 \\
3
\end{bmatrix}, \begin{bmatrix}
3 \\
3 \\
7
\end{bmatrix}, \begin{bmatrix}
-1 \\
0 \\
-1
\end{bmatrix} \right\}$$
And as a set of linearly independent vectors, this would require EROs
#### $$ \left[ \begin{array}{c c c | c}
1 & 3 & -1 & b_{1} \\
1 & 2 & 0 & b_{2} \\
3 & 7 & -1 & b_{3}
\end{array} \right] \longrightarrow \text{EROs} \longrightarrow \left[ \begin{array}{c c c | c}
1 & 0 & 2 & -2b_{1} + 3b_{2} \\
0 & 1 & -1 & b_{1} - b_{2} \\
0 & 0 & 0 & -b_{1} - 2b_{2} + b_{3}
\end{array} \right]$$
In order for this system to be consistent, $-b_{1} - 2b_{2} + b_{3}$ must be equal to 0. This means $b_{3} = b_{1} + 2b_{2}$. And since $b_{1}$ is arbitrary, this defines both $b_{2}$ and $b_{3}$ in terms of $b_{1}$
#### $$\begin{array}{}
b_{1} = b_{1} \\
b_{2} = b_{2} \\
b_{3} = b_{1} + 2b_{2}
\end{array} \implies \vec{b} = \begin{bmatrix}
b_{1} \\
b_{2} \\
b_{3}
\end{bmatrix} = \begin{bmatrix}
b_{1} \\
b_{2} \\
b_{1} + b_{2}
\end{bmatrix} = b_{1}\begin{bmatrix}
1 \\
0 \\
1
\end{bmatrix} + b_{2}\begin{bmatrix}
0 \\
1 \\
2
\end{bmatrix}$$
Hence, the range can be defined as the span of $b_{3}$
#### $$R(A) = col(A) = Sp\left\{ \begin{bmatrix}
1 \\
0 \\
1
\end{bmatrix}, \begin{bmatrix}
0 \\
1 \\
2
\end{bmatrix} \right\}$$

## Rowspace
