[[Imaginary-time Evolution]]
[[Monte Carlo]]

[Fermion Monte Carlo without fixed nodes: A game of life, death, and annihilation in Slater determinant space](zotero://select/items/@boothFermionMonteCarlo2009)

FCIQMC 全称 Full Configuration Interaction Quantum Monte Carlo，是一种利用 Monte Carlo 方法求解系统基态的方法。

FCIQMC 的核心是模拟虚时演化的过程。

每一步时间演化中，有三个步骤：

增殖 (The spawning step)：对每一个母 walker，例如 $\alpha$，其处在态 $i_{\alpha}$ 上，以 $p_{\text{gen}}(j|i_{\alpha})$ 的概率选择 $j$ 态，并且以如下概率产生出一个子 walker：

$$
p_{\text{s}}(j|i_{\alpha})=\frac{\Delta\tau\left|K_{i_{\alpha}j}\right|}{p_{\text{gen}}(j|i_{\alpha})}
$$

子 walker 的符号等于 $-\mathop{\text{sign}}(K_{i_{\alpha}j})\mathop{\text{sign}}(\alpha)$。这里 $p_{\text{gen}}$ 的选择是具有任意性的。如果 $p_{s}>1$，那么会在 $j$ 上首先产生 $\lfloor p_{s}\rfloor$ 个子 walker，然后以 $p_{s}-\lfloor p_{s}\rfloor$ 的概率产生一个子 walker。一般来说，新产生的子 walker 数目远小于母 walker 数目，一般有 $N_{s}\sim10^{-4}N_{w}$。

对角死亡/克隆 (The diagonal death/cloning step)：对每一个母 walker，计算：

$$
p_{\text{d}}(i_{\alpha})=\Delta\tau(K_{i_{\alpha}i_{\alpha}}-S)
$$
如果 $p_{d}>0$，该 walker 以 $p_{d}$ 的概率死亡，如果 $p_{d}<0$，以 $\left|p_{d}\right|$ 的概率克隆该 walker，这里概率的含义同增殖步骤中的含义相同。

在一开始的时候，为了能有更多 walker，我们常令 $S$ 比较大，从而使得更多的 clone 步骤发生。

湮灭 (The annihilation step)：该步骤把相同组态但符号相反的 walker 成对湮灭。

事实上，第一个和第二个步骤是可以同时进行的，它们彼此之间没有任何关系，按顺序列出来只是为了方便。

FCIQMC 相较于一般求解微分方程的办法的好处在于，在演化过程中，大部分组态上是没有 walker 的，因此相较于正常情况下每个组态前都有系数，其计算量要小很多。在系统达到稳态后，即可多次重复取样求平均值，得到系统基态。