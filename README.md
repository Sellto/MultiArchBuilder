## Prerequisites
*Thoses tasks must be do on every linux device*


### Create sudo-user
### Install docker 
#### add your sudo-user into docker group

- fedora
``` 
sudo groupadd docker && sudo gpasswd -a ${USER} docker && sudo systemctl restart docker
newgrp docker
```
- debian
```
sudo groupadd docker
sudo usermod -aG docker $USER
```
### Enable ssh and copy public key.
### Install python dependencies
- fedora
``` 
dnf install python-pip
dnf install libselinux-python
```
- debian
```
sudo apt install python-pip
pip install --upgrade setuptools
```



