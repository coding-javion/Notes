动能项这么近似的原因？

Thomas-Feimi理论把系统的能量写为粒子数密度的泛函：

$$
\begin{align*}
E=C_{K}\int[\rho(\boldsymbol{r})]^{\frac{5}{3}}\,\mathrm{d}\boldsymbol{r}+e\int\rho(\boldsymbol{r})v(\boldsymbol{r})\,\mathrm{d}\boldsymbol{r}+\frac{1}{2}e^{2}\int\frac{\rho(\boldsymbol{r})\rho(\boldsymbol{r}^{\prime})}{\left|\boldsymbol{r}-\boldsymbol{r}^{\prime}\right|}\,\mathrm{d}\boldsymbol{r}\mathrm{d}\boldsymbol{r}^{\prime}
\end{align*}
$$

该泛函的后两项十分自然，即经典的势能和相互作用能。但动能项的写出存在一定困难，有两种推导如下：

## 推导1

近似考虑将一个处于平衡态的系统分成许多小块儿，每份体积为$\Delta V$，在这个体积内有$\Delta N$个粒子（不同小份中可能不同），并且我们假设这些粒子在这些小块儿中的行为就好像在同样大小盒子里的独立费米子。

我们由此可以直接得到：

$$
\begin{align*}
\Delta N=\frac{4\mathrm{\pi}}{3}k_{F}^{3}\cdot\frac{V}{4\mathrm{\pi}^{3}}
\end{align*}
$$

由此我们得到粒子数密度和费米动量的关系：

$$
\begin{align*}
\rho=\frac{\Delta N}{\Delta V}=\frac{k_{F}^{3}}{3\mathrm{\pi}^{2}}
\end{align*}
$$

该盒子内的动能密度为：

$$
\begin{align*}
t=\frac{\Delta T}{\Delta V}=\int_{0}^{k_{F}}\frac{\hbar^{2}}{2m}k^{2}\cdot\frac{k^{2}}{\mathrm{\pi}^{2}}\,\mathrm{d}k=\frac{\hbar^{2}}{10m\mathrm{\pi}^{2}}k_{F}^{5}
\end{align*}
$$

考虑所有的小块儿，即得到：

$$
\begin{align*}
t(\boldsymbol{r})=\frac{3\hbar^{2}}{10m}(3\mathrm{\pi}^{2})^{2/3}(\rho(\boldsymbol{r}))^{5/3}
\end{align*}
$$

因此我们得到：

$$
\begin{align*}
T[\rho]=C_{K}\int\rho(\boldsymbol{r})^{5/3}\,\mathrm{d}\boldsymbol{r}
\end{align*}
$$

其中：

$$
C_{K}=\frac{3\hbar^2}{10m}(3\mathrm{\pi}^{2})^{2/3}
$$

## 推导2

定义：

$$
\begin{align*}
\rho(\boldsymbol{r}_{1},\boldsymbol{r}_{2})=2\sum_{i}\phi_{i}(\boldsymbol{r}_{1})\phi_{i}^{*}(\boldsymbol{r}_{2})
\end{align*}
$$

则动能项可以写为：

$$
\begin{align*}
T[\rho]=\int[-\frac{\hbar^{2}}{2m}\nabla_{1}^{2}\rho(\boldsymbol{r}_{1},\boldsymbol{r}_{2})]_{\boldsymbol{r}_{2}=\boldsymbol{r}_{1}}\mathrm{d}\boldsymbol{r}_{1}
\end{align*}
$$

考虑：

$$
\begin{align*}
\psi_{\boldsymbol{k}}(\boldsymbol{r})=\frac{1}{\sqrt{V}}\mathrm{e}^{\mathrm{i}\boldsymbol{k}\cdot\boldsymbol{r}}
\end{align*}
$$

于是有：

$$
\begin{align*}
\rho(\boldsymbol{r}_{1},\boldsymbol{r}_{2})=\frac{2}{V}\sum_{\boldsymbol{k}}\mathrm{e}^{\mathrm{i}\boldsymbol{k}\cdot(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})}
\end{align*}
$$

这里只对占据态求和。如果占据的态足够多，可以近似用积分替代：

$$
\begin{align*}
\rho(\boldsymbol{r}_{1},\boldsymbol{r}_{2})=\frac{1}{4\mathrm{\pi}^{3}}\int\mathrm{e}^{\mathrm{i}\boldsymbol{k}\cdot(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})}\,\mathrm{d}\boldsymbol{k}
\end{align*}
$$

