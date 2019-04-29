## Laravel Development Environment With Vagrant & Ansible

Uses Vagrant to provision a virtual machine running on Centos7 for Laravel development. Complete the installation by navigating to http://127.0.0.1:8080 and finishing the Wordpress wizard.

---

Ansible playbooks for:

- Add epel & webtatic & mariadb repos to the server.
- Install required system packages.
- Install apache web server.
- Install php7 & php-fpm and some dependencies.
- Install mariadb server & client and secure db.
- Install composer.

## Prerequisites

- Install [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- Install [Vagrant](http://www.vagrantup.com/) (tested with 2.1.5)

## Usage:

- Clone this repository to the root of your project directory
  ```bash
  git clone git@github.com:abdelrahman403/vagrant-ansible-laravel.git
  ```
- Change the variables at `group_vars/all`
- In your project directory, run `vagrant up`

### Port forwarding:

Nginx works on port 80 on the guest is forwarded to port 8080 on the host.
