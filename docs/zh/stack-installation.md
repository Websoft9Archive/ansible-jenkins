# 初始化安装

在云服务器上部署 Jenkins 预装包之后，请参考下面的步骤快速入门。

## 准备

1. 在云控制台获取您的 **服务器公网IP地址** 
2. 在云控制台安全组中，检查 **Inbound（入）规则** 下的 **TCP:15672** 端口是否开启
3. 若想用域名访问 Jenkins，请先到 **域名控制台** 完成一个域名解析

## Jenkins 安装向导

1. 使用本地电脑的 Chrome 或 Firefox 浏览器访问网址：*http://域名* 或 *http://Internet IP*, 进入初始化页面
   ![](https://libs.websoft9.com/Websoft9/DocsPicture/en/jenkins/jenkins-installstart-websoft9.png)

2. 运行命令`sudo cat /var/lib/jenkins/secrets/initialAdminPassword`，获取管理解锁密码

3. 成功登录到 Jenkins 后台  
   ![](https://libs.websoft9.com/Websoft9/DocsPicture/en/jenkins/jenkins-installcustomer-websoft9.png)

4. 安装插件  
   ![](https://libs.websoft9.com/Websoft9/DocsPicture/en/jenkins/jenkins-installing-websoft9.png)

6. 修改管理员admin的密码
   ![](https://libs.websoft9.com/Websoft9/DocsPicture/en/jenkins/jenkins-modfiypw-websoft9.png)

5. 创建更多管理员用户  
   ![](https://libs.websoft9.com/Websoft9/DocsPicture/en/jenkins/jenkins-installusers-websoft9.png)

> 需要了解更多 Jenkins 的使用，请参考官方文档：[Jenkins 用户文档中心](https://www.jenkins.io/zh/doc/)

## 常见问题

#### 浏览器打开IP地址，无法访问 Jenkins（白屏没有结果）？

您的服务器对应的安全组80端口没有开启（入规则），导致浏览器无法访问到服务器的任何内容

#### Jenkins 解锁密码 initialAdminPassword 是什么？

主要用于第一次登录 Jenkins，解锁密码就是默认的管理员账号 `admin` 对应的密码