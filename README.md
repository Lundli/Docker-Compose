# Docker-Compose
Installation guide for Ubuntu. Version 19.10 (eoan) used for this writeup.


## Table of Contents
=================
* [Install Compose](#install-compose)
* [Install Docker](#install-docker)
    * [Ubuntu based distro](#ubuntu-based-distro)
* [Install Django](#install-django)


## Install Compose
This is a short writeup from the [documentation](https://docs.docker.com/compose/install/).


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
Short writeup from the [documentation](https://docs.docker.com/install/)

The following steps will work on ubuntu. See [docker](https://docs.docker.com/install/linux/docker-ce/ubuntu/) for Ubuntu documentation.


**1. Update packages**
`
$ sudo apt-get update
`

**2. Install packages to allow apt to use a repository over HTTPS:**
```
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
```
    
**3. Add Docker’s official GPG key:**
```
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

**Verify fingerprints**

Verify that you have a key with fingerprint `9DC8 5822 9FC7 DD38 854A E2D8 8D81 803C 0EBF CD88`<br/>
```
$ sudo apt-key fingerprint 0EBFCD88
```

**4. To install the stable repository**
<br/>(x86_64 / amd64)
```
$ sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```

### Ubuntu-based-distro

If you are using a Debian based distro (such as Linux Mint), you have to replace `$(lsb_release -cs) \` with the name of your upstream distro.

**Example 1:**
If you are using Linux Mint 19.1 (Tessa), you would have to replace `$(lsb_release -cs) \` with `bionic \`, as that is the upstream distro.

**Example 2:**
If you are using Ubuntu 19.10 (which as of 20.10.2019) is not currently supported, you could replace `$(lsb_release -cs) \` with `disco \` (distro name of Ubuntu 19.04).



### Install docker engine - community
**1. Update package manager**
```
$ sudo apt-get update
```

**2. Install the latest version of Docker Engine - Community and containerd (see documentation to install a specific version)**
```
$ sudo apt-get install docker-ce docker-ce-cli containerd.io
```

**3. Verfiy that installation succeeded**

`
$ sudo docker run hello-world
`


#### To Upgrade docker enginge - community
To upgrade Docker Engine - Community, first run `$ sudo apt-get update`, then follow the installation instructions, choosing the new version you want to install.


   
   
 ## Install Django
 
**Update package manager**
```
$ sudo apt-get update
```
 

```
$ sudo apt-get install python3 python3-pip
$ sudo apt-get install python3-django
```

**Verify that Django installation succeeded:**
```
$ django-admin --version
```
   
