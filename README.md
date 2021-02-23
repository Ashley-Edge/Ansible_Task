## Simple ansible playbook

Write an Ansible playbook that will install Docker on a VM with Ansible installed. Here are the instructions on how to install Docker, you will need to convert these steps in to Ansible tasks.

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

## How to check it is working

```
cd Ansible_Task/docker
ansible-playbook playbook.yaml
```
Output
```
[WARNING]: provided hosts list is empty, only localhost is available. Note that the implicit localhost does not match 'all'

PLAY [localhost] ******************************

TASK [Gathering Facts] ******************************
ok: [localhost]

TASK [Installing dependencies using APT] ******************************
ok: [localhost]

TASK [Get the docker APT key] ******************************
ok: [localhost]

TASK [Add the APT repo] ******************************
ok: [localhost]

TASK [Install docker-ce using APT] ******************************
ok: [localhost]

TASK [Starting docker] ******************************
ok: [localhost]

TASK [Install docker pip3 package] ******************************
ok: [localhost]

TASK [Adding user to the docker grpup] ******************************
ok: [localhost]
[WARNING]: Reset is not implemented for this connection

PLAY RECAP ******************************
localhost                  : ok=8    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0 
```
