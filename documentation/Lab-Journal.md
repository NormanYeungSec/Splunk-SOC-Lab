# Lab Journal

---

## Day 1 — July 12, 2026

### Goal

Build the foundation for a home SOC lab using Windows Server 2022, VirtualBox, and Splunk Enterprise.

### Completed

- Created the Splunk-SOC-Lab GitHub repository.
- Designed the repository structure.
- Created project documentation.
- Created the lab roadmap.
- Installed Oracle VirtualBox.
- Downloaded the Windows Server 2022 Evaluation ISO.
- Created a Windows Server 2022 virtual machine.
- Configured the VM (6 GB RAM, 2 vCPUs, 80 GB virtual disk).
- Installed Windows Server 2022 Desktop Experience.
- Renamed the server to **LAB-DC01**.
- Captured installation screenshots.

### Challenges

**Issue**

VirtualBox displayed a black screen after rebooting the server.

**Resolution**

Performed **Machine → Reset** in VirtualBox.

### Lessons Learned

- Use descriptive hostnames.
- Machine Reset can recover from temporary VirtualBox boot issues.

### Next Objectives

- Install VirtualBox Guest Additions.
- Configure networking.
- Install Splunk Enterprise.

---

## Day 2 — July 13, 2026

### Goal

Improve the usability of the Windows Server virtual machine before installing security tools.

### Completed

- Installed VirtualBox Guest Additions.
- Enabled dynamic display resizing.
- Enabled shared clipboard.
- Improved mouse integration between the host and guest.
- Restarted the virtual machine.
- Captured Guest Additions installation screenshots.

### Lessons Learned

- Guest Additions significantly improves the virtual machine experience.
- Dynamic display resizing and shared clipboard make administration much easier.
- Installing Guest Additions early saves time during the rest of the lab.

### Next Objectives

- Configure networking.
- Install Splunk Enterprise.
- Install Splunk Universal Forwarder.
- Install Sysmon.
