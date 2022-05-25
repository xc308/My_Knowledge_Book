---
layout: post
title: "What is Max-stable Process?"
date: 2022-05-25
---
{%include _includes/head.html%}

Ref: https://spatialextremes.r-forge.r-project.org/index.php?module=pages&action=maxstable



## Max-stable process
- max-stable processes are an extension of the multivariate extreme value theory to the infinite dimensional case
- very useful spectral characterisation for unit Frechet max-stable processes is [Schlather, 2002]
  * $Z(x) = max_{i \geq 1} \xi_i Y_i(x) $
  * where $(\xi_i)_{i\geq 1}$ are points of Poisson Point Process on $(0, \infty]$ with intensity measure $d\Lambda(\xi) = \xi^{(-2)} d\xi$
  * $Y_i(x)$ are independentreplications of a positive stochastic process having continuous sample paths $Y$ and $\mathbb{E}(x) = 1$ for $x \in \mathbb{R}^d$




## Function "rmaxstab": Simulate max-stable processes
can simulate a max-stable process using its limiting characterisation i.e. find the normalizing functions  and  and simulate  indendant replications of a stochastic process $Y(x)$ for which the normalizing function are based.
- disadvantage: requiring a large number of independent replicates 
- but also pose the question of how many replicates should be simulated?
- A better strategy: using one of the spectral representation
- In most cases this will be more efficient since one can simulate the points of a Poisson point process with intensity $d \Lambda(\xi) = \xi^{-2} d\xi$
-  where $\xi_i = \sum_{1}^{i} \frac{1}{E_j}$ and $E_j \overset{iid}{\sim} Exp(1)$
-  and $\xi_i \rightarrow 0$ as $i \rightarrow \infty$
- If we further assume that the stochastic process used in the spectral characterisation is bounded above



