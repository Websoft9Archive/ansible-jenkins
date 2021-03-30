# Initial Installation

If you have completed the Jenkins deployment on Cloud Platform, the following steps is for you to start use it quikly

## Preparation

1. Get the **Internet IP** on your Cloud Platform
2. Check you **[Inbound of Security Group Rule](https://support.websoft9.com/docs/faq/tech-instance.html)** of Cloud Console to ensure the TCP:80 is allowed
3. Make a domain resolution on your DNS Console if you want to use domain for Jenkins

## Jenkins Installation Wizard

1. Using local Chrome or Firefox to visit the URL *http://DNS* or *http://Internet IP*, you will enter installation wizard of Jenkins
   ![](https://libs.websoft9.com/Websoft9/DocsPicture/en/jenkins/jenkins-installstart-websoft9.png)

2. Run the command `sudo cat /var/lib/jenkins/secrets/initialAdminPassword` to get the password

3. Login the Jenkins console  
   ![](https://libs.websoft9.com/Websoft9/DocsPicture/en/jenkins/jenkins-installcustomer-websoft9.png)

4. Install plugins  
   ![](http://libs.websoft9.com/Websoft9/DocsPicture/en/jenkins/jenkins-installing-websoft9.png)

5. Create user for Jenkins  
   ![](https://libs.websoft9.com/Websoft9/DocsPicture/en/jenkins/jenkins-installusers-websoft9.png)

> More useful Jenkins guide, please refer to [Jenkins Documentation](https://www.jenkins.io/zh/doc/)

## Q&A

#### I can't visit the start page of Jenkins?

Your TCP:80 of Security Group Rules is not allowed so there no response from Chrome or Firefox

#### What is the Jenkins's initialAdminPassword?

initialAdminPassword is the default administrator user admin password