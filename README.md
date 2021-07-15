# Docker-Installation

### Installation on Ubuntu

First we want check any older Docker version is install on the machine so that we can remove it
```bash
 sudo apt-get remove docker docker-engine docker.io containerd runc
```

Images, containers, volumes, or customized configuration files on your host are not automatically removed. To delete all images, containers, and volumes
```bash
  sudo rm -rf /var/lib/docker
```

```bash
  sudo rm -rf /var/lib/containerd
 ```
 
Install using the repository
Before you install Docker Engine for the first time on a new host machine, you need to set up the Docker repository. Afterward, you can install and update Docker from the repository.

This is the recommended approach.

Set up the repository
Update the apt package index and install packages to allow apt to use a repository over HTTPS:

```bash
 sudo apt-get update
```
 
 ```bash
 sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
 ```
 
 Add Docker’s official GPG key:
```bash
 curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
 ```
 
 Use the following command to set up the stable repository
 ```bash
 echo \
  "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

Update the apt package index, and install the latest version of Docker Engine and containerd, or go to the next step to install a specific version
```bash
sudo apt-get update
```
```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io
```

After installation check Docker version
```bash
 sudo docker version
```

Check Docker service is enable or not
```bash
sudo service docker status
```
if service not service not activated 
```bash
sudo service docker start 
```

Verify that Docker Engine is installed correctly by running the hello-world image.

```bash
 sudo docker run hello-world
 ```
 
 Verify pull image
 ```bash
 sudo docker images
 ```
 
 
 ## Docker installation on windows
 Follow the official page of Docker ,there is direct setup .exe file so we can install docker 
 
 https://docs.docker.com/docker-for-windows/install/
 
 
 
 
 Thanks.
 
 
 
