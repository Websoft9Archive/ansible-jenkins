# FAQ

#### Jenkins 是否支持中文？

支持，可以很方便的切换多语言（包括中文），Jenkins根据浏览器的语言显示文本，详情参照[Jenkins 语言设置](https://www.jenkins.io/doc/book/using/using-local-language/)。

#### Jenkins 是否提供CLI工具？

是，参考 [Jenkins CLI](/zh/solution-cli.md)

#### 如何扩展Jenkins的功能？

安装更多[插件](https://plugins.jenkins.io/)

#### 如果没有域名是否可以部署 Jenkins？

可以，直接通过服务器公网IP访问即可

#### 是否可以修改Jenkins的源码路径？

不可以

#### 如何修改上传的文件权限?

```shell
# 拥有者
chown -R nginx.nginx /data/wwwroot/
# 读写执行权限
find /data/wwwroot/ -type d -exec chmod 750 {} \;
find /data/wwwroot/ -type f -exec chmod 640 {} \;
```

#### 部署和安装有什么区别？

部署是将一序列软件按照不同顺序，先后安装并配置到服务器的过程，是一个复杂的系统工程。  
安装是将单一的软件拷贝到服务器之后，启动安装向导完成初始化配置的过程。  
安装相对于部署来说更简单一些。 

#### 云平台是什么意思？

云平台指提供云计算服务的平台厂家，例如：Azure,AWS,阿里云,华为云,腾讯云等

#### 实例，云服务器，虚拟机，ECS，EC2，CVM，VM有什么区别？

没有区别，只是不同厂家所采用的专业术语，实际上都是云服务器