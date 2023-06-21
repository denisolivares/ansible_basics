# ansible_basics
Learn Ansible Basic

ansible-controller  192.168.1.209
ansible-target-01   192.168.1.180
ansible-target-02   192.168.1.99

CentOS 
yum install epel-release
yum install ansible

sudo vim /etc/sysconfig/network-scripts/ifcfg-enp0s3

ansible target1 -m ping -i inventory.txt

## Disable Key Host Check

```bash
vim /etc/ansible/ansible.cfg
host_key_checking = False
```