# Splunk SOC Lab

## Overview

This repository documents my home SOC lab. I use Splunk Enterprise, Windows event logs, and Sysmon to collect data and test simple detection searches.

## Current Lab

- Windows 11 host
- Oracle VirtualBox
- Windows Server 2022 virtual machine (`LAB-DC01`)
- Splunk Enterprise
- Splunk Universal Forwarder
- Sysmon with the SwiftOnSecurity configuration
- Splunk Add-on for Sysmon

## Detection Searches

- [Detect PowerShell Execution](spl_queries/01_detect_powershell.md)
- [Detect Command Prompt Execution](spl_queries/02_detect_cmd.md)
- [Detect Failed Logons](spl_queries/03_detect_failed_logon.md)

## Documentation

- [Lab Architecture](documentation/Lab-Architecture.md)
- [Lab Journal](documentation/Lab-Journal.md)
- [Lab Roadmap](documentation/Lab-Roadmap.md)
- [Screenshot Guide](screenshots/README.md)

## Current Status

The basic lab setup is complete, and three detection searches are documented. The remaining work is tracked in the [lab roadmap](documentation/Lab-Roadmap.md).
