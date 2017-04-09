---
layout: post
title: "Essence of Machine Learning (and Deep Learning)"
date: 2016-10-01
category: t
---
Preliminary course for new members at DSLab-HUST. Pre-requisite for following courses in *Topic models (Probabilistic Graphical Models - PGM)* and *Deep neural networks - DNN*. 

*Motivation.* Students at DSLab-HUST have been struggling (*a lot*) moving from reading Deep neural networks to Probabilistic models and vice-versa. This short course, therefore, is introduced to guide new starters to the field of Machine Learning with a more ***principled approach***. Through the lens of *probabilistic modelling*, the series hope to help the new starters understand the motivation and intuition behind [Machine Learning core concepts](#core) that  define the spectrum of research in the field (which eventually includes *Deep Learning* along the course), keep their heads up on the big picture to not get lost in the complexity of the field, later learn advanced materials efficiently and catch up with recent advances in Machine Learning.

 

*Intended learning objectives*: 
1. understand and know what constitute of the [core concepts](#core) in Machine Learning (ML); 
2. be able to navigate new concepts/terminology in [the Map of Machine Learning](#map) to devise proper study-plans; and 
3. *optionally* - articulate the math behind each model or concept and implement the ML models or algorithms covered in the course properly (expected from students who do the homework and ["Study-group" sessions](#study))

## <a name="core">Core concepts</a>
{% marginnote 'mn-map' 'TODO draw the Map' %} We will cover the following concepts. <font color="red">Note</font>: if not stated otherwise, concepts in ***bold italic*** are covered in the prelim course. [Course notes](#notes) is to be expected in respective blog posts. 

### Build a Machine Learning model
`>` Design principle: ***Model*** {% sidenote 'sn-model' '*"Model is a simplification of reality"*. Formulate real-life problems as ***parametric models***. Note: *non-parametric models/methods* and [*geometric modelling*](https://metacademy.org/roadmaps/rgrosse/dgml) - a more abstract approach of modelling - are not covered and left for further reading after this prelim course.' %} = *(model)* ***Structure***{% sidenote 'sn-structure' 'Relationships between the elements of a model: data, parameters, and hyperparameters.  Relationships can either be *deterministic* or *stochastic*, and can be summarized graphically by ***graphical models***.' %} + ***Learning Framework***{% sidenote 'sn-framework' 'Probabilistic framework: ***maximum likelihood estimation*** and ***Bayesian reasoning***; non-probabilistic framework: *margin learning*, *metric learning* (not covered in prelim course)' %}

`>` Tasks to do:  ***Learning***, ***Inference***, and ***Decision making***{% sidenote 'sn-estimate' 'Find/compute point estimates of unknown parameters (***learning task***) of the model, and other quantities of interest, e.g.predictive posterior distribution of outcomes, given trained model (***inference tasks***), in order to make optimal ***decision*** under *uncertainties*.' %} 

### Evaluate performance of a model

***Assessment metrics***: which metrics to measure the performance?

***Analyze results***: are the results meaningful{% sidenote 'sn-meaningful' 'in terms of *statistical* significance, interpretability, or interesting observation' %}  and legitimate{% sidenote 'sn-analyze' 'We will touch on ***experimental design***' %}? 

### Regularize a model
`>` to fight ***overfitting*** issue. Example approaches: weight penalty, ***Bayesian reasoning***{% sidenote 'sn-bayes' 'We will also see Bayesian reasoning, and eventually *Bayesian inference*, when building ***generative models*** for clustering problem' %}, Early-stopping, Data augmentation, Dropout; or

`>` to achieve some interpretability via *sparsity*{% sidenote 'sn-sparse' "covered in Topic Models course" %} or [other objectives](https://en.wikipedia.org/wiki/Regularization*(mathematics)).

### Tuning for more performance
***Model selection*** and *Ensemble* techniques



## References
Course content is partially taken from the following sources:

> Christopher Bishop's [Pattern Recognition and Machine Learning](https://www.amazon.com/Pattern-Recognition-Learning-Information-Statistics/dp/0387310738) <- Comprehensive textbook on Probabilistic modelling with focus on Bayesian methods.

> Andrew Ng's Machine Learning class ([Coursera](https://www.coursera.org/learn/machine-learning) or [CS229](http://cs229.stanford.edu/)) <- Practical introduction to Machine Learning and common learning algorithms.

> Stanford Univ's [CS231n - ConvNet for Visual Recognition](http://cs231n.stanford.edu/) <- Practical course on Deep neural networks (DNN) with the context of computer vision problems.

> [Shakir Mohamed](http://shakirm.com/?section=3)'s tutorial on Deep Generative Models in Deep Learning Summer School, 2016 <- Terrific summary of modelling principles and categorization of model classes. Also introduce recent advances in marrying Probabilistic modelling with DNN. 


## <a name="study">Course logistics</a>
2 sessions/week: 1x "**Lecture**" session + 1x optional "**Study-group**" session.
* ***Lectures*** are meant to lead you in the right direction --- just to get your started. They are **not** meant to tell you *everything* in *every details*. Thus, you should also utilize the reference reading materials, online resources for missing details *<- (the role of **self-study**)*

* It should be reckoned that we do not know everything (in *many cases*, we don't even know what we don't know), so do not hestitate to get in touch with the course instructors, the teaching assistant - TAs, your classmates, circles of friends for further support/discussion/...  *<- (the importance of **Study-group**)* 

## <a name="notes">Course notes</a>
PART 1 - (a) [Introduction](https://raw.githubusercontent.com/hoamle/essence_ml/e788aef7617fed6911bcfd710ebbccd8ed34eae6/essence_ml.pdf)  & (b) [Primer on Building a Machine Learning solution](/articles/17/primer-on-building-ml-solutions)

PART 2 - Principles of Modelling: Model structure, Learning framework

PART 3 - Principles of Modelling: Model structure (cont.), Regularization

PART 4 - Bayesian inference, Model selection, Generative models

PART 5 - Recap