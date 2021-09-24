---
layout: post
title: Introduction To Math And Calculus
date: 210907
---
#  Introduction
## Introduction To Math 

Introduction to Math (IM) will teach you bascis in set theory, logic, combinatorics, precise formulation of statments, logical reasonaing and construction of mathematical proofs.
All these concepts will be vital in future courses!
 
Course plan:
 - week 1 - Sets and Logic
 - week 2 - Proofs
 - week 3 - Combinatorics

By the end of the course, you should be able to:
 - work with elemetary properties of sets and lgoic
 - construct elemetary proofs using basic techiques
 - work with elemetary properties of combinatorics

## Exam Rules
There will be two midterm tests:
 - IM (1h)
 - Calculus (2h)
These tests will be independet, but you should still have the prior knowledge.
No notes and electronic devices.

In the 10th week there will be an exam from all material. 

You will have to complete and pass a case study assignment to pass the course (there is some option to repair).

See [canvas page](https://canvas.utwente.nl/courses/9008/pages/intromath-description-topics-educational-targets-examination-rules?module_item_id=257997) for more detail.

#  Sets
Set is a well-defined **unordered** collection of **distinct** elements.
It is denoted within curly brcktes in one of these ways:
 - list of all elemets $\\{1,2,3,4,5,6\\}$
 - pattern $\\{1,2,3...6\\}$
 - properties $\\{ n\|n \in \mathbb{N}; 1 \leq n \leq 9 \\}$
 - intervals $\\{x \in \mathbb{R}; A \leq x < B \\} \leftrightarrow [A,B)$

Notation:
 - $1$ is an element of set $S$: $1 \in S$
 - $1$ is not an element of set $S$: $1 \notin S$
 - $S$ owns $1$: $S \ni 1$
 - $\\{1, 2\\}$ is a subset of $\\{1,2,3\\}$: $\\{1,2\\} \subseteq \\{1,2,3\\}$
 - $\\{1, 2\\}$ is a proper subset of $\\{1,2,3\\}$: $\\{1,2\\} \subset \\{1,2,3\\}$
 - empty set: $\emptyset$

Operations:
 - set union: $\cup$
 - set intersection: $\cap$
 - difference (order must be given by parentheses): $\setminus$
 - complement of $S$ with respect to universal set: $\overline{S} = U \setminus S$
 - cardinality (the number of elements) of $S$: $\|S\|$

Minimum of the set: $min(S) = s \in S \leftrightarrow \forall x \in S:s \leq x$ 
Infimum of the set: $inf(S) = max(\\{i; \forall x \in S: i \leq x\\})$ 
Maximum of the set: $max(S) = s \in S \leftrightarrow \forall x \in S:s \geq x$ 
Supremum of the set: $sup(S) = min(\\{s; \forall x \in S: s \geq x\\})$ 

You can use membership tables to construct Venn Diagrams.

Summation is denoted in the following manner:

$$ 1+2+3+4...n = \sum_{i=1}^n i $$ 

In a similiar manner, repeated union:

$$ A_1 \cup A_2 \cup A_3 \leftrightarrow \bigcup_{i=1}^3 A_i $$

## Sets of numbers
 - natural numbers: $\mathbb{N}$
 - integers: $\mathbb{Z}$
 - rational numbers: $\mathbb{Q}$
 - real numbers: $\mathbb{R}$

[See Canvas](https://canvas.utwente.nl/courses/9008/pages/micro-lectures-week-1) for the microlectures. 

# Logic
Proposition is a statement whose truth can be objectivelly determined as either 'true' or 'false'.

Predicate is a statement that can contain variables that inflence its truth value.

Tautology is a statement that is always true.  
Contradiction is a statement that is always false.

Operators:
 - and: $\land$
 - or: $\lor$
 - not: $\neg$
 - implication: $\rightarrow$
 - logical implication: $\Rightarrow$
 - equivalence: $\leftrightarrow$
 - logical equivalence: $\Leftrightarrow$
 - for all: $\forall$
 - exists: $\exists$
 
You can use truth tables to determine equivalency.

# Proofs 
**Lemma** is and intermidiary result.

Conditional statement $p \rightarrow q$ has converse statement $q \rightarrow p$.

## Proof techniques
 1. proof by example
    - prepositions starting with $\exists$ can be proved by an example  
    - prepositions starting with $\forall$ can be disproved by a counter-example
 2. proof by cases
 3. proof by contradiction
 4. mathematical induction
    - we are proving a predicate $S(n);n\in \mathbb N$
    - basis step: $S(0)$ is true
    - induction hypothesis: $\exists k; S(k)$ is true
    - induction step: we prove, that given induction hypothesis, $S(n+1)$ also holds
    - $S(1) \land (S(n) \rightarrow S(n+1)) \Rightarrow S(n) \forall n \in \mathbb{N}$
    - conclusion


# Counting
**Heuristic** is a non-perfect model with trade off between optimality and speed.

**Permutation** of $n$ objects is their possible ordering. The number of 
permutations of $k$ objects out of a set of $n$ objects is 
$P(n, k) = \frac{n!}{(n-r)!}$.

**Combination** of $n$ distinct elements is an unordered subset of $r$ elements,
where $0 \leq r \leq n$. It is: 

$$C(n, r) = \begin{pmatrix} n \\ r \end{pmatrix} = = \frac {P(n,r)} {r!} = \frac {n!} {r!*(n-r)!}$$

## Sum Rule
If $A$ and $B$ are finite **disjoint** ($A \cap B = \emptyset$) sets, then $|A \cup B| = |A| + |B|$.


## Principle of of inclusion exclusion
If $A$ and $B$ are not disjoint $|A \cup B| = |A| + |B| \ |A \cap B|$.


## Product Rule
If $A$ and $B$ are finite sets there are $|A| * |B|$ pairs $(a, b); a \in A, b \in B$

## Newton's binomial theorem

$$ (x+y)^n = \sum_{i=0}^n \begin{pmatrix} n \\ i \end{pmatrix} x^i y^{n-i} $$
