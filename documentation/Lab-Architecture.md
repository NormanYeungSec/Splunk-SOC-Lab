# Lab Architecture

## Current Setup

- Windows 11 host
  - Oracle VirtualBox
    - Windows Server 2022 virtual machine (`LAB-DC01`)
      - Splunk Enterprise
      - Splunk Universal Forwarder
      - Sysmon with the SwiftOnSecurity configuration
      - Splunk Add-on for Sysmon

## Planned Expansion

- Configure the Windows Server as a domain controller.
- Add a Windows 11 client.
- Collect additional Windows and Sysmon events in Splunk.
- Build dashboards and alerts from the collected data.
