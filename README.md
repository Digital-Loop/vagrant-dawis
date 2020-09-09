# Vagrant DAWIS

The open source data warehouse system in a local environment.

A Vagrant box based containing Lubuntu linux, Python, Pipenv, MongoDB, MySQL, ChromeDriver and DAWIS. Provisioned with ansible.

## Requirements

* VirtualBox
* Vagrant

## Useful Info

* If this is your first time, please install the guest extension plugin:

```shell
vagrant plugin install vagrant-vbguest
```

* to start a new instance:

```shell
vagrant up
```

* to provision the environment:

```shell
vagrant provision
```

* access the VM using SSH:

```shell
vagrant ssh
```

* in the VM:

```shell
cd dawis/
```

* in the VM:

```shell
sudo pipenv install
```

* in the VM:

```shell
pipenv shell
```

* in the VM:

```shell
sudo systemctl daemon-reload
```

* in the VM:

```shell
sudo systemctl start dawis.service
```

* in the VM:

```shell
sudo systemctl status dawis.service
```

* in the VM:

```shell
python3.8 dawis.py worker
```

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
