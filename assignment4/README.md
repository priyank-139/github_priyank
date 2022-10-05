# Assignment4 

## Prerequisites

1- master node - Python 3.10.6 | pip | ansible [core 2.13.3]

2- remote server - Python 3.10.6 | 

3- ssh master node to remote server

4-Inventory file content 
```
[ test2 ansible_host=34.217.108.95 ansible_user=ubuntu ansible_ssh_private_key_file=/home/priyank/Downloads/ansible_key.pem ]
```

## create  a role  according to the problem statement

1-ansible-galaxy init system_manager

2-vim git_rep.yml   mvn.yml  softwares.yml  users.yml

3-vim main.yml
```
include_tasks: softwares.yml
include_tasks: mvn.yml  
include_tasks: users.yml
include_tasks: git_rep.yml 
```
4- vim /vars/main.yml
```
- mysql-server
- maven
```

## create a playbook to deploy the services using role system_manager.yml
```
system_manager.yml
```
run a role using command 
```
ansible-playbook system_manager.yml
```
Output of the plabook after deploying the service on the remote server 



![1](https://user-images.githubusercontent.com/114915047/194126333-db513ec5-9960-41f5-834d-a39c7663d44f.png)

![2](https://user-images.githubusercontent.com/114915047/194126362-8d27617e-0de5-49c6-9ca0-a4385aa217e7.png)


