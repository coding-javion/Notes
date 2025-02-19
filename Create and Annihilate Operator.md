# 产生湮灭算符

## 产生湮灭算符

### 玻色子情形

我们先考虑一个算符 $a$，先不管它是什么空间中的，只要它满足如下的关系，我们就称其为湮灭算符，其共轭 $a^{\dagger}$ 称为产生算符：

$$
[a,a^{\dagger}]=1
$$

我们称厄米算符 $a^{\dagger}a$ 为粒子数算符。其命名的原因会在其性质清晰后自明。我们的任务是找到其本征值和本征矢，为此我们先假设其本征矢为 $|\alpha\rangle$：

$$
a^{\dagger}a|\alpha\rangle=\alpha|\alpha\rangle
$$

并假设其是归一化的。于是有：

$$
\begin{aligned}
\alpha & =\langle\alpha|a^{\dagger}a|\alpha\rangle=\lVert a|\alpha\rangle\rVert^{2}\geq0
\end{aligned}
$$

这意味着所有的本征值都是实的且非负的。此外，利用对易子的基本性质可以得到：

$$
\begin{aligned}
(a^{\dagger}a)a|\alpha\rangle & =a(a^{\dagger}a-1)|\alpha\rangle=(\alpha-1)a|\alpha\rangle\\
(a^{\dagger}a)a^{\dagger}|\alpha\rangle & =a^{\dagger}(a^{\dagger}a+1)|\alpha\rangle=(\alpha+1)a^{\dagger}|\alpha\rangle
\end{aligned}
$$

由此可见，$a|\alpha\rangle,a^{\dagger}|\alpha\rangle$ 都是 $a^{\dagger}a$ 的本征矢，且本征值分别为 $\alpha-1$ 和 $\alpha+1$，此外，还可以推出：

$$
\begin{aligned}
\lVert a|\alpha\rangle\rVert & =\sqrt{\alpha}\\
\lVert a^{\dagger}|\alpha\rangle\rVert & =\sqrt{\alpha+1}
\end{aligned}
$$

假设 $a^{n}|\alpha\rangle\neq0$，那么 $a^{n}|\alpha\rangle$ 的本征值为 $\alpha-n$，显然 $n$ 不能任意大，因为前面已经推得了本征值是一定大于 0 的。于是我们一定有：

$$
a^{n}|\alpha\rangle\neq0\qquad but\qquad a^{n+1}|\alpha\rangle=0
$$

令 $|\alpha-n\rangle$ 表示归一化的 $a^{n}|\alpha\rangle$，于是有 $\lVert a|\alpha-n\rangle\rVert=\sqrt{\alpha-n}=0$，即 $\alpha=n$。这意味着 $a^{\dagger}a$ 的本征值一定为非负整数，并且存在一个基态使得 $a|0\rangle=0$。通过不断将 $a^{\dagger}$ 作用到上面，即可得到所有的正整数本征值和本征矢。

假设 $|n\rangle$ 是归一化的，则有：

$$
\begin{aligned}
a|n\rangle & =\sqrt{n}|n-1\rangle\\
a^{\dagger}|n\rangle & =\sqrt{n+1}|n+1\rangle
\end{aligned}
$$

由此我们也可以得到 $|n\rangle$ 的表达式，即：

$$
|n\rangle=\frac{1}{\sqrt{n!}}(a^{\dagger})^{n}|0\rangle
$$

此外，也可以验证（亦可直接得到）：

$$
\begin{aligned}
\langle m|n\rangle & =\delta_{mn}\\
a^{\dagger}a|n\rangle & =n|n\rangle
\end{aligned}
$$

### 费米子情形

如果是：

$$
\begin{aligned}
\{a,a^{\dagger}\} & =1\\
\{a,a\}=\{a^{\dagger},a^{\dagger}\} & =0
\end{aligned}
$$

我们仍然寻找 $a^{\dagger}a$ 的本征值和本征矢，同样假设其本征值和本征矢为 $\alpha$ 和 $|\alpha\rangle$。本征值同样是非负的，利用反对易子的基本性质，可得：

$$
a^{2}=a^{\dagger2}=0
$$

还可以得到：

$$
\begin{aligned}
a^{\dagger}aa|\alpha\rangle & =a\left(-a^{\dagger}a-1\right)|\alpha\rangle=(-\alpha+1)a|\alpha\rangle=0\\
a^{\dagger}aa^{\dagger}|\alpha\rangle & =a^{\dagger}(-a^{\dagger}a+1)|\alpha\rangle=(-\alpha+1)a^{\dagger}|\alpha\rangle=a^{\dagger}|\alpha\rangle
\end{aligned}
$$

其中最后一个等号是直接由前面的性质得到的。由第一个和第二个等式我们分别可以得到：

$$
\begin{aligned}
a|\alpha\rangle=0 & \text{或}\alpha=1\\
a^{\dagger}|\alpha\rangle=0 & \text{或}\alpha=0
\end{aligned}
$$

