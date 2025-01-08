## skyrme力推出skyrme密度泛函

记skyrme相互作用为：

$$
\begin{align*}
V^{(2)}= & t_{0}(1+x_{0}P_{\sigma})\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})\\
 & +\frac{1}{2}t_{1}(\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})k^{2}+k^{\prime2}\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2}))\\
 & +t_{2}\boldsymbol{k}^{\prime}\cdot\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})\boldsymbol{k}+\mathrm{i}W_{0}(\boldsymbol{\sigma}_{1}+\boldsymbol{\sigma}_{2})\cdot(\boldsymbol{k}^{\prime}\times\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})\boldsymbol{k})\\
V^{(3)}= & t_{3}\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})\delta(\boldsymbol{r}_{2}-\boldsymbol{r}_{3})
\end{align*}
$$

 其中$\boldsymbol{k}$和$\boldsymbol{k}^{\prime}$为：

$$
\begin{align*}
\boldsymbol{k} & =\frac{1}{2\mathrm{i}}(\nabla_{1}-\nabla_{2})\\
\boldsymbol{k}^{\prime} & =-\frac{1}{2\mathrm{i}}(\nabla_{1}-\nabla_{2})
\end{align*}
$$

$\boldsymbol{k}^{\prime}$是作用到左侧波函数的。$\boldsymbol{\sigma}$表示Pauli矩阵，$P_{\sigma}$表示自旋交换算符。$t_{0},t_{1},t_{2},t_{3},x_{0},W_{0}$都是参数。

我们想把能量密度泛函表示成下列密度分布的函数：

1.质子或中子数密度：

$$
\rho_{t}(\boldsymbol{r})=\sum_{i,s}\left|\phi_{i}(\boldsymbol{r},s,t)\right|^{2}
$$

这里$\phi_{i}(\boldsymbol{r},s,t)=\langle\boldsymbol{r},s,t|i\rangle$。可以把总密度定义为$\rho(\boldsymbol{r})=\rho_{\text{p}}(\boldsymbol{r})+\rho_{\text{n}}(\boldsymbol{r})$。

2.质子或中子的动能密度：

$$
\tau_{t}(\boldsymbol{r})=\sum_{i,s}\left|\nabla\phi_{i}(\boldsymbol{r},s,t)\right|^{2}
$$

总自旋密度为$\tau(\boldsymbol{r})=\tau_{\text{p}}(\boldsymbol{r})+\tau_{\text{n}}(\boldsymbol{r})$。

3.自旋轨道流：

$$
\boldsymbol{J}_{t}(\boldsymbol{r})=-\mathrm{i}\sum_{i,s,s^{\prime}}\phi_{i}^{*}(\boldsymbol{r},s,t)(\nabla\phi_{i}(\boldsymbol{r},s^{\prime},t)\times[\boldsymbol{\sigma}]_{ss^{\prime}})
$$

总自旋轨道流密度为$\boldsymbol{J}(\boldsymbol{r})=\boldsymbol{J}_{\text{p}}(\boldsymbol{r})+\boldsymbol{J}_{\text{n}}(\boldsymbol{r})$。

这里$i$为占据单粒子态指标，$s$和$t$分别为自旋$z$方向分量和同位旋指标$z$方向分量。

我们要计算HF态下的能量期待值，根据Hartree Fock的结果，我们有：

$$
E=\langle\text{HF}|\hat{H}|\text{HF}\rangle=\sum_{i}\varepsilon_{i}+\frac{1}{2}\sum_{ij}\langle ij|\bar{v}^{(2)}|ij\rangle+\frac{1}{6}\sum_{ijk}\langle ijk|\bar{v}^{(3)}|ijk\rangle
$$

由于 skyrme 势中全是 $\delta (\boldsymbol r_1 - \boldsymbol r_2)$ 函数，因此我们期望最后结果能表示成：

$$
E=\int\mathrm{d}\boldsymbol{r}\,\mathcal{H}(\boldsymbol{r})
$$

我们挨个计算两体项，为此我们需要知道：

$$
\langle ij|\bar{v}|ij\rangle=\langle ij|v(1-P_{r}P_{\sigma}P_{\tau})|ij\rangle
$$

这里$P_{r}$和$P_{\tau}$分别为坐标和同位旋交换算符。于是第一项可以写为：

