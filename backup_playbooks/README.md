# Ansible Playbook: Backup Configuration Files

This Ansible playbook is designed to create a backup of configuration files on all hosts.

## Usage

### Prerequisites

Before running this playbook, ensure you have the following prerequisites:

- Ansible is installed on your control node.
- Your inventory file includes the target servers.
- SSH access to the target servers is configured.
- Python is installed on the target servers.
- Privilege escalation is configured (if necessary) to allow Ansible to execute commands with elevated privileges.

### Running the Playbook

To run the playbook, use the following command:

```bash
ansible-playbook -i inventory playbook.yml

1 Playbook Description
The playbook performs the following tasks:

Create Backup Directory:
Creates a directory at /var/backups/config to store the backup files.

Backup Configuration Files:
Archives the /etc/config_files directory into a compressed tarball named inventory_hostname_config_backup.tar.gz within the backup directory.

2 Requirements
Ensure the following requirements are met before running the playbook:

Ansible is installed on the control node.
SSH access to the target servers is available.
Python is installed on the target servers.
Privilege escalation is configured as needed.
