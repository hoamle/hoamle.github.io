---
title: "Principle of Modelling: Model Structure and Learning Framework"
layout: post
category: t

---
{% maincolumn 'assets/img/model_structures.png' '' %}
## Case study
Extend from the `iris` case-study in week 1

### Statistical reasoning
Statistis provide concrete mathematical framework to reason, and make decision (e.g. prediction, action) under **uncertainties**.

Reason about distribution of each flower type $y_{n}$ with and without information from features $x_{n}$

By decision theory {% sidenote "sn-id-decision" %}, the most optimal prediction is to set prediction $\hat{y}_{n}=\text{arg}\underset{\underbar{y}_{n}}{\max}\text{Pr}\left(y_{n}|x_{n}\right)$

###  Model structure
built from scratch, parametric assumed
...
{}

### Learning framework
Maximum likelihood principle {% marginnote %}
Reason: the MLE satisfies "nice" properties of an estimator, which are asymptotic unbiased, and asymptoticly low variance (efficient i.e. variance reach Cramer-XX lower bound)

## Learning 
Find all estimates of \theta s.t. $\hat{\theta}=\text{arg}\underset{\underbar{\theta}}{\max}\text{Pr}\left(y_{1..N}|x_{1..N};\theta\right)$

$J\left(\theta,\mathcal{D}\right)=\sum_{n}\sum_{k}y_{nk}\log\mu_{nk}$

Closed-form solution not available => resort to numerical solution, found by optimization algorithm: gradient ascent (more commonly known as gradient descent when we minimize error function).

$\hat{\theta}^{\left(i+1\right)}\leftarrow\hat{\theta}^{\left(i\right)}+\alpha\cdot\dfrac{1}{N}\cdot\nabla_{\theta}J\left(\hat{\theta}^{\left(i\right)}\right)$

$\nabla_{\theta}J\left(\hat{\theta}^{\left(i\right)}\right)=\left.\dfrac{\partial J}{\partial\theta}\right|_{\theta=\hat{\theta}^{\left(i\right)}}$

Note: although the gradients in Softmax regression model can be computed analytically, it is not the case in models with more complex structure (e.g. TODO link to week 3). In such cases, **back-propagation** is a common algorithm to compute these gradients.

## Inference and Prediction
Infer: $\text{Pr}\left(\left.y^{\text{\left(new\right)}}\right|x^{\text{\left(new\right)}},\mathcal{D}\right)$

$\text{Pr}\left(\left.y^{\text{\ensuremath{\left(new\right)}}}\right|x^{\text{\ensuremath{\left(new\right)}}},\mathcal{D}\right)=...=\text{Pr}\left(\left.y^{\text{\ensuremath{\left(new\right)}}}\right|\mu^{\text{\ensuremath{\left(new\right)}}}=f\left(\hat{w}^{T}x^{\left(\text{new}\right)}\right)\right)
 $

Predict $\hat{y}_{n}=\text{arg}\underset{\underbar{y}_{n}}{\max}\text{Pr}\left(y_{n}|x_{n}\right)$


