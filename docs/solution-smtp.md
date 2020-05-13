# SMTP

Sending mail is a common feature for Jenkins. After a large number of user practice feedback, only one way is recommended, that is, using the **third-party STMP service** to send the email.

> Do not try to install **Sendmail** or other Mail server software on your Cloud Server for sending mail, because it is very difficulty in maintenance.

Follow is the sample using **SendGrid's SMTP Service** to configure sending mail for Jenkins:

1. Install the Jenkins plugin [Email Extension](https://plugins.jenkins.io/email-ext/)
   ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/jenkins/jenkins_installemailplugin-websoft9.png)

2. Log in SendGrid console, prepare your SMTP settings like the follow sample
   ```
   SMTP host: smtp.sendgrid.net
   SMTP port: 25 or 587 for unencrypted/TLS email, 465 for SSL-encrypted email
   SMTP Authentication: must be checked
   SMTP Encryption: must SSL
   SMTP username: websoft9smpt
   SMTP password: #fdfwwBJ8f    
   ```
3. Log in Jenkins Console, open 【Manage Jenkins】>【Configure System】, set you SMTP
   ![Jenkins SMTP](https://libs.websoft9.com/Websoft9/DocsPicture/zh/jenkins/jenkins_configuresmtp-websoft9.png)

4. Test it

More SMTP Service(Gmail, Hotmail, QQ mail, Yahoo mail, SendGrid and so on)  settings or Issues with SMTP, please refer to Websoft9's *[SMTP Guide](https://support.websoft9.com/docs/faq/tech-smtp.html)*