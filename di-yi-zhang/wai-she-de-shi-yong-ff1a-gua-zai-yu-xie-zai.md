# Linun下外设的使用：挂载与卸载

在Linux中使用外设（如软盘、U盘、光驱和磁带等）的时候，不像Windows下那么智能，都需要通过**挂载**方式才能使用。

> 在Linux系统中，硬件设备都以文件的形式存在。
>
> 事实上，在Linux中所有对象都可以看成文件【in UNIX, everything is file】.

因而不同的硬件设备有不同的文件类型，常见的文件类型如表：

| 文件系统格式 | 备注 |
| :--- | :--- |
| msdos | DOS文件系统类型 |
| vfat | 支持长文件名的DOS分区系统类型，也可理解为Window文件系统类型 |
| iso9660 | 光盘格式文件系统类型 |
| ext2/ext3/ext4 | Linux下的主流文件系统类型 |
| xfs | Linux 下一种高性能的日志文件系统，在Centos 7.X中为默认文件系统 |

挂载点就是在Linux下制定的挂载目录，将设备指定到这个挂载目录后，以后访问这个挂载目录，就相当于访问这个设备了。

* Linux 系统中有一个`/mnt` 目录，专门用作临时挂载点目录；
* 此外，Linux系统中还有一个`/media`目录，此目录是一个自动挂载的目录，主要用于自动挂载光盘、U盘等移动设备；
* 在Centos7.X版本中，出现一个`/run`自动挂载目录，所有移动设备都会自动挂载到这个目录下。

#### Linux 下挂载的命令如下：

```
mount -t 【系统类型】 【设备名】 【挂载点】
```

**1）挂载软盘**

```
mount -t msdos /dev/fd0 /mnt/floppy
```

这样就将DOS文件格式的一张软盘装载进来，以后就可以在`/mnt/floppy` 目录下找到这张软盘的所有内容。

**2）挂载光盘**

```
mount -t iso9660 /dev/hda /mnt/cdrom
```

这里需要注意一个问题，用`mount`命令挂载的是软盘、光盘和U盘，而不是软驱和光驱。

### 卸载设备的命令：

```
umount /mnt/usb
```

例如卸载光盘可输入如下命令：

```
umount /mnt/cdrom
```

Linux 对文件系统的保护做的很到位，在光盘没有卸载之前，光驱上面的弹出键不起任何作用。

