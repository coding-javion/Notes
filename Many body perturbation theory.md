---
related:
  - "[[Time-Independent Perturbation Theory]]"
  - "[[Hartree-Fock]]"
  - "[[Wick Theorem]]"
title: Many body perturbation theory
author: Chenjiawei
date: 
---
在一般的微扰论中，我们并没有生成哈密顿量为单体哈密顿量，因此，只要我们使用多体哈密顿量和相应的多体波函数，即可得到多体微扰论[^1]。

在形式微扰理论中，Hamilton 量依被划分为两部分。在作这样的划分时，只要已知其完备正交的本征态，$H_{0}$ 的选取是任意的。

在 Hartree-Fock 近似中，Fock 算符代表了多体 Hamilton 量中全部的单体项，而剩余的多体作用只有在研究高阶近似时才会产生贡献。因此，自然而然地，我们可以利用 Fock 算符作为多体微扰理论中的 $H_{0}$，并将在 Hartree-Fock 近似中忽略的多体相互作用看作是在基础上对系统进行的微扰。

我们假设哈密顿量为：

$$
\begin{aligned}
H & =S+D+T\\
 & =\sum_{pq}s_{pq}a_{p}^{\dagger}a_{q}+\frac{1}{2}\sum_{pqrs}d_{pqrs}a_{p}^{\dagger}a_{q}^{\dagger}a_{s}a_{r}+\frac{1}{6}\sum_{pqrstu}t_{pqrstu}a_{p}^{\dagger}a_{q}^{\dagger}a_{r}^{\dagger}a_{u}a_{t}a_{s}
\end{aligned}
$$

这里，系数为：

$$
\begin{aligned}
s_{pq} & =\langle p|s|q\rangle\\
d_{pqrs} & =\langle pq|d|rs\rangle\\
t_{pqrstu} & =\langle pqr|t|stu\rangle
\end{aligned}
$$

利用 Wick 定理将系统的 Hamilton 量写成正规序算符的形式。单体算符项为：

$$
S=\sum_{pq}s_{pq}:\mathrel{a_{p}^{\dagger}a_{q}}:+\sum_{i}s_{ii}
$$

两体算符项有：

$$
\begin{aligned}D & =\frac{1}{2}\sum_{pqrs}d_{pqrs}:\mathrel{a_{p}^{\dagger}a_{q}^{\dagger}a_{s}a_{r}}:\\
 & -\frac{1}{2}\sum_{iqr}d_{iqri}:\mathrel{a_{q}^{\dagger}a_{r}}:-\frac{1}{2}\sum_{pis}d_{piis}:\mathrel{a_{p}^{\dagger}a_{s}}:\\
 & -\frac{1}{2}\sum_{ij}d_{ijji}+\frac{1}{2}\sum_{ij}d_{ijij}
\end{aligned}
+\frac{1}{2}\sum_{iqs}d_{iqis}:\mathrel{a_{q}^{\dagger}a_{s}}:+\frac{1}{2}\sum_{pir}d_{piri}:\mathrel{a_{p}^{\dagger}a_{r}}:
$$

引入符号：

$$
\bar{d}_{pqrs}=d_{pqrs}-d_{pqsr}
$$

并进行适当的指标替换，我们可以发现二体算符项可以化简为：

$$
\begin{aligned}D & =\frac{1}{2}\sum_{pqrs}d_{pqrs}:\mathrel{a_{p}^{\dagger}a_{q}^{\dagger}a_{s}a_{r}}:+\sum_{ipq}\bar{d}_{ipiq}:\mathrel{a_{p}^{\dagger}a_{q}}:+\frac{1}{2}\sum_{ij}\bar{d}_{ijij}\end{aligned}
$$

三体算符项有些复杂，我们把 Wick 定理得到的缩并项分成四部分，第一部分为完全没有缩并的：

$$
T_{3}=\frac{1}{6}\sum_{pqrstu}t_{pqrstu}:\mathrel{a_{p}^{\dagger}a_{q}^{\dagger}a_{r}^{\dagger}a_{u}a_{t}a_{s}}:
$$

