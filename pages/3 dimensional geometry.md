- ![Class-12-2-Mathematics-Part-II-05_Three Dimensional Geometry.pdf](../assets/Class-12-2-Mathematics-Part-II-05_Three_Dimensional_Geometry_1786587202980_0.pdf)
- direction cosines and direction ratios of a line
	- if a directed line L passing through the origin makes angles \alpha, \beta, \gamma with x, y, z-axes, called direction angles, then cosine of these angles  cos \alpha, cos \beta, cos \gamma are called direction cosines of the directed line L.
	- if we reverse the direction of L, then the direction angles are replaced by their supplements, i.e., \pi-\alpha, \pi-\beta, \pi-\gamma. thus, the signs of the direction cosines are reversed.
	- ![image.png](../assets/image_1788165049521_0.png)
		- note that a given line in space can be extended in 2 opposite directions and so it has 2 sets of direction cosines. in order to have a unique set of direction cosines for a given line in space, we must take the given line as a directed line. these unique direction cosines are denoted by l, m, n
		- remark: if the given line in space does not pass through the origin, then, in order to find its direction cosines, we draw a line through the origin and parallel to the given line. now take one the directed lines from the origin and find its direction cosines as 2 parallel line have same set of direction cosines.
			- any 3 numbers which are proportional to the direction cosines of a line are called the `direction ratios (direction numbers)` of the line. if l, m, n are direction cosines and a, b, c are direction ratios of a line, then a = \lambda l, b = \lambda m, c = \lambda n, for any nonzero \lambda in $\mathbb{R}$
			- a, b, c be direction ratios of a line and let l, m, n be the direction cosines (d.c's) of the line. then
			  $\frac{l}{a} = \frac{m}{b} = \frac{n}{c} = k$, k being a constant
			  l = ak, m = bk, n = ck
			  $l^2 + m^2 + n^2 = 1$
			  therefore $k^2(a^2 + b^2 + c^2) = 1$
			  $k = \pm \frac{1}{\sqrt{a^2 + b^2 + c^2}}$
			  d.c's of the line are
			  $l = \pm \frac{a}{\sqrt{a^2 + b^2 + c^2}}, m = \pm \frac{b}{\sqrt{a^2 + b^2 + c^2}}, n = \pm \frac{c}{\sqrt{a^2 + b^2 + c^2}}$
			  where, depending on the desired sign of k, either a positive or a negative sign is to be taken for l, m and n
			- for any line if a, b, c are direction ratios of a line, then ka, kb, kc; k \neq 0 is also a set of direction ratios. so, any 2 sets of direction rations of a line are also proportional. also, for any line there are infinitely many sets of direction ratios.
	- relation between the direction cosines of a line
		- ![image.png](../assets/image_1788167886773_0.png)
		- consider a line RS with direction cosines l, m, n. through the origin draw a line parallel to the given line and take a point P(x, y, z) on the line. for P draw a perpendicular PA on the x-axis.
		- OP = r. then $cos \alpha = \frac{OA}{OP} = \frac{x}{r}$. this gives x = lr
		  similarly y = mr, z = nr
		  thus $x^2 + y^2 + z^2 = r^2 (l^2 + m^2 + n^2)$
		  but $x^2 + y^2 + z^2 = r^2$
		  hence $l^2 + m^2 + n^2 = 1$
	- direction cosines of a line passing through 2 points
		- ![image.png](../assets/image_1788169592239_0.png)
		- since one and only one line passes through 2 given points, we can determine the direction cosines of a line passing through the given points $P(x_1, y_1, z_1)$ and $Q(x_2, y_2, z_2)$ as follows
		- l, m, n be the direction cosines of the line PQ and let it makes angles \alpha, \beta, \gamma with x, y, z -axis
		- draw perpendiculars from P and Q to XY-plane to meet at R and S. draw a perpendicular from P to QS to meet at N. now in right angle triangle PNQ, $\angle{PQN} = \gamma$
		  id:: 6a954e34-dc05-4af5-a520-e695b01bd33a
		  therefore $cos \gamma = \frac{NQ}{PQ} = \frac{z_2 - z_1}{PQ}$
		  $cos \alpha = \frac{x_2 - x_1}{PQ}$ and
		  $cos \beta = \frac{y_2 - y_1}{PQ}$
		  hence, the direction cosines of the line segment joining the points $P(x_1, y_1, z_1)$ and $Q(x_2, y_2, z_2)$ are $\frac{x_2 - x_1}{PQ}$, $\frac{y_2 - y_1}{PQ}$, $\frac{z_2 - z_1}{PQ}$
		  where PQ = $\sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2 + (z_2 - z_1)^2}$
		- note: the direction ratios of the line segment joining $P(x_1, y_1, z_1)$ and $Q(x_2, y_2, z_2)$ may be taken as $x_2 - x_1, y_2 - y_1, z_2 - z_1$ or $x_1 - x_2, y_1 - y_2, z_1 - z_2$
