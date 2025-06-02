# SOCjira Ansible Project

## Usage

Run the full setup:

```bash
ansible-playbook -i inventory/inventory.ini playbooks/setup.yml --ask-become-pass
```
After installation, access Jira via: http://<vm_ip>:8080

# SOCjira Ansible Role

This Ansible project automates the installation and configuration of **Jira Software** on a Linux server (tested on Ubuntu).

## 🚀 What It Does

- Creates necessary users and directories
- Downloads and installs Jira silently
- Sets up Jira to run as a systemd service
- Optionally configures Jira to start on boot
- Enables access from a web browser for OSINT-related tracking/reporting

## 📁 Project Structure

socjira-ansible/
├── tasks/
│ └── main.yml
├── templates/
│ └── jira-response.varfile.j2
├── files/
├── vars/
│ └── main.yml
└── README.md


## 🛠️ Requirements

- Ansible
- Target: Ubuntu server VM with internet access

## 🔧 Variables

```yaml
jira_user_group: jira
jira_user: jira
jira_home: "/var/jira"
jira_version: "9.12.23"
jira_download_link: "https://www.atlassian.com/software/jira/downloads/binary/atlassian-jira-software-9.12.23-x64.bin"
jira_user_home_dir: "/opt/atlassian"
```

---

### ✅ 3. **LICENSE**

```text
MIT License

Copyright (c) 2025 Nada Mejri

Author contact: mejrinada8@gmail.com
