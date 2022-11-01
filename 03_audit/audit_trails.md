# Powershell commands to trail suspicious activity

```bash=1
#list all events from Security that contain EntryType:FailureAuidt
Get-EventLog Security -after (get-date).addminutes(-5) | where EntryType  -eq FailureAudit | format-list *
```