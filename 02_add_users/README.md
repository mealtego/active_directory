# 02 Automating add XYZ Users

1. Pre-requirements

```shell
$dc = New-PSSession 192.168.243.155 -Credential (Get-Credential)
Copy-Item .\ad_schema.json -ToSession $dc C:\Windows\Tasks
```