## 变分法推导

### BCS 波函数

所谓的 BCS 态为：

$$
|\text{BCS}\rangle=\prod_{i>0}(u_{i}+v_{i}a_{i}^{\dagger}a_{\bar{i}}^{\dagger})|\rangle
$$

这里用 $\bar{i}$ 表示 $i$ 的时间反演态，求和的时候用 $>0$ 表示只对态和反演态之间的一个求和。 $i$ 和 $\bar{i}$ 这两个能级只能同时被占据，占据的概率是 $\left|v_{i}\right|^{2}$，未被占据的概率是 $\left|u_{i}\right|^{2}$，因此有 $\left|u_{i}\right|^{2}+\left|v_{i}\right|^{2}=1$。我们同时假设 $u_i$ 和 $v_{i}$ 都为正实数，这在不含时的情况下已经足够了[^1]。另外，为了方便，我们时常假设 $u_{\bar{i}}=u_{i}, v_{\bar{i}}=-v_{i}$。

接下来我们研究一下 BCS 的态的性质。首先验证归一性：

$$
\begin{align*}
\langle\text{BCS}|\text{BCS}\rangle & =\langle|\prod_{i>0}(u_{i}+v_{i}a_{\bar{i}}a_{i})\prod_{i^{\prime}>0}(u_{i^{\prime}}+v_{i^{\prime}}a_{i^{\prime}}^{\dagger}a_{\bar{j}}^{\dagger})|\rangle\\
 & =\prod_{i>0}(u_{i}^{2}+v_{i}^{2})=1
\end{align*}
$$

可以看出，BCS 态的粒子数并不守恒，可以将粒子数算符作用到上面验证这一点：

$$
\sum_{i>0}a_{i}^{\dagger}a_{i}+a_{\bar{i}}^{\dagger}a_{\bar{i}}|\text{BCS}\rangle=\sum_{i>0}2v_{i}a_{i}^{\dagger}a_{\bar{i}}^{\dagger}\prod_{j\neq i>0}(u_{j}+v_{j}a_{j}^{\dagger}a_{\bar{j}}^{\dagger})|\rangle
$$

显然 BCS 态并不是粒子数算符的本征态。不过我们还是可以计算粒子数的期望值：

$$
\langle N\rangle=\langle\text{BCS}|\sum_{i>0}a_{i}^{\dagger}a_{i}+a_{\bar{i}}^{\dagger}a_{\bar{i}}|\text{BCS}\rangle=\sum_{i>0}2v_{i}^{2}
$$

粒子数的不确定度为 $\Delta N^{2}=\langle N^{2}\rangle-\langle N\rangle^{2}$，为了计算粒子数的不确定度，我们首先需要计算 $\langle N^{2}\rangle$：

$$
\begin{align*}
\langle N^{2}\rangle & =\langle\text{BCS}|\bigl(\sum_{i>0}a_{i}^{\dagger}a_{i}+a_{\bar{i}}^{\dagger}a_{\bar{i}}\bigr)^{2}|\text{BCS}\rangle\\
 & =\langle\text{BCS}|\sum_{ij>0}\bigl(a_{i}^{\dagger}a_{i}+a_{\bar{i}}^{\dagger}a_{\bar{i}}\bigr)2v_{j}a_{j}^{\dagger}a_{\bar{j}}^{\dagger}\prod_{k\neq j>0}(u_{k}+v_{k}a_{k}^{\dagger}a_{\bar{k}}^{\dagger})|\rangle
\end{align*}
$$

上述求和号内的式子在 $i=j$ 时为：

$$
4v_{j}a_{j}^{\dagger}a_{\bar{j}}^{\dagger}\prod_{k\neq j>0}(u_{k}+v_{k}a_{k}^{\dagger}a_{\bar{k}}^{\dagger})
$$

而在 $i\neq j$ 时为：

