---
layout: page2
title: FMS
permalink: /FMS/
---

# The Fast Median Subspace (FMS) algorithm

[Gilad Lerman](http://www-users.math.umn.edu/~lerman/) and [Tyler Maunu](https://twmaunu.github.io/)

[Fast, robust and non-convex subspace recovery](https://arxiv.org/abs/1406.6145) (2017)

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

## Materials

[fms code only](https://drive.google.com/file/d/1l7CvgHd4Ljg8FRfOMmGtgFIhIKSPxrYw/view?usp=sharing)

* While the default method in the paper uses a randomized SVD algorithm, we have noticed instability of this method in some of our tests. In particular, the method does not appear to be stable within our algorithm when the data matrix becomes very ill-conditioned. If the user desires accuracy, they should use standard SVD, which is the default in the code here. However, for truly large applications, randomized SVD should be used to save time.


[code to recreate figures from the paper](https://drive.google.com/file/d/0B3WZIZpLrsPYR3ZfRHJvdUJCMHM/view?usp=sharing)

[larger datasets from the paper](https://drive.google.com/file/d/0B3WZIZpLrsPYaEJYZk9icWVwcEk/view?usp=sharing)

## Acknowledgments

This work was supported by NSF awards DMS-09-56072 and DMS-14-18386
and the Feinberg Foundation Visiting Faculty Program Fellowship of the Weizmann
Institute of Science.

