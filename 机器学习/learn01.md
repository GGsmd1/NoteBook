## 机器学习入门
### 特征工程
开始机器学习的第一步是理解如何评估和改进数据集的质量。管理特征的类别和缺失、归一化和降维（PCA、ICA、NMF）是大幅提高算法性能的基本技术，而且还有助于研究如何将数据集分割成训练集和测试集、如何采取交叉验证来取代传统的测试方法。

### Numpy：Python 数值计算之王！
使用 Python 时，Numpy 不仅仅是一个库。它是几乎所有机器学习实现的基础，因此了解它的工作原理、关注向量化和广播（broadcasting）是非常必要的。这些技术可以帮助加速大多数算法的学习过程，利用多线程和 SIMD、MIMD 架构的力量。

### 数据可视化
Matplotlib 即使不是纯粹的机器学习话题，了解如何可视化数据集也很重要。Matplotlib 可能是最广泛使用的解决方案：Matplotlib 易用，允许绘制不同种类的图表。Bokeh 和 Seaborne 提供了有趣的替代方案。不必要彻底了解所有包，但是了解每一个包的优点和弱点还是很有用的，可以帮助你选择合适的包。

了解 Matplotlib 细节的资源：《掌握 Matplotlib》，McGreggor D. 著


### 线性回归
线性回归是最简单的模型之一，可以把它作为一个优化问题来研究，该问题可通过最小化均方误差而得到求解。该方法虽然有效，但是限制了可利用的可能性。我建议还可以把它当作贝叶斯问题，使用之前的可能性展示参数（比如，高斯分布），优化变成了最大似然估计（Maximum Likelihood Estimation，MLE）。即使这看起来更加复杂，但该方法提供了一个可供几十个其他复杂模型共享的新方法。


### 线性分类
通常情况下，Logistic 回归是最佳起始点，也是研究信息论进而了解信息熵、交叉熵和互信息的好机会。类别交叉熵（Categorical cross-entropy）是深度学习分类中最稳定、使用最广泛的代价函数，一个简单的 logistic 回归可以展示它是如何加速学习过程的（与均方差相比）。另一个重要的话题是正则化（Ridge、Lasso 和 ElasticNet）。很多情况下，人们认为它是一种提高模型准确率的深奥方式，但是它的真实意义是更准确，在具体实例的帮助下变得易于理解。我还建议刚开始的时候，把 logistic 回归当作一个简单的神经网络，可视化（以 2D 实例为例）权重向量在学习过程中的移动轨迹。

我还建议本节应包括超参数网格搜索。网格搜索不在没有完整了解的情况下尝试不同的值，而是评估不同的超参数集的性能。因此，工程师可以将注意力集中在可达到最高准确率的组合上。当然还有更加强大的贝叶斯优化方法，即利用先验知识逼近未知目标函数的后验分布从而调节超参数的方法。

### 支持向量机（SVM）
支持向量机提供了不同的分类方法（包括线性和非线性方法）。该算法非常简单，具备基础几何知识的人也可以学会。不过，了解核支持向量机的工作原理非常有用，因为它会在线性方法失败的时候展示出其真正实力。


### 决策树
决策树提供了另一种分类和回归的方法。通常，它们不是解决复杂问题的首选，但它们提供了完全不同的方法，即使是非技术人员也可以很容易理解，该方法还可以在会议或演示中可视化。

### 集成学习boosting
在理解了决策树的动态特性以后，研究集成训练树的集（集成）来提高整体准确率的方法很有用。随机森林、梯度树提升和 AdaBoost 都是强大的算法，且复杂度较低。对比简单的树和提升方法与 bagging 方法采用的树的学习过程挺有趣的。Scikit-Learn 提供了最常见的实现方法，但是如果你想更好地驾驭这些方法，我还是建议你在 XGBoost 上多花些时间，XGBoost 是一个既适用于 CPU 又适用于 GPU 的分布式框架，即使在较大的数据集上也能加速学习过程。

### 聚类
当开始聚类方法的学习时，我的建议是从高斯混合算法（基于期望最大化/EM）学起。虽然 K-均值聚类要更加简单易懂（也是必须要学习的），但是高斯混合算法为我们提供了纯粹的贝叶斯方法，在其他类似任务中也十分实用。其它必学的算法还有层次聚类（Hierarchical Clustering）、谱聚类（Spectral Clustering）和 DBSCAN。这对你了解基于实例的学习或研究 K-近邻算法（既适用于有监督又适用于无监督任务）也是有帮助的。

### 神经网络入门
神经网络是深度学习的基础，你可以在单独的课程中学习神经网络。但是，我认为理解感知机、多层感知机以及反向传播算法的概念也很有帮助。Scikit-Learn 提供了一个实现神经网络的简单方法，但是，开始探索 Keras 也是一个好主意，Keras 是一个基于 Tensorflow、Theano 或 CNTK 的高级架构，允许使用最少的努力对神经网络进行建模和训练。

