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
		- determinant of a matrix of order 3 can be determined by expressing it in terms of second order determinants. this is known as expansion of a determinant along a row (or a column). there are 6 ways of expanding a determinant of order 3 corresponding to each of 3 rows ($R_1, R_2$ and $R3$) and 3 columns ($C_1, C_2,$ and $C_3$) giving the same value as shown below.
		- consider the determinant of square matrix A = $[a_{ij}]_{3\times 3}$
		- i.e., |A| = 
		  $$
		  \begin{vmatrix}
		  a_{11} & a_{12} & a_{13} \\
		  a_{21} & a_{22} & a_{23} \\
		  a_{31} & a_{32} & a_{33}
		  \end{vmatrix}
		  $$
		- expansion along first row $R_1$
			- $(-1)^{1+1}\left[(-1)^{\text{sum of suffixes of }a_{11}}\right]$
			- $$
			  \left| A \right| = (-1)^{1+1} a_{11}
			  \begin{vmatrix}
			  a_{22} & a_{23} \\
			  a_{32} & a_{33}
			  \end{vmatrix} 
			  + (-1)^{1+2} a_{12}
			  \begin{vmatrix}
			  a_{21} & a_{23} \\
			  a_{31} & a_{33}
			  \end{vmatrix} 
			  + (-1)^{1+3} a_{13}
			  \begin{vmatrix}
			  a_{21} & a_{22} \\
			  a_{31} & a_{32}
			  \end{vmatrix}
			  $$
			  
			  $$
			  = a_{11}
			  \begin{vmatrix}
			  a_{22} & a_{23} \\
			  a_{32} & a_{33}
			  \end{vmatrix} 
			  - a_{12}
			  \begin{vmatrix}
			  a_{21} & a_{23} \\
			  a_{31} & a_{33}
			  \end{vmatrix} 
			  + a_{13}
			  \begin{vmatrix}
			  a_{21} & a_{22} \\
			  a_{31} & a_{32}
			  \end{vmatrix}
			  $$
	- remarks:
		- for easier calculations, we shall expand the determinant along that row or column which contains maximum number of zeros.
		- while expanding, instead of multiplying by (-1)^{i+j}, we can multiply by +1 or -1 according as (i + j) is even or odd
		- if A = kB where A and B are square matrices of order n, then |A| = k^n |B|, where n = 1, 2, 3
- properties of determinants
- area of a triangle
- adjoint and inverse of a matrix
	- adjoint of a matrix
- application of determinants and matrices
	- solution of system of linear equations using inverse of a matrix