# Install and Start Nginx Playbook

This playbook automates the installation and starting of the Nginx web server on target hosts. It ensures that Nginx is installed and the service is started, allowing for quick and easy deployment of web servers.

## Usage

To use this playbook, ensure Ansible is installed on your system and update the inventory file to specify the target hosts where Nginx should be installed. Then, execute the playbook using the ansible-playbook command:

```bash
ansible-playbook -i inventory install_and_start_nginx.yml
