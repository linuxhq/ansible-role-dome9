# ansible-role-dome9

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-dome9.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-dome9)

RHEL/CentOS - Dome9 RPM repository

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    dome9_pkg: dome9
    dome9_ver: 0.1.0
    dome9_rel: 1
    dome9_arch: noarch
    dome9_baseurl: "http://repository.dome9.com/centos/5/{{ dome9_arch }}"
    dome9_release: "{{ dome9_pkg }}-{{ dome9_ver }}-{{ dome9_rel }}"
    dome9_fetch: "{{ dome9_baseurl }}/{{ dome9_release }}.{{ dome9_arch }}.rpm"
    dome9_repos:
      Dome9: False

All repositories are disabled by default.

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.dome9
          dome9_repos:
            Dome9: True

## License

GPLv3

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).
