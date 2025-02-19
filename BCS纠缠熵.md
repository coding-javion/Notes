部分空间 $A$ 上的 Mask 函数 $\theta_{A}(\boldsymbol{r})$ 定义为：

$$
\theta_{A}(\boldsymbol{r})=\begin{cases}
1 & \boldsymbol{r}\in A\\
0 & \boldsymbol{r}\notin A
\end{cases}
$$

单粒子部分空间投影算符定义为：

$$
\langle\boldsymbol{r}s|P_{A}|\boldsymbol{r}^{\prime}s^{\prime}\rangle=\delta(\boldsymbol{r}-\boldsymbol{r}^{\prime})\delta_{ss^{\prime}}\theta_{A}(\boldsymbol{r})
$$

容易看出其是厄米算符。可以验证：

$$
\begin{align*}
\langle\boldsymbol{r}s|P_{A}|i\rangle & =\sum_{s^{\prime}}\int\mathrm{d}\boldsymbol{r}^{\prime}\langle\boldsymbol{r}s|P_{A}|\boldsymbol{r}^{\prime}s^{\prime}\rangle\langle\boldsymbol{r}^{\prime}s^{\prime}|\phi_{i}\rangle\\
 & =\int\mathrm{d}\boldsymbol{r}^{\prime}\delta(\boldsymbol{r}-\boldsymbol{r}^{\prime})\theta_{A}(\boldsymbol{r})\phi_{i}(\boldsymbol{r}^{\prime},s)\\
 & =\theta_{A}(\boldsymbol{r})\phi_{i}(\boldsymbol{r},s)
\end{align*}
$$

相当于只保留了 $A$ 空间上的波函数。此外可以验证：

$$
\begin{align*}
\langle\boldsymbol{r}s|P_{A}P_{A}|\boldsymbol{r}^{\prime}s^{\prime}\rangle & =\sum_{s^{\prime\prime}}\int\mathrm{d}\boldsymbol{r}^{\prime\prime}\langle\boldsymbol{r}s|P_{A}|\boldsymbol{r}^{\prime\prime}s^{\prime\prime}\rangle\langle\boldsymbol{r}^{\prime\prime}s^{\prime\prime}|P_{A}|\boldsymbol{r}^{\prime}s^{\prime}\rangle\\
 & =\sum_{s^{\prime\prime}}\int\mathrm{d}\boldsymbol{r}^{\prime\prime}\delta(\boldsymbol{r}-\boldsymbol{r}^{\prime\prime})\delta_{ss^{\prime\prime}}\theta_{A}(\boldsymbol{r})\delta(\boldsymbol{r}^{\prime\prime}-\boldsymbol{r}^{\prime})\delta_{s^{\prime\prime}s^{\prime}}\theta_{A}(\boldsymbol{r}^{\prime})\\
 & =\theta_{A}(\boldsymbol{r})\delta(\boldsymbol{r}-\boldsymbol{r}^{\prime})\delta_{ss^{\prime}}\\
 & =\langle\boldsymbol{r}s|P_{A}|\boldsymbol{r}^{\prime}s^{\prime}\rangle
\end{align*}
$$

证明其确实为投影算符。

Dirac 表示下的部分空间投影算符为：

$$
P_{A}=\sum_{s}\int_{A}\mathrm{d}\boldsymbol{r}\,|\boldsymbol{r}s\rangle\langle\boldsymbol{r}s|
$$

这里 $\int_{A}$ 表示只在 $A$ 空间上积分。

Fock 空间上其无定义。例如假设我们考虑其定义为：

$$
\begin{align*}
\langle\boldsymbol{r}_{1}s_{1}\dots\boldsymbol{r}_{N}s_{N}|P_{A}|i_{1}\dots i_{N}\rangle & =|\langle\boldsymbol{r}_{i}s_{i}|P_{A}|i_{j}\rangle|_{\zeta}\\
 & =\sum_{Q}\zeta^{Q}\prod_{i}\langle\boldsymbol{r}_{i}s_{i}|P_{A}|i_{Q(i)}\rangle
\end{align*}
$$

然而，一方面，我们想要部分空间投影算符之和为 1：

