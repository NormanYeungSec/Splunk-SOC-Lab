# Detect Failed Logon

## Purpose

Detect failed Windows logon attempts using Windows Security Event ID 4625.

## SPL Query

```spl
index=main source="WinEventLog:Security" EventCode=4625
```

## Result

This query returns failed Windows logon attempts from the Security event log. Failed logons are useful for detecting password guessing, brute-force attacks, and unauthorized access attempts.

## Screenshot

screenshots/08_failed_logon/32_failed_logon_detection.png
