---
related:
  - "[[Quantum Statistics]]"
---
## 基本理论

假设我们要考虑的对称群为 $G$，其对称群群元为 $g$。$|\lambda\mu\rangle$ 展开了该群的不可约表示空间，其中 $\lambda$ 标记了这个不可约表示，$\mu$ 标记了不同的态矢。群元 $g$ 对应的表示记为 $D (g)$，$\lambda$ 标记的不可约表示为 $D^{\lambda}(g)$，而相应的矩阵分量记为 $D_{\mu\nu}^{\lambda}(g)$ 。那么我们显然有：

$$
D(g)|\lambda\nu\rangle=\sum_{\mu}D_{\mu\nu}^{\lambda}(g)|\lambda\mu\rangle
$$

如果是对称群是有限群，由群表示的正交定理，我们知道：

$$
\frac{1}{\left|G\right|}\sum_{g}D_{\mu\nu}^{\lambda*}(g)D_{\mu^{\prime}\nu^{\prime}}^{\lambda^{\prime}}(g)=\frac{1}{d_{\lambda}}\delta_{\lambda\lambda^{\prime}}\delta_{\mu\mu^{\prime}}\delta_{\nu\nu^{\prime}}
$$

这里 $d_{\lambda}$ 是不可约表示的维度，$\left|G\right|$ 是群的阶，对有限群来说它就等于群元素的个数。

然而我们实际考虑的往往是紧李群，对紧李群来说，我们需要做替换：

$$
\frac{1}{\left|G\right|}\sum_{g}\rightarrow\int\mathrm{d}g
$$

这里李群上的积分使用归一的 Harr 测度，有 $\int_{G}\mathrm{d}g=1$。因此我们实际通常使用的式子为：

$$
\int\mathrm{d}g\,D_{\mu\nu}^{\lambda*}(g)D_{\mu^{\prime}\nu^{\prime}}^{\lambda^{\prime}}(g)=\frac{1}{d_{\lambda}}\delta_{\lambda\lambda^{\prime}}\delta_{\mu\mu^{\prime}}\delta_{\nu\nu^{\prime}}
$$

结合前面的式子，我们容易得到：

$$
\int\mathrm{d}gD_{\mu\nu}^{\lambda*}(g)D(g)|\lambda^{\prime}\nu^{\prime}\rangle=\frac{1}{d_{\lambda}}\delta_{\lambda\lambda^{\prime}}\delta_{\nu\nu^{\prime}}|\lambda\mu\rangle
$$

我们可以定义算符：

$$
P_{\mu\nu}^{\lambda}=d_{\lambda}\int\mathrm{d}g\,D_{\mu\nu}^{\lambda*}(g)D(g)
$$

这一算符作用到态矢上有 $P_{\mu\nu}^{\lambda}|\lambda^{\prime}\nu^{\prime}\rangle=|\lambda\mu\rangle$，因此实际上有 $P_{\mu\nu}^{\lambda}=|\lambda\mu\rangle\langle\lambda\nu|$ ，很容易看出 $P_{\mu\mu}^{\lambda}$ 为投影算符。由于投影算符之和仍为投影算符，因此接下来我们可以进一步定义投影算符：

$$
P^{\lambda}=\sum_{\mu}P_{\mu\mu}^{\lambda}=d_{\lambda}\int\mathrm{d}g\,\chi_{\lambda}^{*}(g)D(g)
$$

这里 $\chi_{\lambda}(g)=\sum_{\mu}D_{\mu\mu}^{\lambda}(g)$ 为不可约表示 $\lambda$ 的特征标。

## 应用

将此理论应用于不同的对称群即可。

### 粒子数投影算符

$$
\hat{P}^{N}=\frac{1}{2\mathrm{\pi}}\int\mathrm{d}\phi\,\mathrm{e}^{\mathrm{i}\phi N}\mathrm{e}^{-\mathrm{i}\phi\hat{N}}
$$

### 动量投影算符

$$
\hat{P}^{\boldsymbol{P}}=\frac{1}{V}\int\mathrm{d}\boldsymbol{x}\,\mathrm{e}^{\mathrm{i}\boldsymbol{x}\cdot\boldsymbol{P}}\mathrm{e}^{-\mathrm{i}\boldsymbol{x}\cdot\hat{\boldsymbol{P}}}
$$

### 角动量投影算符

如果使用Euler角，则有：

$$
\hat{P}^{J}=\frac{2J+1}{16\mathrm{\pi}^{2}}\int_{0}^{4\mathrm{\pi}}\mathrm{d}\alpha\int_{0}^{\mathrm{\pi}}\sin\beta\mathrm{d}\beta\int_{0}^{2\mathrm{\pi}}\mathrm{d}\gamma\,\chi^{*}_{J}(R)\hat{U}(R)
$$

这里用 $R$  表示 Euler 角 $R (\alpha,\beta,\gamma)$。特征标为：

$$
\chi_{J}(R)=\sum_{M}\langle JM|U(R)|JM\rangle
$$

转动群的表示为：

$$
\hat{U}(R)=\mathrm{e}^{\mathrm{i}\alpha \hat{J}_{z}}\mathrm{e}^{\mathrm{i}\beta \hat{J}_{y}}\mathrm{e}^{\mathrm{i}\gamma \hat{J}_{z}}
$$

## 有限温情况

设密度矩阵为 $\rho$，投影算符为 $P$，则投影后的配分函数为：

$$
Z_{p}=\mathop{\text{Tr}}(P\rho P)=\mathop{\text{Tr}}(P\rho)
$$

投影后的密度矩阵为：

$$
\rho_{p}=\frac{1}{Z_{p}}P\rho P
$$

于是可观测量为：

$$
\langle O\rangle_{p}=\mathop{\text{Tr}}(\rho_{p}O)
$$

之所以不能直接写成 $\langle O\rangle_{p}=\mathop{\text{Tr}}(P\rho O)$，是因为在密度矩阵为纯态的时候要能回复到表达式 $\langle O\rangle_{p}=\langle\Psi|POP|\Psi\rangle$。