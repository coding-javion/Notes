---
authors: Shang Haoyu
---

点开左边remote explorer项，其中SSH右边的设置按钮可以打开config file

```SSH 
Host 自己起个名字，你喜
    HostName 远程服务器的IP地址
    User 系统用户名
    Port 端口号，SSH一般都是22
    IdentityFile 密钥对里的私钥的本地保存位置(用双引号括起来)

```

为了不每次输入密码，可以使用密钥

其概念就是一个锁一个钥匙，都可以在本地生成（先买一个带钥匙的锁）。钥匙是私钥，锁是公钥。然后将锁安到服务器上就行了。

## 在本地生成密钥

```cmd
ssh-keygen
```

然后一路回车使用默认参数即可（一定不要改路径）。在上述过程中，第一步是产生密钥的地址，可以去对应的路径看相应的文件。

## 上传公钥到服务器

把公钥放到.ssh/authorized_keys文件里

* 手动上传

将公钥中复制到上述文件中即可，注意换行。

* 自动上传

```cmd
ssh-copy-id -i id_rsa user@host
```

其中id_rsa(.pub)是公钥文件的名字，上述命令可以自动帮助你复制到指定文件中。

## 补充注意事项

通过 vscode 使用远程会在远程上有一些配置文件，如果出现一些问题，可以用如下解决方案。

**点击view下的‘command palette’下的’remote-ssh: kill vs code server on host…'**