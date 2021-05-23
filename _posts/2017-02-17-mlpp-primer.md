---
layout: post
title: "Machine Learning as Probabilistic (Bayesian) modelling, in simpler language"
date: 2017-02-17
tag: [tutorial]
---
{% marginnote 'motivation' "*Motivation*. Many DSLab-HUST members, including myself back in late 2015, had been struggling with studying **probabilistic (Bayesian) modelling** given pretty limited training we had. The issue got worse when some others, instead, explored Deep Neural Networks - DNN first, and their intersection - Deep Bayesian modelling, where the links / intuition between the 2 domains were hard to made without a *proper foundation* in Probabilistic modelling. I reckoned that adding more training sessions to the existing ones with *revised* ML fundamentals - to fill in probabilistic interpretation and DNN bits, *more visualization* - to accompany the equation, and [*augmented graphical model notation*](//edwardlib.org/api/model) - to include deterministic nodes in stochastic structures - might have alleviated the problem. For that this series was developed, and added to the training sessions in early 2017 - while I was a Research assistant at the lab." %}
**"Base"** course for Machine Learning (ML) starters, under the language of ***probabilistic modelling***. Pre-requisite for subsequent training sessions in Probabilistic (graphical) models e.g. Topic models, Deep Learning, and other ML topics.

The objective of this course is to introduce core concepts of <em>modern</em> Machine learning under probabilistic perspective, with (i) more visualization & interpretation of the accompanied math, and (ii) <a href="//edwardlib.org/api/model">augmented graphical model notation</a> to incorporate DNN architectures into stochastic structure of Probabilistic models. Upon completing this course, the learners can, hopefully, explore the <a href="/post/16/a-ml-dl-map">spectrum of ML/AI research</a>  with minimal guidance, keep their heads up on the big picture to not get lost in the complexity of the field, later learn advanced materials more efficiently.

