# FAQ

#### Jenkins support multi-languages?

Yes, you can change you language very easy in you Jenkins Console

#### Is there CLI tool for Jenkins?

Yes, please refer to [Jenkins CLI](/zh/solution-cli.md)

#### How can I extend more functions for Jenkins?

Install more [plugins](https://plugins.jenkins.io/)

#### If there is no domain name, can I deploy Jenkins?

Yes, visit Jenkins by *http://Internet IP*

#### Is it possible to modify the source path of Jenkins?

No

#### How to change the permissions of filesytem?

Change owner(group) or permissions like below:

```shell
chown -R nginx.nginx /data/wwwroot
find /data/wwwroot -type d -exec chmod 750 {} \;
find /data/wwwroot -type f -exec chmod 640 {} \;
```

#### What's the difference between Deployment and Installation?

- Deployment is a process of installing and configuring a sequence of software in sequence in a different order, which is a complex system engineering.  
- Installation is the process of starting the initial wizard after the application is prepared.  
- Installation is simpler than deployment. 

#### What's Cloud Platform?

Cloud platform refers to platform manufacturers that provide cloud computing services, such as: **Azure, AWS, Alibaba Cloud, HUAWEI CLOUD, Tencent Cloud**, etc.

#### What is the difference between Instance, Cloud Server, Virtual Machine, ECS, EC2, CVM, and VM?

No difference, just the terminology used by different manufacturers, actually cloud servers