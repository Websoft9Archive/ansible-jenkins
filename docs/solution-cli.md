# CLI

JJenkins has a built-in command line interface that allows users and administrators to access Jenkins from a script or shell environment. This can be convenient for scripting of routine tasks, bulk updates, troubleshooting, and more.

Refer to the following step to use your CLI:

```
wget -O /data/wwwroot/jenkins/jenkins-cli.jar http://localhost/jnlpJars/jenkins-cli.jar
cd /data/wwwroot
java -jar jenkins-cli.jar -ssh

...................
Neither -s nor the JENKINS_URL env var is specified.
Jenkins CLI
Usage: java -jar jenkins-cli.jar [-s URL] command [opts...] args...
Options:
 -s URL              : the server URL (defaults to the JENKINS_URL env var)
 -http               : use a plain CLI protocol over HTTP(S) (the default; mutually exclusive with -ssh)
 -webSocket          : like -http but using WebSocket (works better with most reverse proxies)
 -ssh                : use SSH protocol (requires -user; SSH port must be open on server, and user must have registered a public key)
 -i KEY              : SSH private key file used for authentication (for use with -ssh)
 -noCertificateCheck : bypass HTTPS certificate check entirely. Use with caution
 -noKeyAuth          : don't try to load the SSH authentication private key. Conflicts with -i
 -user               : specify user (for use with -ssh)
 -strictHostKey      : request strict host key checking (for use with -ssh)
 -logger FINE        : enable detailed logging from the client
 -auth [ USER:SECRET | @FILE ] : specify username and either password or API token (or load from them both from a file);
                                 for use with -http.
                                 Passing credentials by file is recommended.
                                 See https://jenkins.io/redirect/cli-http-connection-mode for more info and options.
```

More detail refer to：[Jenkins CLI ](https://www.jenkins.io/zh/doc/book/managing/cli/)