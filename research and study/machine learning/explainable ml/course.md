为什么 explainable ML 很重要？

1. correct anwsers $\neq$ intelligence
2. 具体各个领域都需要解释

牛顿力学需要解释吗？

1. 理论是自洽的

有没有 interpretable 和 powerful 并存的算法？

1. decision tree？
   1. too large tree
   2. random forest: harder to interpretable

目标是什么？
人脑也是黑盒子，为什么可以相信？
没有确定的目标，让人满意就可以？

分类
local/global explanation
local：类似于还原论的想法

图片：删除或者修改某些部分
有点像 test and error，暴力求解

saliency map：error 对 pixel 的偏微分
有点像稳定性测试 add terbulance to the input and see how the output change

时间序列的 saliency map？

eg：png 和 jpeg 背景颜色判断 pokemon 和 digimon

smoothgrad，加噪声得结果，试验很多次取平均

Limitation: gradient saturation
边际效应会减弱的，梯度不一定最重要

Integrated gradient (IG)

Attention is not (not) explanation

use the NN to reproduce the input

对于人类也没有相关数据的知识，可以利用 explainable ML 的技术从 ML 里得到 insight。
global explanation:

1. 不具体看某一个输入，而是看每一层是什么样子
2. 考虑什么样的输入来 maximize 某个类别的输出
   1. adversary attack 相关，输入会是噪声，怎么办？加 constriant，可以是数学的，也可以是从 image generator 生成的（？）

其他方法：用可解释的简单模型去替代黑盒子的部分
lIME: local interpretable model-agnostic explanations