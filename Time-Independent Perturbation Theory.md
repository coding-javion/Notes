## 形式微扰论

设想用一个比较小的算符 $V$ 微扰系统 $H_{0}$，进而得到哈密顿量为 $H=H_{0}+V$ 的新系统，我们用微扰论处理。

假设原来 $H_0$ 的本征态 $|\phi_{n}\rangle$ 变成了相应地本征态 $|\psi_{n}\rangle$，相应的本征值从 $\varepsilon_{n}$ 变成 $E_{n}$。如果我们能对投影算符 $P_{n}=|\phi_{n}\rangle\langle\phi_{n}|$ 和 $P_{n}^{\perp}$ 投影出来的空间进行正交分解[^1]，我们就可以有：

$$
\begin{align*}

|\psi_{n}\rangle=|\phi_{n}\rangle+P_{n}^{\perp}|\psi_{n}\rangle

\end{align*}
$$

当然，这种形式的 $\psi_{n}$ 是没有归一化的。

我们将本征态 $|\psi_{n}\rangle$ 所满足的本征值方程写为：

$$
\begin{align*}

(\zeta-H_{0})|\psi_{n}\rangle=(V-E_n+\zeta)|\psi_{n}\rangle

\end{align*}
$$

这里两边加了一个常数算符 $\zeta$ [^2]。引入格林算符：

$$
\begin{align*}

\mathcal{G}(\zeta)=\frac{1}{\zeta-H_{0}}

\end{align*}
$$

将其限制在 $P_{n}^{\perp}$ 限制的子空间上，即：

$$
\begin{align*}

\mathcal{G}^{\perp}(\zeta)=P_{n}^{\perp}\frac{1}{\zeta-H_{0}}P_{n}^{\perp}\equiv\frac{P_{n}^{\perp}}{\zeta-H_{0}}

\end{align*}
$$

我们由此得到：

$$
\begin{align*}

P_{n}^{\perp}|\psi_{n}\rangle=\mathcal{G}^{\perp}(\zeta)(V-E_n+\zeta)|\psi_{n}\rangle

\end{align*}
$$

将其代入 $|\psi_{n}\rangle=|\phi_{n}\rangle+P_{n}^{\perp}|\psi_{n}\rangle$ ，再不断进行迭代，即得：

$$
\begin{align*}

|\psi_{n}\rangle=\sum_{k=0}^{\infty}[\mathcal{G}^{\perp}(\zeta)(V-E_n+\zeta)]^{k}|\phi_{n}\rangle

\end{align*}
$$

这个式子中由于含有 $E_{n}$，所以并不能真正求解，我们实际上做的是利用它求出 $E_{n}$。

对 $V|\psi_{n}\rangle=(E_{n}-H_{0})|\psi_{n}\rangle$ 左乘 $\langle\phi_{n}|$，得到：

$$
\begin{align*}

E_{n}-\varepsilon_{n}=\langle\phi_{n}|V|\psi_{n}\rangle

\end{align*}
$$

于是我们可以将 $|\psi_{n}\rangle$ 代入得到关于 $E_{n}$ 的方程，并迭代求解。

为了使 $V-E_{n}+\zeta$ 为小量，我们可以取 $\zeta=E_{n}$ 和 $\zeta=\varepsilon_{n}$，两者分别对应 Brillouin-Wigner 微扰论和 Rayleigh-Schrodinger 微扰论。

## Brillouin-Wigner 微扰论

我们知道：

$$
\begin{align*}

|\psi_{n}\rangle=\sum_{k=0}^{\infty}[\mathcal{G}^{\perp}(E_{n})V]^{k}|\phi_{n}\rangle

\end{align*}
$$

于是有：

$$
\begin{align*}

E_{n}-\varepsilon_{n}=\langle\phi_{n}|T^{\perp}(E_{n})|\phi_{n}\rangle

\end{align*}
$$

其中：

$$
\begin{align*}

