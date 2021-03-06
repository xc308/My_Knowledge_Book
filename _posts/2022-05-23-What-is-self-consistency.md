---
layout: post
title: "What is self-consistent vectors?"
date: 2022-05-23
---
{% include_relative _includes/head.html %}

*Ref: Thaddeus Tarpey and Bernard Flury (1996) Self-Consistency: A Fundamental Concept in Statistics*
* Declear: This post is just an reading notes recording some of the useful information. The copy right and property right all belong to the original author.*


## 1. Abstract / Intro

* The term "self-consistency" was introduced in 1989 by Hastie and Stuetzle to describe the property that each point on a smooth curve or surface is the mean of all points that project orthogonally onto it
* Generalize this concept to self-consistent random vectors: a random vector Y is self-consistent for X if $E[X \mid Y] = Y$ almost surely
* This allows us to construct a unified theoretical basis for principal components, principal curves and surfaces, principal points, principal variables, principal modes of variation and other statistical methods.

  - What is principle curve? 
  - "Principal curves are smooth one-dimensional curves that pass through the middle of a p-dimensional data set, providing a nonlinear summary of the data."
  - https://hastie.su.domains/Papers/Principal_Curves.pdf

* Key words and phrases: Elliptical distribution; EM algorithm; k-means algorithm; mean squared error; 
principal components; principal curves;principal modes of variation; principal points; principal variables; regression;
$\color{red}{\text{self-organizing maps}}$; spherical distribution; Voronoi region

  * self-organizing maps: 
    - an unsupervised machine learning technique used to produce a low-dimensional (typically two-dimensional) representation of a higher dimensional data set while preserving the topological structure of the data.
    - https://en.wikipedia.org/wiki/Self-organizing_map


## 2. SELF-CONSISTENT RANDOM VECTORS

* want to represent or approximate the distribution of a random vector X by a random vector Y whose structure is less complex.
* One measure of how well Y approximates X is the mean squared error $E \parallel X-Y \parallel ^2$
* In terms of mean squared error, the approximation of X by Y can always be improved using $E[X \mid Y]$
* since for any function g, $E \parallel X - E[X \mid Y] \parallel^2 \leq E \parallel X - g(Y) \parallel^2$
* and taking g to be identity, $E \parallel X - E[X \mid Y] \parallel^2 \leq E \parallel X - Y \parallel^2$
* Thus the random vector Y is locally optimal for approximating X if $Y = E[X \mid Y]$, in which case we call Y selfconsistent for X.

* Def 2.1 For two jointly distributed random vectors X and Y, we say that Y is self-consistent for X if $E [X \mid Y] = Y$ almost surely.

* Two extreme cases: 
  - $X = E[X \mid X]$: X is self-consistent for X; and no loss of information
  - $Y = E[X]$: Y is self-consistent for X; and total loss of information

* interesting self-consistency lies in between
* Many relevant cases of self-consistency are obtained by taking conditional means over subsets of the sample space of X.


* Example 2.1: 
  - Partial sum
  - $\{X_n \}$: a sequence of independent, mean-zero random variables
  - $S_n = \sum_{i=1}^n X_i$
  - $E[S_{n+k} \mid S_n] = S_n + E[X_{n+1}, \dots, X_{n+k} \mid S_n] = S_n + E[X_{n+1}, \dots, X_{n+k}] = S_n$
  - $S_n$ is self-consistency for $S_{n+k}$ 


* For a given X, a self-consistent approximation Y can be generated by partitioning the sample space
of X and defning Y as a random variable taking as values the conditional means of subsets in the partition.

* Elementary properties of self-consistent random vectors:
  - Lemma 2.2. If Y is self-consistent for X, then $E[Y] = E[X]$
  - Notation for the mean squared error (MSE) of a random vector Y for X: $MSE(Y;X) = E \parallel Y - X \parallel ^2$
  - lemma relates the MSE of a self-consistent Y for X in terms of their respective covariance matrices
    * Denote $\Psi_X, \Psi_Y$ as convariance matrices as vector X and vector Y
    * Lemma 2.3 If Y is self-consistent for X, then the following hold:
    * (1) $\Psi_X \geq \Psi_Y$, $\Psi_X - \Psi_Y$ is p.s.d
    * (2) $ MSE(Y; X) = tr(\Psi_X) - tr(\Psi_Y)$
    * Follows from the lemma 2.3. $cov(Y) = cov(X)$ exactly if $cov(X \mid Y) = 0 a.s. i.e. Y = X a.s.$
    * For 1-D random variable X, Y, if Y is self-consistent for X, then $var[Y] \leq var[X]$, with equality exactly if $Y = X a.s.$






