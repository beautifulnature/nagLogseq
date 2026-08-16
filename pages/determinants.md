- ![Class-12-1-Mathematics-Part-I-04_Determinants.pdf](../assets/Class-12-1-Mathematics-Part-I-04_Determinants_1786553152995_0.pdf)
- introduction
	- a system of linear equations like
	  $$
	  a_1 x + b_1 y = c_1 \\
	  a_2 x + b_2 y = c_2
	  $$ can be represented as
	  $$
	  \begin{bmatrix}
	  a_1 & b_1 \\
	  a_2 & b_2
	  \end{bmatrix}
	  \begin{bmatrix}
	  x \\
	  y
	  \end{bmatrix}
	  = 
	  \begin{bmatrix}
	  c_1 \\
	  c_2
	  \end{bmatrix}
	  $$
	- now, this system of equations has a unique solution or not, is determined by the number $a_1 b_2 - a_2 b_1$
	- if $\frac{a_1}{a_2} \neq \frac{b_1}{b_2}$ or $a_1 b_2 - a_2 b_1 \neq 0$, then the system of linear equations has a unique solution.
	- the number $a_1 b_2 - a_2 b_1$ which determines uniqueness of solution is associated with the matrix 
	  $$
	  \begin{bmatrix}
	  a_1 & b_1 \\
	  a_2 & b_2
	  \end{bmatrix}
	  $$ and is called the determinant of A or det A.
	- determinants have wide applications in engineering, science, economics, social science etc.
- determinant
	- definition
		- to every square matrix A = [a_{ij}] of order n, we can associate a number (real or complex) called determinant of the square matrix A, where a_{ij} = (i, j)^{th} element of A. this may be thought of as a function which associates each square matrix with a unique number (real or complex). if M is the set of square matrices, K is the set of numbers (real or complex) and f: M -> K is defined by f(A) = k, where A \in M and k \in K, then f(A) is called the determinant of A. it is also denoted by |A| or det A or \Delta
		- if A = 
		  $$
		  \begin{bmatrix}
		  a & b \\
		  c & d
		  \end{bmatrix}
		  $$, then determinant of A is written as |A| = 
		  $$
		  \begin{vmatrix}
		  a & b \\
		  c & d
		  \end{vmatrix} = det (A)
		  $$
		- for matrix A, |A| is read as determinant of A and not modulus of A
		- only square matrices have determinants
	- determinant of a matrix of order one
		- A = [a] be the matrix of order 1, then determinant of A is defined to be equal to a
	- determinant of a matrix of order two
		- $$
		  A = 
		  \begin{bmatrix}
		  a_{11} & a_{12} \\
		  a_{21} & a_{22}
		  \end{bmatrix}
		  $$ be a matrix of order 2 x 2
		- then the determinant of A is defined as
			- det(A) = |A| = \Delta = $a_{11}a_{22} - a_{21}a_{12}$
	- determinant of a matrix of order 3 x 3
- properties of determinants
- area of a triangle
- adjoint and inverse of a matrix
	- adjoint of a matrix
- application of determinants and matrices
	- solution of system of linear equations using inverse of a matrix