Confluence
==========

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

1) Install Confluence

    - hosts: all
      roles:
         - { role: confluence }

License
-------

BSD

Author Information
------------------

Kevin Brebanov
