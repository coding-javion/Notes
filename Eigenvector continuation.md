---
author: Chenjiawei
data: "20240113"
related:
  - "[[非正交基]]"
---
## 基本理论

Eigenvector continuation (EC) 属于 Reduced-Basis Method (RBM) 的一种。

Reduced-Basis Method 的流程如下：

- 建立关于感兴趣的量的积分形式的方程
	- 可以利用期待解的静态泛函（利用变分原理）
	- 也可以把基本的方程乘上试探函数后积分为零。（Galerkin approach）
- 利用高精度的解降低问题维度
- 解决低维问题
	- 对于变分形式，转化为广义本征值问题
	- 对于 Galerkin 形式，如果试探函数取为所得的高精度解，则同变分形式相同。

EC 的核心在于，当哈密顿量中的参数变化时，其本征矢几乎只在一个有限维且维度很小的子空间上运动。

哈密顿量应当具有如下的形式：

$$
H(\boldsymbol{\theta})=\sum_\alpha f_\alpha(\boldsymbol{\theta})H_\alpha
$$

其中 $\boldsymbol{\theta}$ 是一系列参数 $\{\theta_1,\theta_2,\cdots\}$，记 $|\psi_{i}\rangle$ 为参数取 $\boldsymbol{\theta}_{i}$ 时的哈密顿量本征矢 $|\psi (\boldsymbol{\theta}_{i})\rangle$。

由于本征矢几乎只在一个很小的子空间上运动，我们可以只在这个子空间上求解这个问题。由于这个小的子空间是由非正交基展开的，因此这对应于一个广义本征值问题。

定义：
$$
\begin{align*}
H_{ij} & =\langle\psi_{i}|H|\psi_{j}\rangle\\
N_{ij} & =\langle\psi_{i}|\psi_{j}\rangle
\end{align*}
$$
则对应的广义本征值问题为：

$$
\sum_{j}H_{ij}\beta_{j}=E\sum_{j}N_{ij}\beta_{j}
$$

## 体积依赖性



## 散射

散射问题可以利用 Kohn 变分法解决，因此可以利用 EC 解决[^1]。可以算波函数和相移。

## MBPT

利用 EC 可以使不收敛的 MBPT 变得更容易收敛。

[^1]: 实质上这应该是用所谓的 RBM 解决的，因为它并不与 EC 的步骤相同，但符合 RBM 的步骤。