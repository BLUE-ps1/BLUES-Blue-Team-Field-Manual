# Detection Playbooks

## Suspicious PowerShell
Search for encoded or suspicious PowerShell invocations.
Example Splunk query (Sysmon):
```
index=main sourcetype="XmlWinEventLog:Microsoft-Windows-Sysmon/Operational" EventCode=1 Image="*\powershell.exe"
| search CommandLine="*-enc*" OR CommandLine="*-nop*"
```

## New Scheduled Tasks
Watch for schtasks.exe process creates in Sysmon.
