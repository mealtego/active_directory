 # 01 Installing the Domain Controller 


1. Use `sconfig` to:
    - Change the hostname
    - Change the IP address to static
    - Change the DNS server tp our own IP address

2.  Install the AD Windows Features

```shell
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
```

```
Get-NetIPAddress
```
```
Get-DnsClientServerAddress 
```

```
Set-DnsClientServerAddress  -InterfaceIndex {index} -ServerAddresses {ip.addr}
```

# Joining the Workstation to the domain 

```
Add-Computer -DomainName xyz.com - Credential xyz\Administrator -Force -Restart
```