由此可见该费米子的反对易关系下，只有两种可能的情况：

- $a|\alpha\rangle=0\ \text{且}\ \alpha=0$，$|\alpha\rangle$ 可以解释为粒子数为 $0$ 的态。
- $a^{\dagger}|\alpha\rangle=0\ \text{且}\ \alpha=1$，$|\alpha\rangle$ 可以解释为粒子数为 $1$ 的态。

有一种特殊的情况是需要特意排除的：

$$
a|\alpha\rangle=0\text{且}a^{\dagger}|\alpha\rangle=0\text{且}\alpha=0
$$

显然，将 $\{a,a^{\dagger}\}=1$ 作用到 $|\alpha\rangle$ 中，会得到 $|\alpha\rangle$ 等同于 $0$ 矢量，这是没有意义的。

## 全同粒子体系

### Fock 空间

我们先从可分辨粒子开始，如果 $|\psi_{1}\rangle,\cdots,|\psi_{n}\rangle$ 是单粒子态，那么 $|\psi\rangle$ 就描述了 $n$ 个粒子的态：

$$
|\psi\rangle=|\psi_{1}\rangle\otimes\cdots\otimes|\psi_{n}\rangle
$$

其中第 $i$ 个粒子在 $|\psi_{i}\rangle$。考虑 $|\varphi\rangle=|\varphi_{1}\rangle\otimes\cdots\otimes|\varphi_{n}\rangle$，我们可以定义内积 $\langle\varphi|\psi\rangle$：

$$
\langle\varphi|\psi\rangle=\langle\varphi_{1}|\psi_{1}\rangle\cdots\langle\varphi_{n}|\psi_{n}\rangle
$$

描述 $n$ 个可分辨粒子的 Hilbert 空间 $\mathcal{H}^{n}$ 由所有的 $|\psi\rangle$ 这样的单粒子态张量积构成的张量张成。考虑第 $i$ 个粒子在 $\boldsymbol{x}_{i}$ 处的态 $|\boldsymbol{x}_{1}\rangle\cdots|\boldsymbol{x}_{n}\rangle$，自然，这样的态构成了 $\mathcal{H}^{n}$ 空间的一组正交归一完备基：

$$
\begin{aligned}
(\langle\boldsymbol{x}_{1}|\cdots\langle\boldsymbol{x}_{n}|)(|\boldsymbol{y}_{1}\rangle\cdots|\boldsymbol{y}_{n}\rangle)=\delta^{3}(\boldsymbol{x}_{1}-\boldsymbol{y}_{1})\cdots\delta^{3}(\boldsymbol{x}_{n}-\boldsymbol{y}_{n})\\
\int\mathrm{d}^{3}\boldsymbol{x}_{1}\cdots\mathrm{d}^{3}\boldsymbol{x}_{n}(|\boldsymbol{x}_{1}\rangle\cdots|\boldsymbol{x}_{n}\rangle)(\langle\boldsymbol{x}_{1}|\cdots\langle\boldsymbol{x}_{n}|)=1
\end{aligned}
$$

 坐标表象下 $n$ 粒子态可以写为：

$$
\begin{aligned}
\psi(\boldsymbol{x}_{1},\cdots,\boldsymbol{x}_{n}) & =(\langle\boldsymbol{x}_{1}|\cdots\langle\boldsymbol{x}_{n}|)|\psi\rangle\\
 & =\psi_{1}(\boldsymbol{x}_{1})\cdots\psi_{n}(\boldsymbol{x}_{n})
\end{aligned}
$$

这里 $\psi_{i}(\boldsymbol{x}_{i})$ 等同于 $\langle\boldsymbol{x}_{i}|\psi_{i}\rangle$。

接下来考虑不可分辨粒子，为了区分玻色子和费米子，我们定义一个符号 $\zeta$，其在粒子为玻色子的时候为 $+1$，在粒子为费米子的时候为 $-1$。于是 $n$ 不可分辨粒子态的态矢量可以写为：

$$
|\psi_{1},\cdots,\psi_{n}\rangle=\frac{1}{\sqrt{n!}}\sum_{P}\zeta^{P}|\psi_{P(1)}\rangle\cdots|\psi_{P(n)}\rangle
$$

其中 $P$ 为 $n$ 阶置换群的一个元素，$\sum_{P}$ 表示对置换群所有元素求和，$\zeta^{P}$ 对于 $P$ 为偶置换的情况为 $1$，对于奇置换的情况则为 $-1$。自然，描述 $n$ 个不可分辨粒子的 $\mathcal{H}^{n}$ 的子空间就由这样的态矢量张成。我们称之为 $n$ 粒子 Fock 空间 $\mathcal{F}^{n}$。

$\mathcal{F}^{n}$ 空间内积的定义可以从之前的定义得到：

