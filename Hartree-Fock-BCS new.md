   ### BCS 波函数

所谓的 BCS 态为：

$$
|\text{BCS}\rangle=\prod_{i>0}(u_{i}+v_{i}a_{i}^{\dagger}a_{\bar{i}}^{\dagger})|\rangle
$$

这里用 $\bar{i}$ 表示 $i$ 的时间反演态，求和的时候用 $>0$ 表示只对态和反演态之间的一个求和。 $i$ 和 $\bar{i}$ 这两个能级只能同时被占据，占据的概率是 $\left|v_{i}\right|^{2}$，未被占据的概率是 $\left|u_{i}\right|^{2}$，因此有 $\left|u_{i}\right|^{2}+\left|v_{i}\right|^{2}=1$。我们同时假设 $u_i$ 和 $v_{i}$ 都为正实数，这在不含时的情况下已经足够了[^1]。另外，为了方便，我们时常假设 $u_{\bar{i}}=u_{i}, v_{\bar{i}}=-v_{i}$。

接下来我们研究一下 BCS 的态的性质。首先验证归一性：

$$
\begin{align*}
\langle\text{BCS}|\text{BCS}\rangle & =\langle|\prod_{i>0}(u_{i}+v_{i}a_{\bar{i}}a_{i})\prod_{j>0}(u_{j}+v_{j}a_{j}^{\dagger}a_{\bar{j}}^{\dagger})|\rangle\\
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

BCS 态之所以写成这样，一方面它很直观的体现出了对的特点，另一方面还有个好处，如果定义 BCS 变换：

$$
\alpha_{k}^{\dagger}	=u_{k}a_{k}^{\dagger}-v_{k}a_{\bar{k}}
$$
这里湮灭算符的变换关系可以取厄米共轭得出。由此我们可以发现：

$$
|\text{BCS}\rangle\propto\prod_{k}\alpha_{k}|\rangle
$$
这意味着 BCS 波函数是一个“直积态”，如果我们称 $\alpha^{\dagger},\alpha$ 定义的粒子为准粒子，那么它就是准粒子直积态。

### BCS 方程

多体哈密顿量为：

$$
\hat{H}=\sum_{ij}t_{ij}a_{i}^{\dagger}a_{j}+\frac{1}{4}\sum_{ijkl}\bar{v}_{ijkl}a_{i}^{\dagger}a_{j}^{\dagger}a_{l}a_{k}
$$

根据变分原理，我们可以得到 BCS 波函数中的 $u_{k}$ 和 $v_{k}$。为了让粒子数守恒，我们在变分的时候需要施加限制 $\langle \hat{N}\rangle=N$。因此变分为：

$$
\delta\langle\text{BCS}|\hat{H}-\mu (\hat{N}-N)|\text{BCS}\rangle=0
$$

$\mu$ 是拉格朗日乘子，也是化学势。由于 $\mu N$ 是常数，在变分问题中我们可以直接将其省略。我们首先计算 $\langle\text{BCS}|\hat{H}-\mu \hat{N}|\text{BCS}\rangle$，然而 $\langle\text{BCS}|a_{i}^{\dagger}a_{j}^{\dagger}a_{l}a_{k}|\text{BCS}\rangle$ 的计算比较复杂，一个简明的推导是利用 Wick 定理。唯一需要注意的是，这里的缩并不再是简单的 $\delta$ 函数，而是：

$$
\begin{align*}
\langle a_{k}^{\dagger}a_{l}\rangle & =v_{k}^{2}\delta_{kl}\\
\langle a_{k}a_{l}^{\dagger}\rangle & =u_{k}^{2}\delta_{kl}\\
\langle a_{k}a_{l}\rangle & =-u_{k}v_{k}\delta_{k\bar{l}}\\
\langle a_{k}^{\dagger}a_{l}^{\dagger}\rangle & =u_{k}v_{k}\delta_{k\bar{l}}
\end{align*}
$$

这里我们利用 $\langle a_{k}^{\dagger}a_{l}\rangle=\langle\text{BCS}|a_{k}^{\dagger}a_{l}|\text{BCS}\rangle$ 表示算符 $a_{k}^{\dagger}$ 和 $a_{l}$  的缩并，具体计算很简单，只需要将 $a, a^{\dagger}$ 替换成。由此，无需利用 Wick 定理我们就可以得到单体部分为：

$$
\sum_{k_{1}k_{2}}(t_{k_{1}k_{2}}-\lambda\delta_{k_{1}k_{2}})\langle a_{k_{1}}^{\dagger}a_{k_{2}}\rangle=\sum_{k}(t_{kk}-\lambda) v_{k}^{2}
$$

而两体部分为 ：

