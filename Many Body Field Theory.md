满足薛定谔方程的经典场量子化得到的多体理论与从量子力学出发得到的产生湮灭算符描述的多体理论等价。

而场的量子化有两种方案，一种是正则量子化，一种是路径积分量子化，它们是等价的。

第一部分讲多体量子力学等价于薛定谔场的正则量子化。

第二部分从正则量子化的框架得到路径积分表述。

## 薛定谔场的正则量子化

### 薛定谔经典场

拉格朗日量密度为：

$$
\mathscr{L}=\mathrm{i}\hbar\psi^{*}(\boldsymbol{r},t)\dot{\psi}(\boldsymbol{r},t)-\frac{\hbar^{2}}{2\mu}\nabla\psi^{*}\cdot\nabla\psi-V_{1}\psi^{*}\psi-\frac{1}{2}\int\mathrm{d}\boldsymbol{r}^{\prime}\,\psi^{*}(\boldsymbol{r}^{\prime},t)\psi^{*}(\boldsymbol{r},t)V_{2}(\boldsymbol{r},\boldsymbol{r}^{\prime})\psi(\boldsymbol{r},t)\psi(\boldsymbol{r}^{\prime},t)
$$

经典场的运动方程为：

$$
\frac{\partial}{\partial t}\left(\frac{\partial\mathscr{L}}{\partial\dot{\psi}}\right)+\nabla\cdot\left(\frac{\partial\mathscr{L}}{\partial(\nabla\psi)}\right)=\frac{\partial\mathscr{L}}{\partial\psi}
$$

代入上述拉氏量密度，得到：

$$
\mathrm{i}\hbar\frac{\partial\psi(\boldsymbol{r},t)}{\partial t}=-\frac{\hbar^{2}}{2m}\nabla^{2}\psi(\boldsymbol{r},t)+V_{1}(\boldsymbol{r},t)\psi(\boldsymbol{r},t)+\left(\int\mathrm{d}\boldsymbol{r}^{\prime}\,\psi^{*}(\boldsymbol{r}^{\prime},t)V_{2}(\boldsymbol{r},\boldsymbol{r}^{\prime})\psi(\boldsymbol{r}^{\prime},t)\right)\psi(\boldsymbol{r},t)
$$

可以看出，这就是多体 Schrodinger 方程。为转入正则框架，定义正则动量场：

$$
\mathrm{\pi}(\boldsymbol{r},t)=\frac{\partial\mathscr{L}}{\partial\dot{\psi}}=\mathrm{i}\hbar\psi^{*}(\boldsymbol{r},t)
$$

进而得到哈密顿量密度：

$$
\begin{align*}
\mathscr{H} & =\mathrm{\pi}\dot{\psi}-\mathscr{L}\\
 & =\frac{\hbar^{2}}{2m}\nabla\psi^{*}\cdot\nabla\psi+V_{1}\psi^{*}\psi+\frac{1}{2}\int\mathrm{d}\boldsymbol{r}^{\prime}\psi^{*}(\boldsymbol{r}^{\prime},t)\psi^{*}(\boldsymbol{r},t)V_{2}(\boldsymbol{r},\boldsymbol{r}^{\prime})\psi(\boldsymbol{r},r)\psi(\boldsymbol{r}^{\prime},t)
\end{align*}
$$

于是哈密顿量为：

$$
\begin{align*}
H(t) & =\int\mathrm{d}\boldsymbol{r}\,\mathscr{H}\\
 & =\int\mathrm{d}\boldsymbol{r}\left(\frac{\hbar^{2}}{2m}\nabla\psi^{*}\cdot\nabla\psi+V_{1}\psi^{*}\psi\right)+\frac{1}{2}\int\mathrm{d}\boldsymbol{r}\mathrm{d}\boldsymbol{r}^{\prime}\,\psi^{*}(\boldsymbol{r}^{\prime},t)\psi^{*}(\boldsymbol{r},t)V_{2}(\boldsymbol{r},\boldsymbol{r}^{\prime})\psi(\boldsymbol{r},t)\psi(\boldsymbol{r}^{\prime},t)
\end{align*}
$$

### 薛定谔场的反对易规则正则量子化

