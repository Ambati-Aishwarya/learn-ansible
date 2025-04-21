# learn-ansible

dnf install ansible(offers ansible core which is ansible-7)
latest and greatest ansible is available here:(11.4.0)
https://pypi.org/project/ansible/

to install Ansible:


$ sudo pip3.11 install Ansible

what is inventory?
inventory is a file that has the list of all the vm ip's that need to be managed by ansible
all is default group on this file that includes everything on the file.

running ansible commands manually:

if we execute the commands manually, we can execute one command at a time

$ ansible -i inv all -e ansible_user=ec2-user -e ansible_password=DevOps321 -m ansible.builtin.shell -a uptime
ansible -i inv all -e ansible_user=ec2-user -e ansible_password=DevOps321 -m ansible.builtin.ping

Ansible is all about modules (from version 2.8, we are referring them as collections )
if we go with the manual way of running these commands we can run one command at a time

in our case we need to unstall ngnix start the service and download the package
 ansible -i inventoryFileName all -e ansible_user=ec2-user -e ansible_password=DevOps321 -m ansible.builtin.package ngnix

 ansible -i inventoryFileName all -e ansible_user=ec2-user -e ansible_password=DevOps321 -m ansible.builtin.systemd_service ngnix

 nsible -i inventoryFileName all -e ansible_user=ec2-user -e ansible_password=DevOps321 -m ansible.builtin.grt_url ngnix http://syxzz/d

 running commands manually is not a great way and not a right approach to handle.

 the right approach to handle ansible is using playbooks(ansible scripts)

 to do automation using ansible we achieve it using PLAYBOOKS. Playbooks are written using YAML language
 learning yaml is very easy
 YAML is all about 
   
   . Dictionary: a key with single value is referred as Dictionary
     a=10
     .lists: a key with multiple value is referred as list
     courses:
          - python
          - jsvs
          - nodejs

 in ansible what is aplaybook?
 a playbook is nothing but list of plays 
 a play is nothing but list of tasks
 a task is nothing but list of actions

 how to run a ansible playbook ?
 $ ansible-playbook -i inv -e ansible-user=ec2-user -e ansible-password=DevOps321 playBookname.yml


