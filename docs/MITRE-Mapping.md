# MITRE ATT&CK Mapping

## Overview
This document maps detection logic developed in this case study to the MITRE ATT&CK framework. The purpose is to provide standardized context for adversary behaviors and align detection engineering efforts with known threat techniques.

Mapping detections to ATT&CK helps improve visibility, identify coverage gaps, and ensure that defensive controls are aligned with real-world adversary tactics.

---

## Mapping Approach

Each detection is analyzed and mapped based on:

- The observed adversary behavior
- The closest matching ATT&CK technique
- The phase of the attack lifecycle (tactic)
- The available telemetry used for detection

Mappings are performed at the technique level when possible to ensure precision and relevance.

---

## Example Technique Mappings

### Initial Access
- **T1566 - Phishing**
  - Detection focus: Malicious email attachment execution or link-based payload delivery
  - Telemetry: Email logs, process execution, endpoint alerts

---

### Execution
- **T1059 - Command and Scripting Interpreter**
  - Detection focus: Execution of scripts via PowerShell, Bash, or command line interfaces
  - Telemetry: Process creation logs, command-line auditing

---

### Persistence
- **T1547 - Boot or Logon Autostart Execution**
  - Detection focus: Modifications to startup registry keys or scheduled tasks
  - Telemetry: Registry monitoring, scheduled task creation logs

---

### Privilege Escalation
- **T1068 - Exploitation for Privilege Escalation**
  - Detection focus: Attempts to exploit system vulnerabilities to gain elevated privileges
  - Telemetry: Security logs, exploit detection alerts

---

### Defense Evasion
- **T1070 - Indicator Removal on Host**
  - Detection focus: Log clearing, artifact deletion, or forensic evasion activity
  - Telemetry: Windows Event Logs, file system monitoring

---

### Credential Access
- **T1003 - OS Credential Dumping**
  - Detection focus: Accessing LSASS memory or credential dumping tools
  - Telemetry: Endpoint security logs, process injection alerts

---

### Discovery
- **T1082 - System Information Discovery**
  - Detection focus: Enumeration of system configuration, users, and network information
  - Telemetry: Command execution logs, endpoint monitoring

---

### Lateral Movement
- **T1021 - Remote Services**
  - Detection focus: Use of RDP, SMB, or SSH for lateral movement between systems
  - Telemetry: Authentication logs, network connection data

---

### Command and Control
- **T1071 - Application Layer Protocol**
  - Detection focus: HTTP/S or DNS-based communication to external command-and-control servers
  - Telemetry: Network traffic logs, proxy logs, DNS logs

---

### Exfiltration
- **T1041 - Exfiltration Over C2 Channel**
  - Detection focus: Data transfer through established command-and-control channels
  - Telemetry: Network flow logs, firewall logs

---

## Summary

MITRE ATT&CK mapping provides a structured framework for aligning detection engineering efforts with real-world adversary behaviors. It ensures that detections are contextualized, measurable, and aligned with industry-standard threat modeling practices.
