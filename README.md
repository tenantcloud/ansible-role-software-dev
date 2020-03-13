tenantcloud.software_dev
=========

Ansible role for install dev software. This role include install:

  - nginx
  - php@7.1
  - mysql-connector-c
  - mysql-client
  - imagemagick
  - dnsmasq
  - awscli
  - byobu
  - sequel-pro-nightly
  - phpstorm
  - libreoffice
  - docker
  - docker-compose
  - ansible
  - java@8
  - node@10
  - supervisor

Requirements
------------

Install tenantcloud.software_common

Role Variables
--------------

work_user: "user" os username
node_version:
nvm_version:
nvm_node_version: 
java_version:
java_build_version:
java_release:
java_name:
java_url:
aws_access_key_id:
aws_secret_access_key:
aws_default_region:

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
        aws_access_key_id:
        aws_secret_access_key:
        aws_default_region:
        nvm_node_version: 
      roles:
        - tenantcloud.software_dev

License
-------

BSD

Author Information
------------------

TenantCloud DevOps Team
