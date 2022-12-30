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

#### 

