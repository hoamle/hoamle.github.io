---
layout: post
title: "Essence of Machine Learning (and Deep Learning)"
date: 2016-10-01
category: t
---
"Base" course for new members at DSLab-HUST. Pre-requisite for subsequent training sessions in *Topic models* (or *Probabilistic Graphical Models*) and *Deep Learning*. 

**Motivation.** The majority of DSLab-HUST members, including myself back in early 2016, are aspiring ML ***self-learners***, and have been struggling (*a lot*) to study **probabilistic/Bayesian modelling** on our own. For the newcomers - who are very likely exposed to Deep Neural Networks (DNN) *before* probabilistic modelling - I found it considerably more challenging and time-consuming to see the [big picture of Machine Learning](#map) (*Deep Learning* included) research without *proper background in probabilistic (graphical) models - PGM*.

Nevertheless, it's truly hard to find a beginner-level MOOC in PGM{% sidenote 'sn-id-mooc' "Prof. [Daphne Koller's course in PGM](https://www.coursera.org/specializations/probabilistic-graphical-models) is a little bit abstract, and not a beginner-level course on ML" %} which can instill (i) probabilistic/statistical reasoning, and also introduce (ii) [ML core concepts](#core) in a intuitive flow as Prof. [Andrew Ng's course](https://www.coursera.org/learn/machine-learning) did. Therefore, this course is devised to address the 2 purposes. Upon completing this course, the learners can, hopefully, explore the spectrum of ML research with minimal guidance, keep their heads up on the big picture to not get lost in the complexity (and the hype!) of the field, later learn advanced materials more efficiently, and catch up with recent advances in Machine Learning research.
 
**Intended Learning Objectives**
1. understand the motivation and intuition behind Bayesian inference/reasoning and other [core concepts](#core) in ML, including representative models/methods for each concept; 
2. be able to navigate new concepts/terminology in [the Map(s) of Machine Learning](#map) to devise proper study-plans; and 
3. *optionally* - understand the math behind each model/concept and implement the ML models/algorithms covered in the course (expected from students who do the homework and ["Study-group" sessions](#study))

**Pre-requisite**. {% marginnote 'mn-id-math' "Don't be afraid of Math, embrace it. Math is (1) essentially \"giving the **same name** to different things\" (Henri Poincare). Once we rephrase a problem in mathematical tongue, we may see hidden  connections between numerous of *supposedly* unrelated problems in different fields [[DAslides:pp22-38]](https://1drv.ms/b/s!ApOZHae4ogqZ3AJg76xtDPEzSlH-). Further more, Math is (2) **non-ambiguous** so that we can devise a solution with transparent and concrete reasoning." %} Basic knowledge in the following mathematical areas
* Linear Algebra: understand the notion of *vectors* and *space* to represent data points; basic arithmetics: dot product, matrix multiplication.
* Calculus: can do partial derivatives, know the chain-rule 
* Probability & Statistics: understand the notion of *probability distribution* to quantitatively express "possibilities"

## <a name="core">Core concepts</a>
Via the lens of probabilistic modelling, we will cover the following concepts. <font color="red">Note</font>: if not stated otherwise, concepts in ***bold italic*** are covered in the prelim course. [Course notes](#notes) is to be expected in respective blog posts. 

### Build a Machine Learning model
`>` Design principle: ***Model*** {% sidenote 'sn-model' '*"Model is a simplification of reality"*. Formulate real-life problems as ***parametric models***. Note: *non-parametric models/methods* are not covered and left for further reading after this prelim course. See [the map](#map).' %} = *(model)* ***Structure***{% sidenote 'sn-structure' 'Relationships between the elements of a model: data, parameters, and hyperparameters.  Relationships can either be *deterministic* or *stochastic*, and can be summarized graphically by ***graphical models***.' %} + ***Learning Framework***{% sidenote 'sn-framework' 'Probabilistic framework: ***maximum likelihood estimation*** and ***Bayesian reasoning***; non-probabilistic framework e.g. [*geometric approach*](https://metacademy.org/roadmaps/rgrosse/dgml) - a more mathematical i.e. more abstract approach of modelling.' %}

`>` Tasks to do:  ***Learning***, ***Inference***, and ***Decision making***{% sidenote 'sn-estimate' 'Find/compute point estimates of unknown parameters (***learning task***) of the model, and other quantities of interest, e.g.predictive posterior distribution of outcomes, given trained model (***inference tasks***), in order to make optimal ***decision*** under *uncertainties*.' %} 

### Evaluate performance of a model

***Assessment metrics***: which metrics to measure the performance?

***Analyze results***: are the results meaningful{% sidenote 'sn-meaningful' 'in terms of *statistical* significance, interpretability, or interesting observation' %}  and legitimate{% sidenote 'sn-analyze' 'We will touch on ***experimental design***' %}? 

### Regularize a model
`>` to fight ***overfitting*** issue. Example approaches: weight penalty, ***Bayesian reasoning***{% sidenote 'sn-bayes' 'We will also see Bayesian reasoning, and eventually *Bayesian inference*, when building ***generative models*** for clustering problem' %}, Early-stopping, Data augmentation, Dropout;

`>` to achieve some interpretability via *sparsity*{% sidenote 'sn-sparse' "covered in Topic Models course" %} or [other objectives](https://en.wikipedia.org/wiki/Regularization*(mathematics)).

### Deploy
***Model selection*** and *Model ensemble*



## <a name="ref">References</a>
Course content is partially taken from the following sources:

`>` Christopher Bishop's [Pattern Recognition and Machine Learning](https://www.amazon.com/Pattern-Recognition-Learning-Information-Statistics/dp/0387310738) & Kevin Murphy's [Machine Learning: a Probabilistic Perspective](https://www.cs.ubc.ca/~murphyk/MLbook/) <- Comprehensive textbooks on Probabilistic models.

`>` Andrew Ng's Machine Learning class ([Coursera](https://www.coursera.org/learn/machine-learning) or [CS229](http://cs229.stanford.edu/)) <- Practical introduction to ML and common ML algorithms.

`>` Stanford Univ's [CS231n - ConvNet for Visual Recognition](http://cs231n.stanford.edu/) <- Practical course on DNN under the context of visual recognition.

`>` [Shakir Mohamed](http://videolectures.net/deeplearning2016_mohamed_generative_models/)'s talk on Deep Generative Models in Deep Learning Summer School, 2016 <- Terrific summary of modelling principles and categorization of model classes. Also introduce recent advances in marrying Probabilistic modelling with DNN. 


## <a name="study">Course logistics</a>
2 sessions/week: 1x "**Lecture**" session + 1x optional "**Study-group**" session.
* ***Lectures*** are meant to lead you in the right direction --- just to get your started. They are **not** meant to tell you *everything* in *every details*. Thus, you should also utilize the reference reading materials, online resources for missing details *<- (the role of **self-study**)*

* It should be reckoned that we do not know everything (in *many cases*, we don't even know what we don't know), so do not hesitate to get in touch with the course instructors, the teaching assistant - TAs, your classmates, circles of friends for further support/discussion/...  *<- (the importance of **Study-group**)* 

## <a name="notes">Course notes</a>
PART 1 - (a) [Introduction](https://raw.githubusercontent.com/hoamle/essence_ml/e788aef7617fed6911bcfd710ebbccd8ed34eae6/essence_ml.pdf)  & (b) [Primer on Building a Machine Learning solution](/articles/17/primer-on-building-ml-solutions)

PART 2 - Principles of Modelling: Model structure (linear models), Learning framework

PART 3 - Model structure (non-linear models), Regularization, Model selection

PART 4 - Bayesian inference, Generative models

PART 5 - [Recap](https://1drv.ms/p/s!ApOZHae4ogqZgog1P9HHN_4u3UeMeA) & Introduction to [Latent Variable Models + (advanced) Bayesian inference](https://1drv.ms/p/s!ApOZHae4ogqZgog1P9HHN_4u3UeMeA)

## <a name="map">The Map(s) of Machine Learning</a>
***Disclaimer***: The map below, with focus on different model classes, is an INCOMPLETE map. It has been designed to make it easier for aspiring ML self-learners to transit from DNN (or [basic ML](https://www.coursera.org/learn/machine-learning)) to PGM, given that they had covered the "base" (the first 4 parts in [Course content](#notes) above). For a more comprehensive picture of model classes, see [Shakir Mohamed's talk](http://videolectures.net/deeplearning2016_mohamed_generative_models/).

{% maincolumn 'assets/img/mapofML.png' 'The Map(s) of Machine Learning, with focus on model classes & connection to other fields of study. Materials covered in this course correspond to the "base"  on the map' %}