第二部分为有一项缩并的：

$$
\begin{aligned}
T_{2} & =\frac{1}{6}\biggl(\sum_{iqrtu}t_{iqritu}:\mathrel{a_{q}^{\dagger}a_{r}^{\dagger}a_{u}a_{t}}:-\sum_{iqrsu}t_{iqrsiu}:\mathrel{a_{q}^{\dagger}a_{r}^{\dagger}a_{u}a_{s}}:+\sum_{iqrst}t_{iqrsti}:\mathrel{a_{q}^{\dagger}a_{r}^{\dagger}a_{t}a_{s}}:\\
 & -\sum_{pirtu}t_{piritu}:\mathrel{a_{p}^{\dagger}a_{r}^{\dagger}a_{u}a_{t}}:+\sum_{pirsu}t_{pirsiu}:\mathrel{a_{p}^{\dagger}a_{r}^{\dagger}a_{u}a_{s}}:-\sum_{pirst}t_{pirsti}:\mathrel{a_{p}^{\dagger}a_{r}^{\dagger}a_{t}a_{s}}:\\
 & +\sum_{pqitu}t_{pqiitu}:\mathrel{a_{p}^{\dagger}a_{q}^{\dagger}a_{u}a_{t}}:-\sum_{pqisu}t_{pqisiu}:\mathrel{a_{p}^{\dagger}a_{q}^{\dagger}a_{u}a_{s}}:+\sum_{pqist}t_{pqisti}:\mathrel{a_{p}^{\dagger}a_{q}^{\dagger}a_{t}a_{s}}:\biggr)
\end{aligned}
$$

改变一下指标，可得：

$$
\begin{aligned}T_{2} & =\frac{1}{2}\biggl(\sum_{ipqrs}t_{ipqirs}:\mathrel{a_{p}^{\dagger}a_{q}^{\dagger}a_{s}a_{r}}:-\sum_{ipqrs}t_{ipqris}:\mathrel{a_{p}^{\dagger}a_{q}^{\dagger}a_{s}a_{r}}:+\sum_{ipqsr}t_{ipqrsi}:\mathrel{a_{p}^{\dagger}a_{q}^{\dagger}a_{s}a_{r}}:\biggr)\end{aligned}
$$

定义符号：

$$
\bar{t}_{pqrstu}=t_{pqrstu}-t_{pqrsut}+t_{pqrtsu}-t_{pqrtus}+t_{pqrust}-t_{pqruts}
$$

于是可以写为：

$$
T_{2}=\frac{1}{4}\sum_{ipqrs}\bar{t}_{ipqirs}:\mathrel{a_{p}^{\dagger}a_{q}^{\dagger}a_{s}a_{r}}:
$$

第三部分为有两项缩并的，由于两项缩并的比较麻烦，我们先详细的写出来有哪些项：

