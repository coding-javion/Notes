## 为什么要用 zotero？

zotero 是一个论文管理软件。

zotero 是一个开源的、强大的、可以安装插件的论文管理和阅读软件，而最重要的是，由于它的强拓展性，它可以和很多软件或者工具联动！

## 基础安装与配置

### 安装

去[官网](https://www.zotero.org/)下载即可。

### 配置

zotero 的几乎不需要操作就可以直接使用，只需要将 pdf 直接拖进 zotero 或者使用浏览器插件即可将 pdf 等导入 zotero。但为了更方便的使用，可以根据需要配置。点击左上角的编辑-首选项，即可打开下列界面，可以根据需要调整常规选项。

![[Zotero首选项-常规.png]]

数据同步最好是开启，不过这首先需要注册一个账户。文件同步建议关闭，因为 zotero 自带的空间比较小，我们可以通过 [[#zot-file]] 使用自己的同步工具同步。

![[Zotero首选项-同步.png]]

如果我们想用自己的工具同步，有一件事是必须做的，那就是把论文放到我们自己的文件夹中，这是因为 zotero 自己存论文的时候会将其放在乱码文件夹中，完全无法找到。
把论文放到自己的文件夹中不需要手动操作，只需要将高级-文件和文件夹中的根目录需要设置为论文的存放路径：

![[Zotero首选项-高级.png]]

之后全选所有的文献，如下操作：

![[点击论文右键.png|400]]

### 配置/插件推荐

#### pdf-translator

pdf-translator 的作用是翻译 pdf，只需要选中即可自动翻译。可以在右侧更改翻译引擎，只要没有小钥匙标志的都可以随意使用。

![[选择翻译引擎.png|400]]

#### zot-file

zotfile 的主要作用是自动重命名和自动把论文移动到自定义的文件夹。点击工具-zotfile preference。
第一行的文件夹设置为论文下载到的位置（可以设置为 C 盘的下载文件夹），Custom location 设置为自定义存放论文的文件夹（这里必须和之前设置的一样），其它地方如图设置：

![[zotfile-general settings.png]]

Renaming Rules 如图设置即可（可以不改变）。

![[Pasted image 20230430222247.png]]

一般来说，移动和重命名自动完成的，如果有时候不能自动完成，可以手动右键 Manage attachments-Rename and Move。

#### Sci-hub

zotero sci-hub 插件基本可以直接用，如果不能成功，可以去编辑-首选项-Zotero-Scihub 中把 Sci-hub URL 改成 https://sci-hub.ee/ ，或者你可以正常登陆的 sci-hub 网址。

![[Zotero首选项-ZoteroScihub.png]]

#### Zotero PDF Preview

PDF Preview 是一个可以预览 pdf 的插件，使用效果如图：

![[PDF Preview示意.png]]

右下角的预览就是 viewer 的效果。

#### RSS

RSS 订阅只需要到官网上把网址复制到下图中就好了，例如 PRC： http://feeds.aps.org/rss/recent/prc.xml ，PRL Nuclear Physics： http://feeds.aps.org/rss/tocsec/PRL-NuclearPhysics.xml 。

![[Zotero-RSS.png|300]]



## 进一步讨论

以后写。