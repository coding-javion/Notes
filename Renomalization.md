## 起源

重整化起源于量子场论中对发散的研究。

量子场论中很多费曼图的计算中含有动量从零到无穷大的积分，部分这样的积分是发散的。这些发散分红外发散和紫外发散，红外发散是零附近的积分即低动量部分导致的，紫外发散是积分到无穷大即高动量部分导致的。

对于这些发散，我们首先要有一个方式来判断其发散的程度，这就是正规化。正规化的最简单的例子就是截断正规化，例如将积分上限取为 $\Lambda$ ，然后通过积分关于 $\Lambda$ 的行为判断其发散程度。

红外发散不是相对论性量子场论的专利，在量子多体问题里算个电子气的库伦能也会遇到。其解决也比较简单，只需要采用某种正规化方式，就会发现计算中出现的无穷大互相抵消了，没什么困难。

紫外发散就没这么简单了，发散就在那里存在，根本抵消不了。为此，我们需要重整化这套框架。

## 框架

重整化框架是一套流程，这一套流程中有两个步骤具有很多种方案，一个是上面提到的正规化方案，另一个是重整化条件。

正规化的方式有很多种，在具体问题上可以选择不同的方式，例如上述提到的最简单的截断正规化，还有 Pauli-Villars 正规化和维数正规化。选取不同的正规化方案会导致计算难度上的巨大差别，但不会对最终结果产生影响，因为计算的最后我们都要取极限，例如会让积分上限 $\Lambda$ 趋于无穷。

所谓的重整化条件就是“强行”给出了一系列的条件，并证明只要你重新调整一下拉氏量中参数的大小，并满足这些条件，发散就能消失。重整化条件有在壳重整化条件，固定动量减除条件和 MS bar 重整化条件等。

为了了解这套流程，我们看一个最简单的例子，$\phi^{4}$ 理论，它是最简单相互作用量子场论之一，等价于伊辛模型：

$$
\mathscr{L}=\frac{1}{2}(\partial_{\mu}\phi)^{2}-\frac{1}{2}m^{2}\phi^{2}-\frac{\lambda_{0}}{4!}\phi^{4}
$$

为了简单，我们只看看耦合常数 $\lambda_{0}$ 的重整化。

在计算一圈图中的时候，我们会得到散射振幅为：

$$
\mathcal{M}=\frac12(\lambda_0)^2\int_0^1\mathrm{d}\alpha\int\frac{\mathrm{d}k}{(2\mathrm{\pi})^4}\frac1{(k^2-c^2+\mathrm{i}\varepsilon)^2}
$$

这里 $c^{2}=m^{2}-\alpha (1-\alpha) p^{2}$。一般来讲，加入我们采用的正规化方案里有一参数 $\varepsilon$，上述散射振幅的计算结果为 $\mathcal{M}=-\lambda_{0}^{2}V_{\varepsilon} (p^{2})$。

考虑了所有一阶二阶图后，散射振幅为：

$$
\mathrm{i}\mathcal{M}=-\mathrm{i}\lambda_0-\mathrm{i}\lambda_0^2\left[V_{\varepsilon}(s)+V_{\varepsilon}(t)+V_{\varepsilon}(u)\right]+O(\lambda_0^3)
$$

其中 $s, t, u$ 为 Mandelstam 不变量（就是散射前后的四动量加加减减后的平方）。

假如我们使用在壳重整化条件，它的其中一个条件为 $s=4 m^{2}, t=u=0$ 时令 $\mathrm{i}\mathcal{M}=-\mathrm{i}\lambda$，因此我们得到：

$$
-\mathrm{i}\lambda=-\mathrm{i}\lambda_{0}-\mathrm{i}\lambda_{0}^{2}[V_{\varepsilon}(4m^{2})+2V_{\varepsilon}(0)]+O(\lambda_0^3)
$$

其中 $\lambda$ 是新定义的耦合常数。由于 $V_{\varepsilon}$ 实际上是发散的，我们可以看出，$\lambda$ 和 $\lambda_{0}$ 必定有一个是发散的。由于我们想通过重定义来解决发散问题，因此我们只能让重定义后的 $\lambda$ 为有限值，而 $\lambda_{0}$ 因此就成了发散的值。

在这么定义后，我们可以进而定义 $\lambda+\delta\lambda=\lambda_{0}$，可以求得：

$$
-\mathrm{i}\delta\lambda=\mathrm{i}\lambda^{2}(V_{\varepsilon}(4m^{2})+2V_{\varepsilon}(0))+O(\lambda^3)
$$

于是原本的一项 $\frac{\lambda_{0}}{4!}\phi^{4}$ 被拆成了两项，$\frac{\lambda}{4!}\phi^{4}+\frac{\delta\lambda}{4!}\phi^{4}$，可以证明，后一项的第  $n$ 阶图恰好抵消了前一项的 $n+1$ 阶图中的发散。这是一件非常复杂的事，也不好证明。但我们可以首先看看最低阶的情况是什么情况，为此，我们需要具体的 $V_{\mu}(t)$ 的形式，因此需要考虑正规化方案，我们这里采用维数正规化（我们就不讲解维数正规化到底是什么了，大体上来讲，它相当于在被积函数上乘了个 $k^{-\varepsilon}$，因此会压低高动量部分），其计算的结果为：

$$
V_{\varepsilon}(p^2)=-\frac{1}{32\pi^2}\left(\frac2\epsilon+\int_0^1\mathrm{d}x\,\log\left(\frac{\mu^2}{m^2-x(1-x)p^2}\right)\right)
$$

维数正规化引入了两个参数 $\varepsilon$ 和 $\mu$，但 $\mu$ 是一个常数，为了得到最终结果我们只需令 $\varepsilon$ 趋于零，因此在维数正规化下发散项只是 $2/\varepsilon$。于是我们可以发现，原本的 $\lambda_{0}$ 的二阶项与 $\delta\lambda$ 的一阶项求和为：

$$
-\mathrm{i}\lambda^{2}[V_{\varepsilon}(s)+V_{\varepsilon}(t)+V_{\varepsilon}(u)-V_{\varepsilon}(4m^{2})-2V_{\varepsilon}(0)]
$$

发散项被完全抵消。大致上讲，进一步的证明就是说，每一个发散的关于 $\lambda$ 的图，都恰好对应一个关于 $\delta\lambda$ 的图，因此可以两两相消，最终的结果是收敛的。

## 重整化群和有效场论

经过上面一通操作，我们理论中的参数 $\lambda_{0}$ 变成了无穷大，但最终的结果成功变成了有限值。那么这么操作的物理意义是什么？这一问题由 Wilson 的重整化群理论给出了比较好的回答，并在 Weinberg 的有效场论框架下得到了进一步发展。

我们再来看这个式子：

$$
\mathrm{i}\mathcal{M}=-\mathrm{i}\lambda=-\mathrm{i}\lambda_{0}-\mathrm{i}\lambda_{0}^{2}[V_{\varepsilon}(4m^{2})+2V_{\varepsilon}(0)]+O(\lambda_0^3)
$$

这里散射振幅 $\mathcal{M}$ 是可以实验上测量的，因此是可以确定的，因此，$\lambda$ 才是实验物理学家真正关心的量，而 $\lambda_{0}$ 是一个随 $\varepsilon$ 变化的量，在 $\varepsilon$ 趋于零时发散，是非物理的，因此，其发散也就变得不那么奇怪了。耦合常数 $\lambda_{0}$ 的这种变化称为耦合常数跑动。



## 应用

### 计算兰姆位移

### 粗粒化

### 相似重整化群

### 局域化

### Cooper 对