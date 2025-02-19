---
related:
  - "[[Density Matrix]]"
---
### Hartree-Fock 方程

非相对论情况下，只包含两体项的哈密顿量可以写为：

$$
  
H=\sum_{ij}t_{ij}a_{i}^{\dagger}a_{j}+\frac{1}{2}\sum_{ijkl}v_{ijkl}a_{i}^{\dagger}a_{j}^{\dagger}a_{l}a_{k}  
$$

其中指标 $i, j, k, l$ 标记了一组正交归一的单粒子态，$a^{\dagger}$ 代表产生算符，$a$ 代表湮灭算符。求和遍历所有可能的态。在不考虑粒子数变化的情况下，这个哈密顿量的本征态可以写为一系列求和，求和的每一项核子数相同为 $A$，但占据了不同的单粒子态：

$$
  
|\psi\rangle=\sum_{i_{1},\cdots,i_{A}}c_{i_{1}\cdots i_{A}}a_{i_{1}}^{\dagger}\cdots a_{i_{A}}^{\dagger}|0\rangle  
$$

$i_{n}$ 就代表了不同的单粒子态。这个表达式是严格的，然而我们无法计算。为此，我们采用一个近似，即只考虑具有表达式其中一项形式的态矢：

$$
  
|\psi\rangle=a_{1}^{\dagger}a_{2}^{\dagger}\cdots a_{A}^{\dagger}|0\rangle  
$$

我们在此基础上使用变分法，从而得到Hartree-Fock方程。

首先考虑任意一个产生算符的变动：

$$
  
\delta a_{i}^{\dagger}=\varepsilon a_{j}^{\dagger}  
$$

这里 $i\neq j$，因此这一变动会导致态被湮灭掉，并无意义。我们然后考虑态矢的变动：

$$
  
\begin{aligned} |\delta\psi_{i}\rangle & =\varepsilon a_{1}^{\dagger}\cdots a_{i-1}^{\dagger}a_{j}^{\dagger}a_{i+1}^{\dagger}\cdots a_{A}^{\dagger}|0\rangle\\ & =\varepsilon a_{j}^{\dagger}a_{i}|\psi\rangle \end{aligned}  
$$

所有的变动都可以写成上述变动线性叠加的形式。可以看出，$j$ 必须大于 $A$，否则会导致变动为 $0$。

接下来，为了区分占据态（小于 A）和非占据态，我们用 $i, j$ 表示占据态，用 $m, n$ 表示非占据态，用 $k, l$ 表示自由的指标。于是上述变动表示为 $|\delta\psi_{i}\rangle=\varepsilon a_{m}^{\dagger}a_{i}|\psi\rangle$。

于是能量本征值的变分为：

$$
  
\delta E[\psi]=\delta\left(\frac{\langle\psi|H|\psi\rangle}{\langle\psi|\psi\rangle}\right)=\frac{\langle\delta\psi|H-E[\psi]|\psi\rangle+\langle\psi|H-E[\psi]|\delta\psi\rangle}{\langle\psi|\psi\rangle}  
$$

$|\psi\rangle$ 是归一化的，由此得：

$$
  
\begin{aligned} \delta\langle\psi|H|\psi\rangle & =\varepsilon^{*}\langle\psi|a_{i}^{\dagger}a_{m}H|\psi\rangle+\varepsilon^{*}\langle\psi|Ha_{m}^{\dagger}a_{i}|\psi\rangle-E[\psi](\langle\psi|a_{i}^{\dagger}a_{m}|\psi\rangle+\langle\psi|a_{m}^{\dagger}a_{i}|\psi\rangle)\\ & =2\varepsilon^{*}\Re(\langle\psi|a_{i}^{\dagger}a_{m}H|\psi\rangle) \end{aligned}  
$$

由于 $a_{i}^{\dagger}a_{m}H$ 是厄米算符，因此上式中的期待值本来即为实数。由此上述式子等于0的充要条件是：

$$
  
\langle\psi|a_{i}^{\dagger}a_{m}H|\psi\rangle=0  
$$

代入哈密顿量：

$$
  