$$
\begin{aligned}T_{1} & =\frac{1}{6}\biggl(\sum_{pqrstu}t_{pqrstu}:\mathrel{{\color{teal}a_{p}^{\dagger}}{\color{red}a_{q}^{\dagger}}a_{r}^{\dagger}{\color{teal}a_{u}}{\color{red}a_{t}}a_{s}}:+\sum_{pqrstu}t_{pqrstu}:\mathrel{{\color{teal}a_{p}^{\dagger}}{\color{red}a_{q}^{\dagger}}a_{r}^{\dagger}{\color{teal}a_{u}}{a_{t}}{\color{red}a_{s}}}:+\sum_{pqrstu}t_{pqrstu}:\mathrel{{\color{teal}a_{p}^{\dagger}}{\color{red}a_{q}^{\dagger}}a_{r}^{\dagger}{\color{red}a_{u}}{\color{teal}a_{t}}a_{s}}:\\
 & +\sum_{pqrstu}t_{pqrstu}:\mathrel{{\color{teal}a_{p}^{\dagger}}{\color{red}a_{q}^{\dagger}}a_{r}^{\dagger}a_{u}{\color{teal}a_{t}}{\color{red}a_{s}}}:+\sum_{pqrstu}t_{pqrstu}:\mathrel{{\color{teal}a_{p}^{\dagger}}{\color{red}a_{q}^{\dagger}}a_{r}^{\dagger}{\color{red}a_{u}}a_{t}{\color{teal}a_{s}}}:+\sum_{pqrstu}t_{pqrstu}:\mathrel{{\color{teal}a_{p}^{\dagger}}{\color{red}a_{q}^{\dagger}}a_{r}^{\dagger}a_{u}{\color{red}a_{t}}{\color{teal}a_{s}}}:\\
 & +\sum_{pqrstu}t_{pqrstu}:\mathrel{{\color{teal}a_{p}^{\dagger}}a_{q}^{\dagger}{\color{red}a_{r}^{\dagger}}{\color{teal}a_{u}}{\color{red}a_{t}}a_{s}}:+\sum_{pqrstu}t_{pqrstu}:\mathrel{{\color{teal}a_{p}^{\dagger}}a_{q}^{\dagger}{\color{red}a_{r}^{\dagger}}{\color{teal}a_{u}}{a_{t}}{\color{red}a_{s}}}:+\sum_{pqrstu}t_{pqrstu}:\mathrel{{\color{teal}a_{p}^{\dagger}}a_{q}^{\dagger}{\color{red}a_{r}^{\dagger}}{\color{red}a_{u}}{\color{teal}a_{t}}a_{s}}:\\
 & +\sum_{pqrstu}t_{pqrstu}:\mathrel{{\color{teal}a_{p}^{\dagger}}a_{q}^{\dagger}{\color{red}a_{r}^{\dagger}}a_{u}{\color{teal}a_{t}}{\color{red}a_{s}}}:+\sum_{pqrstu}t_{pqrstu}:\mathrel{{\color{teal}a_{p}^{\dagger}}a_{q}^{\dagger}{\color{red}a_{r}^{\dagger}}{\color{red}a_{u}}a_{t}{\color{teal}a_{s}}}:+\sum_{pqrstu}t_{pqrstu}:\mathrel{{\color{teal}a_{p}^{\dagger}}a_{q}^{\dagger}{\color{red}a_{r}^{\dagger}}a_{u}{\color{red}a_{t}}{\color{teal}a_{s}}}:\\
 & +\sum_{pqrstu}t_{pqrstu}:\mathrel{a_{p}^{\dagger}{\color{teal}a_{q}^{\dagger}}{\color{red}a_{r}^{\dagger}}{\color{teal}a_{u}}{\color{red}a_{t}}a_{s}}:+\sum_{pqrstu}t_{pqrstu}:\mathrel{a_{p}^{\dagger}{\color{teal}a_{q}^{\dagger}}{\color{red}a_{r}^{\dagger}}{\color{teal}a_{u}}{a_{t}}{\color{red}a_{s}}}:+\sum_{pqrstu}t_{pqrstu}:\mathrel{a_{p}^{\dagger}{\color{teal}a_{q}^{\dagger}}{\color{red}a_{r}^{\dagger}}{\color{red}a_{u}}{\color{teal}a_{t}}a_{s}}:\\
 & +\sum_{pqrstu}t_{pqrstu}:\mathrel{a_{p}^{\dagger}{\color{teal}a_{q}^{\dagger}}{\color{red}a_{r}^{\dagger}}a_{u}{\color{teal}a_{t}}{\color{red}a_{s}}}:+\sum_{pqrstu}t_{pqrstu}:\mathrel{a_{p}^{\dagger}{\color{teal}a_{q}^{\dagger}}{\color{red}a_{r}^{\dagger}}{\color{red}a_{u}}a_{t}{\color{teal}a_{s}}}:+\sum_{pqrstu}t_{pqrstu}:\mathrel{a_{p}^{\dagger}{\color{teal}a_{q}^{\dagger}}{\color{red}a_{r}^{\dagger}}a_{u}{\color{red}a_{t}}{\color{teal}a_{s}}}:\biggr)
