# Detect PowerShell Execution

## Purpose

Detect PowerShell execution using Sysmon Process Create events.

## SPL Query

```spl
index=main PowerShell
```

## Result

This query returns PowerShell execution events collected by Sysmon and forwarded to Splunk.

## Screenshot

screenshots/06_spl_queries/28_detect_powershell.png
