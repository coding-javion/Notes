---
created: 2024-06-20 T20:05:24 (UTC +08:00)
tags: []
source: https://blog.csdn.net/m0_62171658/article/details/128062482
Author:
---

一、问题描述

 ![](https://img-blog.csdnimg.cn/d4f91def18a4426697b819f5f6388931.png)

一直显示正在安装，几个小时也没动静，特别是那个 c/c++插件的安装。

二、解决方法——采用手动安装插件的方式

 **①、先去这个网站找你要安装的插件，然后下载到本地电脑。**

 [All categories Extensions - Visual Studio Marketplace]( https://marketplace.visualstudio.com/search?target=VSCode&category=All%20categories&sortBy=Installs "All categories Extensions - Visual Studio Marketplace")

 ![](https://img-blog.csdnimg.cn/0689c16825334562a1147b53ddad1256.png)

  比如我要下载 Cmake

 ![](https://img-blog.csdnimg.cn/fd7fea2f434d4511b234d6c27881a877.png)

  ![](https://img-blog.csdnimg.cn/d9a738dc31b443b3a8a72a6bbd905917.png)

  点红色框里的 Download Extension

 ![](https://img-blog.csdnimg.cn/e119712adc4e42c095de1a1e29ee56e6.png)

  ![](https://img-blog.csdnimg.cn/87a768062e1440bbad7844aafcfb731b.png)

  下载成功！！！

 **②上传到 linux 服务器**

 ![](https://img-blog.csdnimg.cn/a43422fd162747a1884154d1f2742dc1.png)

 ![](https://img-blog.csdnimg.cn/4b111682a0274242b53ad3db00c82f94.png)

  ![](https://img-blog.csdnimg.cn/d65b16eee0df489ab530be8b7b54d5c2.png)

 **如果 rz 上传文件时遇到乱码问题，解决方法如下：**

 **先删除乱码文件，然后重启 xshell，再试一次 rz 上传文件。**

 **不行就进行下面系列操作。**

 ![](https://img-blog.csdnimg.cn/31ce7ae3b278462eb58dd2a82722c271.png)

  ![](https://img-blog.csdnimg.cn/132bcda9fce346b6a1506adb04249185.png)

 ![](https://img-blog.csdnimg.cn/837b5515483e460d8ce683e5ff84b17d.png)

 **③打开 vscode 链接远程，使用 vsix 安装。**

 ![](https://img-blog.csdnimg.cn/3845258a6d004f6f92fbc4666c12dbd5.png)

  ![](https://img-blog.csdnimg.cn/deb9219df5f54597acd1fd24ce54d8aa.png)

  ![](https://img-blog.csdnimg.cn/7df5fc7a766b4e638696e290202966d5.png)

  安装完毕！！！！记得删除安装包

copilot 可以直接在设置中添加：
```json
"remote. ExtensionKind": {
        "GitHub. Copilot": ["ui"],
        "GitHub. Copilot-chat": ["ui"],
    },
```