T^{\perp}=V+V\mathcal{G}^{\perp}V+V\mathcal{G}^{\perp}V\mathcal{G}^{\perp}V+\dots

\end{align*}
$$

我们可以用微扰迭代的方法不断逼近精确的 $E_{n}$。首先，如果 $T^{\perp}=0$，我们显然有 $E_{n}^{(0)}=\varepsilon_{n}$，这里上标 $(0)$ 表示第 $0$ 阶微扰。然后我们取 $T^{\perp}=V$，容易得到：

$$
\begin{align*}

E_{n}^{(1)}=\varepsilon_{n}+\langle\phi_{n}|V|\phi_{n}\rangle

\end{align*}
$$

再取 $T^{\perp}=V+V\mathcal{G}^{\perp}V$ ，则有[^3]：

$$
\begin{align*}

E_{n}^{(2)}	&=\varepsilon_{n}+\langle\phi_{n}|V|\phi_{n}\rangle+\langle\phi_{n}|V\mathcal{G}^{\perp}(E_{n}^{(0)})V|\phi_{n}\rangle \\

&=\varepsilon_{n}+\langle\phi_{n}|V|\phi_{n}\rangle+\sum_{m\neq n}\frac{\left|\langle\phi_{n}|V|\phi_{m}\rangle\right|^{2}}{\varepsilon_{n}-\varepsilon_{m}}

\end{align*}
$$

以此类推，如果这个过程收敛，我们就可以得到精确解。当然实际上我们用的一般只有前两阶。我们还可以得到一阶近似的波函数，这也是常用的：

$$
\begin{align*}

|\psi_{n}^{(1)}\rangle=|\phi_{n}\rangle+\sum_{m\neq n}\frac{\langle\phi_{m}|V|\phi_{n}\rangle}{\varepsilon_{n}-\varepsilon_{m}}|m\rangle

\end{align*}
$$

## Reyleigh-Schrodinger 微扰论

此种情况下有：

$$
\begin{align*}

|\psi_{n}\rangle=\sum_{k=0}^{\infty}[\mathcal{G}^{\perp}(\varepsilon_{n})(V-E_{n}+\varepsilon_{n})]^{k}|\phi_{n}\rangle

\end{align*}
$$

可以看出，此种情况下的表达式要更为复杂。试计算其各阶微扰，很容易发现其零阶和一阶微扰同 Brillouin-Wigner 微扰相同，二阶微扰实际上也相同：

$$
\begin{align*}

E_{n}^{(2)}	&=\varepsilon_{n}+\langle\phi_{n}|V|\phi_{n}\rangle+\langle\phi_{n}|V\mathcal{G}^{\perp}(\varepsilon_{n})(V-E_{n}^{(1)}+\varepsilon_{n})|\phi_{n}\rangle\\

&=\varepsilon_{n}+\langle\phi_{n}|V|\phi_{n}\rangle+\langle\phi_{n}|V\mathcal{G}^{\perp}(\varepsilon_{n})V|\phi_{n}\rangle\\

&= \varepsilon_{n}+\langle\phi_{n}|V|\phi_{n}\rangle+\sum_{m\neq n}\frac{\left|\langle\phi_{n}|V|\phi_{m}\rangle\right|^{2}}{\varepsilon_{n}-\varepsilon_{m}}

\end{align*}
$$

第二个等号是因为 $P_{n}^{\perp}|\phi_{n}\rangle=0$。尽管如此，此种微扰方式向高阶推广会更困难。

之所以提及这种微扰论，是因为这实际上等价于我们最初按阶展开能量和波函数的方式。[^4]

[^1]: 只要 $H_{0}$ 原来的本征值和其余本征值之间存在一个有限的能隙。
[^2]: 不同的 $\zeta$ 取值对应不同的微扰论。
[^3]: 注意这里的推导只适用于单体波函数。
[^4]: 目前没研究为什么等价。