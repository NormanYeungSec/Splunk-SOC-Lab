# Splunk SOC Lab Roadmap

Completed setup work is recorded in the [lab journal](Lab-Journal.md) and the [screenshot collection](../screenshots/README.md).

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

- [x] [Detect Failed Logons (Event ID 4625)](../spl_queries/03_detect_failed_logon.md)
- [x] Detect Successful Logons (../spl_queries/04_detect_successful_logon.md)
- [ ] Detect RDP Logons (Logon Type 10)

### Process Execution

- [x] [Detect PowerShell Execution](../spl_queries/01_detect_powershell.md)
- [x] [Detect Command Prompt Execution](../spl_queries/02_detect_cmd.md)

### Account & Privilege Changes

- [x] Detect User Account Creation (../spl_queries/06_detect_user_creation.md)
- [x] Detect Administrator Group Changes (../spl_queries/07_detect_admin_group_change.md)

### Persistence

- [x] Detect Service Installation (../spl_queries/08_detect_service_installation.md)
- [x] Detect Scheduled Task Creation (../spl_queries/09_detect_scheduled_task_creation.md)

### Network / Device Activity

- [x] Detect Network Connections (../spl_queries/05_detect_network_connection.md)
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
