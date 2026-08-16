- ![Class-12-1-Mathematics-Part-I-03_Matrices.pdf](../assets/Class-12-1-Mathematics-Part-I-03_Matrices_1786553139087_0.pdf)
- matrix
	- definition
		- a `matrix` is an ordered rectangular array of numbers or functions. the numbers or functions are called the elements or the entries of the matrix.
		- matrices denoted by capital letters
			- example
				- $$
				  A = 
				  \begin{bmatrix}
				  1 & 2 \\
				  3 & 4
				  \end{bmatrix}
				  $$
		- horizontal lines of elements are said to constitute, rows of the matrix
		- vertical lines of elements are said to constitute, columns of the matrix
	- order of a matrix
		- a matrix having m rows and n columns is called a matrix of order m x n or simply m x n matrix (read as m by n matrix)
		- $$
		  A=[a_{ij}]_{m\times n}
		  =
		  \begin{pmatrix}
		  a_{11} & a_{12} & a_{13} & \cdots & a_{1n} \\
		  a_{21} & a_{22} & a_{23} & \cdots & a_{2n} \\
		  a_{31} & a_{32} & a_{33} & \cdots & a_{3n} \\
		  \vdots & \vdots & \vdots & \ddots & \vdots \\
		  a_{m1} & a_{m2} & a_{m3} & \cdots & a_{mn}
		  \end{pmatrix}
		  $$
		  or $A = [a_{ij}]_{m x n}, 1 \leq i\leq m, 1 \leq j \leq n, i, j \in N$
		- i^{th} row consists of the elements $a_{i1}, a_{i2}, a_{i3}, ..., a_{in}$, while the j^{th} column consists of the elements $a_{1j}, a_{2j}, a_{3j}, ..., a_{mj}$
		- in general, $a_{ij}$, is an element lying in the i^{th} row and j^{th} column. we can also call it as the (i, j)^{th} element.
		- the number of elements in an m x n matrix will be equal to mn
		- we shall follow the notation, namely $A=[a_{ij}]_{m\times n}$ to indicate that A is a matrix of order m x n
		- we shall consider only those matrices whose elements are real numbers or functions taking real values
		- we can also represent any point (x, y) in a plane by a matrix (column or row) as 
		  $$
		  \begin{bmatrix}
		  x \\
		  y
		  \end{bmatrix}
		  $$
		  or
		  $$
		  \begin{bmatrix}
		  0 & 1
		  \end{bmatrix}
		  $$
		- matrices can be used as representations of vertices of geometrical figures in a plane
