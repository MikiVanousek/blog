---
layout: post
title: Linear Structures 1
date: 210907
---
#  Pólya's 4 Steps for problem-solving
 1. Getting Started
  - state the important information and summarize the problem
  - include diagram if possible
  - try to note all your assumptions
 2. Devise Plan
  - before trying to solve the problem, try to break it down into smaller pieces
 3. Execute Plan
  - explain each step
 4. Evaluate Solution
  - is the solution intuitive?
  - did you use all assumptions? what for?
  

#  Linear Algebra
## Vector in $\mathbb{R}^n$
They have n elements.
They can be represented:
 - row vector $u = (x_1, x_2...x_n)$
 - column vector $$u = \begin{pmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{pmatrix}$$
 - their geometric representation

Multidimensional vectors are used to store complex information.

Operations:
 - addition: $u + v = (u_1 + v_1, u_2 + v_2 ... u_n + v_n)$
 - scalar multiplication: $tu = (tu_1 + tu_2 ... tu_n)$
  - is the solution intuitive?
  - did you use all assumptions? what for?
  

#  Linear Algebra
## Vector in $\mathbb{R}^n$
They have n elements.
They can be represented:
 - row vector $u = (x_1, x_2...x_n)$
 - column vector $$u = \begin{pmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{pmatrix}$$
 - their geometric representation

Multidimensional vectors are used to store complex information.

Operations:
 - addition: $u + v = (u_1 + v_1, u_2 + v_2 ... u_n + v_n)$
  - is the solution intuitive?
  - did you use all assumptions? what for?
  

#  Linear Algebra
## Vector in $\mathbb{R}^n$
They have n elemets.
They can be represented:
 - row vector $u = (x_1, x_2...x_n)$
 - column vector $$u = \begin{pmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{pmatrix}$$
 - their geometric representation

Multidimensional vecotrs are used to store complex information.

Operations:
 - addition: $u + v = (u_1 + v_1, u_2 + v_2 ... u_n + v_n)$
  
Zero vector consists of all 0.

## Matrix in $M_{m\times n}(\mathbb{R})$
A rectangular $m \times n$ matrix $A$ consists of $m$ rows and $n$ columns.

$$ A = \begin{pmatrix} 
 a_{11} & ... & a_{1j} & ... & a_{1n} \\
 \vdots &     & \vdots &     & \vdots \\
 a_{i1} & ... & a_{ij} & ... & a_{in} \\
 \vdots &     & \vdots &     & \vdots \\
 a_{m1} & ... & a_{mj} & ... & a_{mn} \\
\end{pmatrix}
$$

Operations:
 - addition ($A$ and $B$ must have the same dimension!):

$$ A + B = \begin{pmatrix} 
 a_{11}+b_{11} & a_{12}+b_{12}  \\
 a_{21}+b_{21} & a_{22}+b_{22}  \\
\end{pmatrix} $$

- scalar multiplications:

$$ xA =
\begin{pmatrix}
 xa_{11} & xa_{12} \\
 xa_{21} & xa_{22} \\
\end{pmatrix}$$

- transpose $m \times n$ matrix $A$

$$ (A^t)_{ij} = A_{ji} $$

   - (aA + bB)^T = aA^t + bB^t

**Symmetric matrix** is a matrix A such that $A^t = A \Leftrightarrow A_{ij} = A_{ji}$

**Diagonal matrix** is a matrix where $A_{ij} = 0 \forall i \neq j$ 

**Trace** of an $n \times n$ matrix $A$: $tr(A) = \sum_{i=1}^n A_{ii}$

## Fields
Field is a set for which addition and multiplication are defined, so that for:
 - $\forall x,y \in F: x+y \in F, xy \in F$
 - $\forall a,b,c \in S$ all the the following properties must hold:
   1. commutativity of A,M:   
    $a+b = b+a$ and $a \cdot b = b \cdot a$
   2. associativity of addition, multiplication (A,M): 
    $(a+b) +c = a+(b+c)$ and $(ab)c = a(bc)$
   3. identity A,M:  
    $a+0 = a$ and $1a=a$
   4. inverse of A,M:  
    $a+(-a)=0$ and $\forall a \neq 0 \exists aa^{-1}=1$
   5. distributivity of multiplication over adition: 
    $a(b+c) = ab + ac$

## Polynomials in $P_n(\mathbb R)$
A polynomail of degree $n$ with coefficients $a_0, a_1 ... + a_n \in \mathbb R$:

$$ f(x) = a_n x^n + a_{n-1} x^{n-1} ... a_0$$
$$ a \neq 0$$

Degree of $0$ is $-1$.

Set of all polynomials is a vector space.

## Vector spaces
A vector space (VS) is made up of a set $V$ over field $F$ and 2 operations:
 - vector addition (VA): $\forall u, v \in V: u+v \in V$
 - scalar multiplication (SM): $\forall u \in V: c\in F, cu \in V$  
We say $V$ is closed with respekt to VA and SM.

All of the following properties must hold $\forall u,v,w \in V; a,b\in F$:
 1. commutativity of VA:  
  $u+v = v+u$
 2. associativity of VA:  
  $u +(v+w) = (u+v)+w$
 3. identity element of VA:  
  $0 + v=v$
 4. inverse element of VA:  
  $v + (-v) = 0$
 5. compatibility of SM with field multiplication:  
  $a(bv) = (ab)v$
 6. identity element of SM:  
  $1v=v$
 7. distributivity of SM with respect ot VA:  
  $a(u+w) = au + av$
 8. distributivity of SM with respect to field addition:  
  $(a+b)u = au + bu$

## Subspaces
If $V$ is a VS over $F$, $W \subset V$ is a subspace if $W$ is a VS with VA and SM defined
as in $V$.
These conditions must hold $\forall x, y \in W, c \in F:
 - a.  $0 \in W$
 - b. $x+y \in W$
 - c. $ cx \in W$

## Linear systems
You can represent systems of $n$ linear equations with $n$ variables as a $n\times
n$ matrix:

$$
\begin{array}{c c c}
1a_1 &+3a_2 &-5a_3 &=1\\
0a_1 &+1a_2 &+2a_3 &=0\\
4a_1 &-3a_2 &-5a_3 &=2\\
\end{array}
\qquad
\begin{bmatrix}
1 & 2 & 5 & 1\\
0 & 1 & 2 & 0\\
4 &-3 &-5 & 2\\
\end{bmatrix}
$$

Elementary operations (the solution of the linear system represented by the matrix does not change):
 - **interchange** 2 rows
 - **multiply** a row by non-zero value
 - **replace** a row with sum of itself and a multiple of another row

### Gausian elimination
 - in the leftmost non-zero column pick a pivot $p$
 - place row where the pivot is in the upper-most position that did not have a pivot yet
 - multiply the row by $\frac 1 p$ so the pivot becomes $1$
 - use pivot to eliminate all entries in this column other than itself
 - repeat until you run out of pivots  
 We are left with a **cannonical form** of a matrix (staircase form).

## Linear combination of vectors
Let $V$ be a VS over $F$ and $S \subset V$. Then $v \in V$ is a linear combination of vectors in S, if:

$$
\exists u_1, u_2 ... u_n \in S; a_1, a_2 ... a_n \in F: \sum_{i=1}^n a_i u_i = v
$$

The equation of a plane through noncollinear points $A,B,C$: $x = A + s(B \setminus A) + t(C \setminus A); s, t \in \mathbb R$

In the special case when $A$ is zero (the plane is subspace of $R^3$): $x = sB + rC

### Span
Let $V$ be VS over $F$, $S \neq \emptyset, S \\subseteq V$. Then span of $S$ denoted $span(S)$ is
the set of all linear combinations of the vectors in $S$. 

By convention: $span(\emptyset) = \\{0\\}$

If $span(S)=P$ we say **$S$ generates $P$** 

## Linear dependence
Subset $S = \\{u_1...u_n\\}$ of VS $V$ is called linearly dependent
if there exist scalars $a_1 ... a_n$ **not all zero** such that:
$\sum a_i u_i = 0$.
This is equivalent to one of the vectors being a linear combination of the others.

Trivial representation of 0: $0 = \sum 0u_i$

Nontrivial representation of zero implies linear dependence.

If $0 \in S$, $S$ is linearly dependent.

If subset is not linearly dependent, it is linearly independent (trivial representation of zero is the only representation.
In any VS $\emptyset$ and $\\{u\\}$ are linearly independent.

If no proper subset of $S$ generates $S$, it must be linearly independent.


## Bases and dimension
If $S$ generates subspace $W$ and no subset of $S$ generates $W$,
then $S$ must be linearly independent. Every vector in $W$ can be represented as exactly one linear combination of vectors in $S$.

A basis $\beta$ of $V$ is a linearly independent set of vectors that generates V.

In $F^n$ the set of vectors $(1, 0...0), (0,1..0) ... (0,0...1)$ is called standard basis.

In $P_n(F)$ we call $\\{1, x, x^2...x^n\\}$ the standard basis.


### The Replacement Theorem
 Let $V$ be a VS generated by a set $G$ containing 
 exactly $n$ vectors, and let $L$ be a linearly independent 
 subset of $V$ containing exactly $m$ vectors. Then $m \leq n$
 and there exsist $H \subseteq G$ containing exactly $n-m$ vecotors
 such that $L \cup H$ generates $V$.


#### Corollaries
 - Let $V$ be a vecotr space having a finite basis. 
 Then every basis has the same number of vectors.
   - If the number of vectos in basis is finite, we call
   VS **finite-dimensional**. We call it **infinite-dimensional**
   if it does not have finite basis. 
   - The number of vectors in each basis of a finite-dimensional VS
   $V$ is called **dimension** and is denoted by $dim(V)$.
     - $dim(\\{0\\})=0$
 - Let $V$ be a VS with dimension $n$:
   - Any generating set for V contains at least $n$ vectors 
   and generating set for $v$ that contains exactly $n$ vectors 
   is a basis for $V$. 
   - Any linearly independent subset of $V$ that contains 
   exaclty $n$ vectos is a basis for $V$
   - Any linearly independent subset of $V$ can be extended to 
   a basis for $V$ 


### Other theorems
 - Let $V$ be a VS and $\beta \subseteq V$. 
 Then $\beta$ is a basis for V if on only if 
 each $v\in V$ can be uniquely expressed as 
 a linear combination of vectors of $\beta$. 
 - If a VS $V$ is generated by finite set $S$, 
 then some subset of $S$ is a basis for $V$.
 - Let $W$ be s subspace for finite dimensional VS $V$. 
 Then $dim(W) \leq dim(V)$ And $dim(V) = dim(W) \Leftrightarrow V = W$ 
   - Any basis for $W$ can be extended to basis for $V$.
