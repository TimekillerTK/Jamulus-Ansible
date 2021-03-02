unattended-upgrades
===================

Sets up unattended upgrades with mail notification

Requirements
------------

- `smtp-setup` ansible role

Role Variables
--------------

vars/main.yml
* `notify_email`: e-mail to send unattended upgrade notifications to

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

https://github.com/TimekillerTK/