ASSIGNMENT 3

Prerequisites

1- master node - Python 3.10.6 | pip | ansible [core 2.13.3]
2- remote server - Python 3.10.6 | 
3- ssh master node to remote server 
4-Inventory file content 

[ test2 ansible_host=34.217.108.95 ansible_user=ubuntu ansible_ssh_private_key_file=/home/priyank/Downloads/ansible_key.pem ]

5- write a playbook according to the problem statement 

modules used for performoing task on the remote server

1-apt module -install java 11 mysql and maven
2-get_url -Downloading tomcat 7 tar.gz file
3-unarchive -extracting tomcat file
4- shell module -starting tomcat
5- git module to clone Spring3HibernateApp repo
playbook name -assignment_3.yml

command to run playbook - ansible-playbook assignment_3.yml

Output of the plabook after deploying the service on the remote server
 

