jamulus-setup
=============

Sets up a working Jamulus server, assumes `firewalld` as firewall

Requirements
------------
- `firewalld` used as system firewall

Role Variables
--------------

vars/main.yml
* `jamulus_archive_path`: path to the jamulus archive file, by default indicates file in the `files` directory

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

