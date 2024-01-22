# Ansible Role: PostgreSQL
Installs and configures PostgreSQL server 

## Features

* Create database 
* Dump an existing database to a file
* Create postgres user
* Grant privileges on a database to a user


#### Note: if you need set dns for installing postgres you can add pre-install role in play.yaml like this:
```
- name: install postgresql service
  hosts:
    - database
  become: yes
  roles:
    - pre_install
    - postgresql
```
### Add SSH key
run these commands to add ssh key :
```
ssh-keygen
ssh-copy-id -i ~/.ssh/id_rsa.pub user@[target_server]
```

### Run the Playbook:
```
ansible-playbook -i [inventory file] play.yml
```

### Access to postgres:
you can check instalation on target server by running these commands:
```
user:~$ sudo -i -u postgres
postgres@user:~$ psql
```
Also you can access postgres from remote servers on its default port 5432