- types of matrices
	- column matrix
		- a matrix is said to be a column matrix if it has only one column
		- in general, $A=[a_{ij}]_{m\times 1}$ is a column matrix of order m x 1
		- example
			- $$
			  A = 
			  \begin{bmatrix}
			  0 \\
			  \sqrt{3} \\
			  -1 \\
			  \frac{1}{2}
			  \end{bmatrix}
			  $$ is a column matrix of order 4 x 1
	- row matrix
		- a matrix is said to be a row matrix if it has only one row
		- in general, $B=[b_{ij}]_{1\times n}$ is a row matrix of order 1 x n
		- example
			- $$
			  B = 
			  \begin{bmatrix}
			  \frac{-1}{2} & \sqrt{5} & 2 & 3
			  \end{bmatrix}
			  $$
	- square matrix
		- a matrix in which the number of rows are equal to the number of columns, is said to be a square matrix. thus an m x n matrix is said to be a square matrix if m = n and is known as a square matrix of order n.
		- in general, $A=[a_{ij}]_{m\times n}$ is a square matrix of order m
		- example
			- $$
			  A = 
			  \begin{bmatrix}
			  3 & -1 & 0 \\
			  \frac{3}{2} & 3\sqrt{2} & 1\\
			  4 & 3 & -1
			  \end{bmatrix}
			  $$ is a square matrix of order 3
		- if A = [a_{ij}] is a square matrix of order n, then elements (entries) $a_{11}, a_{22}, ..., a_{nn}$ are said to constitute the `diagonal`, of the matrix A
	- diagonal matrix
		- a square matrix $B = [b_{ij}]_{m\times n}$ is said to be a diagonal matrix if all its non diagonal elements are zero, that is a matrix $B = [b_{ij}]_{m\times n}$ is said to be a diagonal matrix if $b_{ij} = 0$, when $i \neq j$
			- example:
				- A = [4]
				- $$
				  B = 
				  \begin{bmatrix}
				  -1 & 0 \\
				  0 & 2
				  \end{bmatrix}
				  $$
				- $$
				  C = 
				  \begin{bmatrix}
				  -1 & 0 & 0\\
				  0 & 2 & 0 \\
				  0 & 0 & 3
				  \end{bmatrix}
				  $$
				- are diagonal matrices of order 1, 2, 3 respectively
	- scalar matrix
		- a diagonal matrix is said to be a scalar matrix if its diagonal elements are equal, that is, a square matrix $B = [b_{ij}]_{n\times n}$ is said to be a scalar matrix if 
		  b_{ij} = 0, when i \neq j
		  b_{ij} = k, when i = j, for some constant k
		- example
			- A = [3]
			- $$
			  B = 
			  \begin{bmatrix}
			  -1 & 0 \\
			  0 & -1
			  \end{bmatrix}
			  $$
			- $$
			  C = 
			  \begin{bmatrix}
			  \sqrt{3} & 0 & 0\\
			  0 & \sqrt{3} & 0 \\
			  0 & 0 & \sqrt{3}
			  \end{bmatrix}
			  $$
			- are scalar matrices of order 1, 2 and 3
	- identity matrix
		- a square matrix in which elements in the diagonal are all 1 and rest are all zero is called an identity matrix. in other words, the square matrix A = $A=[a_{ij}]_{n\times n}$ is an identity matrix, if 
		  $$
		  a_{ij} = 
		  \begin{cases}
		  1 & if & i = j \\
		  0 & if & i \neq j
		  \end{cases}
		  $$
		- we denote the identity matrix of order n by $I_n$. when order is clear from the context, we simply write it as I
			- example
				- [1]
				- $$
				  \begin{bmatrix}
				  1 & 0 \\
				  0 & 1
				  \end{bmatrix}
				  $$
				- $$
				  \begin{bmatrix}
				  1 & 0 & 0\\
				  0 & 1 & 0 \\
				  0 & 0 & 1
				  \end{bmatrix}
				  $$
				- are identity matrices of order 1, 2, 3 respectively
			- observe that a scalar matrix is an identity matrix when k = 1. but every identity matrix is clearly a scalar matrix
	- zero matrix
		- a matrix is said to be zero matrix or null matrix if all its elements are zero
			- example
				- [0]
				- $$
				  \begin{bmatrix}
				  0 & 0 \\
				  0 & 0
				  \end{bmatrix}
				  $$
				- $$
				  \begin{bmatrix}
				  0 & 0 & 0\\
				  0 & 0 & 0 \\
				  0 & 0 & 0
				  \end{bmatrix}
				  $$
				- are all zero matrices. we denote zero matrix by O. its order will be clear from the context
	- definition
		- equality of matrices
			- 2 matrices $A = [a_{ij}]$ and $B = [b_{ij}]$ are said to be equal if
				- they are of the same order
				- each element in A is equal to the corresponding element of B, that is $a_{ij} = b_{ij}$ for all i and j
			- if 2 matrices A and B are equal, we write A = B
