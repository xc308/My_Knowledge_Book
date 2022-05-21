---
layout: post
title: "What is the relation between deterministic chaos and randomness?"
date: 2022-05-21
---
{% include_relative _includes/head.html %} 

Ref: *L. Mark Berline, Statistics, Probability and Chaos*

*Declear: The copy right and property right all belong to the original author of the paper. Below is just simple copy from the paper and a reading record and note.*

## 2.2 Randomness and Chaos

- reviews various relationships between chaos and randomness
- key ideas involve the interrelations between sensitivity to initial conditions, uncertainty modeling and ergodic theory


### 2.2.1 Uncertainty, chaos and randomness

- how uncertainty, especially in the presence of complexity, naturally leads to the use of random or probabilistic methods

- A primary example of the use of probabilistic methods to partially overcome difficulties in a complex, deterministic setting is statistical mechanics
    * Suppose that the system is such that we can assume that the motion of all the particles are governed by the deterministic laws of motion of classical physics
    * In principle, we should then be able to compute, given all of the requisite initial conditions, the exact future behavior of the entire system. 
    * However, don't know the exact initial conditions
    * In the presence of uncertainty concerning these initial conditions, the motion of the particles (or, at least, observable functions of these motions) not only appear "random," but are successfully modeled via stochastic techniques. 

- The second example: nonlinear dynamical chaos system
  * probabilistic methods have long been suggested in the area of fluid dynamics, particularly, turbulenc
  * If we could know exactly the laws of nature and the situation of the universe at the Initial instant, we should be able to predict the situation of this same universe at a subsequent instant
  * But even when the natural laws should have no further secret for us, we could know the initial situation only approximately. 
  * If that permits us to foresee the succeeding situation with the same degree of approximation, that is all we require, we say the phenomenon had been predicted, that it is ruled by laws
  * But it is not always the case; it may happen that slightly differences in the initial conditions produce very great differ- ences in the final phenomena; a slight error in the former would make an enormous error in the latter


- It includes the mathematical problem of sensitivity to initial conditions
- Poincare's explicit suggestion that we can perceive "chance" to be at works as a result of our uncertainty. 
- Poincare also suggested basically involving the treatment of unknown initial conditions as random.


### 2.2.2 Defining chaotic to be random

- symbolic dynamics
- discrete time dynamical system
- At each iterate, xn, n > 0, of the process, we will associate a simple indicator function based on the location of xn. 
- In particular, suppose we let Yn = 1 if Xn $\in$ S and Yn = 0 otherwise, where S is some subset of D.
- each initial condition of the system is now associated with an infinite sequence of 0's and l's.
- if this definition is satisfied, the deterministic dynamical system is, in a sense, at least as rich as Bernoulli coin tossing


### 2.2.3 Ergodic theory and chaos

- strongest relationships between deterministic chaos and randomness are found through consideration of ergodic theory
- imagine that some arbitrary system (stochastic or deterministic) is under study
- one experiment in which we will observe the evolution of some variable of the systems over time. 
- In another experiment, we will observe the same variable, but for several "similar" replicates of the same system at a given time point.
- Ergodic theory seeks to answer the question, "When can we expect the average of the data, over time, in the first experiment, to be the same (in expectation) as the average of the data, over the replicates at a fixed time?
- There is an intriguing relationship between the question of ergodic theory and the familiar question of "independent versus repeated measures" observation

- To see the role of ergodic theory in deterministic chaos, formalisation:
  * probability triple (X, F, P),
  * The function, or transformation, f is said to be measure preserving (or invariant) with respect to P if the random variable f(X) has distribution P
  * For an invertible transformation f, a subset A $\in$ F is invariant if $f^{-1}(A) = A$.
  * For a noninvertible f, invariance of A means $f^{t}(A)$ = A for all t > 0.
  * Further, f is said to be ergodic if for every invariant subset, $A \in F$, P(A) = 0 or 1.
  * if f is ergodic, sample paths of the dynamical system obtained from f do not become trapped in proper subsets of the support of P, but rather mix over its support. 
  * Further, if f is ergodic with respect to two probability measures P1, and P2 on the same measure space, then either P1 = P2 or P1 is orthogonal to P2

- state a simple version of the ergodic theorem:
  * If f is measure-preserving and ergodic on (X, F, P) 
  * and Y is any random variable such that $E(Y) < \inf$,
  * then $1/n \sum_{i = 1} ^n Y(f^i (x_0)) \rightarrow E_P(Y) a.s.(P)$ as $n \rightarrow \inf$
  
- A most intimate relationship between ergodic theory, chaos and randomness
  * Under the assumptions of the ergodic theorem, if the initial condition xo is generated according to P, the sequence $\{Y(f^{i}(x_o)) = Yi(x_o), i > 0\}$ is a stationary stochastic process.
  * Thus, if we choose Y to be the identity transformation, Y(x) = x, the deterministic dynamical system with initial condition somehow chosen, with care to avoid sets of P-measure zero, is a realization of a stochastic process. 










