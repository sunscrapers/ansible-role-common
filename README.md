# Ansible role for common tasks

[![Build Status](https://travis-ci.org/sunscrapers/ansible-role-common.svg)](https://travis-ci.org/sunscrapers/ansible-role-common)

This role manages remote users, authorized keys and ssh keys.

Developed by [SUNSCRAPERS](http://sunscrapers.com/) with passion & patience.

## Installation

```
$ ansible-galaxy install sunscrapers.common -p roles/
```

## Customization

To customize the role you can override the default variables in the following way:

```yaml
common_users: ['app']
common_authorized_users: ['root', 'app']
common_authorized_keys: ['https://github.com/haxoza.keys']
common_ssh_private_key: "{{ lookup('file', 'files/id_rsa') }}"
common_ssh_public_key: "{{ lookup('file', 'files/id_rsa.pub') }}"
common_ssh_private_key_filename: ~/.ssh/id_rsa
common_ssh_public_key_filename: ~/.ssh/id_rsa.pub
common_ssh_keys_users: "{{ common_users }}"
common_known_hosts: []
common_ssh_known_hosts_filename: ~/.ssh/known_hosts
common_known_hosts_users: "{{ common_users }}"
```
