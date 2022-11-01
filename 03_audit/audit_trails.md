# Powershell commands to trail suspicious activity

```
Get-EventLog Security -after (get-date).addminutes(-5) | where EntryType  -eq FailureAudit | format-list *
```