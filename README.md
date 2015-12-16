Vagrant Centos 7 lamp using Ansible playbook
=========================================

[![Issues](https://img.shields.io/github/issues/skecskes/vagrant-centos7-ansible-lamp.svg?style=plastic)](https://github.com/skecskes/vagrant-centos7-ansible-lamp/issues) 
[![Forks](https://img.shields.io/github/forks/skecskes/vagrant-centos7-ansible-lamp.svg?style=plastic)](https://github.com/skecskes/vagrant-centos7-ansible-lamp/network) 
[![Stars](https://img.shields.io/github/stars/skecskes/vagrant-centos7-ansible-lamp.svg?style=plastic)](https://github.com/skecskes/vagrant-centos7-ansible-lamp/stargazers) 
[![License](https://img.shields.io/badge/license-GPLv2-blue.svg?style=plastic)](LICENSE)


This personal development VM with Ansible provisioning is **fully working example**. I created this VM in order to 
have a proper php testbed for my php applications. After vagrant up, the main url will welcome you with phpinfo(). 
I hope you will enjoy this VM and I always accept recommendations and requests.

## Guest OS

I am using the lastest CentOS 7 x64 image from official [Hashicorp](https://atlas.hashicorp.com/centos/7) (thanks)

## Prerequisites / Requirements

- [Virtualbox platform](https://www.virtualbox.org/wiki/Downloads)
- [Vagrant](https://docs.vagrantup.com/v2/installation/) 
- guest additions to Vagrant `vagrant plugin install vagrant-vbguest`
- [Git]()

## How to run

Create your new folder for your project. Clone this repository into that folder, which will download all configuration
needed to run vagrant machine. Then just run `vagrant up` in terminal and the rest will be done automatically.

Note, that if you run it first time, vagrant will download the guest OS (414 MB of Centos 7 in this case) box 
from internet, which in my case took 8 minutes and will save it locally so that you can use it later.

1. open terminal
2. $ *cd /var/www*
3. $ *mkdir project*
4. $ *cd project*
5. $ *git clone git@github.com:skecskes/vagrant-centos7-ansible-lamp.git*
6. $ *vagrant up*
7. Enjoy

Your /var/www/project folder will be synced with with vagrants apache root directory.

## What is included

### Tag 1.0

- Apache 2.4.6
- latest php 5.6.*
- latest mySQL MariaDB 5.5.* on port 3306 (user: root, pass: toor)
- phpinfo() on http://10.0.0.10
- phpmyadmin on http://10.0.0.10:9000 (latest version is cloned into vagrantbox)


### Tag 2.0

Same as previous, but latest PHP 7.0.* (php7) is used

![php7](ansible/roles/php70/php7.png)    