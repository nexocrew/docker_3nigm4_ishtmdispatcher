# Supported tags and respective `Dockerfile` links

-	[`0.1.7-beta`, `latest` (*0.1/Dockerfile*)](https://github.com/nexocrew/docker_3nigm4_ishtmdispatcher/0.1/Dockerfile)

# What is 3nigm4 "If Something Happens To Me" dispatcher?
The Ishtm dispatcher manage the delivery of a mail notifying a "will" uploaded by another user who is no more interacting with the the system.

# How to use this image

## start a ishtmdispatcher instance

The following example links to a mongodb container from the official [MongoDb image](https://hub.docker.com/_/mongo/).

```console
$ docker run -d --name ishtm-dispatcher --link mongodb:mongodb nexo/3n4ishtmdispatcher run -d 127.0.0.1:27017 -u dbuser -w dbpwd --smtpaddress 192.168.0.1 --smtpport 443 --smtpuser username --smtppwd pwd 
```
