---
layout: post
title: "Why is the diffusion model's training loss in the form of a weighted average?"
math: true
date: 2025-12-31
---

Let $x^{(0)}$ denote a clean image at the start $t = 0$. Then the probability that the generative model assigned to this data is 

$$
p(x^{(0)}) = \int dx^{(1, \ldots, T)} p(x^{(0, \ldots, T)})
$$

Our goal is to maximise the training loss $L$, where 

$$
L = \int dx^{(0)} q(x^{(0)}) log^{ p(x^{(0)})}.
$$

**But why does the training loss $L$ have this weighted average form, where the log of the model prediction $p(x^{(0)})$ is weighted by ground truth $q(x^{(0)})$, for all possible clean image $x^{(0)}$?**

The answer lies in the KL-divergence ($D_{KL}$) between the ground truth $q$ and model prediction $p$, i.e., $D_{KL}(q \lVert p)$.  

$$
D_{KL}(q \lVert p) = \int q(x) log^{\frac{q(x)}{p(x)}} dx 
                  = \int q(x)log^{q(x)} dx - \int q(x) log^{p(x)} dx

$$
