Confluence
==========

[![Build Status](https://travis-ci.org/kbrebanov/ansible-confluence.svg?branch=master)](https://travis-ci.org/kbrebanov/ansible-confluence)

Installs Confluence.

Requirements
------------

This role requires Ansible 1.9 or higher.

Role Variables
--------------

| Name                          | Default                                                          | Description                      |
|-------------------------------|------------------------------------------------------------------|----------------------------------|
| confluence_version            | 5.9.6                                                            | Version of Confluence to install |
| confluence_archive_sha256sum  | bff3b56a89ef277a03c6f9ff863194f1fe2b43ed5d8c5d92f319d90b55709469 | SHA 256 checksum of archive      |
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