$$
(2v_{i}a_{i}^{\dagger}a_{\bar{i}}^{\dagger})(2v_{j}a_{j}^{\dagger}a_{\bar{j}}^{\dagger})\prod_{k\neq i,j>0}(u_{k}+v_{k}a_{k}^{\dagger}a_{\bar{k}}^{\dagger})
$$

因此最终得到：

$$
\langle N^{2}\rangle=4\sum_{i>0}v_{i}^{2}+4\sum_{i\neq j>0}v_{i}^{2}v_{j}^{2}
$$

由此可以得到：

$$
\begin{align*}
\Delta N^{2} & =4\sum_{i>0}v_{i}^{2}(1-v_{i}^{2})=4\sum_{i>0}u_{i}^{2}v_{i}^{2}
\end{align*}
$$

严格来说，这样的不确定度当然是不存在的，只有当 $\Delta N\ll N$ 时，我们才可以认为这种不确定度是不重要的，这一情况在凝聚态的研究中是满足的，而在核物理中往往并不满足，因此需要额外做处理[^2]。

### BCS 方程

多体哈密顿量为：

$$
\hat{H}=\sum_{ij}t_{ij}a_{i}^{\dagger}a_{j}+\frac{1}{4}\sum_{ijkl}\bar{v}_{ijkl}a_{i}^{\dagger}a_{j}^{\dagger}a_{l}a_{k}
$$

根据变分原理，我们可以得到 BCS 波函数中的 $u_{k}$ 和 $v_{k}$。为了让粒子数守恒，我们在变分的时候需要施加限制 $\langle \hat{N}\rangle=N$。因此变分为：

$$
\delta\langle\text{BCS}|\hat{H}-\mu (\hat{N}-N)|\text{BCS}\rangle=0
$$

$\mu$ 是拉格朗日乘子，也是化学势。由于 $\mu N$ 是常数，在变分问题中我们可以直接将其省略。我们首先计算 $\langle\text{BCS}|\hat{H}-\mu \hat{N}|\text{BCS}\rangle$，然而 $\langle\text{BCS}|\bar{v}_{ijkl}a_{i}^{\dagger}a_{j}^{\dagger}a_{l}a_{k}|\text{BCS}\rangle$ 的计算比较复杂。通过分析可知，不为零的项只有：

$$
\begin{align*}
\bar{v}_{i\bar{i}j\bar{j}}a_{i}^{\dagger}a_{\bar{i}}^{\dagger}a_{\bar{j}}a_{j}\\
\bar{v}_{ijij}a_{i}^{\dagger}a_{j}^{\dagger}a_{j}a_{i}\\
\bar{v}_{ijji}a_{i}^{\dagger}a_{j}^{\dagger}a_{i}a_{j}
\end{align*}
$$

根据反对称性质，后两项相同。于是相当于计算：

$$
\sum_{ij}\langle\text{BCS}|\bar{v}_{i\bar{i}j\bar{j}}a_{i}^{\dagger}a_{\bar{i}}^{\dagger}a_{\bar{j}}a_{j}+2\bar{v}_{ijij}a_{i}^{\dagger}a_{j}^{\dagger}a_{j}a_{i}|\text{BCS}\rangle
$$

然而这实际上是不正确的，因为这里存在 double counting。令 $j=\bar{i}$，可以看出，第一项和第二项，第三项得到了相同的结果。因此我们实际上需要再减去 $\sum_{i}\langle\text{BCS}|2\bar{v}_{i\bar{i}\bar{i}i}a_{i}^{\dagger}a_{\bar{i}}^{\dagger}a_{i}a_{\bar{i}}|\text{BCS}\rangle$。因此我们实际上应该计算：