$$
\langle\boldsymbol{r}_{1}s_{1}\dots\boldsymbol{r}_{N}s_{N}|P_{A}+P_{A^{\perp}}|i_{1}\dots i_{N}\rangle=\left|\langle\boldsymbol{r}_{i}s_{i}|i_{j}\rangle\right|_{\zeta}
$$

另一方面，按照我们的定义，结果实际上却是：

$$
\begin{align*}
\langle\boldsymbol{r}_{1}s_{1}\dots\boldsymbol{r}_{N}s_{N}|P_{A}+P_{A^{\perp}}|i_{1}\dots i_{N}\rangle & =|\langle\boldsymbol{r}_{i}s_{i}|P_{A}|i_{j}\rangle|_{\zeta}+|\langle\boldsymbol{r}_{i}s_{i}|P_{A^{\perp}}|i_{j}\rangle|_{\zeta}\\
 & =\left(\prod_{i}\theta_{A}(\boldsymbol{r}_{i})+\prod_{i}\theta_{A^{\perp}}(\boldsymbol{r}_{i})\right)\left|\langle\boldsymbol{r}_{i}s_{i}|i_{j}\rangle\right|_{\zeta}\\
 & \neq\left|\langle\boldsymbol{r}_{i}s_{i}|i_{j}\rangle\right|_{\zeta}
\end{align*}
$$

因此这一定义并不好。

考虑 BCS 态为：

$$
|\text{BCS}\rangle=\prod_{k}\alpha_{i}|\rangle
$$

准粒子产生湮灭算符满足：

$$
\begin{align*}
\{\alpha_{i},\alpha_{j}^{\dagger}\} & =\delta_{ij}\\
\{\alpha_{i},\alpha_{j}\}=\{\alpha_{i}^{\dagger},\alpha_{j}^{\dagger}\} & =0
\end{align*}
$$

由此可以计算出：

$$
\begin{align*}
\{P_{A}\alpha_{i},P_{A}\alpha_{j}\} & =M_{ij}\\
\{(P_{A}\alpha_{i})^{\dagger},(P_{A}\alpha_{j})^{\dagger}\} & =M_{ij}^{*}\\
\{P_{A}\alpha_{i},(P_{A}\alpha_{j})^{\dagger}\} & =N_{ij}^{*}\\
\{(P_{A}\alpha_{i})^{\dagger},P_{A}\alpha_{j}\} & =N_{ij}
\end{align*}
$$

令 $\zeta=\begin{bmatrix}P_{A}\alpha & (P_{A}\alpha)^{\dagger}\end{bmatrix}$。由此可得：

$$
\{\zeta,\zeta^{\dagger}\}=\begin{bmatrix}M & N^{*}\\
N & M^{*}
\end{bmatrix}
$$

如果 $M$ 是实矩阵，那么其一定是厄米矩阵，可以使用酉矩阵 $W$ 将之对角化，猜测其对角化后具有形式：

$$
W\begin{bmatrix}M & N^{*}\\
N & M^{*}
\end{bmatrix}W^{\dagger}=\mathop{\text{diag}}(d_{1},\dots,d_{\Omega},d_{1},\dots,d_{\Omega})
$$

由此可以定义一组新的基 $\xi = W\zeta$，满足：

$$
\{\xi,\xi^{\dagger}\}=W\{\zeta,\zeta^{\dagger}\}W^{\dagger}=\mathop{\text{diag}}(d_{1},\dots,d_{\Omega},d_{1},\dots,d_{\Omega})
$$

令 $\xi=\begin{bmatrix}\beta & \beta^{\dagger}\end{bmatrix}$，则 $\beta$ 满足正常产生湮灭算符的对易关系。再定义 $\gamma_{i}^{A}=\frac{1}{\sqrt{d_{i}}}\beta_{i}$，即可得到归一化的产生湮灭算符。

对 B 空间同理，最终得到一组产生算符 $\gamma_{i}^{B}$。

由此：

