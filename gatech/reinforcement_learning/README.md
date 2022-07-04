## Reinforcement Learning

GA Course Link: https://omscs.gatech.edu/cs-7642-reinforcement-learning


### Access to Code

Instructions [here](../README.md)


### Course Overview

_The course explores automated decision-making from a computational perspective through a combination of classic papers and more recent work. It examines efficient algorithms, where they exist, for learning single-agent and multi-agent behavioral policies and approaches to learning near-optimal decisions from experience._

_Topics include Markov decision processes, stochastic and repeated games, partially observable Markov decision processes, reinforcement learning, deep reinforcement learning, and multi-agent deep reinforcement learning. Of particular interest will be issues of generalization, exploration, and representation. We will cover these topics through lecture videos, paper readings, and the book Reinforcement Learning by Sutton and Barto._


### Projects

Detailed assignment description, code and write ups are accessible from the link above.


#### Project 01

Understanding and replication of the results Richard Sutton's 1988 paper ["Learning to Predict by Methods of Temporal Differences"](http://incompleteideas.net/papers/sutton-88-with-erratum.pdf).


#### Project 02

Extend reinforcement learning to generalizable solutions utilizing Deep (although not that deep) Reinforcement Learning. In this project a Deep Q-Learner was trained to land a "lunar lander" utilizing the [OpenAI Gym environment](https://www.gymlibrary.ml/). The system "learns" to land the lander utilizing feedback from the environment.

This project was finished down to the wire and could have used another 12+ hours of training. Back story - I kicked off a hail mary training run at 1.30am and got up at 5.30am to check intermediate results; thankfully they were good enough to submit. The project made me rue my mac for its poorly optimized TensorFlow implementation. This is a good reminder that Mac's are not always the best development system.


#### Project 03

This project involves replicating Figures 3(parts a-d) of the 2004 paper ["Correlated Q-Learning"](https://www.aaai.org/Papers/ICML/2003/ICML03-034.pdf) by Amy Greenwald and Keith Hall. The paper:

> ... introduces Correlated-Q (CE-Q) learning, a multiagent Q-learning algorithm based on the correlated equilibrium (CE) solution concept. CE-Q generalizes both Nash- Q and Friend-and-Foe-Q: in general-sum games, the set of correlated equilibria contains the set of Nash equilibria; in constantsum games, the set of correlated equilibria contains the set of minimax equilibria. This paper describes experiments with four variants of CE-Q, demonstrating empirical convergence to equilibrium policies on a testbed of general-sum Markov games.
