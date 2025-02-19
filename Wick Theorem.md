我们首先定义算符的正规序，我们只考虑算符为产生湮灭算符的情况，正规序即永远把产生算符放到前面，同时在前面产生符号，符号为$\zeta^{P}$，其中，$\zeta$对于玻色子为$1$，对于费米子为$-1$。$P$表示从原本的序到正规序经历的置换次数。$AB$的正规序用$:AB:$表示，例如：

$$
:\mathrel{a_{p}^{\dagger}a_{q}a_{r}^{\dagger}}:=\zeta a_{p}^{\dagger}a_{r}^{\dagger}a_{q}
$$

如果我们用大写字母 $AB\cdots$ 表示产生或湮灭算符，那么两个算符的缩并定义为：

$$
{\color{teal}AB}=AB-:AB:
$$

这里我们用相同的颜色表示缩并，如${\color{teal}AB}$[^1]。可以验证：

$$
\begin{align*}
{\color{teal}a_{p}a_{q}} & =0\\
{\color{teal}a_{p}^{\dagger}a_{q}^{\dagger}} & =0\\
{\color{teal}a_{p}^{\dagger}a_{q}} & =0\\
{\color{teal}a_{p}a_{q}^{\dagger}} & =\delta_{pq}
\end{align*}
$$

这表明缩并永远为常数。接下来我们引入符号：

$$
:\mathrel{A{\color{teal}B}C{\color{teal}D}\cdots}:\equiv\zeta^{P}:\mathrel{A{\color{teal}BD}C\cdots}:\equiv\zeta^{P}{\color{teal}BD}:\mathrel{AC\cdots}:
$$

第一个等号后面的 $\zeta^{P}$ 取决于第一个等号左边到右边经历的置换次数，在第二个等号处我们实际上定义了包含常数项的正规序可以直接把常数提出来。需要注意的是，对于 $:\mathrel {{\color{teal}A}{\color{red}B}{\color{teal}C}{\color{red}D}} :$ 这种情况，它等于 $\zeta:\mathrel {{\color{teal}AC}{\color{red}BD}} :$，因为这里只置换了一次。

Wick定理的形式是：

$$
\begin{align*}
ABCDEF\cdots & =:\mathrel{ABCDEF\cdots}:\\
 & \phantom{=}+\sum:\mathrel{{\color{teal}AB}CDEF\cdots}:(\text{所有的一阶缩并项})\\
 & \phantom{=}+\sum:\mathrel{{\color{teal}AB}{\color{red}CD}EF\cdots}:(\text{所有的二阶缩并项})\\
 & \phantom{=}+\cdots
\end{align*}
$$

Wick 定理的作用就是把算符写成正规序的形式。这一点时而是十分有效的。

## 证明

我们使用数学归纳法：对于$n=1$的情况，这是显然成立的。我们用$W(ABCDEF\cdots)$表示上述定理的右侧。

于是我们假设对于 $n-1$ 的情况也成立，有 $BCDEF\cdots=W(BCDEF\cdots)$。对于 $n$ 的情况，假设 $A$ 是产生算符：

$$
\begin{align*}
ABCDEF\cdots & =AW(BCDEF\cdots)
\end{align*}
$$

显然，上式右侧包含了所有不含$A$与其它算符缩并的项，但是由于$A$为产生算符，因此其与其它算符缩并一定为$0$。因此上式右侧就是$W(ABCDEF\cdots)$。

对于$A$是湮灭算符的情况，显然我们需要把它移到右面，而每一次交换移动都会产生一个$\delta$函数，形成一个少了两个算符的新项，同时在交换了顺序的项前面产生一个$\zeta$的系数。而$A$算符与和它交换的算符之间的缩并也恰好为$\delta$函数，因此，$A$向右移动的过程相当于产生了所有所有可能的缩并。同时，由于每一次移动就是一次置换，因此也自动的满足了前面的符号问题。

综上所述，$A$是任意算符的情况下上述定理都成立。

实际上，Wick 定理在正规序定义为任意序的情况下也成立，只要对易子或反对易子与所有其它算符（反）对易。不过，在改变了正规序的定义后，缩并的值也会改变。例如，如果定义正规序为湮灭算符在前，则有：

$$
\begin{align*}
{\color{teal}a_{p}^{\dagger}a_{q}} & =a_{p}^{\dagger}a_{q}-\zeta a_{q}a_{p}^{\dagger}=[a_{p}^{\dagger},a_{q}]_{\zeta}=-\delta_{pq}\\
{\color{teal}a_{p}a_{q}^{\dagger}} & =a_{p}a_{q}^{\dagger}-a_{p}a_{q}^{\dagger}=0
\end{align*}
$$

此外，把正常的原本的排列替换为另一种序（例如量子场论或者量子多体中常用的编时序），即把 $AB\dots$  替换为 $T(AB\dots)$，这里用 $T$ 算符表示给括号里面的算符排序。 Wick 定理也依然成立，更详细的内容读者可以参考量子场论或者量子多体的书籍。

Wick定理的一个重要的应用是计算一大堆产生湮灭算符作用在真空态上的期待值。而所有正规序作用到真空态都为$0$，所以有：

$$
\langle|ABCDEF\cdots|\rangle=\sum\zeta^{P(ABCDEF\cdots;{\color{teal}AB}{\color{red}CD}{\color{blue}EF}\cdots)}{\color{teal}AB}{\color{red}CD}{\color{blue}EF}\cdots
$$

图中的求和表示对所有缩并完全不再包含正规序的部分求和。

