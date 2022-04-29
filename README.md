# Vagrant DAWIS - SEO Data Warehouse

The open source SEO data warehouse system in a local environment.

A Vagrant box based containing Lubuntu linux, Python, Pipenv, MongoDB, MySQL, ChromeDriver and DAWIS. Provisioned with ansible.

## Requirements

* VirtualBox
* Vagrant

## Useful Info

* If this is your first time, please install the guest extension plugin:

```shell
vagrant plugin install vagrant-vbguest
```

## How To Use

* clone the repository

```shell
git clone https://github.com/Digital-Loop/vagrant-dawis.git
```

* from the cloned directory

```shell
cd vagrant-dawis
```

* to start a new instance:

```shell
vagrant up --provision
```

* access the VM using SSH:

```shell
vagrant ssh
```

* in the VM:

```shell
cd dawis/
```

* in the VM: Install dependencies

```shell
sudo pipenv install
```

* in the VM: Run the Celery worker for the dawis project

```shell
pipenv run python3.8 dawis.py -A dawis worker -l info -B
```

* in the VM: Terminate all running tasks

```shell
Ctrl + C
```

* in the VM: Clear cache in the lock file works every time

```shell
sudo pipenv lock --clear
```

* in the VM: Reinstall dependencies

```shell
sudo pipenv install
```

* in the VM: Start Dawis and MongoDB as a services

```shell
sudo systemctl start mongod.service
sudo systemctl start dawis.service
```

## Private network

### Linux enviroment virtual machine

- Ip: "192.168.33.10"

### Software Versions

 - Lubuntu desktop 18.04
 - Python 3.8
 - Pipenv 2020.8.13
 - MongoDB 4.4.0
 - MySQL 5.7.31
 - ChromeDriver (stable release)
 - DAWIS (last version)

### Ansible Roles

- python
- mongodb
- mysql
- chromedriver
- dawis

### Common Packages

 - ash-completion
 - python-pycurl
 - git
 - htop
 - tree
 - vim
 - curl
 - zip
 - rsync
 - wget
 - ant
 - tmux
