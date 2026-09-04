\# Detect RDP Logon



\## Purpose



The goal of this search is to find successful Remote Desktop logons to the Windows Server.



Remote Desktop is commonly used for legitimate administration, but unexpected RDP activity can also be a sign that someone is remotely accessing a system.



\## Data Source



\- Windows Security Event Log

\- Event ID 4624 - Successful Logon

\- Logon Type 10 - RemoteInteractive



A successful Remote Desktop login creates Event ID 4624 with Logon Type 10.



\## SPL Query



```spl

index=main EventCode=4624 Logon\_Type=10

| eval RDP\_Account=mvindex(Account\_Name,1)

| table \_time RDP\_Account Logon\_Type Logon\_Process Authentication\_Package Source\_Network\_Address Workstation\_Name ComputerName

| sort - \_time

```



\## What I Tested / Result



I connected to `LAB-DC01` using Remote Desktop from my host computer.



The search returned one successful RDP logon event. The result showed the `Administrator` account logging in with Logon Type 10 from `10.0.2.2`.



\## Screenshot



!\[RDP logon search results](../screenshots/detections/10\_detect\_rdp\_logon.png)

