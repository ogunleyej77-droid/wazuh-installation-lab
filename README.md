# Wazuh Installation Lab

## Overview
This repository documents my Wazuh SIEM installation and cybersecurity lab practice using Wazuh VM (Wazuh v4.14.4 OVA) on VirtualBox.

## Objectives
- Install Wazuh SIEM
- Configure monitoring
- Learn SIEM operations
- Practice troubleshooting

## Tools Used
- Wazuh v4.14.4 OVA
- VirtualBox
- Ubuntu Linux

## Installation Steps
1. Downloaded the Wazuh OVA file
2. Imported the OVA into VirtualBox
3. Started the Wazuh VM
4. Accessed the Wazuh dashboard
5. Explored manager and indexer services

## Troubleshooting

### Issue
wazuh-manager failed to start.

### Error Check

```bash
sudo journalctl -xeu wazuh-manager
sudo systemctl status wazuh-manager
sudo systemctl status wazuh-indexer
```

### Cause
- Configuration error in Wazuh VM settings
- Wazuh indexer service was inactive
- Wazuh manager service failed

### Solution

```bash
sudo systemctl restart wazuh-manager
sudo systemctl restart wazuh-indexer
```

Corrected the configuration issue and restarted the services successfully.

## Lessons Learned
- Learned basic SIEM operations
- Improved Linux command-line skills
- Understood how to troubleshoot Linux services
- Learned how Wazuh monitoring works

## Screenshots
<img width="1280" height="720" alt="61035bfc-4bf0-4375-9ad5-18b03e82dd19" src="https://github.com/user-attachments/assets/2fc58c5a-4201-47ef-9270-917bdcb3db7b" />
<img width="1280" height="720" alt="7953e3f2-ea9e-4abe-938c-cc5444b6bdf3" src="https://github.com/user-attachments/assets/ca9e0a71-bd72-43eb-af41-bdb5737ee437" />
