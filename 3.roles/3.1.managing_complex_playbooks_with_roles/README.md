```
# ansible-playbook -i inventory tasks.yml -e user_name=giangvu -e user_state=present

# ansible-playbook -i inventory tasks.yml -e user_name=giangvu -e user_state=absent
```
The last task will fail because the user is already removed.
