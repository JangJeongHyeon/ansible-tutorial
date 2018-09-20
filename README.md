### Ansible tutorial with Docker



1. Ansible installation Via Apt(Ubuntu)
```bash
sudo apt-get update
sudo apt-get install software-properties-common
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get update
sudo apt-get install ansible
```

2. Docker installation Via apt(Ubuntu)
	
	2.1 Uninstall old version
	```bash
	sudo apt-get remove docker docker-engine docker.io
	sudo apt autoremove
	```

	2.2 Install pacakges to allow apt to use a repository over https
	```bash
	sudo apt-get update
	sudo apt-get install apt-transport-https ca-certificates curl software-properties-common
	```

	2.3 Add Docker's official GPG Key
	```bash
	curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-keyy add -
	sudo apt-key fingerprint 0EBFCD88
	```

	2.4 Install stable version
	```bash
	sudo apt-get-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu$(lsb_release -cs)stable"
	```

	2.5 Update the apt package index
	```bash
	sudo apt-get update
	sudo apt-get install docker-ce
	```

	2.4 Verify that Docker CE is installed correctly by running the hello-world image.
	```bash
	sudo docker run hello-world
	```
