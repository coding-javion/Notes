在低密度极限下，把核物质考虑为多元理想经典气体，不同粒子间没有相互作用，但可以发生反应使得组分改变。

多元经典理想气体的哈密顿量为：

$$
H=\sum_{i}\frac{p_{i}^{2}}{2m_{i}}+h_{i}
$$

这里的 $i$ 指标为无视组分直接对不同粒子编码的指标，$m_{i},h_{i}$ 会根据粒子所属的组分自动变化。$h_{i}$ 为粒子内部自由度的哈密顿量。

由此我们可以写出系统的巨配分函数为：

$$
\Xi=\sum_{\{N_{i}\}}\mathrm{e}^{-\sum_{i}N_{i}\alpha_{i}}Z
$$

注意，这里用指标 $i$ 表示不同的组分，$N_{i}$ 表示该组分粒子个数，$\{N_{i}\}$ 表示不同组分粒子个数分布。由于是理想经典气体，可以有：

$$
Z=\prod_{i}\frac{1}{N_{i}!}Z_{1,i}^{N_{i}}
$$
因此可以计算：

$$
\begin{align*}\Xi & =\sum_{\{N_{i}\}}\prod_{i}\frac{1}{N_{i}!}\left(\mathrm{e}^{-\alpha_{i}}Z_{1,i}\right)^{N_{i}}\\
 & =\prod_{i}\sum_{N_{i}}\frac{1}{N_{i}!}\left(\mathrm{e}^{-\alpha_{i}}Z_{1,i}\right)^{N_{i}}\\
 & =\prod_{i}\exp\left(\mathrm{e}^{-\alpha_{i}}Z_{1,i}\right)
\end{align*}
$$

于是：

$$
\ln\Xi=\sum_{i}\mathrm{e}^{-\alpha_{i}}Z_{1,i}
$$
单粒子配分函数可以求出：

$$
\begin{align*}
Z_{1,i} & =\frac{V}{\lambda_{i}^{3}}\sum_{n}(2J_{in}+1)\mathrm{e}^{-\beta E_{in}}\\
 & \equiv\frac{V}{\lambda_{i}^{3}}g_{i}(T)
\end{align*}
$$


这里为了方便定义了 $g_{i}(T)$，其为内部自由度的配分函数，而 $V/\lambda_{i}^{3}$ 为整体自由度的配分函数。这里对 $n$ 求和为对所有基态激发态求和。

可以求得巨势为：

$$
\Omega(T,V,\mu_{i})=-TV\sum_{i}\frac{g_{i}}{\lambda_{i}^{3}}\exp\left(\frac{\mu_{i}}{T}\right)
$$

不同组分的粒子数密度可以给出：

$$
n_{i}=-\frac{1}{V}\left.\frac{\partial\Omega}{\partial\mu_{i}}\right|_{T,V,\mu_{j\neq i}}=\frac{g_{i}}{\lambda_{i}^{3}}\exp\left(\frac{\mu_{i}}{T}\right)
$$

由此得到：

$$
\mu_{i}=T\ln\left(\frac{n_{i}\lambda_{i}^{3}}{g_{i}}\right)
$$

对于任何一个反应，可以写为：

$$
\sum_{i}\nu_{i}A_{i}=0
$$
其中 $\nu_{i}$ 为反应方程式的系数，按照约定，生成物系数为正，反应物系数为负。$A_{i}$ 是相应的生成物或反应物。

在等温等压条件下，吉布斯函数理应达到最小值，此时假设发生一次反应，吉布斯函数的变化理应为 $0$：

$$
\Delta G=\sum_{i}\nu_{i}\mu_{i}=0
$$

由此得到了反应平衡条件。

根据反应平衡条件，可得：

$$
\sum_{i}\nu_{i}\ln\left(\frac{n_{i}\lambda_{i}^{3}}{g_{i}}\right)=0
$$
即：

$$
\prod_{i}n_{i}^{\nu_{i}}=K(T)\equiv\prod_{i}\left(\frac{g_{i}}{\lambda_{i}^{3}}\right)^{\nu_{i}}
$$
