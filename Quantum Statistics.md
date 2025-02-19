---
related:
  - "[[Density Matrix]]"
---

## 正则系综

假如 $|\varphi_{i}\rangle$ 是哈密顿量 $H$ 的本征右矢，$E_{i}$ 是对应的本征值，对于正则系综，系统处于 $|\varphi_{i}\rangle$ 态的概率是：

$$
\frac{1}{Z}\mathrm{e}^{-\beta E_{i}}
$$

其中 $Z=\sum_{i}\mathrm{e}^{-\beta E_{i}}$ 是配分函数。如此，密度矩阵为 $\rho=\sum_{i}\omega_{i}|\varphi_{i}\rangle\langle\varphi_{i}|$ 的情况下，显然有：

$$
\omega_{i}=\frac{1}{Z}\mathrm{e}^{-\beta E_{i}}
$$

于是我们可以得到：

$$
\begin{align*}
\rho & =\frac{1}{Z}\sum_{i}\mathrm{e}^{-\beta E_{i}}|\varphi_{i}\rangle\langle\varphi_{i}|=\frac{1}{Z}\sum_{i}\mathrm{e}^{-\beta\hat{H}}|\varphi_{i}\rangle\langle\varphi_{i}|\\
 & =\frac{1}{Z}\mathrm{e}^{-\beta\hat{H}}
\end{align*}
$$

而配分函数可以写为：

$$
Z=\sum_{i}\mathrm{e}^{-\beta E_{i}}=\mathop{\mathrm{Tr}}\mathrm{e}^{-\beta \hat{H}}
$$

如果我们令重新定义 $\hat{D}=\mathrm{e}^{-\beta \hat{H}}$ 为未归一化的密度矩阵，我们可以得到其遵循的微分方程：

$$
-\frac{\partial\hat{D}}{\partial\beta}=\hat{H}\hat{\rho}
$$

实际使用时密度矩阵时常是未归一化的。

### 正则系综密度矩阵作为自由能极值点

自由能 $F=E-TS$，在量子统计中可以写为：

$$
\mathop{\text{Tr}}[\hat{\rho}(\hat{H}+\frac{1}{\beta}\ln\hat{\rho})]
$$

考虑约束 $\mathop{\text{Tr}}\hat{\rho}=1$，容易计算得到：

$$
\begin{align*}
\frac{\delta(F-\lambda\mathop{\text{Tr}}\hat{\rho})}{\delta\hat{\rho}} & =\mathop{\text{Tr}}(\delta\hat{\rho}\hat{H})+\frac{1}{\beta}\mathop{\text{Tr}}(\delta\hat{\rho}\ln\hat{\rho}+1)-\lambda\mathop{\text{Tr}}\delta\hat{\rho}\\
 & =\mathop{\text{Tr}}[\delta\hat{\rho}(\hat{H}+\frac{1}{\beta}\ln\hat{\rho}+\frac{1}{\beta}-\lambda)]
\end{align*}
$$

令其为零，得到：

$$
\rho=\mathrm{e}^{-\beta\hat{H}}\mathrm{e}^{\beta\lambda-1}
$$

考虑约束条件，即可得到：

$$
\begin{align*}
\hat{\rho} & =\frac{1}{Z}\mathrm{e}^{-\beta\hat{H}}\\
Z & =\mathop{\text{Tr}}(\mathrm{e}^{-\beta\hat{H}})
\end{align*}
$$

进一步计算二阶变分也可以证明，它实际上是自由能的最小值点。

### 零温极限

零温极限意味着 $\beta\rightarrow\infty$，假设哈密顿量 $\hat{H}=E_{0}+\hat{H}^{\prime}$，其中 $E_{0}$ 是基态能量，那么此时配分函数为：

