# MailSlurper Docker Container for AARCH64, ARMv7l, X86 and X64

For using MailSlurper with Docker.  
MailSlurper is a handy SMTP mail server useful for local and team application development.  
You can use this image to send mail to a SMTP host
and MailSlurper provides the SMTP server and web frontend.  
For more information on MailSlurper please see MailSlurper [website](http://mailslurper.com/) and [Wiki](https://github.com/mailslurper/mailslurper/wiki).

## Docker Container usage
- copy `mpconfig/custom-config-SAMPLE.json` to `mpconfig/custom-config.json`
- edit the file if needed
- copy `docker-compose-<ARCH>-SAMPLE.yaml` to `docker-compose.yaml`
- edit the file if needed
- run `$ ./dc-m-ms.sh up`

To stop the container run `$ ./dc-m-ms.sh down`

## Email Client configuration
- SMTP port: 2500 (by default)
- SMTP Authentification required?: no
- SMTP via SSL or TLS?: no

## Web Frontend usage
Navigate to `http://localhost:9009` in your webbrowser.  
Note: if you modified the port that is mapped to port 8080 inside the container
you'll need replace "9009" in above URL with that port number.

## Required Docker Image
The Docker Image **mail-mailslurper-\<ARCH\>** will automaticly be downloaded from the Docker Hub.  
The source for the image can be found here [https://github.com/tsitle/dockerimage-mail-mailslurper](https://github.com/tsitle/dockerimage-mail-mailslurper).
