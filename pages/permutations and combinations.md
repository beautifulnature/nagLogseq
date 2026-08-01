- ![class-11-mathematics-ch7-permutations_and_combinations.pdf](../assets/class-11-mathematics-ch7-permutations_and_combinations_1785556692284_0.pdf)
- fundamental principle of counting
	- `fundamental principle of counting` (`multiplication principle`)
		- if an event can occur in m different ways, following which another event can occur in n different ways, then the total number of occurrence of the events in the given order is mxn
- permutations
	- definition: a permutation is an arrangement in a definite order of a number of objects taken some or all at a time
	- permutations when all the objects are distinct
		- theorem: the number of permutations of n different objects taken r at a time, where 0 < r \(\leq\) n and the objects do not repeat is 
		  n (n-1) (n-2) ... (n-(r-1))
		  or 
		  n (n-1) (n-2) ... (n-r+1) 
		  and is represented as \(^nP_r\)
	- fractional notation
		- the notation `n!` (read as `n factorial`) represents the product of first n natural numbers
			- n! = 1 x 2 x 3 x ... x (n-1) x n
			- we define 0! = 1
			- for a natural number n
			  n ! = n (n - 1)!
			       = n (n - 1) (n - 2)! (provided n \(\geq 2\))
			       = n (n - 1) (n - 2) (n - 3)! (provided n \(\geq 3\))
	- derivation of the formula for \(^{n}P_{r}\)
		- \(^{n}P_{r}\) = \(\frac{n!}{(n-r)!}\), 0 \(\leq\) r \(\leq\) n
		- when r = n, \(^{n}P_{n}\) = \(\frac{n!}{0!}\) = n!
		- arranging no object at all is the same as leaving behind all the objects and there is only one way of doing so
		  \(^{n}P_{0}\) = 1 = \(\frac{n!}{n!}\) = \(\frac{n!}{(n-0)!}\)
		- theorem: the number of permutations of n different objects taken r at a time, where repetition is allowed, is \(n^r\)
	- permutations when all the objects are not distinct objects
		- theorem: the number of permutations of n objects, where p objects are of the same kind and rest are all different = \(\frac{n!}{p!}\)
		- theorem: the number of permutations of n objects, where \(p_1\) objects are of one kind, \(p_2\) are of second kind, ..., \(p_k\) are of \(k^{th}\) kind and the rest, if any, are of different kind is \(\frac{n!}{p_1! p_2! ... p_k!}\)
- combinations
	- \(^nP_r = ^nC_r r!, 0 < r \leq n \)
	- \(^nC_r = \frac{n!}{r! (n-r)!} \)
	  :LOGBOOK:
	  CLOCK: [2026-08-01 Sat 12:29:30]
	  :END:
	  in particular if r = n, \(^nCn = \frac{n!}{n! 0!} = 1 \)
	- we define \(^nC_0 = 1\), i.e., the number of combinations of n different things taken nothing at all is considered to be 1. counting combinations is merely counting the number of ways in which some or all objects at a time are selected. selecting nothing at all is the same as leaving behind all the objects and we know that there is only one way of doing so. this way we define \(^nC_0 = 1 \)
	- as \(\frac{n!}{0! (n-0)!} = 1 = nC_0 \), the formula \(^nC_r = \frac{n!}{r! (n-r)!} \) is applicable for r = 0 also 
	  \(^nC_r = \frac{n!}{r! (n-r)!}, 0 \leq r \leq n \)
	- \(^nC_{n-r} = \frac{n!}{(n-r)! (n-(n-r))!} = \frac{n!}{(n-r)! r!} = nC_r \)
	  i.e., selecting r objects out of n objects is same as rejecting (n-r) objects
	- \(nC_a = nC_b => a = b or a = n - b, i.e., n = a + b
	- \(^nC_r + ^nC_{r-1} = ^{n+1}C_r \)
	  is a Pascal's identity
	  it says that the number of ways to choose r objects from n + 1 objects can be split into 2 cases: either one particular object is included, or it is not.
	  if it includes the object, choose the remaining r - 1 objects from the other n objects in \(nC{r-1}\) ways; if it excludes the object, choose all r objects from the n objects in \(nC_r\) ways. these 2 cases are disjoint and cover all possibilities