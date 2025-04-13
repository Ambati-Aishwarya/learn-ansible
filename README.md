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

$ ansible -i inventoryFileName all -e ansible_user=ec2-user -e ansible_password=DevOps321 -m ansible.builtin.shell -a uptime
ansible -i inventoryFileName all -e ansible_user=ec2-user -e ansible_password=DevOps321 -m ansible.builtin.ping

Ansible is all about modules (from version 2.8, we are referring them as collections )

