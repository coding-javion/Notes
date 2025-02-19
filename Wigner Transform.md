---
date created: 2023-02-04 10:07
related:
  - "[[Density Matrix]]"
---



## Wigner 函数

Wigner 变换把算符变换到相空间，从而得到量子力学的相空间表述。

任意一个算符 $A$ 的 Wigner 变换是：

$$
A_{\text{w}}(x,p)=\int\mathrm{e}^{-\mathrm{i}py/\hbar}\langle x+\frac{y}{2}|A|x-\frac{y}{2}\rangle\,\mathrm{d}y
$$

我们也可以做「逆变换」，不过得到的结果是矩阵元[^1]：

$$
\frac{1}{2\mathrm{\pi}\hbar}\int A_{\text{w}}(\frac{x+x^{\prime}}{2},p)\mathrm{e}^{\mathrm{i}p(x-x^{\prime})/\hbar}\,\mathrm{d}p=A(x,x^{\prime})
$$

证明只需要直接的计算：

$$
\begin{aligned} \text{L.H.S}=& \frac{1}{2\mathrm{\pi}\hbar}\int\mathrm{e}^{-\mathrm{i}py/\hbar}\langle\frac{x+x^{\prime}}{2}+\frac{y}{2}|A|\frac{x+x^{\prime}}{2}-\frac{y}{2}\rangle\mathrm{e}^{\mathrm{i}p(x-x^{\prime})/\hbar}\,\mathrm{d}p\,\mathrm{d}y\\
= & \int\langle\frac{x+x^{\prime}}{2}+\frac{y}{2}|A|\frac{x+x^{\prime}}{2}-\frac{y}{2}\rangle\delta(x-x^{\prime}-y)\,\mathrm{d}y\\
= & \langle x|A|x^{\prime}\rangle\\
= & A(x,x^{\prime})=\text{R.H.S}
\end{aligned}
$$

密度矩阵 $\rho$ 的 Wigner 变换可以记作 $f_{\text{w}}(x, p)$，称作 Wigner 函数。由逆变换的存在我们知道 Wigner 函数和密度矩阵包含相同的信息。事实上，我们可以得到：

$$
\frac{1}{2\mathrm{\pi}\hbar}\int f_{\text{w}}(x,p)A_\text{w}(x,p)\,\mathrm{d}x\,\mathrm{d}p=\mathop{\mathrm{Tr}}\rho A
$$

证明只需要直接的计算：

$$
\begin{aligned}
&\frac{1}{2\mathrm{\pi}\hbar}\int\mathrm{e}^{-\mathrm{i}py/\hbar}\langle x+\frac{y}{2}|\rho|x-\frac{y}{2}\rangle\mathrm{e}^{-\mathrm{i}pz/\hbar}\langle x+\frac{z}{2}|A|x-\frac{z}{2}\rangle\,\mathrm{d}p\,\mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z\\
=&\int\langle x+\frac{y}{2}|\rho|x-\frac{y}{2}\rangle\langle x+\frac{z}{2}|A|x-\frac{z}{2}\rangle\delta(y+z)\,\,\mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z\\
=&	\int\langle x+\frac{y}{2}|\rho|x-\frac{y}{2}\rangle\langle x-\frac{y}{2}|A|x+\frac{y}{2}\rangle\,\mathrm{d}x\,\mathrm{d}y\\
=&	\int\langle y|\rho|x\rangle\langle x|A|y\rangle\,\mathrm{d}x\,\mathrm{d}y\\
=&	\mathop{\mathrm{Tr}}\rho A
\end{aligned}
$$

根据这个关系，我们只需要知道 $\rho (x, p)$ 就可以得到任意物理量 $A (x, p)$ 的期待值。我们称这种量子力学的框架为相空间表述。

