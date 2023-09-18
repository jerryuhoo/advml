## 指数族 (Exponential Family)

指数族是一大类概率分布，它们可以被写成一个特定的形式。许多常见的概率分布如正态分布、柏松分布和Bernoulli分布都属于这个家族。

一个概率分布属于指数族，如果它的概率密度函数 (对于连续型变量) 或概率质量函数 (对于离散型变量) 可以被写为如下形式：

\[ p(x | \theta) = h(x) \exp(\eta(\theta) \cdot T(x) - A(\theta)) \]

其中:

- \( x \) 是观察到的数据
- \( \theta \) 是分布的参数
- \( \eta(\theta) \) 是自然参数或链接函数
- \( T(x) \) 是统计量函数
- \( h(x) \) 是基础测度
- \( A(\theta) \) 是对数分割函数，确保概率函数积分或求和为1

### Bernoulli分布

对于Bernoulli分布，我们的随机变量 \( X \) 可以取0或1的值，其概率质量函数为：

\[ P(X=k) = p^k (1-p)^{1-k} \]

转化为指数族形式，我们可以得到：

\[ p(x|p) = \exp(x\log\left(\frac{p}{1-p}\right) + \log(1-p)) \]

其中，自然参数 \( \eta(p) = \log\left(\frac{p}{1-p}\right) \) 和对数分割函数 \( A(p) = -\log(1-p) \)。

### 柏松分布

柏松分布描述了在给定的时间段或空间中事件发生的次数，其概率质量函数为：

\[ P(X=k) = \frac{\lambda^k e^{-\lambda}}{k!} \]

转化为指数族形式，我们得到：

\[ p(x|\lambda) = \frac{1}{x!} \exp(x\log(\lambda) - \lambda) \]

其中，自然参数 \( \eta(\lambda) = \log(\lambda) \) 和对数分割函数 \( A(\lambda) = \lambda \)。
