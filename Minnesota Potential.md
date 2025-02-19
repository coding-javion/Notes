Minnesota 势的形式为：

$$
V(r)=\frac{1}{2}\left(V_{R}(r)+\frac{1}{2}(1+P_{12}^{\sigma})V_{T}(r)+\frac{1}{2}(1-P_{12}^{\sigma})V_{S}(r)\right)(1-P_{12}^{\sigma}P_{12}^{\tau})
$$

其中 $V_{\alpha}(r)=V_{\alpha}\exp (-\alpha r^{2})$。$P_{12}^{\sigma}=(1+\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2})/2$ 是自旋交换算符，$P_{12}^{\tau}=(1+\boldsymbol{\tau}_{1}\cdot\boldsymbol{\tau}_{2})/2$ 是同位旋交换算符。

利用：

$$
V(q)=\frac{1}{(2\mathrm{\pi})^{3}}\int\mathrm{d}\boldsymbol{r}\,\mathrm{e}^{-\mathrm{i}\boldsymbol{q}\cdot\boldsymbol{r}}V(r)
$$

可得其在动量空间的形式为：

$$
V(q)=\frac{1}{2}\left(V_{\text{R}}(q)+\frac{1}{2}(1+P_{12}^{\sigma})V_{\text{T}}(q)+\frac{1}{2}(1-P_{12}^{\sigma})V_{\text{S}}(q)\right)(1-P_{12}^{\sigma}P_{12}^{\tau})
$$

其中，每一个 $V_{\alpha}(r)$ 都变成了 $V_{\alpha}(q)$。可以求得 $V_{\alpha}(q)$ 的形式为：

$$
\begin{align*}
V_{\alpha}(q) =\frac{V_{\alpha}}{(2\mathrm{\pi})^{3}}\left(\frac{\mathrm{\pi}}{\alpha}\right)^{\frac{3}{2}}\exp\left(-\frac{q^{2}}{4\alpha}\right)
\end{align*}
$$

接下来将 Minnesota 势的进行标准的分解。首先把交换算符都替换成 $\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2}$ 和 $\boldsymbol{\tau}_{1}\cdot\boldsymbol{\tau_{2}}$，再利用 $(\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2})^{2}=3-2\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2}$，将 $\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2}$ 的二次项转化为一次项，即可得到：

$$
\begin{align*}V(q) & =\left[\frac{3V_{\text{R}}(q)}{8}+\frac{3V_{\text{S}}(q)}{16}+\frac{3V_{\text{T}}(q)}{16}+\left(-\frac{V_{\text{R}}(q)}{8}+\frac{V_{\text{S}}(q)}{16}-\frac{3V_{\text{T}}(q)}{16}\right)(\boldsymbol{\tau}_{1}\cdot\boldsymbol{\tau}_{2})\right]\\
 & +\left[-\frac{V_{\text{R}}(q)}{8}-\frac{3V_{\text{S}}(q)}{16}+\frac{V_{\text{T}}(q)}{16}+\left(-\frac{V_{\text{R}}(q)}{8}-\frac{V_{\text{S}}(q)}{16}-\frac{V_{\text{T}}(q)}{16}\right)(\boldsymbol{\tau}_{1}\cdot\boldsymbol{\tau}_{2})\right]\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2}
\end{align*}
$$

利用 Mathematica 计算即可。

```Mathematica
P[x_] = (1 + x)/2;
Collect[Expand[Expand[1/2(VR + 1/2 (1 + P[σ]) VT + 1/2 (1 - P[σ]) VS) (1 - P[σ] P[τ])] //. σ^2 -> 3 - 2 σ], {σ, τ}]
```

上面用到的公式证明如下：

$$
\begin{align*}
(\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2})^{2} & =\sigma_{i}^{1}\sigma_{j}^{1}\sigma_{i}^{2}\sigma_{j}^{2}\\
 & =(\delta_{ij}+\mathrm{i}\sum_{k}\varepsilon_{ijk}\sigma_{k}^{1})(\delta_{ij}+\mathrm{i}\sum_{l}\varepsilon_{ijl}\sigma_{l}^{2})\\
 & =3-2\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2}
\end{align*}
$$

