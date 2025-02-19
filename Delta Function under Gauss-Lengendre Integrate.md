在 Gauss 积分中，普通的积分变为：

$$
\int f(x)\,\mathrm{d}x\rightarrow\sum_{i}w_{i}f(x_{i})
$$
原本的 $\delta$ 函数的性质为：

$$
\int f(x)\delta(x-x^{\prime})\,\mathrm{d}x=f(x^{\prime})
$$

在做离散化后，$x$ 变得只有一系列 $x_{i}$ 的离散取值。因此 $\delta (x-x^{\prime})$ 将会变成只有两个离散指标的函数，用 $\delta_{ij}^{\prime}$ 表示，则有：

$$
\begin{align*}
\sum_{i}w_{i}f(x_{i})\delta^{\prime}_{ij} & =f(x_{j})
\end{align*}
$$

于是可以很容易得到：
$$
\delta^{\prime}_{ij}=\frac{1}{w_{i}}\delta_{ij}
$$
其中，$\delta_{ij}$ 是通常的 Kroenecko $\delta$ 函数。