# Password-Changer
_Ansible playbook for generating and changing passwords for multiple users on multiple hosts and creating CSV report._

## Usage:
1. Define users and target servers in [inventory.ini](./inventory.ini) file.
2. Change password complexity and report pattern in [password.yml](./password.yml) if needed.
3. Run playbook. Example:
```
ansible-playbook playbook.yml -i inventory.ini --ask-become-pass --ask-pass
```
4. Check ```ansible-password-changer-report.txt``` file which appeared in your current directory.

## To do:
- [ ] Set complexity in inventory file
