> 在RHEL 7.x / CentOS 7.x 版本中，一个最重要的改变就是使用systemd管理机制。
>
> 它不仅可能完成系统的初始化工作，还能对系统和服务进行管理。



### 启动、停止、重启服务

要通过systemctl 命令启动一个Apache HTTP服务，可以使用以下命令。

```
systemctl start httped.service
```

要停掉它，只需要这样：

```
systemctl stop httpd.service
```



