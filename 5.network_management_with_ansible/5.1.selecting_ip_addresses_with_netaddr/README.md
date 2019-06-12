Install the ipaddr filter tool.
```
# sudo yum install -y python-netaddr
```
Run ansible-playbook.
```
# ansible-playbook tasks.yml

ok: [localhost] => {
    "msg": "A good format of IP address and prefix length is 10.10.0.1/27"
}

ok: [localhost] => {
    "msg": "The next IP address is 10.10.0.2/27"
}
```