对于基态而不是真空态，例如 $|0\rangle=\prod_{i}a_{i}^{\dagger}|\rangle$。我们使用粒子-空穴的观点，对于同一个算符 $a_{p}$，其在 $p<A$ 的时候是空穴产生算符，而对于 $p>A$ 的时候是粒子的湮灭算符，$a_{p}^{\dagger}$ 则对于 $p>$ 的时候是粒子产生算符，而 $p<A$ 的时候是空穴湮灭算符。由于正规序的定义是任意的，因此我们可以把正规序定义为永远把该意义下的产生算符放到左边，可以验证，对于任意情况下该定义都是有意义的。在此种情况下，缩并的值为：

$$
\begin{align*}
{\color{teal}a_{p}^{\dagger}a_{q}}&=\begin{cases}
0 & p\neq q\\
\delta_{pq} & p=q<A\\
0 & p=q>A
\end{cases}\\
{\color{teal}a_{p}a_{q}^{\dagger}}&=\begin{cases}
0 & p\neq q\\
0 & p=q<A\\
\delta_{pq} & p=q>A
\end{cases}
\end{align*}
$$

在进行计算的时候，这是有用的。

当然，如果我们定义一个新的算符 $b$：

$$
\begin{align*}
b_{i} & =a_{i}^{\dagger}\\
b_{a} & =a_{a}
\end{align*}
$$

正规序定义为始终把 $b^{\dagger}$ 放到左边，则有：

$$
{\color{teal}b_{p}^{\dagger}b_{q}}=0
$$

然而在推导中这是不常用的。

## 推广的 Wick 定理

### 推广一

该版本的推广 Wick 定理指出：

$$
\begin{align*}
:\mathrel{ABCD\cdots}::\mathrel{EFGH\cdots}: & =:\mathrel{ABCD\cdots EFGH}:\\
+ & \sum:\mathrel{{\color{teal}A}{\color{red}B}CD\cdots{\color{teal}E}{\color{red}F}GH}:\text{(所有只在两个正规序之间的算符缩并的缩并项)}
\end{align*}
$$

我们用 $T_{1}$ 表示 $ABCD\cdots$，用 $T_{2}$ 表示 $EFGH\cdots$，我们有：

$$
\begin{align*}
:\mathrel{T_{1}}: & =T_{1}-W^{\prime}(T_{1})\\
:\mathrel{T_{2}}: & =T_{2}-W^{\prime}(T_{2})
\end{align*}
$$

这里我们用 $W^{\prime}$ 表示除了零阶项的所有缩并项。

由此很容易得到：

$$
:\mathrel{T_{1}}::\mathrel{T_{2}}:=T_{1}T_{2}-T_{1}W^{\prime}(T_{2})-W^{\prime}(T_{1})T_{2}+W^{\prime}(T_{1})W^{\prime}(T_{2})
$$

另有：

$$
\begin{align*}
:\mathrel{T_{1}T_{2}}: & =T_{1}T_{2}-:\mathrel{T_{1}}:W^{\prime}(T_{2})-W^{\prime}(T_{1}):\mathrel{T_{2}}:-W^{\prime}(T_{1})W^{\prime}(T_{2})-{\color{teal}T_{1}T_{2}}\\
 & =T_{1}T_{2}-T_{1}W^{\prime}(T_{2})-W^{\prime}(T_{1})T_{2}+W^{\prime}(T_{1})W^{\prime}(T_{2})-{\color{teal}T_{1}T_{2}}
\end{align*}
$$

这里我们有点滥用符号的嫌疑，我们用 ${\color{teal}T_{1}T_{2}}$ 表示所有在 $T_{1}$ 和 $T_{2}$ 之间的缩并。

不难发现：

$$
:\mathrel{T_{1}}::\mathrel{T_{2}}:=:\mathrel{T_{1}T_{2}}:+{\color{teal}T_{1}T_{2}}
$$

即为上述定理。

### 推广二

该版本的 Wick 定理推广 $AB\dots$ 为产生湮灭算符的线性组合，如可以令 $A=c_{p}a_{p}^{\dagger}+c_{q}a_{q}$。如果产生湮灭算符 $a^{\dagger},a$ 的正规序已经定义，那么它们的线性组合 $AB$ 的正规序定义为：

$$
\begin{align*}
:\mathrel{AB}: & =:\mathrel{(c_{p}a_{p}^{\dagger}+c_{q}a_{q})(c_{r}a_{r}^{\dagger}+c_{s}a_{s})}:\\
 & =c_{p}c_{r}:\mathrel{a_{p}^{\dagger}a_{r}^{\dagger}}:+c_{p}c_{s}:\mathrel{a_{p}^{\dagger}a_{s}}:+c_{q}c_{r}:\mathrel{a_{q}a_{r}^{\dagger}}:+c_{q}c_{s}:\mathrel{a_{q}a_{s}}:
\end{align*}
$$

此时正常定义缩并即可。这实际上是在说正规序具有线性性，即 $:\mathrel{\sum_{i}c_{i}T_{i}}:=\sum_{i}c_{i}:\mathrel{T_{i}}:$，由此，推广的 Wick 定理的证明非常简单，只需要把乘积 $AB\dots$ 展开成 $\sum_{i}c_{i}T_{i}$，其中每个 $T_{i}$ 都是简单的产生湮灭算符的乘积，然后单独应用 Wick 定理得到 $\sum_{i}c_{i}W (T_{i})$，由于 $W (T_{i})$  均为正规序，而正规序仍具有线性性，当然有 $\sum_{i}c_{i}W (T_{i})=W (\sum_{i}c_{i}T_{i})$，因此我们就得到了 $W (AB\dots)$。

### 推广三



[^1]: 必须指出，这与通常的符号不同，之所以可以用这种记号，还得感谢计算机。