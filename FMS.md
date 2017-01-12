---
layout: page2
title: FMS
permalink: /FMS/
---
# Fast, robust and non-convex subspace recovery

## a.k.a. Fast Median Subspace (FMS) algorithm

[Gilad Lerman](http://www-users.math.umn.edu/~lerman/) and [Tyler Maunu](https://twmaunu.github.io/)

[arXiv](https://arxiv.org/pdf/1406.6145v2.pdf) (2016)

[code](https://github.com/twmaunu/FMS/blob/master/FMS.zip)

Abstract:
This work presents a fast and non-convex algorithm for robust subspace recovery.
The data sets considered include inliers drawn around a low-dimensional
subspace of a higher dimensional ambient space, and a possibly large portion of
outliers that do not lie nearby this subspace. The proposed algorithm, which we
refer to as Fast Median Subspace (FMS), is designed to robustly determine the
underlying subspace of such data sets, while having lower computational complexity
than existing methods. We prove convergence of the FMS iterates to a
stationary point. Further, under a special model of data, FMS converges to a
point which is near to the global minimum with overwhelming probability. Under
this model, we show that the iteration complexity is globally bounded and
locally r-linear. The latter theorem holds for any fixed fraction of outliers (less
than 1) and any fixed positive distance between the limit point and the global
minimum. Numerical experiments on synthetic and real data demonstrate its
competitive speed and accuracy.


The goal is to solve the optimization problem

$$ \text{argmin}_{L \in G(D,d)} \sum_{\boldsymbol{x}_i} \text{dist}(\boldsymbol{x}_i,L) $$

To deal with the non-differentiability of the cost in the above formulation, we instead consider the Huber-like version of this cost

$$ \text{argmin}_{L \in G(D,d)} \sum_{\text{dist}^{2-p}(\boldsymbol{x}_i,L) > p \delta} \text{dist}^p(\boldsymbol{x}_i,L) + \sum_{\text{dist}^{2-p}(\boldsymbol{x}_i,L) \leq p \delta} \frac{\text{dist}^2(\boldsymbol{x}_i,L)}{2\delta} + C_{p,\delta}   $$



TODO:
- complete description
- illustration
- experiments



