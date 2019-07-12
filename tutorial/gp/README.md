# Tutorial: Gaussian Process Regression

> **Gaussian process regression** is a Bayesian model for **nonparametric** regression. (That is, nonparametric in the sense that the complexity of the regression function grows with the amount of data.) The model places a prior directly on the output values without reference to an underlying parametric model. (from [Metacademy](https://metacademy.org/graphs/concepts/gaussian_process_regression))
![gp](.\Gaussian_Process_Regression.png)

- 要点
  - [Gaussian processes (GP)](https://metacademy.org/graphs/concepts/gaussian_process_regression#focus=gaussian_processes&mode=learn), [wiki](https://en.wikipedia.org/wiki/Gaussian_process): 简单来说就是多维正态变量的推广
  - 一个 GP 由 mean function $m(x)$ 与covariance function $k(x, x') = Cov (f(x), f(x'))$ 决定. Covariance $k(x,x')$ 决定了 GP 的形状、光滑性、周期性.
  - Gaussian process regression is a **kernelized** version of Bayesian linear regression.
  - 超参：In order to apply Gaussian processes in practice, it is necessary to fit the **hyperparameters** of the model, such as the **lengthscale** and **variance** of a squared-exp kernel. **Marginal likelihood** is one commonly used criterion for doing so. (参见 prml 6.4.3, gpml Ch5)
  - Inference of continuous values with a Gaussian process prior is known as **Gaussian process regression**, or **kriging**
  - Extending Gaussian process regression to **multiple** target variables is known as **cokriging**.
  - Gaussian process regression can be further extended to address learning tasks in both supervised (e.g. **probabilistic classification**) and unsupervised (e.g. **manifold learning** [prml]) learning frameworks.
  
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
- 相关学者
  - [Carl Edward Rasmussen](http://mlg.eng.cam.ac.uk/carl/): Cambridge, gpml 作者
  - [Zoubin Ghahramani](http://mlg.eng.cam.ac.uk/zoubin/): Cambridge
  - [Kevin P Murphy](https://www.cs.ubc.ca/~murphyk/): google
  - [David Duvenaud](http://www.cs.toronto.edu/~duvenaud/): University of Toronto