$$
E_{0}=\frac{1}{2}\sum_{ij}\langle ij|t_{0}\delta (\boldsymbol r_1 - \boldsymbol r_2)(1+x_{0}P_{\sigma})(1-P_{r}P_{\sigma}P_{\tau})|ij\rangle
$$

由于在这个积分里 $\delta$ 的存在，因此 $P_{r}=1$，[^1]。由于 skyrme 相互作用不改变同位旋，因此交换同位旋后只有两核子同位旋相等才不为零，即 $P_{\tau}=\delta_{t_{1}t_{2}}$。再利用 $P_{\sigma}=\frac{1}{2}(1+\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2})$，得到：

$$
\begin{align*}
E_{0} & =\frac{1}{2}t_{0}\sum_{ij}\langle ij|\delta (\boldsymbol r_1 - \boldsymbol r_2)[1+\frac{1}{2}x_{0}(1+\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2})][1-\frac{1}{2}\delta_{t_{1}t_{2}}(1+\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2})]|ij\rangle
\end{align*}
$$

利用 $(\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2})^{2}=3-2\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2}$，我们可以把 Pauli 算符的二次项转化为一次项。接下来为了继续推导，我们必须假设 HF 基态具有时间反演不变性[^2]。利用时间反演不变性，我们可以得到 Pauli 算符的一次项为零，证明放在附录 [[#Pauli 算符一次项为零]]。由此我们得到：

$$
E_{0}=\frac{1}{2}t_{0}\sum_{ij}\langle ij|\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})[1+\frac{1}{2}x_{0}-\delta_{t_{1}t_{2}}(\frac{1}{2}+x_{0})]|ij\rangle
$$

由此可以写成数密度的形式：

$$
\begin{align*}
E_{0} & =\frac{1}{2}t_{0}\sum_{tt^{\prime}}\int\mathrm{d}\boldsymbol{r}\,\rho_{t}(\boldsymbol{r})\rho_{t^{\prime}}(\boldsymbol{r})[1+\frac{1}{2}x_{0}-\delta_{tt^{\prime}}(\frac{1}{2}+x_{0})]\\
 & =\frac{1}{2}t_{0}\int\mathrm{d}\boldsymbol{r}\,[(1+\frac{1}{2}x_{0})\rho(\boldsymbol{r})\rho(\boldsymbol{r})-(\frac{1}{2}+x_{0})(\rho_{\text{n}}^{2}(\boldsymbol{r})+\rho_{\text{p}}^{2}(\boldsymbol{r}))]
\end{align*}
$$

由此：

$$
\mathcal{H}_{0}(\boldsymbol{r})=\frac{1}{2}t_{0}[(1+\frac{1}{2}x_{0})\rho(\boldsymbol{r})\rho(\boldsymbol{r})-(\frac{1}{2}+x_{0})(\rho_{\text{n}}^{2}(\boldsymbol{r})+\rho_{\text{p}}^{2}(\boldsymbol{r}))]
$$

与第一项相同，我们也可以写出第二项，由于$k^{\prime2}\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})$仅仅是$\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})k^{2}$的Hermite共轭[^3]，因此我们只需计算其一，即：

$$
\begin{align*}
E_{1} & =\frac{1}{2}\sum_{ij}\langle ij|\frac{1}{2}t_{1}\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})k^{2}[1-\frac{1}{2}\delta_{t_{1}t_{2}}(1+\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2})]|ij\rangle+\text{h.c.}\\
 & =\frac{1}{4}t_{1}\sum_{ij}\langle ij|\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})(k_{1}^{2}+k_{2}^{2}-2\boldsymbol{k}_{1}\cdot\boldsymbol{k}_{2})[1-\frac{1}{2}\delta_{t_{1}t_{2}}(1+\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2})]|ij\rangle+\text{h.c.}
\end{align*}
$$

出于和上面相同的对时间反演对称性的考量，我们可以略去$k_{1}^{2}$和$k_{2}^{2}$，但由于$\boldsymbol{k}_{1}\cdot\boldsymbol{k}_{2}$同时改变了$i$和$j$核子的波函数，因此不再为零。我们得到：

$$
\begin{align*}
E_{1}= & \frac{1}{4}t_{1}\sum_{ij}\langle ij|\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})(k_{1}^{2}+k_{2}^{2}-2\boldsymbol{k}_{1}\cdot\boldsymbol{k}_{2})(1-\frac{1}{2}\delta_{t_{1}t_{2}})|ij\rangle+\text{h.c.}\\
+ & \frac{1}{4}t_{1}\sum_{ij}\langle ij|\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})\delta_{t_{1}t_{2}}\boldsymbol{k}_{1}\cdot\boldsymbol{k}_{2}(\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2})|ij\rangle+\text{h.c.}\\
\equiv & E_{11}+E_{12}
\end{align*}
$$

