# ansible-projects
# Ansible Setup and Basic Usage

This README provides a guide to set up Ansible and perform basic tasks.

## Setup

### Create EC2 Instances:

- Launch two EC2 instances named ansible_server and target_server.

### Login to Ansible Server:

- SSH into the Ansible server.
- Update the package lists:
  ```bash
  sudo apt update

Install Ansible:
sudo apt install ansible

Verify Installation:
Check Ansible version:
ansible --version

Set Up Passwordless Authentication:
SSH into the target server using its private IP:
ssh <target_server_private_ip>

Update packages:
sudo apt update

Generate SSH keys on the Ansible server:
ssh-keygen

Copy the public key:
cat /home/ubuntu/.ssh/id_rsa.pub

SSH into the target server and navigate to SSH directory:

ssh <target_server_private_ip>

Create authorized_keys file:
vim ~/.ssh/authorized_keys

Paste the public key of the Ansible server into authorized_keys.

Verify Setup:
SSH into the Ansible server using its private IP to ensure successful login.


Usage

Create an inventory file and add the public IP of the target server:
echo "<target_server_public_ip>" > inventory

Execute Ansible Ad-hoc Commands

Run commands:
Create a file named "ashwini" on all servers:

ansible -i inventory all -m shell -a "touch ashwini"

Check the number of processors on all servers:
ansible -i inventory all -m shell -a "nproc"
