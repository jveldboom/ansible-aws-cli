# Ansible AWS CLI Playbook
Ansible playbook to install AWS CLI on Ubuntu 14.04. Should work on most other versions of Ubuntu too.

## Setup
- Clone or download the repo to your Ansible machine
- Add your host information within `inventories/hosts`
- Add your AWS creditentials within `vars/vars.yml`

## Run Playbook
Below is how I prefer to run Ansible playbooks since it allows you to choose the host and SSH user dynamically.

```
ansible-playbook -i inventories/hosts playbook.yml --extra-vars="hosts=vagrant user=vagrant" --ask-pass
```

The `--extra-vars` parameter sets the "host" and "user" variable in the `playbook` file. And `--ask-pass` will prompt you for a password.

## Questions, comments, or suggestions are welcome!
Please [submit an issue](https://github.com/jveldboom/ansible-aws-cli/issues) if you have any questions or want to help improve this playbook. Thanks!
