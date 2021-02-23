## AFTERNOON ANSIBLE TASK

THIS IS TO BE COMPLETED AFTER THE TUTORIALS FROM THE MODULES COVERED TODAY

Write an Ansible playbook that will install Docker on the local machine. (The VM you have Ansible installed on)

Here are the instructions on how to install Docker, you will need to convert these steps in to Ansible tasks.

- Install these dependencies using APT		
  - apt-transport-https
  - ca-certificates
  - curl
  - software-properties-common
  - python3
  - python3-pip
  - python-setuptools
- Get the Docker APT key located here - https://download.docker.com/linux/ubuntu/gpg
- Add the APT repo - "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionicstable"
- Install docker-ce using APT
- Extras:
  -Install the Docker pip package (Make sure Ansible is using pip3)
	- Add your user to the docker group
	- Reset the connection to ensure the user can complete docker commands.