$$
\sum_{ij}\langle\text{BCS}|\bar{v}_{i\bar{i}j\bar{j}}a_{i}^{\dagger}a_{\bar{i}}^{\dagger}a_{\bar{j}}a_{j}|\text{BCS}\rangle+\sum_{ij}\langle\text{BCS}|2\bar{v}_{ijij}a_{i}^{\dagger}a_{j}^{\dagger}a_{j}a_{i}|\text{BCS}\rangle - \sum_{i}\langle\text{BCS}|2\bar{v}_{i\bar{i}\bar{i}i}a_{i}^{\dagger}a_{\bar{i}}^{\dagger}a_{i}a_{\bar{i}}|\text{BCS}\rangle
$$

计算第一项得：

$$
\begin{align*}
\sum_{ij}\langle\text{BCS}|\bar{v}_{i\bar{i}j\bar{j}}a_{i}^{\dagger}a_{\bar{i}}^{\dagger}a_{\bar{j}}a_{j}|\text{BCS}\rangle & =\sum_{ij>0}\langle\text{BCS}|4\bar{v}_{i\bar{i}j\bar{j}}a_{i}^{\dagger}a_{\bar{i}}^{\dagger}a_{\bar{j}}a_{j}|\text{BCS}\rangle\\
 & =\sum_{\begin{subarray}{c}
ij>0\\
j\neq i
\end{subarray}}4\bar{v}_{i\bar{i}j\bar{j}}u_{i}v_{i}u_{j}v_{j}+\sum_{i>0}4\bar{v}_{i\bar{i}i\bar{i}}v_{i}^{2}
\end{align*}
$$

计算第二项得：

$$
\sum_{ij}\langle\text{BCS}|2\bar{v}_{ijij}a_{i}^{\dagger}a_{j}^{\dagger}a_{j}a_{i}|\text{BCS}\rangle=\sum_{j\neq\bar{i}}2\bar{v}_{ijij}v_{i}^{2}v_{j}^{2}+\sum_{i}2\bar{v}_{i\bar{i}i\bar{i}}v_{i}^{2}
$$

这里我们利用了 $v_{\bar{i}}=-v_{i}$ 的假设。

计算第三项得：

$$
\sum_{i}\langle\text{BCS}|2\bar{v}_{i\bar{i}\bar{i}i}a_{i}^{\dagger}a_{\bar{i}}^{\dagger}a_{i}a_{\bar{i}}|\text{BCS}\rangle=\sum_{i}2\bar{v}_{i\bar{i}i\bar{i}}v_{i}^{2}
$$

将它们相加，得到：

$$
\sum_{\begin{subarray}{c}
ij>0\\
j\neq i
\end{subarray}}4\bar{v}_{i\bar{i}j\bar{j}}u_{i}v_{i}u_{j}v_{j}+\sum_{i>0}4\bar{v}_{i\bar{i}i\bar{i}}v_{i}^{2}+\sum_{j\neq\bar{i}}2\bar{v}_{ijij}v_{i}^{2}v_{j}^{2}
$$

利用 $u_{i}^{2}+v_{i}^{2}=1$，我们最终可以得到：

$$
\frac{1}{4}\sum_{ijkl}\langle\text{BCS}|\bar{v}_{ijkl}a_{i}^{\dagger}a_{j}^{\dagger}a_{l}a_{k}|\text{BCS}\rangle=\frac{1}{2}\sum_{ij}\bar{v}_{ijij}v_{i}^{2}v_{j}^{2}+\sum_{ij>0}\bar{v}_{i\bar{i}j\bar{j}}u_{i}v_{i}u_{j}v_{j}
$$

将单体部分也算出来，于是最终得到：

$$
\langle\text{BCS}|H-\mu N|\text{BCS}\rangle=\sum_{i}\Bigl[(t_{ii}-\mu)v_{i}^{2}+\frac{1}{2}\sum_{j}\bar{v}_{ijij}v_{i}^{2}v_{j}^{2}\Bigr]+\sum_{ij>0}\bar{v}_{i\bar{i}j\bar{j}}u_{i}v_{i}u_{j}v_{j}
$$

