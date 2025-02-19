正则系综的配分函数为：

$$
Z=\mathop{\text{Tr}}(\mathrm{e}^{-\beta H})
$$

巨正则系综只需要把 $H$ 替换为 $K=H-\mu\hat{N}$。正则系综的密度矩阵为：

$$
\rho=\frac{\mathrm{e}^{-\beta H}}{Z}
$$


一个算符 $O$ 的系综平均值可以写为：

$$
\langle O\rangle=\mathop{\text{Tr}}(\rho O)
$$


现在我们利用路径积分表示配分函数。由于相干态是过完备的，我们不能直接把求迹定义为对所有相干态求和。我们采用插入完备基的方式推导：

$$
\begin{align*}
Z & =\sum_{n}\langle n|\mathrm{e}^{-\beta H}|n\rangle\\
 & =\int\mathrm{d}\psi\,\mathrm{e}^{-\bar{\psi}\cdot\psi}\sum_{n}\langle\zeta\psi|\mathrm{e}^{-\beta H}|n\rangle\langle n|\psi\rangle\\
 & =\int\mathrm{d}\psi\,\mathrm{e}^{-\bar{\psi}\cdot\psi}\langle\zeta\psi|\mathrm{e}^{-\beta H}|\psi\rangle
\end{align*}
$$
由此我们可以使用路径积分公式：

