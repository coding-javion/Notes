---
related:
  - "[[Density Matrix]]"
  - "[[Wick定理]]"
  - "[[Mean Field and Variational Principle]]"
---
> Hartree Fock 方法的本质是，用平均场哈密顿量去近似原哈密顿量。根据[[Mean Field and Variational Principle]]所述，这等价于拿一个试探的直积态去做变分。

## Hartree Fock 能量

用 $|\text{HF}\rangle$ 表示 Hartree Fock 态，$|\rangle$ 表示真空态，有：

$$
|\text{HF}\rangle=\prod_{i}a_{i}^{\dagger}|\rangle  
$$

这意味着 $|\text{HF}\rangle$ 是直积态。我们采用如下符号规则，$i,j,k\dots$代表占据态，$a,b,c\dots$代表未占据态，$p,q,r\dots$代表任意态。用产生湮灭算符写出哈密顿量为：

$$
H=\sum_{pq}t_{pq}a_{p}^{\dagger}a_{q}+\frac{1}{2}\sum_{pqrs}v_{pqrs}a_{p}^{\dagger}a_{q}^{\dagger}a_{s}a_{r}
$$

于是该态的能量可以计算出来：

$$
\begin{align*}
E & =\langle\text{HF}|H|\text{HF}\rangle\\
 & =\sum_{pq}t_{pq}\langle a_{p}^{\dagger}a_{q}\rangle+\frac{1}{2}\sum_{pqrs}v_{pqrs}\langle a_{p}^{\dagger}a_{q}^{\dagger}a_{s}a_{r}\rangle
\end{align*}
$$

这里用 $\langle\hat{O}\rangle$ 表示 $\langle\text{HF}|\hat{O}|\text{HF}\rangle$。根据 Wick 定理：

$$
\langle a_{p}^{\dagger}a_{q}^{\dagger}a_{s}a_{r}\rangle=\langle a_{p}^{\dagger}a_{r}\rangle\langle a_{q}^{\dagger}a_{s}\rangle-\langle a_{p}^{\dagger}a_{s}\rangle\langle a_{q}^{\dagger}a_{r}\rangle
$$

这里 $\langle a_{p}^{\dagger}a_{q}\rangle$ 其实是单粒子密度矩阵，有 $\rho_{qp}=\langle a_{p}^{\dagger}a_{q}\rangle$。因此：

$$
E=\sum_{pq}t_{pq}\rho_{qp}+\frac{1}{2}\sum_{pqrs}\bar{v}_{pqrs}\rho_{rp}\rho_{sq}
$$

这里定义了 $\bar{v}_{pqrs}=v_{pqrs}-v_{pqsr}$ 。

## Hartree Fock 方程

接下来我们考虑对 $|\text{HF}\rangle$ 变分，让能量最小。为此我们不妨先看看能量的表达式，我们发现能量的表达式中与 $|\text{HF}\rangle$ 相关的只有 $\rho$，因此我们可以考虑对 $\rho$ 变分，只要这一变分的过程能保持 $|\text{HF}\rangle$ 态的形式不变，即保持其为直积态。

