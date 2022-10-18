# ansible

* install ansible: `python3 -m pip install --user ansible`

* add computers:
file: `/etc/ansible/hosts`
```
[myvirtualmachines]
192.0.2.50
192.0.2.51
192.0.2.52
```

* verify hosts: `ansible all --list-hosts`
* ping: `ansible all -m ping`
* basic config to install apt packages:
```
- hosts: servers
  gather_facts: no
  tasks:
   - name: install php
     apt:
      name: 
       - php8.0-fpm 
       - php-common 
       - php-curl 
       - php-json
       - php-mbstring 
       - php-xml 
       - php-zip
      state: present
   - name: install certbot
     apt:
      name: python3-certbot-nginx
      state: present
```
* run command: `ansible servers -a "echo 'test'"`