\end{aligned}
$$

缩并后即：

$$
\begin{aligned}T_{1} & =\frac{1}{6}\biggl(-\sum_{ijrs}t_{ijrsji}:\mathrel{a_{r}^{\dagger}a_{s}}:+\sum_{ijrt}t_{ijrjti}:\mathrel{a_{r}^{\dagger}a_{t}}:+\sum_{ijrs}t_{ijrsij}:\mathrel{a_{r}^{\dagger}}a_{s}:\\
 & -\sum_{ijru}t_{ijrjiu}:\mathrel{a_{r}^{\dagger}}a_{u}:-\sum_{ijrt}t_{ijritj}:\mathrel{a_{r}^{\dagger}}a_{t}:+\sum_{ijru}t_{ijriju}:\mathrel{a_{r}^{\dagger}}a_{u}:\\
 & +\sum_{ijqs}t_{iqjijs}:\mathrel{a_{q}^{\dagger}a_{s}}:-\sum_{ijqt}t_{iqjitj}:\mathrel{a_{q}^{\dagger}a_{t}}:-\sum_{ijqs}t_{iqjjis}:\mathrel{a_{q}^{\dagger}}a_{s}:\\
 & +\sum_{ijqu}t_{iqjuij}:\mathrel{a_{q}^{\dagger}a_{u}}:+\sum_{ijqt}t_{iqjjti}:\mathrel{a_{q}^{\dagger}a_{t}}:-\sum_{ijqu}t_{iqjuji}:\mathrel{a_{q}^{\dagger}}a_{u}:\\
 & -\sum_{ijps}t_{pijijs}:\mathrel{a_{p}^{\dagger}a_{s}}:+\sum_{ijpt}t_{pijitj}:\mathrel{a_{p}^{\dagger}a_{t}}:+\sum_{ijps}t_{pijjis}:\mathrel{a_{p}^{\dagger}}a_{s}:\\
 & -\sum_{ijpu}t_{pijuij}:\mathrel{a_{p}^{\dagger}a_{u}}:-\sum_{ijpt}t_{pijjti}:\mathrel{a_{p}^{\dagger}a_{t}}:+\sum_{ijqu}t_{pijuji}:\mathrel{a_{p}^{\dagger}}a_{u}:\biggr)
\end{aligned}
$$

更换一下指标，即可得到：

$$
\begin{aligned}T_{1} & =\frac{1}{6}\sum_{ijpq}\biggl(-t_{ijpqji}+t_{ijpjqi}+t_{ijpqij}-t_{ijpjiq}-t_{ijpiqj}+t_{ijpijq}\\
 & +t_{ipjijq}-t_{ipjiqj}-t_{ipjjiq}+t_{ipjqij}+t_{ipjjqi}-t_{ipjqji}\\
 & -t_{pijijq}+t_{pijiqj}+t_{pijjiq}-t_{pijqij}-t_{pijjqi}+t_{pijqji}\biggr):\mathrel{a_{p}^{\dagger}a_{q}}:
\end{aligned}
$$

利用先前定义的符号，即可得到：

$$
\begin{aligned}T_{1} & =\frac{1}{6}\sum_{ijpq}\biggl(-\bar{t}_{ijpqji}+\bar{t}_{ipjijq}-\bar{t}_{pijijq}\biggr):\mathrel{a_{p}^{\dagger}a_{q}}:\\
 & =\frac{1}{2}\sum_{ijpq}\bar{t}_{ijpijq}:\mathrel{a_{p}^{\dagger}a_{q}}:
\end{aligned}
$$

第四部分即有三项缩并的，根据排列组合的知识，我们很容易的知道共有六个项，并且恰好对应于我们定义的 $\bar{t}$ 中的六项，因此我们可以直接写出：

