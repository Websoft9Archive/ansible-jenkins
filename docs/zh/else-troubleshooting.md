# 故障处理

此处收集使用 Jenkins 过程中最常见的故障，供您参考

> 大部分故障与云平台密切相关，如果你可以确认故障的原因是云平台造成的，请参考[云平台文档](https://support.websoft9.com/docs/faq/zh/tech-instance.html)

#### 如何查看错误日志？

日志文件路径为：`/data/logs`。检索关键词 **Failed** 或者 **error** 查看错误

#### Jenkins服务无法启动？

1. 以调试模式运行`jenkins-server console`，便可以查看启动状态和错误
   ```
   jenkins-server console
   ```
2. 打开日志文件：*/data/logs/jenkins-server*，检索 **failed** 关键词，分析错误原因


#### 在Chrome下修改密码后报错？

这个并不是服务器端的问题，只要更新浏览器即可。

![chrome error of Jenkins](https://libs.websoft9.com/Websoft9/DocsPicture/zh/jenkins/jenkins-chromeerror-websoft9.png)

