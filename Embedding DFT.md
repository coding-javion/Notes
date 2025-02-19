---
related: "[[Density Functional]]"
date: 2023-01-27 15:24
---
通常的密度泛函写为：
$$
E[\rho]=T_{\text{S}}[\rho]+V_{\text{nuc}}[\rho]+E_{\text{H}}[\rho]+E_{\text{XC}}[\rho]+V_{\text{nn}}
$$

如果把 $\rho$ 写作子系统的密度之和：

$$
\rho(\boldsymbol{r})=\rho_{\mathrm{tot}}(\boldsymbol{r})=\sum_{I}\rho_{I}(\boldsymbol{r})
$$

每一个子系统的密度可以通过无相互作用系统的轨道表出：

$$
\rho_{I}(\boldsymbol{r})=\sum_{i_{I}}^{N_{i}}\left|\psi_{i_{I}}(\boldsymbol{r})\right|^{2}
$$

如果我们试图在子系统内做计算，我们势必要将动能写成只与子系统相关的形式，首先我们写成：

$$
T_{\text{S}}[\rho]\approx\sum_{I}T_{\text{S}}[\rho_{I}]
$$

这里之所以写成约等号，是因为：

$$
\begin{align*}
T_{\text{S}}[\rho] & =\min_{\{\psi_{i}\}\rightarrow\rho}\sum_{i}^{N}\langle\psi_{i}|-\nabla^{2}/2|\psi_{i}\rangle\\
\sum_{I}T_{\text{S}}[\rho_I] & =\sum_{I}\min_{\{\psi_{i_{I}}\}\rightarrow\rho_{I}}\sum_{i}^{N_{I}}\langle\psi_{i_{I}}|-\nabla^{2}/2|\psi_{i_{I}}\rangle
\end{align*}
$$

可以看出，两者并不一定相等。

我们把剩余的动能部分简单的定义为 $T_{\text{S}}^{\text{nad}}$：

$$
T_{\text{S}}^{\text{nad}}[\{\rho_{I}\}]=T_{\text{S}}[\rho]-\sum_{I}T_{\text{S}}[\rho_{I}]
$$

于是能量泛函为：

$$
E[\rho]=\sum_{I}T_{\text{S}}[\rho_{I}]+V_{\text{nuc}}[\rho]+J[\rho]+E_{\text{XC}}[\rho]+T_{\text{S}}^{\text{nad}}[\{\rho_{I}\}]+V_{\text{nn}}
$$

现在只考虑两个子系统 $A,B$，对能量泛函做变分得到：

$$
\left(-\frac{\nabla^{2}}{2}+v_{\text{eff}}^{(A)}[\rho_{A}](\boldsymbol{r})+v_{\text{emb}}^{(A)}[\rho_{A},\rho_{B}](\boldsymbol{r})\right)\psi_{i_{A}}(\boldsymbol{r})=\varepsilon_{i_{A}}\psi_{i_{A}}(\boldsymbol{r})
$$

这里，$v_{\text{eff}}^{(A)}[\rho_{A}]$ 为：

$$
v_{\text{eff}}^{(A)}[\rho_{A}](\boldsymbol{r})=v_{\text{nuc}}^{(A)}(\boldsymbol{r})+v_{\text{H}}[\rho_{A}](\boldsymbol{r})+v_{\text{XC}}[\rho_{A}](\boldsymbol{r})
$$

而 $v_{\text{emb}}^{(B)}[\rho_{A},\rho_{B}]$ 为：

$$
v_{\text{emb}}^{(A)}[\rho_{A},\rho_{B}](\boldsymbol{r})=v_{\text{nuc}}^{(B)}(\boldsymbol{r})+v_{\text{H}}[\rho_{B}](\boldsymbol{r})+v_{\text{XC}}^{\text{nad}}[\rho_{A},\rho_{B}](\boldsymbol{r})+v_{\text{kin}}^{\text{nad}}[\rho_{A},\rho_{B}](\boldsymbol{r})
$$

### Nonadditive Kinetic Energy

大概率的（也就是说没有证明），有：

$$
T_{\text{S}}^{\text{nad}}[\{\rho_{I}\}]\geq0
$$

