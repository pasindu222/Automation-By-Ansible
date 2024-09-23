# Ansible Project: Automatically Log into Different User Accounts on Windows PCs

## **Description:**
This project uses **Ansible** to automate the process of logging into different user accounts on multiple **Windows** client machines from a **Linux** server without manually typing credentials. 

## **Key Features:**
- **Automated User Switch:** 
  - Automatically switch all Windows client PCs to a specified user account simultaneously.
  
- **Efficient User Management:** 
  - Manage multiple Windows clients through one central **Linux** server using **Ansible**.
  
- **Credential-less Login:**
  - No need to manually enter credentials for each user account switch.

## **Technologies Used:**
- **Ansible** for automation.
- **Linux** server for orchestration.
- **Windows** client machines.

## **Prerequisites:**
1. Ensure Ansible is installed on your Linux server.
    ```bash
    sudo apt update
    sudo apt install ansible
    ```

2. Set up SSH connectivity to Windows machines (e.g., using `pywinrm` for remote management).

3. Configure Windows clients to accept Ansible commands.
    - Install WinRM on Windows clients.
    - Open PowerShell and run:
    ```powershell
    winrm quickconfig
    ```

## **Usage:**
1. Clone this repository:
    ```bash
    git clone https://github.com/yourusername/ansible-windows-user-switch.git
    ```

2. Update the inventory file with the IP addresses of the Windows client machines.

3. Run the Ansible playbook to switch users:
    ```bash
    ansible-playbook switch-user.yml
    ```

4. Verify the changes by logging into the Windows clients.


## **Contact:**
For any queries, contact me at [pasindu.erangak@gmail.com].
