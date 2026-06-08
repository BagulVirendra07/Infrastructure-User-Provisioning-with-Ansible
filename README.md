# Linux User Provisioning with Ansible

## Project Overview

This project demonstrates infrastructure automation and Linux user administration using Ansible on Amazon Linux EC2 instances. It leverages Ansible Roles to provision and manage user accounts, configure SSH access, assign group memberships, and implement privilege management through reusable and scalable automation practices.

## Key Features

* Provision multiple Linux users from a centralized variable file
* Assign users to predefined groups for role-based access control
* Configure SSH public key authentication for secure remote access
* Manage sudo privileges using Jinja2-based sudoers templates
* Secure user passwords with Ansible Vault encryption
* Implement idempotent playbooks for consistent and repeatable deployments
* Support conditional task execution and selective task tagging
* Include structured error handling using `block`, `rescue`, and `always`

## Technologies & Concepts

* Ansible Roles
* Ansible Vault
* Linux User & Group Management
* SSH Key Management
* Jinja2 Templates
* Infrastructure as Code (IaC)
* Task Tags & Conditionals
* Loops and Variable Management
* Error Handling and Debugging

## Project Structure

```text
ansible-user-management/
├── inventory.ini
├── site.yml
└── roles/
    └── user_management/
        ├── tasks/
        │   └── main.yml
        ├── handlers/
        │   └── main.yml
        ├── templates/
        │   └── sudoers.j2
        ├── defaults/
        │   └── main.yml
        └── vars/
            └── main.yml
```

## Learning Outcomes

* Developed hands-on experience with Ansible Role-based project architecture
* Automated Linux user and access management tasks
* Applied Infrastructure as Code (IaC) principles for server configuration
* Implemented secure credential management using Ansible Vault
* Improved understanding of Linux administration and automation workflows

## Execution

```bash
ansible-playbook -i inventory.ini site.yml \
--vault-password-file ~/.vault_pass
```