我们当然期望这种表述和经典力学的相空间表述对应，因此我们期望把 $f_{\text{w}}(x, p)$ 诠释为概率分布。但实际上这是不允许的，原因是在部分区域会有负值，并且它也不满足联合分布的条件（由不确定性原理这是显然的）。[^2]

尽管如此，$f_{\text{w}}(x, p)$ 仍然具有一个良好的性质：

$$
\begin{aligned}
P(p)	&=\int f_{\text{w}}(p,x)\,\mathrm{d}x\\
P(x)	&=\frac{1}{2\mathrm{\pi}\hbar}\int f_{\text{w}}(p,x)\,\mathrm{d}p
\end{aligned}
$$

这意味着对一个变量积分后可以得到另一个变量的概率分布。第二条证明只需利用密度矩阵的性质 $\rho(x,x)=\langle x|\rho|x\rangle=P (x)$：

$$
\frac{1}{2\mathrm{\pi}\hbar}\int\mathrm{e}^{-\mathrm{i}py/\hbar}\langle x+\frac{y}{2}|\rho|x-\frac{y}{2}\rangle\,\mathrm{d}y\,\mathrm{d}p	=\langle x|\rho|x\rangle=P(x)
$$

第一条还需要利用 $\rho (p, p)=P (p)$ 和：

$$
\rho(p,p^{\prime})=\int\rho(x,x^{\prime})\mathrm{e}^{(-\mathrm{i}/\hbar)(px-p^{\prime}x^{\prime})}\,\mathrm{d}x\,\mathrm{d}x^{\prime}
$$

剩余的推导十分简单：

$$
\int\mathrm{e}^{-\mathrm{i}py/\hbar}\langle x+\frac{y}{2}|\rho|x-\frac{y}{2}\rangle\,\mathrm{d}x\,\mathrm{d}y=\int\mathrm{e}^{-\mathrm{i}p(x-y)/\hbar}\langle x|\rho|y\rangle\,\mathrm{d}x\,\mathrm{d}y=\rho(p,p)=P(p)
$$

## 运动方程

为了得到运动方程，我们需要将密度矩阵的演化方程 $\dot{\rho}=-\mathrm{i}[H,\rho]$ 也做 Wigner 变换，为此，我们首先要计算两个算符乘积 $AB$ 的 Wigner 变换。首先考虑如下公式：

$$
\begin{aligned}
\langle x|A|x^{\prime}\rangle	&=\frac{1}{2\mathrm{\pi}\hbar}\int A_{\text{w}}(\frac{x+x^{\prime}}{2},p)\mathrm{e}^{\mathrm{i}p(x-x^{\prime})/\hbar}\,\mathrm{d}p\\
&=\int \widetilde{A}_{\text{w}}(\alpha,x^{\prime}-x)\mathrm{e}^{\mathrm{i}(\frac{x+x^{\prime}}{2})\alpha/\hbar}\,\mathrm{d}\alpha
\end{aligned}
$$

其中 $\widetilde{A}_{\text{w}}$ 是 $A_{\text{w}}$ 的 Fourier 变换：

$$
\widetilde{A}_{\text{w}}(\alpha,\beta)	=\frac{1}{2\mathrm{\pi}\hbar}\int A_{\text{w}}(x,p)\mathrm{e}^{-\mathrm{i}(\alpha x+\beta p)/\hbar}\,\mathrm{d}x\,\mathrm{d}p
$$

因此可以得到：

$$
\begin{aligned}
(AB)_{\text{w}}(x,p) & =\int\langle x+\frac{y}{2}|AB|x-\frac{y}{2}\rangle\mathrm{e}^{-\mathrm{i}py/\hbar}\,\mathrm{d}y\\
 & =\int\langle x+\frac{y}{2}|A|z\rangle\langle z|B|x-\frac{y}{2}\rangle\mathrm{e}^{-\mathrm{i}py/\hbar}\,\mathrm{d}y\,\mathrm{d}z\\
 & =\int\widetilde{A}_{\text{w}}(\alpha,z-x-\frac{y}{2})\widetilde{B}_{\text{w}}(\beta,x-\frac{y}{2}-z)\mathrm{e}^{\mathrm{i}(\frac{x+y/2+z}{2}\alpha+\frac{x-y/2+z}{2}\beta-py)/\hbar}\,\mathrm{d}\alpha\,\mathrm{d}\beta\,\mathrm{d}y\,\mathrm{d}z
