Linux Hardening Role
=========

This role is designed to test the security posture of Linux OS Servers and harden them where needed.  DISA publicly available STIG criteria as of 2014-06-11 for RedHat 5/6 are the foundation of this role and have been modified as needed to work on the other operating systems.

You are **STRONGLY** encouraged to run this against a test server first.  There are a couple of changes to ipv4/v6 settings that have been known to cause issues.  If you're really concerned you can check the description for each task and adjust for your needs.

See [DISA STIG Guidelines](https://iase.disa.mil/stigs/Pages/index.aspx) for more information

Requirements
------------

This role is currently specific to Linux OS and mostly on RedHat/CentOS with some support for Ubuntu.  

Role Variables
--------------

There are several variables to consider since this role looks to change insecure or default settings to something more secure.  See the options in the /vars

Dependencies
------------

Not applicable.

Example Playbook
----------------

```
- name: Run the hardening role
  hosts: your_hosts
  become: true
  become_user: root
  roles:
    - { role: hardenlinux }

```

License
-------

GPL v3

Author Information
------------------

Authored by Kevin White
