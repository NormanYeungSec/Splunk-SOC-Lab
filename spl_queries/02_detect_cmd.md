# Detect Command Prompt Execution

## Purpose

Detect Command Prompt execution using Sysmon events.

## SPL Query

```spl
index=main cmd.exe
```

## Result

Displays Command Prompt execution events collected by Sysmon.

## Screenshot

screenshots/06_spl_queries/29_detect_cmd.png
