Confluence
==========

[![Ansible Role](https://img.shields.io/ansible/role/3979.svg)](https://galaxy.ansible.com/list#/roles/3979)

Installs Confluence.

Requirements
------------

This role requires Ansible 1.6 or higher.

Role Variables
--------------

| Name                          | Default                                                          | Description                      |
|-------------------------------|------------------------------------------------------------------|----------------------------------|
| confluence_version            | 5.8.16                                                           | Version of Confluence to install |
| confluence_archive_sha256sum  | 9ccf96838a7b00439b62f4a3f1377cd32a83b3169f5e4ee7bd6c8a244b1ea59b | SHA 256 checksum of archive      |
| confluence_jvm_minimum_memory | 1024m                                                            | Confluence JVM minimum memory    |
| confluence_jvm_maximum_memory | 1024m                                                            | Confluence JVM maximum memory    |

Dependencies
------------

- kbrebanov.java (Java 8)

Example Playbook
----------------

Install Confluence
```
- hosts: all
  roles:
    - { role: kbrebanov.confluence }
```

Install Confluence specifying version
```
- hosts: all
  roles:
    - { role: kbrebanov.confluence, confluence_version: 5.7.3 confluence_archive_sha256sum: 81bc02e8557a108731c41723162bbbfc42c7023d970fad347156497c9586ed42 }
```

Install Confluence specifying Confluence JVM memory
```
- hosts: all
  roles:
    - { role: kbrebanov.confluence, confluence_jvm_minimum_memory: 3000m, confluence_jvm_maximum_memory: 4096m }
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov
