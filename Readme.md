# Learn Ansible

## Basic implementation of Ansible.

### Installation/Setup

-   Install the dependencies on host system.

```sh
sudo apt-get update
sudo apt-get install ansible
sudo apt-get install sshpass
```

-   Create an inventory dir where the config files for target hosts will be stored.

```sh
mkdir inventory
cd inventory
touch hosts
```

-   Command to check connection.

```sh
ansible -i ./inventory/hosts ubuntuServers -m ping --user yash --ask-pass
```

-   Command to run playbook.

```sh
ansible-playbook ./playbooks/apt.yml --user yash --ask-pass --ask-become-pass -i ./inventory/hosts
```
