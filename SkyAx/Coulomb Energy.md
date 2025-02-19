库仑能按理来说不能精确计算，但是对于原子核来讲，库仑能的精确计算不甚重要，因此我们只需采用Hartree-Fock近似即可，即认为 $E_{\text{coul}}=E_{\text{coul-h}}+E_{\text{coul-f}}$，其中 Hartree 项为：

$$
E_{\text{coul-h}}=\int\frac{\rho(\boldsymbol{r})\rho(\boldsymbol{r})}{|\boldsymbol{r}-\boldsymbol{r}^{\prime}|}\,\mathrm{d}\boldsymbol{r}\mathrm{d}\boldsymbol{r}^{\prime}
$$

这里 $\rho (\boldsymbol{r})$ 是质子密度分布。由于我们只考虑质子不涉及同位旋，因此 Fock 项为：

$$
E_{\text{coul-f}}=\frac{e^2}{2}\sum_{ij}\sum_{s_{1}s_{2}}\int\frac{\psi_{i}^{*}(\boldsymbol{r}_{1},s_{1})\psi_{j}^{*}(\boldsymbol{r}_{2},s_{2})\psi_{j}(\boldsymbol{r}_{1},s_{1})\psi_{i}(\boldsymbol{r}_{2},s_{2})}{\left|\boldsymbol{r}_{1}-\boldsymbol{r}_{2}\right|}\,\mathrm{d}\boldsymbol{r}_{1}\mathrm{d}\boldsymbol{r}_{2}
$$

Fock 项不能表示直接表示成密度的函数，但我们可以近似将其表示成密度的函数。考虑到原子核内密度大体上是均匀的，因此我们采用类似 Thomas-Fermi 的处理：把原子核分成块儿，每一块儿用费米气体模型即能考虑到大部分的交换库仑能，费米气体模型里有：

$$
\psi_{i}(\boldsymbol{r},s)=\frac{1}{\sqrt{V}}\mathrm{e}^{\mathrm{i}\boldsymbol{k}_{i}\cdot\boldsymbol{r}}\delta_{s_{i}s}
$$

由 Fermi 气体模型，对 $i, j$ 的求和变为：

$$
\sum_{ij}\rightarrow\frac{V}{(2\mathrm{\pi})^{3}}\sum_{ss^{\prime}}\int^{k_{\text{F}}}\mathrm{d}\boldsymbol{k}\mathrm{d}\boldsymbol{k}^{\prime}
$$
消去所有的自旋求和，得到 Fock 项可以写为：

$$
E_{\text{coul-f}}=\frac{e^{2}V}{(2\mathrm{\pi})^{3}}\int^{k_{\text{F}}}\frac{\mathrm{e}^{\mathrm{i}\boldsymbol{k}\cdot(\boldsymbol{r}_{2}-\boldsymbol{r}_{1})}\mathrm{e}^{\mathrm{i}\boldsymbol{k}^{\prime}\cdot(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})}}{\left|\boldsymbol{r}_{1}-\boldsymbol{r}_{2}\right|}\,\mathrm{d}\boldsymbol{k}\mathrm{d}\boldsymbol{k}^{\prime}\mathrm{d}\boldsymbol{r}_{1}\mathrm{d}\boldsymbol{r}_{2}
$$

上式可以计算出来，得：

$$
E_{\text{coul-f}}=-\frac{e^{2}}{4\mathrm{\pi}^{3}}(3\mathrm{\pi}^{2})^{4/3}\rho^{4/3}V
$$

如果把所有的小块儿加起来，就得到：

$$
E_{\text{coul-f}}=-\frac{e^{2}}{4\mathrm{\pi}^{3}}(3\mathrm{\pi}^{2})^{4/3}\int\rho^{4/3}(\boldsymbol{r})\,\mathrm{d}\boldsymbol{r}
$$

Hartree项可以等价的写为：

$$
E_{\text{coul-h}}=\int\rho(\boldsymbol{r})v_{\text{ave}}(\boldsymbol{r})\,\mathrm{d}\boldsymbol{r}
$$

其中：

$$
v_{\text{ave}}(\boldsymbol{r})=\int v_{\text{coul}}(\boldsymbol{r}-\boldsymbol{r}^{\prime})\rho(\boldsymbol{r}^{\prime})\,\mathrm{d}\boldsymbol{r}
$$
这里：

$$
v_{\text{coul}}(\boldsymbol{r}-\boldsymbol{r}^{\prime})=\frac{1}{|\boldsymbol{r}-\boldsymbol{r}^{\prime}|}
$$

这相当于是个卷积，而用 FFT 能加速卷积的运算，因此我们考虑使用 FFT 计算。有两种方案：

第一种，解析地做 Fourier 变换，得到：

$$
v_{\text{ave}}(\boldsymbol{r})=\frac{1}{(2\mathrm{\pi})^{3}}\int v_{\text{coul}}(\boldsymbol{k})\rho(\boldsymbol{k})\mathrm{e}^{\mathrm{i}\boldsymbol{k}\cdot\boldsymbol{r}}\,\mathrm{d}\boldsymbol{r}
$$

于是可以数值的对 $\rho (\boldsymbol{r})$   做 Fourier 变换，然后乘上 $v (\boldsymbol{k})$ 后做逆变换。

但是这一方法有严重的问题，即对于 $\boldsymbol{k}=0$ 的点，$v_{\text{coul}}(\boldsymbol{k})$ 是发散的，如果离散的求和，这一发散值会导致无穷大的产生。

第二种，数值的考虑，上述积分就是：

$$
v_{\text{ave},n}=d^{3}\sum_{m}v_{\text{coul},n-m}\rho_{m}
$$
其中 $n, m$ 表示格点，$d$ 表示格距。

利用离散 Fourier 变换的卷积定理 [[Discrete Fourier Transform]]，我们有：

$$
v_{\text{ave},n}=\frac{d^3}{N}\sum_{k}v_{\text{coul},k}\rho_{k}\mathrm{e}^{\mathrm{i}\frac{2\mathrm{\pi}}{N}kn}
$$

然而，卷积定理假设了势场是周期势，显然实际上并不如此。但是考虑到原子核的密度在边界上应该接近于零，因此我们应当可以把势场替换为周期势而没有很大的影响。