# Ansible Role: Install sury

[![Build Status](https://travis-ci.org/tschifftner/ansible-role-sury.svg?branch=master)](https://travis-ci.org/tschifftner/ansible-role-sury)

Installs sury repositories on Debian and ppa:ondrej/php on Ubuntu linux servers. More information can be found on [deb.sury.org](https://deb.sury.org/)

## Requirements

ansible 2.1+

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```
sury_install_repositories: Yes

sury_apt_key: 'http://www.sury.org/sury.gpg'

sury_apt_packages:
 - apt-transport-https

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

 - Debian 9 (Stretch)
 - Debian 8 (Jessie)
 - Ubuntu 18.04 (Bionic Beaver)

## Required ansible version

Ansible 2.5+

## License

[MIT License](http://choosealicense.com/licenses/mit/)

## Author Information

 - [Tobias Schifftner](https://twitter.com/tschifftner), [ambimax® GmbH](https://www.ambimax.de)