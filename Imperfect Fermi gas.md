我们现在仔细考虑稀疏的硬核（有短程强排斥芯的[^1]）费米气。理论基于如下的观察：某些相互作用势尽管非常强且具有奇点，但相应的散射振幅依然可能很小。 [[#附录1]] 说明了上述论点。

尽管相互作用势是奇异的，稀疏费米气仍然有一个非常小的参数 $k_{\text{F}}a$，这里 $a$ 是散射长度。于是我们可以把基态能量


## 附录 1

我们考虑一个简单的无限高方势垒的散射问题，如果势垒半径为 $a$，则可以得到散射振幅为：

$$
f(k,\theta)=\sum_{l=0}^{\infty}\frac{2l+1}{k}\mathrm{e}^{\mathrm{i}\delta_{l}}\sin\delta_{l}P_{l}(\cos\theta)
$$

其中相移在 $ka\rightarrow0$ 时为：

$$
\begin{cases}
\delta_{l}(k)=-\frac{(ka)^{2l+1}}{(2l+1)!!(2l-1)!!} & l>0\\
\delta_{0}(k)=-ka & l=0
\end{cases}
$$

可以看出，$ka\rightarrow0$ 时也有 $f(k,\theta)\rightarrow0$。

更一般的，我们利用表达式：

$$
f(\boldsymbol{k}^{\prime},\boldsymbol{k})=-\frac{m}{2\mathrm{\pi}\hbar^{2}}\int\mathrm{d}^{3}\boldsymbol{x}\,\mathrm{e}^{-\mathrm{i}\boldsymbol{k}^{\prime}\cdot\boldsymbol{x}}V(\boldsymbol{x})\psi_{\boldsymbol{k}}^{+}(\boldsymbol{x})
$$

可以看出，由于在硬核中波函数振幅为 $0$，因此整个散射振幅依然可以为有限值。[^2]

[^1]: 任何现实的势都必须具有排斥芯，否则不会有平衡密度，系统会坍缩。此外需要强调的是，这里的势能没有任何吸引作用。
[^2]: 似乎有点奇怪。