**Pre-requisite**. Basic knowledge in the following mathematical areas
* Linear Algebra: understand the notion of *vectors* and *space* to represent data; basic arithmetics: dot product, matrix multiplication.
* Probability & Statistics: understand the notion of *probability distribution* to quantitatively express "possibilities"
* Calculus: can do partial derivatives, know the chain-rule (not required for "base" course if not diving deep into *how* [learning task](#core) is done, but recommended for the long-term nevertheless)

## <a name="core">Core concepts</a>
Via the lens of probabilistic modelling, we will introduce the following high-level concepts (in ***bold italic***).
> *Tip: read  the side notes, tap on the numbered superscript below (if you're on your phone) for more details.*

### Build a Machine Learning model
* Design principle: <a name="arc">***Model***</a> {% sidenote 'sn-model' '*"Model is a simplification of reality"*. Formulate real-life problems as ***parametric models***. Note: *non-parametric models/methods* are not covered and left for further reading after "base" course. See [the map](#map).' %} = *(model)* ***Structure***{% sidenote 'sn-structure' 'Relationships between the elements of a model: data, parameters, and hyperparameters.  Relationships can either be *deterministic* or *stochastic*, and can be summarized graphically by <a name="graphical" href="/post/17/principle-of-modelling">***graphical models***</a>.' %} + ***Learning Framework***{% sidenote 'sn-framework' 'Probabilistic framework: ***maximum likelihood estimation*** and ***Bayesian reasoning***. Non-probabilistic frameworks include [*differential geometry*](//metacademy.org/roadmaps/rgrosse/dgml), which is more mathematical i.e. more abstract, and is only recommended upon completing `PGM` node in the [study-plan](#plan).' %}

> *Note: the term "**Architecture**" - often seen in DNN - can be thought of as a sub-concept of "**Structure**"*

* Tasks to do:  ***Learning***, ***Inference***, and ***Decision making***{% sidenote 'sn-estimate' 'Realize a model by finding/computing (point) estimates of unknown parameters/ hyper-parameters (***learning task***) of the model; other quantities of interest, e.g. predictive posterior distribution of outcomes/ estimates of missing data/ ... given trained model (***inference tasks***), in order to make optimal ***decisions*** - prediction, actions - under *uncertainties*.' %} 

### Evaluate performance of a model

* ***Assessment metrics***: Which metrics to measure model performance?
* ***Model selection***: Which model to use, or can we ensemble / average different models?
* ***Model criticism***: Are the results meaningful{% sidenote 'sn-meaningful' 'in terms of *statistical* significance, interpretability, or interesting observation' %}  and legitimate{% sidenote 'sn-analyze' 'We will touch on ***Experimental design***' %}? 

### Regularize a model
* To fight ***overfitting*** issue. Example approaches: weight penalty, ***Bayesian inference/reasoning***{% sidenote 'sn-bayes' 'We will also see Bayesian reasoning, and eventually *Bayesian inference methods*, when building ***generative models*** for clustering problem' %}, Data augmentation, Dropout, Ensemble methods
* To strive for human-interpretable model via *sparsity*{% sidenote 'sn-sparse' "covered in Topic Models course" %} or [other objectives](//en.wikipedia.org/wiki/Regularization*(mathematics)).


## <a name="note">Course notes</a>
Session 1 - [Introduction](//raw.githubusercontent.com/hoamle/essence_ml/e788aef7617fed6911bcfd710ebbccd8ed34eae6/essence_ml.pdf)  & [Primer on Building a Machine Learning solution](/post/17/primer-on-building-ml-solutions)

Session 2 - Principles of Modelling: Model structure (linear models), Learning framework

Session 3 - Model structure (non-linear models), Regularization, Model selection

Session 4 - Bayesian inference, Generative models

[RECAP Session 2-4](//1drv.ms/p/s!ApOZHae4ogqZgog1P9HHN_4u3UeMeA) 

Session 5 - Introduction to [Latent Variable Models & How to learn classical LVMs](//1drv.ms/p/s!ApOZHae4ogqZgog1P9HHN_4u3UeMeA)

## <a name="ref">References</a>
For this course
> Andrew Ng's Machine Learning class ([Coursera](//www.coursera.org/learn/machine-learning) or [CS229](//cs229.stanford.edu/)) <- Practical introduction to ML and common ML algorithms.

> [Stanford CS231n](//cs231n.stanford.edu/) - ConvNet for Visual Recognition <- Practical course on DNN under the context of visual recognition.

> [Machine Learning: a Probabilistic Perspective](//www.cs.ubc.ca/~murphyk/MLbook/) (Kevin Murphy) <- Comprehensive textbooks on Probabilistic modelling. Alternative: [Pattern Recognition and Machine Learning](//www.amazon.com/Pattern-Recognition-Learning-Information-Statistics/dp/0387310738) (Christopher Bishop) 

For bigger, more expressive landscape of Deep Bayesian modelling
> [Shakir Mohamed's talk](//videolectures.net/deeplearning2016_mohamed_generative_models/) on Deep Generative Models in Deep Learning Summer School, 2016 <- Terrific summary of modelling principles and categorization of model classes

> [Durk Kingma's PhD Thesis](//twitter.com/dpkingma/status/914277278602821633?lang=en) <- Self-contained references for the building blocks of the most recent advances such as Amortized inference with path-wise Stochastic-gradient VI (where VAE is a special case), Variational Dropout, Inverse Autoregressive Flow 

## <a name="study">Course logistics</a>
2 sessions/week: 1x "**Lecture**" session + 1x optional "**Study-group**" session.

*Lectures* are meant to lead you in the right direction, and that's it --- just to get you started. They are **not** meant to tell you *everything* in *every* details. Thus, you should also utilize the reference reading materials, online resources for missing details

It should also be reckoned that *we do not know everything*. In many situations, we *don't even know what we don't know*. Thus do not hesitate to get in touch with the course instructors, the teaching assistant, your classmates, circles of friends for further support/discussion/...