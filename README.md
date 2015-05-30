Confluence
==========

[![Ansible Galaxy](https://img.shields.io/badge/galaxy-kbrebanov.confluence-660198.svg)](https://galaxy.ansible.com/list#/roles/3979)

Installs Confluence.

Requirements
------------

This role requires Ansible 1.6 or higher.

Role Variables
--------------

| Name                          | Default                                                          | Description                      |
|-------------------------------|------------------------------------------------------------------|----------------------------------|
| confluence_version            | 5.7.4                                                            | Version of Confluence to install |
| confluence_archive_sha256sum  | 3f84676dabec1d4a9bac6a2676f600cdfee2088b8b9693a4fac88324fa279db2 | SHA 256 checksum of archive      |
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
