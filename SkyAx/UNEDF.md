UNEDF 把相互作用写为：

$$
\mathcal{H}=\sum_{T=0,1}\mathcal{H}_{T}^{\text{even}}+\mathcal{H}_{T}^{\text{odd}}
$$

其中 Time even 项为：

$$
\begin{align*}
\mathcal{H}_{T}^{\text{even}}(\boldsymbol{r}) & =C_{T}^{\rho\rho}\rho_{T}^{2}+C_{T}^{\rho\tau}\rho_{T}\tau_{T}+C_{T}^{\boldsymbol{J}^{2}}\boldsymbol{J}_{T}^{2}\\
 & +C_{T}^{\rho\Delta\rho}\rho_{T}\Delta\rho_{T}+C_{T}^{\rho\nabla\cdot\boldsymbol{J}}\rho_{T}\nabla\cdot\boldsymbol{J}_{T}
\end{align*}
$$

Time odd 项为：

$$
\begin{align*}
\mathcal{H}_{T}^{\text{odd}} & =C_{T}^{\boldsymbol{s}^{2}}\boldsymbol{s}_{T}^{2}+C_{T}^{\boldsymbol{s}\cdot\Delta\boldsymbol{s}}\boldsymbol{s}_{T}\cdot\Delta\boldsymbol{s}_{T}+C_{T}^{\boldsymbol{s}\cdot\boldsymbol{T}}\boldsymbol{s}_{T}\cdot\boldsymbol{T}_{T}+C_{T}^{(\nabla\cdot\boldsymbol{s})^{2}}(\nabla\cdot\boldsymbol{s}_{T})^{2}\\
 & +C_{T}^{\boldsymbol{j}^{2}}\boldsymbol{j}_{T}^{2}+C_{T}^{\boldsymbol{s}\cdot\nabla\times\boldsymbol{j}}\boldsymbol{s}_{T}\cdot\nabla\times\boldsymbol{j}_{T}
\end{align*}
$$

其中 $T=\text{s}$ 表示 isoscalar 项，有 $\rho_{\text{s}}=\rho_{\text{p}}+\rho_{\text{n}}$。而 $T=\text{v}$ 表示 isovector 项，有 $\rho_{\text{v}}=\rho_{\text{n}}-\rho_{\text{p}}$。

这里 $C_{T}^{\rho\rho}$ 还和 isoscalar 密度有关：

$$
C_{T}^{\rho\rho}=C_{T0}^{\rho\rho}+C_{TD}^{\rho\rho}\rho_{\text{s}}^{\gamma}
$$

考虑：

$$
\frac{b_{0}}{2}\rho^{2}-\frac{b_{0}^{\prime}}{2}\sum_{t}\rho_{t}^{2}
$$

可以化为：

$$
\frac{b_{0}}{2}\rho_{\text{s}}^{2}-\frac{b_{0}^{\prime}}{4}(\rho_{\text{s}}^{2}+\rho_{\text{v}}^{2})=\left(\frac{b_{0}}{2}-\frac{b_{0}^{\prime}}{4}\right)\rho_{\text{s}}^{2}-\frac{b_{0}^{\prime}}{4}\rho_{\text{v}}^{2}
$$
利用 $(t, x)$ 参数即可得到：

$$
\frac{3}{8}t_{0}\rho_{\text{s}}^{2}-\frac{1}{4}t_{0}\left(\frac{1}{2}+x_{0}\right)\rho_{\text{v}}^{2}
$$

同理：