由于 $u_{i}^{2}+v_{i}^{2}=1$，根据链式法则，在使用 $u_{i}, v_{i}$ 同时作为变量时，我们应当把对单一变量 $v_{i}$ 的偏导替换为：

$$
\frac{\partial}{\partial v_{i}}\rightarrow\frac{\partial}{\partial v_{i}}+\frac{\partial u_{i}}{\partial v_{i}}\frac{\partial}{\partial u_{i}}=\frac{\partial}{\partial v_{i}}-\frac{v_{i}}{u_{i}}\frac{\partial}{\partial u_{i}}
$$

变分方程即为：

$$
\left(\frac{\partial}{\partial v_{i}}-\frac{v_{i}}{u_{i}}\frac{\partial}{\partial u_{i}}\right)\langle\text{BCS}|H-\mu N|\text{BCS}\rangle=0
$$

只需把上面得到的结果代入，即可得到变分方程。需要注意的是，变分时我们只对 $i>0$ 的 $v_{i}, u_{i}$ 做变分，因此首先需要把上面的式子写成只有 $v_{i}, u_{i}(i>0)$ 的式子：

$$
\sum_{i>0}\Bigl[(t_{ii}-\mu)v_{i}^{2}+(t_{\bar{i}\bar{i}}-\mu)v_{i}^{2}+\frac{1}{2}\sum_{j>0}(\bar{v}_{ijij}+\bar{v}_{i\bar{j}i\bar{j}}+\bar{v}_{\bar{i}j\bar{i}j}+\bar{v}_{\bar{i}\bar{j}\bar{i}\bar{j}})v_{i}^{2}v_{j}^{2}\Bigr]+\sum_{ij>0}\bar{v}_{i\bar{i}j\bar{j}}u_{i}v_{i}u_{j}v_{j}
$$

接下来正常变分即可得到BCS方程：

$$
2\tilde{\varepsilon}_{i}u_{i}v_{i}+\Delta_{i}(v_{i}^{2}-u_{i}^{2})=0
$$

其中：

$$
\tilde{\varepsilon}_{i}=\frac{1}{2}\left(t_{ii}+t_{\bar{i}\bar{i}}+\sum_{j}(\bar{v}_{ijij}+\bar{v}_{\bar{i}j\bar{i}j})v_{j}^{2}\right)-\mu
$$

能隙为：

$$
\Delta_{i}=-\sum_{j>0}\bar{v}_{i\bar{i}j\bar{j}}u_{j}v_{j}
$$

结合 $u_{i}^{2}+v_{i}^{2}=1$，我们可以得到一组形式解：

$$
\begin{align*}
v_{i}^{2} & =\frac{1}{2}\left(1-\frac{\tilde{\varepsilon}_{i}}{\sqrt{\tilde{\varepsilon}_{i}^{2}+\Delta_{i}^{2}}}\right)\\
u_{i}^{2} & =\frac{1}{2}\left(1+\frac{\tilde{\varepsilon}_{i}}{\sqrt{\tilde{\varepsilon}_{i}^{2}+\Delta_{i}^{2}}}\right)
\end{align*}
$$

当没有相互作用时，$\Delta_{k}=0$，我们期待 $v_{k}$ 退化为阶梯函数，事实也的确如此。

上面的方程和粒子数的约束 $2\sum_{i>0}v_{i}^{2}=N$ 一起构成了一个非线性方程组，确定了参数 $u_{i}, v_{i}$ 的值。通常来讲方程无法直接求解，只能通过迭代计算。

将 $u_{i}$ 和 $v_{i}$ 的定义式代入到能隙中去，我们还可以得到所谓的 gap equation：

$$
\Delta_{i}=-\frac{1}{2}\sum_{j>0}\bar{v}_{i\bar{i}j\bar{j}}\frac{\Delta_{j}}{\sqrt{\tilde{\varepsilon}_{j}^{2}+\Delta_{j}^{2}}}
$$

[^1]: 然而我需要含时的情况，哈哈。
[^2]: 可以做粒子数投影。

