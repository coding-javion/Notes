## 经典模型

假设有三个物体，密度分布分别为 $\rho_{A}(\boldsymbol{r}_{A})$，$\rho_{B}(\boldsymbol{r}_{B})$，$\rho_{C}(\boldsymbol{r}_{C})$。两个物体相互作用为：

$$
f_{AB}=\int f(\boldsymbol r_A,\boldsymbol r_B)\rho_{A}(\boldsymbol{r}_{A})\rho_{B}(\boldsymbol{r}_{B})\,\mathrm{d}\boldsymbol{r}_{A}\mathrm{d}\boldsymbol{r}_{B}
$$
此时，三个物体相互作用为：

$$
V=f_{AB}+f_{AC}+f_{BC}
$$

这只是两体力的简单相加。

然而，物体并不是刚性的，实际上，在受力后物体的密度分布会发生改变。例如，$A$ 和 $B$ 相互作用后，密度分布会变成 $\rho_{A; B}(\boldsymbol r_A)$ 和 $\rho_{B;A}(\boldsymbol{r}_{B})$，这样，它们两者之间的相互作用为：

$$
f_{AB}=\int f(\boldsymbol{r}_{A},\boldsymbol{r}_{B})\rho_{A;B}(\boldsymbol{r}_{A})\rho_{B;A}(\boldsymbol{r}_{B})\,\mathrm{d}\boldsymbol{r}_{A}\mathrm{d}\boldsymbol{r}_{B}
$$

类比可知 $f_{BC}$，$f_{AC}$ 的形式。

但此时如果再加入物体 $C$，密度又将发生改变，此时的密度分布变为 $\rho_{A;BC}(\boldsymbol{r}_{A})$，$\rho_{B;AC}(\boldsymbol{r}_{B})$ 和 $\rho_{C;AB}(\boldsymbol{r}_{C})$。这种写法中 $\rho_{A;BC}(\boldsymbol{r}_{A})$ 和 $\rho_{A;CB}(\boldsymbol{r}_{A})$ 没有任何区别。但是，显然有：

$$
\rho_{C;AB}(\boldsymbol{r}_{C})\neq\rho_{C;A}(\boldsymbol{r}_{C})\neq\rho_{C;B}(\boldsymbol{r}_{C})
$$

此时，$A$ 与 $B$ 之间的相互作用为：

$$
f^\prime_{AB}=\int f(\boldsymbol{r}_{A},\boldsymbol{r}_{B})\rho_{A;BC}(\boldsymbol{r}_{A})\rho_{B;AC}(\boldsymbol{r}_{B})\,\mathrm{d}\boldsymbol{r}_{A}\mathrm{d}\boldsymbol{r}_{B}
$$

$f_{BC}^{\prime}$ 和 $f_{AC}^{\prime}$ 具有完全类似的形式。由上述形式可以得知，$f_{AB}^{\prime}\neq f_{AB}$，因此最终这三个物体之间的相互作用为：

$$
V=f_{AB}^{\prime}+f_{BC}^{\prime}+f_{AC}^{\prime}\neq f_{AB}+f_{BC}+f_{AC}
$$

我们把多出来的部分，即：

$$
f_{ABC}=f_{AB}^{\prime}+f_{BC}^{\prime}+f_{AC}^{\prime}-f_{AB}-f_{BC}-f_{AC}
$$

称为三体力。此时的相互作用为：

$$
V=f_{AB}+f_{BC}+f_{AC}+f_{ABC}
$$

假如我们假定密度的变化量不大，即有：

$$
\begin{align*}
\rho_{A;BC}(\boldsymbol{r}_{A}) & =\rho_{A;B}(\boldsymbol{r}_{A})+\delta_{A;B;C}(\boldsymbol{r}_{A})\\
 & =\rho_{A;C}(\boldsymbol{r}_{A})+\delta_{A;C;B}(\boldsymbol{r}_{A})
\end{align*}
$$

这里 $\delta_{A;B;C}(\boldsymbol{r}_{A})\neq\delta_{A;C;B}(\boldsymbol{r}_{A})$。利用这种表示方式，我们有：

$$
\begin{align*}
f_{AB}^{\prime}-f_{AB} & =\int f(\boldsymbol{r}_{A},\boldsymbol{r}_{B})\rho_{A;B}(\boldsymbol{r}_{A})\delta_{B;A;C}(\boldsymbol{r}_{B})\,\mathrm{d}\boldsymbol{r}_{A}\mathrm{d}\boldsymbol{r}_{B}\\
 & +\int f(\boldsymbol{r}_{A},\boldsymbol{r}_{B})\delta_{A;B;C}(\boldsymbol{r}_{A})\rho_{B;A}(\boldsymbol{r}_{B})\,\mathrm{d}\boldsymbol{r}_{A}\mathrm{d}\boldsymbol{r}_{B}\\
 & +\int f(\boldsymbol{r}_{A},\boldsymbol{r}_{B})\delta_{A;B;C}(\boldsymbol{r}_{A})\delta_{B;A;C}(\boldsymbol{r}_{B})\,\mathrm{d}\boldsymbol{r}_{A}\mathrm{d}\boldsymbol{r}_{B}
\end{align*}
$$

这样我们就直接得到了 $f_{ABC}$ 的形式。不过是上述形式的轮换相加，可以看出这一项涉及到三个物体，因此写作 $f_{ABC}$。

## 量子化

