## Prerequisites

1. Ansible installed - https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html
2. Vagrant installed (only for local-testing) - https://www.vagrantup.com/downloads.html

## Steps to test on vagrant box

1. Run `$ vagrant up` for getting vagrant box up and running
2. Rename `ansible.cfg.example` to `ansible.cfg` and update value of `private_key_file` with ssh_private_key value of vagrant box that can be retrieved from `$ vagrant ssh-config`
3. Rename `hosts.example` to `hosts`
4. Run command `$ ansible-playbook -vvv site.yml`, in the output of this command at "Get Admin Password" stage copy Jenkins inital password from `stdout_lines` key.
5. Enter intial password at http://<host>:8080 

