谱函数正规化为：

$$
\tilde{V}(q)=\frac{2}{\mathrm{\pi}}\int_{2m}^{\infty}\mathrm{d}\mu\,\mu\frac{\Im \tilde{V}(-\mathrm{i}\mu)}{\mu^{2}+q^{2}}
$$

做一次减除的谱函数正规化为：

$$
\tilde{V_{1}}(q)=-\frac{2q^{2}}{\mathrm{\pi}}\int_{2m}^{\infty}\mathrm{d}\mu\,\frac{\Im \tilde{V}(-\mathrm{i}\mu)}{\mu(\mu^{2}+q^{2})}
$$

可以证明，它们之间至多差一个一次多项式。因此将其 Fourier 变换回去，应该至多相差一个 $\delta$ 函数再加上一个 $\delta$ 函数的导数。

直接做 Fourier 逆变换得到：

$$
V(r)=\frac{1}{2\mathrm{\pi}^2}\int_{2m}^{\infty}\mathrm{d}\mu\,\mu\frac{\mathrm{e}^{-\mu r}}{r}\Im \tilde{V}(-\mathrm{i}\mu)
$$

接下来对一次减除的势做 Fourier 逆变换，利用 Fourier 变换的性质，可以得到动量空间的 $q^{2}$ 对应坐标空间的 $-\nabla^{2}$ ，再利用
$$
\nabla^{2}\left (\frac{\mathrm{e}^{-\mu r}}{r}\right)=-\mu^{2}\frac{\mathrm{e}^{-\mu r}}{r}
$$

即可得到

$$
V_{1}(r)=\frac{1}{2\mathrm{\pi}^{2}}\int_{2m}^{\infty}\mathrm{d}\mu\,\mu\frac{\mathrm{e}^{-\mu r}}{r}\Im \tilde{V}(-\mathrm{i}\mu)
$$

我们幸运的发现，他们不相差任何东西。