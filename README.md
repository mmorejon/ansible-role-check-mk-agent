check_mk_agent
=========

[![Ansible Role](https://img.shields.io/badge/ansible--galaxy-mmorejon.check--mk--agent-blue.svg)](https://galaxy.ansible.com/mmorejon/check-mk-agent)
[![Build Status](https://travis-ci.org/mmorejon/ansible-role-check-mk-agent.svg?branch=master)](https://travis-ci.org/mmorejon/ansible-role-check-mk-agent)

Ansible role for installing Check MK Agent.

Requirements
------------

Currently working with Debian/Ubuntu.

Role Variables
--------------

### url

The url is used to download the agent for Check MK into client machine. The system Check MK always have an internal link to the agent that use. This link can be found inside Monitoring Agents section.

The `url` doesn't containg the package name.

### dest

The physical path where we are going to download and after intall the agent.

### package

The agent package name.

Dependencies
------------

No.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      become: true
      roles:
         - { role: check-mk-agent, when: ansible_distribution_release == 'trusty' }

License
-------

GPLv2

Author Information
------------------

Created by Manuel Morejón.