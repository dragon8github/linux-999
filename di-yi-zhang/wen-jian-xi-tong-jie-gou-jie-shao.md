## 目录结构和功能介绍

> Linix 系统设计中最优秀的特性之一，就是将所有内容都以文件的形式展示出来。通过一个树形结构统一管理和组织这些文件。

1） /etc 目录

这个目录主要存放系统管理相关的配置文件及子目录。

其中比较重要的有系统初始化文件`/etc/rc`、用户信息文件 `/etc/passwd`等，相关网络配置文件和服务启动文件也在这个目录下。

2） /usr 目录

此目录主要用于存放应用程序和文件。

平时安装的一些软件默认情况下也会安装到此目录内。因此这个目录一般比较大。

3） /var 目录

此目录主要用于存放系统运行及软件运行的日志信息。

4） /dev 目录

包含系统所有的设备文件。

5）/proc 目录

此目录是一个虚拟目录，目录中所有信息都是内存的映射。

可以获取有关进程的有用信息，同事也可以在系统运行中修改内核参数。

与其他目录不同，/proc存在于内存中，而不是硬盘上。

6\) 其他目录

| 目录名 | 介绍 |
| :--- | :--- |
| /boot | 该目录存放的是启动Linux时的一些核心文件，具体包含一些镜像文件和链接文件。因此这个目录非常重要，如果遭到破坏，雄将无法启动。 |
| /bin | bin 其实就是Binary的缩写，该目录存放的都是可执行的二进制文件，就是我们经常使用的Linux命令：ls、cd、cp、vi、mount、df，等等。 |
| /sbin | s 是 Super User的意思，也就是说，只有超级用户才能执行这些命令。譬如磁盘分区命令fdisk、关机命令 shutdown、创建文件系统命令mkfs和初始化系统命令Init等。 |
| /home | 该目录是系统中每个用户的工作目录。在Linux系统中，每个用户都有自己的一个目录，该目录一般由用户的账号命名的。譬如，如果有一个Lee用户，那么它的默认目录就是/home/lee |
| /lib | 该目录存放的是共享程序库和映像文件，可供很多程序使用。 |
| /root | 该目录是Linux超级用户root的默认主目录。 |
| /run | 该目录出现在Centos7.X版本中，是外在设备的自动挂载点目录，用来自动挂碍光驱和U盘。另外，还有一个/media目录，与/run 基本类似。最后，还有一个目录/mnt 主要用来手动挂载一些移动设备，比如可移动磁盘等。 |
| /lost + found | 该目录用于保存丢失的文件。不恰当的关机操作和磁盘错误均会导致文件丢失，这些丢失的文件会临时房在/lost + found下。除了“/”分区上的这个目录外，在每个分区上均有一个lost  + found 目录。 |
| /tmp | 该目录为临时文件目录，主要用于存放临时文件。 |



