---
title: Multi channel scattering
author: Chenjiawei
date: 2023-01-27 15:24
---
## 多道散射

![](D:/Research/Repo/附件/多道散射.svg)

## 分道哈密顿量与渐进态

考虑如下情况的散射

$$
a+(bc)\rightarrow\begin{cases}
a+b+c & \text{1 break up}\\
a+(bc) & \text{2 elastic}\\
a+(bc)^{*} & \text{3 excitation}\\
b+(ac) & \text{4 rearrangement}
\end{cases}
$$

对不同的道，渐进哈密顿量不一定相同，称为分道哈密顿量。例如，在只考虑二体力的情况下，对于 $1$ 道有：

$$
H=\sum_{i=1}^{3}\frac{p_{i}^{2}}{2m_{i}}
$$

而对于 $2,3$ 道有

$$
H=\sum_{i=1}^{3}\frac{p_{i}^{2}}{2m_{i}}+V_{bc}
$$

因此，渐进态也不一样，例如对于 $1$ 道，渐进态即三个粒子的自由运动，而对于 $4$ 道，渐进态为：

$$
\psi^4(\boldsymbol{x})=\phi(\boldsymbol{x}_{b},\bar{\boldsymbol{x}}_{ac})\varphi_{(ac)}(\boldsymbol{x}_{ac})
$$

这里 $\phi$ 描述 $b$ 和 $(ac)$ 的自由运动，$\varphi$ 描述 $(ac)$ 这一束缚态的内部运动[^1]。

## 多道 $S$ 算符

尽管实际上的粒子只从一个道入射，但为了理论上的方便，我们假设其可以从各个道入射，于是散射前和散射后的 Moller 波算符 $\Omega_\mp = U(0,\pm\infty)$ 变成了波算符矢量 $\Omega_{\mp}^{\alpha}$，其指标为道的指标，将两个波算符矢量相乘，即可得到多道 $S$ 算符 $S^{\alpha\beta}=\Omega_{-}^{\alpha\dagger}\Omega_{+}^{\beta}$ 。进而我们可以得到多道 $T$ 算符，它依然是个矩阵。利用微扰展开，可以得到多道的 Born 近似

$$
\begin{aligned}
t(\psi^{\prime\beta}\leftarrow\psi^{\alpha}) & \simeq\langle\psi^{\prime\beta}|V^{\alpha}|\psi^{\alpha}\rangle\\
t(\psi^{\prime\beta}\leftarrow\psi^{\alpha}) & \simeq\langle\psi^{\prime\beta}|V^{\beta}|\psi^{\alpha}\rangle
\end{aligned}
$$

这两者在壳时相等。进一步的，也可以得到高阶 Born 近似和扭曲波 Born 近似 (DWBA)。

我们还可以得到多道的 LS 方程：

$$
|\psi^{\alpha}\pm\rangle=|\psi^{\alpha}\rangle+\mathcal{G}^{\alpha}(E^{\pm})V^{\alpha}|\psi^{\alpha}\pm\rangle
$$

这里 $\mathcal{G}^{\alpha}(z)=1/(z-H_{0}^{\alpha})$，其中 $H_{0}^{\alpha}$ 为渐进哈密顿量。此外 $V^{\alpha}$ 为忽略掉的相互作用，两者满足 $H=H_{0}^{\alpha}+V^{\alpha}$。

## 耦合道方程

考虑波函数：

$$
|\Psi\rangle=\sum_{\alpha}\chi^{\alpha}|\psi^{\alpha}\rangle
$$

于是薛定谔方程为：

$$
\sum_{\alpha}\chi^{\alpha}(H_{0}^{\alpha}-E+V^{\alpha})|\psi^{\alpha}\rangle=0
$$

左乘 $\langle\psi^{\beta}|$ 得（假设了正交性）：

$$
\left[(E-E_{0}^{\beta})+\langle\psi^{\beta}|V^{\beta}|\psi^{\beta}\rangle\right]\chi^{\beta}=\sum_{\alpha\neq\beta}\chi^{\alpha}\langle\psi^{\beta}|V^{\alpha}|\psi^{\alpha}\rangle
$$

可以看到，不同道的波函数耦合在了一起。

[^1]: 这一做法被雅克比坐标支持。
