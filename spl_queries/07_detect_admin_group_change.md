\# Detect Administrator Group Change



\## Purpose



The goal of this search is to find when an account is added to a local security group on the Windows Server.



Changes to the Administrators group are important because adding an account to this group gives it elevated privileges. An unexpected change could be worth investigating.



\## Data Source



\- Windows Security Event Log

\- Event ID 4732 - Member Added to Local Security Group



Windows Security Event ID 4732 is created when a member is added to a security-enabled local group.



\## SPL Query



```spl

index=main EventCode=4732

| eval Changed\_By=mvindex(Account\_Name,0)

| eval Added\_Member\_SID=mvindex(Security\_ID,1)

| table \_time Changed\_By Added\_Member\_SID Group\_Name ComputerName

| sort - \_time

```



\## What I Tested / Result



I added `LabTestUser` to the local Administrators group using the Administrator account.



The search returned one Event ID 4732 event. The result showed `Administrator` making the change and adding a member with a SID ending in `-1000` to the `Administrators` group on `LAB-DC01`.



I verified separately that this SID belonged to `LabTestUser`.



\## Screenshot



!\[Administrator group change search results](../screenshots/detections/07\_detect\_admin\_group\_change.png)

