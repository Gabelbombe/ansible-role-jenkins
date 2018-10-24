# Test setup

This is an example setup, based on vagrant + virtualbox, that allows to easily run ansible commands to test the module.

# Requirements

- vagrant > 2.0.0
- vagrant plugin install vagrant-aws
- virtualbox > 5.1.28

# Setup

in `$WORK_DIR/ansible-role-jenkins/tests`:

- Add dummy box `vagrant box add dummy https://github.com/mitchellh/vagrant-aws/raw/master/dummy.box`
- provision VM: `vagrant up`
- connect to the VM to check the configuration: `vagrant ssh`
- destroy VM when needed: `vagrant destroy -f`

in `$WORK_DIR`:

- run ansible-playbook: `ansible-playbook ansible-role-jenkins/tests/test_7_default.yml -i ansible-role-jenkins/tests/inventory`
