Skyrme 相互作用由两体部分和三体部分组成：

$$
V=v^{(2)}+v^{(3)}
$$

两体部分分为局域的和非局域的：

$$
v^{(2)}=v_{\text{loc}}^{(2)}+v_{\text{nloc}}^{(2)}
$$

首先考虑局域部分。为了简单我们暂时只考虑坐标空间，考虑核力的平移不变性，我们可以把核力表示为 $\langle\boldsymbol{r}^{\prime}|v|\boldsymbol{r}\rangle$，又由于这一部分是局域的，得到 $\langle\boldsymbol{r}^{\prime}|v|\boldsymbol{r}\rangle=\delta (\boldsymbol{r}^{\prime}-\boldsymbol{r}) v (\boldsymbol{r})$，再考虑空间转动不变性，即得 $v (\boldsymbol{r})=v (r)$。因此内积 $\langle\psi^{\prime}|v|\psi\rangle$ 写到坐标空间即为：

$$
\langle\psi^{\prime}|v|\psi\rangle=\int\psi^{\prime*}(\boldsymbol{r})v(r)\psi(\boldsymbol{r})\,\mathrm{d}\boldsymbol{r}
$$

利用 Taylor 展开，我们得到：

$$
\begin{align*}
\langle\psi^{\prime}|v|\psi\rangle & =\int(1+\boldsymbol{r}\cdot\nabla+\frac{1}{2}(\boldsymbol{r}\cdot\nabla)^{2}+\dots)\psi^{\prime*}|_{\boldsymbol{r}=\boldsymbol{0}}v(r)(1+\boldsymbol{r}\cdot\nabla+\frac{1}{2}(\boldsymbol{r}\cdot\nabla)^{2}+\dots)\psi|_{\boldsymbol{r}=\boldsymbol{0}}\,\mathrm{d}\boldsymbol{r}\\
 & =\int\psi^{\prime*}(\boldsymbol{0})v(r)\psi(\boldsymbol{0})\,\mathrm{d}\boldsymbol{r}+\int(\boldsymbol{r}\cdot\nabla)\psi^{\prime*}|_{\boldsymbol{r}=\boldsymbol{0}}v(r)(\boldsymbol{r}\cdot\nabla)\psi|_{\boldsymbol{r}=\boldsymbol{0}}\,\mathrm{d}\boldsymbol{r}\\
 & +\int(\boldsymbol{r}\cdot\nabla)^{2}\psi^{\prime*}|_{\boldsymbol{r}=\boldsymbol{0}}v(r)\psi|_{\boldsymbol{r}=\boldsymbol{0}}\,\mathrm{d}\boldsymbol{r}+\int\psi^{\prime*}|_{\boldsymbol{r}=\boldsymbol{0}}v(r)(\boldsymbol{r}\cdot\nabla)^{2}\psi|_{\boldsymbol{r}=\boldsymbol{0}}\,\mathrm{d}\boldsymbol{r}+\dots
\end{align*}
$$

这里一阶项消失是因为被积函数是 $\boldsymbol{r}$ 的奇函数。基于同样的原因，我们可以得到：

$$
\int r_{i}r_{j}v(r)\,\mathrm{d}\boldsymbol{r}=\frac{\delta_{ij}}{3}\int r^{2}v(r)\,\mathrm{d}\boldsymbol{r}
$$

由此，我们定义令：

$$
\begin{align*}
v_{0} & =\int v(r)\,\mathrm{d}\boldsymbol{r}\\
v_{2} & =\frac{1}{3}\int r^{2}v(r)\,\mathrm{d}\boldsymbol{r}
\end{align*}
$$

得到：

$$
\langle\psi^{\prime}|v|\psi\rangle=\int\psi^{\prime*}(\boldsymbol{r})(v_{0}\delta(\boldsymbol{r})+\frac{v_{2}}{2}(\overleftarrow{\nabla}^{2}+\overrightarrow{\nabla}^{2}+2\overleftarrow{\nabla}\overrightarrow{\nabla})+\dots)\psi(\boldsymbol{r})\,\mathrm{d}\boldsymbol{r}
$$

对比可得：

$$
v(r)=v_{0}\delta(\boldsymbol{r})+\frac{v_{2}}{2}(\overleftarrow{\nabla}^{2}+\overrightarrow{\nabla}^{2}+2\overleftarrow{\nabla}\overrightarrow{\nabla})\delta(\boldsymbol{r})+\dots
$$

skyrme 势的形式为：

$$
\begin{align*}
V^{(2)}= & t_{0}(1+x_{0}P_{\sigma})\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})\\
 & +\frac{1}{2}t_{1}(\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})k^{2}+k^{\prime2}\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2}))\\
 & +t_{2}\boldsymbol{k}^{\prime}\cdot\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})\boldsymbol{k}+\mathrm{i}W_{0}(\boldsymbol{\sigma}_{1}+\boldsymbol{\sigma}_{2})\cdot(\boldsymbol{k}^{\prime}\times\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})\boldsymbol{k})\\
V^{(3)}= & t_{3}\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})\delta(\boldsymbol{r}_{2}-\boldsymbol{r}_{3})
\end{align*}
$$

这里带指标 $1,2$ 意味着是算符，例如：

$$
\begin{align*}
\langle s_{i}^{\prime}s_{j}^{\prime}|\boldsymbol{\sigma}_{1}\cdot\boldsymbol{\sigma}_{2}|s_{i}s_{j}\rangle & =\sum_{k}[\sigma_{k}]_{s_{i}^{\prime}s_{i}}[\sigma_{k}]_{s_{j}^{\prime}s_{j}}\\
(\langle s_{i}^{\prime}s_{j}^{\prime}|\boldsymbol{\sigma}_{1}+\boldsymbol{\sigma}_{2}|s_{i}s_{j}\rangle)_{k} & =[\sigma_{k}]_{s_{i}^{\prime}s_{i}}+[\sigma_{k}]_{s_{j}^{\prime}s_{j}}\\
\langle\boldsymbol{r}_{i}^{\prime}\boldsymbol{r}_{j}^{\prime}|\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})|\boldsymbol{r}_{i}\boldsymbol{r}_{j}\rangle & =\delta(\boldsymbol{r}_{i}^{\prime}-\boldsymbol{r}_{i})\delta(\boldsymbol{r}_{j}^{\prime}-\boldsymbol{r}_{j})\delta(\boldsymbol{r}_{i}-\boldsymbol{r}_{j})\\
\langle\boldsymbol{r}_{i}^{\prime}\boldsymbol{r}_{j}^{\prime}|\nabla_{1}-\nabla_{2}|\boldsymbol{r}_{i}\boldsymbol{r}_{j}\rangle & =\delta(\boldsymbol{r}_{i}^{\prime}-\boldsymbol{r}_{i})\delta(\boldsymbol{r}_{j}^{\prime}-\boldsymbol{r}_{j})(\nabla_{i}-\nabla_{j})
\end{align*}
$$

在动量表象下：

$$
(2\mathrm{\pi})^{3}\langle\boldsymbol{k}^{\prime}|V^{(2)}|\boldsymbol{k}\rangle=t_{0}(1+x_{0}P_{\sigma})+\frac{1}{2}t_{1}(k^{2}+k^{\prime2})+t_{2}\boldsymbol{k}^{\prime}\cdot\boldsymbol{k}+\mathrm{i}W_{0}(\boldsymbol{\sigma}_{1}+\boldsymbol{\sigma}_{2})\cdot(\boldsymbol{k}^{\prime}\times\boldsymbol{k})
$$