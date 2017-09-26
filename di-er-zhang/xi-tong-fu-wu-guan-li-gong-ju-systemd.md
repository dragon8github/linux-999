> 在RHEL 7.x / CentOS 7.x 版本中，一个最重要的改变就是使用systemd管理机制。
>
> 它不仅可能完成系统的初始化工作，还能对系统和服务进行管理。

### 启动、停止、重启服务

要通过systemctl 命令启动一个httpd服务，既Apache HTTP服务，可以使用以下命令。

```
systemctl start httped.service
```

要停掉它，只需要这样：

```
systemctl stop httpd.service
```

要重启 httpd 服务：

可以使用restart选项。此选项的含义是：如果服务在运行中，它将重启服务，如果服务不在运行中，它将会启动。

也可以使用try-start选项。它只会在服务已经运行的状态下重启服务。

还可以使用reload选项，它会重新加载配置文件。

```
systemctl restart httpd.service
systemctl try-restart httpd.service
systemctl reload httpd.service
```



