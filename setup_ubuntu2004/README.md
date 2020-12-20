# Initial Server Setup on Ubuntu 20.04

This playbook will execute a initial server setup for Ubuntu 20.04 systems. A password will be set to the sudo remote user.
Review `server_passwords/README.md` details about password vault.

## Settings

- `create_user`: the name of the remote sudo user to create.
- `copy_local_key`: path to a local SSH public key that will be copied as authorized key for the new user. By default, it copies the key from the current system user running Ansible.
- `sys_packages`: array with list of packages that should be installed.


## Run the Playbook

```command
ansible-playbook -l [target] -i [inventory file] -u [remote user] --vault-id [tag]@[vault_passwd] playbook.yml
```
