# Jamulus-Ansible
Set of ansible roles to create a security-hardened Ubuntu 20.04 server for Jamulus sessions.

## Example usage
Use/modify `main.yml` file to suit your needs or use the example below
```
---
- name: Play for security hardening, SMTP setup & unattended upgrades
  hosts: raw
  roles:
  - provision
  - smtp-setup
  - unattended-upgrades
  - linux-security

- name: Play to set up Jamulus
  hosts: raw
  roles:
  - jamulus-setup
```

Don't forget to set variables (check `rolename/defaults/main.yml` for defaults):
* `jamulus-setup/vars/main.yml`
* `linux-security/vars/main.yml`
* `provision/vars/main.yml`
* `smtp-setup/vars/main.yml`
* `unattended-upgrades/vars/main.yml`


