# bm-services-docker

## Introduction
* nginx as reverse proxy
* owncloud
* elk stack

## Usage
Create external network for internal container communication
```
docker network create container-net
```
## ToDo

- Add Letsencrypt working to the stack (Certificate renewal does not work)
* Solution 1: Only handle 443 with nginx and have certbot control over port 80
* Solution 2: Try to get the init-letsencryp script running
* Solution 3: Something Else
