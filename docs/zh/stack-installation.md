# 初始化安装

在云服务器上部署 Jenkins 预装包之后，请参考下面的步骤快速入门。

## 准备

1. 在云控制台获取您的 **服务器公网IP地址** 
2. 在云控制台安全组中，检查 **Inbound（入）规则** 下的 **TCP:80** 端口是否开启
3. 若想用域名访问 Jenkins，请先到 **域名控制台** 完成一个域名解析

## Jenkins 安装向导

1. 使用本地电脑的 Chrome 或 Firefox 浏览器访问网址：*http://域名* 或 *http://Internet IP*, 进入初始化页面
   ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/jenkins/jenkins-installstart-websoft9.png)

2. 运行命令`sudo cat /data/wwwroot/jenkins/secrets/initialAdminPassword`，获取管理解锁密码

3. 成功登录到 Jenkins 后台  
   ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/jenkins/jenkins-installcustomer-websoft9.png)

4. 安装插件  
   ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/jenkins/jenkins-installing-websoft9.png)

5. 创建更多管理员用户  
   ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/jenkins/jenkins-installusers-websoft9.png)

> 需要了解更多 Jenkins 的使用，请参考官方文档：[Jenkins 用户文档中心](https://www.jenkins.io/zh/doc/)

## Jenkins 入门向导

下面范例主要讲述github上项目通过 Jenkins 自动构建部署的过程：

1. 设置 Personal access tokens，自动生成的token只会显示一次，无法再次查看，请注意保存
 ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/jenkins/jenkins-wizard1-websoft9.png)
 ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/jenkins/jenkins-wizard2-websoft9.png)

2. Jenkins全局系统设置，设置完成后请保存
 ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/jenkins/jenkins-wizard3-websoft9.png)
 ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/jenkins/jenkins-wizard4-websoft9.png)
 ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/jenkins/jenkins-wizard5-websoft9.png)

3. 开始构建任务，输入任务名，按流程分别输入github项目url，账号密码等信息后保存
 ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/jenkins/jenkins-wizard6-websoft9.png)
 ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/jenkins/jenkins-wizard7-websoft9.png)
 ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/jenkins/jenkins-wizard8-websoft9.png)
 ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/jenkins/jenkins-wizard9-websoft9.png)
 ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/jenkins/jenkins-wizard10-websoft9.png)
 ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/jenkins/jenkins-wizard11-websoft9.png)

4. 在对应github项目修改后，push提交；Jenkins完成自动化构建部署
 ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/jenkins/jenkins-wizard12-websoft9.png)


## 常见问题

#### 浏览器打开IP地址，无法访问 Jenkins（白屏没有结果）？

您的服务器对应的安全组80端口没有开启（入规则），导致浏览器无法访问到服务器的任何内容

#### Jenkins 解锁密码 initialAdminPassword 是什么？

主要用于第一次登录 Jenkins，解锁密码就是默认的管理员账号 `admin` 对应的密码