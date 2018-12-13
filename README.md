# Munki

Ansible Role to installs a [Munki](https://www.munki.org) server on Ubuntu.
This just sets up an empty munki repo on your host and makes it available over
HTTP (nginx) and SMB (samba).


## Requirements

The server should run a recent version of Ubuntu Linux.
I've tested with version 18.04 (bionic beaver).


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
