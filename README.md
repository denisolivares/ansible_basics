# ansible_basics
Learn Ansible Basic

CentOS 
yum install epel-release
yum install ansible

sudo vim /etc/sysconfig/network-scripts/ifcfg-enp0s3
ansible target1 -m ping -i inventory.txt

## Disable Key Host Check

```bash
vim /etc/ansible/ansible.cfg

[default]
host_key_checking = False
```

## Ansible Concepts

### Inventory
Inventory file or default file - /etc/ansible/hosts

### Ansible parameters

- `ansible_host` - server1.company.com
- `ansible_connection` - ssh/winrm/localhost
- `ansible_port` - 22/5986
- `ansible_user` - root/administrator
- `ansible_ssh_pass` or `ansible_password` (windows) - password

### Ansible Playbooks

Dictionaries are unordered whilst lists are ordered. This is very important while constructing your playbooks as it can result in erros if a list is declared in the incorrect order.

- `ansible-doc -l` - to check the available modules for Ansible


### Ansible Variables

### Ansible Loops

loop == with_* (*lookup plugins)

### Ansible Roles

Ansible galaxy
- `ansible-galaxy init mysql` - will create the folder structure
- Folder structure
  - `/etc/ansible/roles` - Default folder if you don't define one
  - Under a `roles` folder within your project folder
  - /etc/ansible/ansible.cfg -> `roles_path = ...`
- List roles
  - `ansible galaxy search`
  - `ansible_galaxy install`
  - `ansible_galaxy list`
  - `ansible-config dump | grep ROLE`

### Conclusion

```bash
sudo yum install ansible -y
ansible-galaxy install geerlingguy.nodejs -p /home/bob/playbooks/roles

```