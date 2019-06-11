```
# ansible-playbook -i inventory tasks.yml -e file_state=touch --start-at-task='the second task'

# ansible-playbook -i inventory tasks.yml -e file_state=absent --start-at-task='the second task'
```
