﻿2022 OOP - In-class Talk - Functional Programming
================================================================
<p style='text-align: right;'> 2020080172 李钟曙 </p>

What is Functional Programming?
----------------------------------------------------------------

#### [01. Introduction](#01.-Introduction)

#### [02. Background](#02.-Background)

#### [03. Concepts of Functional Programming](#03.-Concepts-of-Functional-Programming)

#### [04. Pros & Cons](#04.-Pros-&-Cons)

****************************************************************

# 01. Introduction<a id="01.-Introduction"></a>

## Programming Paradigm

![Changing Programming Paradigm](https://user-images.githubusercontent.com/66354904/170830032-cd747044-c57a-4462-9b20-b671135373b8.png)

- Programming Paradigm
    - Imperative Programming (# "How" to solve)
        - Procedural Programming
        - Object-oriented Programming
    - Declaration Programming (# "What" to solve)
        - Functional Programming


> "Functional Programming is programming without assignment statements"   
> - Rober C.Martin, the author of the book "Clean Code"

****************************************************************

# 02. Background<a id="#02.-Background"></a>

## 01. Lambda Calculus (λ-calculus)

![Alonzo Church](https://user-images.githubusercontent.com/66354904/170830145-6f6b0b65-25cd-4fa0-afea-8ccf6747f718.png)

Developed by **Alonzo Church** (1903 – 1995), a renowned American mathematician, logician, philosopher, professor and editor

- Anything that can be computed by lambda calculus is computable
- Equivalent to **Turing machine** in its ability to compute
- Forms the basis of almost all current functional programming languages

> Fun fact : Alan Turing, who created Turing machine which laid the foundation of imperative programming style, was a student of Alonzo Church

## 02. Functional Programming Languages<a id=""></a>

The list of most popular functional programming languages and languages that support programming in functional style or have functional as well as OOP capabilities.

    - Elixir
    - OCaml
    - Idris
    - PureScript
    - Wolfram
    - Scala
    - Erlang
    - Common Lisp
    - Haskell
    - F#
    - Clojure
    - Elm
    - Python
    - Kotlin
    - Racket
    - JavaScript
    ...

*********************************

# 03. Concepts of Functional Programming<a id="03.-Concepts-of-Functional-Programming"></a>

## 01. First-class Functions

- In Functional programming, functions are treated as **"First-class citizens"**
- Passing as arguments to other functions, returning as the values from other functions, and assigning to variables or storing in data structures are all **"POSSIBLE"**

```cpp
//Using std::function in C++11 :
#include <iostream>
#include <functional>

auto twice = [](const std::function<int(int)>& f)
{
    return [&f](int x) {
        return f(f(x));
    };
};

auto plus_three = [](int i)
{
    return i + 3;
};

int main()
{
    auto g = twice(plus_three);

    std::cout << g(7) << '\n'; // 13
}
```
## 02. Pure Functions

- Always the same output for the same input
- No side effects or hidden I/O (Immutability)   i.e. they do not modify any arguments or local/global streams variables or input/output

Pure function :
```cpp
void f() {
    static std::atomic<unsigned int> x = 0;
    ++x;
}
```

Impure functions :
```cpp
int f() {
    return x;
}

void f(int* x) {
    ++*x;
}
```

## 03. Referential Transparency

- Variable once defined do not change their values throughout the program
- Eliminates any chances of side effects

```cpp
int g = 0;
int rt(int x) {
    return x + 1;
} 
// Function rt( ) is **referentially transparant**, while function ro( ) is **referentially opaque**.
int ro(int x) {
    g++;
    return x + g;
}
// If x == y, rt(x) == rt(y).
// However, ro(x) != ro(y) since global variable g might change the output
```

## Variables are immutable

    Impossible to modify a variable after it has been initialized

> OOP makes it easy for us to manage state   In FP, we don't need to manage state !

****************************************************************

# 04. Pros & Cons<a id="04.-Pros-&-Cons"></a>

| | Pros | Cons |
|:---:|:---:|:---:|
| 01 | Shorter code | Readability |
| 02 | Easy debugging | Difficulty |
| 03 | Parallel programming | Performance |

## Comparison with OOP

> "Evaluation of the functional and object-oriented programming paradigms: a replicated experiment"
> (Samaraweera, L.G., Harrison, R., 1998)

| **Process metrics :** | **Product metrics :** |
|:---:|:---:|
|• The number of known errors found during execution of the test scripts (KE).|• The number of non-comment, non-blank source lines (NCSL).|
|• The time to fix the known errors (TKE).|• The number of distinct functions called (N\*)|
|• The number of modifications requested (MR) during code reviews, testing and maintenance.|• The number of distinct library functions called (L)|
|• The time to implement modifications (TMR).|• The depth of the function call hierarchy chart.|
|• A subjective assessment of complexity (SC).|• The number of function declarations (dec)
|• Development Time and Testing Time.|• The number of function definitions (def)
| |• The number of distinct domain-specific (image analysis) functions called by the program, D, where D = N\* - L.|

    **Statistically significant differences :**

    • TMR, 111 % more for C++
    • NCSL, 66% more for C++
    • N\*, 30% more for SML
    • L, 525% more for SML
    • the depth of the function hierarchy, 29% more for SML
    • L/N\*, a measure of reuse, 377% more for SML.

>Samaraweera, L.G., Harrison, R., 1998. Evaluation of the functional and object-oriented programming paradigms. ACM SIGSOFT Software Engineering Notes 23, 38–43.. doi:10.1145/286366.286374.

*********************************

THANK YOU !

2020080172 李钟曙

