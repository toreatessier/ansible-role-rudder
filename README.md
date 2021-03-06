# Ansible Role : Rudder

Ansible Role for Rudder

Requirements
------------

- Debian 9 with minimal install
- SSH installed and sshd.service enabled
- **sudo** package installed
- One bridged interface (no more) using the **.20.29/26 IP**
- DNS set to 192.168.4.2 in */etc/resolv.conf*
- [User 'Ansible' already configured](https://github.com/nickjj/ansible-user)

**Note** : A template Debian 9 VM **with all requirements satisfied** is available [here](https://192.168.4.16/Equipe_1_Jakarta/debian9-template).

Example Playbook
----------------

```
- name: Deploy Rudder for Jakarta
  hosts: "{{hosts}}"
  remote_user: ansible
  tasks:
  - import_role:
      name: rudder
      tasks_from: install
```

Author Information
------------------

* **Toréa TESSIER** - <torea.tessier@reseau.eseo.fr> - [Jakarta Project](https://192.168.4.16/Equipe_1_Jakarta/)