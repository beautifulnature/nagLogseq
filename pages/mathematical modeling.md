- ![Class-11-Mathematics-a2_Mathematical_Modelling.pdf](../assets/Class-11-Mathematics-a2_Mathematical_Modelling_1785690280731_0.pdf)
- introduction
	- the process of translation of a real-life problem into a mathematical form can given a better representation and solution of certain problems. the process of translation is called Mathematical Modelling.
- preliminaries
	- steps involved
		- step 1: study the real-life problem, and identify the parameters
		- step 2: formulate the problem mathematically
		- step 3: solution of the problem. interpreting the mathematical solution to the real situation
	- a mathematical model is a representation which comprehends a situation
- what is mathematical modelling
	- definition: mathematical modelling is an attempt to study some part (or form) of the real-life problem in mathematical terms
	- conversion of physical situation into mathematics with some suitable conditions is knows as mathematical modelling. mathematical modelling is nothing but a technique and the pedagogy taken from fine arts and not from the basic sciences.
	- let us now understand the different processes involved in mathematical modelling. 4 steps are involved in this process. as an illustrative example, we consider the modelling done to study the motion of a simple pendulum.
	- understanding the problem
		- this involves, for example, understanding the process involved in the motion of simple pendulum. all of us are familiar with the simple pendulum. this pendulum is simply a mass (known as bob) attached to one end of a string whose other end is fixed at a point. we have studied that the motion of the simple pendulum is periodic. the period depends upon the length of the string and acceleration due to gravity. so, what we need to find is the period of oscillation. based on this, we give a precise statement of the problem as
	- statement
		- how do we find the period of oscillation of the simple pendulum?
		- the next step is formulation.
	- formulation: consists of 2 main steps.
		- identifying the relevant factors
			- in this, we find out what are the factors / parameters involved in the problem. for example, in the case of pendulum, the factors are period of oscillation (T), the mass of the bob (m), effective length (l) of the pendulum which is the distance between the point of suspension to the centre of mass of the bob. here we consider the length of string as effective length of the pendulum and acceleration due to gravity (g), which is assumed to be constant at a place.
			- so we have identified 4 parameters for studying the problem. now, our purpose is to find T. for this we need to understand what are the parameters that affect the period which can be done by performing a simple experiment.
			- we take 2 metal balls of 2 different masses and conduct experiment with each of them attached to 2 strings of equal lengths. we measure the period of oscillation. we make the observation that there is no appreciable change of the period with mass. now, we perform the same experiment on equal mass of balls but take strings of different lengths and observe that there is clear dependence of the period on the length of the pendulum.
			- this indicates that the mass m is not an essential parameter for finding period whereas the length l is an essential parameter.
			- this process of searching the `essential parameters` is necessary before we go to the next step.
		- mathematical description
			- this involves finding an equation, inequality or a geometric figure using the parameters already identified.
			- in the case of simple pendulum, experiments were conducted in which the values of period T were measured for different values of l. these values were plotted on a graph which resulted in a curve that resembled a parabola. it implies that the relation between T and l could be expressed
			  $T^2 = kl$
			  it was found that $k = \frac{4\pi{2}}{g}$. this give the equation
			  $T = 2\pi \sqrt{\frac{l}{g}}$
			  equation gives the mathematical formulation of the problem.
			- finding the solution
				- the mathematical formulation rarely gives the answer directly. usually we have to do some operation which involves solving an equation, calculation or applying a theorem etc. in the case of simple pendulums the solution involves applying the formula given in equation.
				- the period of oscillation calculated for different pendulums having different lengths.
			- interpretation / validation
				- a mathematical model is an attempt to study, the essential characteristic of a real life problem. many times model equations are obtained by assuming the situation in an idealised context. the model will be useful only if it explains all the facts that we would like it to explain. otherwise, we will reject it, or else, improve it, then test it again. in other words, `we measure the effectiveness of the model by comparing the results obtained from the mathematical model, with the known facts about the real problem. this process is called validation of the model`.
				- in the case of simple pendulum, we conduct some experiments on the pendulum and find out period of oscillation. now, we compare the measured values with the calculated values.
				- the difference in the observed values and calculated values gives the error.
				- once we accept the model, we have to interpret the model. `the process of describing the solution in the context of the real situation is called interpretation of the model`. in this case, we can interpret the solution in the following way:
					- a) the period is directly proportional to the square root of the length of the pendulum.
					- b) it is inversely proportional to the square root of the acceleration due to gravity.
				- our validation and interpretation of this model shows that the mathematical model is in good agreement with the practical (or observed) values. but we found that there is some error in the calculated result and measured result. this is because we have neglected the mass of the string and resistance of the medium. so in such situation we look for a better model and this process continues.
				- this leads us to an important observation. the real world is far too complex  to understand and describe completely. we just pick 1 or 2 main factors to be completely accurate that may influence the situation. then try to obtain a simplified model which gives some information about the situation. we study the simple situation with this model expecting that we can obtain a better model of the situation.
				- now, we summarise main process involved in the modelling as
					- a) formulation
					- b) solution
					- c) interpretation / validation
	- example 3
		- a farm house uses at least 800 kg of special food daily. the special food is a mixture of corn and soyabean with the following compositions
			- |material|nutrients present per kg protein|nutrients present per kg fibre|cost per kg|
			  |corn|0.09|0.02|Rs 10|
			  |soyabean|0.6|0.06|Rs 20|
			- the dietary requirements of the special food stipulate at least 30% protein and at most 5% fibre, determine the daily minimum cost of the food mix.
			- solution:
			- step 1: here the objective is to minimise the total daily cost of the food which is made up of corn and soyabean. so the variables (factors) that are to be cosidered are
				- x = the amount of corn
				- y = the amount of soyabean
				- z = the cost
			- step 2
				- z = 10 x +20 y
				- the problem is to minimise z with the following constratints
				- a) the farm used at least 800 kg food consisting of corn and soyabean
				  i.e., $x + y \geq 800$
				- the food should have at least 30% protein dietary requirement in the proportion as given.
				  $0.09x + 0.6y \geq 0.3 (x + y)$
				- food should have at most 5% fibre in the proportion given
				  $0.02 x + 0.06 y \leq 0.05 (x + y)$
				- we simplify the constraints by grouping all the coefficients of x, y
				- then the problem can be restated in the following mathematical form
				- statement: minimize z subject to
				  $x + y \geq 800$
				  $0.21 x - 0.3 y \leq 0$
				  $0.03 x - 0.01 y \geq 0$
				- this give the formulation of the model
		- step 3
			- this can be solved graphically. the shaded region gives the possible solution of the equations. from the graph is is clear that the minimum value is got the point (470.6, 329.4)
			- this gives the value of z as z = 10 x 470.6 + 20 x 329.4 = 11294
			- this is the mathematical solution
		- step 4
			- the solution can eb interpreted as saying that, "the minimum cost of the special food with corn and soyabean having the required portion of nutrient contents, protein and fibre is Rs 11294 and we obtain this minimum cost if we use 470.6 kg of corn and 329.4 kg of soyabean"
	- example 4
		- suppose a population control unit wants to find out "how many people will be there in a certain country after 10 years"
		- step 1:
			- formulation
				- we first observe that the population changes with time and it increases with birth and decreases with deaths.
				- we want to find the population at a particular time. let t denote the time in years. then t takes values 0, 1, 2, ..., t=0 stands for the present time, t = 1 stands for the next year etc. for any time t, let p(t) denote the population in that particular year.
				- suppose we want to find the population in a particular year, say $t_0 = 2006$. how will we do that. we find the population by Jan 1st 2005. add the number of births in that year and subtract the number of deaths in that year. let B(t) denote the number of births in the one year between t and t+1 and D(t) denote the number of deaths between t and t+1. the we get the relation
				  P(t+1) = P(t) + B(t) - D(t)
				- now we make some assumption and definitions
					- $\frac{B(t)}{P(t)}$ is called the `birth rate` for the time interval t to t+1
					- $\frac{D(t)}{P(t)}$ is called the `death rate` for the time interval t to t+1
			- assumptions
				- the birth rate is the same for all intervals, likewise, the death rate is the same for all intervals. this means that there is a constant b, called the birth rate, and a constant d, called the death rate so that, for all $t \geq 0$
				  logseq.order-list-type:: number
				- there is no migration into or out of the population; i.e., the only source of population change is birth and death
				  logseq.order-list-type:: number
				  as a result of assumptions 1 and 2, we deduce that, for $t \geq 0$,
				  P(t +1) = P(t) + B(t) - D(t) = P(t) + bP(t) -dP(t) = (1 + b - d) P(t)
				- setting t = 0, P(1) = (1 + b -  d) P(0)
				- setting t = 1, $P(2) = (1 + b -  d) P(1) = (1 + b -  d) (1 + b -  d) P(0) = (1 + b -  d)^2 P(0)$
				- $P(t) = (1 + b -  d)^t P(0)$
				- for t = 0, 1, 2, ... the constant 1 + b - d is often abbreviated by r and called the `growth rate` or in mor high-flown languate, the `Malthusian parameter`, in honor of Robert Malthus who first brought this model to popular attention. in terms of r, $P(t)  = P(0) r^t$, t = 0, 1, 2, ...
				- P(t) is an example of an `exponential function`. any function of the form $cr^t$, where c and r are constants, is an exponential function.
				- equation gives the mathematical formulation of the problem.
		- step 2: solution
			- suppose the current population is 250,000,000 and the rates are b = 0.02 and d = 0.01. what will the population be in 10 years?
			  $P(10) = (1.01)^{10}(250000000) = 276155531.25$
		- step 3: interpretation and validation
			- naturally, this result is absurd, since one can't have 0.25 of a person. so we do some approximation and conclude that the population is 276155531 (approximately). here, we are not getting the exact answer because of the assumptions that we have made in our mathematical model.
	- since a mathematical model is a simplified representation of a real problem, by its very nature, has built-in assumptions and approximations. obviously, the most important question is to decide whether our mode is a good one or not i.e., when the obtained results are interpreted physically whether or not the model gives reasonable answers. if a model is not accurate enough, we try to identify the sources of shortcomings. it may happen that we need a new formulation, new mathematical manipulation and hence a new evaluation. thus mathematical modelling can be a cycle of the modelling process as shown in the flowchart given below
	- ![image.png](../assets/image_1788432883113_0.png)
	-