$$
\langle\varphi_{1},\cdots,\varphi_{n}|\psi_{1},\cdots,\psi_{n}\rangle=\begin{vmatrix}\langle\varphi_{1}|\psi_{1}\rangle & \cdots & \langle\varphi_{1}|\psi_{n}\rangle\\
\vdots & \ddots & \vdots\\
\langle\varphi_{n}|\psi_{1}\rangle & \cdots & \langle\varphi_{n}|\psi_{n}\rangle
\end{vmatrix}_{\zeta}
$$

其中，对于任意一个矩阵 $A$，$\left|A\right|_{\zeta}$ 的定义为：

$$
\left|A\right|_{\zeta}=\sum_{P}\zeta^{P}A_{1P(1)}\cdots A_{nP(n)}
$$

$\zeta$ 为 $-1$ 时该式为行列式，为 $+1$ 时称积和式。

*Proof.* 直接计算即可：

$$
\begin{aligned}
\langle\varphi_{1},\cdots,\varphi_{n}|\psi_{1},\cdots,\psi_{n}\rangle & =\frac{1}{n!}\sum_{P}\sum_{Q}\zeta^{P}\zeta^{Q}\langle\varphi_{P(1)}|\psi_{Q(1)}\rangle\cdots\langle\varphi_{P(n)}|\psi_{Q(n)}\rangle\\
 & =\frac{1}{n!}\sum_{P}\sum_{Q}\zeta^{P^{-1}Q}\langle\varphi_{1}|\psi_{P^{-1}Q(1)}\rangle\cdots\langle\varphi_{n}|\psi_{P^{-1}Q(n)}\rangle\\
 & =\frac{1}{n!}\sum_{P}\sum_{R}\zeta^{R}\langle\varphi_{1}|\psi_{R(1)}\rangle\cdots\langle\varphi_{n}|\psi_{R(n)}\rangle\\
 & =\sum_{R}\zeta^{R}\langle\varphi_{1}|\psi_{R(1)}\rangle\cdots\langle\varphi_{n}|\psi_{R(n)}\rangle\\
 & =\left|\langle\varphi_{i}|\psi_{j}\rangle\right|_{\zeta}
\end{aligned}
$$

利用上述表达式，我们可以得到坐标表象下的波函数：

$$
\psi(\boldsymbol{x}_{1},\cdots,\boldsymbol{x}_{n})=\begin{vmatrix}\psi_{1}(\boldsymbol{x}_{1}) & \cdots & \psi_{1}(\boldsymbol{x}_{n})\\
\vdots & \ddots & \vdots\\
\psi_{n}(\boldsymbol{x}_{1}) & \cdots & \psi_{n}(\boldsymbol{x}_{n})
\end{vmatrix}_{\zeta}
$$

对于费米子的情况，这被称为 Slater 行列式。

现在我们用 $\{|\alpha\rangle\}=\{|1\rangle,|2\rangle,\cdots\}$ 表示一组正交归一完备的单粒子基矢。此种情况下上述态矢量确实是正交的，但并未归一化，因此我们现在计算一下得到其归一化的形式：

$$
\begin{aligned}
\frac{|\alpha_{1},\cdots,\alpha_{n}\rangle}{\sqrt{n_{1}!n_{2}!\cdots}} & (\alpha_{1}\leq\cdots\leq\alpha_{n})\qquad bosons\\
|\alpha_{1},\cdots,\alpha_{n}\rangle & (\alpha_{1}<\cdots<\alpha_{n})\qquad fermions
\end{aligned}
$$

*Proof.* 计算上述态矢量的模即可：

$$
\begin{aligned}
\langle\alpha_{1},\cdots,\alpha_{n}|\alpha_{1},\cdots\alpha_{n}\rangle & =\sum_{P}\zeta^{P}\langle\alpha_{1}|\alpha_{P(1)}\rangle\cdots\langle\alpha_{n}|\alpha_{P(n)}\rangle\\
 & =\begin{cases}
n_{1}!n_{2}!\cdots & bosons\\
1 & fermions
\end{cases}
\end{aligned}
$$

两种情况下，完备性都可以表述为：

$$
\frac{1}{n!}\sum_{\alpha_{1}}\cdots\sum_{\alpha_{n}}|\alpha_{1},\cdots,\alpha_{n}\rangle\langle\alpha_{1},\cdots,\alpha_{n}|=1
$$

这里，$\alpha_{i}$ 的范围没有限制，但对于费米子而言，不符合泡利不相容原理的态矢量为 $0$。显然，$1/n!$ 的出现是因为这个表达方式太蠢了，以至于 $n!$ 个不同的表达方式实际上都是一个态矢量。[^1]

现在，我们已经构建了 $\mathcal{F}^{n}$ 空间，接下来，为了研究粒子数可以变化的情况，我们把这所有的 $\mathcal{F}^{n}$ 空间直和起来，得到 Fock 空间 $\mathcal{F}$，其中的一个态矢量具有如下形式：

$$
|\psi\rangle=|\psi^{(0)}\rangle\oplus|\psi^{(1)}\rangle\oplus|\psi^{(2)}\rangle\oplus\cdots
$$

