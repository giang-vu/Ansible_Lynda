Edit the inventory file to run all tasks as root because we connect as the "ansible" user.
```
web1 ansible_ssh_host=172.31.1.20 ansible_user=ansible ansible_become=yes
web2 ansible_ssh_host=172.31.1.30 ansible_user=ansible ansible_become=yes
db1 ansible_ssh_host=172.31.1.40 ansible_user=ansible ansible_become=yes
db2 ansible_ssh_host=172.31.1.50 ansible_user=ansible ansible_become=yes
```
Run ansible-playbook
```
# ansible-playbook tasks.yml -e file_state=touch -e pkg_state=latest

# ansible-playbook tasks.yml -e file_state=absent -e pkg_state=absent
```
