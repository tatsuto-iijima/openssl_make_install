openssl_make_install
=========

[![Build Status](https://www.travis-ci.com/tatsuto-iijima/openssl_make_install.svg?branch=main)](https://www.travis-ci.com/tatsuto-iijima/openssl_make_install)

Ansible Role to install OpenSSL with make.

Requirements
------------

The supported Ansible version are as follows:

- 2.10

The OpenSSL versions that can be installed with this Role are as follows:

- 1.1.1

The supported platforms are as follows:

- CentOS 7

Role Variables
--------------

See [defaults/main.yml](./defaults/main.yml).
See [vars/main.yml](./vars/main.yml).

Dependencies
------------

Nothing.

Example Playbook
----------------

An example of using this role is as follows:

    - hosts: servers
      roles:
        - role: tatsuto_iijima.openssl_make_install
          tiomi_openssl_install_version: 1.1.1h
          tiomi_openssl_prefix: /usr/local/openssl
          tiomi_openssl_config_option:
            - -fPIC
            - shared
            - "--prefix={{ tiomi_openssl_prefix }}"

License
-------

MIT

Author Information
------------------

https://github.com/tatsuto-iijima