- operations on matrices
	- addition of matrices
		- sum of 2 matrices is a matrix obtained by adding the corresponding elements of the given matrices. furthermore, the 2 matrices have to be of the same order.
		- in general, if $A = [a_{ij}]$ and $B = [b_{ij}]$ are 2 matrices of the same order, say m x n. then, the sum of the 2 matrices A and Bis defined as a matrix C = $[c_{ij}]_{m\times n}$, where $c_{ij} = a_{ij} + b_{ij}$, for all possible values of i and j
		- thus, if 
		  $$
		  A = 
		  \begin{bmatrix} 
		  a_{11} & a_{12} & a_{13} \\
		  a_{21} & a_{22} & a_{23}
		  \end{bmatrix}
		  $$ is a 2 x 3 matrix
		- $$
		  B = 
		  \begin{bmatrix} 
		  b_{11} & b_{12} & b_{13} \\
		  b_{21} & b_{22} & b_{23}
		  \end{bmatrix}
		  $$
		- then, we define 
		  $$
		  A + B = 
		  \begin{bmatrix} 
		  a_{11} + b_{11} & a_{12} + b_{12} & a_{13} + b_{13}\\
		  a_{21} + b_{21} & a_{22} + b_{22} & a_{23} + b_{23}
		  \end{bmatrix}
		  $$
		- if A and B are not of the same order, then A + B is not defined
		- addition of matrices is an example of binary operation on the set of matrices of the same order
	- multiplication of a matrix by a scalar
		- if $A = [a_{ij}]_{m\times n}$ is a matrix and k is a scalar, then kA is another matrix which is obtained by multiplying each element of A by the scalar k.
		- $kA = k[a_{ij}]_{m\times n} = [k(a_{ij})]_{m\times n}$, that is, (i, j)^{th} element of kA is ka_{ij} for all possible values of i and j.
		- example:
			- $$
			  A = 
			  \begin{bmatrix} 
			  3 & 1 & 1.5 \\
			  \sqrt{5} & 7 & -3 \\
			  2 & 0 & 5
			  \end{bmatrix}
			  $$, then
			  $$
			  3A = 3
			  \begin{bmatrix} 
			  3 & 1 & 1.5 \\
			  \sqrt{5} & 7 & -3 \\
			  2 & 0 & 5
			  \end{bmatrix} 
			  = 
			  \begin{bmatrix} 
			  9 & 3 & 4.5 \\
			  3\sqrt{5} & 21 & -9 \\
			  6 & 0 & 15
			  \end{bmatrix} 
			  $$
		- negative of a matrix
			- negative of a matrix is denoted by -A. we define -A = (-1) A
			- example:
				- $$
				  A = 
				  \begin{bmatrix} 
				  3 & 1 \\
				  -5 & x
				  \end{bmatrix}
				  $$, then -A is given by
				  $$
				  -A = (-1) A 
				  = (-1)\begin{bmatrix} 
				  3 & 1 \\
				  -5 & x
				  \end{bmatrix}
				  = \begin{bmatrix} 
				  -3 & -1 \\
				  5 & -x
				  \end{bmatrix}
				  $$
		- difference of matrices
			- if A = [a_{ij}], B = [b_{ij}] are 2 matrices of the same order, say m x n, then difference A - B is defined as matrix D = [d_{ij}], where d_{ij} = a{ij} - b_{ij}, fo all values of i and j.
			- in other words, D = A - B = A + (-1)B, that is sum of the matrix A and the matrix -B
	- properties of matrix addition
		- commutative law
			- A, B matrices of the same order say m x n, then A + B = B + A
		- associative law
			- for any 3 matrices A, B, C of the same order, say m x n, (A + B) + C = A + (B + C)
		- existence of additive identity
			- A be an m x n matrix and O be an m x n zero matrix, the A + O = O + A = A
			- O is the additive identity for matrix addition
		- the existence of additive inverse
			- A be any matrix, then we have another matrix as -A, such that A + (-A) = (-A) + A = O. so -A is the additive inverse of A or negative of A
	- properties of scalar multiplication of a matrix
		- A, B be 2 matrices of the same order m x n, and k and l are scalars, then
		- k(A + B) = kA + kB
		- (k + l)A = kA + lA
	- multiplication of matrices
		- the product of 2 matrices A and B is defined if the number of columns of A is equal to the number of rows of B.
		- A = [a_{ij}] be an m x n matrix and B = [b_{jk}] be an n x p matrix. then the product of the matrices A and B is the matrix C of order m x p.
		- to get the (i, k)^{th} element c_{ik} of the matrix C, we take the i^{th} row of A and k^{th} column of B, multiply them elementwise and take the sum of all these products.
		- A = [a_{ij}]_{m\times n}, B = [b_{jk}]_{n\times p}, then the i^{th} row of A is $[a_{i1} a_{i2} ... a_{in}] and the k^{th} column of B is 
		  $$
		  \begin{bmatrix}
		  b_{1k} \\
		  b_{2k} \\
		  .
		  .
		  .
		  b_{nk}
		  \end{bmatrix}
		  $$, then $c_{ik} = a_{i1}b_{1k} + a_{i2}b_{2k} + a_{i3}b_{3k} + ... + a_{in}b_{nk} = \sum_{j=1}^n a_{ij}b_{jk}$
		  the matrix C = [c_{ik}]_{m\times p} is the product of A and B
		- if AB is defined, then BA need not be defined. if A and B are, respectively m x n, k x l matrices, then both AB and BA are defined if and only if n = k and l = m.
		- if both A and B are square matrices of the same order, then both AB and BA are defined
		- non-commutativity of multiplication of matrices
			- even if AB and BA are both defined, it is not necessary that AB = BA
		- multiplication of diagonal matrices of same order will be commutative
		- zero matrix as the product of 2 non zero matrices
			- for real numbers, a, b if ab = 0, then either a = 0 or b = 0. this need not be true for matrices.
			- if the product of 2 matrices is a zero matrix, it is not necessary that one of the matrices is a zero matrix
	- properties of multiplication of matrices
		- the associative law
			- A, B and C, (AB) C = A (BC), whenever both sides of the equality are defined
		- the distributive law
			- A (B + C) = AB + AC
			- (A + B) C = AC + BC, whenever both sides of equality are defined
		- the existence of multiplicative identiy
			- for every square matrix A, there exist an identity matrix of same order such that IA = AI = A