$$
\begin{align*}
\alpha_{i} & =P_{A}\alpha_{i}+P_{B}\alpha_{i}\\
 & =(W^{A\dagger}D^{A}[\gamma^{A},\gamma^{A\dagger}]^{\mathrm{T}})_{i}+(W^{B\dagger}D^{B}[\gamma^{B},\gamma^{B\dagger}]^{\mathrm{T}})_{i}
\end{align*}
$$

BCS 波函数可以写为：

$$
\begin{align*}
\prod_{i}\alpha_{i}|\rangle & =\prod_{i}[(W^{A\dagger}D^{A}[\gamma^{A},\gamma^{A\dagger}]^{\mathrm{T}})_{i}+(W^{B\dagger}D^{B}[\gamma^{B},\gamma^{B\dagger}]^{\mathrm{T}})_{i}]|\rangle
\end{align*}
$$

 $W^{A}$ 和 $W^{B}$ 是否相等？

考虑：

$$
\langle\boldsymbol{r}|\{P_{A}\alpha_{i},P_{A}\alpha_{j}\}|\boldsymbol{r}^{\prime}\rangle=\sum_{n}\left(\langle\boldsymbol{r}|P_{A}\alpha_{i}|n\rangle\langle n|P_{A}\alpha_{j}|\boldsymbol{r}^{\prime}\rangle+\langle\boldsymbol{r}|P_{A}\alpha_{j}|n\rangle\langle n|P_{A}\alpha_{i}|\boldsymbol{r}^{\prime}\rangle\right)
$$

取其中一项有：

$$
\begin{align*}
\langle\boldsymbol{r}|P_{A}\alpha_{i}|n\rangle & =\langle\boldsymbol{r}|P_{A}(u_{i}a_{i}-v_{i}a_{\bar{i}}^{\dagger})|n\rangle\\
 & =\sum_{j}\langle\boldsymbol{r}|P_{A}|j\rangle\langle j|(u_{i}a_{i}-v_{i}a_{\bar{i}}^{\dagger})|n\rangle
\end{align*}
$$

由此，当 $|n\rangle=|ij\rangle$ 或者 $|n\rangle=|\rangle$ 且 $j=\bar{i}$ 时，上式不为零。

$$
\begin{align*}
\langle\boldsymbol{r}|P_{A}\alpha_{i}|\rangle & =-v_{i}\phi_{\bar{i}}(\boldsymbol{r})\theta_{A}(\boldsymbol{r})\\
\langle\boldsymbol{r}|P_{A}\alpha_{i}|ik\rangle & =\sum_{j}\langle\boldsymbol{r}|P_{A}|j\rangle\langle j|u_{i}a_{i}|ik\rangle\\
 & =u_{i}\phi_{k}(\boldsymbol{r})\theta_{A}\left(\boldsymbol{r}\right)
\end{align*}
$$

另有：

$$
\begin{align*}
\langle|P_{A}\alpha_{i}|\boldsymbol{r}\rangle & =0\\
\langle ik|P_{A}\alpha_{i}|\boldsymbol{r}\rangle & =\sum_{j}\langle ik|P_{A}\alpha_{i}|j\rangle\langle j|\boldsymbol{r}\rangle\\
 & =-v_{i}\sum_{j}\sum_{lm}P_{lm}\langle ik|a_{l}^{\dagger}a_{m}a_{\bar{i}}^{\dagger}|j\rangle\phi_{j}^{*}(\boldsymbol{r})\\
 & =-v_{i}\sum_{j}\sum_{lm}P_{lm}(\delta_{ij}\delta_{kl}\delta_{m\bar{i}}-\delta_{il}\delta_{kj}\delta_{m\bar{i}})\phi_{j}^{*}(\boldsymbol{r})\\
 & =v_{i}\left(P_{i\bar{i}}\phi_{k}^{*}(\boldsymbol{r})-P_{k\bar{i}}\phi_{i}^{*}(\boldsymbol{r})\right)
\end{align*}
$$

由此：

