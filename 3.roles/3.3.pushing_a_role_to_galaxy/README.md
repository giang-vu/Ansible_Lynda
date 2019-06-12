- Edit your personal information in README.md and meta/main.yml under the role directory.
- Push your role directory to GitHub.
- Login to Ansible Galaxy with GitHub account.
```
# ansible-galaxy login
```
- Import the role from GitHub to Ansible Galaxy.
```
# ansible-galaxy import [author name] [role name]
Ex:
# ansible-galaxy import giangvu createUser
```
- Search the role from Ansible Galaxy.
```
# ansible-galaxy search giangvu.createUser
```
- Download the role to the working directory.
```
# ansible-galaxy install giangvu.createUser -p ./
```
- Change the role_path in /etc/ansible/ansible.cfg if you want to have centralized store of roles.
```
# vim /etc/ansible/ansible.cfg

roles_path = /etc/ansible/roles
```
