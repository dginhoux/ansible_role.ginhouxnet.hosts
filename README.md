Ansible Role : dginhoux.hosts
=========

This ansible role populate `/etc/hosts` file

Requirements
------------

This role require a supported platform defined in `meta/main.yml`.
It will skip node with unsupported platform ; this behaviour can be bypassed by settings this variable `asserts_bypass=True`.


Role Variables
--------------

Two dicts, one for ipv4 entries, one for ipv6 entries : 

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


Dependencies
------------

none


Example Playbook
----------------



License
-------

BSD


Author Information
------------------

https://github.com/dginhoux/