按照正则量子化规则，提升 $\psi$ 为算符 $\hat{\psi}$，$\pi$ 为算符 $\hat{\pi}$，对费米子引入反对易规则 $\{\hat{\psi}(\boldsymbol{r}, t),\hat{\mathrm{\pi}}(\boldsymbol{r}^{\prime}, t)\}=\mathrm{i}\hbar\delta (\boldsymbol{r}-\boldsymbol{r}^{\prime})$，即：

$$
\begin{align*}
\{\hat{\psi}(\boldsymbol{x},t),\hat{\psi}^{\dagger}(\boldsymbol{x}^{\prime},t)\} & =\delta(\boldsymbol{x}-\boldsymbol{x}^{\prime})\\
\{\hat{\psi}(\boldsymbol{x},t),\hat{\psi}(\boldsymbol{x}^{\prime},t)\} & =\{\hat{\psi}^{\dagger}(\boldsymbol{x},t),\hat{\psi}^{\dagger}(\boldsymbol{x}^{\prime},t)\}=0
\end{align*}
$$

这里我们把 $\psi^{*}$ 对应的算符写成了 $\hat{\psi}^{\dagger}$。于此同时，经典场哈密顿量变为量子场哈密顿量：

$$
\hat{H}(t)=\int\mathrm{d}\boldsymbol{r}\,\hat{\psi}^{\dagger}\left(-\frac{\hbar^{2}}{2m}\nabla^{2}+V_{1}\right)\hat{\psi}+\frac{1}{2}\int\mathrm{d}\boldsymbol{r}\mathrm{d}\boldsymbol{r}^{\prime}\,\hat{\psi}^{\dagger}(\boldsymbol{r}^{\prime},t)\hat{\psi}(\boldsymbol{r},t)V_{2}(\boldsymbol{r},\boldsymbol{r}^{\prime})\hat{\psi}(\boldsymbol{r},t)\hat{\psi}(\boldsymbol{r}^{\prime},t)
$$

这一量子场的运动方程与原来一样，只是经典场变为了量子场。

### 与多体量子力学的等价性

我们发现，正则量子化中引入的反对易规则很像产生湮灭算符的反对易规则，实际上，它们只不过是在海森堡绘景下工作的坐标表象的产生湮灭算符。

为了说明这一点，我们首先验证这些场算符的运动方程实际上就是它们在海森堡绘景下的运动方程即可。

海森堡绘景下算符的运动方程为：

$$
\frac{\mathrm{d}\hat{O}}{\mathrm{d}t}=\frac{\partial\hat{O}}{\partial t}+\frac{1}{\mathrm{i}\hbar}[\hat{O},\hat{H}]
$$

这里算符 $\hat{\psi}$ 不显含时间，因此有：

$$
\begin{align*}
\mathrm{i}\hbar\frac{\partial\hat{\psi}(\boldsymbol{r},t)}{\partial t} & =[\hat{\psi},\hat{H}]\\
 & =\left(-\frac{\hbar^{2}}{2m}\nabla^{2}+V_{1}(\boldsymbol{r},t)+\int\mathrm{d}\boldsymbol{r}^{\prime}\psi^{\dagger}(\boldsymbol{r}^{\prime},t)V_{2}(\boldsymbol{r},\boldsymbol{r}^{\prime})\hat{\psi}(\boldsymbol{r}^{\prime},t)\right)\hat{\psi}(\boldsymbol{r},t)
\end{align*}
$$

需要特别注意这里的 $\partial$ 和 $\mathrm{d}$ 的含义，不要被表象混淆。可以看出，这和我们之前的场方程完全相同，因此我们证明了场算符的运动方程就是场算符在海森堡绘景下的运动方程。

说明了这一点后，我们定义薛定谔绘景下的场算符：

$$
\hat{\psi}_{\text{S}}=\mathrm{e}^{-\mathrm{i}\hat{H}t/\hbar}\hat{\psi}_{\text{H}}(t)\mathrm{e}^{\mathrm{i}\hat{H}t/\hbar}
$$

逆着把这一式子代入，即可发现它满足上述运动方程。薛定谔绘景下的哈密顿量算符与海森堡绘景下的哈密顿量算符相同，为了方便也可以把场算符从海森堡绘景变成薛定谔绘景。

