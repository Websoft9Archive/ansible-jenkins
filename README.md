# Jenkins自动化安装与部署

本项目是由 [Websoft9](http://www.websoft9.com) 研发的 [Jenkins](https://jenkins.io) 自动化安装程序，开发语言是 Ansible。使用本项目，只需要用户在 Linux 上运行一条命令，即可自动化安装 Jenkins，让原本复杂的安装过程变得没有任何技术门槛。  

本项目是开源项目，采用 LGPL3.0 开源协议。

## 配置要求

操作系统：目支持Ubuntu18.x 以上部署此脚本  
硬件配置：最低1核2G，10G系统盘空间，否则无法安装

更多配置要求请参考官方文档：https://jenkins.io/zh/doc/pipeline/tour/getting-started/


## 组件

包含的核心组件为：Jenkins,Nginx,Java,Docker

更多请见[参数表](/docs/zh/stack-components.md)

## 本项目安装的是 Jenkins 最新版吗？

本项目采用APT安装，Jenkins官方已经提供了保持最新的源地址，因此可以保证每次安装都是最新版本。

Jenkins的[版本号查看](https://jenkins.io/zh/download/)

## 安装指南

## 安装指南

登录 Linux，运行下面的**命令脚本**即可启动自动化部署，然后耐心等待，直至安装成功。

```
#非 root 用户登录后，需先提升成为 root 权限
sudo su -

#自动化安装命令
wget https://raw.githubusercontent.com/Websoft9/linux/master/ansible_script/install.py ; python install.py playb=jenkins url=https://github.com/Websoft9/ansible-jenkins.git init=0 ansible=y

```

注意：  

1. 自动化脚本需服务器上已经安装 Python 2.7 或以上版本方可运行，一般操作系统会自带 Python。如果无法运行，系统会提示用户先安装 Python，再运行自动化安装命令。
2. 由于自动化安装过程中有大量下载任务，若网络不通（或速度太慢）会引起下载失败，从而导致安装程序终止运行。此时，请重置服务器后再次尝试安装，若仍然无法完成，请使用我们在公有云上发布的 [BT 镜像](https://apps.websoft9.com/jenkins) 的部署方式


## 文档

文档链接：https://support.websoft9.com/docs/jenkins

## FAQ

- 命令脚本部署与镜像部署有什么区别？请参考[镜像部署-vs-脚本部署](https://support.websoft9.com/docs/faq/zh/bz-product.html#镜像部署-vs-脚本部署)
- 本项目支持在 Ansible Tower 上运行吗？支持