\begin{aligned} & \langle\psi|a_{i}^{\dagger}a_{m}\left(\sum_{k_{1}k_{2}}t_{k_{1}k_{2}}a_{k_{1}}^{\dagger}a_{k_{2}}+\frac{1}{2}\sum_{k_{1}k_{2}k_{3}k_{4}}v_{k_{1}k_{2}k_{3}k_{4}}a_{k_{1}}^{\dagger}a_{k_{2}}^{\dagger}a_{k_{4}}a_{k_{3}}\right)|\psi\rangle\\ = & \sum_{k_{1}k_{2}}t_{k_{1}k_{2}}\langle\psi|a_{i}^{\dagger}a_{m}a_{k_{1}}^{\dagger}a_{k_{2}}|\psi\rangle+\frac{1}{2}\sum_{k_{1}k_{2}k_{3}k_{4}}v_{k_{1}k_{2}k_{3}k_{4}}\langle\psi|a_{i}^{\dagger}a_{m}a_{k_{1}}^{\dagger}a_{k_{2}}^{\dagger}a_{k_{4}}a_{k_{3}}|\psi\rangle \end{aligned}  
$$

使用wick定理（颜色相同表示缩并）计算第一项中的期待值：

$$
  
{\color{teal}a_{i}^{\dagger}}{\color{blue}a_{m}a_{k_{1}}^{\dagger}}{\color{teal}a_{k_{2}}}  
$$

得到 $-\delta_{ik_{2}}\delta_{mk_{1}}$。类似的，计算第二项中的期待值：

$$
\begin{gather*}
{\color{teal}a_{i}^{\dagger}}{\color{red}a_{m}}{\color{red}a_{k_{1}}^{\dagger}}{\color{blue}a_{k_{2}}^{\dagger}}{\color{teal}a_{k_{3}}}{\color{blue}a_{k_{4}}}  
\\
{\color{teal}a_{i}^{\dagger}}{\color{blue}a_{m}}{\color{red}a_{k_{1}}^{\dagger}}{\color{blue}a_{k_{2}}^{\dagger}}{\color{teal}a_{k_{3}}}{\color{red}a_{k_{4}}}  
\\
{\color{teal}a_{i}^{\dagger}}{\color{red}a_{m}}{\color{red}a_{k_{1}}^{\dagger}}{\color{blue}a_{k_{2}}^{\dagger}a_{k_{3}}}{\color{teal}a_{k_{4}}}  
\\  
{\color{teal}a_{i}^{\dagger}}{\color{blue}a_{m}}{\color{red}a_{k_{1}}^{\dagger}}{\color{blue}a_{k_{2}}^{\dagger}}{\color{red}a_{k_{3}}}{\color{teal}a_{k_{4}}}  
\end{gather*}
$$

第二项的期待值为 $-\delta_{ik_{3}}\delta_{mk_{1}}\delta_{k_{2}k_{4}}+\delta_{ik_{3}}\delta_{mk_{2}}\delta_{k_{1}k_{4}}+\delta_{ik_{4}}\delta_{mk_{1}}\delta_{k_{2}k_{3}}-\delta_{ik_{4}}\delta_{mk_{2}}\delta_{k_{1}k_{3}}$，由于最后一个 $\delta$ 的指标均小于 $A$，因此替换为$j$。代入得：

$$
  
t_{mi}+\frac{1}{2}\sum_{j}(v_{jmji}-v_{mjji}-v_{jmij}+v_{mjij})=0  
$$

根据 $v$ 的定义，同时交换12和34指标不变，有 $v_{jmji}=v_{mjij}, v_{mjji}=v_{jmij}$。因此有：

$$
  
t_{mi}+\sum_{j}(v_{mjij}-v_{mjji})=0  
$$

定义 $\bar{v}_{ijkl}=v_{ijkl}-v_{ijlk}$，则上式可以写成：

$$
  
t_{mi}+\sum_{j}\bar{v}_{mjij}=0  
$$

定义 Fock 矩阵 $f_{mi}$：

$$
\begin{aligned}f_{kl} & =t_{kl}+\sum_{j}\bar{v}_{kjlj}\\
 & =\begin{bmatrix}f_{\text{pp}} & f_{\text{hp}}\\
f_{\text{ph}} & f_{\text{hh}}
\end{bmatrix}
\end{aligned}
$$

第二部是将矩阵分块，指标的 h 表示空穴，p 表示粒子，于是变分为零得到的方程实际上是在说，这个矩阵的 $f_{\text{hp}}$, $f_{\text{ph}}$ 为零。因此，一个简便的方式（有选择的自由度）为取 $f_{kl}$ 为对角阵，这被称为正则 Hartree-Fock，我们于是可以得到正则 Hartree-Fock 方程：

