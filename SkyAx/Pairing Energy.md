通常的 skyrme 势并不能描述好 pp 和 hh 相互作用。但是拓展的 skyrme 势可以描述好。[Spin-isospin and pairing properties of modified Skyrme interactions](zotero://select/items/@vangiaiSpinisospinPairingProperties1981) [An effective Skyrme-type interaction for nuclear structure calculations: (I). Ground-state properties](zotero://select/items/@waroquierEffectiveSkyrmetypeInteraction1983) [Hartree-Fock-Bogolyubov description of nuclei near the neutron-drip line](zotero://select/items/@dobaczewskiHartreeFockBogolyubovDescriptionNuclei1984) 。

但通常使用的是更简单的唯象的方式，即对 pp hh 道单独使用一种核力。

[Pairing with a delta interaction in the energy density nuclear mass formula](zotero://select/items/@tondeurPairingDeltaInteraction1979) 是最初使用这种形式的工作。此时对力是不依赖于密度的（Volume Delta Interaction）。

在核物质的计算中对能非常小（$\leq 100\,\text{keV}$），因此对能在表面比在内部更重要。于是对能可以写成密度依赖项（Density-Dependent Delta Interaction）的形式来调节其在内部和表面大小， [Density-dependent delta interactions and actinide pairing matrix elements](zotero://select/items/@chasmanDensitydependentDeltaInteractions1976)。除此之外还有 Mixing 形式的对力，把 VDI 和 DDDI 混合起来（其实就是加了个 $1/2$）。

我们假设对力为：

$$
v_{\text{pair}}=v_{t_{1}}(1-\frac{\rho}{\rho_{0}})\delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})\delta_{t_{1}t_{2}}
$$

## 方法一

考虑矩阵元 $\langle i\bar{i}|\bar{v}_{\text{pair}}|j\bar{j}\rangle$，则有：

$$
\begin{align*}
\langle i\bar{i}|\bar{v}_{\text{pair}}|j\bar{j}\rangle & =\sum_{\dots}\int\mathrm{d}\boldsymbol{r}\dots\psi_{i}^{*}(\boldsymbol{r}_{1},s_{1},t_{1})\psi_{\bar{i}}^{*}(\boldsymbol{r}_{2},s_{2},t_{2})\langle\boldsymbol{r}_{1}s_{1}t_{1};\boldsymbol{r}_{2}s_{2}t_{2}|\bar{v}_{\text{pair}}|\boldsymbol{r}_{1}^{\prime}s_{1}^{\prime}t_{1}^{\prime}\boldsymbol{r}_{2}^{\prime}s_{2}^{\prime}t_{2}^{\prime}\rangle\psi_{j}(\boldsymbol{r}_{2}^{\prime},s_{2}^{\prime},t_{2}^{\prime})\psi_{\bar{j}}(\boldsymbol{r}_{1}^{\prime},s_{1}^{\prime},t_{1}^{\prime})\\
 & =-\sum_{s_{1}s_{2}t}\int\mathrm{d}\boldsymbol{r}\psi_{i}^{*}(\boldsymbol{r},s_{1},t)\psi_{\bar{i}}^{*}(\boldsymbol{r},s_{2},t)\langle\boldsymbol{r}s_{1}t;\boldsymbol{r}s_{2}t|v_{\text{pair}}|\boldsymbol{r}s_{1}t\boldsymbol{r}s_{2}t\rangle(\psi_{j}(\boldsymbol{r},s_{1},t)\psi_{\bar{j}}(\boldsymbol{r},s_{2},t)-\psi_{j}(\boldsymbol{r},s_{2},t)\psi_{\bar{j}}(\boldsymbol{r},s_{1},t))\\
 & =-\sum_{st}\int\mathrm{d}\boldsymbol{r}\psi_{i}^{*}(\boldsymbol{r},s,t)\psi_{\bar{i}}^{*}(\boldsymbol{r},-s,t)\langle\boldsymbol{r}st;\boldsymbol{r},-st|v_{\text{pair}}|\boldsymbol{r}st\boldsymbol{r},-st\rangle(\psi_{j}(\boldsymbol{r},s,t)\psi_{\bar{j}}(\boldsymbol{r},-s,t)-\psi_{j}(\boldsymbol{r},-s,t)\psi_{\bar{j}}(\boldsymbol{r},s,t))\\
 & =-\sum_{st}\int\mathrm{d}\boldsymbol{r}\psi_{i}^{*}(\boldsymbol{r},s,t)2s\psi_{i}(\boldsymbol{r},s,t)\langle\boldsymbol{r}st;\boldsymbol{r},-st|v_{\text{pair}}|\boldsymbol{r}st\boldsymbol{r},-st\rangle(\psi_{j}(\boldsymbol{r},s,t)2s\psi_{j}^{*}(\boldsymbol{r},s,t)-\psi_{j}(\boldsymbol{r},-s,t)(-2s)\psi_{j}^{*}(\boldsymbol{r},-s,t))\\
 & =-\sum_{st}\int\mathrm{d}\boldsymbol{r}\psi_{i}^{*}(\boldsymbol{r},s,t)\psi_{i}(\boldsymbol{r},s,t)\langle\boldsymbol{r}st;\boldsymbol{r},-st|v_{\text{pair}}|\boldsymbol{r}st\boldsymbol{r},-st\rangle(\psi_{j}(\boldsymbol{r},s,t)\psi_{j}^{*}(\boldsymbol{r},s,t)+\psi_{j}(\boldsymbol{r},-s,t)\psi_{j}^{*}(\boldsymbol{r},-s,t))\\
 & =-\sum_{st}\int\mathrm{d}\boldsymbol{r}\psi_{i}^{*}(\boldsymbol{r},s,t)\psi_{i}(\boldsymbol{r},s,t)\langle\boldsymbol{r}st;\boldsymbol{r},-st|v_{\text{pair}}|\boldsymbol{r}st\boldsymbol{r},-st\rangle(\sum_{s^{\prime}}\psi_{j}(\boldsymbol{r},s^{\prime},t)\psi_{j}^{*}(\boldsymbol{r},s^{\prime},t))\\
 & =-\sum_{t}v_{t}\int\mathrm{d}\boldsymbol{r}\left(1-\frac{\rho(\boldsymbol{r})}{\rho_{0}}\right)(\sum_{s}\psi_{i}^{*}(\boldsymbol{r},s,t)\psi_{i}(\boldsymbol{r},s,t))(\sum_{s^{\prime}}\psi_{j}^{*}(\boldsymbol{r},s^{\prime},t)\psi_{j}(\boldsymbol{r},s^{\prime},t))
\end{align*}
$$

因此对能为：

$$
\begin{align*}
 & \frac{1}{4}\sum_{ijkl}\langle ij|\bar{v}_{\text{pair}}|kl\rangle\langle a_{i}^{\dagger}a_{j}^{\dagger}\rangle\langle a_{l}a_{k}\rangle\\
= & \frac{1}{4}\sum_{ij}\langle i\bar{i}|\bar{v}_{\text{pair}}|j\bar{j}\rangle\langle a_{i}^{\dagger}a_{\bar{i}}^{\dagger}\rangle\langle a_{\bar{j}}a_{j}\rangle\\
= & -\frac{1}{4}\sum_{ij}\sum_{t}v_{t}\int\mathrm{d}\boldsymbol{r}\left(1-\frac{\rho(\boldsymbol{r})}{\rho_{0}}\right)(\sum_{s}\left|\psi_{i}(\boldsymbol{r},s,t)\right|^{2})(\sum_{s^{\prime}}\left|\psi_{j}(\boldsymbol{r},s^{\prime},t)\right|^{2})\lambda_{i\bar{i}}\kappa_{j\bar{j}}\\
= & \frac{1}{4}\sum_{t}v_{t}\int\mathrm{d}\boldsymbol{r}\left(1-\frac{\rho(\boldsymbol{r})}{\rho_{0}}\right)\bar{\xi}_{t}(\boldsymbol{r})\xi_{t}(\boldsymbol{r})
\end{align*}
$$

由于对相互作用只在费米面附近作用比较大，因此可以在对能中加权重，以控制其在原理费米面时候的效果：

$$
E_{\text{pair}}=\sum_{ij}\omega_{i}\omega_{j}\bar{v}_{i\bar{i}j\bar{j}}\kappa_{i\bar{i}}\kappa_{j\bar{j}}
$$
[Self-consistent study of triaxial deformations: Application to the isotopes of Kr, Sr, Zr and Mo](zotero://select/items/@boncheSelfconsistentStudyTriaxial1985) 
[An improved pairing interaction for mean field calculations using skyrme potentials*](zotero://select/items/@kriegerImprovedPairingInteraction1990)

## 方法二

为了计算出 Hartree Fock 能量，我们需要计算坐标空间单体反常密度矩阵。首先计算 $\langle a (\boldsymbol{r}, s, t) a (\boldsymbol{r}^{\prime}, s^{\prime}, t^{\prime})\rangle$：

$$
\begin{align*}
\langle a(\boldsymbol{r},s,t)a(\boldsymbol{r}^{\prime},s^{\prime},t^{\prime})\rangle & =\sum_{ij}\psi_{i}(\boldsymbol{r},s,t)\psi_{j}(\boldsymbol{r}^{\prime},s^{\prime},t^{\prime})\langle a_{i}a_{j}\rangle\\
 & =\sum_{i}\psi_{i}(\boldsymbol{r},s,t)\psi_{\bar{i}}(\boldsymbol{r}^{\prime},s^{\prime},t^{\prime})\kappa_{\bar{i}i}\\
 & =\sum_{i}-2s^{\prime}\psi_{i}(\boldsymbol{r},s,t)\psi_{i}^{*}(\boldsymbol{r}^{\prime},-s^{\prime},t^{\prime})\kappa_{\bar{i}i}
\end{align*}
$$

下面计算一种特殊情况：

$$
\begin{align*}
 \langle a(\boldsymbol{r},s,t)a(\boldsymbol{r},-s,t)\rangle&=\sum_{i}\psi_{i}(\boldsymbol{r},s,t)\psi_{\bar{i}}(\boldsymbol{r},-s,t)\kappa_{\bar{i}i}\\
 & =\sum_{i>0}\psi_{i}(\boldsymbol{r},s,t)\psi_{\bar{i}}(\boldsymbol{r},-s,t)\kappa_{\bar{i}i}+\psi_{\bar{i}}(\boldsymbol{r},s,t)\psi_{i}(\boldsymbol{r},-s,t)\kappa_{i\bar{i}}\\
 & =\sum_{i>0}2s\psi_{i}(\boldsymbol{r},s,t)\psi_{i}^{*}(\boldsymbol{r},s,t)\kappa_{\bar{i}i}+2s\psi_{i}^{*}(\boldsymbol{r},-s,t)\psi_{i}(\boldsymbol{r},-s,t)\kappa_{\bar{i}i}\\
 & =2s\sum_{i>0}\sum_{s}\psi_{i}(\boldsymbol{r},s,t)\psi_{i}^{*}(\boldsymbol{r},s,t)\kappa_{\bar{i}i}\\
&=2s\sum_{i>0}\sum_{s}|\psi_{i}(\boldsymbol{r},s,t)|^{2}\kappa_{\bar{i}i}\\
&=s\xi_{t}(\boldsymbol{r})
\end{align*}
$$

这里：

$$
\xi_{t}(\boldsymbol{r})=2\sum_{i>0}\sum_{s}|\psi_{i}(\boldsymbol{r},s,t)|^{2}\kappa_{\bar{i}i}
$$

另外计算：

$$
\begin{align*}
\langle a(\boldsymbol{r},s,t)a(\boldsymbol{r},s,t)\rangle_{\theta} & =\sum_{i}\psi_{i}(\boldsymbol{r},s,t)\psi_{\bar{i}}(\boldsymbol{r},s,t)\kappa_{\bar{i}i}=0
\end{align*}
$$

由此可得：

$$
\begin{align*}
\langle a(\boldsymbol{r},s,t)a(\boldsymbol{r},s^{\prime},t)\rangle_{\theta} & =\delta_{s,-s^{\prime}}\langle a(\boldsymbol{r},s,t)a(\boldsymbol{r},-s,t)\rangle_{\theta}=s\delta_{s,-s^{\prime}}\bar{\xi}_{t}(\boldsymbol{r})
\end{align*}
$$

类似的，计算 $\langle a^{\dagger}(\boldsymbol{r}, s, t) a^{\dagger}(\boldsymbol{r}^{\prime}, s^{\prime}, t^{\prime})\rangle$：

$$
\begin{align*}
\langle a^{\dagger}(\boldsymbol{r},s,t)a^{\dagger}(\boldsymbol{r}^{\prime},s^{\prime},t^{\prime})\rangle & =\sum_{i}\psi_{i}^{*}(\boldsymbol{r},s,t)\psi_{\bar{i}}^{*}(\boldsymbol{r}^{\prime},s^{\prime},t^{\prime})\langle a_{i}^{\dagger}a_{\bar{i}}^{\dagger}\rangle\\
 & =\sum_{i}\psi_{i}^{*}(\boldsymbol{r},s,t)\psi_{\bar{i}}^{*}(\boldsymbol{r}^{\prime},s^{\prime},t^{\prime})\lambda_{i\bar{i}}\\
 & =\sum_{i}-2s^{\prime}\psi_{i}^{*}(\boldsymbol{r},s,t)\psi_{i}(\boldsymbol{r}^{\prime},-s^{\prime},t^{\prime})\lambda_{i\bar{i}}
\end{align*}
$$

计算特殊情况：

$$
\begin{align*}
\langle a^{\dagger}(\boldsymbol{r},-s,t)a^{\dagger}(\boldsymbol{r},s,t)\rangle & =\sum_{i}\psi_{i}^{*}(\boldsymbol{r},-s,t)\psi_{\bar{i}}^{*}(\boldsymbol{r},s,t)\lambda_{i\bar{i}}\\
 & =\sum_{i>0}\psi_{i}^{*}(\boldsymbol{r},-s,t)\psi_{\bar{i}}^{*}(\boldsymbol{r},s,t)\lambda_{i\bar{i}}+\psi_{\bar{i}}^{*}(\boldsymbol{r},-s,t)\psi_{i}^{*}(\boldsymbol{r},s,t)\lambda_{\bar{i}i}\\
 & =\sum_{i>0}2s\psi_{i}^{*}(\boldsymbol{r},-s,t)\psi_{i}(\boldsymbol{r},-s,t)\lambda_{\bar{i}i}+2s\psi_{i}(\boldsymbol{r},s,t)\psi_{i}^{*}(\boldsymbol{r},s,t)\lambda_{\bar{i}i}\\
 & =2s\sum_{i>0}\sum_{s}\psi_{i}(\boldsymbol{r},s,t)\psi_{i}^{*}(\boldsymbol{r},s,t)\lambda_{\bar{i}i}\\
 & =2s\sum_{i>0}\sum_{s}|\psi_{i}(\boldsymbol{r},s,t)|^{2}\lambda_{\bar{i}i}\\

 & =s\bar{\xi}_{t}(\boldsymbol{r})
\end{align*}
$$

这里：

$$
\bar{\xi}_{t}(\boldsymbol{r})=2\sum_{i>0}\sum_{s}\left|\psi_{i}(\boldsymbol{r},s,t)\right|^{2}\lambda_{\bar{i}i}
$$

此外：

$$
\langle a^{\dagger}(\boldsymbol{r},-s,t)a^{\dagger}(\boldsymbol{r},-s,t)\rangle=\sum_{i}\psi_{i}^{*}(\boldsymbol{r},-s,t)\psi_{\bar{i}}^{*}(\boldsymbol{r},-s,t)\lambda_{i\bar{i}}=0
$$

由此可得：

$$
\langle a^{\dagger}(\boldsymbol{r},-s,t)a^{\dagger}(\boldsymbol{r},s^{\prime},t)\rangle=s\delta_{s,s^{\prime}}\bar{\xi}_{t}(\boldsymbol{r})
$$

那么对能为：

$$
\begin{align*}
 & \frac{1}{4}\sum_{\dots}\int\mathrm{d}\boldsymbol{r}\dots\langle\boldsymbol{r}_{1}s_{1}t_{1};\boldsymbol{r}_{2}s_{2}t_{2}|\bar{v}_{\text{pair}}|\boldsymbol{r}_{1}^{\prime}s_{1}^{\prime}t_{1}^{\prime};\boldsymbol{r}_{2}^{\prime}s_{2}^{\prime}t_{2}^{\prime}\rangle\langle a^{\dagger}(\boldsymbol{r}_{1},s_{1},t_{1})a^{\dagger}(\boldsymbol{r}_{2},s_{2},t_{2})\rangle\langle a(\boldsymbol{r}_{2}^{\prime},s_{2}^{\prime},t_{2}^{\prime})a(\boldsymbol{r}_{1}^{\prime},s_{1}^{\prime},t_{1}^{\prime})\rangle\\
= & \frac{1}{4}\sum_{st}\int\mathrm{d}\boldsymbol{r}\langle\boldsymbol{r},-s,t;\boldsymbol{r},s,t|v_{t}\left(1-\frac{\rho}{\rho_{0}}\right)|\boldsymbol{r},-s,t;\boldsymbol{r},s,t\rangle\langle a^{\dagger}(\boldsymbol{r},-s,t)a^{\dagger}(\boldsymbol{r},s,t)\rangle(\langle a(\boldsymbol{r},s,t)a(\boldsymbol{r},-s,t)\rangle-\langle a(\boldsymbol{r},-s,t)a(\boldsymbol{r},s,t)\rangle)\\
= & \frac{1}{4}\sum_{st}\int\mathrm{d}\boldsymbol{r}\langle\boldsymbol{r},-s,t;\boldsymbol{r},s,t|v_{t}\left(1-\frac{\rho}{\rho_{0}}\right)|\boldsymbol{r},-s,t;\boldsymbol{r},s,t\rangle s\bar{\xi}_{t}(\boldsymbol{r})[s\xi_{t}(\boldsymbol{r})-(-s)\xi_{t}(\boldsymbol{r})]\\
= & \frac{1}{8}\sum_{st}\int\mathrm{d}\boldsymbol{r}\langle\boldsymbol{r},-s,t;\boldsymbol{r},s,t|v_{t}\left(1-\frac{\rho}{\rho_{0}}\right)|\boldsymbol{r},-s,t;\boldsymbol{r},s,t\rangle\bar{\xi}_{t}(\boldsymbol{r})\xi_{t}(\boldsymbol{r})\\
= & \frac{1}{8}\sum_{st}v_{t}\int\mathrm{d}\boldsymbol{r}\left(1-\frac{\rho(\boldsymbol{r})}{\rho_{0}}\right)\bar{\xi}_{t}(\boldsymbol{r})\xi_{t}(\boldsymbol{r})\\
= & \frac{1}{4}\sum_{t}v_{t}\int\mathrm{d}\boldsymbol{r}\left(1-\frac{\rho(\boldsymbol{r})}{\rho_{0}}\right)\bar{\xi}_{t}(\boldsymbol{r})\xi_{t}(\boldsymbol{r})
\end{align*}
$$
