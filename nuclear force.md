核力对 $S, J, M_{J}, M_{T}$ 守恒且与 $M_{J}$ 无关，并且 $L+S+T$ 为奇数。

$V(T_z = -1) = V_{pp}$ , $V(T_z = 0) = V_{np}$, $V(T_Z = 1) = V_{nn}$ 。


$$
\begin{align*}
w_{1} & =1\\
w_{2} & =\boldsymbol{L}\cdot(\boldsymbol{\sigma}_{1}+\boldsymbol{\sigma}_{2})\\
w_{3} & =\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2}\\
w_{4} & =(\boldsymbol{r}\cdot\boldsymbol{\sigma}_{1})(\boldsymbol{r}\cdot\boldsymbol{\sigma}_{2})\\
w_{5} & =(\boldsymbol{p}\cdot\boldsymbol{\sigma}_{1})(\boldsymbol{p}\cdot\boldsymbol{\sigma}_{2})\\
w_{6} & =(\boldsymbol{L}\cdot\boldsymbol{\sigma}_{1})(\boldsymbol{L}\cdot\boldsymbol{\sigma}_{2})
\end{align*}
$$


$$
\begin{aligned}
w_1&=1\\
w_2&=\vec{\sigma}_1 \cdot \vec{\sigma}_2\\
w_3&=i(\vec{\sigma}_1 + \vec{\sigma}_2)\cdot (\mathbf{p}\times\mathbf{p'})\\
w_4&=\vec{\sigma}_1\cdot (\mathbf{p}\times\mathbf{p'})\,\vec{\sigma}_2\cdot (\mathbf{p}\times\mathbf{p'})\\
w_5&=\vec{\sigma}_1\cdot (\mathbf{p'}+\mathbf{p})\,\vec{\sigma}_2\cdot (\mathbf{p'}+\mathbf{p})\\
w_6&=\vec{\sigma}_1\cdot (\mathbf{p'}-\mathbf{p})\,\vec{\sigma}_2\cdot (\mathbf{p'}-\mathbf{p})\\
\end{aligned}
$$

## 核力是实是虚

平面波表象

矩阵元 $\langle\boldsymbol{p}_{1}^{\prime}s_{1}^{\prime}\boldsymbol{p}_{2}^{\prime}s_{2}^{\prime}|V|\boldsymbol{p}_{1}s_{1}\boldsymbol{p}_{2}s_{2}\rangle$。

- 厄米性 $=\langle\boldsymbol{p}_{1}s_{1}\boldsymbol{p}_{2}s_{2}|V|\boldsymbol{p}_{1}^{\prime}s_{1}^{\prime}\boldsymbol{p}_{2}^{\prime}s_{2}^{\prime}\rangle^*$。
- 宇称 $=\langle-\boldsymbol{p}_{1}^{\prime}s_{1}^{\prime},-\boldsymbol{p}_{2}^{\prime}s_{2}^{\prime}|V|-\boldsymbol{p}_{1}s_{1},-\boldsymbol{p}_{2}s_{2}\rangle$。
- 时间反演 $=\langle-\boldsymbol{p}_{1},-s_{1},-\boldsymbol{p}_{2},-s_{2}|V|-\boldsymbol{p}_{1}^{\prime},-s_{1}^{\prime},-\boldsymbol{p}_{2}^{\prime},-s_{2}^{\prime}\rangle$。

考虑三种变换的联合，得到 $=\langle\boldsymbol{p}_{1}^{\prime},-s_{1}^{\prime},\boldsymbol{p}_{2}^{\prime},-s_{2}^{\prime}|V|\boldsymbol{p}_{1},-s_{1},\boldsymbol{p}_{2},-s_{2}\rangle^{*}$，只需 $s_{1}, s_{1}^{\prime}, s_{2}, s_{2}^{\prime}$ 反号不变，则可得到矩阵元是实的。考虑 Pauli 矩阵的形式，发现 $\sigma_{x}$ 在 $s$ 变号下不变，$\sigma_{y},\sigma_{z}$ 在 $s$ 变号下反号。因此要么没有 $\sigma$ 算符，要么出现 $\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2}$ 使得变的号相消，否则矩阵元就不是实的。因此，上面六项 $w$ 中只有 $w_{1}, w_{2}$ 是实的。
