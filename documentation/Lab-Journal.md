# Lab Journal

---

## Day 1

### Completed

- Created the GitHub repository.
- Created the project structure.
- Created the project documentation and roadmap.
- Installed Oracle VirtualBox.
- Downloaded the Windows Server 2022 Evaluation ISO.
- Created a Windows Server 2022 virtual machine.
- Configured the VM (6 GB RAM, 2 CPUs, 80 GB disk).
- Installed Windows Server 2022 Desktop Experience.
- Renamed the server to **LAB-DC01**.
- Captured setup screenshots.

### Challenges

- VirtualBox showed a black screen after restarting.
- Fixed the issue by using **Machine → Reset** in VirtualBox.

---

## Day 2

### Completed

- Installed VirtualBox Guest Additions.
- Enabled dynamic screen resizing.
- Enabled shared clipboard.
- Improved mouse integration.
- Installed Splunk Enterprise.
- Created the Splunk administrator account.
- Verified the Splunk web interface.
- Logged into the Splunk dashboard.
- Installed Splunk Universal Forwarder.
- Enabled receiving on port **9997**.
- Installed Sysmon using the SwiftOnSecurity configuration.
- Created the `inputs.conf` file.
- Restarted the Universal Forwarder.
- Verified Sysmon events were successfully sent to Splunk.
- Captured installation and verification screenshots.
