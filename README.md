tenantcloud.software_dev
=========

Ansible role for install dev software. This role include install:

  - nginx-full
  - php
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
  - vault
  - bash
  - grep
  - mc
  - xcode

Requirements
------------

Install tenantcloud.software_common

Role Variables
--------------

ansible_user: "user" os username
node_version:
nvm_node_version: 
java_version:
java_build_version:
java_release:
java_name:
java_url:
aws_access_key_id:
aws_secret_access_key:
aws_default_region:
pm2:

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
        ansible_user: "user"
        aws_access_key_id:
        aws_secret_access_key:
        aws_default_region:
        nvm_node_version: 
        pm2: 'true'
        mas_installed_apps:  
          - { id: 497799835, name: "Xcode" }
      roles:
        - geerlingguy.mas
        - tenantcloud.software_dev
      environment:
        PATH: "/usr/local/bin:{{ ansible_env.PATH }}"

License
-------

BSD

Author Information
------------------

TenantCloud DevOps Team
