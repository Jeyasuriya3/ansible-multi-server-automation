Ansible Multi-Server Automation Lab

Project Overview
Built a hands-on Ansible automation lab using an Ubuntu WSL control node and two Ubuntu Docker containers as managed nodes. Configured SSH key-based authentication and automated basic Linux administration tasks across both nodes.

Technologies Used
- Ubuntu Linux / WSL
- Ansible Core
- Docker
- SSH key-based authentication
- YAML
- Nginx

Lab Architecture
- Control Node: Ubuntu on WSL with Ansible installed
- Managed Node 1: Ubuntu Docker container
- Managed Node 2: Ubuntu Docker container
- Connection: SSH key-based authentication

Tasks Implemented
1. Created two Ubuntu Docker containers for Ansible practice.
2. Configured the `ansible` user and SSH public-key authentication.
3. Created an Ansible inventory to manage multiple hosts.
4. Verified connectivity using the Ansible ping module.
5. Executed Linux commands across multiple managed nodes.
6. Created a playbook to retrieve server hostnames.
7. Created a disk usage monitoring playbook.
8. Automated Nginx package installation using Ansible.
9. Configured privilege escalation for package management in the lab.

Example Commands

Verify connectivity:

`ansible webservers -i inventory/inventory.example -m ping`

Run the Nginx installation playbook:

`ansible-playbook -i inventory/inventory.example playbooks/install-nginx.yml`

Key Learnings
- Ansible inventory and host groups
- SSH authentication and remote execution
- YAML playbook structure
- Ansible modules, variables, and task execution
- Privilege escalation with `become`
- Linux package management and basic infrastructure automation

Lab Limitations
The managed nodes are Docker containers, not full virtual machines. Since systemd is not running as PID 1 in this lab, `systemctl`-based service verification is not supported by the current container setup.

Future Improvements
- Deploy a custom HTML page through Nginx.
- Add disk usage threshold alerts.
- Use Ansible roles to organize reusable tasks.
- Integrate the project with GitHub Actions for automated checks.

Disclaimer
This project is for learning and demonstration purposes. No private SSH keys, passwords, or other secrets should be committed to the repository.