由此薛定谔绘景下的态矢演化满足：

$$
|\Psi(t)\rangle=\mathrm{e}^{-\mathrm{i}\hat{H}t/\hbar}|\Psi(0)\rangle
$$

则可以由此得到态矢的演化方程：

$$
\mathrm{i}\hbar\frac{\partial}{\partial t}|\Psi\rangle=\hat{H}|\Psi\rangle
$$

下面验证它就是多体的薛定谔方程。定义粒子数算符 $\hat{N}=\int\hat{\psi}^{\dagger}(\boldsymbol{r})\hat{\psi}(\boldsymbol{r})\,\mathrm{d}\boldsymbol{r}$。可以发现粒子数守恒。因此不同粒子数的波函数演化下不交叉，我们可以将其写为 $|\Psi_{N}\rangle$。将其转入坐标表象，即可得到：

$$
\mathrm{i}\hbar\frac{\partial}{\partial t}\Psi_{N}=\sum_{i}\left[-\frac{\hbar^{2}}{2m}\nabla_{i}^{2}+V_{i}^{(1)}(\boldsymbol{r}_{i})\right]\Psi_{N}(\boldsymbol{r}_{1},\dots,\boldsymbol{r}_{N},t)+\frac{1}{2}\sum_{i\neq j}V^{(2)}(\boldsymbol{r}_{i},\boldsymbol{r}_{j})\Psi_{N}(\boldsymbol{r}_{1},\dots,\boldsymbol{r}_{N},t)
$$

于是这就证明了和多体量子力学等价。

## 正则量子化推导路径积分

### 相干态

相干态是湮灭算符的本征态，使用这一工具容易得到路径积分的表达式。

#### 玻色子

玻色子情况下相干态写为：

$$
|\phi\rangle=\exp\left(\sum_{i}\phi_{i}a_{i}^{\dagger}\right)|0\rangle
$$

其中 $\phi=\{\phi_{i}\}$ 是一系列复数。

- 可以验证：

$$
a_{i}|\phi\rangle=\phi_{i}|\phi\rangle
$$

只需利用 $[a, (a^{\dagger})^{n}]=n (a^{\dagger})^{n-1}$，可以得到：

$$
\begin{align*}a_{i}|\phi\rangle & =a_{i}\exp\left(\phi\cdot a^{\dagger}\right)|\rangle=[a_{i},\exp\left(\phi\cdot a^{\dagger}\right)]|\rangle\\
 & =\sum_{n=1}^{\infty}\frac{\phi_{i}^{n}}{n!}[a_{i},(a_{i}^{\dagger})^{n}]\exp\left(\sum_{j\neq i}\phi_{j}a_{j}^{\dagger}\right)|\rangle\\
 & =\phi_{i}\sum_{n=1}^{\infty}\frac{\phi^{n-1}}{(n-1)!}(a_{i}^{\dagger})^{n-1}\exp\left(\sum_{j\neq i}\phi_{j}a_{j}^{\dagger}\right)|\rangle\\
 & =\phi_{i}\mathrm{e}^{\phi_{i}a_{i}^{\dagger}}\exp\left(\sum_{j\neq i}\phi_{j}a_{j}^{\dagger}\right)|\rangle\\
 & =\phi_{i}\exp\left(\phi\cdot a^{\dagger}\right)|\rangle=\phi_{i}|\phi\rangle
\end{align*}
$$

取厄米共轭，得到：

$$
\langle\phi|a_{i}^{\dagger}=\langle\phi|\bar{\phi}_{i}
$$

这里 $\bar{\phi}_{i}$ 是 $\phi_{i}$  的复共轭，$\langle\phi|=\langle|\exp\left (\bar{ \phi }\cdot a \right)$ 。

- 可以很直接的看出：

$$
a_{i}^{\dagger}|\phi\rangle=\frac{\partial}{\partial\phi_{i}}|\phi\rangle
$$

注意，$|\phi\rangle$ 并不是产生算符的本征态。

- 非正交性：

$$
\langle\eta|\phi\rangle=\langle|\exp\left( \bar{\eta }\cdot a \right)|\phi\rangle=\exp\left( \bar{\eta }\cdot \phi \right)\langle|\phi\rangle=\exp\left( \bar{\eta }\cdot \phi \right)
$$

