# Ansible User Management Role

## What this project does
Automates Linux user management on Amazon Linux EC2 using Ansible.

## Concepts covered
- Ansible Roles structure
- Ansible Vault (encrypted passwords)
- block / rescue / always (error handling)
- loops (create multiple users from a list)
- tags + when conditionals
- register + debug

## Role features
- Creates multiple users from a single variable list
- Assigns users to a devops group
- Deploys SSH public keys per user
- Grants selective sudo access via sudoers template
- Vault-encrypted passwords — safe to commit to Git
- Fully idempotent — safe to re-run anytime

## Project structure
ansible-task2/
├── inventory.ini
├── site.yml
└── roles/
    └── webserver/
        ├── tasks/main.yml
        ├── handlers/main.yml
        ├── templates/sudoers.j2
        ├── defaults/main.yml
        └── vars/main.yml

## How to run
ansible-playbook -i inventory.ini site.yml \
  --vault-password-file ~/.vault_pass

## Author
Your Name | LinkedIn: linkedin.com/in/yourprofile
