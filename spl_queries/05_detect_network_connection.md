\# Detect Network Connection



\## Purpose



The goal of this search is to find network connections recorded by Sysmon on the Windows Server.



Network connections are normal activity, but they can also be useful during an investigation. Seeing which process connected to an IP address and which port it used can help identify unusual or suspicious activity.



\## Data Source



\- Sysmon

\- Event ID 3 - Network Connection



Sysmon Event ID 3 is created when a process makes a network connection.



\## SPL Query



```spl

index=main EventCode=3

| table \_time User Image Protocol SourceIp SourcePort DestinationIp DestinationHostname DestinationPort DestinationPortName

| sort - \_time

```



\## What I Tested / Result



I used PowerShell to make a TCP connection to `8.8.8.8` on port `443`.



The search returned one network connection event. The result showed `powershell.exe` connecting from `10.0.2.15` to `8.8.8.8` using TCP on port `443`.



\## Screenshot



!\[Network connection search results](../screenshots/detections/05\_detect\_network\_connection.png)

