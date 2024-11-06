![Ansible Is Nice](ansibleitsnice.jpg)

# Ansible Class Task

- Create bash script that determines Linux Distro based on os-release file in `/etc` folder
- Use ansible to copy script to all servers in inventory file
- Run the script on all the servers in the inventory file


## Table Of Contents

- [Prerequisites](#prerequisites)
- [Usage](#usage)
- [Script](#script)
- [Installation](#installation)
- [Contributing](#contributing)


## Prerequisites
1. Linux Debian distribution 
2. Docker environment installed (docker-compose)
3. Ansible installed


## Usage 
In this task, we create an environment of four different nodes, each with a different OS and an Ansible host node. 
The bash script created will check which Linux distrobution is installed in each node. 
The task will be preformed by ansible playbook connecting and runnig the task on each node. 

![Architecture](ansible_arch.png)


## Script 
''' #!/bin/bash '''

''' # Read the /etc/os-release file ''' 
''' source /etc/os-release '''

''' # Print the distro information ''' 
''' echo "The distro is: ${PRETTY_NAME}" '''


## Installation 
### Updating, upgarding and installing in linux debian: 

1. ''' sudo apt update '''
2. ''' sudo apt-get upgrade '''
3. ''' sudo apt install docker-compose '''
4. ''' ansible --version '''

### Uploading Docker nodes: 

5. ''' mkdir -p task/ansible/docker '''
6. ''' git init '''
7. ''' 