下面计算$E_{11}$，首先我们要知道：

$$
\begin{align*}
\sum_{ist}\phi_{i}^{*}(\boldsymbol{r},s,t)\nabla\phi_{i}(\boldsymbol{r},s,t) & =\frac{1}{2}\sum_{ist}\phi_{i}^{*}(\boldsymbol{r},s,t)\nabla\phi_{i}(\boldsymbol{r},s,t)+\phi_{i}(\boldsymbol{r},-s,t)\nabla\phi_{i}^{*}(\boldsymbol{r},-s,t)=\frac{1}{2}\nabla\rho(\boldsymbol{r})\\
\sum_{ist}\phi_{i}^{*}(\boldsymbol{r},s,t)\nabla^{2}\phi_{i}(\boldsymbol{r},s,t) & =\frac{1}{2}\sum_{ist}\phi_{i}^{*}(\boldsymbol{r},s,t)\nabla^{2}\phi_{i}(\boldsymbol{r},s,t)+\phi_{i}(\boldsymbol{r},-s,t)\nabla^{2}\phi_{i}(\boldsymbol{r},-s,t)\\
 & =\frac{1}{2}\nabla^{2}\rho(\boldsymbol{r})-\tau(\boldsymbol{r})
\end{align*}
$$

由此得：

$$
\begin{align*}
\sum_{ij}\langle ij|\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})\nabla_{1}\cdot\nabla_{2}|ij\rangle & =\sum_{ij}\sum_{ss^{\prime}tt^{\prime}}\int\mathrm{d}\boldsymbol{r}\mathrm{d}\boldsymbol{r}^{\prime}\,\phi_{i}^{*}(\boldsymbol{r},s,t)\phi_{j}^{*}(\boldsymbol{r}^{\prime},s^{\prime},t^{\prime})\delta(\boldsymbol{r}-\boldsymbol{r}^{\prime})\nabla\phi_{i}(\boldsymbol{r},s,t)\cdot\nabla\phi_{j}(\boldsymbol{r}^{\prime},s^{\prime},t^{\prime})\\
 & =\frac{1}{4}\int\mathrm{d}\boldsymbol{r}\,(\nabla\rho)^{2}\\
\sum_{ij}\langle ij|\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})k_{i}^{2}|ij\rangle & =\sum_{ij}\sum_{ss^{\prime}tt^{\prime}}\int\mathrm{d}\boldsymbol{r}\mathrm{d}\boldsymbol{r}^{\prime}\,\phi_{i}^{*}(\boldsymbol{r},s,t)\phi_{j}^{*}(\boldsymbol{r}^{\prime},s^{\prime},t^{\prime})\delta(\boldsymbol{r}-\boldsymbol{r}^{\prime})\nabla^{2}\phi_{i}(\boldsymbol{r},s,t)\phi_{j}(\boldsymbol{r}^{\prime},s^{\prime},t^{\prime})\\
 & =\int\mathrm{d}\boldsymbol{r}\,(\frac{1}{2}\nabla^{2}\rho(\boldsymbol{r})-\tau(\boldsymbol{r}))\rho(\boldsymbol{r})
\end{align*}
$$

因此可得：

$$
E_{11}=-\frac{1}{16}t_{1}\int\mathrm{d}\boldsymbol{r}\,\left\{ \rho\nabla^{2}\rho-2\rho\tau-\frac{1}{2}(\nabla\rho)^{2}-\frac{1}{2}\sum_{t}[\rho_{t}\nabla^{2}\rho_{t}-2\rho_{t}\tau_{t}-\frac{1}{2}(\nabla\rho_{t})^{2}]\right\} +\text{h.c.}
$$

分部积分得：

$$
E_{11}=\frac{1}{16}t_{1}\int\mathrm{d}\boldsymbol{r}\,(2\rho\tau-\rho_{\text{n}}\tau_{\text{n}}-\rho_{\text{p}}\tau_{\text{p}}-\frac{3}{2}\rho\nabla^{2}\rho+\frac{3}{4}\rho_{\text{n}}\nabla^{2}\rho_{\text{n}}+\frac{3}{4}\rho_{\text{p}}\nabla^{2}\rho_{\text{p}})+\text{h.c.}
$$

