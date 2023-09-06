#Docker 

Docker allows you to package and run applications in isolated containers, making it easier to deploy, manage, and scale applications across different environments.

# What is a container
A container contains only the application and her dependencies.
It is also called an ==image==.
==A Docker image is a **folder** with a [[Introduction#Dockerfile|Dockerfile]] at the root. It can also contain many other files in order to copy them into your `VM`.==

# Docker Hub
[Docker Hub](https://hub.docker.com/) is like the **App Store**, it contains a lots of images (=containers).

# Dockerfile
A `dockerfile` is the main file of a docker image.
## Example
A `NGINX` image (to host websites)
```dockerfile
FROM		alpine:3.12  						

RUN			apk update && apk upgrade && apk add	\ 													openssl			\ 													nginx			\ 													curl			\ 													vim				\ 													sudo  						
RUN			rm -f /etc/nginx/nginx.conf  						

COPY		./config/nginx.conf /etc/nginx/nginx.conf
COPY		scripts/setup_nginx.sh /setup_nginx.sh  				

RUN			chmod -R +x /setup_nginx.sh  						

EXPOSE		443  						

ENTRYPOINT	["sh", "setup_nginx.sh"]`
```

## Keywords
### `FROM`
- Is **mandatory**. 
- First word of the file.
- Indicate the OS of the virtual machine. 
- Most used are `debian:buster` for **Debian** and `alpine:xxx` for **Linux**.
### `RUN`
- Run a command.
- Usually the firsts `RUN` upgrade the `VM` resources like `apk`,... 
### `COPY`
- Copy a file from the folder to a place in the `VM`.
### `EXPOSE`