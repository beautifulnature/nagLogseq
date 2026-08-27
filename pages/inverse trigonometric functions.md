- ![Class-12-1-Mathematics-Part-I-02_Inverse_trigonometric_functions.pdf](../assets/Class-12-1-Mathematics-Part-I-02_Inverse_trigonometric_functions_1786588037034_0.pdf)
- introduction
	- inverse of a function f, denoted by $f^{-1}$, exists if f is one-one and onto. there are many functions which are not one-one, onto or both.
	- trigonometric functions are not one-one and onto over their natural domains and ranges and hence their inverses do not exist.
- basic concepts
	- sine function, i.e., sine : R -> [-1, 1]
	- cosine function, i.e., cos: R -> [-1, 1]
	- tangent function, i.e., tan : R - { x : x = (2n + 1) $\frac{\pi}{2}$, n \in Z} -> R
	- cotangent function, i.e., cot : R - {x : x = n\pi, n \in Z} -> R
	- secant function, i.e., sec : R - {x : x = (2n + 1) $\frac{\pi}{2}$, n \in Z} -> R - (-1, 1)
	- cosecant function, i.e., cosec : R - {x : x = n\pi, n \in Z} -> R - (-1, 1)
	- if f : X -> Y such that f(x) = y is one-one and onto, then we can define a unique function g : Y -> X such that g(y) = x, where $x \in X$ and $y = f(x)$, $y \in Y$. here, the domain of g = range of f and the range of g = domain of f. the function g is called the inverse of f and is denoted by $f^{-1}$. further, g is also one-one and onto and inverse of g is f. thus, $g^{-1} = (f^{-1})^{-1} = f$. we also have
	  $(f^{-1} \circ f) (x) = f^{-1} (f (x)) = f^{-1} (y) = x$
	  $(f \circ f^{-1}) (y) = f (f^{-1} (y)) = f(x) = y$
	- sine function
		- since the domain of sine function is the set of all real numbers and range is the closed interval [-1, 1]. if we restrict its domain to $\left[ \frac{-\pi}{2}, \frac{\pi}{2} \right]$, then it becomes one-one and onto with range [-1, 1].
		- actually, sine function restricted to any of the intervals $\left[ \frac{-3\pi}{2}, \frac{-\pi}{2} \right]$, $\left[ \frac{-\pi}{2}, \frac{\pi}{2} \right]$, $\left[ \frac{\pi}{2}, \frac{3\pi}{2} \right]$ etc., is one-one and its range is [-1, 1]. we can, therefore, define the inverse of sine function in each of these intervals.
		- we denote the inverse of sine function by $sin^{-1}$ (arc sine function). thus $sin^{-1}$ is a function whose domain is [-1, 1] and range could be any of the intervals $\left[ \frac{-3\pi}{2}, \frac{-\pi}{2} \right]$, $\left[ \frac{-\pi}{2}, \frac{\pi}{2} \right]$, or $\left[ \frac{\pi}{2}, \frac{3\pi}{2} \right]$, and so on.
		- corresponding to each such interval, we get a branch of the function $sin^{-1}$.
		- the branch with range $\left[ \frac{-\pi}{2}, \frac{\pi}{2} \right]$ is called the principal value branch, whereas other intervals as range give different branches of $sin^{-1}$.
		- when we refer o the function $sin^{-1}$, we take it as the function whose domain is [-1, 1] and range is $\left[ \frac{-\pi}{2}, \frac{\pi}{2} \right]$. we write $sin^{-1} : [-1, 1]$ -> $\left[ \frac{-\pi}{2}, \frac{\pi}{2} \right]$
		- from the definition of the inverse functions, it follows that sin ($sin^{-1} x$) = x if $-1 \leq x \leq 1$ 
		  and $sin^{-1}$ (sin x) = x if $\frac{-\pi}{2} \leq x \leq \frac{\pi}{2}$
		  in other words, if y = $sin^{-1} x$, then sin y = x
		- remarks
			- if y = f(x) is an invertible function, then $x = f^{-1}(y)$.
			  collapsed:: true
				- sine function
					- thus, the graph of $sin^{-1} x$ function can be obtained from the graph of original function by interchanging x and y axes, i.e., if (a, b) is a point on the graph of sine function, then (b, a) becomes corresponding point on the graph of inverse sine function. thus, the graph of the function y = $sin^{-1} x$ can be obtained from the graph of y = sin x by interchanging x and y axes. the graphs of y = sin x and y = $sin^{-1} x$ are given in figures. the dark portion of the graph of y = $sin^{-1} x$ represent the principal value branch.
					- ![image.png](../assets/image_1787741035663_0.png)
					- it can be shown that the graph of an inverse function   can be obtained from the corresponding graph of original function as a mirror image (i.e., reflection) along the line y = x.
				- cosine function
				  collapsed:: true
					- like sine function, the cosine function is a function whose domain is the set of all real numbers and range is the set [-1, 1]. if we restrict the domain of cosine function to [0, \pi], then it becomes one-one and onto with range [-1, 1]. actually, cosine function restricted to any of the intervals [-\pi, 0], [0, \pi], [\pi, 2\pi] etc., is bijective with range as [-1, 1]. we can therefor define the inverse of cosine function in each of these intervals. we denote the inverse of the cosine function by $cos^{-1}$ (arc cosine function). thus, $cos^{-1}$ is a function whose domain is [-1, 1] and range could be any of the intervals [-\pi, 0], [0, \pi], [\pi, 2\pi] etc. Corresponding to each such interval, we get a branch of the function $cos^{-1}$. the branch with range [0, \pi] is called the principal value branch of the function $cos^{-1}$. we write
					  $cos^{-1}$ : [-1, 1] -> [0, \pi]. the graphs of y = cos x and y = $cos^{-1}$ x are given in figures.
					- ![image.png](../assets/image_1787743497161_0.png)
					- ![image.png](../assets/image_1787743534988_0.png)
				- $cosec^{-1}$x function
					- since, cosec x = $\frac{1}{sin x}$, the domain of the cosec function is the set $\{x : x \in R\ and\ x \neq n\pi, n \in Z\}$ and the range is the set $\{y : y \in R, y \geq 1\ or\ y \leq -1 \}$ i.e., the set R-(-1, 1). it means that y = cosec x assumes all real values except -1 < y < 1 and is not defined for integral multiple of \pi. if we restrict the domain of cosec function to $\left[ \frac{-\pi}{2}, \frac{\pi}{2} \right] - \{0\}$, the it is one to one and onto with its range as the set R-(-1, 1). actually, cosec function restricted to any of the intervals $\left[ \frac{-3\pi}{2}, \frac{-\pi}{2} \right]-\{-\pi\}$, $\left[ \frac{-\pi}{2}, \frac{\pi}{2} \right] - \{0\}$,$\left[ \frac{\pi}{2}, \frac{3\pi}{2} \right]-\{\pi\}$ etc., is bijective and its range is the set of all real numbers R-(-1,1). thus, $cosec^{-1}$ can be defined as a function whose domain is R-(-1,1) and range could be any of the intervals $\left[ \frac{-3\pi}{2}, \frac{-\pi}{2} \right]-\{-\pi\}$, $\left[ \frac{-\pi}{2}, \frac{\pi}{2} \right] - \{0\}$,$\left[ \frac{\pi}{2}, \frac{3\pi}{2} \right]-\{\pi\}$ etc. the function corresponding to the range $\left[ \frac{-\pi}{2}, \frac{\pi}{2} \right] - \{0\}$ is called the principal value branch of $cosec^{-1}$. we thus have principal branch as 
					  $\cosec^{-1} : \mathbb{R} - (-1, 1) \to [-\tfrac{\pi}{2}, \tfrac{\pi}{2}] - \{0\}$
					- graphs of y = cosec x and y = $cosec^{-1}$ x
						- ![image.png](../assets/image_1787745995736_0.png)
			- $sec^{-1}$x function
			  collapsed:: true
				- sec x = $\frac{1}{cos\ x}$, the domain of y = sec x is the $set\ \mathbb{R} - \{x : x = (2n + 1) \frac{\pi}{2}, n \in Z\}$ and range is the set R-(-1, 1). it means that sec (secant function) assumes all real values except -1 < y < 1 and is not defined for odd multiples of $\frac{\pi}{2}$. if we restrict the domain of secant function [0, \pi] - {$\frac{\pi}{2}$}, then it is one-one and onto with its range as the set R-(-1,1). actually, secant function restricted to any of the intervals [-\pi, 0] - {-$\frac{\pi}{2}$}, [0, \pi] - {$\frac{\pi}{2}$}, [\pi, 2\pi] - {$\frac{3\pi}{2}$} etc., is bijective and its range is R-(-1,1). thus $sec^{-1}$ can be defined as a function whose domain is R-(-1, 1) and range could be any of the intervals [-\pi, 0] - {-$\frac{\pi}{2}$}, [0, \pi] - {$\frac{\pi}{2}$}, [\pi, 2\pi] - {$\frac{3\pi}{2}$} etc. corresponding to each of these intervals, we get different branches of the function $sec^{-1}$. the branch with range [0, \pi] - {$\frac{\pi}{2}$} is called the principal value branch of the function $sec^{-1}$. we thus have
				  $sec^{-1}$ : R-(-1,1) -> [0, \pi] -{$\frac{\pi}{2}$}
				- the graphs of y = sec x and y = $sec^{-1}$ x
					- ![image.png](../assets/image_1787748015200_0.png)
			- $tan^{-1}$ function
			  collapsed:: true
				- the domain of the tan function (tangent function) is the set $\{x : x \in \mathbb{R}\ and\ x \neq (2n+1)\frac{\pi}{2}, n \in Z\}$ and the range is $\mathbb{R}$. it means that tan function is not defined for odd multiples of $\frac{\pi}{2}$. if we restrict the domain of tangent function to $\left[ \frac{-\pi}{2}, \frac{\pi}{2} \right]$, then it is one-one and onto with its range as $\mathbb{R}$. actually, tangent function restricted to any of the intervals $\left[ \frac{-3\pi}{2}, \frac{-\pi}{2} \right]$, $\left[ \frac{-\pi}{2}, \frac{\pi}{2} \right]$, $\left[ \frac{\pi}{2}, \frac{3\pi}{2} \right]$ etc., is bijective and its range is $\mathbb{R}$. thus $tan^{-1}$ can be defined as a function whose domain is $\mathbb{R}$ and range could be any of the intervals $\left[ \frac{-3\pi}{2}, \frac{-\pi}{2} \right]$, $\left[ \frac{-\pi}{2}, \frac{\pi}{2} \right]$, $\left[ \frac{\pi}{2}, \frac{3\pi}{2} \right]$ and so on. these intervals give different branches of the function $tan^{-1}$. the branch with range $\left[ \frac{-\pi}{2}, \frac{\pi}{2} \right]$ is called the principal value branch of the function $tan^{-1}$.
				  we thus have $tan^{-1} : \mathbb{R} \to \left[ \frac{-\pi}{2}, \frac{\pi}{2} \right]$
				- the graphs of the function y = tan x and y = $tan^{-1}$ x
				- ![image.png](../assets/image_1787802493036_0.png)
			- $cot^{-1}$ function
			  collapsed:: true
				- domain of the cot function (cotangent function) is the set $\{x : x \in \mathbb{R}\ and\ x \neq (n\pi, n \in Z\}$ and range is $\mathbb{R}$. it means that cotangent function is not defined for integral multiples of \pi. if we restrict the domain of cotangent function to (0, \pi), then is bijective with and its range as $\mathbb{R}$. in fact, cotangent function restricted to any of the intervals (-\pi, 0), (0, \pi), (\pi, 2\pi) etc., is bijective and its range is $\mathbb{R}$. thus $cot^{-1}$ can be defined as a function whose domain is the $\mathbb{R}$ and range as any of the intervals (-\pi, 0), (0, \pi), (\pi, 2\pi) etc. these intervals give different branches of the function $cot^{-1}$. the function with range (0, \pi) is called the principal value branch of the function $cot^{-1}$. we thus have
				  $cot^{-1} : $\mathbb{R}$ \to (0, \pi)$
				- the graphs of y = cot x and y = $cot^{-1}$ x
					- ![image.png](../assets/image_1787806298120_0.png)
			- inverse trigonometric function (principal value branches) with their domains and ranges
			  collapsed:: true
				- \begin{aligned}
				  \sin^{-1} & : & [-1, 1] & \to & \left[ -\frac{\pi}{2}, \frac{\pi}{2} \right] \\
				  \cos^{-1} & : & [-1, 1] & \to & \left[ 0, \pi \right] \\
				  \cosec^{-1} & : & \mathbb{R}-(-1, 1) & \to & \left[ -\frac{\pi}{2}, \frac{\pi}{2} \right] - {0} \\
				  \sec^{-1} & : & \mathbb{R}-(-1, 1) & \to & \left[ 0, \pi \right] - {\frac{\pi}{2}} \\
				  \tan^{-1} & : & \mathbb{R} & \to & \left[ -\frac{\pi}{2}, \frac{\pi}{2} \right] \\
				  \cot^{-1} & : & \mathbb{R} & \to & \left[ 0, \pi \right]
				  \end{aligned}
			- $sin^{-1}\ x$ should not be confused with $(sin\ x)^{-1}$. in fact $(sin\ x)^{-1} = \frac{1}{sin\ x}$ and similarly for other trigonometric functions
			- whenever no branch of an inverse trigonometric functions is mentioned, we mean the principal value branch of that function
			- the value of an inverse trigonometric functions which lies in the range of principal branch is called the principal value of that inverse trigonometric functions
- properties of inverse trigonometric functions
	- if $y = sin^{-1} x$, then x = sin y and if x = sin y, then $y = sin^{-1} x$ this is equivalent to 
	  $sin (sin^{-1} x) = x, x \in [-1, 1]$ and $sin^{-1} (sin x) = x, x \in \left[ \frac{-\pi}{2}, \frac{\pi}{2} \right]$ same is true for other five inverse trigonometric functions as well.
	- property 1:
		- $sin^{-1}\frac{1}{x} = cosec^{-1} x, x \geq 1 or x \leq -1$
		- $cos^{-1}\frac{1}{x} = sec^{-1} x, x \geq 1 or x \leq -1$
		- $tan^{-1}\frac{1}{x} = cot^{-1} x, x > 0$
	- property 2:
		- $sin^{-1}(-x) = -sin^{-1} x, x \in [-1, 1]$
		- $tan^{-1}(-x) = -tan^{-1} x, x \in \mathbb{R}$
		- $cosec^{-1}(-x) = -cosec^{-1} x, |x| \geq 1$
	- property 3:
		- $cos^{-1}(-x) = \pi - cos^{-1} x, x \in [-1, 1]$
		- $sec^{-1}(-x) = \pi - sec^{-1} x, |x| \geq 1$
		- $cot^{-1}(-x) = \pi - cot^{-1} x, x \in \mathbb{R}$
	- property 4:
		- $sin^{-1}x + cos^{-1}x = \frac{\pi}{2}, x \in [-1, 1]$
		- $tan^{-1}x + cot^{-1}x = \frac{\pi}{2}, x \in \mathbb{R}$
		- $cosec^{-1}x + sec^{-1}x = \frac{\pi}{2}, |x| \geq 1$
	- property 5:
		- $tan^{-1}x + tan^{-1}y = tan^{-1}\frac{x + y}{1 - xy}, xy < 1$
		- $tan^{-1}x - tan^{-1}y = tan^{-1}\frac{x - y}{1 + xy}, xy > -1$
	- property 6:
		- $2tan^{-1}x = sin^{-1} \frac{2x}{1 + x^2}, |x| \leq 1$
		- $2tan^{-1}x = cos^{-1} \frac{1-x^2}{1 + x^2}, |x| \geq 0$
		- $2tan^{-1}x = tan^{-1} \frac{2x}{1 - x^2}, -1 < x < 1$