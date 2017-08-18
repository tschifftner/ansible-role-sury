# Ansible Role: Install sury

[![Build Status](https://travis-ci.org/tschifftner/ansible-role-sury.svg)](https://travis-ci.org/tschifftner/ansible-role-sury)

Installs sury from source on Debian/Ubuntu linux servers.

## Requirements

ansible 1.8+

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```
sury_install_repositories: Yes

sury_apt_key: 'http://www.sury.org/sury.gpg'

sury_apt_repositories:
 - 'deb http://packages.sury.org {{ ansible_distribution_release }} all'
 - 'deb-src http://packages.sury.org {{ ansible_distribution_release }} all'
```

## Dependencies

None.

## Installation

```
$ ansible-galaxy install tschifftner.sury
```

## Example Playbook

    - hosts: server
      roles:
        - { role: tschifftner.sury }

## Supported OS
Ansible          | Debian Jessie    | Ubuntu 14.04*
:--------------: | :--------------: | :-------------:
2.1              | Yes              | Yes
2.2              | Yes              | Yes
2.3              | Yes              | Yes

*) The packages from Dotdeb should work on Ubuntu, but no additional support will be provided.

## License

[MIT License](http://choosealicense.com/licenses/mit/)

## Author Information

 - [Tobias Schifftner](https://twitter.com/tschifftner), [ambimax® GmbH](https://www.ambimax.de)