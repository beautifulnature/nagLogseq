- ![Class-12-1-Mathematics-Part-I-06_Application_of_derivatives.pdf](../assets/Class-12-1-Mathematics-Part-I-06_Application_of_derivatives_1786588343497_0.pdf)
- introduction
	- derivative can be used
		- to determine rate of change of quantities
		- to find the equations of tangent and normal to a curve at a point
		- to find turning points on the graph of a function which in turn will help us to locate points at which largest or smallest value (locally) of a function occurs
		- intervals on which a function is increasing or decreasing
		- approximate value of certain quantities
- rate of change of quantities
	- derivative $\frac{ds}{dt}$, we mean the rate of change of distance s with respect to the time t. whenever one quantity y varies with another quantity x, satisfying some rule y = f(x), then $\frac{dy}{dx}$ (or f'(x)) represents the rate of change of y with respect to x and $\frac{dy}{dx} ]_{x=x_0}$ (or f'($x_0$)) represents the rate of change of y with respect to x at $x = x_0$
	- further, if 2 variables x and y are varying with respect to another variable t, i.e., if x = f(t) and y = g(t), then by chain rule
	  $\frac{dy}{dx} = \frac{\frac{dy}{dt}}{\frac{dx}{dt}}$, if $\frac{dx}{dt} \neq 0$
	  thus, the rate of change of y with respect to x can be calculated using the rate of change of y and that of x both with respect to t.
	- $\frac{dy}{dx}$ is positive if y increases as x increases and is negative if y decreases as x increases
- increasing and decreasing functions
	- function may increase or decrease or none
	- definition 1
		- I be an interval contained in the domain of a real valued function f. then f is said to be
			- increasing on I if $x_1 < x_2$ in I => $f(x_1) \leq f(x_2)$ for all $x_1, x_2 \in I$
			- strictly increasing on I if $x_1 < x_2$ in I => $f(x_1) < f(x_2)$ for all $x_1, x_2 \in I$
			- decreasing on I if $x_1 < x_2$ in I => $f(x_1) \geq f(x_2)$ for all $x_1, x_2 \in I$
			- strictly decreasing on I if $x_1 < x_2$ in I => $f(x_1) > f(x_2)$ for all $x_1, x_2 \in I$
			- graphical representation of functions
				- ![image.png](../assets/image_1788057298375_0.png)
				- ![image.png](../assets/image_1788057321278_0.png)
	- definition 2
		- $x_0$ a point in the domain of definition of a real valued function f. then f is said to be increasing, strictly increasing, decreasing or strictly decreasing at $x_0$ if there exists an open interval I containing $x_0$ such that f is increasing, strictly increasing, decreasing or strictly decreasing, respectively, in I.
		- a function f is said to be increasing at $x_0$ if there exists an interval I = ($x_0-h, x_0+h$), h > 0 such that for $x_1, x_2 \in I$
		  $x_1 < x_2 \in I \to f(x_1) \leq f(x_2)$
	- theorem 1
		- f be continuous on [a, b] and differentiable on the open interval (a, b) then
			- f is strictly increasing in [a, b] if f'(x) > 0 for each x \in (a, b)
			- f is strictly decreasing in [a, b] if f'(x) < 0 for each x \in (a, b)
			- f is a constant function in [a, b] if f'(x) = 0 for each x \in (a, b)
		- remarks
			- if f'(x) > 0 for x in an interval excluding the end points and f is continuous in the interval, then f is strictly increasing. if f'(x) < 0 for x in an interval excluding the end points and f is continuous in the interval, then f is strictly decreasing
			- if a function is strictly increasing or strictly decreasing in an interval I, then it is necessarily increasing or decreasing in I. however, the converse need not be true.