为了计算 $E_{12}$，我们需要利用：

$$
(\nabla_{1}\cdot\nabla_{2})(\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2})=\frac{1}{3}(\nabla_{1}\cdot\boldsymbol{\sigma}_{1})(\nabla_{2}\cdot\boldsymbol{\sigma}_{2})+\frac{1}{2}(\nabla_{1}\times\boldsymbol{\sigma}_{1})\cdot(\nabla_{2}\times\boldsymbol{\sigma}_{2})+(\nabla_{1}\otimes\boldsymbol{\sigma}_{1})^{(2)}\cdot(\nabla_{2}\otimes\boldsymbol{\sigma}_{2})^{(2)}
$$

该式的证明需要利用 [[Spherical Tensor Decomposition of Rank2 Cartesian Tensor]] 中的分解，首先将上式左侧写为：

$$
\begin{align*}
(\nabla_{1}\cdot\nabla_{2})(\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2}) & =\nabla_{1i}\sigma_{1j}\nabla_{2i}\sigma_{2j}
\end{align*}
$$

我们有：

$$
\nabla_{1i}\sigma_{1j}=\frac{1}{3}(\nabla_{1}\cdot\boldsymbol{\sigma}_{1})\delta_{ij}+\frac{1}{2}\varepsilon_{ijk}(\nabla_{1}\times\boldsymbol{\sigma}_{1})_{k}+(\nabla_{1}\otimes\boldsymbol{\sigma}_{1})^{(2)}_{ij}
$$

对 $\nabla_{2 i}\sigma_{2 j}$ 也可以做这种分解，由于这是直和分解，因此两者相乘没有交叉项。再根据 $\sum_{ij}\delta_{ij}\delta_{ij}=3$ 和 $\sum_{ij}\varepsilon_{ijk}\varepsilon_{ijl}=2\delta_{kl}$，即可得到我们要用的式子，注意式子中符号的含义：

$$
(\nabla_{1}\otimes\boldsymbol{\sigma}_{1})^{(2)}\cdot(\nabla_{2}\otimes\boldsymbol{\sigma}_{2})^{(2)}=\sum_{ij}(\nabla_{1}\otimes\boldsymbol{\sigma}_{1})_{ij}^{(2)}(\nabla_{2}\otimes\boldsymbol{\sigma}_{2})_{ij}^{(2)}
$$

我们再假设原子核是轴对称的，可以得到只有第二项会保留下来，其它的都为零，这是一项艰巨的任务，因此放到附录 [[#如果原子核轴对称]]。

于是计算 $E_{12}$ 有：

$$
\begin{align*}
E_{12} & =\frac{1}{4}t_{1}\sum_{ij}\langle ij|\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})\delta_{t_{1}t_{2}}\boldsymbol{k}_{1}\cdot\boldsymbol{k}_{2}(\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2})|ij\rangle+\text{h.c.}\\
 & =-\frac{1}{32}t_{1}\sum_{ij}\sum_{s_{1}s_{2}s_{3}s_{4}t}\int\mathrm{d}\boldsymbol{r}\,\phi_{i}^{*}(\boldsymbol{r},s_{1},t)\phi_{j}^{*}(\boldsymbol{r},s_{3},t)(\nabla_{1}\times[\boldsymbol{\sigma}_{1}]_{s_{1}s_{2}})\cdot(\nabla_{2}\times[\boldsymbol{\sigma}_{2}]_{s_{3}s_{4}})\phi_{i}(\boldsymbol{r},s_{2},t)\phi_{j}(\boldsymbol{r},s_{4},t)\\
 & =\frac{1}{32}t_{1}\int\mathrm{d}\boldsymbol{r}\,(\boldsymbol{J}_{\text{p}}^{2}(\boldsymbol{r})+\boldsymbol{J}_{\text{n}}^{2}(\boldsymbol{r}))+\text{h.c.}
\end{align*}
$$

于是：

$$
E_{1}=\frac{1}{16}t_{1}(4\rho\tau-2\rho_{\text{n}}\tau_{\text{n}}-2\rho_{\text{p}}\tau_{\text{p}}-3\rho\nabla^{2}\rho+\frac{3}{2}\rho_{\text{n}}\nabla^{2}\rho_{\text{n}}+\frac{3}{2}\rho_{\text{p}}\nabla^{2}\rho_{\text{p}}+\boldsymbol{J}_{\text{n}}^{2}+\boldsymbol{J}_{\text{p}}^{2})
$$

