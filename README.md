# SOC Triage and Detection Engineering Portfolio

This repository hosts a verified collection of network forensic investigation logs, host-level security audits, and automated detection rule baselines compiled from live incident captures. Each artifact outlines explicit indicator signatures, transport layer tracking, kernel process auditing parameters, and mitigation playbooks applied across the enterprise defense lifecycle.

## Investigation and Detection Index

### Domain 1: Deep Packet Inspection and Network Forensics

### Case 01: NetSupport RAT System Compromise
- Log Resource: Case_01_NetSupport_RAT.txt
- Affected Endpoint: 10.2.28.88 (DESKTOP-TEYQ2NR) | User: brolf
- Analysis Summary: Triaged a host compromise where the threat actor hijacked the native Windows Background Intelligent Transfer Service (User-Agent: Microsoft BITS/7.8) to retrieve malicious binary blocks. Session reconstruction isolated automated outbound HTTP POST beaconing targeting /fakeurl.htm on external C2 infrastructure 45.131.214.85.
- Mitigation Playbook: Executed perimeter gateway egress blocks, initiated logical network VLAN partitioning, and deployed remote host process termination workflows.

### Case 02: Lumma Info-Stealer Execution Trace
- Log Resource: Case_02_Lumma_stealer.txt
- Affected Endpoint: 10.1.21.58 (DESKTOP-ES9F3ML) | User: gwyatt
- Analysis Summary: Isolated an active credential harvester utilizing an emulated Google Chrome User-Agent header string to bypass perimeter boundary filters. Reconstructed TCP application handshakes to uncover an inbound JavaScript host profiler querying machine hardware concurrency configurations and browser directories, followed by immediate encrypted form-urlencoded data exfiltration to whitepepper.su.
- Mitigation Playbook: Configured boundary domain drops for the malicious Top-Level Domain (.su), implemented centralized directory token invalidations to force global session resets, and cleared local application data cache arrays.

### Case 03: Interlock Ransomware Backdoor Triage
- Log Resource: Case_03_Interlock_Ransomware.txt
- Affected Endpoint: 10.6.13.133 (DESKTOP-5AVE44C) | User: rgaines
- Analysis Summary: Tracked automated HTTP POST communication targeting a spoofed external domain (windows-msgas.com) registered to replicate standard Windows utilities. Parsed unencrypted Kerberos directory authentication streams (kerberos.CNameString) directly over the local network layer to isolate the explicit compromised employee account identity.
- Mitigation Playbook: Enforced perimeter network drop rules, implemented immediate user profile locks within core Active Directory structures, and executed host segmentation parameters.

### Domain 2: Host Forensics and Detection Engineering

### Case 04: Windows Security Auditing Framework
- Log Resource: Case_04_Windows_Event_Logs.txt
- Analysis Summary: Established a core matrix for tracking critical Windows Security and System Event Identifiers across the corporate domain structure. Documented explicit telemetry analysis markers for mapping Successful Logons (Event ID 4624 - Logon Types 2, 3, and 10), Brute-Force velocity indicators (Event ID 4625), Backdoor Account Creation anomalies (Event ID 4720), and malicious Registry Persistence hooks via system service creation (Event ID 7045).

### Case 05: Advanced System Monitor (Sysmon) Tracking
- Log Resource: Case_05_Sysmon_Tracking.txt
- Analysis Summary: Structured a host-level hunting baseline focused on the analysis of deep process manipulation and kernel actions. Isolated evaluation procedures targeting Process Creation telemetry (Event ID 1 for command-line string arguments), Network Connection Tracking (Event ID 3 for non-browser binaries establishing socket states), Image Loading manipulation (Event ID 7 for DLL sideloading detection), and volatile File Write operations (Event ID 11 inside temporary pathways).

### Case 06: Sigma Rule Signature Automation
- Log Resource: Case_06_Sigma_Detection_Rules.txt
- Analysis Summary: Engineered a vendor-neutral, production-grade Sigma detection rule configured to track malicious shell actions inside the enterprise. The rule logic automates the log parsing engines across Sysmon Event ID 1 datasets to intercept PowerShell spawning strings executing with hidden window parameters, stripped profiles, and bypassed local execution policy constraints.

### Domain 3: Linux Architecture and Cloud Environment Security

### Case 07: Linux SSH and Authentication Auditing
- Log Resource: Case_07_Linux_SSH_Auditing.txt
- Analysis Summary: Structured an auditing baseline targeting native Linux authentication logs (/var/log/auth.log) to track remote intrusion vectors. Isolated signature tracking telemetry for detecting brute-force password spraying campaigns, unauthorized privileged remote root logons, and localized administrative shell escalation sequences via sudo override executions.

### Case 08: Web Server Logs & Web Shell Hunting
- Log Resource: Case_08_Linux_Web_Shell_Hunting.txt
- Analysis Summary: Outlined an incident response framework for detecting persistent web application backdoors inside Apache and Nginx access logs. Configured tracking playbooks for identifying anomalous HTTP POST behaviors inside non-executable upload directories, tracing explicit remote command execution (RCE) URL arguments, and tracking process trees running under server daemon accounts (www-data).

### Case 09: Linux Syslog Signature Engineering
- Log Resource: Case_09_Linux_Detection_Rules.txt
- Analysis Summary: Designed an automated, vendor-neutral Linux Sigma rule targeting auditd/syslog engines. The alerting logic systematically intercepts low-privilege web daemon service accounts (www-data, apache, nginx) attempting to spawn interactive command shells (/bin/bash, /bin/sh), providing instantaneous alerting and containment options for active web server compromises.

## Core Technical Competencies
- Traffic Forensic Analysis: Deep packet parsing, protocol hierarchy auditing, stream reconstruction, and display filter tuning inside Wireshark.
- Host-Level Inspection: Windows Security log auditing, Sysmon telemetry monitoring, Linux auth.log parsing, process tree mapping, and registry persistence hunting.
- SIEM & Detection Engineering: Creating vendor-neutral Sigma signatures, tracking indicator attributes, and constructing technical remediation playbooks.
