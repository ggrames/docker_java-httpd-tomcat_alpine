## Build the image:
docker build -t="httpd-tomcat" .

## Run the image, create container and expose Ports
# Run basic command with exposing ports
docker run -d -p 80:80 -p 443:443 -it httpd-tomcat
# Run with additional setting the name of the docker container
docker run --name ht -d -p 80:80 -p 443:443 -it httpd-tomcat
# Run with additional setting the hostname inside the docker container
docker run --name ht -h web.grames.at -d -p 80:80 -p 443:443 -it ggrames/java-httpd-tomcat_alpine

## Login to the container
docker exec -it ht /bin/bash
