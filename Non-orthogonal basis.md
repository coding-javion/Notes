如果在量子力学求解过程中使用了非正交归一基，那么对应的将不再是一个普通的本征值问题，而是一个广义本征值问题。证明如下：

我们知道量子力学变分法等价于薛定谔方程，因此使用变分法证明。变分泛函为：

$$
E[\psi]=\langle\psi|H|\psi\rangle-E(\langle\psi|\psi\rangle-1)
$$

将试探波函数使用非正交基展开：

$$
|\psi\rangle=\sum_{i}\beta_{i}|\psi_{i}\rangle
$$

则变分泛函变为：

$$
E[\psi]=\sum_{ij}\beta_{i}^{*}\beta_{j}\langle\psi_{i}|H|\psi_{j}\rangle-E(\sum_{ij}\beta_{i}^{*}\beta_{j}\langle\psi_{i}|\psi_{j}\rangle-1)
$$

于是变分方程为：

$$
\sum_{j}\beta_{j}\langle\psi_{i}|H|\psi_{j}\rangle-E\sum_{j}\beta_{j}\langle\psi_{i}|\psi_{j}\rangle=0
$$

定义哈密顿算符对应的矩阵为：

$$
H_{ij}=\langle\psi_{i}|H|\psi_{j}\rangle
$$

定义矩阵：

$$
N_{ij}=\langle\psi_{i}|\psi_{j}\rangle
$$

于是上述变分方程写为：

$$
\boldsymbol{H}\boldsymbol{\beta}=E\boldsymbol{N}\boldsymbol{\beta}
$$

正是广义本征值问题的形式。同时我们可以发现，如果是正交归一基，$N_{ij}=\delta_{ij}$ ，我们就回到了通常的本征值问题的形式。
