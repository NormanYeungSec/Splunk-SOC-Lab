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

- [x] Detect PowerShell Execution
- [x] Detect Command Prompt Execution
- [x] Detect Failed Logons (Event ID 4625)
- [ ] Detect Successful Logons (Event ID 4624)
- [ ] Detect Network Connections (Sysmon Event ID 3)
- [ ] Detect User Account Creation (Event ID 4720)
- [ ] Detect Administrator Group Changes (Event ID 4732)
- [ ] Detect Service Installation (Event ID 7045)
- [ ] Detect Scheduled Task Creation (Event ID 4698)
- [ ] Detect RDP Logons (Logon Type 10)
- [ ] Detect USB Device Connections (Event ID 6416)

---

## Phase 3 - Dashboards

- [ ] Authentication Dashboard
- [ ] Process Creation Dashboard
- [ ] PowerShell Activity Dashboard
- [ ] Windows Security Dashboard
- [ ] Network Connections Dashboard

---

## Phase 4 - Alerting

- [ ] Failed Login Alert
- [ ] PowerShell Execution Alert
- [ ] New User Account Alert
- [ ] Service Installation Alert
- [ ] Scheduled Task Alert

---

## Phase 5 - Incident Response

- [ ] Investigation #001 – Failed Login Activity
- [ ] Investigation #002 – Suspicious PowerShell Execution
- [ ] Investigation #003 – Unauthorized Account Creation
- [ ] Investigation #004 – Malicious Service Installation

---

## Phase 6 - Future Improvements

- [ ] Active Directory Integration
- [ ] Sysmon Configuration Tuning
- [ ] MITRE ATT&CK Mapping
- [ ] Sigma Rule Mapping
- [ ] Splunk Enterprise Security Integration
- [ ] Detection Automation
- [ ] Scheduled Reports
- [ ] Additional Attack Simulations