从这一个式子中可以看出，模为：

$$
\langle\phi|\phi\rangle=\exp\left( \bar{\phi }\cdot \phi \right)
$$

- 过完备性：

$$
\int\mathrm{d}\phi\,\mathrm{e}^{-\bar{ \phi }\cdot \phi }|\phi\rangle\langle\phi|=1
$$

这里：

$$
\mathrm{d}\phi\equiv\prod_{i}\frac{\mathrm{d}\bar{\phi}_{i}\mathrm{d}\phi_{i}}{2\mathrm{\pi}}
$$

证明：

$$
\begin{align*}
a_{i}\int\mathrm{d}\phi\,\mathrm{e}^{-\bar{ \phi }\cdot \phi }|\phi\rangle\langle\phi| & =\int\mathrm{d}\phi\,\mathrm{e}^{-\bar{ \phi }\cdot \phi }\phi_{i}|\phi\rangle\langle\phi|\\
& =-\int\mathrm{d}\phi\,\left(\partial_{\bar{\phi}_{i}}\mathrm{e}^{-\bar{ \phi }\cdot \phi }\right)|\phi\rangle\langle\phi|\\
& =\int\mathrm{d}\phi\,\mathrm{e}^{-\bar{ \phi }\cdot \phi }\partial_{\bar{\phi}_{i}}(|\phi\rangle\langle\phi|)\\
& =\int\mathrm{d}\phi\,\mathrm{e}^{-\bar{ \phi }\cdot \phi }|\phi\rangle\langle\phi|a_{i}
\end{align*}
$$

对上式取共轭即得到 $a_{i}^{\dagger}$ 也与 $\int\mathrm{d}\phi\,\mathrm{e}^{-\bar{ \phi }\cdot \phi }|\phi\rangle\langle\phi|$ 是对易，而 $\{a_{i}, a_{i}^{\dagger}\}$ 在 Fock 空间的常规表示是不可约的，因此根据舒尔引理，$\int\mathrm{d}\phi\,\mathrm{e}^{-\bar{ \phi }\cdot \phi }|\phi\rangle\langle\phi|$ 只能是常数。接下来将其夹在真空态间得到：

$$
\int\mathrm{d}\phi\,\mathrm{e}^{-\bar{ \phi }\cdot \phi }\langle|\phi\rangle\langle\phi|\rangle=\int\mathrm{d}\phi\,\mathrm{e}^{-\bar{ \phi }\cdot \phi }=1
$$

这完成了证明。

#### 费米子

由于费米子的反对易特性，湮灭算符的本征值必须为 Grassmann 数，构造相干态的时候也需要用 Grassmann 数。

##### Grassmann 数

为了符合产生湮灭算符的反对易关系，我们要求 Grassmann 数：

$$
\{\eta_{i},\eta_{j}\}  =0
$$

- 两个 Grassmann 数的乘积为普通数。
- Grassmann 数的函数通过 Taylor 展开定义。
	- 如果 $f (\eta)$ 只包含一种 Grassmann 数，则 $f (\eta)=a+b\eta$。
	- 如果是多 Grassmann 数变量的函数，则有

$$
\begin{align*}f( \eta ) & =f(\eta_{1},\dots,\eta_{n})\\
 & =a+\eta_{i}b_{i}+\frac{1}{2}\eta_{i}\eta_{j}c_{ij}+\dots+\frac{1}{n!}\eta_{i_{1}}\dots\eta_{i_{n}}d_{i_{1}\dots i_{n}}
\end{align*}
$$

- Grassmann 数的导数定义为：

$$
\frac{\partial}{\partial\eta_{i}}\eta_{j}=\delta_{ij}
$$

- Grassmann 数的积分定义为：

$$
\int\mathrm{d}\eta_{i}=0,\quad\int\mathrm{d}\eta_{i}\,\eta_{i}=1
$$

- Grassmann 数的求导和积分相同。
- Grassmann 数的积分具有平移不变性。
- 多变量的求导定义为：

