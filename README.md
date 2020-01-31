tenantcloud.ansible_role_software_dev
=========

Ansible role for install dev software. This role include install:

  - nginx
  - redis
  - mysql@5.7
  - rtmpdump
  - libssh2
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

Requirements
------------

Install tenantcloud.ansible_role_software_common

Role Variables
--------------

work_user: "user" os username
work_dir: "work" os user work directory

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
        ansible_python_interpreter: "/usr/local/bin/python3"
        node_version: "v10"
        nvm_version: "v0.35.2"
        java_version: "8"
        java_build_version: "b10"
        java_release: "212"
        java_name: "jdk-8u212-macosx-x64"
        java_url: "https://github.com/frekele/oracle-java/releases/download/{{ java_version }}u{{ java_release }}-{{ java_build_version }}/{{ java_name }}.dmg"
        aws_access_key_id: ""
        aws_secret_access_key: ""
        aws_default_region: ""
      roles:
        - tenantcloud.ansible_role_software_dev

License
-------

BSD

Author Information
------------------

TenantCloud DevOps Team
