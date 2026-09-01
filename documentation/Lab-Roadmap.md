# Splunk SOC Lab Roadmap

---

## Phase 1 - Lab Setup

- [x] Create GitHub repository
- [x] Create project folder structure
- [x] Install Oracle VirtualBox
- [x] Download Windows Server 2022 Evaluation ISO
- [x] Create Windows Server 2022 Virtual Machine
- [x] Install Windows Server 2022
- [x] Configure Windows Server
- [x] Install Splunk Enterprise
- [x] Install Splunk Universal Forwarder
- [x] Configure Splunk to receive forwarded events (Port 9997)
- [x] Install Sysmon (SwiftOnSecurity configuration)
- [x] Configure `inputs.conf`
- [x] Verify Windows Security logs are indexed
- [x] Verify Sysmon logs are indexed
- [x] Install Splunk Add-on for Sysmon

---

## Phase 2 - Detection Engineering

### Authentication
- [x] Detect Failed Logons (Event ID 4625)
- [ ] Detect Successful Logons (Event ID 4624)
- [ ] Detect RDP Logons (Logon Type 10)

### Process Execution
- [x] Detect PowerShell Execution
- [x] Detect Command Prompt Execution

### Account & Privilege Changes
- [ ] Detect User Account Creation (Event ID 4720)
- [ ] Detect Administrator Group Changes (Event ID 4732)

### Persistence
- [ ] Detect Service Installation (Event ID 7045)
- [ ] Detect Scheduled Task Creation (Event ID 4698)

### Network / Device Activity
- [ ] Detect Network Connections (Sysmon Event ID 3)
- [ ] Detect USB Device Connections (Event ID 6416)

### Correlation Detections
- [ ] Detect Multiple Failed Logons Followed by Successful Logon
- [ ] Detect New User Added to Administrators Group
- [ ] Detect PowerShell Followed by Suspicious Network Connection

---

## Phase 3 - Detection Rule Documentation

- [ ] Create standardized detection rule template
- [ ] Convert completed SPL searches into documented detection rules
- [ ] Document data source
- [ ] Document Event ID / Sysmon Event ID
- [ ] Document SPL query
- [ ] Document false positives
- [ ] Document investigation steps
- [ ] Document MITRE ATT&CK mapping

---

## Phase 4 - Dashboards

- [ ] Authentication Dashboard
- [ ] Process Creation Dashboard
- [ ] PowerShell Activity Dashboard
- [ ] Windows Security Dashboard
- [ ] Network Connections Dashboard

---

## Phase 5 - Alerting

- [ ] Failed Login Alert
- [ ] Suspicious PowerShell Alert
- [ ] New User Account Alert
- [ ] Administrator Group Change Alert
- [ ] Service Installation Alert
- [ ] Scheduled Task Alert

---

## Phase 6 - Attack Simulations

- [ ] Simulate Failed Login Activity
- [ ] Simulate Successful Login After Multiple Failures
- [ ] Simulate PowerShell Execution
- [ ] Simulate New User Creation
- [ ] Simulate Administrator Group Modification
- [ ] Simulate Service Installation
- [ ] Simulate Scheduled Task Creation

---

## Phase 7 - Incident Response

- [ ] Investigation #001 - Failed Login Activity
- [ ] Investigation #002 - Suspicious PowerShell Execution
- [ ] Investigation #003 - Unauthorized Account Creation
- [ ] Investigation #004 - Malicious Service Installation
- [ ] Investigation #005 - Suspicious Authentication Sequence

---

## Phase 8 - Future Improvements

- [ ] Active Directory Integration
- [ ] Sysmon Configuration Tuning
- [ ] Additional Windows Event Sources
- [ ] MITRE ATT&CK Mapping
- [ ] Sigma Rule Mapping
- [ ] Splunk Enterprise Security Integration
- [ ] Detection Automation
- [ ] Scheduled Reports
- [ ] Additional Attack Simulations