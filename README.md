# Docker-Compose
Ubuntu 19.10 Installation


Table of Contents
=================
* [Install Compose](#install-compose)
* [Install Docker](#install-docker)


## Install Compose
This is a short writeup from the [documentation](https://docs.docker.com/compose/install/).

The following commands will work on Ubuntu 19.*

**1. Run this command to download the current stable release of Docker Compose:**
```
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.24.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
**2. Apply executable permissions to the binary:**
```
$ sudo chmod +x /usr/local/bin/docker-compose
```

**Test installation:**
```
$ docker-compose --version
docker-compose version 1.24.1, build 1110ad01
```




## Install Docker
docker: https://docs.docker.com/install/linux/docker-ce/ubuntu/

`sudo apt-get update`

`sudo apt-get install \

    apt-transport-https \
    
    ca-certificates \
    
    curl \
    
    gnupg-agent \
    
    software-properties-common`
    
Add Docker’s official GPG key:

`curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -`


`
$ sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
 `
 
 ### NOTE: 
     if you are using version 19.10 (Eon), which is currently (19. Oct) not supported, you can replace 
     `$(lsb_release -cs)` with `disco`. (somewhat hacky, but it does work)
     
     
$ sudo apt-get update
$ sudo apt-get install docker-ce docker-ce-cli containerd.io

See that everything works:
`$ sudo docker run hello-world`


     
 ## Install Django
 sudo apt-get install python3 python3-pip
sudo apt-get install python3-django

check:
django-admin --version
 
   
