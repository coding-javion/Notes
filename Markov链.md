Markov 链是一连串的过程，过程中的每一步都只与前一步有关。因此，Markov 链可以被转移矩阵确定，转移矩阵 $M_{\boldsymbol{x}\boldsymbol{y}}$ 指的是从位形 $\boldsymbol{x}$ 转移到位形 $\boldsymbol{y}$ 的概率。有了转移矩阵后，我们只需要知道某时刻的各个位形的概率分布，两者相乘即可得到下一时刻的概率分布。

部分 Markov 链最终会收敛到一个稳定的概率分布，于是之后过程中的每一步都可以视作一次取样。这就是可以用 Markov 链取样的原因。

Markov 链收敛的一个充分条件是细致平衡条件：

$$
p(\boldsymbol{x})W_{\boldsymbol{x}\boldsymbol{y}}=p(\boldsymbol{y})W_{\boldsymbol{y}\boldsymbol{x}}
$$

一个广泛使用的产生想要分布的 Markov 链的算法是 Metropolis 算法，该算法把转移矩阵分成两部分：

$$
W_{\boldsymbol{x}\boldsymbol{y}}=W_{\boldsymbol{x}\boldsymbol{y}}^{prop}W_{\boldsymbol{x}\boldsymbol{y}}^{acc}
$$

其中，$W_{\boldsymbol{x}\boldsymbol{y}}^{prop}$ 可以任意取，而 $W_{\boldsymbol{x}\boldsymbol{y}}^{acc}$ 则取为 $\min[1,R_{\boldsymbol{x}\boldsymbol{y}}]$。其中 $R_{\boldsymbol{x}\boldsymbol{y}}$ 为：

$$
R_{\boldsymbol{x}\boldsymbol{y}}=\frac{p(\boldsymbol{y})W_{\boldsymbol{y}\boldsymbol{x}}^{prop}}{p(\boldsymbol{x})W_{\boldsymbol{x}\boldsymbol{y}}^{prop}}
$$

可以验证，该取法能使 $W_{\boldsymbol{x}\boldsymbol{y}}$ 满足细致平衡条件。显然有：

$$
R_{\boldsymbol{y}\boldsymbol{x}}=\frac{1}{R_{\boldsymbol{x}\boldsymbol{y}}}
$$

则两者必定有一个大于 1，不妨设 $R_{\boldsymbol{x}\boldsymbol{y}}>1$。因此有：

$$
W_{\boldsymbol{x}\boldsymbol{y}}^{acc}=1\Rightarrow W_{\boldsymbol{x}\boldsymbol{y}}=W_{\boldsymbol{x}\boldsymbol{y}}^{prop}
$$

而 $W_{\boldsymbol{y}\boldsymbol{x}}$ 则等于：

$$
W_{\boldsymbol{y}\boldsymbol{x}}=\frac{p(\boldsymbol{x})W_{\boldsymbol{x}\boldsymbol{y}}^{prop}}{p(\boldsymbol{y})}
$$

于是显然有：

$$
\begin{aligned}
p(\boldsymbol{x})W_{\boldsymbol{x}\boldsymbol{y}} & =p(\boldsymbol{x})W_{\boldsymbol{x}\boldsymbol{y}}^{prop}\\
p(\boldsymbol{y})W_{\boldsymbol{y}\boldsymbol{x}} & =p(\boldsymbol{x})W_{\boldsymbol{x}\boldsymbol{y}}^{prop}
\end{aligned}
$$

满足细致平衡条件。

已知：

$$
p_{i}(t+\Delta t)=M_{ij}p_{j}(t)
$$
$$
\frac{\Delta p_{i}}{\Delta t}=\sum_{j}p_{j}R_{ji}-p_{i}R_{ij}
$$
可以推得：
$$
M_{ij}=(1+\Delta t\sum_{k}R_{ik})\delta_{ij}+\Delta tR_{ji}
$$
