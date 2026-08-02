- /up
- introduction
	- one key basis for mathematical thinking is deductive reasoning.
	- deduction is `given a statement to be proven, often called a conjecture or a theorem in mathematics, valid deductive steps are derived and a proof may or may not be established, i.e., deduction is the application of a general case to a particular case`
	- in contrast to deduction, inductive reasoning depends on working with each case, and developing a conjecture by observing incidences till we have observed each and every case. it is frequently used in mathematics and is a key aspect of scientific reasoning, where collecting and analysing data is the norm. induction means the generalisation from particular cases or facts. in algebra or in other discipline of mathematics, there are certain results or statements that are formulated in terms of n, where n is a positive integer. to prove such statements the well-suited principle that is used-based on the specific technique, is known as the `principle of mathematical induction`.
	- in mathematics, we use a form of complete induction called mathematical induction
	- the set of natural numbers N is a special ordered subset of the real numbers. In fact, N is the smallest subset of R with the following property:
	  A set S is said to be an inductive set if 1 \in S and x + 1 \in S whenever x \in S. Since
	  N is the smallest subset of R which is an inductive set, it follows that any subset of R
	  that is an inductive set must contain N.
- the principle of mathematical induction
	- the principle of mathematical induction is one such tool which can be used to prove a wide variety of mathematical statements. each such statement is assumed as P(n) associated with positive integer n, for which the correctness for the case n = 1 is examined. then assuming the truth of P(k) for some positive integer k, the truth of P(k+1) is established.
	- suppose there is a given statement P(n) involving the natural number n such that
		- i) the statement is true for n = 1, i.e., P(1) is true, and
		- ii) if the statement is true for n = k (where k is some positive integer), then the statement is also true for n = k + 1, i.e., truth of P(k) implies the truth of P(k+1)
		- then, P(n) is true for all natural numbers n
		- property (i) is simply a statement of fact.
		- property (ii) is a conditional property. it does not assert that the given statement is true for n = k, but only that if it is true for n = k, then it is also true for n = k +1. so, to prove that the property holds, only prove that conditional proposition: 
		  if the statement is true for n = k, then it is also true for n = k + 1. 
		  this is sometimes referred to as the inductive step. 
		  the assumption that the given statement is true for n = k in this inductive step is called the inductive hypothesis.