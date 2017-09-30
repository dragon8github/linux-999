> 内容来源：http://www.cnblogs.com/whoamme/p/4039998.html

在Linux CentOS系统上安装完php和MySQL后，为了使用方便，需要将php和mysql命令加到系统命令中，如果在没有添加到环境变量之前，执行“php -v”命令查看当前php版本信息时时，则会提示命令不存在的错误，下面我们详细介绍一下在linux下将php和mysql加入到环境变量中的方法（假设php和mysql分别安装在/usr/local/webserver/php/和/usr/local/webserver/mysql/中）。

**方法一**：直接运行命令：

```
export PATH=$PATH:/usr/local/webserver/php/bin 

export PATH=$PATH:/usr/local/webserver/mysql/bin
```

使用这种方法，只会对当前会话有效，也就是说每当登出或注销系统以后，PATH 设置就会失效，只是临时生效。

---

**方法二**：执行vi ~/.bash\_profile修改文件中PATH一行，将/usr/local/webserver/php/bin 和 /usr/local/webserver/mysql/bin 加入到PATH=$PATH:$HOME/bin一行之后

这种方法只对当前登录用户生效。

---

**方法三**：修改/etc/profile文件使其永久性生效，并对所有系统用户生效，在文件末尾加上如下两行代码：

```
PATH=$PATH:/usr/local/webserver/php/bin:/usr/local/webserver/mysql/bin
export PATH
```

最后：执行 命令**source /etc/profile**或 执行点命令 ./profile使其修改生效，执行完可通过**echo $PATH**命令查看是否添加成功。

