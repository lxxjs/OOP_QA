

2 0 2 2 O O P

Functional

Programming

In Class Talk

2020080172 李钟曙


\*

What is Functional Programming?



01

03

Introduction

Concepts of

Functional Programming

02 04

Background

Pros & Cons



\01.

Introduction



Programming Paradigm





Programming Paradigm

Procedural

Programming

**Imperative**

**Programming**

\# "How" to solve

Object-oriented

Programming (OOP)

**Declarative**

**Programming**

Functional

Programming (FP)

\# "What" to solve




Programming Paradigm

Functional Programming is programming

without assignment statements

\- Rober C.Martin -

(author of the book "Clean Code")






\02.

Background






01

Lambda Calculus

(λ-calculus)

\- Anything that can be computed by lambda calculus is computable

\- Equivalent to **Turing machine** in its ability to compute

\- Forms the basis of almost all current functional programming languages

Developed by **Alonzo Church** (1903 – 1995), a renowned American

mathematician, logician, philosopher, professor and editor

Fun fact : Alan Turing, who created Turing machine which laid the foundation of

imperative programming style, was a student of Alonzo Church






02

\- Elixir

\- OCaml

\- Idris

\- PureScript

\- Wolfram

\- Scala

\- Erlang

\- Common Lisp

\- Haskell

\- F#

\- Clojure

\- Elm

Functional

Programming

Languages

\- Python

\- Kotlin

\- Racket

\- JavaScript

...

The list of most popular functional programming languages and

languages that support programming in functional style or have

functional as well as OOP capabilities.




\03.

Concepts of

Functional

Programming




Main concepts of Functional Programming

01

Using std::function in C++11 :

First-class Functions

\- In Functional programming, functions are treated as **"First-class citizens"**

\- Passing as arguments to other functions, returning as the values from other

functions, and assigning to variables or storing in data structures are all

"**POSSIBLE"**




Main concepts of Functional Programming

02

Impure functions :

Pure function :

Pure Functions

\1) Always the same output for the same input

\2) No side effects or hidden I/O (Immutability)

i.e. they do not modify any arguments or local/global

streams

variables or input/output





Main concepts of Functional Programming

03

Referential

Transparency

Function rt( ) is **referentially transparant**,

while function ro( ) is **referentially opaque**.

If x == y,

rt(x) == rt(y).

However, ro(x) != ro(y)

since global variable g might change the output

\- Variable once defined do not change their values throughout the program

\- Eliminates any chances of side effects




Main concepts of Functional Programming

Variables are immutable

Impossible to modify a variable after it has been initialized

OOP makes it easy for us to manage state

In FP, we don't need to manage state !





\04.

Pros

& Cons




Pros and Cons of Functional Programming

Pros

Cons

Shorter code

01

02

03

You can write shorter codes with functional programming

Easy debugging

Pure functions don't have any hidden side effects

Parallel programming

It can implement parallelism because pure functions don’t change any variables






Comparison with OOP

"Evaluation of the functional and object-oriented programming paradigms: a replicated experiment"

(Samaraweera, L.G., Harrison, R., 1998)

**Process metrics :**

**Product metrics :**

• The number of known errors found during execution of the test scripts (KE• )T.he number of non-comment, non-blank source lines (NCSL).

• The time to fix the known errors (TKE).

• The number of modifications requested (MR) during

code reviews, testing and maintenance.

• The time to implement modifications (TMR).

• A subjective assessment of complexity (SC).

• Development Time and Testing Time.

• The number of distinct functions called, N\*,

• The number of distinct library functions called, L,

• The number of distinct domain-specific (image analysis)

functions called by the program, D, where D = N\* - L.

• The depth of the function call hierarchy chart [HSDL95].

• The number of function declarations, dec.

• The number of function definitions, def





Comparison with OOP

"Evaluation of the functional and object-oriented programming paradigms: a replicated experiment"

(Samaraweera, L.G., Harrison, R., 1998)

**Statistically significant differences :**

• TMR, 111 % more for C++

• NCSL, 66% more for C++

• N\*, 30% more for SML

• L, 525% more for SML

• the depth of the function hierarchy, 29% more for SML

• L/N\*, a measure of reuse, 377% more for SML.

Samaraweera, L.G., Harrison, R., 1998. Evaluation of the functional and object-oriented programming

paradigms. ACM SIGSOFT Software Engineering Notes 23, 38–43.. doi:10.1145/286366.286374.



THANK YOU !

2020080172 李钟曙

