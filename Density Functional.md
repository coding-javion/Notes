## 记号

考虑在有外势的多电子体系，哈密顿量写为：

$$
\begin{align*}
H=\frac{1}{2}\int\nabla\psi^{\dagger}(\boldsymbol{r})\nabla\psi(\boldsymbol{r})\,\mathrm{d}\boldsymbol{r}+\int v(\boldsymbol{r})\psi^{\dagger}(\boldsymbol{r})\psi(\boldsymbol{r})\,\mathrm{d}\boldsymbol{r}+\frac{1}{2}\int\frac{1}{|\boldsymbol{r}-\boldsymbol{r}^{\prime}|}\psi^{\dagger}(\boldsymbol{r})\psi^{\dagger}(\boldsymbol{r}^{\prime})\psi(\boldsymbol{r}^{\prime})\psi(\boldsymbol{r})\,\mathrm{d}\boldsymbol{r}\mathrm{d}\boldsymbol{r}^{\prime}
\end{align*}
$$

用普通的坐标表象写出来即：

$$
\begin{align*}
H=-\frac{1}{2}\sum_{i}\nabla_{i}^{2}+\sum_{i}v(\boldsymbol{r}_{i})+\frac{1}{2}\sum_{ij}\frac{1}{\left|\boldsymbol{r}_{i}-\boldsymbol{r}_{j}\right|}
\end{align*}
$$

对于一个有着$N$个粒子的多体系统来说，基态的粒子数密度$n(\boldsymbol{r})$定义为：

$$
\begin{align*}
n(\boldsymbol{r})=\rho(\boldsymbol{r},\boldsymbol{r}^\prime)|_{\boldsymbol{r}^\prime=\boldsymbol{r}}=\langle \Psi |N\int\psi^{\dagger}(\boldsymbol{r},\boldsymbol{r}_{2},\dots,\boldsymbol{r}_{N})\psi(\boldsymbol{r},\boldsymbol{r}_{2},\dots,\boldsymbol{r}_{N})\,\mathrm{d}\boldsymbol{r}_{2}\dots\mathrm{d}\boldsymbol{r}_{N}|\Psi \rangle
\end{align*}
$$

其中用$\Psi$表示基态。

## Hohenberg-Kohn 定理

### 定理 1

假如有两个哈密顿量 $H_{1}$ 和 $H_{2}$，它们的外势分别为 $v_{1}$ 和 $v_{2}$，如果基态粒子数密度 $n_{1}=n_{2}=n$，那么 $v_{1}-v_{2}=\text{constant}$。即：

外势$v(\boldsymbol{r})$和基态粒子数密度$n_0(\boldsymbol{r})$一一对应。

**证明**

设$\Psi_{1}$和$\Psi_{2}$是它们的基态（可能有简并）。考虑$H_{1}$的基态能量，有：

$$
\begin{align*}
E_{1}	&=\langle\Psi_{1}|H_{1}|\Psi_{1}\rangle \\ &\leq\langle\Psi_{2}|H_{1}|\Psi_{2}\rangle =E_{2}-\int n(\boldsymbol{r})\left(v_{2}(\boldsymbol{r})-v_{1}(\boldsymbol{r})\right)\,\mathrm{d}\boldsymbol{r}
\end{align*}
$$

同理，考虑$H_{2}$的基态能量有：

$$
\begin{align*}
E_{2}\leq E_{1}+\int n(\boldsymbol{r})\left(v_{2}(\boldsymbol{r})-v_{1}(\boldsymbol{r})\right)\,\mathrm{d}\boldsymbol{r}
\end{align*}
$$

由此我们得到：

$$
\begin{align*}
E_{2}-E_{1}=\int n(\boldsymbol{r})\left(v_{2}(\boldsymbol{r})-v_{1}(\boldsymbol{r})\right)\,\mathrm{d}\boldsymbol{r}
\end{align*}
$$

进而得到$\Psi_{1}$也是$H_{2}$的基态。于是有：

$$
\begin{align*}
(E_{2}-E_{1})|\Psi_{1}\rangle=\int\mathrm{d}\boldsymbol{r}\left(v_{2}(\boldsymbol{r})-v_{1}(\boldsymbol{r})\right)\psi^{\dagger}(\boldsymbol{r})\psi(\boldsymbol{r})|\Psi_{1}\rangle
\end{align*}
$$

