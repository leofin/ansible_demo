# ansible_demo
working with ansible to setup a machine with SonarQube's docker image using postgres as DB

## What was used in this project
- EC2 Amazon Linux 2 AMI
- Ansible 2.10.5
- docker version 18.06.1
- postgres:12 - images
- sonarqube:8-community - images

## Prerequisites
- Install Ansible, I used pip to install.
```shell
pip install --user ansible
```

You can find more details about Ansible install guide here:
- https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html

The project uses this plugins:
- community.docker.docker_container
- community.general.docker_network

To install run:
```shell
ansible-galaxy collection install community.docker
ansible-galaxy collection install community.general
```

For more informations:
- https://docs.ansible.com/ansible/latest/collections/community/general/docker_network_module.html
- https://docs.ansible.com/ansible/latest/collections/community/docker/docker_container_module.html
## To setup the enviroment with Ansible
```shell
ansible-playbook site.yml
```

## URL to access the enviroment
http://15.185.223.198:9000/