$$
\begin{align*}
\sum_{n}\langle\boldsymbol{r}|P_{A}\alpha_{i}|n\rangle\langle n|P_{A}\alpha_{j}|\boldsymbol{r}^{\prime}\rangle & =\langle\boldsymbol{r}|P_{A}\alpha_{i}|\rangle\langle|P_{A}\alpha_{j}|\boldsymbol{r}^{\prime}\rangle+\frac{1}{2}\sum_{k}\langle\boldsymbol{r}|P_{A}\alpha_{i}|ik\rangle\langle ik|P_{A}\alpha_{j}|\boldsymbol{r}^{\prime}\rangle\\
 & =\frac{\delta_{ij}}{2}u_{i}v_{i}\theta_{A}(\boldsymbol{r})\sum_{k}\phi_{k}(\boldsymbol{r})\left(P_{i\bar{i}}\phi_{k}^{*}(\boldsymbol{r})-P_{k\bar{i}}\phi_{i}^{*}(\boldsymbol{r})\right)
\end{align*}
$$

上式对于 $i, j$ 是对称的，因此交换 $i, j$ 相加后显然不为零。由此其不满足产生湮灭算符的对易关系，$P_{A}\alpha_{i}$ 不是产生算符。

记 $B$ 为 $A$ 的补空间，考虑矩阵：

$$
\begin{align*}
[M(A)]_{ij} & =\langle|\alpha_{j}P_{A}\alpha_{i}^{\dagger}|\rangle\\{}
[M(B)]_{ij} & =\langle|\alpha_{j}P_{B}\alpha_{i}^{\dagger}|\rangle
\end{align*}
$$

它们显然满足：

$$
[M(A)]_{ij}+[M(B)]_{ij}=\langle|\alpha_{j}^{\dagger}\alpha_{i}|\rangle=\delta_{ij}
$$

可将其同时对角化。

$$
|\{n\}\rangle=\prod_{n_{p}\neq0}a_{p}^{\dagger}|\rangle=\prod_{p}[(1-n_{p})+n_{p}a_{p}^{\dagger}]|\rangle
$$

$$
\begin{align*}
|\{n^{A}\}\{n^{B}\}\rangle & =\prod_{n_{p},n_{q}\neq0}a_{p}^{\dagger}b_{q}^{\dagger}|\rangle\\
 & =\prod_{pq}[(1-n_{p}^{A})+n_{p}^{A}a_{p}^{\dagger}][(1-n_{q}^{B})+n_{q}^{B}b_{q}^{\dagger}]|\rangle
\end{align*}
$$

$$
\begin{align*}
 & \sum_{\{n^{B}\}}\langle\{n^{A}\}\{n^{B}\}|\text{gs}\rangle\langle\text{gs}|\{m^{A}\}\{n^{B}\}\rangle\\
= & \sum_{\{n^{B}\}}\langle|\prod_{pq}\prod_{i}[(1-n_{p}^{A})+n_{p}^{A}a_{p}][(1-n_{q}^{B})+n_{q}^{B}b_{q}](\sqrt{d_{i}}a_{i}^{\dagger}+\sqrt{1-d_{i}}b_{i}^{\dagger})|\rangle\langle|\prod_{j}(\sqrt{d_{j}}a_{j}+\sqrt{1-d_{j}}b_{j})\prod_{rs}[(1-m_{r}^{A})+m_{r}^{A}a_{r}^{\dagger}][(1-n_{s}^{B})+n_{s}^{B}b_{s}^{\dagger}]|\rangle
\end{align*}
$$

$$
\begin{align*}
 & \langle|\prod_{pq}\prod_{i}[(1-n_{p}^{A})+n_{p}^{A}a_{p}][(1-n_{q}^{B})+n_{q}^{B}b_{q}](\sqrt{d_{i}}a_{i}^{\dagger}+\sqrt{1-d_{i}}b_{i}^{\dagger})|\rangle\\
= & \langle|\prod_{pq\neq i}(1-n_{p}^{A})(1-n_{q}^{B})\prod_{i}[(1-n_{q}^{B})n_{p}^{A}\sqrt{d_{i}}a_{p}a_{i}^{\dagger}+(1-n_{p}^{A})n_{q}^{B}\sqrt{1-d_{i}}b_{q}b_{i}^{\dagger}]|\rangle
\end{align*}
$$

