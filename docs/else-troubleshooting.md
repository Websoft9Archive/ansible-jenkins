# Troubleshooting

We collect the most common troubleshooting of using Jenkins for your reference:

#### How can I use the logs?

You can find the keywords **Failed** or **error** from the logs directory: `/data/logs`

#### Jenkins service can't start?

1. Use the debug mode of `jenkins-server console` and you can see the errors
   ```
   jenkins-server console
   ```
2. Search the keywords **Failed** or **error** from logs: */data/logs/jenkins-server*

#### Error in Chrome when modify password?

This error is not attribute to Jenkins server, once you have upgraded you local Chrome, it solved

![chrome error of Jenkins](https://libs.websoft9.com/Websoft9/DocsPicture/zh/jenkins/jenkins-chromeerror-websoft9.png)