可以证明，一个态是直积态等价于它对应的密度矩阵满足 $\rho^2=\rho$ ，这意味着 $\rho$ 是投影算符[[#附录]]。因此我们只需要保证变分中保持这一关系即可。对该式做变分，有：

$$
\rho\cdot\delta\rho+\delta\rho\cdot\rho=\delta\rho
$$

右乘 $\rho$ 得 $\rho\cdot\delta\rho\cdot\rho=0$。右乘 $1-\rho$ 得 $(1-\rho)\cdot\delta\rho\cdot (1-\rho)=0$。

假设我们在对哈密顿量做二次量子化的时候选取的单粒子基同 $|\text{HF}\rangle$ 中的单粒子基相同，则此时密度矩阵 $\rho_{qp}=\delta_{qp}(p\in\text{占据态})$，上式就相当于说 $(\delta\rho)_{ij}=0$，$(\delta\rho)_{ab}=0$。因此我们变分只能对 $\rho_{ai}$ 这样的项变分。

$$
\begin{align*}
\delta E & =\frac{\delta E}{\delta\rho_{ai}}\delta\rho_{ai}+\frac{\delta E}{\delta\rho_{ia}}\delta\rho_{ia}\\
 & =\left(t_{ia}+\sum_{pq}\bar{v}_{ipaq}\rho_{qp}\right)\delta\rho_{ai}+\text{c.c.}
\end{align*}
$$

于是上式为零即得到：

$$
\begin{align*}
t_{ia}+\sum_{pq}\bar{v}_{ipaq}\rho_{qp} & =0
\end{align*}
$$

按理来说我们这样就足够了，但我们还可以进一步要求：

$$
t_{pq}+\sum_{rs}\bar{v}_{prqs}\rho_{sr}=\varepsilon_{p}\delta_{pq}
$$

这就是 Hartree-Fock 方程，又称正则 Hartree-Fock 方程。

考虑到密度矩阵$\rho_{sr}=\delta_{sr}(sr\in\text{occ.})$。可以写为：

$$
t_{pq}+\sum_{i}\bar{v}_{piqi}=\varepsilon_{p}\delta_{pq}
$$

在坐标表象下写这个方程，即为：

$$
\begin{align*}
\begin{aligned}-\frac{\hbar^{2}}{2m}\nabla^{2}\psi_{p}(\boldsymbol{x})+\sum_{i}\int\mathrm{d}^{3}\boldsymbol{x}^{\prime}\psi_{i}^{*}(\boldsymbol{x}^{\prime})V(\boldsymbol{x},\boldsymbol{x}^{\prime})\psi_{p}(\boldsymbol{x}^{\prime})\psi_{i}(\boldsymbol{x})\\
-\sum_{i}\int\mathrm{d}^{3}\boldsymbol{x}^{\prime}\psi_{i}^{*}(\boldsymbol{x}^{\prime})V(\boldsymbol{x},\boldsymbol{x}^{\prime})\psi_{i}(\boldsymbol{x}^{\prime})\psi_{p}(\boldsymbol{x}) & =\varepsilon_{p}\psi_{p}(\boldsymbol{x})
\end{aligned}
\end{align*}
$$

显然，方程左侧第二项和第三项代表了平均场的作用。

## 附录

假设$\Psi$是Slater行列式$|\Psi\rangle=\prod_{i}a_{i}^{\dagger}|\rangle$，容易得到$\rho_{ij}=\langle\Psi|a_{j}^{\dagger}a_{i}|\Psi\rangle=\delta_{ij}$，这里$i,j$均为占据态，否则为零。因此，$\rho$是投影到占据态的投影算符。

由$\rho$为投影算符可以得到 $\Psi$ 为 Slater 行列式，证明如下：

一般来讲，$|\Psi\rangle=\sum_{i}C_{i}|\Phi_{i}\rangle$，其中 $|\Phi_{i}\rangle$ 为一系列 Slater 行列式，其粒子数与 $|\Psi\rangle$ 相同，且所有的 $|\Phi_{i}\rangle$ 都共用一组单粒子基，只不过占据态与未占据态的划分不同。此时单粒子密度矩阵写为：

$$
\rho_{pq}=\sum_{ij}C_{i}^{*}C_{j}\langle\Phi_{i}|a_{q}^{\dagger}a_{p}|\Phi_{j}\rangle
$$

这里 $a_{q}^{\dagger}$，$a_{p}$ 也使用同一组单粒子基，且我们可以令这一组单粒子基恰好使 $\rho_{pq}$ 对角化。对角化后，对角元 $\rho_{pp}$ 对于 $N$ 个为 $1$，其余为零。考虑为 $0$ 的部分，有：

$$
\rho_{pp}=\sum_{i}\left|C_{i}\right|^{2}n_{ip}=0
$$

这里对 $i$ 求和实际上是对一系列分布求和。上述求和中每一项都非负，因此必须每项都为零，这意味着所有 $p$ 态为占据的分布对应的系数 $C_{i}$ 均为零。考虑 $p$ 取遍 $\rho_{pp}$ 为零的态，$i$ 对应的分布中这些均不可以占据，这意味着求和中仅仅含有一项，即对于 $\rho_{pp}$ 为 $1$ 的态是占据的，对于 $\rho_{pp}$ 为 $0$ 的态是非占据的。因此 $\Psi$ 即为简单的 Slater 行列式。