$$
T_{0}=\frac{1}{6}\sum_{ijk}\bar{t}_{ijkijk}
$$

将这四部分加起来，我们便可以得到：

$$
\begin{aligned}T & =T_{3}+T_{2}+T_{1}+T_{0}\\
 & =\frac{1}{6}\sum_{pqrstu}t_{pqrstu}:\mathrel{a_{p}^{\dagger}a_{q}^{\dagger}a_{r}^{\dagger}a_{u}a_{t}a_{s}}:+\frac{1}{4}\sum_{ipqrs}\bar{t}_{ipqirs}:\mathrel{a_{p}^{\dagger}a_{q}^{\dagger}a_{s}a_{r}}:\\
 & +\frac{1}{2}\sum_{ijpq}\bar{t}_{ijpijq}:\mathrel{a_{p}^{\dagger}a_{q}}:+\frac{1}{6}\sum_{ijk}\bar{t}_{ijkijk}
\end{aligned}
$$

我们终于可以写出正规化形式的哈密顿量，但为了使结果简洁，我们发现：

$$
E_{0}^{(0)}=\langle\Phi_{0}|H|\Phi_{0}\rangle=\sum_{i}s_{ii}+\frac{1}{2}\sum_{ij}\bar{d}_{ijij}+\frac{1}{6}\sum_{ijk}\bar{t}_{ijkijk}
$$

于是最终的哈密顿量可以写为：

$$
\begin{aligned}H & =E_{0}^{(0)}+\sum_{pq}(s_{pq}+\sum_{i}\bar{d}_{ipiq}+\frac{1}{2}\sum_{ij}\bar{t}_{ijpijq}):\mathrel{a_{p}^{\dagger}a_{q}}:\\
+ & \frac{1}{4}\sum_{pqrs}(\bar{d}_{pqrs}+\sum_{i}\bar{t}_{ipqirs}):\mathrel{a_{p}^{\dagger}a_{q}^{\dagger}a_{s}a_{r}}:\\
+ & \frac{1}{36}\sum_{pqrstu}\bar{t}_{pqrstu}:\mathrel{a_{p}^{\dagger}a_{q}^{\dagger}a_{r}^{\dagger}a_{u}a_{t}a_{s}}:
\end{aligned}
$$

这里我们只使用了 $s,\bar{d},\bar{t}$ 表示出了哈密顿量。这样做的好处是在计算时减少存储量。

利用正规化的方式理解 Hartree-Fock，我们不难将原本的 Hartree-Fock 理论推广到有三体力的情况，此时 Fock 算符的分量为：

$$
f_{pq}=s_{pq}+\sum_{i}\bar{d}_{ipiq}+\frac{1}{2}\sum_{ij}\bar{t}_{ijpijq}
$$

于是哈密顿量可以写为：

$$
\begin{aligned}H & =E_{0}^{(0)}+\sum_{pq}f_{pq}:\mathrel{a_{p}^{\dagger}a_{q}}:+\frac{1}{4}\sum_{pqrs}(\bar{d}_{pqrs}+\sum_{i}\bar{t}_{ipqirs}):\mathrel{a_{p}^{\dagger}a_{q}^{\dagger}a_{s}a_{r}}:\\
 & +\frac{1}{36}\sum_{pqrstu}\bar{t}_{pqrstu}:\mathrel{a_{p}^{\dagger}a_{q}^{\dagger}a_{r}^{\dagger}a_{u}a_{t}a_{s}}:
\end{aligned}
$$

如果解 Hartree-Fock 方程从而得到了合适的正交归一基，那么有：

$$
f_{pq}=\varepsilon_{p}\delta_{pq}
$$

于是可以写为：

$$
\begin{aligned}
H & =E_{0}^{(0)}+\sum_{p}\varepsilon_{p}:\mathrel{a_{p}^{\dagger}a_{p}}:+\frac{1}{4}\sum_{pqrs}(\bar{d}_{pqrs}+\sum_{i}\bar{t}_{ipqisr}):\mathrel{a_{p}^{\dagger}a_{q}^{\dagger}a_{r}a_{s}}:\\
 & +\frac{1}{36}\sum_{pqrstu}\bar{t}_{pqrstu}:\mathrel{a_{p}^{\dagger}a_{q}^{\dagger}a_{r}^{\dagger}a_{u}a_{t}a_{s}}:
