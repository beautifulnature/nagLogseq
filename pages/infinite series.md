- ![Class-11-Mathematics-a1_Infinite_Series.pdf](../assets/Class-11-Mathematics-a1_Infinite_Series_1785690802311_0.pdf)
- introduction
	- a sequence $a_1, a_2, a_3, ..., a_n, ...$ having infinite number of terms is called `infinite sequence` and its indicated sum, i.e., $a_1 + a_2 + a_3 + ...  + a_n + ...$ is called an `infinite series` associated with infinite sequence.
	  this series can also be expressed in abbreviated form using the sigma notation, i.e.,
	  $a_1 + a_2 + a_3 + ...  + a_n + ... = \sum_{k=1}^{\infty}a_k$
- binomial theorem for any index
	- binomial series
		- $(1 + x)^n = nC_0 + nC_1 x + ... + nC_n x^n$
		  n is non-negative integer
		- binomial theorem, giving an infinite series in which index is negative or a fraction and not a whole number
			- $(1 + x)^m = 1 + mx + \frac{m (m-1)}{1 \times 2} x^2 + \frac{m (m-1)(m-2}{1 \times 2 \times 3} x^3$ + ...
			  holds whenever |x| < 1
			- note carefully the condition |x| < 1, i.e., -1 < x < 1 is necessary when m is negative integer or a fraction
			- note that there are infinite number of terms in the expansion of $(1 + x)^m$, when m is a negative integer or a fraction
				- $(a + b)^m = a^m (1 + \frac{b}{a})^m$
				  $= a^m  + m a^{m-1}b + \frac{m(m-1)}{1 \times 2} a^{m-2}b^2 + ...$
				- this expansion is valid when |b/a| < 1 or equivalently when |b| < |a|
				- the general term in the expansion of $(a + b)^m is $\frac{m(m-1)(m-2)...(m-r+1)a^{m-r}b^r}{1 \times 2 \times 3 \times ... \times r}$
			- $(1 + x)^{-1} = 1 - x + x^2 - x^3 + ...$
			- $(1 - x)^{-1} = 1 + x + x^2 + x^3 + ...$
			- $(1 + x)^{-2} = 1 - 2x + 3x^2 - 4x^3 + ...$
			- $(1 - x)^{-2} = 1 + 2x + 3x^2 + 4x^3 + ...$
- infinite geometric series
	- a sequence $a_1, a_2, a_3, ..., a_n$ is called G.P., if $\frac{a_{k+1}{a_k}} = r$ (constant) for k = 1, 2, 3, ..., n-1. if we take $a_1 = a$, then the resulting sequence $a, ar, ar^2, ..., a^{n-1}$ is taken as standard form of G.P., where a is first term and r the common ratio of G.P.
	- formula to find the sum of finite series $a + ar + ar^2 + ... + a^{n-1} + ...$ which is given by $S_n = \frac{a(1 - r^n)}{1 - r}$
	- for infinite geometric progression $a, ar, ar^2, ..., a^{n-1}, ...$, if numerical value of common ration r is less than 1, then
	  $S_n = \frac{a(1 - r^n)}{1 - r}$ = $\frac{a}{1-r} - \frac{ar^n}{1-r}$
	  in this case, $r^n$ -> 0 as n -> \infty since |r| < 1 and then $\frac{ar^n}{1-r}$ -> 0
	  $S_n$ -> $\frac{a}{1 - r}$ as n -> \infty
	  symbolically, sum of infinity of infinite geometric series is denoted by S
	  S = $\frac{a}{1 - r}$
- exponential series
	- Leonhard Euler introduced the number `e`.
	- the number `e` is useful in calculus as \pi in the study of circle
	- infinite series of numbers $1 + \frac{1}{1!} + \frac{1}{2!} + \frac{1}{3!} + ...$. sum of the series is denoted by e
	- $\frac{1}{n!} < \frac{1}{2^{n+1}}$, when n > 2
	- 2 < e < 3
	- exponential series involving variable x can be expressed as
	  $e^x = 1 + \frac{x}{1!} + \frac{x^2}{2!} + \frac{x^3}{3!} + ... + \frac{x^n}{n!} + ...$
- logarithmic series
	- if |x| < 1, then 
	  $log_e(1 + x) = x - \frac{x^2}{2} + \frac{x ^ 3}{3} - ...$
	  the series on the right hand side of the above is called the `logarithmic series`
	- $log_e2 = 1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + ...$