# active-directory-monitoring

A security operations center (SOC) lab demonstrating Wazuh SIEM integration with Active Directory for log monitoring and threat detection.

Project Overview:

This project demonstrates the setup of a Security Operations Center (SOC) lab environment. It integrates Active Directory (AD) on Windows Server with Wazuh SIEM to monitor, collect, and analyze security event logs, user management activities, and potential threats in real-time.

Tools & Technologies Used:

SIEM / XDR Solution: Wazuh SIEM

Directory Services: Active Directory (AD), Windows Server 2022

Endpoints: Windows 10, Kali Linux (for security testing)

Frameworks & Concepts: MITRE ATT&CK, Vulnerability Detection, Event ID Analysis

Step-by-Step Implementation & Configuration:
1. Active Directory Setup & User Management:
   
Configured Active Directory Domain Services (actived.com) on Windows Server and created organizational units and user accounts.
Screenshot:
![User Created Screenshot](userCreated.jpeg)

3. Group Policy Object (GPO) Audit Configuration:
   
Enabled advanced audit policies (Audit User Account Management set to Success and Failure) to capture security event logs effectively.
Screenshot:
![GPO Configuration](GPO.jpeg)

3.Log Forwarding & Wazuh Agents Deployment:

Configured Wazuh agents to securely forward Windows security event logs to the central SIEM server, connecting Windows Server and Windows 10 endpoints as active agents to the Wazuh SIEM dashboard.
   Screenshot:
![Windows Setup](windowS.jpeg)

Security Event Log Analysis (Wazuh Dashboard):

The Wazuh SIEM successfully collected and monitored crucial Windows Security Event IDs:

Event ID 4720 (User Account Created):
      Screenshot: ![Event 4720](eventid4720.jpeg)

Event ID 4625 (Failed Logon Attempt):
         Screenshot:![Event 4720](eventId4625.jpeg)

Event ID 4624 (Successful Logon):
         Screenshot: ![Event 4624](eventid4624.jpeg)

Event ID 4738 (User Account Modified):
           Screenshot:![Event 4738](eventid4738.jpeg)

Threat Intelligence & Vulnerability Detection:
  
  MITRE ATT&CK Integration: 
  Mapped security alerts to tactics and techniques.
    Screenshot: ![MITRE ATT&CK](mitre.jpeg)

Vulnerability Assessment: 
Scanned connected endpoints for system vulnerabilities, misconfigurations, and CVEs.
  Screenshot:![Vulnerability Detection](vdetection.jpeg)

Detection Rules
The following Windows Security Event IDs were monitored and analyzed using Wazuh SIEM to detect user activities and potential security threats.

*Detection Rules

| Event ID | Detection                |
|----------|--------------------------|
| 4624     | Successful Logon         |
| 4625     | Failed Logon             |
| 4720     | New User Created         |
| 4738     | User Account Modified    |
| 4726     | User Deleted             |

 MITRE ATT&CK Mapping:
The detected security events were mapped to the MITRE ATT&CK Framework to understand attacker tactics and techniques.

| Event ID | MITRE ATT&CK Technique        |
|----------|------------------------       |
| 4625     | T1110 – Brute Force           |
| 4720     | T1136 – Create Account        |
| 4738     | T1098 – Account Manipulation  |

Skills Demonstrated
This project helped me gain hands-on experience in the following areas:

- Active Directory Administration
- Windows Server 2022
- Group Policy Management
- Wazuh SIEM
- Windows Event Logs
- Threat Detection
- Incident Monitoring
- Log Analysis
- MITRE ATT&CK Framework
- SOC Analyst Skills
- Vulnerability Assessment
- Security Monitoring

Learning Outcomes:
During this project, I learned and practiced the following concepts:

-Active Directory Deployment
-Group Policy (GPO) Configuration
-Windows Security Event Monitoring
-Wazuh SIEM Deployment
-Wazuh Agent Installation and Configuration
-Threat Detection and Monitoring
-Windows Log Analysis
-MITRE ATT&CK Mapping
-SOC Monitoring Workflow
-Incident Investigation Process

Challenges Faced:
While implementing this project, I encountered several challenges:

- Configuring Windows Event Forwarding
- Deploying and Registering Wazuh Agents
- Troubleshooting Agent Connectivity Issues
- Fine-tuning Windows Audit Policies
- Understanding Windows Security Event IDs

Future Improvements:
This project can be further enhanced by implementing the following features:

- Integrate Sysmon for advanced endpoint monitoring
- Add Sigma Detection Rules
- Configure Active Response Automation
- Enable Email Alerting
- Implement Ransomware Detection
- Create Brute Force Detection Rules

Conclusion:

This lab successfully showcases centralized log management, threat detection, and Active Directory auditing using an open-source SIEM tool like Wazuh, mirroring real-world SOC operations.
