# Ansible Playbook: Update Packages and Reboot

This Ansible playbook is designed to update packages on all hosts and reboot them if necessary.

## Usage

1. Ensure Ansible is installed on your control node.
2. Configure your inventory file to include the target servers.
3. Run the playbook using the following command:

```
ansible-playbook -i inventory playbook.yml
```
Replace inventory with the path to your inventory file containing the target servers.

Before running this playbook, make sure you have SSH access to the target servers and appropriate privileges to execute commands with elevated privileges if necessary.

Feel free to customize the playbook and inventory according to your specific requirements.