我们用$\rho(\boldsymbol{r})$表示$\rho(\boldsymbol{r},\boldsymbol{r})$，可以计算得：

$$
\begin{align*}
\rho(\boldsymbol{r})=\frac{k_{F}^{3}}{3\mathrm{\pi}^{2}}
\end{align*}
$$

需要注意的是，这里的$k_{F}$是$\boldsymbol{r}$的函数。

我们一般不用$\boldsymbol{r}_{1}$和$\boldsymbol{r}_{2}$来计算，而是利用：

$$
\begin{align*}
\boldsymbol{r}=\frac{1}{2}(\boldsymbol{r}_{1}+\boldsymbol{r}_{2})\qquad\boldsymbol{s}=\boldsymbol{r}_{1}-\boldsymbol{r}_{2}
\end{align*}
$$

可以计算得：

$$
\begin{align*}
\rho(\boldsymbol{r},\boldsymbol{s})=\rho(\boldsymbol{r}_{1},\boldsymbol{r}_{2})=3\rho(\boldsymbol{r})\left[\frac{\sin t-t\cos t}{t^{3}}\right]_{t=k_{F}s}
\end{align*}
$$

利用：

$$
\begin{align*}
\nabla_{1}^{2}=\frac{1}{4}\nabla_{\boldsymbol{r}}^{2}+\nabla_{\boldsymbol{s}}^{2}+\nabla_{\boldsymbol{r}}\nabla_{\boldsymbol{s}}
\end{align*}
$$

得：

$$
\begin{align*}
[\nabla_{1}^{2}\rho(\boldsymbol{r}_{1},\boldsymbol{r}_{2})]_{\boldsymbol{r}_{2}=\boldsymbol{r}_{1}}=\frac{1}{4}\nabla_{\boldsymbol{r}}^{2}\rho(\boldsymbol{r})-\frac{3}{5}(3\mathrm{\pi}^{2})^{2/3}(\rho(\boldsymbol{r}))^{5/3}
\end{align*}
$$

对于我们考虑的大多数情况，有：

$$
\begin{align*}
\int\nabla^{2}\rho(\boldsymbol{r})\,\mathrm{d}\boldsymbol{r}=0
\end{align*}
$$

因此我们得到：

$$
\begin{align*}
T[\rho]=C_{K}\int\rho(\boldsymbol{r})^{5/3}\,\mathrm{d}\boldsymbol{r}
\end{align*}
$$

其中：

$$
C_{K}=\frac{3\hbar^2}{10m}(3\mathrm{\pi}^{2})^{2/3}
$$

## Thomas-Feimi方程

我们考虑在约束条件：

$$
\begin{align*}
\int\rho(\boldsymbol{r})\,\mathrm{d}\boldsymbol{r}=N
\end{align*}
$$

下求得能量极小值：

$$
\begin{align*}
\delta(E-\mu N)=\int\left\{ \frac{5}{3}C_{K}[\rho(\boldsymbol{r})]^{\frac{2}{3}}+ev(\boldsymbol{r})+e^{2}\int\frac{\rho(\boldsymbol{r}^{\prime})}{\left|\boldsymbol{r}-\boldsymbol{r}^{\prime}\right|}\,\mathrm{d}\boldsymbol{r}^{\prime}-\mu\right\} \delta\rho(\boldsymbol{r})\,\mathrm{d}\boldsymbol{r}=0
\end{align*}
$$

于是得到：

$$
\frac{5}{3}C_{K}[\rho(\boldsymbol{r})]^{\frac{2}{3}}+ev(\boldsymbol{r})+e^{2}\int\frac{\rho(\boldsymbol{r}^{\prime})}{\left|\boldsymbol{r}-\boldsymbol{r}^{\prime}\right|}\,\mathrm{d}\boldsymbol{r}^{\prime}=\mu
$$

这就是 Thomas-Feimi 方程。

如果我们引入 $u(\boldsymbol{r})$，令 $\rho(\boldsymbol{r})$ 满足 Poisson 方程：

$$
\begin{align*}
\nabla^{2}u(\boldsymbol{r})=-4\mathrm{\pi}e\rho(\boldsymbol{r})
\end{align*}
$$

还可以得到微分方程形式的 Thomas-Feimi 方程：

$$
\begin{align*}
\nabla^{2}u(\boldsymbol{r})=-\frac{4e}{3\mathrm{\pi}\hbar^{3}}(2m)^{3/2}(\mu-ev(\boldsymbol{r})-eu(\boldsymbol{r}))^{3/2}
\end{align*}
$$
