# Ansible Role: PostgreSQL
Installs and configures PostgreSQL server 

## Features

* Create database 
* Dump an existing database to a file
* Create postgres user
* Grant privileges on a database to a user


### Note: if you need set dns for installing postgres you can add pre-install role in play.yaml like this:
```
- name: install postgresql service
  hosts:
    - database
  become: yes
  roles:
    - pre_install
    - postgresql

```


### Run the Playbook:
```
ansible-playbook -i [inventory file] play.yml
```