第三项的计算非常类似，唯一的区别是这一项作用在P波上，因此$P_{r}=-1$。于是我们可以得到：

$$
E_{2}=\frac{1}{4}t_{2}\sum_{ij}\langle ij|(\overleftarrow{\nabla}_{1}\cdot\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})\overrightarrow{\nabla}_{1}-\overleftarrow{\nabla}_{2}\cdot\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})\overrightarrow{\nabla}_{1})(1+\delta_{t_{1}t_{2}}P_{\sigma})|ij\rangle
$$

分部积分得到：

$$
E_{2}=\frac{1}{4}t_{2}\sum_{ij}\langle ij|[2\overleftarrow{\nabla}_{1}\cdot\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})\overrightarrow{\nabla}_{1}+\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})(\overrightarrow{\nabla}_{1}^{2}+\overrightarrow{\nabla}_{1}\cdot\overrightarrow{\nabla}_{2})](1+\delta_{t_{1}t_{2}}P_{\sigma})|ij\rangle
$$

代入$P_{\sigma}$，只剩下：

$$
\begin{align*}
E_{2} & =\frac{1}{4}t_{2}\sum_{ij}\langle ij|2\overleftarrow{\nabla}_{1}\cdot\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})\overrightarrow{\nabla}_{1}+\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})(\overrightarrow{\nabla}_{1}^{2}+\overrightarrow{\nabla}_{1}\cdot\overrightarrow{\nabla}_{2})|ij\rangle(1+\frac{1}{2}\delta_{t_{i}t_{j}})\\
 & +\frac{1}{8}t_{2}\sum_{ij}\langle ij|\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})(\overrightarrow{\nabla}_{1}\cdot\overrightarrow{\nabla}_{2})(\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2})|ij\rangle\delta_{t_{i}t_{j}}
\end{align*}
$$

利用前面得到的结果，再分部积分得到：

$$
E_{2}=\frac{1}{16}t_{2}(4\rho\tau+2\rho_{\text{n}}\tau_{\text{n}}+2\rho_{\text{p}}\tau_{\text{p}}+\rho\nabla^{2}\rho+\frac{1}{2}\rho_{\text{n}}\nabla^{2}\rho_{\text{n}}+\frac{1}{2}\rho_{\text{p}}\nabla^{2}\rho_{\text{p}}-\boldsymbol{J}_{\text{n}}^{2}-\boldsymbol{J}_{\text{p}}^{2})
$$

接下来计算自旋轨道耦合项，利用1，2的对称性，可以写为：

$$
V_{LS}=\frac{1}{2}\mathrm{i}W_{0}[(\overleftarrow{\nabla}_{1}\times\overrightarrow{\nabla}_{1})\cdot\boldsymbol{\sigma}_{2}+\overleftarrow{\nabla}_{1}\cdot(\overrightarrow{\nabla}_{1}\times\boldsymbol{\sigma}_{1})-(\overleftarrow{\nabla}_{1}\times\overrightarrow{\nabla}_{2})\cdot\boldsymbol{\sigma}_{1}-\overleftarrow{\nabla}_{2}\cdot(\overrightarrow{\nabla}_{1}\times\boldsymbol{\sigma}_{1})]
$$

利用分部积分，可以把$-(\overleftarrow{\nabla}_{1}\times\overrightarrow{\nabla}_{2})\cdot\boldsymbol{\sigma}_{1}$替换成：

$$
(\overleftarrow{\nabla}_{2}\times\overrightarrow{\nabla}_{2})\cdot\boldsymbol{\sigma}_{1}+(\overrightarrow{\nabla}_{1}\times\overrightarrow{\nabla}_{2})\cdot\boldsymbol{\sigma}_{1}+(\overrightarrow{\nabla}_{2}\times\overrightarrow{\nabla}_{2})\cdot\boldsymbol{\sigma}_{1}
$$

经计算可以得到只剩下第二项不为零。由于时间反演对称性，上面这一项可以写为$-\overleftarrow{\nabla}_{2}\cdot(\overrightarrow{\nabla}_{1}\times\boldsymbol{\sigma}_{1})$。类似的方式，我们也可以得到$\overleftarrow{\nabla}_{1}\cdot(\overrightarrow{\nabla}_{1}\times\boldsymbol{\sigma}_{1})$可以替换成$-2\overrightarrow{\nabla}_{2}\cdot(\overrightarrow{\nabla}_{1}\times\boldsymbol{\sigma}_{1})$。因此自旋轨道耦合项可以写为：

