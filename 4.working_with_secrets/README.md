Encrypt the password_file with Ansible Vault password.
```
# ansible-vault encrypt password_file
```
Edit the encrypted password_file.
```
# ansible-vault edit password_file
```
Decrypt when run ansible-playbook.
```
# ansible-playbook -i inventory task.yml --ask-vault-pass
```
