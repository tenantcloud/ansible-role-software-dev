
![Lint Ansible Roles](https://github.com/tenantcloud/ansible-role-software-dev/workflows/Lint%20Ansible%20Roles/badge.svg?branch-master)

tenantcloud.software_dev
=========

Ansible role for install dev software. This role include install:

  - nginx
  - imagemagick
  - awscli
  - byobu
  - sequel-pro-nightly
  - phpstorm
  - libreoffice
  - docker
  - docker-compose
  - ansible
  - java@8
  - vault
  - bash
  - grep
  - mc
  - xcode
  - jq

Requirements
------------

Install tenantcloud.software_common

Role Variables
--------------

ansible_user: "user" os username
java_version:
java_build_version:
java_release:
java_name:
java_url:

Dependencies
------------

  - homebrew
  - python@3
  - ansible

Example Playbook
----------------

```yaml
- hosts: localhost
  become: no
  vars:
    ansible_user: "user"
    mas_installed_apps:  
      - { id: 497799835, name: "Xcode" }
  roles:
    - geerlingguy.mas
    - tenantcloud.software_dev
  environment:
    PATH: "/usr/local/bin:{{ ansible_env.PATH }}"
```

License
-------

BSD

Author Information
------------------

TenantCloud DevOps Team