$$
\begin{align*}\frac{\mathrm{d}}{\mathrm{d}\eta_{1}}\eta_{1}\eta_{2} & =\eta_{2}\\
\frac{\mathrm{d}}{\mathrm{d}\eta_{2}}\eta_{1}\eta_{2} & =-\eta_{1}
\end{align*}
$$

- 多变量的积分需要清楚的定义积分测度中 Grassmann 数的顺序，如定义：

$$
\mathrm{d}^{n} \eta =\mathrm{d}\eta_{n}\mathrm{d}\bar{\eta}_{n}\dots\mathrm{d}\eta_{1}\mathrm{d}\bar{\eta}_{1}
$$

基于上面的讨论，对多变量函数的积分有非常简单的结果：

$$
\begin{align*}I & =\int\mathrm{d}^{n} \eta \,f( \eta )=\int\mathrm{d}\eta_{n}\dots\mathrm{d}\eta_{1}\,f( \eta )\\
 & =\int\mathrm{d}\eta_{n}\dots\mathrm{d}\eta_{1}\,\frac{1}{n!}\eta_{i_{1}}\dots\eta_{i_{n}}d_{i_{1}\dots i_{n}}\\
 & =\frac{1}{n!}\varepsilon_{i_{1}\dots i_{n}}d_{i_{1}\dots i_{n}}
\end{align*}
$$

这里还可以得到：

$$
d_{i_{1}\dots i_{n}}=\varepsilon_{i_{1}\dots i_{n}}I
$$

这一步证明需要用到：

$$
\varepsilon_{i_{1}\dots i_{n}}\varepsilon_{j_{1}\dots j_{n}}=\sum_{P\in S_{n}}\mathop{\text{sgn}}(P)\delta_{i_{1}j_{P(1)}}\dots\delta_{i_{n}j_{P(n)}}
$$

接下来讨论做变量替换时，积分测度如何变化。做线性变换：

$$
\eta_{i}=\sum_{j}J_{ij}\eta_{j}^{\prime}
$$

变量替换后的 $f ( \eta )$ 为：

$$
f( \eta )=a+\dots+\frac{1}{n!}(J_{i_{1}j_{1}}\eta_{j_{1}}^{\prime})\dots(J_{i_{n}j_{n}}\eta_{j_{n}}^{\prime})\varepsilon_{i_{1}\dots i_{n}}I
$$

利用：

$$
\varepsilon_{i_{1}\dots i_{n}}J_{i_{1}j_{2}}\dots J_{i_{n}j_{n}}=\det(J)\varepsilon_{j_{1}\dots j_{n}}
$$

我们就可以得到：

$$
f(\eta)=a+\dots+\frac{1}{n!}\eta_{j_{1}}^{\prime}\dots\eta_{j_{n}}^{\prime}\det(J)d_{j_{1}\dots j_{n}}
$$

因此：

$$
\int\mathrm{d}^{n}\eta^{\prime}\,f(\eta)=\det(J)I
$$

于是我们得到了：

$$
I=(\det J)^{-1}\int\mathrm{d}^{n}\eta^{\prime}\,f(\eta)
$$

#####  费米子 Gauss 积分

我们想计算：

$$
I=\int\mathrm{d}\eta^{n}\,\mathrm{e}^{\bar{\eta}_{i}M_{ij}\eta_{j}}
$$

对 $M$ 做奇异值分解，找到两个幺正矩阵 $U$ 和 $V$，使得：

$$
VMU=\mathop{\text{diag}}(m_{1},\dots,m_{n})
$$

并且 $m_{i}$ 为非负整数。

做变量替换：

$$
\begin{align*}
\eta_{i} & =U_{ij}\eta_{j}^{\prime}\\
\bar{\eta}_{i} & =(V^{\mathrm{T}})_{ij}\bar{\eta}_{j}^{\prime}
\end{align*}
$$

由此得积分变为：

$$
I=(\det U)^{-1}(\det V)^{-1}\int\mathrm{d}^{n}\eta^{\prime}\,\exp\left(\sum_{k}m_{k}\bar{\eta}_{k}^{\prime}\eta_{k}^{\prime}\right)
$$

容易计算出这一积分为：

$$
\begin{align*}
I & =(\det U)^{-1}(\det V)^{-1}\det(VMU)\\
 & =\det M