- transpose of a matrix
	- definition:
		- A = [a_{ij}] be an m x n matrix, then the matrix obtained by interchanging the rows and columns of A is called the transpose of A.
		- transpose of the matrix A is denoted by A' or $A^T$
		- $A = [a_{ij}]_{m\times n}$, then $A^T = [a_{ji}]_{n\times m}$
		- example
			- $$
			  A = 
			  \begin{bmatrix}
			  3 & 5 \\
			  \sqrt{3} & 1 \\
			  0 & \frac{-1}{5}
			  \end{bmatrix}_{3\times 2}
			  $$, then 
			  $$
			  A' = 
			  \begin{bmatrix}
			  3 & \sqrt{3} & 0 \\
			  5 & 1 & \frac{-1}{5}
			  \end{bmatrix}_{2\times 3}
			  $$
	- properties of transpose of the matrices
		- $(A')' = A$
		- $(kA)' = kA'$ (where k is any constant)
		- $(A + B)' = A' + B'$
		- $(A B)' = B' A'$
- symmetric and skew symmetric matrices
	- symmetric matrix: definition
		- a square matrix A = [a_{ij}] is said to be symmetric if A' = A, that is, [a_{ij}] = [a_{ji}] for all possible values of i and j
		- example
			- A = 
			  $$
			  \begin{bmatrix}
			  \sqrt{3} & 2 & 3 \\
			  2 & -1.5 & -1 \\
			  3 & -1 & 1
			  \end{bmatrix}
			  $$ 
			  is a symmetric matrix as A' = A
	- skew symmetric matrix: definition
		- a square matrix A = [a_{ij}] is said to be skew symmetric if A' = -A, that is, [a_{ji}] = -[a_{ij}] for all possible values of i and j.
		- if we put i = j, we have a_{ii} = -a{ii}. therefore 2a_{ii} = 0 or a_{ii} = 0 for all i's. this means that all the diagonal elements of a skew symmetric matrix are zero
		- example
			- B = 
			  $$
			  \begin{bmatrix}
			  0 & 2 & 3 \\
			  -2 & 0 & -1 \\
			  -3 & 1 & 0
			  \end{bmatrix}
			  $$ 
			  is a skew symmetric matrix as B' = -B
		- for any square matrix A with real number entries
			- A + A' is a symmetric matrix
			- A - A' is a skew symmetric matrix
		- any square matrix can be expressed as the sum of a symmetric and skew symmetric matrix
			- $A = \frac{1}{2} (A + A') + \frac{1}{2} (A - A')$
- elementary operation (transformation) of a matrix
	- there are 6 operations (transformations) on a matrix, 3 of which are due to rows and 3 due to columns, which are known as elementary operations or transformations
		- interchange of any 2 rows or 2 columns
			- symbolically the interchange of i_{th} and j_{th} rows is denoted by $R_i ↔ R_j$ and interchange of i{th} and j{th} column is denoted by $C_i ↔ C_j$
			- example
				- applying $R_1 ↔ R_2$ to 
				  $$
				  A = 
				  \begin{bmatrix}
				  1 & 2 & 1 \\
				  -1 & \sqrt{3} & 1 \\
				  5 & 6 & 7
				  \end{bmatrix}
				  , we get 
				  \begin{bmatrix}
				  -1 & \sqrt{3} & 1 \\
				  1 & 2 & 1 \\
				  5 & 6 & 7
				  \end{bmatrix}
				  $$
		- multiplication of the elements of any row or column by a non-zero number
			- symbolically, the multiplication of each element of the i^{th} row by k, where k \neq 0 is denoted by $R_i$ -> $kR_i$
			- the corresponding column operation is denoted by $C_i$ -> $kC_i$
			- example
				- applying $C_3$ -> $\frac{1}{7}C_3$ to 
				  $$B = 
				  \begin{bmatrix}
				  1 & 2 & 1 \\
				  -1 & \sqrt{3} & 1
				  \end{bmatrix}
				  , we get 
				  \begin{bmatrix}
				  1 & 2 & \frac{1}{7} \\
				  -1 & \sqrt{3} & \frac{1}{7}
				  \end{bmatrix}$$
		- the addition to the elements of any row or column, the corresponding elements of any other row or column multiplied by any non-zero number
			- symbolically, the addition to the elements of i^{th} row, the corresponding elements of j^{th} row multiplied by k is denoted by $R_i$ -> $R_i + kR_j$.
			- the corresponding column operation is denoted by $C_i$ -> $C_i + kC_j$
			- example
				- $R_2$ -> $R_2 - 2R_1$, to 
				  $$C = 
				  \begin{bmatrix}
				  1 & 2 \\
				  2 & -1
				  \end{bmatrix}
				  , we get 
				  \begin{bmatrix}
				  1 & 2 \\
				  2-2\times 1 & -1-2\times 2
				  \end{bmatrix}
				  $$
- invertible matrices
	- definition
		- if A is a square matrix of order m, and if there exists another square matrix B of the same order m, such that AB = BA = I, then B is called the inverse matrix of A and it is denoted by A^{-1}. in that case A is said to be invertible.
			- example
				- $$
				  A = 
				  \begin{bmatrix}
				  2 & 3 \\
				  1 & 2
				  \end{bmatrix}
				  $$ and 
				  $$
				  B = 
				  \begin{bmatrix}
				  2 & -3 \\
				  -1 & 2
				  \end{bmatrix}
				  $$
				- now AB = BA = I. thus B is the inverse of A, in other words B = A^{-1} and A is inverse of B, i.e., A = B^{-1}
		- a rectangular matrix does not posses inverse matrix, since for products BA and AB to be defined and to be equal, it is necessary that matrices A and B should be square matrices of the same order.
		- if B is the inverse of A, then A is also the inverse of B
		- uniqueness of inverse
			- inverse of a square matrix, if it exists, is unique
		- A and B are invertible matrices of the same order, then (AB)^{-1} = B^{-1}A^{-1}
	- inverse of a matrix by elementary operations
		- X, A, B matrices of the same order such that X = AB
		- in order to apply a sequence of elementary row operations on the matrix equation X = AB, we will apply these row operations simultaneously on X and on the first matrix A of the product AB on RHS
		- similarly, in order to apply a sequence of elementary column operations on the matrix equation X = AB, we will apply, these operations simultaneously on X and on the second matrix B of the product AB on RHS
		- in view of the above discussion, we conclude that if A is a matrix such that A^{-1} exists, then to find A^{-1} using elementary row operations, write A = IA and apply a sequence of row operation on A = IA till we get, I = BA. the matrix B will be the inverse of A.
		- similarly, if we wish to find A^{-1} using column operations, then, write A = AI and apply a sequence of column operations on A = AI till we get, I = AB
		- in case, after applying one or more elementary row (column) operations on A = IA (A = AI), if we obtain all zeros in one or more rows of the matrix A on L.H.S., then A^{-1} does not exist