$$
V_{LS}=-2\mathrm{i}W_{0}\overrightarrow{\nabla}_{2}\cdot\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})(\overrightarrow{\nabla}_{1}\times\boldsymbol{\sigma}_{1})
$$

由此得到：

$$
E_{LS}=-\mathrm{i}W_{0}\sum_{ij}\int\mathrm{d}\boldsymbol{r}\,[\phi_{i}^{*}(\nabla\times\boldsymbol{\sigma})\phi_{i}]\cdot(\phi_{j}^{*}\nabla\phi_{j})(1+\delta_{t_{i}t_{j}})
$$

即：

$$
E_{LS}=\frac{1}{2}W_{0}\int\mathrm{d}\boldsymbol{r}\,(\nabla\rho\cdot\boldsymbol{J}+\nabla\rho_{\text{n}}\cdot\boldsymbol{J}_{\text{n}}+\nabla\rho_{\text{p}}\cdot\boldsymbol{J}_{\text{p}})
$$

分部积分，得：

$$
\mathcal{H}_{LS}=-\frac{1}{2}W_{0}(\rho\nabla\cdot\boldsymbol{J}+\rho_{\text{n}}\nabla\cdot\boldsymbol{J}_{\text{n}}+\rho_{\text{p}}\nabla\cdot\boldsymbol{J}_{\text{p}})
$$

下面计算三体项：

$$
\begin{align*}
\bar{V}^{(3)} & =t_{3}\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})\delta(\boldsymbol{r}_{2}-\boldsymbol{r}_{3})(1+P_{\sigma}(12)P_{\sigma}(23)P_{\tau}(12)P_{\tau}(23)+P_{\sigma}(13)P_{\sigma}(23)P_{\tau}(13)P_{\tau}(23)\\
 & -P_{\sigma}(12)P_{\tau}(12)-P_{\sigma}(23)P_{\tau}(23)-P_{\sigma}(31)P_{\tau}(31))
\end{align*}
$$

通过重新标记指标，可以得到：

$$
\bar{V}^{(3)}=t_{3}\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})\delta(\boldsymbol{r}_{2}-\boldsymbol{r}_{3})(1+2P_{\sigma}(12)P_{\sigma}(23)P_{\tau}(12)P_{\tau}(23)-3P_{\sigma}(12)P_{\tau}(12))
$$

代入自旋交换算符，只保留不为零的项，得到：

$$
\bar{V}^{(3)}=t_{3}\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})\delta(\boldsymbol{r}_{2}-\boldsymbol{r}_{3})(1+\frac{1}{2}P_{\tau}(12)P_{\tau}(23)-\frac{3}{2}P_{\tau}(12))
$$

于是得到：

$$
E_{3}=\frac{1}{6}t_{3}\sum_{ijk}\int\mathrm{d}\boldsymbol{r}\,(\phi_{i}^{*}\phi_{i})(\phi_{j}^{*}\phi_{j})(\phi_{k}^{*}\phi_{k})(1+\frac{1}{2}\delta_{t_{i}t_{j}\delta_{t_{j}t_{k}}}-\frac{3}{2}\delta_{t_{i}t_{j}})
$$

于是得到：

$$
\mathcal{H}_{3}=\frac{1}{6}t_{3}[\rho^{3}+\frac{1}{2}(\rho_{\text{n}}^{3}+\rho_{\text{p}}^{3})-\frac{3}{2}\rho(\rho_{\text{n}}^{2}+\rho_{\text{p}}^{2})]=\frac{1}{4}t_{3}\rho\rho_{\text{p}}\rho_{\text{n}}
$$

最终我们得到：

