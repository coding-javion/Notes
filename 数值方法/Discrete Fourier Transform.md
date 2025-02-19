对于 $N$ 点序列 $f_{n}$，$n=0,\dots, N-1$，离散 Fourier 变换（DFT）的正变换为：

$$
\tilde{f}_{k}=\sum_{n=0}^{N-1}\mathrm{e}^{-\mathrm{i}\frac{2\mathrm{\pi}}{N}nk}f_{n}
$$
这里 $k=0,\dots, N-1$。离散 Fourier 变换的逆变换为：

$$
f_{n}=\frac{1}{N}\sum_{k=0}^{N-1}\mathrm{e}^{\mathrm{i}\frac{2\mathrm{\pi}}{N}nk}\tilde{f}_{k}
$$

这里的系数 $1/N$ 并不重要，只需正变换逆变换系数相乘为 $1/N$ 即可。

定理 1：

$$
\begin{align*}
\mathcal{F}(\mathrm{e}^{\mathrm{i}\frac{2\mathrm{\pi}}{N}nk_{0}}f_{n}) & =\sum_{n=0}^{N-1}\mathrm{e}^{-\mathrm{i}\frac{2\mathrm{\pi}}{N}n(k-k_{0})}f_{n}\\
 & =\tilde{f}_{k-k_{0}}
\end{align*}
$$

这里 $k$ 依然取 $0,\dots, N-1$，令 $k^{\prime}=k-k_{0}$，对于 $k^{\prime}<0$ 或者 $k^{\prime}\geq N$，我们定义：

$$
\tilde{f}_{k^{\prime}}=\tilde{f}_{k^{\prime}\ \text{mod}\ N}
$$

相当于把 $\tilde{f}_{k}$ 拓展成了周期的。

定理 2：

$$
\begin{align*}
\mathcal{F}(f_{n-n_{0}}) & =\sum_{n=0}^{N-1}\mathrm{e}^{-\mathrm{i}\frac{2\mathrm{\pi}}{N}nk}f_{n-n_{0}}\\
 & =\mathrm{e}^{-\mathrm{i}\frac{2\mathrm{\pi}}{N}n_{0}k}\sum_{n=0}^{N-1}\mathrm{e}^{-\mathrm{i}\frac{2\mathrm{\pi}}{N}(n-n_{0})k}f_{n-n_{0}}\\
 & =\mathrm{e}^{-\mathrm{i}\frac{2\mathrm{\pi}}{N}n_{0}k}\sum_{n^{\prime}=-n_{0}}^{N-n_{0}-1}\mathrm{e}^{-\mathrm{i}\frac{2\mathrm{\pi}}{N}n^{\prime}k}f_{n^{\prime}}\\
 & =\mathrm{e}^{-\mathrm{i}\frac{2\mathrm{\pi}}{N}n_{0}k}\sum_{n^{\prime}=0}^{N-1}\mathrm{e}^{-\mathrm{i}\frac{2\mathrm{\pi}}{N}n^{\prime}k}f_{n^{\prime}}\\
 & =\mathrm{e}^{-\mathrm{i}\frac{2\mathrm{\pi}}{N}n_{0}k}\tilde{f}_{k}
\end{align*}
$$

这里证明的第 4 个等号相当于假设了 $f_{n}$ 是以 $N$ 为周期的函数。

卷积公式：

$$
\begin{align*}
\mathcal{F}(\sum_{m=0}^{M-1}f_{n-m}g_{m}) & =\sum_{n=0}^{N-1}\sum_{m=0}^{M-1}\mathrm{e}^{-\mathrm{i}\frac{2\mathrm{\pi}}{N}nk}f_{n-m}g_{m}\\
 & =\tilde{f}_{k}\sum_{m=0}^{M-1}\mathrm{e}^{-\mathrm{i}\frac{2\mathrm{\pi}}{N}mk}g_{m}\\
 & =\tilde{f}_{k}\tilde{g}_{k}
\end{align*}
$$

这里由于利用了上面的定理 2，因此也相当于假设了 $f_{n}$ 的周期性。