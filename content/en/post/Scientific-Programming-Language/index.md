---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Scientific Programming Language"
subtitle: ""
summary: "Some representation of Scientific Language"
authors: []
tags: [Scientific Posts]
categories: [Scientific Post]
date: 2022-05-22T13:11:32+03:00
lastmod: 2022-05-22T13:11:32+03:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

In computer programming, a scientific programming language can refer to two degrees of the same concept.

In a wide sense, a scientific programming language is a programming language that is used widely for computational science and computational mathematics. In this sense, C/C++ and Python[1] can be considered scientific programming languages.

In a stronger sense, a scientific programming language is one that is designed and optimized for the use of mathematical formula and matrices.[2] Such languages are characterized not only by the availability of libraries performing mathematical or scientific functions, but by the syntax of the language itself.[3] For example, neither C++ nor Python have built-in matrix types or functions for matrix arithmetic (addition, multiplication etc); instead, this functionality is made available through standard libraries. Scientific programming languages in the stronger sense include ALGOL, APL, Fortran, J, Julia, Maple, MATLAB and R.[4][5]

Scientific programming languages should not be confused with scientific language in general, which refers loosely to the higher standards in precision, correctness and concision expected from practitioners of the scientific method. 

## Examples

### Linear algebra

Scientific programming languages provide facilities to work with linear algebra. For example, the following Julia program solves a system of linear equations: 

```C++
A = rand(20, 20)  # A is a 20x20 matrix
b = rand(20)      # b is a 20-element vector
x = A\b           # x is the solution to A*x = 
```

Working with large vectors and matrices is a key feature of these languages, as linear algebra lays the foundation to mathematical optimization, which in turn enables major applications such as deep learning. 

### Mathematical optimization

In a scientific programming language, we can compute function optima with a syntax close to mathematical language. For instance, the following Julia code finds the minimum of the polynomial P(x,y) = x^2 - 3xy + 5y^2 - 7y + 3

```
using Optim

P(x,y) = x^2 - 3x*y + 5y^2 - 7y + 3

z₀ = [ 0.0
       0.0 ]     # starting point for optimization algorithm

optimize(z -> P(z...), z₀, Newton();
         autodiff = :forward)
```

In this example, Newton's method for minimizing is used. Modern scientific programming languages will use automatic differentiation to compute the gradients and Hessians of the function given as input; cf. differentiable programming. Here, automatic forward differentiation has been chosen for that task. Older scientific programming languages such as the venerable Fortran would require the programmer to pass, next to the function to be optimized, a function that computes the gradient, and a function that computes the Hessian.

With more knowledge of the function to be minimized, more efficient algorithms can be used. For instance, convex optimization provides faster computations when the function is convex, quadratic programming provides faster computations when the function is at most quadratic in its variables, and linear programming when the function is at most linear. 


