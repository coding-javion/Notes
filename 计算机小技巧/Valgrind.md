## Valgrind 的介绍

Valgrind 可以用来检测程序是否有非法使用内存的问题，例如访问未初始化的内存、访问数组时越界、忘记释放动态内存等问题。在 Linux 可以使用下面的命令安装 Valgrind：  

```
$ bzip2 -d valgrind-3.13.0.tar.bz2
$ tar -xf valgrind-3.13.0.tar
$ cd valgrind-3.13.0
$ ./autogen.sh
$ ./configure --prefix=$HOME/valgrind
$ make
$ make install
```

为了能够从任何位置运行 Valgrind，您需要将其添加到您的 PATH 环境变量中。您可以通过在 `~/.bashrc` 或 `~/.bash_profile` 文件中添加以下行来实现这一点：

`export PATH=$HOME/valgrind/bin:$PATH`

之后，您可能需要重新加载您的bash配置或重新登录，以使更改生效：

`source ~/.bashrc`
