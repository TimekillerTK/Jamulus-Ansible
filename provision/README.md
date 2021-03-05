provision
=========

For provisioning new Ansible Hosts. Created mostly for myself in order to set up LinuxAcademy cloud servers with public keys from multiple computers for easy accessibility.

End result is one or more Ansible Managed hosts, ready for you to run ansible commands against & SSH into using a previously generated SSH keypair.

Requirements
------------
- `sshpass` package (for password authentication with Ansible)


Role Variables
--------------

vars/default.yml
* `raw_text`: for installing Python 3 on Ubuntu/CentOS hosts, best leave it at default, but modify in `var/default.yml` if needed 
* `pubkeys`: path to public keys to be added to the user ansible is going to be ssh'ing as, best leave it at default and insert your public keys in to the `files/` directory

Dependencies
------------

None.

Example Playbook
----------------

Make sure to include `gather_facts: no` otherwise the run of `ansible_playbook` may fail:

    - name: Provision new Ansible host
      gather_facts: no
      hosts: raw
      roles:
      - provision

Then run your playbook with:
* `ansible-playbook yourplaybook.yml -u username --ask-pass --ask-become-pass`

Enter your SSH username and password. **Make sure the username is root or has sudo privileges!**

License
-------

BSD

Author Information
------------------

https://github.com/TimekillerTK/
