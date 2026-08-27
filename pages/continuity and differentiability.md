- ![Class-12-1-Mathematics-Part-I-05_Continuity_and_differentiability.pdf](../assets/Class-12-1-Mathematics-Part-I-05_Continuity_and_differentiability_1786588262981_0.pdf)
- continuity
	- definition: continuous function
		- f is a real function on a subset of the real numbers and let c be a point in the domain of f. then f is continuous at c if 
		  $lim_{x \to c} f(x) = f(c)$
		- more elaborately, if the left hand limit, right hand limit and the value of the function at x = c exist and equal to each other, then f is said to be continuous at x = c. if the right hand and left hand limits at x = c coincide, the we say that the common value is the limit of the function at x = c. hence, we may rephrase the definition of continuity as follows: a function is continuous at x = c if the functions is defined at x = c and if the value of the function at x = c equals the limit of the function at x = c. if f is not continuous at c, we say f is discontinuous at c and c is called a point of discontinuity of f.
	- definition:
		- a real function f is said to be continuous if it is continuous at every point in the domain of f
		- this definition requires a bit of elaboration. suppose f is a function defined on a closed interval [a, b], then for f to be continuous, it needs to be continuous at every point in [a, b] including the end points a and b. continuity of f at a means
		  $lim_{x \to a^{+}} f(x) = f(a)$
		  and continuity of f at b means
		  $lim_{x \to b^{-}} f(x) = f(b)$
		  observe that $lim_{x \to a^{-}} f(x) = f(a)$ and $lim_{x \to b^{+}} f(x) = f(b)$ do not make sense. as a consequence of this definition, if f is defined only at one point, it is continuous there, i.e., if the domain of f is a singleton, f is a continuous function
	- algebra of continuous functions
		- continuity of a function at a point is entirely dictated by the limit of the function at that point.
		- theorem 1: f and g be 2 real functions continuous at a real number c. then
			- f + g is continuous at x = c
			- f - g is continuous at x = c
			- f . g is continuous at x = c
			- $\frac{f}{g}$ is continuous at x = c, (provided g(c) \neq 0)
			- remarks
				- as a special case of multiplication, if f is a constant function, i.e., f(x) = \lambda for some real number \lambda, then the function (\lambda . g) defined by (\lambda. g) (x) = \lambda . g(x) is also continuous. in particular if \lambda = -1, the continuity of f implies continuity of -f.
				- as a special case of division, if f is the constant function f(x) = \lambda, then the function $\frac{\lambda}{g}$ defined by $\frac{\lambda}{g}(x) = \frac{\lambda}{g(x)}$ is also continuous wherever g(x) \neq 0. in particular, the continuity of g implies continuity of $\frac{1}{g}$
		- theorem 2: f and g are real valued functions such that $(f \circ g)$ is defined at c. if g is continuous at c and if f is continuous at g(c), then $(f \circ g)$ is continuous at c
- differentiability
	- LATER f is a real function and c is a point in its domain. the derivative of f at c is defined by
	  $lim_{h \to 0}\frac{f(c+h) - f(c)}{h}$ provided this limit exists.
	  derivative of f at c is denoted by f'(c) of $\frac{d}{dx}(f(x))|_c$
	  the function defined by
	  $f'(x) = lim_{h \to 0}\frac{f(x + h) - f(x)}{h}$ wherever the limit exists is defined to be the derivative of f. the derivative of f is denoted by f'(x) or $\frac{d}{dx}(f(x))$ or if y = f(x) by $\frac{dy}{dx}$ or y'.
	  the process of finding derivative of a function is called differentiation. we also use the phrase `differentiate f(x) with respect to x` to mean `find f'(x)`
	  following rules were established as a part of algebra of derivative:
	  (u \pm v)' = u' \pm v'
	  (uv)' = u'v + uv' (Leibnitz or product rule)
	  $(\frac{u}{v})' = \frac{u'v - uv'}{v^2}$, wherever v \neq 0 (quotient rule)
	- list of derivatives of certain standard functions
		- |f(x)|x^n|sin x|cos x|tan x|
		  |f'(x)|nx^{n-1}|cos x|-sin x|$sec^2$ x|
		- whenever we defined derivative, we had put a caution `provided the limit exists`. now the natural question is; what if it doesn't? the question is quite pertinent and so is its answer. if $lim_{h \to 0}\frac{f(c+h) - f(c)}{h}$ does not exist, we say that f is not differentiable at c. in other words, we say that a function f is differentiable at a point c in its domain if both $lim_{h \to 0^-}\frac{f(c+h) - f(c)}{h}$ and $lim_{h \to 0^+}\frac{f(c+h) - f(c)}{h}$ are finite and equal. a function is said to be differentiable in an interval [a, b] if it is differentiable at every point of [a, b]. as in case of continuity, at the end point a and b, we take the right hand limit and left hand limit, which are nothing but left hand derivative and right hand derivative of the function at a and b respectively. similarly, a function is said to be differentiable in an interval (a, b) if it is differentiable at every point of (a, b)
	- theorem 3:
		- if a function f is differentiable at a point c, then it is also continuous at that point
		- corollary 1: every differentiable function is continuous
			- we remark that the converse of the above statement is not true. indeed we have seen that the function defined by f(x) = |x| is a continuous function. consider the left hand limit
			  $lim_{h \to 0^-} \frac{f(0 + h) - f(0)}{h} = \frac{-h}{h} = -1$
			  right hand limit
			  $lim_{h \to 0^+} \frac{f(0 + h) - f(0)}{h} = \frac{h}{h} = 1$
			  since the above left and right hand limits at 0 are not equal, 
			  $lim_{h \to 0} \frac{f(0 + h) - f(0)}{h}$  does not exist and hence f is not differentiable at 0. thus f is not a differentiable function
	- derivatives of composite functions
		- theorem 4: chain rule
	- derivatives of implicit functions
	- derivatives of inverse trigonometric functions
- exponential and logarithmic functions
- derivatives of functions in parametric forms
- second order derivative
- mean value theorem