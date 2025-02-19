我们要证明的是：

$$
u_{i}v_{j}=\frac{\boldsymbol{u}\cdot\boldsymbol{v}}{3}\delta_{ij}+\frac{u_{i}v_{j}-u_{j}v_{i}}{2}+\left(\frac{u_{i}v_{j}+u_{j}v_{i}}{2}-\frac{\boldsymbol{u}\cdot\boldsymbol{v}}{3}\delta_{ij}\right)
$$

第二项可以写为 $\varepsilon_{ijk}(\boldsymbol{u}\times\boldsymbol{v})_{k}$。

根据李群李代数的知识，我们知道 $\mathfrak{so}(3)$ 的表示的张量分解有：

$$
3\otimes3=1\oplus3\oplus5
$$

因此，表示空间的张量可以分解到这三个表示的不变子空间。为此，我们只需要像通常的线性空间那样，取一组这些不变子空间的矢量 $\boldsymbol{e}_{i}$，然后有：

$$
\boldsymbol{v}=\sum_{i}\frac{\langle\boldsymbol{v},\boldsymbol{e}_{i}\rangle}{|\boldsymbol{e}_{i}|^{2}}\boldsymbol{e}_{i}
$$

这里的矢量其实都是二阶张量：

$$
\begin{align*}
\langle\boldsymbol{A},\boldsymbol{B}\rangle & =\sum_{ij}A_{ij}B_{ij}\\
|\boldsymbol{A}| & =\sqrt{\langle\boldsymbol{A},\boldsymbol{A}\rangle}=\sqrt{\sum_{ij}A_{ij}^{2}}
\end{align*}
$$

$1$ 的不变子空间对应在转动下不变的子空间，我们可以取一个该子空间的张量 $\delta_{ij}$，于是 $u_{i}v_{j}$ 在该子空间的分量为：

$$
\frac{\langle u_{i}v_{j},\delta_{ij}\rangle}{\left|\delta_{ij}\right|^{2}}\delta_{ij}=\frac{\boldsymbol{u}\cdot\boldsymbol{v}}{3}\delta_{ij}
$$

$3$ 对应在转动下如矢量变换的子空间，我们可以取一组该子空间的张量 $\varepsilon_{ijk}w^{(l)}_{k}$ ，其中 $l=1,2,3$。可以验证，这组矢量张成的空间在转动下确实是不变子空间：

$$
\sum_{lm}\sum_{k}U_{il}U_{jm}\varepsilon_{lmk}w_{k}^{(l)}=\sum_{lmno}\sum_{k}U_{il}U_{jm}U_{kn}U_{ko}\varepsilon_{lmn}w_{o}^{(l)}=\sum_{k}\varepsilon_{ijk}\sum_{o}U_{ko}w_{o}^{(l)}
$$

计算：

$$
\langle u_{i}v_{j},\varepsilon_{ijk}w_{k}\rangle=(\boldsymbol{u}\times\boldsymbol{v})\cdot\boldsymbol{w}
$$

取 $w^{(l)}_{k}=\delta_{kl}$，具体写出来应有类似 $w^{(1)}=(1,0,0)$ 的形式。由此可以得到：

$$
\langle u_{i}v_{j},\varepsilon_{ijk}w^{(l)}_{k}\rangle=(\boldsymbol{u}\times\boldsymbol{v})_{l}
$$

此时可以计算出 $\left|\varepsilon_{ijk}w^{(l)}_{k}\right|^{2}=2$。例如如果 $w^{(1)}=(1,0,0)$，则可以将 $\varepsilon_{ijk}w^{(1)}_{k}$ 写成矩阵的形式：

$$
\varepsilon_{ijk}w^{(1)}_{k}=\begin{bmatrix}0 & 0 & 0\\
0 & 0 & 1\\
0 & -1 & 0
\end{bmatrix}_{ij}
$$

由此便很容易得到上述结果。

因此 $u_{i}v_{j}$ 在 $3$ 的不变子空间的分量为：

$$
\frac{\varepsilon_{ijl}(\boldsymbol{u}\times\boldsymbol{v})_{l}}{2}
$$

减掉了这两部分，我们自然就得到在 $5$ 的不变子空间的分量，由此便将 $u_{i}v_{j}$ 分解到了三个子空间里。