其中，$|\psi^{(n)}\rangle$ 为一个 $n$ 粒子态。现在我们可以定义两个态矢量的内积：

$$
\langle\varphi|\psi\rangle=\langle\varphi^{(0)}|\psi^{(0)}\rangle+\langle\varphi^{(1)}|\psi^{(1)}\rangle+\cdots
$$

完备性可以表述为：

$$
\sum_{n=0}^{\infty}\frac{1}{n!}\sum_{\alpha_{1},\cdots,\alpha_{n}}|\alpha_{1},\cdots,\alpha_{n}\rangle\langle\alpha_{1},\cdots,\alpha_{n}|=1
$$

至此，我们得到了 Fock 空间 $\mathcal{F}$------ 态矢的定义、内积的定义与一组正交归一完备基。

### 产生湮灭算符

之前我们提到过，这个表示方式很蠢，现在我们来试着换一个聪明点的表示方式。我们尝试定义多粒子空间下的产生湮灭算符，首先是产生算符：

$$
a^{\dagger}(\varphi)|\psi_{1},\cdots,\psi_{n}\rangle=|\varphi,\psi_{1},\cdots,\psi_{n}\rangle
$$

而湮灭算符是它的共轭，我们由此求出湮灭算符的表达式（在此省略了一部分逗号）：[^2]

$$
\begin{aligned}
 & \langle\chi_{1}\cdots\chi_{n-1}|a(\varphi)|\psi_{1}\cdots\psi_{n}\rangle\\
= & \langle\psi_{1}\cdots\psi_{n}|a^{\dagger}(\varphi)|\chi_{1}\cdots\chi_{n-1}\rangle^{*}\\
= & \langle\psi_{1}\cdots\psi_{n}|\varphi\chi_{1}\cdots\chi_{n-1}\rangle^{*}\\
= & \begin{vmatrix}\langle\psi_{1}|\varphi\rangle & \langle\psi_{1}|\chi_{1}\rangle & \cdots & \langle\psi_{1}|\chi_{n-1}\rangle\\
\vdots & \vdots & \vdots & \vdots\\
\langle\psi_{n}|\varphi\rangle & \langle\psi_{n}|\chi_{1}\rangle & \cdots & \langle\psi_{n}|\chi_{n-1}\rangle
\end{vmatrix}_{\zeta}^{*}\\
= & \left\{ \sum_{k=1}^{n}\zeta^{k-1}\langle\psi_{k}|\varphi\rangle\begin{vmatrix}\langle\psi_{1}|\chi_{1}\rangle & \cdots & \langle\psi_{1}|\chi_{n-1}\rangle\\
\vdots & (no\ \psi_{k}) & \vdots\\
\langle\psi_{n}|\chi_{1}\rangle & \cdots & \langle\psi_{n}|\chi_{n-1}\rangle
\end{vmatrix}_{\zeta}\right\} ^{*}\\
= & \sum_{k=1}^{n}\zeta^{k-1}\langle\psi_{k}|\chi\rangle^{*}\langle\psi_{1}\cdots(no\ \psi_{k})\cdots\psi_{n}|\chi_{1}\cdots\chi_{n-1}\rangle^{*}\\
= & \sum_{k=1}^{n}\zeta^{k-1}\langle\varphi|\psi_{k}\rangle\langle\chi_{1}\cdots\chi_{n-1}|\psi_{1}\cdots(no\ \psi_{k})\cdots\psi_{n}\rangle
\end{aligned}
$$

于是最终得到了湮灭算符的表达式：

$$
a(\varphi)|\psi_{1}\cdots\psi_{n}\rangle=\sum_{k=1}^{n}\zeta^{k-1}\langle\varphi|\psi_{k}\rangle|\psi_{1}\cdots(no\ \psi_{k})\cdots\psi_{n}\rangle
$$

从产生算符的表达式，我们可以得到：

$$
a^{\dagger}(\varphi_{1})a^{\dagger}(\varphi_{2})=\zeta a^{\dagger}(\varphi_{2})a^{\dagger}(\varphi_{1})
$$

由此得：

$$
[a^{\dagger}(\varphi_{1}),a^{\dagger}(\varphi_{2})]_{-\zeta}=0
$$

其中，$[A,B]_{-\zeta}=AB-\zeta BA$，为对易子或反对易子。对此式取共轭即得到：

$$
[a(\varphi_{1}),a(\varphi_{2})]_{-\zeta}=0
$$

接下来计算 $[a(\varphi_{1}),a^{\dagger}(\varphi_{2})]_{-\zeta}$，为此，首先计算：

$$
\begin{aligned}
 & a(\varphi_{1})a^{\dagger}(\varphi_{2})|\psi_{1}\cdots\psi_{n}\rangle\\
= & a(\varphi_{1})|\varphi_{2},\psi_{1}\cdots\psi_{n}\rangle\\
= & \langle\varphi_{1}|\varphi_{2}\rangle|\psi_{1}\cdots\psi_{n}\rangle+\sum_{k=1}^{n}\zeta^{k}\langle\varphi_{1}|\psi_{k}\rangle|\varphi_{2}\psi_{1}\cdots(no\ \psi_{k})\cdots\psi_{n}\rangle
\end{aligned}
$$

接下来计算：

$$
\begin{aligned}
 & a^{\dagger}(\varphi_{2})a(\varphi_{1})|\psi_{1}\cdots\psi_{n}\rangle\\
= & a^{\dagger}(\varphi_{2})[\sum_{k=1}^{n}\zeta^{k-1}\langle\varphi_{1}|\psi_{k}\rangle|\psi_{1}\cdots(no\ \psi_{k})\cdots\psi_{n}\rangle]\\
= & \sum_{k=1}^{n}\zeta^{k-1}\langle\varphi_{1}|\psi_{k}\rangle|\varphi_{2}\psi_{1}\cdots(no\ \psi_{k})\cdots\psi_{n}\rangle
\end{aligned}
$$

于是可以得到：

$$
[a(\varphi_{1}),a^{\dagger}(\varphi_{2})]_{-\zeta}=\langle\varphi_{1}|\varphi_{2}\rangle
$$

这就是基本对易关系。如果仍然用 $\{|\alpha\rangle\}=\{|1\rangle,|2\rangle,\cdots\}$ 表示一组正交归一完备的单粒子基矢，那么可以得到：

$$
[a_{\alpha},a_{\beta}^{\dagger}]_{-\zeta}=\delta_{\alpha\beta}
$$

事实上，复杂的全同粒子空间的性质被编码在了这几个简单的基本对易关系中。可以证明，我们也可以从简单的对易关系出发得到上面的一切，就如同我们对最简单的情况所做的那样。

### 基矢与基变换

#### 玻色子基矢

在正交归一完备的单粒子基矢情况下，我们可以用更为简便的方式表示基矢：

$$
|n_{1}n_{2}\cdots\rangle=\frac{|1,\cdots,1,2,\cdots,2,\cdots\rangle}{\sqrt{n_{1}!n_{2}!\cdots}}
$$

其中，$n_{\alpha}$ 表示 $\alpha$ 在右矢中出现的次数。用这种表示方式我们可以得到：

$$
\begin{aligned}
a_{\alpha}^{\dagger}|n_{1}n_{2}\cdots n_{\alpha}\cdots\rangle & =\sqrt{n_{\alpha}+1}|n_{1}n_{2}\cdots n_{\alpha}+1\cdots\rangle\\
a_{\alpha}|n_{1}n_{2}\cdots n_{\alpha}\cdots\rangle & =\sqrt{n_{\alpha}}|n_{1}n_{2}\cdots n_{\alpha-1}\cdots\rangle
\end{aligned}
$$

事实上部分地方正是用上述关系作为玻色子产生湮灭算符的定义。基本对易关系仍为：

$$
[a_{\alpha},a_{\beta}]=[a_{\alpha}^{\dagger},a_{\beta}^{\dagger}]=0\qquad[a_{\alpha},a_{\beta}^{\dagger}]=\delta_{\alpha\beta}
$$

#### 费米子基矢

利用原本的符号，我们有：

$$
\begin{aligned}
a_{\alpha}^{\dagger}|\alpha_{1},\cdots,\alpha_{n}\rangle & =|\alpha,\alpha_{1},\cdots,\alpha_{n}\rangle\\
a_{\alpha}|\alpha_{1},\cdots,\alpha_{n}\rangle & =\sum_{k=1}^{n}(-1)^{k-1}\delta_{\alpha\alpha_{k}}|\alpha_{1},\cdots,\alpha_{k-1},\alpha_{k+1},\cdots,\alpha_{n}\rangle
\end{aligned}
$$

我们也可以用同玻色子一样的符号来表示基矢：

$$
|n_{1}n_{2}\cdots\rangle=|\alpha_{1},\alpha_{2}\cdots\rangle
$$

$n_{\alpha}$ 仍然表示 $\alpha$ 在右矢中出现的次数。如果 $n_{\alpha}$ 等于 $0$，那么 $a_{\alpha}^{\dagger}$ 使之变为 1，$a_{\alpha}$ 使态矢变为 0。而如果 $n_{\alpha}$ 等于 1，那么 $a_{\alpha}^{\dagger}$ 会使态矢变为 0，但是 $a_{\alpha}$ 会使 $n_{\alpha}$ 变为 $0$。凡是不使态矢变为 $0$ 的，均可能改变态矢的符号，相当于在前面乘上 $(-1)^{\sum_{k<i}n_{i}}$。

部分地方用上述关系作为费米子产生湮灭算符的定义。基本对易关系仍为：

$$
[a_{\alpha},a_{\beta}]_{+}=[a_{\alpha}^{\dagger},a_{\beta}^{\dagger}]=0\qquad[a_{\alpha},a_{\beta}^{\dagger}]_{+}=\delta_{\alpha\beta}
$$

#### 基变换

当我们变换基矢时，产生湮灭算符如何变化？如果：

$$
|\chi\rangle=\alpha|\psi\rangle+\beta|\varphi\rangle
$$

则：

$$
\begin{aligned}
a^{\dagger}(\chi) & =\alpha a^{\dagger}(\psi)+\beta a^{\dagger}(\varphi)\\
a(\chi) & =\alpha^{*}a(\psi)+\beta^{*}a(\varphi)
\end{aligned}
$$

上面的公式意味着产生算符如同右矢那般变换，而湮灭算符如同左矢那般变换。于是，当对基矢做如下 Fourier 变换时：

$$
|\boldsymbol{k}\rangle=\int\mathrm{d}\boldsymbol{x}\mathrm{e}^{-\mathrm{i}\boldsymbol{k}\cdot\boldsymbol{x}}|\boldsymbol{x}\rangle
$$

 产生算符和湮灭算符的 Fourier 变换我们就定义为：

$$
\begin{aligned}
a^{\dagger}(\boldsymbol{k}) & =\int\mathrm{d}\boldsymbol{x}\,a^{\dagger}(\boldsymbol{x})\mathrm{e}^{-\mathrm{i}\boldsymbol{k}\cdot\boldsymbol{x}}\\
a(\boldsymbol{k}) & =\int\mathrm{d}\boldsymbol{x}\,a(\boldsymbol{x})\mathrm{e}^{\mathrm{i}\boldsymbol{k}\cdot\boldsymbol{x}}
\end{aligned}
$$

## 用产生湮灭算符表示算符

我们考虑一个算符作用到单粒子上的 $A^{(1)}$，我们想找到一个算符 $A$，它代表把 $A^{(1)}$ 算符作用到所有的粒子上，即如果我们有一个 $n$ 粒子态：

$$
|\psi\rangle=|\psi_{1};\cdots;\psi_{n}\rangle=|\psi_{1}\rangle\times\cdots\times|\psi_{n}\rangle
$$

我们想让 $A|\psi\rangle$ 满足：

$$
\begin{aligned}
A|\psi\rangle= & A^{(1)}|\psi_{1}\rangle\times|\psi_{2}\rangle\times\cdots\times|\psi_{n}\rangle+|\psi_{1}\rangle\times A^{(1)}|\psi_{2}\rangle\times\cdots\times|\psi_{n}\rangle\\
 & +\cdots+|\psi_{1}\rangle\times|\psi_{2}\rangle\times\cdots\times A^{(1)}|\psi_{n}\rangle
\end{aligned}
$$

这意味着，如果 $|\psi_{i}\rangle$ 是 $A^{(1)}$ 算符的本征值为 $a_{i}$ 的本征矢，那么有：

$$
A|\psi\rangle=(a_{1}+\cdots+a_{n})|\psi\rangle
$$

考虑 $A^{(1)}=|\alpha\rangle\langle\beta|$ 的情况，此时不再考虑可分辨粒子态，而是考虑不可分辨粒子：

$$
|\psi\rangle=|\psi_{1},\cdots,\psi_{n}\rangle=\frac{1}{\sqrt{n!}}\sum_{P}\zeta^{P}|\psi_{P(1)}\rangle\cdots|\psi_{P(n)}\rangle
$$

将 $A$ 作用到该态上得到：

$$
\begin{aligned}
A|\psi\rangle & =\frac{1}{\sqrt{n!}}\sum_{P}\zeta^{P}(\langle\beta|\psi_{P(1)}\rangle|\alpha\rangle\cdots|\psi_{P(n)}\rangle+\cdots+\langle\beta|\psi_{P(n)}\rangle|\psi_{P(1)}\rangle\cdots|\alpha\rangle)\\
 & =\frac{1}{\sqrt{n!}}\sum_{P}\zeta^{P}(\sum_{i=1}^{n}\langle\beta|\psi_{i}\rangle|\psi_{P(1)}\rangle\cdots|\alpha\rangle\cdots|\psi_{P(n)}\rangle)\\
 & =\sum_{i=1}^{n}\langle\beta|\psi_{i}\rangle\left(\frac{1}{\sqrt{n!}}\sum_{P}\zeta^{P}|\psi_{P(1)}\rangle\cdots|\alpha\rangle\cdots|\psi_{P(n)}\rangle\right)
\end{aligned}
$$

其中，$|\alpha\rangle$ 在第 $P(i)$ 个位置上，这是因为其完全继承了 $|\psi_{i}\rangle$ 的位置。因此得到：

$$
\begin{aligned}
A|\psi\rangle & =\langle\beta|\psi_{1}\rangle|\alpha,\psi_{2},\cdots,\psi_{n}\rangle+\langle\beta|\psi_{2}\rangle|\psi_{2},\alpha,\cdots,\psi_{n}\rangle\\
 & \phantom{=}+\cdots+\langle\beta|\psi_{n}\rangle|\psi_{1},\cdots,\psi_{n},\alpha\rangle
\end{aligned}
$$

而我们又可以验证：

$$
a^{\dagger}(\alpha)a(\beta)|\psi\rangle=\sum_{k=1}^{n}\zeta^{k-1}\langle\beta|\psi_{k}\rangle|\alpha,\psi_{1},\cdots,(no\ \psi_{k}),\cdots,\psi_{n}\rangle
$$

并且有：

$$
\zeta^{k-1}|\alpha,\psi_{1},\cdots,(no\ \psi_{k}),\cdots,\psi_{n}\rangle=|\psi_{1},\cdots,\psi_{k-1},\alpha,\psi_{k+1},\cdots,\psi_{n}\rangle
$$

所以当 $A^{(1)}=|\alpha\rangle\langle\beta|$ 时，$A=a^{\dagger}(\alpha)a(\beta)$，因此，我们可以任取一组基，将单粒子算符 $A^{(1)}$ 写成如下形式：

$$
A^{(1)}=\sum_{\alpha,\beta}|\alpha\rangle\langle\alpha|A^{(1)}|\beta\rangle\langle\beta|=\sum_{\alpha,\beta}A_{\alpha\beta}^{(1)}|\alpha\rangle\langle\beta|
$$

从而对应的算符 $A$ 为：

$$
A=\sum_{\alpha,\beta}A_{\alpha\beta}^{(1)}a^{\dagger}(\alpha)a(\beta)
$$

我们考虑一种特殊的二体算符 $\hat{V}^{(2)}$，它是对称的，且其作用到两个态矢的张量积 $|\psi_{i};\psi_{j}\rangle$ 上有：

$$
\hat{V}^{(2)}|\psi_{i};\psi_{j}\rangle=V^{(2)}(\psi_{i},\psi_{j})|\psi_{i};\psi_{j}\rangle
$$

同上面的考虑，我们想找到一个算符 $V$，使其作用到态 $|\psi\rangle=|\psi_{1};\cdots;\psi_{n}\rangle$ 上时有：

$$
V|\psi\rangle=\frac{1}{2}\sum_{i\neq j}V^{(2)}(\psi_{i},\psi_{j})|\psi_{1};\cdots;\psi_{n}\rangle
$$

首先我们考虑一个简单的情况：

$$
V^{(2)}=|\beta_{2};\alpha_{2}\rangle\langle\alpha_{1};\beta_{1}|
$$

这里的计算同单体的情况完全相同：

$$
\begin{aligned}
V|\psi\rangle & =\frac{1}{\sqrt{n!}}\sum_{P}\zeta^{P}\frac{1}{2}\sum_{i\neq j}\langle\alpha_{1}|\psi_{P(i)}\rangle\langle\beta_{1}|\psi_{P(j)}\rangle|\psi_{P(1)}\rangle\cdots|\alpha_{2}\rangle\cdots|\beta_{2}\rangle\cdots|\psi_{n}\rangle\\
 & =\frac{1}{2}\sum_{i\neq j}\langle\alpha_{1}|\psi_{i}\rangle\langle\beta_{1}|\psi_{j}\rangle|\psi_{1},\cdots,\alpha_{2},\cdots,\beta_{2},\cdots,\psi_{n}\rangle
\end{aligned}
$$

我们又可以验证：

$$
\begin{aligned}
 & a^{\dagger}(\alpha_{2})a^{\dagger}(\beta_{2})a(\beta_{1})a(\alpha_{1})|\psi_{1},\cdots,\psi_{n}\rangle\\
= & a^{\dagger}(\alpha_{2})a^{\dagger}(\beta_{2})a(\beta_{1})\sum_{i=1}^{n}\zeta^{i-1}\langle\alpha_{1}|\psi_{i}\rangle|\psi_{1},\cdots(no\ \psi_{i})\cdots\psi_{n}\rangle\\
= & a^{\dagger}(\alpha_{2})a^{\dagger}(\beta_{2})\sum_{i\neq j}\zeta^{i-1}\eta_{ij}\langle\alpha_{1}|\psi_{i}\rangle\langle\beta_{1}|\psi_{j}\rangle|\psi_{1},\cdots(no\ \psi_{i},\psi_{j})\cdots\psi_{n}\rangle\\
= & \sum_{i\neq j}\zeta^{i-1}\eta_{ij}\langle\alpha_{1}|\psi_{i}\rangle\langle\beta_{1}|\psi_{j}\rangle|\alpha_{2},\beta_{2},\psi_{1},\cdots(no\ \psi_{i},\psi_{j})\cdots\psi_{n}\rangle\\
= & \sum_{i\neq j}\langle\alpha_{1}|\psi_{i}\rangle\langle\beta_{1}|\psi_{j}\rangle|\psi_{1},\cdots,\alpha_{2},\cdots,\beta_{2},\cdots,\psi_{n}\rangle
\end{aligned}
$$

其中：

$$
\eta_{ij}=\begin{cases}
\zeta^{j-1} & if\ i>j\\
\zeta^{j} & if\ i<j
\end{cases}
$$

因此在此种情况下，$V=\frac{1}{2}a^{\dagger}(\alpha_{2})a^{\dagger}(\beta_{2})a(\beta_{1})a(\alpha_{1})$。

我们可以取一组基，将双粒子算符写成下面的形式：

$$
V^{(2)}=\sum_{\alpha_{1},\alpha_{2},\beta_{1},\beta_{2}}\langle\alpha_{2};\beta_{2}|V^{(2)}|\beta_{1};\alpha_{1}\rangle|\beta_{2};\alpha_{2}\rangle\langle\alpha_{1};\beta_{1}|
$$

此时对应的多粒子算符为：

$$
V=\frac{1}{2}\sum_{\alpha_{1},\alpha_{2},\beta_{1},\beta_{2}}\langle\alpha_{2};\beta_{2}|V^{(2)}|\beta_{1};\alpha_{1}\rangle a^{\dagger}(\alpha_{2})a^{\dagger}(\beta_{2})a(\beta_{1})a(\alpha_{1})
$$

往往可以简写为：

$$
V=\frac{1}{2}\sum_{i,j,k,l}V_{ijkl}a_{i}^{\dagger}a_{j}^{\dagger}a_{k}a_{l}
$$

在坐标表象下，$V_{ijkl}$ 为：

$$
V_{ijkl}=\int\mathrm{d}^{3}\boldsymbol{x}_{1}\mathrm{d}^{3}\boldsymbol{x}_{2}\psi_{i}^{*}(\boldsymbol{x}_{1})\psi_{j}^{*}(\boldsymbol{x}_{2})V(\boldsymbol{x}_{1},\boldsymbol{x}_{2})\psi_{k}(\boldsymbol{x}_{2})\psi_{l}(\boldsymbol{x}_{1})
$$

[^1]: $n=0$ 的情况意味着态矢量为零阶张量，即标量，用 $|0\rangle$ 或 $|vac\rangle$ 表示，为真空态。
[^2]: 此处使用了行列式和积和式的展开，证明如下：
	
	$$
	\begin{aligned}
	\left|A\right|_{\zeta} & =\sum_{P}\zeta^{P}A_{1P(1)}\cdots A_{nP(n)}\\
	 & =\sum_{P}\zeta^{P}A_{iP(i)}A_{1P(1)}\cdots(no\ A_{iP(i)})\cdots A_{nP(n)}
	\end{aligned}
	$$
	
	$P$ 可以分解为保持 $P(i)$ 不动的 $n$ 部分。尽管这并不是子群，我们姑且将这些部分记为 $P/k$：
	
	$$
	\left|A\right|_{\zeta}=\sum_{k}\zeta^{k-i}A_{ik}\sum_{P/k}\zeta^{P+i-k}A_{1P(1)}\cdots(no\ A_{iP(i)})\cdots A_{nP(n)}
	$$
	
	定义新的置换 $Q=P/k$：
	
	$$
	Q=\begin{pmatrix}1 & 2 & \cdots & (no\ i) & \cdots & n\\
	P(1) & P(2) & \cdots & (no\ P(i)) & \cdots & P(n)
	\end{pmatrix}
	$$
	
	尽管这看起来并不合理（因为上下并不一样），但实际上这可以通过指标的重命名解决，即将所有 $i,P(i)$ 后面的指标提前一个。
	
	现在唯一的问题是上述 $\zeta^{P+i-k}$ 是否是 $\zeta^{Q}$。从逆序数的角度考虑，首先，把指标提前的操作不会改变这一值，所以仅剩的带来影响的操作是消除 $P(i)$，我们把这一步骤改为，首先将所有的 $P(j)$ 移到 $j$ 位置，然后消除 $P(i)$，再将其余的回到原位，于是此时消除 $P(i)$ 不会带来影响，第一步和第三步的操作，除了将 $P(i)$ 移动到 $i$ 位置的操作，其它操作都可以一一对应相反，于是总的来看，对 $\zeta^{P}$ 的影响只有移动这一操作，这一操作带来的影响恰好是时 $\zeta^{P}$ 变为 $\zeta^{P+i-k}$，于是有：
	
	$$
	\left|A\right|_{\zeta}=\sum_{k}\zeta^{k-i}A_{ik}\sum_{Q}\zeta^{Q}A_{1Q(1)}\cdots A_{nQ(n)}
	$$
	
	即：
	
	$$
	\left|A\right|_{\zeta}=\sum_{k}\zeta^{k-i}A_{ik}\begin{vmatrix}A_{11} & \cdots & (no\ A_{1k}) & \cdots & A_{1n}\\
	\vdots &  &  &  & \vdots\\
	(no\ A_{i1}) &  & \cdots &  & (no\ A_{in})\\
	\vdots &  &  &  & \vdots\\
	A_{n1} & \cdots & (no\ A_{nk}) & \cdots & A_{nn}
	\end{vmatrix}_{\zeta}
	$$


