-----------------------------------------------
## Version Info - packed components
-----------------------------------------------
# Apache HTTPD
Alpine Linux pkg installation
* Server version: Apache/2.4.23 (Unix)
* Server built:   Nov  4 2016 16:35:09

# Apache Tomcat
* apache-tomcat-8.0.39 --> can be configured over Dockerfile

# Java JDK
Alpine Linux pkg installation
* openjdk version "1.8.0_111-internal"
* OpenJDK Runtime Environment (build 1.8.0_111-internal-alpine-r0-b14)
* OpenJDK 64-Bit Server VM (build 25.111-b14, mixed mode)

--------------------------------
## Build / Run the image
--------------------------------
docker build -t="httpd-tomcat" .

# Run the image, create container and expose Ports
 Run basic command with exposing ports
docker run -d -p 80:80 -p 443:443 -it httpd-tomcat
# Run with additional setting the name of the docker container
docker run --name ht -d -p 80:80 -p 443:443 -it java-httpd-tomcat_alpine
# Run with additional setting the hostname inside the docker container
docker run --name ht -h web.mydomain.at -d -p 80:80 -p 443:443 -it java-httpd-tomcat_alpine


--------------------------------
## Login to the container
--------------------------------
docker exec -it ht /bin/bash