$$
  
t_{kl}+\sum_{j}\bar{v}_{kjlj}=\delta_{kl}\varepsilon_{k}  
$$

在坐标表象下写这个方程，即为：

$$
\begin{aligned}-\frac{\hbar^{2}}{2m}\nabla^{2}\psi_{k}(\boldsymbol{x})+\sum_{j}\int\mathrm{d}^{3}\boldsymbol{x}^{\prime}\psi_{j}^{*}(\boldsymbol{x}^{\prime})V(\boldsymbol{x},\boldsymbol{x}^{\prime})\psi_{k}(\boldsymbol{x}^{\prime})\psi_{j}(\boldsymbol{x})\\
-\sum_{j}\int\mathrm{d}^{3}\boldsymbol{x}^{\prime}\psi_{j}^{*}(\boldsymbol{x}^{\prime})V(\boldsymbol{x},\boldsymbol{x}^{\prime})\psi_{j}(\boldsymbol{x}^{\prime})\psi_{k}(\boldsymbol{x}) & =\varepsilon_{k}\psi_{k}(\boldsymbol{x})
\end{aligned}
$$

显然，方程左侧第二项和第三项代表了平均场的作用。

### 应用

用 $|0\rangle$ 表示基态，$|\rangle$ 表示真空态，有：

$$
  
|0\rangle=\prod_{i}a_{i}^{\dagger}|\rangle  
$$

基态的能量可以计算出来：

$$
\begin{align*}
E_{0} & =\langle 0|H|0\rangle\\
 & =\sum_{k_{1}k_{2}}t_{k_{1}k_{2}}\langle 0|a_{k_{1}^{\dagger}}a_{k_{2}}|0\rangle+\frac{1}{2}\sum_{k_{1}k_{2}k_{3}k_{4}}v_{k_{1}k_{2}k_{3}k_{4}}\langle 0|a_{k_{1}^{\dagger}}a_{k_{2}}^{\dagger}a_{k_{4}}a_{k_{3}}|0\rangle\\
 & =\sum_{i}t_{ii}+\frac{1}{2}\sum_{ij}\bar{v}_{ijij}\\
 & =\sum_{i}\varepsilon_{i}-\frac{1}{2}\sum_{ij}\bar{v}_{ijij}
\end{align*}
$$

这一结果表明总的能量并不等于所有单粒子能量之和，这是与平均场近似的物理图像冲突的。激发态的能量也可以这么算，然而实际上 Hartree-Fock 方程与占据态有关，因此这并不严谨。但是在比较大的核里，一个核子的跃迁对平均场影响不大，对波函数影响更小，因此也可以用来估算。

我们用 $|mi\rangle$ 表示一个粒子的激发态：

$$
  
|mi\rangle=a_{m}^{\dagger}a_{i}|0\rangle  
$$

用 $|mnij\rangle$ 表示两个粒子的激发态：

$$
  
|mnij\rangle=a_{m}^{\dagger}a_{n}^{\dagger}a_{i}a_{j}|0\rangle  
$$

于是单粒子态的能量为：

$$
\begin{align*}
E_{mi} & =\langle mi|H|mi\rangle\\
 & =\sum_{k_{1}k_{2}}t_{k_{1}k_{2}}\langle mi|a_{k_{1}^{\dagger}}a_{k_{2}}|mi\rangle+\frac{1}{2}\sum_{k_{1}k_{2}k_{3}k_{4}}v_{k_{1}k_{2}k_{3}k_{4}}\langle mi|a_{k_{1}^{\dagger}}a_{k_{2}}^{\dagger}a_{k_{3}}a_{k_{4}}|mi\rangle
\end{align*}
$$

我们发现计算的时候可以把 $|mi\rangle$ 当成新的基态，于是和原来的区别只是求和的时候指标范围不同：

$$
  
\begin{aligned} E_{mi} & =E_{0}-t_{ii}+t_{mm}+\sum_{j}(\bar{v}_{ijij}-\bar{v}_{mjmj})-\bar{v}_{mimi}\\ & =E_{0}+\varepsilon_{m}-\varepsilon_{i}-\bar{v}_{mimi} \end{aligned}  
$$

