简单地说，SecureCRT就是window下登录 UNIX 或 Linux 服务主机的软件，SecureCRT 支持 SSH\*（SSH1 和 SSH2）。

SSH的英文全称是 Secure Shell，属于网络服务的一种。类似于我们知道的Telnet和 FTP服务。但SSH又与 Telnet 和 FTP 服务不同的：

* 传统的Telnet 和 FTP在数据传输上是不安全的，因为它们在网络上传送的数据和密码都是以明文的形式发送，这样一来，网络黑客就非常容易的截取传送的数据和密码。

* 而通过SSH客户端与Linux服务端通信时，所有传送的数据都是经过加密处理的，即使黑客中途获取了传送的数据。也无法得到传送的内容。同时SSH的数据传输都是经过压缩的，这样就提高了数据传输的速度。



