# ASSIGNMENT 5 

## Prerequisites 

1- master node - Python 3.10.6 | pip | ansible [core 2.13.3]
2- remote server - Python 3.10.6 | 
3- ssh master node to remote servers 
4-Inventory file content

```
[amazon_debian_centos]
test2 ansible_host=34.217.108.95 ansible_user=ubuntu ansible_ssh_private_key_file=/home/priyank/Downloads/ansible_key.pem
test1 ansible_host=35.91.73.204 ansible_user=ec2-user ansible_ssh_private_key_file=/home/priyank/Downloads/ansible_key.pem
test3 ansible_host=54.218.236.235 ansible_user=ec2-user ansible_ssh_private_key_file=/home/priyank/Downloads/ansible_key.pem

```
## Steps to create role for hashi corp vault installation

1-ansible-galaxy init hashi_corp_vault

2-cd hashi_corp_vault/

3-cd tasks/

4-vim hashi_corp_vault_centios.yml | hashi_corp_vault_debian.yml | hashi_corp_vault_linux.yml | main.yml

5- vim main.yml

 ```
  include_tasks: hashi_corp_vault_debian.yml
  include_tasks: hashi_corp_vault_linux.yml
  include_tasks: hashi_corp_vault_centos.yml
 
 ```

## Modules used in hashi_corp_vault_debian.yml

1-apt for installing gpg  and vault for debian distribution
```
GPG, is a command line tool with features for easy integration with other applications
```
2-shell module for Add the HashiCorp GPG key | Verify the key's fingerprint  | Add the official HashiCorp Linux repository.

3-yum module installing yum-utils and vault for centos and amazon linux distribution
```
yum-utils is a collection of tools and programs for managing yum repositories, installing debug packages, source packages, extended information from repositories and administration.
```
## playbook for role hashi_corp_vault.yml

command for deploy HashiCorp vault on debian , amazon linux and centos distributions
```
ansible-playbook hashi_corp_vault.yml
```
## Output of the plabook after deploying the service on the remote server



![1](https://user-images.githubusercontent.com/114915047/194117285-b68e78a5-569e-44fa-82fd-af6e0f2e5ce9.png)



![2](https://user-images.githubusercontent.com/114915047/194117313-9da4396d-f801-49a8-8c53-ce5b471aed84.png)