注意，这里使用了张量 $\bar{v}$ 的对称和反对称性质，即同时交换其第一个和第二个指标，第三个和第四个指标结果不变，以及 $\bar{v}_{iiii}$ =0。

然而，值得注意的是，哈密顿量在 $|mi\rangle$ 态下并不是对角的，这是不合常理的，因此这只是一个粗糙的近似。

## 正规序推导

上述 Hartree-Fock 方法有明显的缺点，那就是不能回答所得结果的近似程度如何。下面我们换一种推导，从而能够把略去的部分表示出来。根据前面的推导，我们知道 Hartree-Fock 实际上就是利用变分法找到一个最贴合真实基态的波函数，而在变分的过程实际上就是不断的做基变换的过程。

我们把哈密顿量用 Wick 定理展开，对单体算符项展开为：

$$
a_{k_{1}}^{\dagger}a_{k_{2}}=:\mathrel{a_{k_{1}}^{\dagger}a_{k_{2}}}:+:\mathrel{{\color{teal}a_{k_{1}}^{\dagger}a_{k_{2}}}}:
$$

于是可以把单体算符项写为：

$$
\sum_{kl}t_{kl}:\mathrel{a_{k}^{\dagger}a_{l}}:+\sum_{i}t_{ii}
$$

两体算符项为：

$$
  
\begin{aligned} a_{k_{1}}^{\dagger}a_{k_{2}}^{\dagger}a_{k_{4}}a_{k_{3}} & =:\mathrel{a_{k_{1}}^{\dagger}a_{k_{2}}^{\dagger}a_{k_{4}}a_{k_{3}}}:\\ & +:\mathrel{{\color{teal}a_{k_{1}}^{\dagger}}a_{k_{2}}^{\dagger}{\color{teal}a_{k_{4}}}a_{k_{3}}}:+:\mathrel{{\color{teal}a_{k_{1}}^{\dagger}}a_{k_{2}}^{\dagger}a_{k_{4}}{\color{teal}a_{k_{3}}}}:+:\mathrel{a_{k_{1}}^{\dagger}{\color{teal}a_{k_{2}}^{\dagger}}{\color{teal}a_{k_{4}}}a_{k_{3}}}:+:\mathrel{a_{k_{1}}^{\dagger}{\color{teal}a_{k_{2}}^{\dagger}}a_{k_{4}}{\color{teal}a_{k_{3}}}}:\\ & +:\mathrel{{\color{teal}a_{k_{1}}^{\dagger}}{\color{red}a_{k_{2}}^{\dagger}}{\color{teal}a_{k_{4}}}{\color{red}a_{k_{3}}}}:+:\mathrel{{\color{teal}a_{k_{1}}^{\dagger}}{\color{red}a_{k_{2}}^{\dagger}a_{k_{4}}}{\color{teal}a_{k_{3}}}}: \end{aligned}  
$$

利用 $v_{k_{1}k_{2}k_{4}k_{3}}$ 的对称性，可以把二体算符项写成：

$$
\begin{align*}
 & \frac{1}{2}\sum_{k_{1}k_{2}k_{3}k_{4}}v_{k_{1}k_{2}k_{3}k_{4}}:\mathrel{a_{k_{1}}^{\dagger}a_{k_{2}}^{\dagger}a_{k_{4}}a_{k_{3}}}:+\sum_{klj}\bar{v}_{jkjl}:\mathrel{a_{k}^{\dagger}a_{l}}:+\frac{1}{2}\sum_{ij}\bar{v}_{ijij}
\end{align*}
$$

于是哈密顿量写成：

$$
\begin{align*}H & =\sum_{k_{1}k_{2}}t_{k_{1}k_{2}}a_{k_{1}}^{\dagger}a_{k_{2}}+\frac{1}{2}\sum_{k_{1}k_{2}k_{3}k_{4}}v_{k_{1}k_{2}k_{3}k_{4}}a_{k_{1}}^{\dagger}a_{k_{2}}^{\dagger}a_{k_{4}}a_{k_{3}}\\
 & =\sum_{i}t_{ii}+\frac{1}{2}\sum_{ij}\bar{v}_{ijij}\\
 & +\sum_{kl}\left(t_{kl}+\sum_{j}\bar{v}_{jkjl}\right):\mathrel{\mathrel{a_{k}^{\dagger}a_{l}}}:\\
 & +\frac{1}{2}\sum_{k_{1}k_{2}k_{3}k_{4}}v_{k_{1}k_{2}k_{3}k_{4}}:\mathrel{a_{k_{1}}^{\dagger}a_{k_{2}}^{\dagger}a_{k_{4}}a_{k_{3}}}:
