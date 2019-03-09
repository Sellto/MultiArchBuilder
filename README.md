## Prerequisites
*Thoses tasks must be do on every linux device*

### Install Ansible
- debian
Add the following line to /etc/apt/sources.list:
```
deb http://ppa.launchpad.net/ansible/ansible/ubuntu trusty main
```

Then run these commands:
```
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 93C4A3FD7BB9C367
sudo apt-get update
sudo apt-get install ansible
```
### Create sudo-user
*Readme in progress*
### Install docker
*Readme in progress*
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
#### Add to one device the experimental docker capabilities.
*Readme in progress*

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

## Playbook Configuration
### Add your docker account information
Replace commmented informations by yours
in the file : /roles/pre-task/tasks/set_facts.yml

```
- name: Get docker account data
  set_fact:
    image_name : #imagename
    username   : #yourdockerusername
    password   : #yourpassward
    email      : #youremail
 ```   
### Update your playbook inventory
Use the hosts.ini.sample file to create your host.ini inventory
and place it into the inventory folder
#### ALL section
*Readme in progress*
#### Experimental section
*Readme in progress*
#### Other section
*Readme in progress*

## Launch the playbook
`ansible-playbook -i inventory/hosts.ini multiarch-img.yml`
