ssh

toDo install dependencies
install docker

fedora
sudo groupadd docker && sudo gpasswd -a ${USER} docker && sudo systemctl restart docker
newgrp docker

debian
sudo groupadd docker
sudo usermod -aG docker $USER




install pip
dnf install python-pip
dnf install libselinux-python

sudo apt install python-pip
pip install --upgrade setuptools


clean /tmp
