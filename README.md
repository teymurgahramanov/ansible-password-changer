# Password-Changer
_Ansible playbook for generating passwords for multiple users on multiple hosts and creating CSV report importable to password manager solution._

## Usage:
1. Define users and target servers in ini file (Look at users-example.ini)
2. Change password complexity and report pattern in password.yml if needed.
3. Run playbook
```
ansible-playbook playbook.yml -i users.ini --ask-become-pass --ask-pass
```
4. Check ```ansible-password-changer-report.txt``` file which appeared in your current directory.

## To do
- Custom complexity per user