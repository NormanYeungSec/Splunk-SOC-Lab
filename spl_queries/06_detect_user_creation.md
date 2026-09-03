\# Detect User Account Creation



\## Purpose



The goal of this search is to find when a new user account is created on the Windows Server.



Creating user accounts is normal administrative activity, but an unexpected account could also be a sign that someone is trying to gain or keep access to the system.



\## Data Source



\- Windows Security Event Log

\- Event ID 4720 - User Account Creation



Windows Security Event ID 4720 is created when a new user account is created.



\## SPL Query



```spl

index=main EventCode=4720

| eval Creator\_Account=mvindex(Account\_Name,0)

| eval New\_Account=mvindex(Account\_Name,1)

| table \_time Creator\_Account New\_Account ComputerName

| sort - \_time

```



\## What I Tested / Result



I created a test account named `LabTestUser` using the Administrator account.



The search returned one user creation event. The result showed `Administrator` as the account that created `LabTestUser` on `LAB-DC01`.



\## Screenshot



!\[User account creation search results](../screenshots/detections/06\_detect\_user\_creation.png)