$$
\begin{align*}
Z & =\mathrm{e}^{-\beta E_{0}}\mathop{\text{Tr}}(\mathrm{e}^{-\beta\hat{H^{\prime}}})\\
 & =\mathrm{e}^{-\beta E_{0}}\sum_{n}\langle n|\mathrm{e}^{-\beta\hat{H^{\prime}}}|n\rangle\\
 & =\mathrm{e}^{-\beta E_{0}}\sum_{n}\mathrm{e}^{-\beta E_{n}^{\prime}}\\
 & =\mathrm{e}^{-\beta E_{0}}
\end{align*}
$$


保留首阶可以看出，此时配分函数指数的趋近于零。只有 $E_{0}=0$ 才可以使得 $Z=1$。

但配分函数为零并无影响，我们真正要计算的是物理量的期待值，即：

$$
\frac{\mathop{\text{Tr}}(\mathrm{e}^{-\beta(E_{0}+\hat{H}^{\prime})}\hat{O})}{\mathop{\text{Tr}}(\mathrm{e}^{-\beta(E_{0}+\hat{H}^{\prime})})}
$$
而很容易可以看出，在 $\beta\rightarrow \infty$ 时，上式趋近于 $\langle\Psi|\hat{O}|\Psi\rangle$，正是零温的情况。


## 巨正则系综

对于巨正则系综，只需令：

$$
\omega_{i}=\frac{1}{\Xi}\mathrm{e}^{-\beta(E_{i}-\mu N_{i})}
$$

这里巨正则配分函数为：

$$
\Xi=\sum_{i}\mathrm{e}^{-\beta(E_{i}-\mu N_{i})}
$$

即可得到：

$$
\Xi=\mathop{\text{Tr}}\mathrm{e}^{-\beta(\hat{H}-\mu\hat{N})}
$$

和：

$$
\hat{\rho}=\frac{1}{\Xi}\mathrm{e}^{-\beta(\hat{H}-\mu\hat{N})}
$$

对于这里未归一化的密度矩阵 $\hat{D}=\mathrm{e}^{-\beta (\hat{H}-\mu\hat{N})}$，我们也可以得到：

$$
-\frac{\partial\hat{D}}{\partial\beta}=\hat{H}\hat{\rho}
$$

### 巨正则密度矩阵作为巨势的极值点

巨势 $J=E-TS-\mu N$，量子统计中可写为：

$$
\mathop{\text{Tr}}[\hat{\rho}(\hat{H}+\frac{1}{\beta}\ln\hat{\rho}-\mu\hat{N})]
$$

考虑约束 $\mathop{\text{Tr}}\hat{\rho}=1$，容易计算得到：

$$
\begin{align*}
\frac{\delta(J-\lambda\mathop{\text{Tr}}\hat{\rho})}{\delta\hat{\rho}} & =\mathop{\text{Tr}}(\delta\hat{\rho}\hat{H})+\frac{1}{\beta}\mathop{\text{Tr}}(\delta\hat{\rho}\ln\hat{\rho}+1)-\mu\mathop{\text{Tr}}(\delta\hat{\rho}\hat{N})-\lambda\mathop{\text{Tr}}(\delta\hat{\rho})\\
 & =\mathop{\text{Tr}}[\delta\hat{\rho}(\hat{H}+\frac{1}{\beta}\ln\hat{\rho}+\frac{1}{\beta}-\mu\hat{N}-\lambda)]
\end{align*}
$$

令其为零并考虑约束条件即得：

$$
\begin{align*}\hat{\rho} & =\frac{1}{\Xi}\mathrm{e}^{-\beta(\hat{H}-\mu\hat{N})}\\
\Xi & =\mathop{\text{Tr}}(\mathrm{e}^{-\beta(\hat{H}-\mu\hat{N})})
\end{align*}
$$

进一步可以证明，它实际上是巨势的最小值点。

若考虑限制粒子数为 $N$，则我们需要最小化的为：

$$
\mathop{\text{Tr}}[\hat{\rho}(\hat{H}+\frac{1}{\beta}\ln\hat{\rho}-\mu(\hat{N}-N))]
$$

由于多出来的项只是常数，由此得到的密度矩阵仍为上面的样子。这说明巨正则系综中是无法限制粒子数的。