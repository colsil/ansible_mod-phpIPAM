Ansible Modules - phpIPAM
=========================

Requirements
=========================
ansible >= 2.7

Installation
=========================

Installing with ansible galaxy:

```ansible-galaxy install git+https://github.com/rcanderson23/ansible_mod-phpIPAM.git```

To manually install, copy the library and module_utils directories to your ansible directory.

Example Plays
=========================

phpipam_freeip
-------------------------

```yaml
  phpipam_freeip:
    username: admin
    password: secret
    url: 'http://ipam.domain.tld/api/app/'
    subnet: '192.168.10.0/24'
    section: ansible-section
    description: 'Optional description'
  register: new_ip
```

phpipam_section
------------------------

```yaml
  phpipam_section:
    username: admin
    password: secret
    url: 'http://ipam.domain.tld/api/app/'
    section: ansible-section
    master_section: 'root'
    description: 'Optional description'
    state: present
```

phpipam_subnet
-----------------------

```yaml
  phpipam_subnet:
    username: admin
    password: secret
    url: 'http://ipam.domain.tld/api/app/'
    subnet: '192.168.10.0/24'
    section: ansible-section
    vlan: '100'
    description: 'Optional description'
    state: present
```

phpipam_vlan
----------------------

```yaml
  phpipam_vlan:
    username: admin
    password: secret
    url: 'http://ipam.domain.tld/api/app/'
    vlan: '100'
    name: 'required name'
    description: 'Optional description'
    domainid: "1" # optional l2domain id, default: 1
    state: present
```