- equation of a line in space
	- vector and cartesian equations of a line in space.
	- a line is uniquely determined if
		- it passes through a given point and has given direction or
		- it passes through 2 given points
	- equation of a line through a given point and parallel to a given vector $\overrightarrow{b}$
		- ![image.png](../assets/image_1788170580349_0.png)
		- $\overrightarrow{a}$ be the position vector of the given point A with respect to the origin O of the rectangular coordinate system. l be the line which passes through point A and is parallel to given vector $\overrightarrow{b}$. let $\overrightarrow{r}$ be the position vector of an arbitrary point p on the line.
		- then $\overrightarrow{AP}$ is parallel to the vector $\overrightarrow{b}$ i.e., $\overrightarrow{AP} = \lambda \overrightarrow{b}$, where \lambda is some real number
		  but $\overrightarrow{AP} = \overrightarrow{OP} - \overrightarrow{OA}$
		  $\lambda \overrightarrow{b} = \overrightarrow{r} - \overrightarrow{a}$
		  conversely, for each value of the parameter \lambda, this equation gives the position vector of a point P on the line. hence the vector equation of the line is given by
		  $\overrightarrow{r} = \overrightarrow{a} + \lambda \overrightarrow{b}$
		- remark: if $\overrightarrow{b} = a \hat{i} + b \hat{j} + c \hat{k}$, then a, b, c are direction ratios of the line and conversely, if a, b, c are direction ratios of a line, then $\overrightarrow{b} = a \hat{i} + b \hat{j} + c \hat{k}$ will be the parallel to the line. here, b should not be confused with $|\overrightarrow{b}|$
		- derivation of cartesian form from vector form
			- let the coordinates of the given point A be $(x_1, y_1, z_1)$ and the direction ratios of the line be a, b, c. consider the coordinates of any point P be (x, y, z). then
			  $\overrightarrow{r} = x \hat{i} + y \hat{j} + z \hat{k}$, $\overrightarrow{a} = x_1 \hat{i} + y_1 \hat{j} + z_1 \hat{k}$
			  and $\overrightarrow{b} = a \hat{i} + b \hat{j} + c \hat{k}$
			  substituting in vector equation of the line and equating coefficients of $\hat{i}, \hat{j}, \hat{k}$, we get
			  $x = x_1 + \lambda a; y = y_1 + \lambda b; z = z_1 + \lambda c$
			  $\frac{x - x_1}{a} =\frac{y - y_1}{b} = \frac{z - z_1}{c}$
			  this is the Cartesian equation of the line
			- note: l, m, n are the direction cosines of the line, the equation of the line is $\frac{x - x_1}{l} =\frac{y - y_1}{m} = \frac{z - z_1}{n}$
	- equation of a line passing through 2 given points
		- $\overrightarrow{a}$, $\overrightarrow{b}$ 2 position vectors of 2 points $A(x_1, y_1, z_1)$ and $B(x_2, y_2, z_2)$ that are lying on a line
		- ![image.png](../assets/image_1788250174880_0.png)
		- $\overrightarrow{r}$ be the position vector of an arbitrary point P (x, y, z) then P is a point on the point on the line if and only if $\overrightarrow{AP}$ = $\overrightarrow{r}$ - $\overrightarrow{a}$ and $\overrightarrow{AB}$ = $\overrightarrow{b}$ -$\overrightarrow{a}$ are collinear vectors. therefore, P is on the line if and only if 
		  $\overrightarrow{r} - \overrightarrow{a} = \lambda ( \overrightarrow{b} - \overrightarrow{a})$
		  or $\overrightarrow{r} = \overrightarrow{a} + \lambda ( \overrightarrow{b} - \overrightarrow{a}), \lambda \in \mathbb{R}$
		  this is the vector equation of the line.
		- derivation of cartesian form from vector form
			- $\overrightarrow{r} = x \hat{i} + y \hat{j} + z \hat{k}, \overrightarrow{a} = x_1 \hat{i} + y_1 \hat{j} + z_1 \hat{k}, \overrightarrow{b} = x_2 \hat{i} + y_2 \hat{j} + z_2 \hat{k}$
			  :LOGBOOK:
			  CLOCK: [2026-09-01 Tue 15:32:51]--[2026-09-01 Tue 15:32:53] =>  00:00:02
			  :END:
			  $x \hat{i} + y \hat{j} + z \hat{k} = x_1 \hat{i} + y_1 \hat{j} + z_1 \hat{k} + \lambda [(x_2 - x_1) \hat{i} + (y_2 - y_1) \hat{j} + (z_2 - z_1) \hat{k}$]
			  equating the like coefficients of $\hat{i}, \hat{j}, \hat{k}$, we get
			  $x = x_1 + \lambda (x_2 - x_1); y = y_1 + \lambda (y_2 - y_1); z = z_1 + \lambda (z_2 - z_1)$
			  $\frac{x - x_1}{x_2 - x_1} = \frac{y - y_1} {y_2 - y_1} = \frac{z - z_1}{z_2 - z_1}$
			  which is the equation of the line in Cartesian form
