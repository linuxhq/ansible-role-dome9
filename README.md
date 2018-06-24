# ansible-role-dome9

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-dome9.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-dome9)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-dome9-blue.svg?style=flat)](https://galaxy.ansible.com/linuxhq/dome9)
[![License](https://img.shields.io/badge/license-GPLv3-brightgreen.svg?style=flat)](COPYING)

RHEL/CentOS - Dome9 RPM repository

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    dome9_arch: noarch
    dome9_baseurl: "https://s3.amazonaws.com/repository.dome9.com/centos/5/{{ dome9_arch }}"
    dome9_disablerepo: []
    dome9_enablerepo: []
    dome9_fetch: "{{ dome9_baseurl }}/{{ dome9_release }}.{{ dome9_arch }}.rpm"
    dome9_packages: []
    dome9_pkg: dome9
    dome9_rel: 1
    dome9_release: "{{ dome9_pkg }}-{{ dome9_ver }}-{{ dome9_rel }}"
    dome9_repository_dome9: false
    dome9_ver: 0.1.0

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.dome9
          dome9_repository_dome9: true

## License

Copyright (C) 2018 Taylor Kimball <tkimball@linuxhq.org>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
