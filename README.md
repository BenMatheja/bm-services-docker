# bm-services-docker

## Introduction
* nginx
* owncloud
* elk stack

## Usage
Create external network for internal container communication
```
docker network create container-net
```
The nginx container depends on all web containers and will crash if started without the services
## ToDo

### Add Letsencrypt working to the stack (Certificate renewal does not work)
* Solution 1: Only handle 443 with nginx and have certbot control over port 80
* Solution 2: Try to get the init-letsencryp script running
* Solution 3: Something Else

### Add Authentication to Kibana
* Solution 1: Build something into nginx (would mean build with custom modules)
* Solution 2: Use something as ID-Provider (Maybe Owncloud?)
* Solution 3: Use Basic Auth (don't want)

### Add Restic Backups
* Solution 1: Run it as seperate Container
* Solution 2: Install it on "bare metal"

### Unify docker-compose files to one
* If possible, just have a single "docker-compose up"