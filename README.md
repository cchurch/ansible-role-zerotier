[![Build Status](http://img.shields.io/travis/cchurch/ansible-role-zerotier.svg)](https://travis-ci.org/cchurch/ansible-role-zerotier)
[![Galaxy](http://img.shields.io/badge/galaxy-cchurch.zerotier-blue.svg)](https://galaxy.ansible.com/cchurch/zerotier/)

ZeroTier
========

Install the [ZeroTier](https://zerotier.com/) network client on the target
system. Requires Ansible 2.4 or later.

Requirements
------------

Assumes the role is being run with become capabilities on the target system.

Role Variables
--------------

The following variables may be defined to customize this role:

- `zerotier_state`: One of `present`, `latest` or `absent`. Indicates whether to
  install, upgrade or remove ZeroTier. Default is `present`.
- `zerotier_network`: ZeroTier network ID to join (16 hex digits).
- `zerotier_network_state`: One of `present` or `absent`. Indicates whether to
  join or leave network. Default is `present`.

Example Playbook
----------------

The following example playbook installs the ZeroTier client and joins a network:

    - name: install zerotier
      hosts: all
      roles:
        - name: cchurch.zerotier
          vars:
            zerotier_state: present
            zerotier_network: "deadbeefcafe1234"

License
-------

BSD

Author Information
------------------

Chris Church ([cchurch](https://github.com/cchurch))
