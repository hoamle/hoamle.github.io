---
layout: post
title: "Essence of Machine Learning (and Deep Learning)"
date: 2016-10-01
category: t
---
**"Base"** course for Machine Learning (ML) starters, under the language of ***probabilistic modelling***. Pre-requisite for subsequent training sessions in *Topic models* -or *Probabilistic (graphical) models, Deep Learning*, and *other ML topics* (see "The Map(s) of Machine Learning" below). 

*Motivation*. The majority of DSLab-HUST members, including myself back in early 2016, are aspiring ML ***self-learners***, and have been struggling (*a lot*) to study **probabilistic/Bayesian modelling** on our own. For the newcomers - who are very likely exposed to Deep Neural Networks (DNN) *before* probabilistic modelling - I found it considerably more challenging and time-consuming to see the [big picture i.e. map(s) of Machine Learning](#map) (including Deep Learning) research without *proper background in probabilistic (graphical) models -PGM*.

Nevertheless, it's truly hard to find a beginner-level MOOC in PGM{% sidenote 'sn-id-mooc' "Prof. [Daphne Koller's course in PGM](https://www.coursera.org/specializations/probabilistic-graphical-models) is *not* an introductory course on Machine Learning, and is only recommended upon having learnt the [core concepts of ML](#core) under the language of probabilistic modelling. If anyone knows such an introductory course, please do share!" %} which can (i) instill probabilistic/statistical reasoning, and also introduce (ii) [ML core concepts](#core) in an intuitive flow as Prof. [Andrew Ng's course](https://www.coursera.org/learn/machine-learning) did. Therefore, this course is devised to address the 2 purposes. Upon completing this course, the learners can, hopefully, explore the spectrum of ML research with minimal guidance, keep their heads up on the big picture to not get lost in the complexity (and the hype!) of the field, later learn advanced materials more efficiently, and catch up with recent advances in the field.
 
<a name="ilo">**Intended Learning Objectives**</a>
1. understand the motivation and intuition behind Bayesian inference/reasoning and other [core concepts](#core) in ML, including representative models and/or methods for each concept; 
2. be able to navigate new concepts/terminology in [the Map(s) of Machine Learning](#map) to devise proper study-plans; and 
3. *optionally* - understand the math behind each model/concept and implement the ML models/algorithms covered in the course (expected from students who do the homework and ["Study-group" sessions](#study))

**Pre-requisite**. {% marginnote 'mn-id-math' "Don't be afraid of Math, embrace it. Math is (1) essentially \"giving the **same name** to different things\" (Henri Poincare). Once we rephrase a problem in mathematical tongue, we may see hidden  connections between numerous of *supposedly* unrelated problems in different fields [[DAslides:pp22-38]](https://1drv.ms/b/s!ApOZHae4ogqZ3AJg76xtDPEzSlH-). Further more, Math is (2) **non-ambiguous** so that we can devise a solution with transparent and concrete reasoning." %} Basic knowledge in the following mathematical areas
* Linear Algebra: understand the notion of *vectors* and *space* to represent data; basic arithmetics: dot product, matrix multiplication.
* Probability & Statistics: understand the notion of *probability distribution* to quantitatively express "possibilities"
* Calculus: can do partial derivatives, know the chain-rule (not required for "base" course if not diving deep into *how* [learning task](#core) is done, but recommended for the long-term nevertheless)

## <a name="core">Core concepts</a>
Via the lens of probabilistic modelling, we will introduce the following high-level concepts (in ***bold italic***). [Course notes](#note) is to be expected in respective blog posts. 

> *Tip: read the side notes on the right margin of this page for more details.*

### Build a Machine Learning model
`>` Design principle: ***Model*** {% sidenote 'sn-model' '*"Model is a simplification of reality"*. Formulate real-life problems as ***parametric models***. Note: *non-parametric models/methods* are not covered and left for further reading after "base" course. See [the map](#map).' %} = *(model)* ***Structure***{% sidenote 'sn-structure' 'Relationships between the elements of a model: data, parameters, and hyperparameters.  Relationships can either be *deterministic* or *stochastic*, and can be summarized graphically by <a name="graphical" href="/articles/17/principle-of-modelling">***graphical models***</a>.' %} + ***Learning Framework***{% sidenote 'sn-framework' 'Probabilistic framework: ***maximum likelihood estimation*** and ***Bayesian reasoning***. Non-probabilistic frameworks include [*differential geometry*](https://metacademy.org/roadmaps/rgrosse/dgml), which is more mathematical i.e. more abstract, and is only recommended upon completing `PGM` node in the [study-plan](#plan).' %}

> *Note: the term "<a name="arc">**Architecture**</a>" - often seen in DNN - can be thought of as a sub-concept of "**Structure**"*

`>` Tasks to do:  ***Learning***, ***Inference***, and ***Decision making***{% sidenote 'sn-estimate' 'Realize a model by finding/computing (point) estimates of unknown parameters/ hyper-parameters (***learning task***) of the model; other quantities of interest, e.g. predictive posterior distribution of outcomes/ estimates of missing data/ ... given trained model (***inference tasks***), in order to make optimal ***decisions*** - prediction, actions - under *uncertainties*.' %} 
> *Note: in many cases, the term "**inference methods**" refers to methods that do both learning and inference tasks.*

### Evaluate performance of a model

***Assessment metrics***: which metrics to measure the performance?

***Analyze results***: are the results meaningful{% sidenote 'sn-meaningful' 'in terms of *statistical* significance, interpretability, or interesting observation' %}  and legitimate{% sidenote 'sn-analyze' 'We will touch on ***experimental design***' %}? 

### Regularize a model
`>` to fight ***overfitting*** issue. Example approaches: weight penalty, ***Bayesian inference/reasoning***{% sidenote 'sn-bayes' 'We will also see Bayesian reasoning, and eventually *Bayesian inference methods*, when building ***generative models*** for clustering problem' %}, Early-stopping, Data augmentation, Dropout;

`>` to achieve some interpretability via *sparsity*{% sidenote 'sn-sparse' "covered in Topic Models course" %} or [other objectives](https://en.wikipedia.org/wiki/Regularization*(mathematics)).

### Deploy
***Model selection*** and *Model ensemble*

## <a name="note">Course notes</a>
PART 1 - (a) [Introduction](https://raw.githubusercontent.com/hoamle/essence_ml/e788aef7617fed6911bcfd710ebbccd8ed34eae6/essence_ml.pdf)  & (b) [Primer on Building a Machine Learning solution](/articles/17/primer-on-building-ml-solutions)

PART 2 - Principles of Modelling: Model structure (linear models), Learning framework

PART 3 - Model structure (non-linear models), Regularization, Model selection

PART 4 - Bayesian inference, Generative models

PART 5 - [Recap](https://1drv.ms/p/s!ApOZHae4ogqZgog1P9HHN_4u3UeMeA) & Introduction to [Latent Variable Models + Bayesian inference methods](https://1drv.ms/p/s!ApOZHae4ogqZgog1P9HHN_4u3UeMeA)

## <a name="ref">References</a>
Course content is partially taken from the following sources:

> Christopher Bishop's [Pattern Recognition and Machine Learning](https://www.amazon.com/Pattern-Recognition-Learning-Information-Statistics/dp/0387310738) & Kevin Murphy's [Machine Learning: a Probabilistic Perspective](https://www.cs.ubc.ca/~murphyk/MLbook/) <- Comprehensive textbooks on Probabilistic models.

> Andrew Ng's Machine Learning class ([Coursera](https://www.coursera.org/learn/machine-learning) or [CS229](http://cs229.stanford.edu/)) <- Practical introduction to ML and common ML algorithms.

> Stanford Univ's [CS231n - ConvNet for Visual Recognition](http://cs231n.stanford.edu/) <- Practical course on DNN under the context of visual recognition.

> [Shakir Mohamed's talk](http://videolectures.net/deeplearning2016_mohamed_generative_models/) on Deep Generative Models in Deep Learning Summer School, 2016 <- Terrific summary of modelling principles and categorization of model classes. Also introduce recent advances in marrying Probabilistic modelling with DNN. 


## <a name="study">Course logistics</a>
2 sessions/week: 1x "**Lecture**" session + 1x optional "**Study-group**" session.
* ***Lectures*** are meant to lead you in the right direction --- just to get your started. They are **not** meant to tell you *everything* in *every details*. Thus, you should also utilize the reference reading materials, online resources for missing details *<- (the role of **self-study**)*

* It should be reckoned that we do not know everything (in many situations, we *don't even know what we don't know*), so do not hesitate to get in touch with the course instructors, the teaching assistant - TAs, your classmates, circles of friends for further support/discussion/...  *<- (the role of **Study-group**)* 


## <a name="map">The Map(s)  of Machine Learning</a>
The map below is one of many possible [projections](https://en.wikipedia.org/wiki/Map_projection) of Machine Learning. This map, in particular, focuses on **model classes** & connection to other fields of study. In addition, the map also aims to devise a *more principled* [**study-plan**](#plan){% sidenote 'sn-id-plan' "motivated by [metacademy\'s philosophy](https://metacademy.org/about)" %} to make it easier for aspiring ML self-learners to step-up/transit from [basic ML](https://www.coursera.org/learn/machine-learning) or DNN to PGM, ***given that they had covered the "base"*** (the first 4 parts in ["base" course's content](#note) above). 

*Note*: Open the image in new tab to view in full size. For a ***more comprehensive picture/maps*** of model classes, see [Shakir Mohamed's talk](http://videolectures.net/deeplearning2016_mohamed_generative_models/).

> ***Disclaimer***: The map was designed accordingly to my self-study/reading/working via MOOCs/papers/projects related to statistical machine learning, thus there might exist some (hopefully minor) inaccuracies. Any suggestions and critics to improve this map are highly appreciated. 

{% maincolumn 'assets/img/mapofML.png' "" %}

|:---:|:---|
|PGM | Probabilistic Graphical Models i.e. Probabilistic models |
|GLM | Generalized Linear Models |
|GMM, PPCA | (Gaussian) Mixture Models, Probabilistic Principle Component Analysis |
|HMM, LDS | Hidden Markov Models, Linear Dynamical Systems (for modelling *sequential data*) |
|Topic Models | Latent Dirichlet Allocation (LDA - *not to be confused with* Linear Discriminant Analysis) and variants |
|DNN | Deep Neural Networks |
|MLP, CNN | Multi-layer Perceptrons, Convolutional NNs i.e. FNN - Feed-forward NN |
|RNN | Recurrent NNs, also including Recursive NN and Bi-directional RNN (for modelling *sequential data*) | 
|"gates" | Gating mechanism: LSTM modules, GRUs, Residual connections |
|EBM | Energy-based Models (*undirected* PGM) |
|RBM, DBN, DBM | Restricted Boltzmann Machines, Deep Belief Networks (*not to be confused with* Dynamic Bayesian Networks), Deep Boltzmann Machines |
|VAE, DRAW, AIR | Variational Auto-encoder, Deep Recurrent Attentive Writer, Attention-Infer-Repeat |
|GAN | Generative Adversarial Networks |
|AAE | Adversarial Auto-encoders |
|SVM | Support Vector Machines |
|DP, GP | Dirichlet Processes, Gaussian Processes |
|Tree, RF | Decision Trees, Random Forests |
|kNN | k-Nearest Neighbours |

{% marginnote 'mn-id-global' 'The farther we go on the map, the more materials in *Global topics* we will also encounter' %}The <a name="plan">**study-plan**</a> can be read directly from the model classes i.e. the nodes in the map. The expected contents covered in each node is summarized in the list below, in which the references are chosen so that their technical details have as small overlap with the references in other nodes as possible. The objective is to optimize the time spent on learning, while covering wide enough spectrum of ML research. 

**Note**: From my experience, working on (research/practical) *projects* helps learn a lot of materials while making the theory less daunting, ***provided*** that you have ***firm foundation on the prerequisites*** or a ***big & complete picture*** of the projects. Your mileage may vary though.

> ***Disclaimer***. The following references are subject to my current expertise (which obviously has lots of room to improve). Any suggestions for better alternatives *and* for missing nodes in the study-plan are welcome. Also, [metacademy](https://metacademy.org/) is an excellent source to look for (in-depth) references if you want to learn about a new ML concept.
  
* base : as [Intended Learning Objectives](#ilo) above
> *refs*: [base-notes](#note), [base-ref](#ref)

* <a name="pgm">PGM</a> (all stochastic nodes{% sidenote 'sn-id-node' 'Nodes of the respective [*graphical model*](#graphical), not the study-plan' %}) : Intro. to Latent Variable Models + Bayesian inference methods (*Variational methods*, *MCMC sampling e.g. Gibbs sampling*) + Sparse regularization + (optional) convex optimization
> *refs*: as in "base" course's [Recap](#note) slides, optionally incl. HMM, LDS for modelling *sequential data*. Further reading: [Daphne Koller's course](https://www.coursera.org/specializations/probabilistic-graphical-models)

* <a name="dnn">DNN</a> (all deterministic nodes{% sidenote 'sn-id-node' 'Nodes of the respective [*graphical model*](#graphical), not the study-plan' %}) : "Architectures" + Applications of modern DNNs to CompVis, NLP + Attention mechanism + (optional) non-convex optimization
> *refs*: [CS231n](http://cs231n.stanford.edu/), [CS224d](http://cs224d.stanford.edu/). Further reading: [Nando de Freitas's course](https://www.youtube.com/playlist?list=PLE6Wd9FR--EfW8dtjAuPoTuPcqmOV53Fu) @ Oxford,  [Deep Learning textbook](http://www.deeplearningbook.org/)

* "Deep" PGM : <a name="ebm">Undirected PGM</a> + More MCMC sampling methods (*e.g. CD-k*)
> *refs*: TODO - [Daphne Koller's course](https://www.coursera.org/specializations/probabilistic-graphical-models) (undirected PGM lectures), last-half of [Geoffrey Hinton's NN course](https://www.coursera.org/learn/neural-networks), and/or [Ruslan Salakhutdinov's tutorials](https://www.cs.cmu.edu/~rsalakhu/) in KDD 2011/2014 (?)

* <a name="pgmdnn">PGM+DNN</a> : PGM whose stochastic nodes are parametrized by DNNs + Monte Carlo's SGD-based Variational Inference + Structured priors i.e. Structured latent factors (incl. probabilistic attention mechanism)
> *refs*: [Shakir Mohamed's talk](http://videolectures.net/deeplearning2016_mohamed_generative_models/) for the big picture + (huge body of) relevant works, especially VAE and variants.

* <a name="gan">GAN</a> : Adversarial learning + Optimize (minimax.) an objective function and related issues (*e.g. mode collapsing*) + Insight to Game Theory research (?)
> *refs*: TODO - Ian Goodfellow et al's original paper (obviously) + an up-to-date GAN survey (?)

* [TODO - other topics not mentioned]
> *refs*: distribute materials in pending reading lists to appropriate nodes
> [Metacademy's Bayesian ML roadmap](https://metacademy.org/roadmaps/rgrosse/bayesian_machine_learning)
> [Dr Truyen Tran's 3-part tutorial @ AusDM'16 + Exhaustive list of resources](https://truyentran.github.io/ausdm16-tute.html)
> Ferenc Huszar's posts, e.g. [Deep Learning is easy](http://www.inference.vc/deep-learning-is-easy/); [probabilistic interpretation of DAE](http://www.inference.vc/probabilistic-models-and-autoencoders-my-new-favourite-papers/)

* [TODO - ...]