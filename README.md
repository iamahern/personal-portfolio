# Personal Portolio
Description of OpenSource and Major Academic Projects

Index:
* Personal projects
  * [IfInjector](#ifinjector)

* [Academic (GATech)](#academic-projects)
  * [Reinforcement Learning](#reinforcement-learning)
  * TODO - see below


# TODO

Will update with Academic Projects by EOD 4rd July


# Personal Projects

## IFInjector

GitHub [IfInjector](https://github.com/iamahern/IfInjector)

Decided to learn C# to gain an understanding of the language features available there (vs. Java). Experimented with frameworks for developing cross platform mobile applications using C#. I found options for "mobile capable" dependency injection frameworks lacking and decided to write my own. I also used this as an opportunity to learn the LINQ framework which provides a means to compile expressions into byte-code (on non-mobile platforms).

The project originally started as a fork of the fFastInjector framework, but was eventually rewritten for performance. For a brief few days the framework was near the top of some of the C# dependency injection framework benchmarks. You can find some references to the project on the internet archive:
https://web.archive.org/web/20180611033508/https://github.com/danielpalme/IocPerformance


# Academic Projects

For security and academic honesty, my academic projects from Georgia Tech are stored separately on Google drive. Below are descriptions of the projects. There is a password protected link to access sources. The password has been communicated separately.

Password protected link to Georgia Tech projects folder:
> [Georgia Tech Projects Folder](https://jstrieb.github.io/link-lock/#eyJ2IjoiMC4wLjEiLCJlIjoiZVZ2TFc0MjVDTkZjbFZTa1hUTzRYY1pqRWducDczWTFpdTJaYlF5ak1KSlk2UmZ4WExHak9kUjBFLzhCL2xrNnE2MkpIT3NBU3J1c09Tbk0xRm1VeFNiODUvWmdlN0Vkam1IUHpMTWZpYUg3Y2pjNEZ5MUZCQWJiYk9HUkRtL0JIME1tSEE9PSIsInMiOiJnaFoya1lBY3Z0Q3Y1V1l1M3ZRKzZnPT0iLCJpIjoicEVxY1kwSkJmWU95dWhWYSJ9)

**NOTE** All content below is accessible via this link


## Reinforcement Learning

GA Course Link: https://omscs.gatech.edu/cs-7642-reinforcement-learning


### Course Overview

_The course explores automated decision-making from a computational perspective through a combination of classic papers and more recent work. It examines efficient algorithms, where they exist, for learning single-agent and multi-agent behavioral policies and approaches to learning near-optimal decisions from experience._

_Topics include Markov decision processes, stochastic and repeated games, partially observable Markov decision processes, reinforcement learning, deep reinforcement learning, and multi-agent deep reinforcement learning. Of particular interest will be issues of generalization, exploration, and representation. We will cover these topics through lecture videos, paper readings, and the book Reinforcement Learning by Sutton and Barto._


### Projects

Detailed assignment description, code and write ups are accessible from the link above.


**Project 01**

Understanding and replication of the results Richard Sutton's 1988 paper ["Learning to Predict by Methods of Temporal Differences"](http://incompleteideas.net/papers/sutton-88-with-erratum.pdf).


**Project 02**

Extend reinforcement learning to generalizable solutions utilizing Deep (although not that deep) Reinforcement Learning. In this project a Deep Q-Learner was trained to land a "lunar lander" utilizing the [OpenAI Gym environment](https://www.gymlibrary.ml/). The system "learns" to land the lander utilizing feedback from the environment.

This project was finished down to the wire and could have used another 12+ hours of training. Back story - I kicked off a hail mary training run at 1.30am and got up at 5.30am to check intermediate results; thankfully they were good enough to submit. The project made me rue my mac for its poorly optimized TensorFlow implementation. This is a good reminder that Mac's are not always the best development system.


**Project 03**

This project involves replicating Figures 3(parts a-d) of the 2004 paper ["Correlated Q-Learning"](https://www.aaai.org/Papers/ICML/2003/ICML03-034.pdf) by Amy Greenwald and Keith Hall. The paper:

> ... introduces Correlated-Q (CE-Q) learning, a multiagent Q-learning algorithm based on the correlated equilibrium (CE) solution concept. CE-Q generalizes both Nash- Q and Friend-and-Foe-Q: in general-sum games, the set of correlated equilibria contains the set of Nash equilibria; in constantsum games, the set of correlated equilibria contains the set of minimax equilibria. This paper describes experiments with four variants of CE-Q, demonstrating empirical convergence to equilibrium policies on a testbed of general-sum Markov games.
