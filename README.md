# Munki

[![Build Status](https://travis-ci.org/bjoernalbers/ansible-role-munki.svg?branch=master)](https://travis-ci.org/bjoernalbers/ansible-role-munki)

Ansible Role to install a [Munki](https://www.munki.org) server on Ubuntu.
This creates an empty munki repository and makes it available via
http://munki/repo and smb://munki/repo (if the server's hostname is "munki").
It also comes with automatic daily backups using `rsnapshot`.


## Requirements

The server should run a recent version of Ubuntu Linux.
I've tested with Ubuntu 16.04 (Xenial Xerus) and 18.04 (Bionic Beaver).


## Role Variables

You might want to change `munki_samba_password` (default: "munki").


## Dependencies

None :-)


## Example Playbook

    ---
    - name: Install Munki Server
      hosts: munki
      roles:
        - role: munki
          munki_samba_password: a575bdacc5a6f2a77ccee76b9dad45bf


## License

This Ansible role is released under the [MIT License](LICENSE.txt).
