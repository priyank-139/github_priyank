ASSIGNMENT 1

Prerequisites

1- master node - Python 3.10.6 | pip | ansible [core 2.13.3]
2- remote server - Python 3.10.6 | 
3- ssh master node to remote server 
4-Inventory file content 

[ test2 ansible_host=34.217.108.95 ansible_user=ubuntu ansible_ssh_private_key_file=/home/priyank/Downloads/ansible_key.pem ]

5- write a playbook according to the problem statement 

modules used for performoing task on the remote server 

1-apt module - install nginx and apache2 service on remote server
2-copy module - copy file /etc/logrotate.d/nginx and file /var/www to remote server 
3-systemd module - restart nginx and apache service 
4- handlers - used to restart the service 

Playbook name - assign1.yml

command to run playbook - ansible-playbook assign1.yml

Output of the plabook after deploying the service on the remote server 


