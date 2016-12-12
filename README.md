## Build the image:
docker build -t="httpd-tomcat" .

## Run the image, create container and expose Ports
docker run --name ht -d -p 80:80 -p 443:443 -it httpd-tomcat

## Login to the container
docker exec -it ht /bin/bash
