# ansible-system_grub

## Description

[![Galaxy Role](https://img.shields.io/badge/galaxy-system_grub-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/system_grub)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-system_grub.svg)](https://github.com/lotusnoir/ansible-system_grub/releases/latest)
[![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-system_grub?color=orange&style=flat)](https://galaxy.ansible.com/lotusnoir/system_grub)
[![downloads](https://img.shields.io/ansible/role/d/)](https://galaxy.ansible.com/lotusnoir/system_grub)
[![Ansible Quality Score](https://img.shields.io/ansible/quality/)](https://galaxy.ansible.com/lotusnoir/system_grub)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)

Configures grub options

## Requirements

none

## Role variables

See [variables](/defaults/main.yml) for more details.

## Examples

        ---
        - hosts: system_grub
          become: true
          become_method: sudo
          gather_facts: true
          roles:
            - role: ansible-system_grub


## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.

## Author Information

- [Philippe LEAL](https://github.com/lotusnoir)
