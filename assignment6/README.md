# ASSIGNMENT 6

## Prerequisites

1- master node - Python 3.10.6 | pip | ansible [core 2.13.3]

2- remote server - Python 3.10.6 | 

3- ssh master node to remote servers

## Inventory file content
```
[amazon_debian]
test2 ansible_host=34.217.108.95 ansible_user=ubuntu ansible_ssh_private_key_file=/home/priyank/Downloads/ansible_key.pem
test1 ansible_host=35.91.73.204 ansible_user=ec2-user ansible_ssh_private_key_file=/home/priyank/Downloads/ansible_key.pem

```

## Steps to create role for assignmet6

1- ansible-galaxy init assignment6
2- cd tasks
3- vim git_rep.yml  group.yml   mysql_setup.yml  nginx_setup.yml  tomcat_setup.yml  users.yml
4- vim main.yml
```
  include_tasks: nginx_setup.yml
 
  include_tasks: tomcat_setup.yml
  

  include_tasks: group.yml
 
  include_tasks: mysql_setup.yml

  include_tasks: git_rep.yml
 

  include_tasks: users.yml
 ``` 

## create playbook for role assignment6 i.e., assignment6.yml

```
ansible-playbook assignmet6.yml

```

## output -



![1](https://user-images.githubusercontent.com/114915047/194127614-b68d9ca5-2849-47ad-8cc1-092224bd8fab.png)



![2](https://user-images.githubusercontent.com/114915047/194127647-0fe90d29-660d-4ae5-8043-b3f5a49bf735.png)



![3](https://user-images.githubusercontent.com/114915047/194127708-28517c2c-0652-453f-b97d-bc194d6a79a0.png)



