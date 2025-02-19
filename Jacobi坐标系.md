## Jacobi 坐标

$A$ 体系统的 Jacobi 坐标可以写为：

$$
\begin{align*}
\boldsymbol{\xi}_{0}&=\sqrt{\frac{1}{A}}(\boldsymbol{x}_{1}+\boldsymbol{x}_{2}+\dots+\boldsymbol{x}_{A})\\\boldsymbol{\xi}_{k}&=\sqrt{\frac{k}{k+1}}\left[\frac{1}{k}\left(\boldsymbol{x}_{1}+\boldsymbol{x}_{2}+\dots+\boldsymbol{x}_{k}\right)-\boldsymbol{x}_{k+1}\right]\quad(k=1,\dots,A-1)
\end{align*}
$$

设变换矩阵为 $T$，即 $\boldsymbol{\xi}_i = T_{ij} \boldsymbol{x}_j$ 。具体计算可以证明 $T$ 是正交矩阵，即有 $T_{ij}T_{kj} = \delta_{ik}$ 。

令 Jacobi 坐标系下的动量为 $\boldsymbol{\pi}_k$，于是可以证明 $\boldsymbol{p}_{i}=T_{ji}\boldsymbol{\pi}_{j}$。

总角动量 $\boldsymbol{L}=\sum_{i}\boldsymbol{l}_i=\sum_{i}\boldsymbol{x}_{i}\times\boldsymbol{p}_{i}$ ，可以证明：

$$
\begin{align*}
\boldsymbol{L}&=\sum_{i}\boldsymbol{x}_{i}\times\boldsymbol{p}_{i}\\&=\sum_{i}T_{ji}T_{ki}\boldsymbol{\xi}_{j}\times\boldsymbol{\mathrm{\pi}}_{k}\\&=\sum_{k}\boldsymbol{\xi}_{k}\times\boldsymbol{\mathrm{\pi}}_{k}\\
&=\sum_{k}\boldsymbol{\lambda}_k
\end{align*}
$$
这里用 $\boldsymbol{\lambda}_{k}$ 表示 Jacobi 坐标系中的相对角动量。
