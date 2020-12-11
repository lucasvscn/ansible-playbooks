# Ansible Playbooks

**Features**

 - Handle server passwords with ansible-vault
 - Initial server setup
 - Install LEMP stack
 - Set firewall ports
 - Set site SSL
 - Set new PHP site
 - Set new static site
 - Set new MySQL db
 - Set new MySQL user
 - Set supervisor services
 - Set crontab tasks


## Handling server passwords

First you need to create a password file for your vault with following command.

```bash
$ mkdir .vault && echo 'dev my_secret_password' > .vault/vault_passwd
```

Run the `servers_passwords/playbook.yml` to generate passwords for all your hosts.

```bash
$ ansible-playbook -i hosts server_passwords/playbook.yml
```

Generated passwords will be stored by default in `.vault/vault.yml` file.