\end{align*}
$$

可能有 $n\rightarrow\infty$ ，我们因此省略掉 $n$，而指标也可能取值连续，我们因此省略掉指标。于是写成紧凑的形式有：

$$
\int\mathrm{d} \eta \,\mathrm{e}^{\bar{\eta}M\eta}=\det M
$$

##### 费米子相干态

定义费米子相干态为：

$$
|\eta\rangle=\exp\left(-\sum_{i}\eta_{i}a_{i}^{\dagger}\right)|\rangle
$$

- 可以验证：

$$
a_{i}|\eta\rangle=\eta_{i}|\eta\rangle
$$

利用 $a (1-\eta a^{\dagger})|\rangle=\eta aa^{\dagger}|\rangle=\eta|\rangle=\eta (1-\eta a^{\dagger})|\rangle$ 即可得到：

$$
\begin{align*}a_{i}|\eta\rangle & =a_{i}\exp\left(-\sum_{i}\eta_{i}a_{i}^{\dagger}\right)|\rangle\\
 & =a_{i}(1-\eta_{i}a_{i}^{\dagger})\exp\left(-\sum_{j\neq i}\eta_{j}a_{j}^{\dagger}\right)|\rangle\\
 & =\eta_{i}(1-\eta_{i}a_{i}^{\dagger})\exp\left(-\sum_{j\neq i}\eta_{j}a_{j}^{\dagger}\right)|\rangle\\
 & =\eta_{i}\mathrm{e}^{-\eta_{i}a_{i}^{\dagger}}\exp\left(-\sum_{j\neq i}\eta_{j}a_{j}^{\dagger}\right)|\rangle\\
 & =\eta_{i}\exp(- \eta \cdot a ^{\dagger})|\rangle=\eta_{i}|\eta\rangle
\end{align*}
$$

取厄米共轭，得到：

$$
\langle\eta|a_{i}^{\dagger}=\langle\eta|\bar{\eta}_{i}
$$

这里 $\bar{\eta}_{i}$ 是 $\eta_{i}$ 的复共轭，$\langle\eta|=\langle|\exp\left(\sum_{i}\bar{\eta}_{i}a_{i}\right)$ [^1]。

- 可以看出，有：

$$
a_{i}^{\dagger}|\eta\rangle=-\frac{\partial}{\partial\eta_{i}}|\eta\rangle
$$

也可以得到：

$$
\langle\eta|a_{i}=\frac{\partial}{\partial\bar{\eta}_{i}}\langle\eta|
$$

- 非正交性：

$$
\langle\psi|\eta\rangle=\langle|\exp\left(\bar{ \psi }\cdot a \right)|\eta\rangle=\exp\left(\bar{ \psi }\cdot \eta \right)\langle|\eta\rangle=\exp\left(\bar{ \psi }\cdot \eta \right)
$$

由此可以看出模为：

$$
\langle\eta|\eta\rangle=\exp\left(\bar{ \eta }\cdot \eta \right)
$$

- 过完备性：

$$
\int\mathrm{d}\eta\,\mathrm{e}^{-\bar{ \eta }\cdot \eta }|\eta\rangle\langle\eta|=1
$$

这里：

$$
\mathrm{d}\eta\equiv\prod_{i}\mathrm{d}\bar{\eta}_{i}\mathrm{d}\eta_{i}
$$

证明：

$$
\begin{align*}
a_{i}\int\mathrm{d}\eta\,\mathrm{e}^{-\bar{\eta}\cdot\eta}|\eta\rangle\langle\eta| & =-\int\mathrm{d}\eta\,\mathrm{e}^{-\bar{\eta}\cdot\eta}a_{i}|\eta\rangle\langle\eta|\\
 & =-\int\mathrm{d}\eta\,\mathrm{e}^{-\bar{\eta}\cdot\eta}\eta_{i}|\eta\rangle\langle\eta|\\
 & =\int\mathrm{d}\eta\,\frac{\partial}{\partial\bar{\eta}_{i}}(\mathrm{e}^{-\bar{\eta}\cdot\eta})|\eta\rangle\langle\eta|\\
 & =-\int\mathrm{d}\eta\,\mathrm{e}^{-\bar{\eta}\cdot\eta}\frac{\partial}{\partial\bar{\eta}_{i}}(|\eta\rangle\langle\eta|)\\
 & =\int\mathrm{d}\eta\,\mathrm{e}^{-\bar{\eta}\cdot\eta}|\eta\rangle\frac{\partial}{\partial\bar{\eta}_{i}}(\langle\eta|)\\
 & =\int\mathrm{d}\eta\,\mathrm{e}^{-\bar{\eta}\cdot\eta}|\eta\rangle\langle\eta|a_{i}