- tangents and normals
	- use differentiation to find the equation of the tangent line and the normal line to a curve at a given point
	- equation of a straight line passing through a given point $(x_0, y_0)$ having finite slope m is given by
	  $y - y_0 = m (x - x_0)$
	- note that the slope of the tangent to the curve y = f(x) at the point $(x_0, y_0)$ is given by $\frac{dy}{dx}]_{(x_0, y_0)}$ (or $f'(x_0)$)
	- so the equation of the tangent at $(x_0, y_0)$ to the curve y = f(x) is given by
	  $y - y_0 = f'(x_0) (x - x_0)$
	- also, since the normal is perpendicular to the tangent, the slope of the normal to the curve y = f(x) at (x_0, y_0) is $\frac{-1}{f'(x_0)}$
	- therefore, the equation of the normal to the curve y = f(x) at $(x_0, y_0)$ is given by
	  $y - y_0 = \frac{-1}{f'(x_0)} (x - x_0)$
	  i.e. $y - y_0  f'(x_0) + (x - x_0) = 0$
	- if a tangent line to the curve y = f(x) makes an angle \theta with x-axis in the positive direction, then $\frac{dy}{dx}$ = slope of the tangent = tan \theta
	- particular cases
		- if slope of the tangent line is zero, then tan \theta = 0 and so \theta = 0 which means the tangent line is parallel to the x-axis. in this case, the equation of the tangent at the point $(x_0, y_0)$ is given by $y = y_0$
		- if \theta -> $\frac{\pi}{2}$, then tan \theta = \infty, which means the tangent line is perpendicular to the x-axis, i.e., parallel to the y-axis. in this case, the equation of the tangent at $(x_0, y_0)$ is given by $x = x_0$
- approximations
	- ![image.png](../assets/image_1788069053287_0.png)
	- use differentials to approximate values of certain quantities
	- f : D \to R, D \sub R be a given function and let y = f(x). let \Delta x denote small increment in x. the increment in y corresponding to the increment in x, denoted by \Delta y, given by \Delta y = f(x + \Delta y) - f(x). we define the following
		- the differential of x, denoted by dx, is defined by dx = \Delta x
		- the differential of y, denoted by dy, is defined by dy = f'(x) dx or $dy = \left[ \frac{dy}{dx} \right] \Delta x$
			- in case of dy = \Delta x is relatively small when compared with x, dy is a good approximation of \Delta y and we denote it by dy \approx \Delta y
			- note: differential of the dependent variable is not equal to increment of the variable where as the differential of independent variable is equal to the increment of the variable.
- maxima and minima
	- use the concept of derivatives to calculate the maximum or minimum values of various functions. find the `turning points` of the graph of a function and thus find points at which the graph reaches its highest (or lowest) locally. the knowledge of such points is very useful in sketching the graph of a given function. we will find the absolute maximum and absolute minimum of a function that are necessary for the solution of many applied problems.
		- definition 3
		  collapsed:: true
			- f be a function defined on an interval I. then
			  collapsed:: true
				- f is said to have a `maximum value` in I, if there exists a point c in I such that f(c) > f(x), for all x \in I.
				  the number f(c) is called the maximum value of f in I and the point c is called a `point of maximum value` of f in I
				- f is said to have a `minimum value` in I, if there exists a point c in I such that f(c) < f(x), for all x \in I.
				  the number f(c) is called the minimum value of f in I and the point c is called a `point of minimum value` of f in I
				- f is said to have a `extreme value` in I, if there exists a point c in I such that f(c) is either a maximum value or a minimum value of f in I.
				  the number f(c) is called an extreme value of f in I and the point c is called an `extreme point`
				- ![image.png](../assets/image_1788071787609_0.png)
				- remarks
					- monotonic function f in an interval I, we mean that f is either increasing in I or decreasing in I
					- every monotonic function assumes its maximum / minimum value at the end points of the domain of definition of the function.
					- every continuous function on a closed interval has a maximum and a minimum value
		- ![image.png](../assets/image_1788072684525_0.png)
			- point A, B, C, D on the graph the function changes its nature from decreasing to increasing or vice-versa. these points are called `turning points`. points A, C may be regarded as points of `local minimum value` (or `relative minimum value`) and points B, D may be regarded as points of `local maximum value` (or `relative maximum value`) for the function. the `local maximum value` and `local minimum value` of the function are referred to as `local maxima` and `local minima` of the function
		- definition 4
		- theorem 2
		- theorem 3 (first derivative test)
		- theorem 4 (second derivative test)
	- maximum and minimum values of a function in a closed interval
		- theorem 5
		- theorem 6
	-