\end{align*}
$$

可以看出，第一项为常数项，第二项为单体算符，第三项为两体算符。如果令第二项对角化，即：

$$
  
t_{kl}+\sum_{j}\bar{v}_{jkjl}=\delta_{kl}\varepsilon_{k}  
$$

于是得到了 Hartree-Fock 方程。于是我们可以看出，Hartree-Fock 近似实际上略去了两体的部分，我们称之为剩余相互作用 $V_{\text{res}}$：

$$
  
V_{res}=\frac{1}{2}\sum_{k_{1}k_{2}k_{3}k_{4}}v_{k_{1}k_{2}k_{3}k_{4}}:\mathrel{a_{k_{1}}^{\dagger}a_{k_{2}}^{\dagger}a_{k_{4}}a_{k_{3}}}:  
$$

现在我们可以尝试用略去了这一项之后的哈密顿量计算基态能量，可以得到：

$$
E_{0}=\sum_{i}t_{ii}+\frac{1}{2}\sum_{ij}\bar{v}_{ijij}=\sum_{i}\varepsilon_{i}-\frac{1}{2}\sum_{ij}\bar{v}_{ijij}
$$

这和之前的结果是一样的。

## 密度矩阵推导

定义单粒子密度矩阵：

$$
\rho_{kl}=\langle\Phi|a_{l}^{\dagger}a_{k}|\Phi\rangle
$$

这实际上和 $\rho (x, x^{\prime})$ 类似。当 $|\Phi\rangle$ 为 Slater 行列式时，可以证明 $\rho^{2}=\rho$ 。我们首先从简单的情况出发，假设 $|\Phi\rangle$ 是由和产生湮灭算符 $a_{k}^{\dagger}$ 和 $a_{k}$ 相同的单粒子基组成的，显然有：

$$
\rho_{kl}=\begin{cases}
\delta_{kl} & k\leq A\\
0 & k>A
\end{cases}
$$

此时 $\rho^{2}=\rho$ 显然成立。如果 $|\Phi\rangle$ 不是由和产生湮灭算符 $a_{k}^{\dagger}$ 和 $a_{k}$ 相同的单粒子基组成，我们假设 $|\Phi\rangle$ 对应的产生湮灭算符为 $b^{\dagger}_k$ 和 $b_k$，那么我们一定有：

$$
\begin{align*}
a_{i} & =\sum_{j}U_{ij}b_{j}\\
a_{k} & =\sum_{l}U_{kl}^{*}b_{l}^{\dagger}
\end{align*}
$$

如果想保持对易关系，那么我们一定有：

$$
\sum_{j}U_{ij}U_{kj}^{*}=\delta_{ik}\quad\text{即}\quad UU^{\dagger}=I
$$

于是我们可以有：

$$
\begin{align*}
\rho_{ik} & =\langle\Phi|a_{k}^{\dagger}a_{i}|\Phi\rangle=\sum_{jl}U_{kl}^{*}U_{ij}\langle\Phi|b_{l}^{\dagger}b_{j}|\Phi\rangle\\
 & =\sum_{j}U_{kj}^{*}U_{ij}\rho_{jl}\\
 & =\begin{cases}
\delta_{ik} & k\leq A\\
0 & k>A
\end{cases}
\end{align*}
$$

显然有 $\rho^{2}=\rho$。

我们可以发现，$\rho$ 实际上为投影到占据态空间的投影算符，因此我们可以把前面的 $f_{\text{ph}}$ 和 $f_{\text{hp}}$ 改写成：

$$
\begin{align*}
f_{\text{hp}} & =\rho h(1-\rho)\\
f_{\text{ph}} & =(1-\rho)h\rho
\end{align*}
$$

于是 Hartree-Fock 方程变为：

$$
\begin{align*}
\rho f & =\rho f\rho\\
f\rho & =\rho f\rho
\end{align*}
$$

这等价于：

$$
[\rho,f]=0
$$
