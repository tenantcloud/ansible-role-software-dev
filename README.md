tenantcloud.ansible_role_software_dev
=========

Ansible role for install dev software. This role include install:

  - nginx
  - redis
  - mysql@5.7
  - rtmpdump
  - libssh2
  - php@7.1
  - python@2
  - mysql-connector-c
  - mysql-client
  - imagemagick
  - dnsmasq
  - awscli
  - byobu
  - sequel-pro-nightly
  - phpstorm
  - libreoffice

Requirements
------------

Role Variables
--------------

work_user: "user" os username

Dependencies
------------

  - homebrew
  - python@3
  - ansible

Example Playbook
----------------

    - hosts: localhost
      become: no
      vars:
        work_user: "user"
      roles:
        - tenantcloud.ansible_role_software_dev

License
-------

BSD

Author Information
------------------

TenantCloud DevOps Team
