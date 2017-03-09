---
layout: post
title: "Machine learning appendix"
date: 2017-02-01
category: t
---
_(to be updated sporadically)_
For personal use, but suggestions are highly appreciated.
<!--more-->

## <a name="glossary">Glossary</a>
Glossary of common terms and their _synonyms_ (or <em><font color="red">strongly related</font></em>).

> $$\text{Pr}\left(x\right)$$ is written in place of $$\text{Pr}\left(X=x\right)$$ for brevity. Read [more](#more).

| Term | Common notations and more information (if any)|
|:---- |:-----------------------|
| estimation/prediction/inference of a quantity  | the quantity with a "hat" eg. $$\hat{y}$$, $$\hat{\theta}$$, $$\text{Pr}\left(y\left\|x,\hat{\theta}\right.\right)$$ |
| *ước lượng/dự đoán/suy diễn một đại lượng nào đấy* |  |
| objective function, error function, loss function, cost function | $$J\left(\cdot\right)$$ ; or $$L\left(\cdot\right)$$ ; or $$l\left(\cdot\right)$$ |
| *hàm mục tiêu, hàm lỗi, hàm tổn thất, hàm chi phí* |  |
| learning, training; <font color="red">related</font>:  parameter estimation | |
| *học mô hình, huấn luyện mô hình, ước lượng tham số* |  |
| evaluating, forward pass - *as in* "computing some quantity given estimates of all unknown quantities" | <font color="red">note</font>: not to be confused with `performance evaluation`
| *tính toán, chiều xuôi*  | |
| score function; <font color="red">related</font>: (inverse) link function | $$s\left(\cdot\right)$$ ; or $$g\left(\cdot\right)$$ if link function |
| *hàm tính điểm, hàm liên kết* |  |
| neuron/unit; <font color="red">related</font>: dimension (of a vector) | $$x_{d}$$ where $$d$$ is a dimesion of vector $$x$$|
| *nơ-ron, chiều (của một vec-tơ)* |  |
| feature; <font color="red">related</font>: independent variable, explanatory variable, predictor | $$x_{d}$$ where $$d$$ is a dimesion of vector $$x$$. <font color="red">note</font>: in practice, most of the time we imply `feature` as `feature vector`, thus use vector $$x$$ instead  |
| *vec-tơ đặc trưng, biến độc lập, biến giải thích, nhân tố giải thích* |  |
| mid-/high-level feature, hidden/latent variable; <font color="red">related</font>: hidden neuron**s**/unit**s** | $$z$$ ; or $$h$$ ; or $$\theta$$ if assumed a random variable |
| *đặc trưng bậc trung hoặc bậc cao, biến ẩn, các nơ-ron ẩn* | |
| target, label; <font color="red">related</font>: dependent variable, response variable | $$y$$ ; or $$t$$ |
| *mục tiêu, nhãn, biến phụ thuộc, biến (?)* | |
| observed data/variable(s), | $$\mathcal{D}$$ ; or $$x$$ ; or $$x$$ and $$y$$ if supervised learning |
|*dữ liệu/biến quan sát được (đã biết)* | |
| unobserved data/variable(s) | $$\tilde{\mathcal{D}}$$ ; or $$\tilde{\mathcal{x}}$$ ; or $$x'$$ ; or $$x^{\left(\text{new}\right)}$$ |
| *dữ liệu/biến không quan sát được (chưa biết)* | |
| data point | $$x$$ ; or (if working with more than 1 data point) $$x^{\left(n\right)}$$, or $$x_{n}$$ if $$x$$ represents a set of data points |
| *điểm dữ liệu* |  |
| parameter; <font color="red">related</font>: weight, bias (as the "offset" from the origin) | $$\theta$$ , $$W$$, $$b$$ respectively |
| *tham số, trọng số, độ lệch* | <font color="red">note</font>: `bias` is an [umbrella term](https://en.wikipedia.org/wiki/Umbrella_term) |
| | `bias` has more [common meanings](https://en.wikipedia.org/wiki/Bias_(statistics)) |
| parameterized function | $$f\left(x,y\,\mathbf{;}\,\theta\right)$$  |
|*hàm có tham số* | |
| parametric distribution | $$p\left(x\mathbf{;}\,\theta\right)$$; or $$p_{\theta}\left(x\right)$$ where {% m %} p\left(\cdot\right) {% em %} is density function |
| *phân bố xác suất có tham số* | 

### <a name="more">More notation</a> 

> For brevity, $$\text{Pr}\left(x\right)$$ is often seen in ML literature instead of $$\text{Pr}\left(X=x\right)$$ as in statistical texts. I also use an overhead circle e.g. {% m %} \overset{\circ}{x} {% em %} to denote random variable, in place of capital letters e.g. X, N, K which are preserved for either sets of data points, matrices, or total number of samples/classes/features/...

| Notation | |
|:---:|:---|
|{% m %} \overset{\circ}{y_{n}} {% em %} | A random variable. Thus {% m %} \text{Pr}\left(\overset{\circ}{y_{n}}\|\cdot\right) {% em %} implies a probability distribution. |
|{% m %} y_{n} {% em %} | A realization of random variable {% m %} \overset{\circ}{y_{n}} {% em %}. Thus {% m %} \text{Pr}\left(y_{n}\|\cdot\right) {% em %} is a value. |
| {% m %} \Omega_{\overset{\circ}{y_{n}}} {% em %} | Set of all possible realization {% m %} y_{n}{% em %}'s of random variable {% m %} \overset{\circ}{y_{n}} {% em %} i.e. ***sample space*** of {% m %} \overset{\circ}{y_{n}} {% em %}. |
|{% m %} \hat{y}_{n} {% em %} | An estimate of random variable {% m %} \overset{\circ}{y_{n}} {% em %} |
| {% m %} \underset{y_{n}^{'}}{\text{argmax}}\text{Pr}\left(y_{n}^{'}\|\cdot\right) {% em %} | short for {% m %} \underset{y_{n}^{'}\in\Omega_{\overset{\circ}{y_{n}}}}{\text{argmax}}\text{Pr}\left(\overset{\circ}{y_{n}}=y_{n}^{'}\|\cdot\right) {% em %}. We use notation {% m %} y_{n}^{'} {% em %} to not confuse with {% m %} y_{n} {% em %} which is reserved for the realization provided by training data {% m %} \mathcal{D}=\left\{ x_{n},y_{n}\right\}_{n=1}^{N}  {% em %}. |

## Back-propogation algorithm
{% marginnote 'backprop-demo' "*Conditions*: (i) J is differentiable every where w.r.t. theta; (ii) J and all thetas form a directed acyclic computational graph." %} **For what**: computes gradient {% m %} 
\nabla_{\theta}J=\dfrac{\partial J}{\partial\theta} {% em %} for **all** {% m %} \theta 
{% em %}'s of interest. 
[[Demo](#)] TODO

*Use case(s)*: update optimal parameter {% m %} \hat{\theta} {% em %}'s of a neural network (or a certain class of probabilistic models) by gradient descent algorithms; 

## Manifold learning
> __Manifold Learning__ (often also referred to as [__non-linear dimensionality reduction__](http://en.wikipedia.org/wiki/Nonlinear_dimensionality_reduction)) pursuits the goal to ___embed data that originally lies in a high dimensional space in a lower dimensional space___, while preserving characteristic properties. This is possible because *for any high dimensional data to be interesting, it must be intrinsically low dimensional*. For example, images of faces might be represented as points in a high dimensional space (let's say your camera has 5MP -- so your images, considering each pixel consists of three values \[r,g,b\], lie in a 15M dimensional space), but not every 5MP image is a face. Faces lie on a sub-manifold in this high dimensional space. A **sub-manifold** is ___locally Euclidean___, i.e. if you take two _very similar points_, for example two images of identical twins, you can _interpolate_ between them and still _obtain an image on the manifold_, but ___globally not Euclidean___ -- if you take two images that are very different --- for example [Arnold Schwarzenegger](http://www.anorak.co.uk/wp-content/uploads/2011/07/31.jpeg) and [Hillary Clinton](http://vivirlatino.com/i/2008/11/hillary-clinton.jpg) -- you _cannot interpolate_ between them{% sidenote 'sn-manifold-global' "The example assumely talked about a \"limited\" face image manifold right?" %}.
> <cite>[(ref)](http://www.cs.cornell.edu/~kilian/research/manifold/manifold.html)</cite>