\end{aligned}
$$

做变量替换：

$$
\begin{aligned}
\xi	&=z-x-\frac{y}{2}\\
\eta	&=x-\frac{y}{2}-z
\end{aligned}
$$

则得到：

$$
\begin{aligned}
(AB)_{\text{w}}(x,p)	&=\int[\widetilde{A}_{\text{w}}(\alpha,\xi)\mathrm{e}^{\mathrm{i}(\alpha x+\xi p)}]\mathrm{e}^{\frac{\mathrm{i}}{2\hbar}(\xi\beta-\alpha\eta)}[\widetilde{B}_{\text{w}}(\beta,\eta)\mathrm{e}^{\mathrm{i}(\beta x+\eta p)/\hbar}]\,\mathrm{d}\alpha\,\mathrm{d}\beta\,\mathrm{d}\xi\,\mathrm{d}\eta\\
&=A_{\text{w}}(x,p)\exp\left[\frac{\hbar}{2\mathrm{i}}\left(\mathop{\partial_{p}^{\leftarrow}}\mathop{\partial_{x}}^{\rightarrow}-\mathop{\partial_{x}^{\leftarrow}}\mathop{\partial_{p}}^{\rightarrow}\right)\right]B_{\text{w}}(x,p)
\end{aligned}
$$

这被称为 Moyal 积，记做 $A\star B$，这是算符乘法对应的相空间的乘法运算[^3]。我们继续定义 Moyal 括号为：

$$
\{A_{\text{w}}(x,p),B_{\text{w}}(x,p)\}_\text{M}\equiv\frac{2\mathrm{i}}{\hbar}A_{\text{w}}(x,p)\sin\left[\frac{\hbar}{2\mathrm{i}}(\mathop{\mathop{\partial_{x}}^{\leftarrow}}\mathop{\partial_{p}}^{\rightarrow}-\mathop{\mathop{\partial_{p}}^{\leftarrow}}\mathop{\partial_{x}}^{\rightarrow})\right]B_{\text{w}}(x,p)
$$

于是我们得到对易子的 Wigner 变换为：

$$
[A,B]_{\text{w}}(x,p)=\mathrm{i}\hbar\{A_{\text{w}}(x,p),B_{\text{w}}(x,p)\}_\text{M}
$$

再从密度矩阵的演化方程，可以得到 Wigner 函数的演化方程为：

$$
\frac{\mathrm{d}}{\mathrm{d}t}f_{\text{w}}(x,p)=\{H(x,p),f_{\text{w}}(x,p)\}_{\text{M}}
$$

可以看出 Moyal 括号在经典极限下退化为 Poisson 括号，Wigner 函数的演化方程退化为经典力学的演化方程。

[^1]: 真正的逆变换为 Weyl 变换，与 Weyl 量子化有关。

[^2]: [相空间表述 - 维基百科，自由的百科全书 (wikipedia.org)](https://zh.m.wikipedia.org/zh-sg/%E7%9B%B8%E7%A9%BA%E9%97%B4%E8%A1%A8%E8%BF%B0) 可以证明，分布值为负的区域非常小，其对于系统整体的影响在几ħ内，因而会在经典极限情况时会消失。这种负值在相干态出现的时候就会产生。

[^3]: 利用 Moyal 积我们可以对纯态的情况下的本征值方程 $H\rho=E\rho$ 做 Wigner 变换，得到相空间中的本征方程 $H\star f_{\text{w}}=E\cdot f_{\text{w}}$。
