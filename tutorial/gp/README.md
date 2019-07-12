# Tutorial: Gaussian Process Regression

> **Gaussian process regression** is a Bayesian model for **nonparametric** regression. (That is, nonparametric in the sense that the complexity of the regression function grows with the amount of data.) The model places a prior directly on the output values without reference to an underlying parametric model. (from [Metacademy](https://metacademy.org/graphs/concepts/gaussian_process_regression))

- 基本概念
  - [Gaussian processes (GP)](https://metacademy.org/graphs/concepts/gaussian_process_regression#focus=gaussian_processes&mode=learn): 简单来说就是多维正态变量的推广
  - 一个 GP 由 mean function $m(x)$ 与covariance function $k(x, x') = Cov (f(x), f(x'))$ 决定. Covariance $k(x,x')$ 决定了 GP 的形状与光滑性.

## 资源

- 阅读
  - (GPML) C. E. Rasmussen, C. K. I. Williams (2006), [Gaussian process for machine learning](http://www.gaussianprocess.org/gpml/)
    > Gaussian processes (GPs) provide a principled, practical, probabilistic approach to learning in kernel machines. GPs have received increased attention in the machine-learning community over the past decade, and this book provides a long-needed systematic and unified treatment of theoretical and practical aspects of GPs in machine learning. The treatment is comprehensive and self-contained, targeted at researchers and students in machine learning and applied statistics.
  - Kevin P. Murphy, [Machine Learning: a Probabilistic Perspective](https://www.cs.ubc.ca/~murphyk/MLbook/), the MIT Press (2012)
  - (PRML) Christopher M. Bishop (2011) [Pattern Recognition and Machine Learning](http://research.microsoft.com/en-us/um/people/cmbishop/PRML/index.htm)
  - [The Matrix Cookbook](http://www2.imm.dtu.dk/pubdb/views/edoc_download.php/3274/pdf/imm3274.pdf)
  - David Duvenaud, [The Kernel Cookbook](http://www.cs.toronto.edu/~duvenaud/cookbook/index.html)
  - [高斯世界下的Machine Learning](https://zhuanlan.zhihu.com/gpml2016)，知乎专栏
- Course
  - [Probabilistic Machine Learning 4f13 Michaelmas 2018](http://mlg.eng.cam.ac.uk/teaching/4f13/1819/), University of Cambridge
  - [](https://duvenaud.github.io/sta414/)
