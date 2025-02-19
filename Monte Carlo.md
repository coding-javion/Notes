Monte Carlo 是对一类利用采样方式计算期望的方法的统称。它的一个应用是记算积分。对于任意一个积分：

$$
I=\int f(x)\,\mathrm{d}x
$$

可以做如下转换：

$$
I = \int \frac{f(x)}{p(x)}p(x)\,\mathrm{d}x\equiv\int \tilde{f}(x)p(x)\,\mathrm{d}x
$$

其中 $p(x)$ 是一个概率分布。我们只需要按照 $p(x)$ 的概率产生随机数，根据中心极限定理，积分值可以使用如下平均值代替：

$$
I\approx\frac{1}{M}\sum_{i=1}^{M}\tilde{f}(x_{i})
$$

其中 $M$ 是产生的随机数的个数。由此，可以通过概率分布做取样来计算积分。

当然，实际应用时，Monte Carlo 方法一般用来算高维积分，此时产生的就不是随机数，而是随机**位形**$\boldsymbol{\boldsymbol{x}}$。使用 Markov 链就是一种按照 $\rho(x)$ 的概率产生随机位形的方式。

量子蒙卡在 thijssen 书中有不错的介绍。