在坐标表象下写出来即：

$$
\begin{align*}
\left(E_{2}-E_{1}-\sum_{i=1}^{N}(v_{2}-v_{1})(\boldsymbol{r}_{i})\right)\Psi_{1}=0
\end{align*}
$$

可得（这里假设了 $v(\boldsymbol{r})$ 具有唯一延拓的性质[^1]，一般情况下是满足的）：

$$
\begin{align*}
E_{2}-E_{1}-\sum_{i=1}^{N}(v_{2}-v_{1})(\boldsymbol{r}_{i})=0
\end{align*}
$$

由此得：

$$
\begin{align*}
v_{2}-v_{1}=\frac{E_{2}-E_{1}}{N}
\end{align*}
$$

确定了势$v(\boldsymbol{r})$我们就确定了哈密顿量，进而得到一切物理量原则上都可以从基态粒子数密度得出。因此都可以写成关于粒子数密度分布的泛函。

### 定理 2

对于给定外势$v(\boldsymbol{r})$，可以定义一个能量泛函$E[n]$，使得基态粒子数密度$n_0(\boldsymbol{r})$是能量泛函取最小值时的密度分布。

其中定义的能量泛函为：

$$
\begin{align*}
E[n]=\langle\Psi[n]|H|\Psi[n]\rangle
\end{align*}
$$

其中$\Psi[n]$是$n(\boldsymbol{r})$对应哈密顿量的基态。（注意，分子数密度为$n(\boldsymbol{r})$的态可能不是某哈密顿量的基态，我们排除了这些态）

**证明**

对于基态粒子数密度$n(\boldsymbol{r})$，其对应的基态波函数之一记为$\Psi$，对于另一不对应基态的粒子数密度$n^{\prime}(\boldsymbol{r})$，则一定对应某一不是基态的波函数$\Psi^{\prime}$，由变分原理，我们得到：

$$
\begin{align*}
E[n]=\langle\Psi|H|\Psi\rangle<\langle\Psi^{\prime}|H|\Psi^{\prime}\rangle=E[n^{\prime}]
\end{align*}
$$

**疑问**

对能量期待值做变分可以得到激发态，那么能量泛函变分能得到激发态吗？

我认为应该是不行的，因为这里变分的范围被限制了，不是任意的。

## Mermin-Hohenberg-Kohn 定理

