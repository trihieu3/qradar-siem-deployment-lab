# qradar-siem-deployment-lab
1. Lab Overview
This hands-on lab is designed to guide users through deploying and integrating several security devices into IBM QRadar SIEM.
The lab includes:
- Palo Alto Firewall
- Windows Endpoint (Windows 10)
- Windows Server 2016
- Local Web Server
The main objective of this lab is to demonstrate how QRadar collects, parses, and correlates security events to detect potential threats from the internet.

2. Lab Objectives
After completing this lab, users will be able to:
- Collect security event logs from different log sources
- Parse and normalize events in QRadar
- Create detection rules to generate offenses for security analysts

3. Lab Architecture

The lab environment consists of the following components:
- IBM QRadar SIEM
- Windows Endpoint and Windows Server 2016
- Palo Alto Firewall
- Web Application protected by WAF
- All devices send logs to QRadar using supported log collection methods.

4. Step-by-Step Lab Implementation

Step 1: Log Source Collection
In this step, QRadar is configured to collect logs from multiple security devices.
Log Sources included:
- Windows Event Logs (Security, System, Application)
- Palo Alto Firewall Events
- Web Application Firewall (WAF) Events
Log sources are added in QRadar using the appropriate log source type and protocol (Syslog or WinCollect).

Step 2: Log Parsing and Normalization
After logs are collected, QRadar parses incoming events based on the log source type.
Parsing helps QRadar extract important fields such as source IP, destination IP, username, and event type Correct log source selection ensures accurate parsing
Parsed events are automatically normalized into QRadar event categories
Proper parsing is critical for effective rule creation and threat detection.

Step 3: Detection Rules and Offense Generation
In this step, correlation rules are created in QRadar to detect suspicious or malicious activities.
Examples of detection rules:
- Multiple failed login attempts from external IP addresses
- Web attacks detected by WAF (SQL Injection, XSS)
- Malicious traffic blocked by Palo Alto Firewall
When rule conditions are met, QRadar generates offenses to alert SOC analysts for investigation.

5. Conclusion
This hands-on lab demonstrates a complete QRadar SIEM workflow, from log collection to threat detection.
By integrating firewall, endpoint, and web security logs, QRadar provides centralized visibility and improves security monitoring capabilities.
