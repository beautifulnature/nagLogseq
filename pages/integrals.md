- ![Class-12-2-Mathematics-Part-II-01_Integrals.pdf](../assets/Class-12-2-Mathematics-Part-II-01_Integrals_1786586799711_0.pdf)
- introduction
	- differential calculus is centered on the concept of the derivative. the original motivation for the derivative was the problem of defining tangent lines to the graphs of functions and calculating the slope of such lines. integral calculus is motivated by the problem of defining and calculating the area of the region bounded by the graph of the functions.
	- if a function f is differentiable in an interval I, i.e., its derivative f' exists at each point of I, then a natural question arises that given f' at each point of I, can we determine the function? the functions that could possibly have given function as a derivative are called anti derivatives (or primitive) of the function. further, the formula that gives all these anti derivatives is called the `indefinite integral` of the function and such process of finding antiderivatives is called `integration`. such type of problems arise in many practical situations. for instance, if we know the instantaneous velocity of an object at any instant, then there arises a natural question, i.e., can we determine the position of the object at any instant? there are several such practical and theoretical situations where the process of integration is involved. the development of integral calculus arises out of the efforts of solving the problems of the following types:
		- the problem of finding a function whenever its derivative is given
		- the problem of finding the area bounded by the graph of a function under certain conditions
	- these 2 problems lead to the 2 forms of the integrals, e.g. indefinite and definite integrals, which together constitute the `Integral Calculus`. there is a connection, known as the `Fundamental Theorem of Calculus`, between indefinite integral and definite integral which makes the definite integral as a practical tool for science and engineering. the definite integral is also used to solve many interesting problems from various disciplines like economics, finance and probability.
- integration as an inverse process of differentiation
	- integration is the inverse process of differentiation. instead of differentiating a function, we are given the derivative of a function and asked to find its primitive, i.e., the original function. such process is called `integration` or `anti differentiation`.
	- for any arbitrary real number C, (also called `constant of integration`)
	  $\frac{d}{dx}[F(x) + C] = f(x), \forall x \in I$
	  thus, {F + C, C \in R} denotes a family of anti derivatives of f.
	- Remark
		- functions with same derivatives differ by a constant. to show this, let g and h be 2 functions having the same derivatives on an interval I.
		- consider the function f = g - h define by f(x) = g(x) - h(x), \forall x \in I
		- then $\frac{df}{dx} = f' = g' - h'$ giving f'(x) = g'(x) - h'(x) \forall x \in I
		- or f'(x) = 0, \forall x \in I by hypothesis
		- i.e., the rate of change of f with respect to x is zero on I and hence f is constant.
		- in view of the above remark, it is justified to infer that the family {F+C, C \in R} provides all possible anti derivatives of f.
		- we introduce a new symbol, namely \int f(x) dx which will represent the entire class of anti derivatives read as the indefinite integral of f with respect to x.
		- symbolically, we write \int f(x) dx = F(x) + C
		- notation given that $\frac{dy}{dx} = f(x)$ we write y = \int f(x) dx
		- | symbols / terms / phrases | meaning|
		  | \int f(x) dx | integral of f with respect to x|
		  | f(x) in \int f(x) dx | integrand|
		  | x in \int f(x) dx| variable of integration|
		  | Integrate| find the integral|
		  | an integral of f| a function F such that F'(x) = f(x)|
		  | Integration | the process of finding the integral|
		  | constant of integration | any real number C, considered as constant function |
		- standard formlae
			- | derivatives | integrals (anti derivatives) |
			  | $\frac{d}{dx}\frac{x^{n+1}}{n + 1} = x^n;$ | $\int x^n dx = \frac{x^{n+1}}{n+1} + C, n \neq -1$ |
			  | particularly, we note that $\frac{d}{dx}(x) = 1;$ | $\int dx = x + C$ |
			  | $\frac{d}{dx} (sin\ x) = cos\ x$ | \int cos x dx = sin x + C |
			  | $\frac{d}{dx} (-cos\ x) = sin\ x$ | \int sin x dx = -cos x + C |
			  | $\frac{d}{dx} (tan\ x) = sec^2\ x$ | $\int sec^2\ x\ dx = tan\ x + C$ |
			  | $\frac{d}{dx} (-cot\ x) = cosec^2\ x$ | $\int cosec^2\ x\ dx = -cot\ x + C$ |
			  | $\frac{d}{dx} (sec\ x) = sec\ x\  tan\ x$ | \int sec x tan x dx = sec x + C |
			  | $\frac{d}{dx} (-cosec\ x) = cosec\ x\  cot\ x$ | \int cosec x cot x dx = -cosec x + C |
			  | $\frac{d}{dx} (sin^{-1}\ x) = \frac{1}{\sqrt{1 - x^2}}$ | $\int \frac{dx}{\sqrt{1 - x^2}} = sin^{-1} x + C$ |
			-
		- note: in practice, we normally do not mention the interval over which the various functions are defined. however, in any specific problem one has to keep it in mind.
	- geometrical interpretation of indefinite integral
		- let f(x) = 2x then \int f(x) dx = $x^2$ + C. for different values of C, we get different integrals. but these integrals are very similar geometrically.
	- some properties of indefinite integral
	- comparison between differentiation and integration
- methods of integration
	- integration by substitution
	- integration using trigonometric identities
- integrals of some particular functions
- integration by partial fractions
- integration by parts
- definite integral
	- definite integral as the limit of a sum
- fundamental theorem of calculus
	- area function
	- first fundamental theorem of integral calculus
	- second fundamental theorem of integral calculus
- evaluation of definite integrals by substitution
- some properties of definite integrals