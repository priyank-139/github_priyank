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
  when: ansible_facts['distribution']=="Debian"

  include_tasks: tomcat_setup.yml
  when: ansible_facts['distribution']=="Debian"

  include_tasks: group.yml
  when: ansible_facts['distribution']=="Debian"
  when: ansible_facts['distribution']=="Amazon"

  include_tasks: mysql_setup.yml

  include_tasks: git_rep.yml
  when: ansible_facts['distribution']=="Debian"
  when: ansible_facts['distribution']=="Amazon"

  include_tasks: users.yml
  when: ansible_facts['distribution']=="Debian"
  when: ansible_facts['distribution']=="Amazon"
```

## create playbook for role assignment6 i.e., assignment6.yml

```
ansible-playbook assignmet6.yml

```

## output -

<img src=/Pictures/Screenshots/assignmet6_ansible output/1.png>

<img src=/Pictures/Screenshots/assignmet6_ansible output/2.png>

<img src=/Pictures/Screenshots/assignmet6_ansible output/3.png>




