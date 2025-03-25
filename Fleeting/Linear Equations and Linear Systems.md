20250308174157

Tags:

A linear equation is a set of coefficients and variables that equate to some constant. They always draw lines, since linear means to scale at a constant rate. 

## Formalism
#### Linear Equation
```ad-formula
#### General Form of a Linear Equation
A linear equation with $n$ unknowns typically takes some form 
#### $$a_{1}x_{1} + a_{2}x_{2} + \dots + a_{n}x_{n} = b$$
where $a_{1}$, $a_{2}$, $\dots$, $a_{n}$, and $b$ are constants and $x_{1}$, $x_{2}$, $\dots$, $x_{n}$ are variables.
```

When trying to solve many linear equations together, they are grouped together into a system of linear equations, or a linear system.

#### Linear System

```ad-formula
#### General Form of a Linear System
A linear system is typically in the form of a $(m \times n)$ system, possessing $m$ equations and $n$ variables. 
#### $$\begin{rcases}a_{11}x_{1} + a_{12}x_{2} + \dots + a_{1n}x_{n} = b_{1} \\ a_{21}x_{1} + a_{22}x_{2} + \dots + a_{2n}x_{n} = b_{2} \\ \vdots \\ a_{m1}x_{1} + a_{m2}x_{2} + \dots + a_{mn}x_{n} = b_{m} \end{rcases} \text{m equations}$$
$a_{ij}$ is the coefficient in the equation $i$ multiplying variable $j$.
```
A solution of a system can be written as a sequence of numbers $s_{1}, s_{2}, \dots, s_{n}$, which would make the system a true statement when substituted in for $x_{1}$, $x_{2}$, $\dots$, $x_{n}$. The set of all solutions is called the *solution set* of the linear system. Two linear systems are *equivalent* if they have the same solution set. 

## Methods of Solving
#### Substitution
The substitution method involves solving for one variable in one equation and then substituting into the other equation.
```ad-example
#### Substitution Example
For an system 
#### $$\begin{cases}2x - 4y = 14 \\ -x + 3y = -9\end{cases}$$
equation two can be solved first.
#### $$x = 3y + 9$$
This can then be substituted into equation 1
#### $$\begin{gather} 2(3y + 9) - 4y = 14 \\ 6y + 18  - 4y = 14 \\ 2y = -4 \\ y = -2 \end{gather}$$
Then, the solution for equation 1 can be plugged into equation 2
#### $$x = 3(-2) + 9 = 3$$
So the solution of this system is
#### $$\therefore (x, y) = (3, -2)$$
```

#### Elimination
The elimination method completely removes one variable and then solves for the remaining equation.
```ad-example
#### Elimination
For a system
#### $$\begin{cases}2x - 4y  = 14 \\ -x + 3y = -9\end{cases}$$
Multiply equation 2 by 2, and then add it to equation 1
#### $$\begin{cases}2x - 4y = 14 \\ -2x + 6y = -18\end{cases}$$
We would get the relationship
#### $$y = -2$$
Then it can be plugged into the other equation
#### $$-x + 3(-2) = -9 \implies x = 9 - 6 = 3$$
So the solution of this system is
#### $$\therefore (x, y) = (3, -2)$$
```

The solution to both of the system can be visualized with the following graph. There's only one solution for this system as the lines are not parallel nor are they incident.
```tikz
\begin{document}
  \begin{tikzpicture}[scale=1]
    \draw[thin] (-0.1,-4.1) grid (16,3);
    \draw[black, ->, very thick] (0,0) -- (16,0) node[right] {\Large $x$};
    \draw[black, ->, very thick] (0,-4) -- (0,3) node[above] {\Large $y$};
    \draw[green, domain=0:13, very thick] plot (\x,{0.5*\x - 3.5}) node[right] {\Large $2x - 4y = 14$};
    \draw[cyan, domain=0:16, very thick] plot (\x,{(1/3)*\x - 3}) node[right] {\Large $-2x + 6y = -17$};
    \filldraw[yellow] (3, -2) circle (4pt) node[right] {\Large $(x, y) = (3, -2)$};
  \end{tikzpicture}
\end{document}
```

#### Choosing Between the Two Methods
Substitution is quite straightforward, but when it comes to linear systems with more variables, it becomes more messy. Using elimination tends to be more systematic. 

## Possible Solutions of a Linear System
There are three possible solutions to a linear set of linear systems.
1. The system has infinitely many solutions (the two functions up perfectly, or are identical)
2. The system has no solution (the two functions are parallel to each other, or are factors of each other)
3. The system has a unique solution (the two functions intersect somewhere)
A system of linear equations is *consistent* if it has either one or infinitely many solutions. It is *inconsistent* if it has no solutions. 

## Three Variable System
A three variable system represents a plane instead of a line with two variable systems. For three variables ($\mathbb{R}^{3}$), there are two distinct types of system. 
#### 2 Planes
Two planes systems are represented as $(2 \times 3)$. 
```ad-formula
#### General Formula for 2 Plane 3 Variable System
#### $$\begin{cases} a_{11}x_{1} + a_{12}x_{2} + a_{13}x_{3} = b_{1} \\ a_{21}x_{1} + a_{22}x_{2} + a_{23}x_{3} = b_{2} \end{cases}$$
```

There are two possibilities for solutions.
1. The system has infinitely many solutions (the two planes are coincident or intersect in a line)
2. The system has no solution (the two planes are parallel)

#### 3 Planes
Three plane systems are represented as $(3 \times 3)$
```ad-formula
#### General Formula for a 3 Plane 3 Variable System
#### $$\begin{cases} a_{11}x_{1} + a_{12}x_{2} + a_{13}x_{3} = b_{1} \\ a_{21}x_{1} + a_{22}x_{2} + a_{23}x_{3} = b_{2} \\ a_{31}x_{1} + a_{32}x_{2} + a_{33}x_{3} = b_{3} \end{cases}$$
```

There are three possibilities for solutions
1. The system has infinitely many solutions (the three planes are coincident or intersect along a line)
2. The system has no solutions (the three planes are parallel to each other and don't have any points in common)
3. The system has a unique solution (the three planes intersect with each other along some line)
___
# References
[[MATH2010_1.1_1.2.pdf]]
