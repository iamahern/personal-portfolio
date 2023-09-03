# Personal Portolio
Description of OpenSource and Major Academic Projects

Index:
* [Work/Personal Projects](#workpersonal-projects)
  * [IfInjector](#ifinjector) - C# dependency injection framework
  * [Runas User Credential Access Jenkins Plugin](#runas-user-credential-access-jenkins-plugin)
* [Academic (GATech)](#academic-projects)
  * [Computational Photography](#computational-photography)
  * [Reinforcement Learning](#reinforcement-learning)


## Work/Personal Projects

### IFInjector

GitHub [IfInjector](https://github.com/iamahern/IfInjector)

This was a personal project resulting from a decision to learn C#. The project originally started as a fork of the fFastInjector framework, but was eventually completely rewritten for performance. For a brief few days the framework was near the top of some of the C# dependency injection framework benchmarks. You can find some references to the project on the internet archive:
https://web.archive.org/web/20180611033508/https://github.com/danielpalme/IocPerformance

The projet was just for fun. Professionally, I would have used an off the shelf IoC project.

### Runas User Credential Access Jenkins Plugin

GitHub [Runas User Credential Access Jenkins Plugin](https://github.com/iamahern/runas-user-credential-access-project)

This plugin allows for user private credentials to be accessed by specially authorized Jenkins jobs without a user needing to select them explicitly in a drop down. One constraint of Jenkins is that private credentials cannot be forwarded to chained jobs. By allowing this propagation, the plugin allowed for chaining of automation jobs utilizing a user's personal credentials. All cloud operations were thus executed with a user's personal API key and GitHub / config changes using a personal access token. In both cases, this results in both an audit of the user carrying out the admin operation as well as the git / config change operations. Revoking the user from either the production git config repository OR the production cloud account resulted in the user being unable to perform production changes via Jenkins.

## Academic Projects

### Computational Photography

GA Course Link: https://omscs.gatech.edu/cs-6475-computational-photography

#### Access to Code

Instructions [here](gatech/README.md)

#### Course Overview

_This class explores how computation impacts the entire workflow of photography, which is traditionally aimed at capturing light from a (3D) scene to form a (2D) image. A detailed study of the perceptual, technical and computational aspects of forming pictures, and more precisely, the capture and depiction of reality on a (mostly 2D) medium of images, is undertaken over the entire term. The scientific, perceptual, and artistic principles behind image-making will be emphasized, especially as impacted and changed by computation. Topics include the relationship between pictorial techniques and the human visual system; intrinsic limitations of 2D representations and their possible compensations; and technical issues involving capturing light to form images. Technical aspects of image capture and rendering, and exploration of how such a medium can be used to its maximum potential, will be examined. New forms of cameras and imaging paradigms will be introduced._

#### Projects

##### Weekly Assignments

The weekly assignments for this course span creating a homemade pinhole camera to implementing panorama and HDR algorithms. The code for these assignments are not included (either here or on the Drive site), but the results can be seen in the [portfolio pdf](comp_photo_portfolio.pdf).

##### Mid Term

The midterm involved replicating the results of the Avidan &amp; Shamir paper [_Seam Carving for Content-Aware Image Resizing_](https://perso.crans.org/frenoy/matlab2012/seamcarving.pdf). he major premise of the work is that the ‘visually’ optimal means for scaling (retargeting) an image is to utilize low energy (non-edge pixels) flat regions of the image but contain​ ​the​ ​path​ ​to​ ​be​ ​spatially​ ​consistent​ ​(follow​ ​a​ ​contiguous​ ​seam). The paper implements a fast Dynamic Programming algorithm for implementing image retargeting. 

#### Final Project

In the final project I attempted to replicate of the Rubinstein et al. paper [_Improved Seam Carving for Video Retargetting_](http://www.eng.tau.ac.il/~avidan/papers/vidret.pdf). The paper implements image retargetting over 3-dimentionsal video cubes (XY-Time). The paper utilizes a graph-cut algorithm for finding the low energy "seam" to extract. In addition, it presents an _improved_ algorithm for finding low energy seams.

Although I correctly reimplemented the paper in 2-dimensions, the paper utilized "zoning" a "sleeve" of pixels out of the video cube for retargetting by downsampling the video. The video resample was only implemented in the XY access, resulting in slow seam extraction as well as lack luster results. In 2D, I validated that the results obtained match the Avidan &amp; Shamir in 2D suggesting that the graph cut algorithm was correctly implemented.

### Reinforcement Learning

GA Course Link: https://omscs.gatech.edu/cs-7642-reinforcement-learning

#### Access to Code

Instructions [here](academic-code-access.md)

#### Course Overview

_The course explores automated decision-making from a computational perspective through a combination of classic papers and more recent work. It examines efficient algorithms, where they exist, for learning single-agent and multi-agent behavioral policies and approaches to learning near-optimal decisions from experience._

_Topics include Markov decision processes, stochastic and repeated games, partially observable Markov decision processes, reinforcement learning, deep reinforcement learning, and multi-agent deep reinforcement learning. Of particular interest will be issues of generalization, exploration, and representation. We will cover these topics through lecture videos, paper readings, and the book Reinforcement Learning by Sutton and Barto._

#### Projects

Detailed assignment description, code and write ups are accessible from the link above.

##### Project 01

Understanding and replication of the results Richard Sutton's 1988 paper ["Learning to Predict by Methods of Temporal Differences"](http://incompleteideas.net/papers/sutton-88-with-erratum.pdf).

##### Project 02

Extend reinforcement learning to generalizable solutions utilizing Deep (although not that deep) Reinforcement Learning. In this project a Deep Q-Learner was trained to land a "lunar lander" utilizing the [OpenAI Gym environment](https://www.gymlibrary.ml/). The system "learns" to land the lander utilizing feedback from the environment.

This project was finished down to the wire and could have used another 12+ hours of training. Back story - I had been strugglying with this and finally got the code close to the deadline. The model did not have sufficient time to converge on an optimial solution; thankfully they were good enough to submit. The project made me rue my mac's software based TensorFlow implementation. This is a good reminder that Mac's are not always the best development system.

##### Project 03

This project involves replicating Figures 3(parts a-d) of the 2004 paper ["Correlated Q-Learning"](https://www.aaai.org/Papers/ICML/2003/ICML03-034.pdf) by Amy Greenwald and Keith Hall. The paper:

> ... introduces Correlated-Q (CE-Q) learning, a multiagent Q-learning algorithm based on the correlated equilibrium (CE) solution concept. CE-Q generalizes both Nash- Q and Friend-and-Foe-Q: in general-sum games, the set of correlated equilibria contains the set of Nash equilibria; in constantsum games, the set of correlated equilibria contains the set of minimax equilibria. This paper describes experiments with four variants of CE-Q, demonstrating empirical convergence to equilibrium policies on a testbed of general-sum Markov games.