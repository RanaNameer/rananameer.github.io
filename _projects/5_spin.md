---
layout: page
title: "SPIN: Fairness Without Demographics via Nuisance Invariance"
description: Reducing worst-group error without group labels by combining nuisance invariance with error-set up-weighting. In preparation.
importance: 2
---

A method for reducing group disparities when sensitive attributes are unavailable at training, validation, and test time. SPIN combines two label-free signals: a nuisance family, a parametric set of input changes that should not affect the decision, and the errors of a briefly trained reference model. It up-weights those errors, penalizes the predictor's sensitivity along random and adversarial views within the family, and refits the classification head under the same penalty. The analysis bounds group-risk disparity by the predictor's sensitivity along the family plus a term for the part of the proxy the family misses, and gives a closed-form account of why the two signals are complementary: invariance to a family that misses the proxy increases reliance on it, while up-weighting weakens the proxy but never removes it.

On two controlled tasks, with families that cover, leak, miss, or under-reach the proxy, SPIN reaches 77.4% and 91.7% worst-group accuracy with a covering family, above a GroupDRO oracle that uses group labels (73.9% and 86.0%), and avoids the collapse that family-only methods suffer when the family misses the proxy. All reported numbers come from held-out seeds; evaluation on real benchmarks (Waterbirds, CelebA, CivilComments, Adult) is planned.

**Status:** In preparation

**Stack:** fairness without demographics, spurious correlations, invariance, robust learning, PyTorch
