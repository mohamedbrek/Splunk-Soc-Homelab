# Splunk SOC Home Lab
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
![Splunk](https://img.shields.io/badge/Splunk-000000?style=for-the-badge&logo=splunk&logoColor=white)
![Sysmon](https://img.shields.io/badge/Sysmon-0078D4?style=for-the-badge&logo=windows&logoColor=white)
![Splunk Universal Forwarder](https://img.shields.io/badge/Splunk_Universal_Forwarder-65A637?style=for-the-badge&logo=splunk&logoColor=white)

## Introduction

This report describes my personal home laboratory set up with SOC and use of Splunk Enterprise on Ubuntu as a virtual machine for the collection and monitoring of events from the Windows operating system.
I have used Sysmon for the generation of logs regarding endpoint activity and Universal Forwarder in order to relay those logs to Splunk for monitoring.
The goal of this report is to show my real-life experience of SIEM deployment and logging and monitoring of the event on Windows as an element of my learning process in the field of cybersecurity.

## Lab Setup

**Windows 11 + Sysmon → Splunk Universal Forwarder → Splunk Enterprise on Ubuntu**

- **Windows 11:** Device producing activities on the system.
- **Sysmon:** Keeps track of system and process activities.
- **Splunk Universal Forwarder:** Forwards Windows events to Splunk server.
- **Ubuntu:** A VM that operates Splunk Enterprise.
- **Splunk Enterprise:** Responsible for indexing and searching events received.
## Tools Used

- Splunk Enterprise
- Splunk Universal Forwarder
- Microsoft Sysmon
- Ubuntu Linux
- Windows 11
- Oracle VirtualBox

## Execution

### 1. Splunk Server Configuration

I installed Splunk Enterprise on an Ubuntu VM and logged into its web interface.

### 2. Event Collection from Windows

I Configured Sysmon on the Windows PC to log system events, including process creation events.

### 3. Log Forwarding

I configured the Splunk Universal Forwarder to transmit Windows Sysmon events to the Splunk server using a network connection.

### 4. Receiving Configuration

Splunk was configured to start receiving forwarded information using port 9997.

### 5. Validation

I used Splunk to search for incoming Windows events to ensure that they were properly logged.


## Key Learnings

- Implementing a security information and event management system in a virtualized system. 
- Gathering Windows endpoint telemetry using Sysmon.
- Sending logs from the Windows computer to the centralized Splunk server. 
- Setting network communication between the systems in the lab. 
- Searching and analyzing Windows's security events in Splunk. 
- Solving service and connectivity problems during installation.

## Future Enhancements

- Continue with the practice of SPL queries for event analysis related to security.
- Create dashboards for Windows activity visualization.
- Study unsuccessful login attempts and execution of potentially suspicious process.
- Create rule of detection and designate investigation processes.
- Map selected detections to MITRE ATT&CK.

## Repository Structure
```text
SPLUNK-SOC-HOMELAB/
├── README.md
└── screenshots/
    ├── 01-Splunk-web-dashboard.png
    ├── 02-Ubuntu-splunk-server.png
    ├── 03-Windows-services.png
    ├── 04-Splunk-receving-configuration.png
    ├── 05-Incoming-sysmon-events.png
    └── 06-Process-creation-event.png
```

## Connect

Thank you for taking the time to view this project.

I'm documenting my cybersecurity learning journey by completing hands-on labs in networking, Linux, digital forensics, cloud computing, and SOC analysis. Feel free to explore my other repositories to see what I'm learning next.

[![GitHub](https://img.shields.io/badge/GitHub-mohamedbrek-181717?logo=github)](https://github.com/mohamedbrek)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Mohamed%20Brek-0A66C2?logo=linkedin)](https://linkedin.com/in/mohamed-brek-9130a6411)
