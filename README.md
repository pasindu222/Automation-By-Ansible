Automating Windows Client User Switch with Ansible
This project demonstrates the use of Ansible, an open-source automation tool, to automate user management tasks on Windows client PCs from a Linux server. Specifically, the playbook switches all connected Windows client machines to a separate user account simultaneously without requiring manual credential input.

Features
Automated user switch across multiple Windows client PCs.
Centralized control from a Linux server.
Efficiency in managing large-scale user account switches.
Technologies Used
Ansible: For configuration management and automation.
Linux: The server operating system to run the Ansible playbooks.
Windows: The client machines where the user switch is performed.
Instructions
Clone the repository to your Ansible control machine (Linux server).

bash
Copy code
git clone https://github.com/yourusername/your-repository.git
Update the inventory file with the Windows client IP addresses.

ini
Copy code
[windows]
192.168.1.101
192.168.1.102
Edit the playbook.yml file to customize the target user account.

yaml
Copy code
---
- name: Switch Windows Clients to a Different User Account
  hosts: windows
  tasks:
    - name: Switch user account
      win_shell: net user newusername newpassword
Run the playbook to apply the changes across all Windows client machines.

bash
Copy code
ansible-playbook playbook.yml -i inventory
Contributing
Feel free to fork this repository, submit issues, and send pull requests. Contributions and suggestions for improvements are always welcome.