[Thermal Properties of the Inhomogeneous Electron Gas (aps.org)](https://journals.aps.org/pr/pdf/10.1103/PhysRev.137.A1441)

上述 HK 定理可以拓展到有限温的情况，我们以巨正则系综为例。记巨正则密度矩阵 $\rho_{0}=\Xi^{-1}\mathrm{e}^{-\beta (H-\mu N)}$，则对任意其它密度矩阵 $\rho$ ，巨势有：

$$
\Omega[\rho]>\Omega [\rho_{0}]
$$

由此，我们可以类比上述定理，得到有限温版本的 HK 定理，由于不需要考虑简并[^2]，甚至还更简单。

### 定理 1

假如有两个哈密顿量 $H_{1}$ 和 $H_{2}$，它们的外势分别为 $v_{1}$ 和 $v_{2}$ ，如果平衡态粒子数密度 $n_{1}=n_{2}=n$，那么 $v_{1}-v_{2}=\text{constant}$。即：

外势 $v(\boldsymbol{r})$ 和基态粒子数密度 $n_0(\boldsymbol{r})$ 一一对应。

**证明**

设 $\rho_{1}$ 和 $\rho_{2}$  是它们的巨正则密度矩阵。考虑 $H_{1}$ 对应的平衡态 巨势 $\Omega _{1}$，有：

$$
\begin{align*}
\Omega _{1}=\mathop{\text{Tr}}[\rho_{1}(H_{1}-\mu N+\frac{1}{\beta}\ln\rho_{1})] & \leq \mathop{\text{Tr}}[\rho_{2}(H_{1}-\mu N+\frac{1}{\beta}\ln\rho_{2})]\\
 & =\Omega _{2}+\mathop{\text{Tr}}[\rho_{2}(v_{1}-v_{2})]\\
 & =\Omega _{2}+\int n(\boldsymbol{r})(v_{1}(\boldsymbol{r})-v_{2}(\boldsymbol{r}))\,\mathrm{d}\boldsymbol{r}
\end{align*}
$$

同理，考虑 $H_{2}$ 对应的平衡态 巨势有：

$$
\Omega _{2}\leq \Omega _{1}+\int n(\boldsymbol{r})(v_{2}(\boldsymbol{r})-v_{1}(\boldsymbol{r}))\,\mathrm{d}\boldsymbol{r}
$$

由此我们得到：

$$
\Omega _{2}-\Omega _{1}=\int n(\boldsymbol{r})(v_{2}(\boldsymbol{r})-v_{1}(\boldsymbol{r}))\,\mathrm{d}\boldsymbol{r}
$$

于是有：

$$
\begin{align*}
\Omega _{2}-\Omega _{1} & =\int\mathop{\text{Tr}}[\rho_{1}\psi^{\dagger}(\boldsymbol{r})\psi(\boldsymbol{r})](v_{2}(\boldsymbol{r})-v_{1}(\boldsymbol{r}))\,\mathrm{d}\boldsymbol{r}\\
 & =\int\mathrm{d}\boldsymbol{r}\int\mathrm{d}\boldsymbol{r}_{1}\dots\mathrm{d}\boldsymbol{r}_{N}\langle\boldsymbol{r}_{1}\dots\boldsymbol{r}_{N}|\psi^{\dagger}(\boldsymbol{r})\psi(\boldsymbol{r})\rho_{1}|\boldsymbol{r}_{1}\dots\boldsymbol{r}_{N}\rangle(v_{2}(\boldsymbol{r})-v_{1}(\boldsymbol{r}))\\
 & =\int\mathrm{d}\boldsymbol{r}\int\mathrm{d}\boldsymbol{r}_{1}\dots\mathrm{d}\boldsymbol{r}_{N}\sum_{k}\delta(\boldsymbol{r}-\boldsymbol{r}_{k})\langle\boldsymbol{r}_{1}\dots\boldsymbol{r}_{N}|\rho_{1}|\boldsymbol{r}_{1}\dots\boldsymbol{r}_{N}\rangle(v_{2}(\boldsymbol{r})-v_{1}(\boldsymbol{r}))\\
 & =\sum_{k}\int\mathrm{d}\boldsymbol{r}_{1}\dots\mathrm{d}\boldsymbol{r}_{N}\langle\boldsymbol{r}_{1}\dots\boldsymbol{r}_{N}|\rho_{1}|\boldsymbol{r}_{1}\dots\boldsymbol{r}_{N}\rangle(v_{2}(\boldsymbol{r}_{k})-v_{1}(\boldsymbol{r}_{k}))\\
 & =\sum_{k}v_{2}(\boldsymbol{r}_{k})-v_{1}(\boldsymbol{r}_{k})
\end{align*}
$$

由此得：

$$
\begin{align*}
v_{2}-v_{1}=\frac{\Omega _{2}-\Omega _{1}}{N}
\end{align*}
$$

确定了势 $v(\boldsymbol{r})$ 我们就确定了哈密顿量，进而得到一切物理量原则上都可以从基态粒子数密度得出。因此都可以写成关于粒子数密度分布的泛函。

### 定理 2

对于给定外势 $v(\boldsymbol{r})$，可以定义一个 巨势泛函 $\Omega [n]$，使得平衡态粒子数密度 $n_0(\boldsymbol{r})$ 是 巨势泛函取最小值时的密度分布。

其中定义的 巨势泛函为：

$$
\Omega [n]=\mathop{\text{Tr}}(\rho[n](H-\mu N+\frac{1}{\beta}\ln\rho[n]))
$$

其中 $\rho[n]$ 是 $n(\boldsymbol{r})$ 对应的哈密顿量的巨正则密度矩阵。（注意，分子数密度为 $n(\boldsymbol{r})$ 的密度矩阵可能不是某哈密顿量的巨正则密度矩阵，我们排除了这些密度矩阵）

**证明**

对于基态粒子数密度 $n(\boldsymbol{r})$，其对应的巨正则密度矩阵记为 $\rho[n]$，对于另一不对应平衡态的密度 $n^{\prime}(\boldsymbol{r})$，则一定对应某一不是巨正则密度矩阵 $\rho^{\prime}[n^{\prime}]$，由 巨势极小原理，我们得到：

$$
\Omega [n]=\mathop{\text{Tr}}(\rho[n](H-\mu N+\frac{1}{\beta}\ln\rho[n]))<\mathop{\text{Tr}}(\rho^{\prime}[n^{\prime}](H-\mu N+\frac{1}{\beta}\ln\rho^{\prime}[n^{\prime}]))=\Omega [n^{\prime}]
$$

## Kohn-Sham 方程

对任何一个有相互作用的 $N$ 粒子体系，其基态粒子密度为 $n(\boldsymbol{r})$，Kohn 和 Sham 假设永远存在一个虚构的无相互作用体系与之有着相同的基态粒子数密度。这是因为我们可以调节外场。

基于这一假设，我们可以将有相互作用系统的能量表示为：

$$
E[n]=T_{\text{S}}[n]+\int\mathrm{d}\boldsymbol{r}v_{\text{ext}}(\boldsymbol{r})n(\boldsymbol{r})+E_{\text{H}}[n]+E_{\text{XC}}[n]
$$

这里 $T_{\text{S}}[n]$ 是无相互作用的动能：

$$
T_{\text{S}}[n]=\langle\Psi_{\text{S}}[n]|\hat{T}|\Psi_{\text{S}}[n]\rangle
$$

这里 $\Psi_{\text{S}}$ 表示无相互作用系统的波函数。需要指出的是，$T_{\text{S}}[n]$ 并不等于真正的动能。

$E_{\text{H}}[n]$ 是粒子数密度 $n$ 对应的 Hartree 能：

$$
E_{\text{H}}=\frac{1}{2}\int\mathrm{d}\boldsymbol{r}\,\mathrm{d}\boldsymbol{r}^{\prime}\,\frac{e^{2}}{4\mathrm{\pi}\varepsilon_{0}\left|\boldsymbol{r}-\boldsymbol{r}^{\prime}\right|}n(\boldsymbol{r})n(\boldsymbol{r}^{\prime})
$$

它也并不是真正的粒子间相互作用能。

$E_{\text{XC}}$ 是交换关联能，实际上这是一项所有无法简单写出的能量的综合。它包含了真正的动能和相互作用能与我们写出的 $T_{\text{S}}$ 和 $E_{\text{H}}$ 的差。

对上述相互作用系统的能量做变分，得：

$$
\left[-\frac{\hbar^{2}\nabla^{2}}{2m}+v_{\text{ext}}(\boldsymbol{r})+v_{\text{H}}(\boldsymbol{r})+v_{\text{XC}}(\boldsymbol{r})\right]\varphi_{i}(\boldsymbol{r})=\varepsilon_{i}\varphi_{i}(\boldsymbol{r})
$$

此即 Kohn-Sham 方程，其中：

$$
\begin{align*}
v_{\text{H}} & (\boldsymbol{r})=\frac{e^{2}}{4\mathrm{\pi}\varepsilon_{0}}\int\mathrm{d}\boldsymbol{r}^{\prime}\,\frac{n(\boldsymbol{r}^{\prime})}{\left|\boldsymbol{r}^{\prime}-\boldsymbol{r}\right|}\\
v_{\text{XC}} & (\boldsymbol{r})=\frac{\delta E_{\text{XC}}}{\delta n(\boldsymbol{r})}
\end{align*}
$$

## Kohn-Sham-Hartree-Fock

把上述的交换关联能拆成交换能 $E_{\text{F}}[n]$ 和关联能 $E_{\text{C}}[n]$，其中交换能即 Fock 项。得到所谓的 Kohn-Sham-Hartree-Fock。

[^1]: 一个非常普遍的性质。
[^2]: 为什么不需要考虑简并？但至少 Mermin 原始论文如此。