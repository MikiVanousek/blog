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

- scalar multiplicstion:
$$ xA =
\begin{pmatrix}
 xa_{11} & xa_{12} \\
 xa_{21} & xa_{22} \\
\end{pmatrix}$$

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

## Vector spaces
A vector space is made up of a set $V$ over field $F$ and 2 operations:
 - vector addition (VA): $\forall u, v \in V: u+v \in V$
 - scalar multiplication (SM): $\forall u \in V: c\in F, cu \in V$  

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

## Polynomials in $P_n(\mathbb R)$
A polynomail of degree $n$ with coefficients $a_0, a_1 ... + a_n \in \mathbb R$:

$$ f(x) = a_n x^n + a_{n-1} x^{n-1} ... a_0$$
$$ a \neq 0$$

Degree of $0$ is $-1$.

Set of all polynomials is a vector space.