### Auto deploy and run gitea in remote server witch ansible.

## How To Use:

Step one: install Ansible `pip install ansible`

Step two: install docker plugin with ansible `ansible-galaxy install nickjj.docker` 

Step three: clone this repo `git clone <repo>`

Step  foo: configure

######host.yml
Config your ssh client. Example: 
```
Host foo
  Hostname ...
  IdentyfiFile ...
  user root
``` 
Add your server in `host.yml`:
```yaml
all:
  hosts:
    foo:
```

Step five: start ansible `ansible-playbook -i host.yml playbook.yml`