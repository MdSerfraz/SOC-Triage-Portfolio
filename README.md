# SOC Triage Portfolio

This repository hosts verified network forensic investigation logs and triage reports compiled from live packet captures (PCAPs). Each artifact outlines explicit indicator signatures, transport layer tracking, and containment workflows applied during the response lifecycle.

## Forensic Case Index

### Case 01: NetSupport RAT System Compromise
- Affected Endpoint: 10.2.28.88
- C2 Destination: 45.131.214.85 (Port 443)
- Summary: Detected unauthorized persistence routines abusing the native Windows Background Intelligent Transfer Service (User-Agent: Microsoft BITS/7.8) to retrieve binary blocks under a masqueraded update path. Application stream tracking exposed continuous automated HTTP POST beacons targeting /fakeurl.htm.
- Remediation: Executed perimeter gateway null-routing against target external infrastructure, enforced logical network VLAN partitioning, and triggered remote process termination hooks via host execution controllers.

### Case 02: Lumma Info-Stealer Execution Trace
- Affected Endpoint: 10.1.21.58 (DESKTOP-ES9F3ML)
- C2 Destination: whitepepper.su (nginx/1.29.1)
- Summary: Triaged a validated credential-harvester framework utilizing emulated Google Chrome headers to obscure malicious traffic layers. TCP session tracking isolated an inbound JavaScript host profiler querying system dimensions, followed by encrypted form-urlencoded data exfiltration via POST commands to /api/set_agent. User identifier gwyatt was isolated through Kerberos authentication auditing.
- Remediation: Configured perimeter domain drop constraints for the malicious Top-Level Domain infrastructure, executed centralized directory token invalidations to force credential resets, and initiated volatile host memory cleanup.

### Case 03: Interlock Ransomware Backdoor Triage
- Affected Endpoint: 10.6.13.133 (DESKTOP-5AVE44C)
- C2 Destination: windows-msgas.com (Port 80)
- Summary: Tracked anomalous outbound web sequences directed at a malicious domain registered to look like legitimate native messaging utilities. Reconstructed directory validation traffic over the local segment to extract the explicit compromised employee account username rgaines from unencrypted Kerberos CName tokens.
- Remediation: Deployed strict perimeter boundary egress drop blocks, enacted account freeze routines within core Active Directory structures, and executed host segmentation rules to safeguard adjacent subnet hosts.

## Core Defensive Competencies
- Traffic Forensic Analysis: Packet parsing, protocol tree auditing, application layer stream carving, and custom display filtering inside Wireshark.
- Lifecycle Incident Response: Remote process orchestration, host network containment, and identity access token invalidation playbooks.
- Infrastructure Hardening: Threat telemetry hunting, endpoint registry cleanup, and security log parsing.
