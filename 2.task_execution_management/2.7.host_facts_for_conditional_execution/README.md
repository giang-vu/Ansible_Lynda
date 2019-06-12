From web1, asking variable hostvars on web2
```
ansible -m debug -a "var=hostvars['web2']" web1
```
