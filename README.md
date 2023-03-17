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

With default variables, this role dont change anything on the system. You need to set the config variables like in the exemple in order to start configuration.

## Examples

        ---
        - hosts: system_grub
          become: true
          become_method: sudo
          gather_facts: true
          roles:
            - role: ansible-system_grub
          vars: 
            grub_options:
              - name: GRUB_DISTRIBUTOR
                value: "{{ ansible_distribution }}"
              - name: GRUB_TIMEOUT
                value: 4
              - name: GRUB_CMDLINE_LINUX
                value: "ipv6.disable=1 apparmor=1 security=apparmor"
            grub_add_filed:
              - file: 01_passwd
                value: |
                  set superusers='root' password_pbkdf2 root grub.pbkdf2.sha512.10000.7C6DC0B6EA14D77D91C260C7410EDD5DF807295BE94284911EEB9C44BBAC0DD86B5606CC8C89BCB3FF4D91F39CDBF091B7C8923372B95BABB7170507D7AED9E6.D6F0E45D0B978919786C1BBAC888E8E38EEE28B454BCC93008D314974F7788C8E4C614C090862CEA4AFA841493131BDC8CD3642E8034F2C542FD87ADFB574797
              - file: 10_linux
                regex: "CLASS="
                value: "--unrestricted"



## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.

## Author Information

- [Philippe LEAL](https://github.com/lotusnoir)
