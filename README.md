# Project1_Cs475
Introduction
Monte Carlo simulation is used to determine the range of outcomes for a series of parameters, each of which has a probability distribution showing how likely each option is to happen. In this project, you will take a scenario and develop a Monte Carlo simulation of it, determining how likely a particular output is to happen.

Clearly, this is very parallelizable -- it is the same computation being run on many permutations of the input parameters. You will run this with OpenMP, testing it on different numbers of threads (at least 1, 2, 4, 6, and 8).


The Scenario


A castle sits on top of a cliff. An amateur band of merceneries is attempting to destroy it.

Normally this would be a pretty straightforward geometric calculation, but these are amateurs. What makes them such amateurs you ask? It's because they are not very good at estimating distances, and not very good at aiming their cannon. They can only determine the 5 input parameters within certain ranges.

Your job is to figure out the probability that these doofuses will actually hit the castle. This is a job for multicore Monte Carlo simulation!


Requirements:


The ranges are:
Variable	Meaning	Range
g	Ground distance to the cliff face	10. - 20.
h	Height of the cliff face	20. - 30.
d	Upper deck distance to the castle	10. - 20.
v	Cannonball initial velocity	20. - 30.
θ	Cannon firing angle in degrees	70. - 80.

In addition you are given:
(θ in radians) = (F_PI/180.f) * (θ in degrees)
vx = v*cos(θ in radians)
vy = v*sin(θ in radians)
TOL = 5.0
GRAVITY = -9.8
TOL is how close the cannonball needs to come to the castle to demolish it.
GRAVITY is the acceleration due to gravity. Be sure the minus sign stays there.


Run this for some combinations of trials and threads. Do timing for each combination. Like we talked about in the Project Notes, run each experiment some number of tries, NUMTRIES, and record just the peak performance.

Produce a rectangular table and two graphs. The two graphs need to be:
Performance versus the number of Monte Carlo trials, with the colored lines being the number of OpenMP threads.
Performance versus the number OpenMP threads, with the colored lines being the number of Monte Carlo trials..
(See the Project Notes to see an example of this and how to get Excel to do most of the work for you.)

Chosing one of the runs (the one with the maximum number of trials would be good), tell me what you think the actual probability is.

Compute Fp, the Parallel Fraction, for this computation.

Given this Fp, what is the maximum Speedup you could ever get, no matter how many cores you use?