$$
\begin{align*}
& \frac{1}{4}\sum_{k_{1}k_{2}k_{3}k_{4}}\bar{v}_{k_{1}k_{2}k_{3}k_{4}}\langle a_{k_{1}}^{\dagger}a_{k_{2}}^{\dagger}a_{k_{4}}a_{k_{3}}\rangle \\ =& \frac{1}{4}\sum_{k_{1}k_{2}k_{3}k_{4}}\bar{v}_{k_{1}k_{2}k_{3}k_{4}}\left(\langle a_{k_{1}}^{\dagger}a_{k_{3}}\rangle\langle a_{k_{2}}^{\dagger}a_{k_{4}}\rangle-\langle a_{k_{1}}^{\dagger}a_{k_{4}}\rangle\langle a_{k_{2}}^{\dagger}a_{k_{3}}\rangle+\langle a_{k_{1}}^{\dagger}a_{k_{2}}^{\dagger}\rangle\langle a_{k_{4}}a_{k_{3}}\rangle\right)\\
 =& \frac{1}{4}\sum_{k_{1}k_{2}k_{3}k_{4}}\bar{v}_{k_{1}k_{2}k_{3}k_{4}}\left[v_{k_{1}}^{2}v_{k_{2}}^{2}(\delta_{k_{1}k_{3}}\delta_{k_{2}k_{4}}-\delta_{k_{1}k_{4}}\delta_{k_{2}k_{3}})+u_{k_{1}}v_{k_{1}}u_{k_{3}}v_{k_{3}}\delta_{k_{1}\bar{k}_{2}}\delta_{k_{3}\bar{k}_{4}}\right]\\
 =&\frac{1}{2}\sum_{kk^{\prime}}\bar{v}_{kk^{\prime}kk^{\prime}}v_{k}^{2}v_{k^{\prime}}^{2}+\frac{1}{4}\sum_{kk^{\prime}}\bar{v}_{k\bar{k}k^{\prime}\bar{k^{\prime}}}u_{k}v_{k}u_{k^{\prime}}v_{k^{\prime}}\\
 =& \frac{1}{2}\sum_{kk^{\prime}}\bar{v}_{kk^{\prime}kk^{\prime}}v_{k}^{2}v_{k^{\prime}}^{2}+\sum_{kk^{\prime}>0}\bar{v}_{k\bar{k}k^{\prime}\bar{k^{\prime}}}u_{k}v_{k}u_{k^{\prime}}v_{k^{\prime}}
\end{align*}
$$

这样我们就得到了：

$$
\langle\text{BCS}|H-\mu N|\text{BCS}\rangle=\sum_{i}\Bigl[(t_{ii}-\mu)v_{i}^{2}+\frac{1}{2}\sum_{j}\bar{v}_{ijij}v_{i}^{2}v_{j}^{2}\Bigr]+\sum_{ij>0}\bar{v}_{i\bar{i}j\bar{j}}u_{i}v_{i}u_{j}v_{j}
$$

由于 $u_{i}^{2}+v_{i}^{2}=1$，根据链式法则，我们有：

$$\frac{\partial}{\partial v_{i}}\rightarrow\frac{\partial}{\partial v_{i}}+\frac{\partial u_{i}}{\partial v_{i}}\frac{\partial}{\partial u_{i}}=\frac{\partial}{\partial v_{i}}-\frac{v_{i}}{u_{i}}\frac{\partial}{\partial u_{i}}$$

变分方程即为：

$$
\left(\frac{\partial}{\partial v_{i}}-\frac{v_{i}}{u_{i}}\frac{\partial}{\partial u_{i}}\right)\langle\text{BCS}|H-\mu N|\text{BCS}\rangle=0
$$

只需把上面得到的结果代入，即可得到变分方程。需要注意的是，变分时我们只对 $i>0$ 的 $v_{i}, u_{i}$ 做变分，因此首先需要把上面的式子写成只有 $v_{i}, u_{i}(i>0)$ 的式子：

$$
\sum_{i>0}\Bigl[(t_{ii}-\mu)v_{i}^{2}+(t_{\bar{i}\bar{i}}-\mu)v_{i}^{2}+\frac{1}{2}\sum_{j>0}(\bar{v}_{ijij}+\bar{v}_{i\bar{j}i\bar{j}}+\bar{v}_{\bar{i}j\bar{i}j}+\bar{v}_{\bar{i}\bar{j}\bar{i}\bar{j}})v_{i}^{2}v_{j}^{2}\Bigr]+\sum_{ij>0}\bar{v}_{i\bar{i}j\bar{j}}u_{i}v_{i}u_{j}v_{j}
$$

接下来正常变分即可得到 BCS 方程：

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
考虑利用坐标空间波函数得到 $\Delta_{i}$，我们需要利用 [[Pairing Energy]] 中的矩阵元并计算：

$$
\begin{align*}
-\sum_{j>0}\langle i\bar{i}|\bar{v}_{\text{pair}}|j\bar{j}\rangle u_{j}v_{j} & =\sum_{t}v_{t}\int\mathrm{d}\boldsymbol{r}\left(1-\frac{\rho(\boldsymbol{r})}{\rho_{0}}\right)\left(\sum_{s}\left|\psi_{i}(\boldsymbol{r},s,t)\right|^{2}\right)\left(\sum_{j>0,s^{\prime}}\left|\psi_{j}(\boldsymbol{r},s^{\prime},t)\right|^{2}u_{j}v_{j}\right)\\
 & \equiv \sum_{t}\frac{1}{2}v_{t}\int\mathrm{d}\boldsymbol{r}\left(1-\frac{\rho(\boldsymbol{r})}{\rho_{0}}\right)\left|\psi_{i}(\boldsymbol{r},t)\right|^{2}\xi_{t}(\boldsymbol{r})
\end{align*}
$$

[^1]: 然而我需要含时的情况，哈哈。
[^2]: 可以做粒子数投影。

