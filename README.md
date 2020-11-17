disable-thp
===========

This role disables Transparent Huge Pages on Ubuntu server.

Role Variables
--------------

- `disable_thp_init_system`: OS init system (upstart or systemd). (default 'systemd')
- `disable_thp_state`: Desired daemon state after role execution (default: 'started')
- `disable_thp_before_service`: If set, disable THP before this service (Ex: 'mongod')

Example Playbook
----------------

    - hosts: servers
      roles:
        - {
          role: disable_thp,
          disable_thp_before_service: 'mongod'
        }

License
-------

MIT

[![Build Status](https://travis-ci.org/GekoCloud/ansible-role-disable-thp.svg?branch=master)](https://travis-ci.org/GekoCloud/ansible-role-disable-thp)
