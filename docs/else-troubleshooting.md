# Troubleshooting

We collect the most common troubleshooting of using Jenkins for your reference:

> Instance troubleshooting is closely related to the Instance provider that is Cloud Platform, refer to [Cloud Platform Documentation](https://support.websoft9.com/docs/faq/tech-instance.html)

#### How can I use the logs?

You can find the keywords **Failed** or **error** from the logs directory: `/data/logs`

#### Jenkins service can't start?

1. You can check the status and logs of Jenkins service
   ```
   systemctl status jenkins
   journalctl -xe
   ```
2. Search the keywords **Failed** or **error** from logs: */data/logs/jenkins*