# Homework Assignment 3


**Problem 1: A Game of Chance (Weight 3)**. You can enter in a game where you get to flip a fair coin 20 times, 
and you will receive $100 any time you get a “Head” after two consecutive “Tail”. 
If you need to pay $250 to enter in the game, estimate the expected reward using Monte Carlo simulation. 

- This experiment involves 20 random events {E_1,E_2,E_3,…,E_20}, where each event E_i results in 
either of two outcomes {Head, Tail}.
- Whenever {Tail, Tail, Head} occurs, we receive $100. So if we use random variable X to denote the total reward, then: 
	- X=$0-$250=-$250 if {Tail, Tail, Head} never occurs
	- X=$100-$250=-$150 if {Tail, Tail, Head} occurs once
	- X=$200-$250=-$50 if {Tail, Tail, Head} occurs twice
	- And so on… 
- Our goal is to estimate "E"[X]. 

Let $\text{S}_1(N) = \sum_{p=1}^N \text{E}(p)$
	
Develop a simulation model to get 1000 realization of X. 
Print the average of these realizations as an estimate for "E"[X].

*Hints*: Create a 'class Game that has a method attribute 
Simulate() that flips a coin 20 times, 
find the number of times that {Tail, Tail, Head} occurs, and return the reward (as calculated above). 

**Problem 2: A Game of Chance with an Unfair Coin (Weight 1)**. 
Modify your model for Problem 1 so that you can specify the probability that a 
coin flip results in head. What is the average reward when this probability is 0.4?
