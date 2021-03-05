
![Lint Ansible Roles](https://github.com/tenantcloud/ansible-role-software-dev/workflows/Lint%20Ansible%20Roles/badge.svg?branch-master)

tenantcloud.software_dev
=========

Ansible role for install and remove (optional) dev software. This role include install:

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
  - nvm  
  - node@12
  - vault
  - bash
  - grep
  - mc
  - xcode
  - jq
  - yq  
  - git-lfs

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
    pm2: 'false'
    mas_installed_apps:  
      - { id: 497799835, name: "Xcode" }
    homebrew_remove:
      - package: ""
    homebrew_cask_remove:
      - package: ""
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
