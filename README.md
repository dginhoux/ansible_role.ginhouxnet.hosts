ginhouxnet.hosts
=========

This ansible role populate /etc/hosts file

Requirements
------------

This ansible role will only run on identified OS defined on meta/main.yml


Role Variables
--------------

It's just two lists, one for ipv4 entries, one for ipv6 entries : 

```
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




Example Playbook
----------------



License
-------

BSD


Author Information
------------------

Dany GINHOUX
