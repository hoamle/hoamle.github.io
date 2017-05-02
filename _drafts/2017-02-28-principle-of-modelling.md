---
title: "Part 2 - Principle of Modelling: Model Structure, Learning Framework"
layout: post
category: t
---
{% maincolumn 'assets/img/model_structures.png' 'TODO' %}

***Case-study***: Extend from the `iris` case-study in week 1



### Statistical reasoning
Statistics provide concrete mathematical framework to reason, and make decision (e.g. prediction, action) under **uncertainties**.

Reason about distribution of each flower type $$y_{n}$$ with and without information from features $$x_{n}$$

Notation: 

|:---:|:---|
|{% m %} \overset{\circ}{y_{n}} {% em %} | A random variable. Thus {% m %} \text{Pr}\left(\overset{\circ}{y_{n}}\|\cdot\right) {% em %} implies a probability distribution. |
|{% m %} y_{n} {% em %} | A realization of random variable {% m %} \overset{\circ}{y_{n}} {% em %}. Thus {% m %} \text{Pr}\left(y_{n}\|\cdot\right) {% em %} is a value. |
| {% m %} \Omega_{\overset{\circ}{y_{n}}} {% em %} | Set of all possible realization {% m %} y_{n}{% em %}'s of random variable {% m %} \overset{\circ}{y_{n}} {% em %} i.e. ***sample space*** of {% m %} \overset{\circ}{y_{n}} {% em %}. |
|{% m %} \hat{y}_{n} {% em %} | An estimate of random variable {% m %} \overset{\circ}{y_{n}} {% em %} |
| {% m %} \underset{y_{n}^{'}}{\text{argmax}}\text{Pr}\left(y_{n}^{'}\|\cdot\right) {% em %} | short for {% m %} \underset{y_{n}^{'}\in\Omega_{\overset{\circ}{y_{n}}}}{\text{argmax}}\text{Pr}\left(\overset{\circ}{y_{n}}=y_{n}^{'}\|\cdot\right) {% em %}. We use notation {% m %} y_{n}^{'} {% em %} to not confuse with {% m %} y_{n} {% em %} which is reserved for the realization provided by training data {% m %} \mathcal{D}=\left\{ x_{n},y_{n}\right\}_{n=1}^{N}  {% em %}. |


*By **decision theory*** {% sidenote "sn-id-decision" "TODO ref"%}, the most optimal prediction $$\hat{y}$$ is one s.t. 
{% math %} \hat{y}=\underset{y}{\text{argmax}}\text{Pr}\left(y|x\right) {% endmath %}

###  Model structure
parametric assumed
...
{% maincolumn 'assets/img/week2.png' '' %}



### Learning framework
*By **Maximum Likelihood principle***, find estimate $$\hat{\theta}$$ s.t. 
{% math %} \hat{\theta}=\underset{\theta}{\text{argmax}}J\left(\theta,\mathcal{D}\right) {% endmath %}

{% math %} J\left(\theta,\mathcal{D}\right)=\log\text{Pr}\left(y_{1..N}|x_{1..N};\theta\right)=...=\sum_{n}\sum_{k}y_{nk}\log\mu_{nk} {% endmath %}

Reason: the estimates found by maximum likelihood principle (called ***maximum likelihood estimates*** i.e. ***MLE***s) satisfy "nice" properties of an estimator, which include asymptotic unbiasedness, and asymptotically approaching a well-defined lower-bound of its variance (Cramer-Rao lower bound) 


## Learning task 
Recall: we need to solve optimization problem {% m %} \hat{\theta}=\underset{\theta}{\text{argmax}}J\left(\theta,\mathcal{D}\right) {% em %}.

Closed-form solution not available => resort to numerical solution, found by optimization algorithm: gradient ascent (more commonly known as gradient descent when we minimize error function).

$$\hat{\theta}^{\left(i+1\right)}\leftarrow\hat{\theta}^{\left(i\right)}+\alpha\cdot\dfrac{1}{N}\cdot\nabla_{\theta}J\left(\hat{\theta}^{\left(i\right)}\right)$$

$$\nabla_{\theta}J\left(\hat{\theta}^{\left(i\right)}\right)=\left.\dfrac{\partial J}{\partial\theta}\right|_{\theta=\hat{\theta}^{\left(i\right)}}$$

Note: although the gradients in Softmax regression model can be computed analytically, it is not the case in models with more complex structure (e.g. TODO link to week 3). In such cases, **back-propagation** is a common algorithm to compute these gradients.

## Inference and Prediction task
**Inference**: 
{% math %} \text{Pr}\left(\left.\overset{\circ}{y^{\left(\text{new}\right)}}\right|x^{\left(\text{new}\right)},\mathcal{D}\right) {% endmath %}

{% m %} =...=\text{Pr}\left(\left.\overset{\circ}{y^{\left(\text{new}\right)}}\right|\mu^{\left(\text{new}\right)}\right)=\mu^{\left(\text{new}\right)}=f\left(\hat{w}^{T}x^{\left(\text{new}\right)}\right)
  {% em %}

**Predict**:
{% math %} \hat{y}^{\left(\text{new}\right)}=\underset{k}{\text{argmax}}\text{Pr}\left(\overset{\circ}{y^{\left(\text{new}\right)}}=k|x^{\left(\text{new}\right)},\mathcal{D}\right) {% endmath %}

{% m %} =\underset{k}{\text{argmax}}\mu_{k}^{\left(\text{new}\right)} {% em %}
