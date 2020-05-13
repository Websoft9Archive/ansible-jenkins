# 故障处理

此处收集使用 Jenkins 过程中最常见的故障，供您参考

> 大部分故障与云平台密切相关，如果你可以确认故障的原因是云平台造成的，请参考[云平台文档](https://support.websoft9.com/docs/faq/zh/tech-instance.html)

#### 如何查看错误日志？

日志文件路径为：`/data/logs`。检索关键词 **Failed** 或者 **error** 查看错误

#### Jenkins服务无法启动？

1. 通过查看服务状态以及日志定位错误原因
   ```
   systemctl status jenkins
   journalctl -xe
   ```
2. 打开日志文件：*/data/logs/jenkins*，检索 **failed** 关键词，分析错误原因