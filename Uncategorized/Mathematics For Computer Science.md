---
Title: Mathematics For Computer Science
Source: https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-042j-mathematics-for-computer-science-fall-2010
---
Type: [[Lecture]] 
Author: [[Tom Leighton]]
Subject: [[Mathematics]] [[Computer Science]]
Status: [[In Progress]]
Abstract:

Summary:
Lecture 2
	Proof by Contradiction:
				Proving that an assumption was wrong, therefore its opposite must be true.
				Example $$\text{Theorem: }\sqrt2\text{ is irrational}$$
				Proof: (By Contradiction) <- Always specify
				Assume that $$\sqrt2$$ is rational
				$$\sqrt2 = a/b$$
				Then $$ 2 = a^2/b^2 $$
				Then $$a^2 = 2b^2$$ which means $$ a \text{ is even } = (2|a)$$ And also means that 4 divides a^2 $$4|a^2$$ Which means $$4|2b^2 = 2|b^2 = \text{b is even}$$ Which means $$a/b \text{ is not in lowest terms}$$ Which is a contradiction therefore:
				$$\sqrt{2}\text{ is irrational}$$ 	
	Induction:
		The most widely used technique in computer science. It is really just an axiom. 
			Let $P(n)$ be a predicate if $P(0)$ is true 
			and $$ \forall n \in \mathbb{N} = \text{For all n in the set of natural numbers} $$ $$ P(n) \implies P(n+1) \text{ is true}$$ then  $$ \forall n \in \mathbb{N} \ P(n) \text{ is true}$$
			Basically if $P(0)$ implies $P(1)$ is true and $P(0)$ is true then $P(1)$ is true and so on forever.
		An example:
			$$\forall n \geq 0 \ \ \ 1+2+3+...+n = \dfrac{n(n+1)}{2}$$
			Proof: By Induction
				Let $P(n)$ Be the predicate that $$\sum_{i=1}^{n}{i} = \dfrac{n(n+1)}{2}$$
			Base Case:
				$$P(0)\text{ is true}$$$$\sum_{i=1}^{0}{i} = \dfrac{0(0+1)}{2} = \frac{0}{2}=0 \text{ is true}$$
			Inductive Step is proving if $P(0)$ is true, $P(1)$ is true 
			$$\text{For }n \geq0 \text{  show } P(n) \implies P(n+1) \text{ is true}$$
			So you must assume the axiom you are trying to prove is true.
			$$\text{if} \sum_{i=1}^{n}{i} = \dfrac{n(n+1)}{2}$$ then this is true$$1+2+3+...+(n+1) = \dfrac{(n+1)(n+2)}{2} $$
			Having assumed until $n$ that it is equal to $\dfrac{n(n+1)}{2}$ you can simplify to: $$\dfrac{n(n+1)}{2} + (n+1) = \dfrac{(n+1)(n+2)}{2}$$ and check for truth:
				$$\dfrac{n^2 + n}{2}+n+1 = \dfrac{n^2 + n + 2n +2}{2} =  \dfrac{(n+1)(n+2)}{2}$$
			
				
Grokked: