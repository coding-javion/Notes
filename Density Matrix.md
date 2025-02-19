## 密度矩阵

如果一个大的系统空间 $\mathcal{F}$ 可以写成 $\mathcal{F}_{1}\otimes\mathcal{F}_{2}$。令 $|\varphi_{i}\rangle$ 为 $\mathcal{F}_{1}$ 的一组完备基，$|\theta_{i}\rangle$ 为 $\mathcal{F}_{2}$ 的一组完备基。则 $\mathcal{F}$ 中的态矢的一般形式为：

$$
|\psi\rangle=\sum_{ij}C_{ij}|\varphi_{i}\rangle|\theta_{j}\rangle
$$

现在，我们把 $\mathcal{F}_{1}$ 当做我们要考虑的系统，而 $\mathcal{F}_{2}$ 当做环境，用 $A$ 表示只作用在系统空间 $\mathcal{F}_{1}$ 上的算符，于是有：

$$
\langle A\rangle	=\langle\psi|A|\psi\rangle=\sum_{ii^{\prime}j}C_{ij}^{*}C_{i^{\prime}j}\langle\varphi_{i}|A|\varphi_{i^{\prime}}\rangle

\equiv\sum_{ii^{\prime}}\langle\varphi_{i}|A|\varphi_{i^{\prime}}\rangle\rho_{i^{\prime}i}
$$

其中，$\rho_{i^{\prime}i}$ 被称为密度矩阵，有：

$$
\rho_{i^{\prime}i}=\sum_{j}C_{ij}^{*}C_{i^{\prime}j}
$$

我们定义算符 $\rho$，使得 $\rho_{i^{\prime}i}=\langle\varphi_{i^{\prime}}|\rho|\varphi_{i}\rangle$，同样，$\rho$ 也仅作用在系统空间 $\mathcal{F}_{1}$ 上。于是我们有：

$$
\langle\psi|A|\psi\rangle	=\sum_{ii^{\prime}}\langle\varphi_{i}|A|\varphi_{i^{\prime}}\rangle\langle\varphi_{i^{\prime}}|\rho|\varphi_{i}\rangle

=\sum_{i}\langle\varphi_{i}|A\rho|\varphi_{i}\rangle=\mathop{\mathrm{Tr}}\rho A
$$

这是一个重要的关系，我们可以由此从密度矩阵直接得到算符的期待值。

由 $\rho$ 的定义可以看出， $\rho$ 是厄米的，因此我们可以用一组完备的正交归一本征矢 $|i\rangle$ 将其对角化：

$$
\rho=\sum_{i}\omega_{i}|i\rangle\langle i|
$$

如果我们令 $A$ 为 1，就可以求得：

$$
\sum_{i}\omega_{i}=\mathop{\mathrm{Tr}}\rho=\langle 1\rangle=\langle\psi|\psi\rangle=1
$$

如果我们令 $A$ 为 $|i^{\prime}\rangle\langle i^{\prime}|$，则有：

$$
\omega_{i^{\prime}}=\mathop{\mathrm{Tr}}\rho A=\langle\psi|A|\psi\rangle=\left|\langle\psi|i^{\prime}\rangle\right|^{2}\geq0
$$

我们发现，$\omega_{i}$ 恰好满足概率的性质，因此我们可以把它诠释成系统处在 $|i\rangle$ 态的概率。事实上：

$$
\langle A\rangle=\sum_{i}\omega_{i}\langle i|A|i\rangle
$$

我们发现的确可以如此诠释。

按照这种诠释，如果只有一个 $\omega_{i}$ 不为零，其它都为零，我们就说系统处于纯态，否则系统就处于混合态。一般来讲，如果我们研究的系统并不是完全孤立的，它就会处于混合态[^1]。

事实上，我们可以用更具有一般性的密度矩阵对量子力学进行重述，但为此我们首先要推导 $\rho$ 的运动方程。这并不是一件复杂的事，由于 $|i\rangle$ 都是我们描述的系统内部的态，薛定谔绘景下[^2]，其时间演化为：

$$
|i(t)\rangle=\mathrm{e}^{-\mathrm{i}Ht}|i(0)\rangle
$$

因此我们有：

$$
\rho(t)=\sum_{i}\omega_{i}\mathrm{e}^{-\mathrm{i}Ht}|i(0)\rangle\langle i(0)|\mathrm{e}^{\mathrm{i}Ht}=\mathrm{e}^{-\mathrm{i}Ht}\rho(0)\mathrm{e}^{\mathrm{i}Ht}
$$

对 $\rho (t)$ 求时间的导数，我们得到：

$$
\frac{\mathrm{d}\rho}{\mathrm{d}t}=-\mathrm{i}[H,\rho]
$$

这就是密度矩阵的运动方程——von Neumann 方程。该方程于密度矩阵，正如 Schrodinger 方程之于波函数。因此我们现在可以用密度矩阵重新表述量子力学：

- 任何系统均可以用密度矩阵 $\rho$ 来描述，其中 $\rho$ 具有 $\sum_{i}\omega_{i}|i\rangle\langle i|$ 这样的形式，其中：
	- $|i\rangle$ 是一组正交归一完备集
	- $\omega_{i}\geq0$
	- $\sum_{i}\omega_{i}=1$
- 给定算符 $A$，则 $A$ 的期待值由 $\langle A\rangle=\mathop{\mathrm{Tr}}\rho A$ 给出
- 密度矩阵的运动方程为：

$$
\frac{\mathrm{d}\rho}{\mathrm{d}t}=-\mathrm{i}[H,\rho]
$$

## 全同粒子的约化密度矩阵

由于实际中使用的密度矩阵经常是不归一化的，我们通常不假设它的归一性，但为了公式简洁我们仍假设归一性，为了得到非归一性的情况，只需要将 $\rho$ 替换为 $\rho/\mathop{\text{Tr}}\rho$。

### 单粒子约化密度矩阵

考虑计算一个单体算符 $\hat{A}=\sum_{ij}A_{ij}a_{i}^{\dagger}a_{j}$ 的期待值，我们有：

$$
\begin{align*}
\langle\hat{A}\rangle & =\mathop{\text{Tr}}(\rho\hat{A})=\mathop{\text{Tr}}(\rho\sum_{ij}A_{ij}a_{i}^{\dagger}a_{j})\\
 & =\sum_{ij}A_{ij}\mathop{\text{Tr}}(\rho a_{i}^{\dagger}a_{j})
\end{align*}
$$

我们定义单粒子约化密度矩阵：

$$
\rho_{ji}=\mathop{\text{Tr}}(\rho a_{i}^{\dagger}a_{j})
$$

则有：

$$
\langle\hat{A}\rangle=\sum_{ij}A_{ij}\rho_{ji}=\text{tr}(\rho A)
$$

这里为了方便我们用 $\mathop{\text{tr}}$ 表示对矩阵求迹，而 $\mathop{\text{Tr}}$ 表示对算符求迹。

需要注意的是，在纯态的情况下，单粒子约化密度矩阵可以写为 $\rho_{ji}=\langle\Psi|a_{i}^{\dagger}a_{j}|\Psi\rangle$ 。

坐标表象下，单粒子约化密度矩阵矩阵可以表示为：

$$
\rho(x,x^{\prime})=\frac{1}{(N-1)!}\int\rho(x,x_{2},\dots,x_{N};x^{\prime},x_{2},\dots,x_{N})\,\mathrm{d}x_{2}\dots\mathrm{d}x_{N}
$$

这里我们用 $\rho (x, x_{2},\dots, x_{N}; x^{\prime}, x_{2},\dots, x_{N})$ 表示 $\langle x, x_{2},\dots, x_{N}|\rho|x^{\prime}, x_{2},\dots, x_{N}\rangle$。

证明为：

$$
\begin{align*}
\rho(x,x^{\prime}) & =\mathop{\text{Tr}}(\rho a^{\dagger}(x^{\prime})a(x))=\mathop{\text{Tr}}(a(x)\rho a^{\dagger}(x^{\prime}))\\
 & =\frac{1}{(N-1)!}\int\mathrm{d}x_{2}\dots\mathrm{d}x_{N}\,\langle x_{2},\dots,x_{N}|a(x)\rho a^{\dagger}(x^{\prime})|x_{2},\dots,x_{N}\rangle\\
 & =\frac{1}{(N-1)!}\int\mathrm{d}x_{2}\dots\mathrm{d}x_{N}\,\langle x,x_{2},\dots,x_{N}|\rho|x^{\prime},x_{2},\dots,x_{N}\rangle\\
 & =\frac{1}{(N-1)!}\int\mathrm{d}x_{2}\dots\mathrm{d}x_{N}\,\rho(x,x_{2},\dots,x_{N};x^{\prime},x_{2},\dots,x_{N})
\end{align*}
$$

不难发现，$\rho (x, x)$ 相当于是在计算算符 $\hat{n}(x)$ 的期待值，即在 $x$ 处的粒子数期待值，因此可以由此得到粒子数密度。

在 Slater 行列式的情况，我们可以把粒子数密度直接计算出来：

$$
\begin{align*}
\rho(x_{1},x_{1}) & =\sum_{i}\omega_{i}\frac{1}{(N-1)!}\int\Psi_{i}(x_{1},x_{2},\dots,x_{N})\Psi_{i}^{*}(x_{1},x_{2},\dots,x_{N})\,\mathrm{d}x_{2}\dots\mathrm{d}x_{N}\\
 & =\sum_{i}\omega_{i}\frac{1}{(N-1)!}\sum_{PP^{\prime}}\zeta^{P+P^{\prime}}\int\prod_{j=1}^{N}\psi_{ij}(x_{P(j)})\prod_{k=1}^{N}\psi_{ik}^{*}(x_{P^{\prime}(k)})\,\mathrm{d}x_{2}\dots\mathrm{d}x_{N}\\
 & =\sum_{i}\omega_{i}\left(\sum_{j=1}^{N}\psi_{ij}(x_{1})\psi_{ij}^{*}(x_{1})\right)
\end{align*}
$$

纯态的时候且密度矩阵归一化的时候即有：

$$
\rho(x,x)=\sum_{i}|\psi_{i}(x)|^2
$$

### 两粒子约化密度矩阵

类似单体算符，考虑两体算符 $\hat{V}=\frac{1}{2}\sum_{ijkl}v_{ijkl}a_{i}^{\dagger}a_{j}^{\dagger}a_{l}a_{k}$ 的期待值，我们有：

$$
\begin{align*}
\langle\hat{V}\rangle & =\mathop{\text{Tr}}(\rho\hat{V})\\
 & =\frac{1}{2}\sum_{ijkl}v_{ijkl}\mathop{\text{Tr}}(\rho a_{i}^{\dagger}a_{j}^{\dagger}a_{l}a_{k})
\end{align*}
$$

我们定义两粒子约化密度矩阵[^3]：

$$
\rho_{klij}^{(2)}=\mathop{\text{Tr}}(\rho a_{i}^{\dagger}a_{j}^{\dagger}a_{l}a_{k})
$$

可以看出，两体算符的期待值可以由两粒子约化密度矩阵给出。

[^1]: 一般来说，如果系统是孤立的，那么可以用纯态描述。但严格来讲这只是人们的信念，是量子力学的基本假设，并不存在什么证明。
[^2]: 显然海森堡绘景下$\mathrm{d}\rho/\mathrm{d}t=0$。
[^3]: 这里的约定可能和其它地方不一样，但不影响本质。