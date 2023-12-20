# ROLE dginhoux.hosts



## DESCRIPTION

This ansible role populate `/etc/hosts` file.




## REQUIREMENTS

#### SUPPORTED PLATFORMS

| Platform | Versions |
|----------|----------|
| Debian | all |
| EL | all |
| Fedora | all |
| Ubuntu | all |

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
- name: Playbook
  hosts: all
  roles:
    - name: start role dginhoux.hosts
      ansible.builtin.include_role:
        name: dginhoux.hosts
```


## VARIABLES

#### DEFAULT VARIABLES

Defaults variables defined in `defaults/main.yml` : 

```yaml
hosts_ipv4_list:
  - ip: 192.168.175.50
    fqdn: gluster.infra.ginhoux.net
    hostname: gluster
  - ip: 192.168.175.50
    fqdn: vip-gluster.infra.ginhoux.net
    hostname: vip-gluster
hosts_ipv4_list_host: []
hosts_ipv4_list_group: []

hosts_ipv6_list: []
hosts_ipv6_list_host: []
hosts_ipv6_list_group: []
```

NOTE : Theses 6 lists are merged. <br />
You can use the `_host` and `_group` lists to specify per host and/or per group content.



#### DEFAULT OS SPECIFIC VARIABLES

Those variables files are located in `vars/*.yml` are used to handle OS differences.<br />
One of theses is loaded dynamically during role runtime using the `include_vars` module and set OS specifics variable's.

`NOT USED BY THIS ROLE`


## AUTHOR

Dany GINHOUX - https://github.com/dginhoux



## LICENSE

MIT