\end{align*}
$$

类似的也可以得到 $a_{i}^{\dagger}$ 与 $\int\mathrm{d}\eta\,\mathrm{e}^{-\bar{\eta}\cdot\eta}|\eta\rangle\langle\eta|$ 也对易。因此 $\int\mathrm{d}\eta\,\mathrm{e}^{-\bar{\eta}\cdot\eta}|\eta\rangle\langle\eta|$ 是常数。接下来只要将其加在真空态中证明其为 1 即可，这里的证明需要用到前面的 Grassmann 数 Gauss 积分，可以很容易看出：

$$
\int\mathrm{d}\eta\,\mathrm{e}^{-\bar{\eta}\cdot\eta}\langle|\eta\rangle\langle\eta|\rangle=\int\mathrm{d}\eta\,\mathrm{e}^{-\bar{\eta}\cdot\eta}=1
$$

### 相干态路径积分

有了相干态这一工具，我们可以写出场算符 $\hat{\psi}$ 的本征态 $|\psi\rangle$，这里 $\psi$ 可以是玻色子场或者费米子场。

于是我们可以写出相干态表象下的传播子，首先我们把时间切片：

$$
\langle\psi_{b},t_{b}|\psi_{a},t_{a}\rangle=\langle\psi_{b}|\mathrm{e}^{\mathrm{i}H(t_{b}-t_{a})}|\psi_{a}\rangle=\langle\psi_{b}|\lim_{N\rightarrow\infty}(\mathrm{e}^{\mathrm{i}H\Delta t})^{N}|\psi_{a}\rangle\quad
$$

这里 $\Delta t=(t_b-t_a)/N$。接下来我们在每个切片之间，插入 $\int\mathrm{d}\psi\,\mathrm{e}^{-\bar{\psi}\cdot\psi}|\psi\rangle\langle\psi|=1$，根据玻色子或费米子，$\psi$ 分别取 $\phi$ 或 $\eta$。因此可以得到：

$$
\langle\psi_{b}|\mathrm{e}^{\mathrm{i}H(t_{b}-t_{a})}|\psi_{a}\rangle=\lim_{N\rightarrow\infty}\int\prod_{n=0}^{N}\mathrm{d}\psi^{n}\exp\left(\mathrm{i}\Delta t\left(\frac{\bar{\psi}^{n}\cdot(\psi^{n+1}-\psi^{n})}{\Delta t}+H(\bar{\psi}^{n+1},\psi^{n})\right)\right)
$$

这里：

$$
H(\bar{\psi}^{\prime},\psi)=\sum_{ij}t_{ij}\bar{\psi}_{i}^{\prime}\psi_{j}+\frac{1}{2}\sum_{ijkl}v_{ijkl}\bar{\psi}_{i}^{\prime}\bar{\psi}_{j}^{\prime}\psi_{l}\psi_{k}
$$

只是把场算符替换成了数。我们发现，在 $\Delta t\rightarrow 0$ 的时候，指数上的形式及其类似于作用量，于是我们形式的写为：

$$
\langle\psi_{b}|\mathrm{e}^{\mathrm{i}Ht}|\psi_{a}\rangle=\int\mathcal{D}\psi\,\exp\left(\mathrm{i}\int_{t_{a}}^{t_{b}}\mathrm{d}t\,\left(\bar{\psi}\cdot\partial_{t}\psi+H\right)\right)=\int\mathcal{D}\psi\,\mathrm{e}^{\mathrm{i}S}
$$

这里 $\mathcal{D}\psi$ 为 $\prod_{n=0}^{N}\mathrm{d}\psi^{n}$ 在 $N\rightarrow\infty$ 时的形式。