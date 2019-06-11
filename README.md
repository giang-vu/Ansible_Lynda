# Ansible_Lynda
Create a user ansible with root privileges for automation.
Ansible bootstrap
```
#!/bin/bash
sudo yum update -y
sudo amazon-linux-extras install -y ansible2
sudo useradd ansible
sudo usermod -aG wheel ansible
sudo echo "ansible ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers
```
Hosts bootstrap
```
#!/bin/bash
sudo yum update -y
sudo useradd ansible
sudo usermod -aG wheel ansible
sudo echo "ansible ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers
sudo mkdir /home/ansible/.ssh
sudo cp /home/ec2-user/.ssh/authorized_keys /home/ansible/.ssh/authorized_keys
sudo chmod 600 /home/ansible/.ssh/authorized_keys
sudo chmod 700 /home/ansible/.ssh
sudo chown ansible:ansible /home/ansible/.ssh/authorized_keys
sudo chown ansible:ansible /home/ansible/.ssh
```
Copy private key to /home/ansible/.ssh/authorized_keys in all machines.
Configure Ansible
```
# sudo vim /etc/ansible/ansible.cfg

[default]
inventory = /home/ansible/inventory
remote_user = ansible
private_key_file = /home/ansible/private-key.pem
```
Test connection
```
# ansible all -m ping
```