$$
\begin{align*}
 & \sum_{\{n^{B}\}}\langle\{n^{A}\}\{n^{B}\}|\text{gs}\rangle\langle\text{gs}|\{m^{A}\}\{n^{B}\}\rangle\\
= & \sum_{\{n^{B}\}}\langle|\prod_{pq\neq i}(1-n_{p}^{A})(1-n_{q}^{B})\prod_{i}[(1-n_{i}^{B})n_{i}^{A}\sqrt{d_{i}}a_{i}a_{i}^{\dagger}+(1-n_{i}^{A})n_{i}^{B}\sqrt{1-d_{i}}b_{i}b_{i}^{\dagger}]|\rangle\langle|\prod_{rs\neq j}(1-m_{r}^{A})(1-n_{s}^{B})\prod_{j}[(1-m_{j}^{A})n_{j}^{B}\sqrt{1-d_{j}}b_{j}b_{j}^{\dagger}+(1-n_{j}^{B})m_{j}^{A}\sqrt{d_{j}}a_{j}a_{j}^{\dagger}]|\rangle\\
= & \sum_{\{n^{B}\}}\prod_{pq\neq i}(1-n_{p}^{A})(1-n_{q}^{B})\prod_{i}[(1-n_{i}^{B})n_{i}^{A}\sqrt{d_{i}}+(1-n_{i}^{A})n_{i}^{B}\sqrt{1-d_{i}}]\prod_{rs\neq j}(1-m_{r}^{A})(1-n_{s}^{B})\prod_{j}[(1-m_{j}^{A})n_{j}^{B}\sqrt{1-d_{j}}+(1-n_{j}^{B})m_{j}^{A}\sqrt{d_{j}}]\\
= & \prod_{p\neq i}(1-n_{p}^{A})\prod_{r\neq j}(1-m_{r}^{A})\sum_{\{n^{B}\}}\prod_{q\neq i}(1-n_{q}^{B})\prod_{i}[(1-n_{i}^{B})n_{i}^{A}\sqrt{d_{i}}+(1-n_{i}^{A})n_{i}^{B}\sqrt{1-d_{i}}]\prod_{s\neq j}(1-n_{s}^{B})\prod_{j}[(1-m_{j}^{A})n_{j}^{B}\sqrt{1-d_{j}}+(1-n_{j}^{B})m_{j}^{A}\sqrt{d_{j}}]\\
= & \prod_{p\neq i}(1-n_{p}^{A})\prod_{r\neq j}(1-m_{r}^{A})\sum_{\{n^{B}\}}\prod_{q\neq i}(1-n_{q}^{B})\prod_{i}[(1-n_{i}^{B})n_{i}^{A}\sqrt{d_{i}}+(1-n_{i}^{A})n_{i}^{B}\sqrt{1-d_{i}}][(1-m_{i}^{A})n_{i}^{B}\sqrt{1-d_{i}}+(1-n_{i}^{B})m_{i}^{A}\sqrt{d_{i}}]\\
= & \prod_{p\neq i}(1-n_{p}^{A})\prod_{r\neq j}(1-m_{r}^{A})\sum_{\{n^{B}\}}\prod_{q\neq i}(1-n_{q}^{B})\prod_{i}[(1-n_{i}^{B})n_{i}^{A}m_{i}^{A}d_{i}+(1-n_{i}^{A})(1-m_{i}^{A})n_{i}^{B}(1-d_{i})]\\
= & \prod_{p\neq i}(1-n_{p}^{A})\prod_{r\neq j}(1-m_{r}^{A})\prod_{i}[n_{i}^{A}m_{i}^{A}d_{i}+(1-n_{i}^{A})(1-m_{i}^{A})(1-d_{i})]\\
= & \prod_{i}[n_{i}^{A}m_{i}^{A}d_{i}+(1-n_{i}^{A})(1-m_{i}^{A})(1-d_{i})]\quad n_{\text{unocc}}^{A},m_{\text{unocc}}^{A}=0\\
= & \prod_{i}[n_{i}^{A}d_{i}+(1-n_{i}^{A})(1-d_{i})]\quad\{m^{A}\}=\{n^{A}\};n_{\text{unocc}}^{A}=0
\end{align*}
$$