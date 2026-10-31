# Wazuh SIEM Home Lab
A home lab using Wazuh SIEM for security monitoring and File Integrity Monitoring (FIM).

## Objective
Built a two-VM home lab using Wazuh to practice endpoint monitoring.

## Environment
- Oracle VirtualBox running on Windows PC
- Ubuntu Desktop 24.04 – Wazuh Manager (192.168.10.11)
- Windows 11 – Wazuh Agent (192.168.10.9)

## Implementation
- Installed and configured the Wazuh Manager and dashboard on the Ubuntu system.
- Installed the Wazuh agent on the Windows machine and registered it with the manager.
- Confirmed the agent showed as Active in the dashboard.
- Edited the agent's `ossec.conf` file to monitor a test folder with `realtime="yes"`.
- Added and deleted test files in the test folder, and then confirmed alerts were generated on Wazuh.

## Results
- The Windows agent was enrolled successfully and showed as **Active**.
- Wazuh FIM detected file **added** and **deleted** events in the monitored folder within seconds.
- Generated alerts after creating and deleting the test files.

## Screenshots

### 1. Before: no agents registered
![No agents registered](screenshots/01-no-agents.png)

### 2. Windows agent configured
![Windows agent running](screenshots/02-agent-running.png)

### 3. After: agent active
![Agent active overview](screenshots/03-agent-active-overview.png)

### 4. Agent details
![Agent list](screenshots/04-agent-list.png)

### 5. FIM configuration
![FIM config](screenshots/05-fim-config.png)

### 6. FIM events
![FIM events](screenshots/06-fim-events.png)

### 7. File added alert
![File added](screenshots/07-fim-file-added.png)

### 8. File deleted alert
![File deleted](screenshots/08-fim-file-deleted.png)