$$
\begin{align*}
\mathcal{H}(\boldsymbol{r}) & =\frac{1}{2}t_{0}[(1+\frac{1}{2}x_{0})\rho^{2}-(x_{0}+\frac{1}{2})(\rho_{\text{n}}^{2}+\rho_{\text{p}}^{2})]\\
 & +\frac{1}{4}(t_{1}+t_{2})\rho\tau+\frac{1}{8}(t_{2}-t_{1})(\rho_{\text{n}}\tau_{\text{n}}+\rho_{\text{p}}\tau_{\text{p}})+\frac{1}{16}(t_{2}-3t_{1})\rho\nabla^{2}\rho+\frac{1}{32}(3t_{1}+t_{2})(\rho_{\text{n}}\nabla^{2}\rho_{\text{n}}+\rho_{\text{p}}\nabla^{2}\rho_{\text{p}})\\
 & +\frac{1}{16}(t_{1}-t_{2})(\boldsymbol{J}_{\text{n}}^{2}+\boldsymbol{J}_{\text{p}}^{2})-\frac{1}{2}W_{0}(\rho\nabla\cdot\boldsymbol{J}+\rho_{\text{n}}\nabla\cdot\boldsymbol{J}_{\text{n}}+\rho_{\text{p}}\nabla\cdot\boldsymbol{J}_{\text{p}})+\frac{1}{4}t_{3}\rho_{\text{n}}\rho_{\text{p}}\rho
\end{align*}
$$

## 附录

### Pauli 算符一次项为零

态 $|i\rangle$ 的时间反演态记做 $|\mathsf{T}i\rangle$，我们有：

$$
\begin{align*}
\phi_{\bar{i}}(\boldsymbol{r},s,t) & =\langle\boldsymbol{r},s,t|\mathsf{T}i\rangle=\langle\mathsf{T}(\boldsymbol{r},s,t)|i\rangle^{*}\\
 & =-2s\langle\boldsymbol{r},-s,t|i\rangle^{*}\\
 & =-2s\phi_{i}^{*}(\boldsymbol{r},-s,t)
\end{align*}
$$

下面我们计算：

$$
\begin{align*}
 & \sum_{i}\phi_{i}^{*}(\boldsymbol{r},s,t)\phi_{i}(\boldsymbol{r},s^{\prime},t)\\
= & \delta_{ss^{\prime}}\sum_{i}|\phi_{i}(\boldsymbol{r},s,t)|^{2}\\
= & \frac{1}{2}\delta_{ss^{\prime}}\sum_{i}(|\phi_{i}(\boldsymbol{r},s,t)|^{2}+|\phi_{i}(\boldsymbol{r},-s,t)|^{2})\\
= & \frac{1}{2}\delta_{ss^{\prime}}\rho_{t}(\boldsymbol{r})
\end{align*}
$$

由此：

$$
\begin{align*}
 & \sum_{iss^{\prime}}\phi_{i}^{*}(\boldsymbol{r},s,t)[\boldsymbol{\sigma}]_{ss^{\prime}}\phi_{i}(\boldsymbol{r},s^{\prime},t)\\
= & \frac{1}{2}\sum_{ss^{\prime}}\delta_{ss^{\prime}}\rho_{t}(\boldsymbol{r})[\boldsymbol{\sigma}]_{ss^{\prime}}\\
= & 0
\end{align*}
$$

上面我们会遇到两种情况，一种是 $\sum_{ij}\langle ij|\delta (\boldsymbol{r}_{1}-\boldsymbol{r}_{2})(\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2})|ij\rangle$，它等于：

$$
\sum_{ij}\sum_{s_{1}s_{2}s_{1}^{\prime}s_{2}^{\prime}}\sum_{tt^{\prime}}\phi_{i}^{*}(\boldsymbol{r},s_{1},t)\phi_{j}^{*}(\boldsymbol{r},s_{2},t^{\prime})[\boldsymbol{\sigma}]_{s_{1}s_{1}^{\prime}}\cdot[\boldsymbol{\sigma}]_{s_{2}s_{2}^{\prime}}\phi_{i}(\boldsymbol{r},s_{1}^{\prime},t)\phi_{j}(\boldsymbol{r},s_{2}^{\prime},t^{\prime})
$$

根据上面的式子它为零。另一种是 $\sum_{ij}\langle ij|\delta (\boldsymbol{r}_{1}-\boldsymbol{r}_{2})\delta_{t_{1}t_{2}}(\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2})|ij\rangle$，它只需要令上面的 $t=t^{\prime}$ 即可，显然依旧为零。

### 如果原子核轴对称

[^1]: 需要考虑到为 S 波。
[^2]: 因此该密度泛函只能用于偶偶核。
[^3]: 只需验证 $\langle i^{\prime}j^{\prime}|k^{\prime2}\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})|ij\rangle=\langle ij|\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})k^{2}|i^{\prime}j^{\prime}\rangle^{*}$。