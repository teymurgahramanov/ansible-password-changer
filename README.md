# Password-Changer
_Ansible playbook for changing passwords for multiple users on multiple hosts. Will generate CSV report importable to password manager solution._

## Usage:
1. Define users and target servers in yaml file (ex. users.yml)
```
users:
  - 'john'
  - 'alice'

targets:
  - srv1.example.com
  - srv2.example.com
  - srv3.example.com

```
2. Change password complexity and report pattern in password.yml if needed.
3. Run playbook
```
ansible-playbook playbook.yml  --ask-become-pass --ask-pass --extra-vars "@users.yml"
```
4. Check ```ansible-password-changer-report.txt``` file which appeared in your current directory.

## To do
- Custom complexity per user