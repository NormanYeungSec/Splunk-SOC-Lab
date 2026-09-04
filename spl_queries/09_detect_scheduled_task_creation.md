\# Detect Scheduled Task Creation



\## Purpose



The goal of this search is to find when a scheduled task is created on the Windows Server.



Scheduled tasks are commonly used for normal administrative work, but attackers can also create them to run programs automatically or maintain access to a system.



\## Data Source



\- Windows Security Event Log

\- Event ID 4698 - Scheduled Task Creation



Windows Security Event ID 4698 is created when a new scheduled task is created.



\## SPL Query



```spl

index=main EventCode=4698

| table \_time Account\_Name Task\_Name ClientProcessId ParentProcessId ComputerName

| sort - \_time

```



\## What I Tested / Result



I created a test scheduled task named `LabTestTask` using the Administrator account.



The search returned one scheduled task creation event. The result showed `Administrator` creating `\\LabTestTask` on `LAB-DC01`.



\## Screenshot



!\[Scheduled task creation search results](../screenshots/detections/09\_detect\_scheduled\_task\_creation.png)