\end{aligned}
$$

我们把常数部分和单体部分当做 $H_{0}$，二体和三体部分当做微扰 $V$。于是可以利用微扰论计算真实的基态能量。近似到零阶会得到 $E_{0}^{(0)}$，而一阶修正则为 $E_{0}^{(1)}=0$。

计算二阶修正时，我们不能直接使用不含时微扰论中的公式，因为完备性关系并不相同。事实上，为了更高阶的推导方便，我们将采用一种新的推导方式。我们从下式出发：

$$
E_{0}^{(2)}=\langle\Phi_{0}|V\mathcal{G}^{\perp}(E_{0}^{(0)})V|\Phi_{0}\rangle
$$

我们发现，将格林算符 $\mathcal{G}^{\perp}$ 作用到一个态矢上，只是在态矢上乘了一个系数，因此，我们在计算时可以最后再补充这一系数。唯一需要注意的是，由于投影算符的存在，$V$ 作用到基态上不能仍为基态。

因此，我们先计算两个 $V$ 的作用效果，先看纯两体部分，我们有：

$$
\begin{aligned}
\langle\Phi_{0}|VV|\Phi_{0}\rangle_2 & =\frac{1}{16}\sum_{pqrstuvw}(\bar{d}_{pqrs}+\sum_{i}\bar{t}_{ipqirs})(\bar{d}_{tuvw}+\sum_{j}\bar{t}_{jtujvw})\\
 & \times\langle\Phi_{0}|:\mathrel{a_{p}^{\dagger}a_{q}^{\dagger}a_{s}a_{r}}::\mathrel{a_{t}^{\dagger}a_{u}^{\dagger}a_{w}a_{v}}:|\Phi_{0}\rangle
\end{aligned}
$$

利用推广的 Wick 定理，我们可以得到：

$$
\langle\Phi_{0}|VV|\Phi_{0}\rangle_2=\frac{1}{4}\sum_{ijab}(\bar{d}_{ijab}+\sum_{k}\bar{t}_{kijkab})(\bar{d}_{abij}+\sum_{k}\bar{t}_{kabkij})
$$

我们不难发现，这种情况下，$V$ 作用到基态上绝不可能仍未基态，因此，我们可以放心的加上系数。

再考虑纯三体部分，容易得出：

$$
\langle\Phi_{0}|VV|\Phi_{0}\rangle_{3}=\frac{1}{36}\sum_{ijkabc}\bar{t}_{ijkabc}\bar{t}_{abcijk}
$$

加上系数后，我们得到：

$$
E_{0}^{(2)}=\frac{1}{4}\sum_{ijab}\frac{(\bar{d}_{ijab}+\sum_{k}\bar{t}_{kijkab})(\bar{d}_{abij}+\sum_{k}\bar{t}_{kabkij})}{\varepsilon_{i}+\varepsilon_{j}-\varepsilon_{a}-\varepsilon_{b}}+\frac{1}{36}\sum_{ijkabc}\frac{\bar{t}_{ijkabc}\bar{t}_{abcijk}}{\varepsilon_{i}+\varepsilon_{j}+\varepsilon_{k}-\varepsilon_{a}-\varepsilon_{b}-\varepsilon_{c}}
$$

在使用的时候，我们经常没有三体项，此时只需要令 $t$ 的分量均为零即可得到：

$$
E_{0}^{(2)}=\frac{1}{4}\sum_{ijab}\frac{\bar{d}_{ijab}\bar{d}_{abij}}{\varepsilon_{i}+\varepsilon_{j}-\varepsilon_{a}-\varepsilon_{b}}
$$

[^1]: 当然实际上还需要很多其它的工作。