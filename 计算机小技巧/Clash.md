## 为什么要用 Clash？

出于众所周知的需求，我们时常需要科学上网（也称为挂梯子）。Clash 就是帮助你快乐地科学上网的工具。

那么为什么推荐 Clash？最大的优点当然是，当你使用 Clash 时，你根本感受不到它的存在，无需像其它工具一样时常打开关闭，至于为什么它可以做到这样，想深究的可以跳到 [[#进一步讨论]]。此外，Clash 功能更为强大，是开源软件等等也是选择它的重要原因。

不过需要注意的是，在使用 Clash 之前，你首先需要一个机场，至于什么是机场，可以简单的理解为给你提供科学上网服务的东西，Clash 所起的作用实际上只是把它们提供的服务配置在你的电脑上。至于如何获得机场，可以 Bing 搜索机场推荐自行选择，当然，你也可以使用我用的这个机场[自由鲸](https://www.freewhale.world/auth/register?code=6oVA) 。

在一切开始之前，首先需要知道 Clash 有多个版本：

-   Clash：一个 Go 语言开发的多平台代理客户端，[Github (opens new window)](https://github.com/Dreamacro/clash)
-   ClashX：Clash 的 Mac 图形客户端，[Github (opens new window)](https://github.com/yichengchen/clashX)
-   ClashForAndroid：Clash 的 Android 图形客户端，[Github (opens new window)](https://github.com/Kr328/ClashForAndroid)
-   **Clash for Windows：Clash 的 Windows/macOS/Linux 图形客户端**，[Github (opens new window)](https://github.com/Fndroid/clash_for_windows_pkg)

如果是 Windows，选择 Clash for Windows 就好，如果是 Mac 则选择 ClashX。本教程以 Clash for Windows 为例。

## 基础安装与配置

本节的目的是以较为详细的步骤使读者上手就能用，深入的内容全部放到后面。

### 安装

下载可以去上面的官网下载，但可能访问速度下载速度比较慢，好处是不会有坑，以及版本是最新的。也可以[点击下载](https://static.loxcloud.com/software/windows/Clash.for.Windows.Setup.0.19.23.exe)  ，显然这是我从别的网站那里偷的，不过能用。

下载完之后安装，一路确定就可以完成了。现在运行它，于是我们来到了这个界面：

![[clash界面.png]]

看起来很复杂，但我们只需要进行一点点操作。

### 配置

首先我们打开注册好的机场，然后复制订阅地址（例如下图中只需要点击第一个就好，注意不要点击第三个）：


![[快速添加节点SSR.png|500]]

接下来进入[这个网站](https://sub-web.ohmy.cat/) ：

![[链接订阅网站.png]]

网站界面如此如上图，只需要按照图中操作即可，当然，在复制到上图中一个链接后，可以再返回机场，再复制一条链接，复制到订阅链接这个框中另外一行，例如复制下图中的 V2ray 订阅链接，这样就可以同时使用 SSR 和 V2ray 两个链接（它们各有自己的优点）。

![[快速添加节点V2RAY.png|500]]

接下来不出意外我们应该跳转到了 Clash 的界面，静等一会儿就可以了。

最后，我们转到 Clash 的 General 页面，即：

![[Clash界面2.png]]

只需要按照上图把那两个开关打开，之后我们就可以科学上网了！而且大部分时候你不需要关掉它！

### 为了无痛看 PRC 需要额外进行的操作

为了我们能在看 PRC 的时候不需要关掉它，有一个额外需要的操作，为此，我们打开 Proxies 界面，向下滚动，找到广告拦截、应用净化、漏网之鱼，设置为 DIRECT 即可。

![[Proxies设置界面.png]]

## 进一步讨论

第一个界面是基本设置，不重要，让我们直接看第二个界面，这个界面意味着Clash 共有三种工作模式：

-   全局（Global）：所有请求直接发往**代理服务器**
-   规则（Rule）：所有请求**根据配置文件规则进行分流**
-   直连（Direct）：所有请求**直接发往目的地**

切换不同模式时，对应的节点列表会对应变化。Global 和 Direct 没什么好说的，我们重点看一下 Rule，其中一些规则的意思如下：

- 自动选择，每隔一段时间进行延迟测试，选择延迟最低的节点
- 故障转移，每次都选组内第一个节点，无法使用再换到第二个，依次类推
- 手动选择，顾名思义，没有特殊功能
- 负载均衡，每个节点都用用，由于很多机场都有连接数的限制，因此实际使用较少

![[测速标记.png|200]]

我们可以点击第二个按钮测速。

现在我们可以看第三个界面，我们可以右击打开如下界面：

![[Profiles界面.png|300]]

点击 Rules：

![[Rules界面.png]]

可以看到上面的界面，于是我们就不难理解 Clash 为什么可以不需要时开时关了，因为它会根据定义的规则以及你连什么网站来选择要不要使用代理。我们还可以进一步自己添加规则等。

搜索就会发现，PRC 所在的网站并不在这里面，事实上，所有不在规则内的网站会被归到漏网之鱼里，这就是我们需要把漏网之鱼设置成 DIRECT 的原因。

至于广告拦截和应用净化，纯粹是因为没用所以关了（笑）。毕竟为什么不在浏览器装一个 AdBlock 呢？

如果想要更深入的了解，可以继续自己捣鼓或者看下面的文章，感谢这位大佬：

[Clash for Windows | Clash for Windows (lbyczf.com)](https://docs.cfw.lbyczf.com/)