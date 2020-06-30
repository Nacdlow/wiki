# Golang Tutorial

This is a tutorial for Go, you'll need to have Go installed.
You can do this by using the package manager on your computer or by downloading
it from [Go's website](https://golang.org).  

-------

The only way to learn a programming language is to make a little project, no
one ever learns a language just by reading a book or watching an hour long
tutorial on YouTube.  

This is why this guide will not teach you how to write Go code, but will
suggest a couple of exercies you could do.


## Exercise 1: Project Euler

[Project Euler](https://projecteuler.net/) is a site which contains a series of
mathematical and computational problems which you can solve by writing a
program in any language. It can be fun and challenging.  

You have to register an account on the website so you can check your answers.

**Goal:** Write programs to solve the first 10 problems in Go.


## Exercise 2: Jamie is alive

In this exercise, we will do Jamie's coursework but in Go instead of ML/Python.

Since you have probably done them before, it should be simple especially when
using the old code as reference.

### 1. Complex number arithmetic

Implement a `cadd` and `cmult` function in Go, you can use the `complex	` 
type. These two functions should return type complex.

For example:
```go
comp := complex(1, -2) // this is 1+2i
fmt.Println(real(comp)) // this prints 1
```

### 2. Sequence arithmetic

Consider an integer array. Implement recursive functions `seqadd` and `seqmult`
which takes in `[]int` and returns `[]int`.

For instance:
```go
seqadd([]int{1,2,3},[]int{-1,2,2})
// returns []int{0,4,5}
```

*Note: Do not write error handling code.*

### 3. Matrices

Now the fun part! You should implement the following functions:

- `isMatrix([][]int) bool`: Whether the 2d array of integers represents a
	matrix (when the length of each row is equal).
- `matrixShape([][]int) (int, int)`: Should return two integers, the number of
	columns and number of rows (in that order).
- `matrixAdd([][]int, [][]int) [][]int`: Matrix addition, which is a simply
	a pointwise addition.
- **A challenge** `matrixMult([][]int, [][]int) [][]int`: Matrix
	multiplication.

**Helpful links:**  

- Matrix addition: <https://www.mathsisfun.com/algebra/matrix-introduction.html>
- Matrix multiplication: <https://www.mathsisfun.com/algebra/matrix-introduction.html>
