### Running the dev box.
1. Install [Python](http://www.python.org.br/wiki) and [pip](https://github.com/pypa/pip)
2. Install [VirtualBox](http://www.virtualbox.org)
3. Install [Vagrant](http://www.vagrantup.com/)
4. Install [Ansible](http://www.ansible.com/)
  pip install ansible
5. Clone the project
  git clone git@github.com:duduribeiro/rails-dev-box.git
  cd rail-dev-box
6. Start the box
  vagrant up
7. SSH to the box
  vagrant ssh

### Configurations
You can configure variables in ansible/vars/main.yml
```
  ruby_version: 2.1.2  # The ruby version you wanna install

  # The following vars are conditional vars. If specified yes, install.
  install_mysql: yes
  install_postgres: yes
```
