# ansible-cowrie

Ansible playbook for Cowrie (https://github.com/micheloosterhof/cowrie)

```
ansible-playbook -i inventory cowrie.yml
```

where file inventory is

```
[cowrie]
10.0.0.1
10.0.0.2
10.0.0.3
...

[all:vars]
ansible_ssh_common_args='-F ./ssh_config'
```

and `ssh_config` is

```
Host *
  IdentityFile          ~/.ssh/my_private_key
  User                  ec2-user
  StrictHostKeyChecking no
```
