### 38 Introduction to NNs
三个方向：启发人脑生物学研究，自动化学习，复杂系统研究
取名的来源，潜在商业价值，解释性研究

#### 38.1 Memories
Addressed-based memory 和 biological memory 的对比：其他记忆系统有两者共有的性质，比如搜索引擎和推荐系统。

很多心理学实验表明 biological memory 在时间维度而言没有那么robust。

architecture, activity rule, learning rule,
architecture and forward stage and backpropagation?

#### 39 The single Neuron as a Classifier
这个思路其实是从最简单的例子开始，和现在dl的思路不一样
linear layer with activation function

threshold function, stochastic activation functions,
no relu

example: sigmoid activation function
how to analyze the function: perpendicular to $w$ or not

weight space: training means searching in the weight space

why take the gradient wrt the weight?
-- weight space

interesting: through analysis of the evolution of the training process, which also leads to the following regularization section

Figure, 39.4
(d): not converge yet

momentum is also not recommended
conjugate gradient algorithms?

ex39.5 In the problem of posterior in bionormial distribution, the sigmoid function appears natually. This is why commuication problems are connected with it.

ex 39.6 similar

ex 40.1 2^N
ex 40.2 2^0 + 2^1 + ... 2^(N-1) = 2^N - 1
ex 40.3 2 * (1/2) ^ 3 = 1/4

#### 40.2 The capacity of a single neuron
binary threshold neuron
only the training set is used
这是一个组合问题：用线性分类器可以有多少种分割方案。
问题是在优化的框架下，这样的信道容量有什么意义呢？
有一些数据是线性不可分的，那么引入非线性或者使用其他技巧（如svm软间隔）就可以了。
stop at p489

### 41 Learning as Inference
Uses a two dimensional parameter example w to show the difference between MLE and bayesian inference. Figure 41.2 are the results.

stop at 41.3, the following parts are different methods to help calculate the intractable bayesian predictions.

### 45 Gaussian Processes
Introduce the "function space" to replace "parameter space" in the bayesian inference framework.

Reservations: equivalency between NN and GP? computational cost?
#### 45.1 Standard methods for nonlinear regression
parametric approaches:
nonparametric approaches: 
example: spline smoothing method
$$M(y(x)) = \frac{1}{2}\beta \sum _{n=1}^{N}(y(x^{(n)})-t_n)^2 + \frac{1}{2}\int [y^{(p)}(x)]^2$$
$p$th derivative

Splines prior are Gaussian process.

45.12, 45.13, below

#### 45.2 From parametric models to Gaussian processes

$y$ linear on $w$,
$$y = Rw$$ 
consider the prior of w, $N(0, \sigma _{w}^2 I)$ then $p(y) 
\sim N(0, \sigma _{w}^2I  RR^T)$
Consider the nosie on t, which also makes the Cov matrix full rank,
final result 45.26
some sampling results
#### 45.3 Using a given Gaussian process model in regression
45.42, 45.43
and some computation complexity analysis
#### Examples of Covariance functions
literature: 
2013 Gaussian process kernels for pattern discovery and extrapolation
Abrahamsen (1997)

FT of a Gaussian is a Gaussian:
https://math.stackexchange.com/questions/1267007/inverse-fourier-transform-of-gaussian

Stationary Covariance functions
nonstationary covariance functions
#### Adaptation of GP models
Learn parameters in GP
When the gradient can be calculated.

#### Classification

Left: 
simulation of:
Figure 45.1
45.55
45.2 



