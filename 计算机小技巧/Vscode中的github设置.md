# git 配置

```bash
git config --global user.name "myname" #myname是注册github的用户名
git config --global user.email "email@***.com" #email是注册关联的邮箱
```

>按道理是每个仓库（不同电脑上同一个工程仓库是不一致的）可以配置一个不同的name，但是我们通过global参数全局定义了name。那么一台电脑上的是每个仓库管理者都是相同的名字。

# 配置密钥

```bash
ssh-keygen -t rsa -C "shangahaoyu1@163.com" #-C是加了一些注释
```

去产生公钥的位置复制公钥，加入到github-setting-SSH and GPG keys中即可

# vscode特有的插件

## git history

在安装此插件后，vscode在右上会出现

![[Pasted image 20230410105733.png|225]]

这一栏。

![[Pasted image 20230410110304.png|25]]：可以展开此版本与之前版本的差异（修改的地方）

## gitLens

## git graph

可以绘制漂亮的历史提交图

在左下角可以直接点

![[Pasted image 20230518152918.png|400]]

# 克隆到本地

>注：
>服务器上git管理的仓库是没法上传到外网的（服务器没有网络），我们需要把服务器上的仓库先克隆下来再上传到我们的GitHub上
在需要放仓库的地方敲如下命令行

```cmd
git clone shy@162.105.151.37:/home_data/shy/n3lo
```

也可以在vscode中实现，任意本地窗口使用"ctrl(右)+shift(右)+P"打开命令行，选择git：clone选项，输入URL即可。他会提示你选在哪里clone

# 提交到github中

首先需要在github中建立一个仓库

## 建立本地与网上仓库的联系

![[Pasted image 20230420213548.png|450]]

如上点击add remote

![[Pasted image 20230420213623.png|375]]

这里输入网上建立仓库的URL或者网址（服务器中格式为“拉到本地”章clone后面的语句）

下一步取一个名字

## 上传仓库到github

![[Pasted image 20230420213813.png|475]]

如上选择

![[Pasted image 20230420213849.png|450]]

选择你刚刚建立连接的仓库即可

>注：
>vscode上使用远程最好把梯子关掉
>pull的时候最好本地的主分支历史上是有和远程现有head一致的版本的否则会出错

# 提交到服务器中

考虑到代码有可能在服务器中调试，需要将本地的push到服务器中。这时候服务器中的工作区有一些未提交的文件可能会被改变（这里前提是服务器中的和本地的已经在提交的版本上merge过了）

此时只需要首先checkout到一个新的分支，再在本地push。最后到远程中checkout回来即可

# 冲突解决

当有很多地方都有咱写的这个库的时候，就会由于版本不一致产生了冲突。我们可能不能直接push和pull，这需要下面这些功能

## merge

### 快进式合并

当被合并的分支的历史完全包含在将要合并到的分支的历史中，这时merge操作会直接将被合并的分支指向合并到的分支

### 普通合并

在左边的选项卡里会看到branch选项卡，在这里右击选择merge into current branch即可

![[Pasted image 20230427114317.png|475]]

## fetch