- angle between 2 lines
	- ![image.png](../assets/image_1788257096592_0.png)
	- $L_1, L_2$ be 2 lines passing through the origin and with direction ratios $a_1, b_1, c_1$ and $a_2, b_2, c_2$. P be a point on $L_1$ and Q be a point on $L_2$. consider the directed lines OP, OQ. \theta be the acute angle between OP and OQ. now recall that the directed line segments OP and OQ are vectors with components $a_1, b_1, c_1$ and $a_2, b_2, c_2$. therefore the angle \theta between them is given by
	  $$
	  cos \theta = \begin{vmatrix} \frac{a_1 a_2 + b_1 b_2 + c_1 c_2}{\sqrt{a_1^{2} + b_1^{2} + c_1^{2}} \sqrt{a_2^{2} + b_2^{2} + c_2^{2}}} \end{vmatrix}
	  $$
	  the angle between the lines in terms of 
	  $sin \theta = \sqrt{1 - cos^2 \theta}$
	  $= \sqrt{1 - \frac{(a_1 a_2 + b_1 b_2 + c_1 c_2)^2}{(a_1^{2} + b_1^{2} + c_1^{2}) (a_2^{2} + b_2^{2} + c_2^{2})}}$
	  $= \frac{\sqrt{(a_1^{2} + b_1^{2} + c_1^{2}) (a_2^{2} + b_2^{2} + c_2^{2}) - (a_1 a_2 + b_1 b_2 + c_1 c_2)^2}}{\sqrt{(a_1^{2} + b_1^{2} + c_1^{2})} \sqrt{(a_2^{2} + b_2^{2} + c_2^{2})}}$
	  $= \frac{\sqrt{(a_1 b_2 - a_2 b_1)^{2} + (b_1 c_2 - b_2 c_1)^{2} + (c_1 a_2 - c_2 a_1)^2}}{\sqrt{(a_1^{2} + b_1^{2} + c_1^{2})} \sqrt{(a_2^{2} + b_2^{2} + c_2^{2})}}$
	- note: in case lines $L_1, L_2$ do not pass through the origin, we may take lines $L_1', L_2'$ which are parallel to $L_1, L_2$ and pass through the origin
	- if instead of direction ratios for the line $L_1, L_2$, direction cosines, $l_1, m_1, n_1$ for $L_1$, $l_2, m_2, n_2$ for $L_2$ are given
	  $cos \theta = |l_1 l_2 + m_1 m_2 + n_1 n_2|$ (as $l_1^2 + m_1^2 + n_1^2 = 1 = l_2^2 + m_2^2 + n_2^2$)
	  and $sin \theta = \sqrt {(l_1 m_2 - l_2 m_1)^2 - (m_1 n_2 - m_2 n_1)^2 + (n_1 l_2 - n_2 l_1)^2}$
	- 2 lines with direction ratios $a_1, b_1, c_1$ and $a_2, b_2, c_2$ are
		- perpendicular i.e., if \theta = 90\deg
			- $a_1 a_2 + b_1 b_2 + c_1 c_2 =0$
		- parallel i.e., if \theta = 0
			- $\frac{a_1}{a_2} = \frac{b_1}{b_2} = \frac{c_1}{c_2}$
	- angle between 2 lines when their equations are given. if \theta is acute angle between the lines
		- $\overrightarrow{r} = \overrightarrow{a_1} + \lambda \overrightarrow{b_1}$ and $\overrightarrow{r} = \overrightarrow{a_2} + µ \overrightarrow{b_2}$
		  then $cos \theta = \begin{vmatrix} \frac{\overrightarrow{b_1} \overrightarrow{b_2}}{|\overrightarrow{b_1}| |\overrightarrow{b_2}|} \end{vmatrix}$
		- in Cartesian form, if \theta is the angle between the lines
		  $\frac{x - x_1}{a_1} = \frac{y - y_1}{b_1} = \frac{z - z_1}{c_1}$
		  and $\frac{x - x_2}{a_2} = \frac{y - y_2}{b_2} = \frac{z - z_2}{c_2}$
		  where $a_1, b_1, c_1$ and $a_2, b_2, c_2$ are the direction ratios of the lines then
		  $$
		  cos \theta = \begin{vmatrix} \frac{a_1 a_2 + b_1 b_2 + c_1 c_2}{\sqrt{a_1^{2} + b_1^{2} + c_1^{2}} \sqrt{a_2^{2} + b_2^{2} + c_2^{2}}} \end{vmatrix}
		  $$
- shortest distance between 2 lines
	- distance between 2 skew lines
	- distance between parallel lines
- plane
	- equation of a plane in normal form
	- equation of a plane perpendicular to a given vector and passing through a given point
	- equation of a plane passing through 2 non collinear points
	- intercept form of the equation of a plane
	- plane passing through the intersection of 2 given planes
- coplanarity of 2 lines
- angle between 2 planes
- distance of a point from a plane
- angle between a line and a plane