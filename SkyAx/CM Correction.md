动量投影算符为：

$$
\hat{P}=\frac{1}{V}\int\mathrm{d}\boldsymbol{x}\,\mathrm{e}^{-\mathrm{i}\boldsymbol{x}\cdot\hat{\boldsymbol{P}}}
$$

能量值为：

$$
\begin{align*}
\langle\text{BCS}|\hat{P}\hat{H}|\text{BCS}\rangle & =\frac{1}{V}\int\mathrm{d}\boldsymbol{x}\langle\text{BCS}|\mathrm{e}^{-\mathrm{i}\boldsymbol{x}\cdot\hat{\boldsymbol{P}}}\hat{H}|\text{BCS}\rangle\\
 & =\frac{1}{V}\int\mathrm{d}\boldsymbol{x}\,K(\boldsymbol{x}) + E_{0}
\end{align*}
$$

这里：

$$
\begin{align*}
K(\boldsymbol{x}) & =\langle\text{BCS}|(\mathrm{e}^{-\mathrm{i}\boldsymbol{x}\cdot\hat{\boldsymbol{P}}}-1)\hat{H}|\text{BCS}\rangle\\
 & =\langle\text{BCS}|\mathrm{e}^{-\mathrm{i}\boldsymbol{x}\cdot\hat{\boldsymbol{P}}}(\hat{H}-\mathrm{e}^{\mathrm{i}\boldsymbol{x}\cdot\hat{\boldsymbol{P}}})|\text{BCS}\rangle
\end{align*}
$$

现在，我们用 $\hat{K}=\sum_{i}k_{i}(\boldsymbol{x})\hat{K}_{i}$ 近似 $\hat{H}-\mathrm{e}^{\mathrm{i}\boldsymbol{x}\cdot\hat{\boldsymbol{P}}}$。
