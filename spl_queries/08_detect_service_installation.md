\# Detect Service Installation



\## Purpose



The goal of this search is to find when a new Windows service is installed on the Windows Server.



Service installation can be normal administrative activity, but attackers can also create services to run programs or maintain access to a system.



\## Data Source



\- Windows System Event Log

\- Event ID 7045 - Service Installation



Windows Event ID 7045 is created when a new service is installed.



\## SPL Query



```spl

index=main EventCode=7045

| table \_time Service\_Name Service\_File\_Name Service\_Type Service\_Start\_Type Service\_Account ComputerName

| sort - \_time

```



\## What I Tested / Result



I created a test service named `LabTestService`.



The search returned one service installation event. The result showed the service pointing to `C:\\Windows\\System32\\cmd.exe`, using `LocalSystem`, and configured as a demand-start service on `LAB-DC01`.



\## Screenshot



!\[Service installation search results](../screenshots/detections/08\_detect\_service\_installation.png)

