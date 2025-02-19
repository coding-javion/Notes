对于不含时的哈密顿量，一个计算基态波函数的方法是虚时演化。令 Schrodinger 方程中的 $t=-\mathrm{i}\tau$，即可得到：

$$
-\frac{\partial}{\partial\tau}\psi=\hat{H}\psi\Rightarrow\psi(\tau)=\mathrm{e}^{-\hat{H}\tau}\psi(0)
$$

假设 $\varphi_{n}$ 是哈密顿量本征值为 $E_{n}$ 的本征态，且有 $\psi=\sum_{n}c_{n}\varphi_{n}$。则可以得到：

$$
\psi(\tau)=\mathrm{e}^{-H\tau}\psi(0)=\mathrm{e}^{-H\tau}\sum_{n}c_{n}(0)\varphi_{n}=\sum_{n}c_{n}(0)\mathrm{e}^{-E_{n}\tau}\varphi_{n}
$$

随着 $\tau\rightarrow\infty$，能量更大的成分衰减更快，最终波函数趋于基态。

数值上，如果基态能量 $E_{0}>0$，基态成分也会衰减，我们可以使用：

$$
\psi(\tau)=\mathrm{e}^{-\tau(\hat{H}-E_{0})}\psi(0)
$$

显然，当 $\tau\rightarrow\infty$ 时，该式趋于基态波函数。然而，我们并不知道 $E_{0}$ 的值，一个方法是引入随虚时变化的 $S(\tau)$ 代替 $E_{0}$：

$$
\psi(\tau)=\mathrm{e}^{-\tau(\hat{H}-S(\tau))}\psi(0)
$$
通过随时改变 $S (\tau)$ 的值[^1]，最终我们可以使得 $S(\tau)$ 的值等于 $E_{0}$。

上述演化可以回到微分方程的形式：

$$
-\frac{\partial}{\partial\tau}\psi=(\hat{H}-S)\psi
$$
或者展开系数的矩阵方程：

$$
-\frac{\mathrm{d}c_{i}}{\mathrm{d}\tau}=\sum_{j}(H_{ij}-S\delta_{ij})c_{j}
$$

实际计算中，为了避免 $\hat{H}$ 对角元过大造成数值上的麻烦[^2]，我们通常减去单粒子填充的能量。例如减去 Hartree-Fock 基态的能量[^3]，使用 $K_{ij}=H_{ij}-\delta_{ij}E_{\text{HF}}$：

$$
-\frac{\mathrm{d}c_{i}}{\mathrm{d}\tau}=\sum_{j}(K_{ij}-S\delta_{ij})c_{j}
$$

[^1]: 具体改变的方式再说。
[^2]: 我其实还不知道会是什么麻烦。
[^3]: Hartree-Fock 基的能量怎么获得是个问题。