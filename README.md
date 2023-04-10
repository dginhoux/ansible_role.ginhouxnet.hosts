# ROLE dginhoux.hosts



## DESCRIPTION

This ansible role populate `/etc/hosts` file.




## REQUIREMENTS

#### SUPPORTED PLATFORMS

This role require a supported platform.<br />
It will skip node with unsupported platform to avoid any compatibility problem.<br />
This behaviour can be bypassed by settings the following variable `asserts_bypass=True`.

| Platform | Versions |
|----------|----------|
| Debian | buster, bullseye |
| Fedora | 33, 34, 35, 36, 37 |
| EL | 7, 8 |

#### ANSIBLE VERSION

Ansible >= 2.13

#### DEPENDENCIES

None.



## INSTALLATION

#### ANSIBLE GALAXY

```shell
ansible-galaxy install dginhoux.hosts
```
#### GIT

```shell
git clone https://github.com/dginhoux/ansible_role.hosts dginhoux.hosts
```


## USAGE

#### EXAMPLE PLAYBOOK

```yaml
- hosts: all
  roles:
    - name: start role dginhoux.hosts
      ansible.builtin.include_role:
        name: dginhoux.hosts
```


## VARIABLES

#### DEFAULT VARIABLES

Defaults variables defined in `defaults/main.yml` : 

```yaml
hosts_ipv4:
  - ip: 192.168.175.50
    fqdn: gluster.infra.ginhoux.net
    hostname: gluster
  - ip: 192.168.175.50
    fqdn: vip-gluster.infra.ginhoux.net
    hostname: vip-gluster

hosts_ipv6: []
```

#### DEFAULT OS SPECIFIC VARIABLES

Those variables files are located in `vars/*.yml` are used to handle OS differences.<br />
One of theses is loaded dynamically during role runtime using the `include_vars` module and set OS specifics variable's.

`NOT USED BY THIS ROLE`


## AUTHOR

Dany GINHOUX - https://github.com/dginhoux



## LICENSE

MIT
