Create a role name "createUser" to keep a set of default variables which are less likely to change but actually easier to override.
```
# ansible-galaxy init createUser
```
Move the preconfig files to the createUser directory.
```
# mv create_user.yml createUser/tasks/main.yml

# mv template.j2 createUser/templates/bashrc.j2
```
Edit the createUser/defaults/main.yml with default values.
```
# vim createUser/defaults/main.yml

user_state: present
```
Run ansible-playbook.
```
# ansible-playbook -i inventory tasks.yml

# ansible-playbook -i inventory tasks.yml -e user_state=absent
```
